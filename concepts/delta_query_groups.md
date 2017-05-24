# <a name="get-incremental-changes-for-groups"></a>Obtener los cambios incrementales de grupos

[Consulta de delta](./delta_query_overview.md) permite consultar las adiciones, eliminaciones o actualizaciones a grupos, por medio de una serie de llamadas a función [delta](../api-reference/v1.0/api/group_delta.md). La consulta de delta le permite descubrir cambios en grupos sin tener que acceder a todo el conjunto de grupos de Microsoft Graph para comparar los cambios.

Los clientes que utilizan grupos de sincronización con un almacén de perfil local pueden utilizar la consulta delta para su sincronización completa inicial y sus sincronizaciones incrementales futuras. Normalmente, el cliente debería realizar una sincronización completa inicial de todos los grupos de inquilino y, después, obtener los cambios incrementales en los grupos de forma periódica. 

## <a name="tracking-group-changes"></a>Seguimiento de los cambios de grupos

El seguimiento de los cambios de grupos normalmente es una ronda de una o varias solicitudes GET con la función **delta**. Realiza una solicitud GET de una forma muy similar a cómo [lista grupos](../api-reference/v1.0/api/group_list.md), excepto que incluye lo siguiente:

- La función **delta**
- Un [token de estado](./delta_query_overview.md) (_deltaToken_ o _skipToken_) de la anterior llamada a función **delta** GET.

## <a name="example"></a>Ejemplo

El ejemplo siguiente muestra una serie de solicitudes para seguir cambios en grupos:

1. [Solicitud inicial](#initial-request) y [respuesta](#initial-response)
2. [Solicitud nextLink](#nextlink-request) y [respuesta](#nextlink-response)
3. [Solicitud nextLink final](#final-nextlink-request) y [respuesta](#final-nextlink-response)
4. [Solicitud de deltaLink](#deltalink-request) y [respuesta deltaLink](#deltalink-response)

## <a name="initial-request"></a>Solicitud inicial

Para comenzar los cambios de seguimiento en el recurso grupo, debe realizar una solicitud incluyendo la función delta en el recurso grupo. 

Tenga en cuenta lo siguiente:

- El parámetro de consulta $select opcional se incluye en la solicitud para demostrar cómo los parámetros de consulta se incluyen automáticamente en futuras solicitudes.
- La solicitud inicial no incluye un token del estado. Los tokens de estado se utilizarán en solicitudes posteriores.

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$select=displayName,description
```

## <a name="initial-response"></a>Respuesta inicial

Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [grupo](../api-reference/v1.0/resources/group.md) en el cuerpo de la respuesta. Suponiendo que todo el conjunto de los grupos sea demasiado grande, la respuesta incluirá también un token de estado nextLink.

En este ejemplo se devuelve una dirección URL nextLink que indica la existencia de páginas de datos adicionales para recuperar en la sesión. El parámetro de consulta $select de la solicitud inicial se codifica en la dirección URL nextLink.

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups(displayName,description)",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjvB7XnF_yllFsCrZJ",
  "value": [
    {
      "displayName":"TestGroup1",
      "description":"Employees in test group 1",
      "id":"c2f798fd-f95d-4623-8824-63aec21fffff"
    },
    {
      "displayName":"TestGroup2",
      "description":"Employees in test group 2",
      "id":"ec22655c-8eb2-432a-b4ea-8b8a254bffff"
    }
  ]
}
```

## <a name="nextlink-request"></a>solicitud de nextLink

La segunda solicitud especifica el `skipToken` devuelto de la respuesta anterior. Tenga en cuenta que el parámetro `$select` no es indispensable, pues `skipToken` lo codifica y lo incluye.

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjvB7XnF_yllFsCrZJ
```

## <a name="nextlink-response"></a>respuesta de nextLink

La respuesta contiene un `nextLink` y otro `skipToken`, indicando que hay más grupos. Sigue realizando solicitudes con la dirección URL nextLink hasta obtener como respuesta una dirección URL deltaLink.

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjtQ5LOhVoS7qQG_wdVCHHlbQpga7",
  "value": [
    {
      "displayName":"TestGroup3",
      "description":"Employees in test group 3",
      "id":"2e5807ce-58f3-4a94-9b37-ffff2e085957"
    },
    {
      "displayName":"TestGroup4",
      "description":"Employees in test group 4",
      "id":"421e797f-9406-4934-b778-4908421e3505"
    }
  ]
}
```

## <a name="final-nextlink-request"></a>solicitud de nextLink final

La tercera solicitud continúa usando el último `skipToken` devuelto desde la última solicitud de sincronización. 

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=ppqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjtQ5LOhVoS7qQG_wdVCHHlbQpga7
```

## <a name="final-nextlink-response"></a>respuesta de nextLink final

Cuando se devuelve la dirección URL deltaLink, no hay más datos sobre el estado existente del recurso para devolver. Para las solicitudes futuras, la aplicación usa la dirección URL deltaLink para obtener información sobre los cambios en el recurso. Guarde `deltaToken` y utilícelo en la dirección URL de solicitud para descubrir cambios a grupos. 

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.deltaLink":"https://graph.microsoft.com/v1.0/groups/delta?$deltatoken=sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw",
  "value": [
    {
      "displayName":"TestGroup5",
      "description":"Employees in test group 5",
      "id":"bed7f0d4-750e-4e7e-ffff-169002d06fc9"
    },
    {
      "displayName":"TestGroup6",
      "description":"Employees in test group 6",
      "id":"421e797f-9406-ffff-b778-4908421e3505"
    }
  ]
}
```

## <a name="deltalink-request"></a>solicitud de deltaLink

Con el `deltaToken` de la [última respuesta](#final-nextlink-response), podrá obtener grupos cambiados (agregados, eliminados o actualizados) desde la última solicitud.

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$deltatoken=sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw
```

## <a name="deltalink-response"></a>respuesta de deltaLink

Si no ha habido cambios, se devuelve el mismo `deltatoken` sin resultados.

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.deltaLink":"https://graph.microsoft.com/v1.0/groups/delta?$deltatoken=sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw",
  "value": []
}
```

Si se han producido cambios, se devuelve el mismo `deltatoken` con una colección de grupos cambiados.

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.deltaLink":"https://graph.microsoft.com/v1.0/groups/delta?$deltatoken=sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw",
  "value": [
    {
      "displayName":"TestGroup7",
      "description":"Employees in test group 7",
      "id":"f764235c-ffff-4843-a14a-1d8826967260"
    }
  ]
}
```

## <a name="see-also"></a>Vea también
Información general sobre [Consulta de delta de Microsoft Graph](../concepts/delta_query_overview.md).