# <a name="security-api-error-responses"></a>Respuestas de error de la API de seguridad

Los errores en la API de seguridad en Microsoft Graph se devuelven mediante códigos de estado HTTP estándar y se entregan por medio de un encabezado de advertencia.

La API de seguridad es un servicio federado que recibe varias respuestas de todos los proveedores de datos. Cuando la API de seguridad recibe un error HTTP, devolverá un encabezado de advertencia con el siguiente formato: <!-- { "blockType": "ignored" } -->

```http
{Vendor}/{Provider}/{StatusCode}/{LatencyInMs}
```

Este encabezado de advertencia sólo se envía a los clientes cuando uno de los proveedores de datos devuelve un código de error que no sea 2xx o 404. Por ejemplo:

- Es posible que se devuelva HttpStatusCode.Forbidden (403) si no se ha concedido el acceso al recurso.
- Si un proveedor excede el tiempo espera, se devuelve HttpStatusCode.GatewayTimeout (504) en el encabezado de advertencia.
- Si se produce un error interno del proveedor, se usa HttpStatusCode.InternalServerError (500) en el encabezado de advertencia.

Si un proveedor de datos devuelve 2xx o 404, no se muestra en el encabezado de advertencia debido a que estos códigos se preven, respectivamente, cuando el resultado es correcto o cuando no se han encontrado datos. En un sistema federado, se prevé un error 404 de no encontrado tantas veces como los datos solo los conozcan uno o varios proveedores, pero no todos.

## <a name="example"></a>Ejemplo

Un usuario solicita `security/alerts/{alert_id}`.

    Provider 1: 404 (provider does not have a record of this alert ID)
    Provider 2: 504 (provider timed out)
    Provider 3: 200 (success)
    Provider 4: 403 (customer has not licensed this provider)

Dado que 404 y 200 son las condiciones previstas, el encabezado de advertencia contiene lo siguiente: 

```HTTP
Warning : 199 - "{Vendor2}/{Provider 2}/504/29000",    (usual timeout limit is set at 29 seconds)
          199 - "{Vendor4}/{Provider 4}/403/10"       (Provider 4 rejected the request in 10 ms)
```

> **Nota:** Cada encabezado HTTP es una colección de subelementos, por lo que los usuarios pueden enumerar el encabezado de advertencia y comprobar todos los elementos.

## <a name="see-also"></a>Consulte también

Si tiene problemas con la autorización, consulte nuestra [entrada de blog](https://techcommunity.microsoft.com/t5/Using-Microsoft-Graph-Security/Authorization-and-Microsoft-Graph-Security-API/m-p/184376#M2).
