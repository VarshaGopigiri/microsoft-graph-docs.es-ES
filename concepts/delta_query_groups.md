# <a name="get-incremental-changes-for-groups"></a>Obtener los cambios incrementales de grupos

[Consulta de delta](./delta_query_overview.md) permite consultar las adiciones, eliminaciones o actualizaciones a grupos, por medio de una serie de llamadas a función [delta](../api-reference/v1.0/api/group_delta.md). La consulta de delta le permite descubrir cambios en grupos sin tener que acceder a todo el conjunto de grupos de Microsoft Graph para comparar los cambios.

Los clientes que utilizan grupos de sincronización con un almacén de perfil local pueden utilizar la consulta delta para su sincronización completa inicial y sus sincronizaciones incrementales futuras. Normalmente, el cliente debería realizar una sincronización completa inicial de todos los grupos de inquilino y, después, obtener los cambios incrementales en los grupos de forma periódica.

## <a name="tracking-group-changes"></a>Seguimiento de los cambios de grupos

El seguimiento de los cambios de grupos normalmente es una ronda de una o varias solicitudes GET con la función **delta**. Realiza una solicitud GET de una forma muy similar a cómo [lista grupos](../api-reference/v1.0/api/group_list.md), excepto que incluye lo siguiente:

- La función **delta**
- Un [token de estado](./delta_query_overview.md) (*deltaToken* o *skipToken*) de la anterior llamada a función **delta** GET.

## <a name="example"></a>Ejemplo

El ejemplo siguiente muestra una serie de solicitudes para seguir cambios en grupos:

