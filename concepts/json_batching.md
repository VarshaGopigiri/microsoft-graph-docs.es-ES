# <a name="combine-multiple-requests-in-one-http-call-using-json-batching-preview"></a>Combinación de varias solicitudes en una llamada HTTP mediante el procesamiento por lotes de JSON (versión preliminar)

El procesamiento por lotes de JSON le permite optimizar la aplicación mediante la combinación de varias solicitudes en un solo objeto JSON. Por ejemplo, un cliente desea crear una vista de datos no relacionados, como:

1. Una imagen almacenada en OneDrive
2. Una lista de tareas de Planner
3. El calendario de un grupo

La combinación de estas tres solicitudes individuales en una sola solicitud por lotes puede ahorrarle a la aplicación una importante latencia de red.

## <a name="first-json-batch-request"></a>Primera solicitud por lotes JSON

En primer lugar, se construye la solicitud por lotes JSON para el ejemplo anterior. En este escenario, las solicitudes individuales no son interdependientes de ningún modo y, por lo tanto, se pueden colocar en la solicitud por lotes en cualquier orden.

```http
POST https://graph.microsoft.com/beta/$batch
Accept: application/json
Content-Type: application/json
```

```json
{
  "requests": [
    {
      "id": "1",
      "method": "GET",
      "url": "/me/drive/root:/{file}:/content"
    },
    {
      "id": "2",
      "method": "GET",
      "url": "/me/planner/tasks"
    },
    {
      "id": "3",
      "method": "GET",
      "url": "/groups/{id}/events"
    },
    {
      "id": "4",
      "url": "/me",
      "method": "PATCH",
      "body": {
        "city" : "Redmond"
      },
      "headers": {
        "Content-Type": "application/json"
      }
    }
  ]
}
```

Las respuestas a las solicitudes por lotes pueden aparecer en otro orden. La propiedad `id` puede utilizarse para poner en correlación las respuestas y solicitudes individuales.

```http
200 OK
Content-Type: application/json
```

```json
{
  "responses": [
    {
      "id": "1",
      "status": 302,
      "headers": {
        "location": "https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi"
      }
    },
    {
      "id": "3",
      "status": 401,
      "body": {
        "error": {
          "code": "Forbidden",
          "message": "..."
        }
      }
    },
    {
      "id": "2",
      "status": 200,
      "body": {
        "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.plannerTask)",
        "value": []
      }
    },
    {
      "id": "4",
      "status": 204,
      "body": null
    }
  ]
}
```

## <a name="request-format"></a>Formato de solicitud

Las solicitudes por lotes se envían siempre mediante el método `POST` al punto de conexión `/$batch`.

Un cuerpo de solicitud por lotes JSON consta de un único objeto JSON con una propiedad necesaria: `requests`. La propiedad `requests` es una matriz de solicitudes individuales. Para cada solicitud individual, las propiedades `id`, `method` y `url` son necesarias.

La propiedad `id` funciona principalmente como un valor de correlación para asociar las respuestas individuales a las solicitudes. Esto permite que el servidor procese las solicitudes en el lote en el orden más eficaz.

Las propiedades `method` y `url` son exactamente lo que vería al principio de cualquier solicitud HTTP determinada. El método es el método HTTP y la dirección URL es la URL de recurso a la que normalmente se enviaría la solicitud individual.

Opcionalmente, las solicitudes individuales también contienen una propiedad `headers` y una propiedad `body`. Ambas propiedades normalmente son objetos JSON, tal y como se muestra en el ejemplo anterior. En algunos casos, `body` puede ser un valor de dirección URL codificada en base64 en lugar de un objeto JSON, por ejemplo, cuando el cuerpo es una imagen. Cuando se incluye un `body` con la solicitud, el objeto `headers` debe contener un valor para `Content-Type`.

## <a name="response-format"></a>Formato de respuesta

El formato de respuesta para las solicitudes por lotes JSON es similar al formato de solicitud. Estas son las diferencias clave:

* La propiedad en el objeto principal JSON se denomina `responses` como contraposición a `requests`.
* Las respuestas individuales pueden aparecer en un orden diferente a las solicitudes.
* En lugar de `method` y `url`, las respuestas individuales tienen una propiedad `status`. El valor de `status` es un número que representa el código de estado HTTP.

Normalmente, el código de estado en una respuesta por lotes es `200` o `400`. Si la propia solicitud por lotes tiene un formato incorrecto, el código de estado es `400`. Si la solicitud por lotes se puede analizar, el código de estado es `200`. Un código de estado `200` en la respuesta por lotes no indica que las solicitudes individuales comprendidas en el lote se hayan realizado correctamente. Por ello, cada respuesta individual en la propiedad `responses` tiene un código de estado.

Además de la propiedad `responses`, podría haber una propiedad `nextLink` en la respuesta por lotes. Esto permite a Microsoft Graph devolver una respuesta por lotes tan pronto como cualquiera de las solicitudes individuales se haya completado. Para asegurarse de que se recibieron todas las respuestas individuales, siga el `nextLink` en caso de que exista.

## <a name="sequencing-requests-with-the-dependson-property"></a>Secuenciar solicitudes con la propiedad dependsOn

Las solicitudes individuales se pueden ejecutar en un orden especificado mediante la propiedad `dependsOn`. Esta propiedad es una matriz de cadenas que hace referencia al `id` de otra solicitud individual. Por este motivo, los valores de `id` deben ser únicos. Por ejemplo, en la siguiente solicitud, el cliente especifica que las solicitudes 1 y 3 se deben ejecutar en primer lugar, luego la solicitud 2 y luego la 4.

```json
{
  "requests": [
    {
      "id": "1",
      "method": "GET",
      "url": "..."
    },
    {
      "id": "2",
      "dependsOn": [ "1" ],
      "method": "GET",
      "url": "..."
    },
    {
      "id": "3",
      "method": "GET",
      "url": "..."
    },
    {
      "id": "4",
      "dependsOn": [ "2" ],
      "method": "GET",
      "url": "..."
    }
  ]
}
```

Si se produce un error en una solicitud individual, cualquier solicitud que dependa de dicha solicitud producirá un error con código de estado `424` (dependencia errónea).

## <a name="bypassing-url-length-limitations-with-batching"></a>Omitir las limitaciones de longitud de URL con el procesamiento por lotes

Un caso de uso adicional para el procesamiento por lotes de JSON es omitir las limitaciones de longitud de dirección URL. En los casos donde la cláusula de filtro es compleja, la longitud de la dirección URL podría superar las limitaciones integradas en los navegadores u otros clientes HTTP. Puede utilizar el procesamiento por lotes de JSON como solución alternativa para ejecutar estas solicitudes porque la longitud de la URL simplemente pasa a formar parte de la carga de la solicitud.

## <a name="known-issues"></a>Problemas conocidos

Para obtener una lista de las limitaciones actuales relacionadas con el procesamiento por lotes, consulte [problemas conocidos][batching-known-issues].

[batching-known-issues]: https://developer.microsoft.com/en-us/graph/docs/concepts/known_issues#json-batching
[odata-4.01-json]: https://www.oasis-open.org/committees/download.php/60365/odata-json-format-v4.01-wd02-2017-03-24.docx


## <a name="see-also"></a>Consulte también

Para obtener más información sobre el formato de solicitud o respuesta por lotes JSON, consulte la [especificación OData JSON, versión de formato 4.01][odata-4.01-json], sección 18. Tenga en cuenta que actualmente esta especificación es un borrador, pero no se espera que cambie.