1. [Solicitud inicial](#initial-request) y [respuesta](#initial-response)
2. [Solicitud nextLink](#nextlink-request) y [respuesta](#nextlink-response)
3. [Solicitud nextLink final](#final-nextlink-request) y [respuesta](#final-nextlink-response)
4. [Solicitud de deltaLink](#deltalink-request) y [respuesta deltaLink](#deltalink-response)

## <a name="initial-request"></a>Solicitud inicial

Para comenzar los cambios de seguimiento en el recurso grupo, debe realizar una solicitud incluyendo la función delta en el recurso grupo.

Tenga en cuenta lo siguiente:

- El parámetro de consulta `$select` opcional se incluye en la solicitud para demostrar cómo los parámetros de consulta se incluyen automáticamente en futuras solicitudes.
- El parámetro de consulta `$expand` opcional se incluye para mostrar cómo se pueden recuperar los miembros del grupo con los objetos del grupo. Esto permite realizar un seguimiento de los cambios de la suscripción, como cuando se agregan o se quitan de grupos de usuarios.
- La solicitud inicial no incluye un token del estado. Los tokens de estado se utilizarán en solicitudes posteriores.

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$select=displayName,description&$expand=members
```

## <a name="initial-response"></a>Respuesta inicial

Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [grupo](../api-reference/v1.0/resources/group.md) en el cuerpo de la respuesta. Si todo el conjunto de grupos es demasiado grande para que quepa en una respuesta, también se incluirá un `nextLink` que contiene un token de estado.

En este ejemplo, se incluyó un `nextLink`; los parámetros de consulta `$select` y `$expand` originales están codificados en el token de estado.

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
      "id":"c2f798fd-f95d-4623-8824-63aec21fffff",
      "members@delta": [
               {
                   "@odata.type": "#microsoft.graph.user",
                   "id": "693acd06-2877-4339-8ade-b704261fe7a0"
               },
               {
                   "@odata.type": "#microsoft.graph.user",
                   "id": "49320844-be99-4164-8167-87ff5d047ace"
               }
      ]
    },
    {
      "displayName":"TestGroup2",
      "description":"Employees in test group 2",
      "id":"ec22655c-8eb2-432a-b4ea-8b8a254bffff"
    }
  ]
}
```

>**Nota:** la propiedad `members@delta` se incluye en el primer objeto de grupo, TestGroup1, y contiene los dos miembros actuales del grupo. TestGroup2 no contiene esta propiedad porque el grupo no tiene ningún miembro.

## <a name="nextlink-request"></a>Solicitud de nextLink

La segunda petición usa el `nextLink` de la respuesta anterior, que contiene el `skipToken`. Tenga en cuenta que los parámetros `$select` y `$expand` no están presentes explícitamente, ya que se codifican en el token.

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjvB7XnF_yllFsCrZJ
```

## <a name="nextlink-response"></a>Respuesta de nextLink

La respuesta contiene otro `nextLink` con un nuevo valor `skipToken`, indicando que hay más grupos disponibles. Siga realizando solicitudes con la dirección URL `nextLink` hasta obtener una dirección URL `deltaLink` en la respuesta final.

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
      "id":"2e5807ce-58f3-4a94-9b37-ffff2e085957",
      "members@delta": [
               {
                   "@odata.type": "#microsoft.graph.user",
                   "id": "632f6bb2-3ec8-4c1f-9073-0027a8c68593"
               }
      ]
    },
    {
      "displayName":"TestGroup4",
      "description":"Employees in test group 4",
      "id":"421e797f-9406-4934-b778-4908421e3505",
      "members@delta": [
               {
                   "@odata.type": "#microsoft.graph.user",
                   "id": "3c8ac7c4-d365-4df9-abfa-356a9dd7763c"
               },
               {
                   "@odata.type": "#microsoft.graph.user",
                   "id": "49320844-be99-4164-8167-87ff5d047ace"
               }
      ]
    }
  ]
}
```

## <a name="final-nextlink-request"></a>Solicitud de nextLink final

La tercera solicitud vuelve a usar la última `nextLink`.

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=ppqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjtQ5LOhVoS7qQG_wdVCHHlbQpga7
```

## <a name="final-nextlink-response"></a>Respuesta de nextLink final

Por último, se devuelve la dirección URL `deltaLink`, lo que significa que no hay ningún dato más para el estado de los grupos existente. Para las solicitudes futuras, la aplicación usa los valores `deltaLink` y `deltaToken` que contiene para obtener información sobre los cambios a los grupos.

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

## <a name="deltalink-request"></a>Solicitud de deltaLink

Con el `deltaLink` de la [última respuesta](#final-nextlink-response), podrá obtener nuevos cambios a los grupos desde la última solicitud. Los cambios incluyen:
- Nuevos objetos de grupo creados.
- Objetos de grupo eliminados.
- Agrupar objetos para los que se ha cambiado una propiedad (por ejemplo, se ha modificado **displayName**).
- Agrupar objetos a los que se han agregado o quitado objetos de miembro.

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$deltatoken=sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw
```

## <a name="deltalink-response"></a>Respuesta de deltaLink

Si no ha habido cambios, se devuelve un `deltaLink` sin resultados, la propiedad `value` está vacía. Asegúrese de que reemplaza el vínculo anterior en la aplicación con el nuevo para usar en futuras llamadas.

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.deltaLink":"https://graph.microsoft.com/v1.0/groups/delta?$deltatoken=sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw",
  "value": []
}
```

Si se han producido cambios, se incluye una colección de grupos cambiados. La respuesta también contiene un `nextLink`, en caso de que haya varias páginas de cambios para recuperar, o un `deltaLink`. Debe implementar el mismo modelo de procedimientos siguiendo el `nextLinks` como antes y conservar el último `deltaLink` para llamadas futuras.

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.deltaLink":"https://graph.microsoft.com/v1.0/groups/delta?$deltatoken=sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw",
  "value": [
          {
              "displayName": "TestGroup3",
              "description": "A test group for change tracking",
              "id": "2e5807ce-58f3-4a94-9b37-ffff2e085957",
              "members@delta": [
                  {
                      "@odata.type": "#microsoft.graph.user",
                      "id": "632f6bb2-3ec8-4c1f-9073-0027a8c6859",
                      "@removed": {
                          "reason": "deleted"
                      }
                  },
                  {
                      "@odata.type": "#microsoft.graph.user",
                      "id": "37de1ae3-408f-4702-8636-20824abda004"
                  }
              ]
          }
      ]
}
```
Algunas cosas que debe tener en cuenta sobre la respuesta del ejemplo anterior:
- Se devuelven los objetos con el mismo conjunto de propiedades especificadas originalmente a través de los parámetros de consulta `$select` y `$expand`.
- Se incluyen propiedades cambiadas y sin cambios. En el ejemplo anterior, la propiedad `description` tiene un nuevo valor, mientras que la propiedad `displayName` no ha cambiado.
- `members@delta` contiene los cambios a la suscripción.
  - El primer usuario en la lista se quitó del grupo, quitando la pertenencia o eliminando el propio objeto de usuario. La propiedad `@removed` lo describe.
  - Se ha agregado al grupo el segundo usuario.

## <a name="paging-through-members-in-a-large-group"></a>Navegar por los miembros en un grupo grande
La propiedad `members@delta` se incluye en los objetos de grupo de forma predeterminada, cuando no se ha especificado el parámetro de consulta `$select`, o cuando el parámetro `$expand=members` se especifica explícitamente. Es posible que en los grupos con muchos miembros no quepan todos los miembros en una sola respuesta; en esta sección se explica el patrón que debe implementar para tratar estos casos.

>**Nota:** este patrón se aplica tanto a la recuperación de estado de grupo inicial como a las llamadas posteriores para obtener los cambios delta.

Supongamos que ejecuta la siguiente consulta delta, ya sea para capturar el estado completo de los grupos inicial o más adelante para obtener cambios delta:

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$select=displayName,description&$expand=members
```

1. Microsoft Graph puede devolver una respuesta que contenga solo un objeto de grupo, con una gran lista de miembros de la propiedad `members@delta`:

**Primera Página**

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=<...>",
  "value": [
    {
      "displayName":"LargeGroup",
      "description":"A group containing thousands of users",
      "id":"2e5807ce-58f3-4a94-9b37-ffff2e085957",
      "members@delta": [
          {
              "@odata.type": "#microsoft.graph.user",
              "id": "632f6bb2-3ec8-4c1f-9073-0027a8c6859",
              "@removed": {
                  "reason": "deleted"
              }
          },
          {
              "@odata.type": "#microsoft.graph.user",
              "id": "37de1ae3-408f-4702-8636-20824abda004"
          },
          <...more users here...>
      ]
    }
    <...no more groups included - this group filled out the entire response...>
  ]
}
```

2. Cuando siga el `nextLink`, es posible que reciba una respuesta de nuevo con el mismo objeto de grupo. Se devolverán los mismos valores de propiedad, pero la propiedad `members@delta` expandida ahora contiene una lista de usuarios diferente.

**Segunda página**

```http
HTTP/1.1 200 OK
Content-type: application/json
{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=<...>",
  "value": [
    {
      "displayName":"LargeGroup",
      "description":"A group containing thousands of users",
      "id":"2e5807ce-58f3-4a94-9b37-ffff2e085957",
      "members@delta": [
          {
              "@odata.type": "#microsoft.graph.user",
              "id": "c08a463b-7b8a-40a4-aa31-f9bf690b9551",
              "@removed": {
                  "reason": "deleted"
              }
          },
          {
              "@odata.type": "#microsoft.graph.user",
              "id": "23423fa6-821e-44b2-aae4-d039d33884c2"
          },
          <...more users here...>
      ]
    }
    <...no more groups included - this group filled out the entire response...>
  ]
}
```

3. Finalmente, se devolverá la lista completa de miembros de este modo y otros grupos empezarán a mostrarse en la respuesta.

Le recomendamos los siguientes procedimientos para administrar correctamente este patrón:
- Siga siempre `nextLink` y combine de forma local cada estado de grupo: a medida que reciba respuestas relacionadas con el mismo grupo, puede usarlas para crear la lista de pertenencia completa en la aplicación.
- Es mejor que no suponga una secuencia específica de las respuestas. Suponga que el mismo grupo podría mostrarse en cualquier lugar en la secuencia `nextLink` y téngalo en cuenta en la lógica de combinación.


## <a name="see-also"></a>Vea también
Información general sobre [Consulta de delta de Microsoft Graph](../concepts/delta_query_overview.md).
