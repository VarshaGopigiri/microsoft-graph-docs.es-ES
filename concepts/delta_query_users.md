# <a name="get-incremental-changes-for-users-preview"></a>Obtener los cambios incrementales para usuarios (versión preliminar)

[Consulta de delta](./delta_query_overview.md) permite consultar las adiciones, eliminaciones o actualizaciones a usuarios, por medio de una serie de llamadas a función [delta](../api-reference/beta/api/user_delta.md). La consulta de delta le permite descubrir cambios en usuarios sin tener que acceder a todo el conjunto de usuarios de Microsoft Graph para comparar los cambios.

La consulta de delta admite tanto la sincronización completa que recoge de recupera de todos los usuarios de un inquilino y la sincronización incremental que recupera solo los usuarios que han cambiado desde la última sincronización. Normalmente, se debería realizar una sincronización completa inicial de todos los usuarios de inquilino y, después, obtener los cambios incrementales en los usuarios de forma periódica. 

## <a name="tracking-user-changes"></a>Seguimiento de los cambios de usuarios

El seguimiento de los cambios de usuarios normalmente es una ronda de una o varias solicitudes GET con la función **delta**. Realiza una solicitud GET de una forma muy similar a cómo [lista usuarios](../api-reference/beta/api/user_list.md), excepto que incluye lo siguiente:

- La función **delta**
- Un [token de estado](./delta_query_overview.md) (_deltaToken_ o _skipToken_) de la anterior llamada a función **delta** GET.

## <a name="example"></a>Ejemplo

El ejemplo siguiente muestra una serie de solicitudes para seguir cambios en usuarios:

1. [Solicitud inicial](#initial-request) y [respuesta](#initial-response)
2. [Solicitud nextLink](#nextlink-request) y [respuesta](#nextlink-response)
3. [Solicitud nextLink final](#final-nextlink-request) y [respuesta](#final-nextlink-response)
4. [Solicitud de deltaLink](#deltalink-request) y [respuesta deltaLink](#deltalink-response)

## <a name="initial-request"></a>Solicitud inicial

Para comenzar los cambios de seguimiento en el recurso usuario, debe realizar una solicitud incluyendo la función delta en el recurso usuario. 

Tenga en cuenta lo siguiente:

- El parámetro de consulta $select opcional se incluye en la solicitud para demostrar cómo los parámetros de consulta se incluyen automáticamente en futuras solicitudes.
- La solicitud inicial no incluye un token del estado. Los tokens de estado se utilizarán en solicitudes posteriores.

``` http
GET https://graph.microsoft.com/beta/users/delta?$select=displayName,givenName,surname
```

### <a name="initial-response"></a>Respuesta inicial

Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto de colección [usuario](../api-reference/beta/resources/user.md) en el cuerpo de la respuesta. Suponiendo que todo el conjunto de los usuarios sea demasiado grande, la respuesta incluirá también un token de estado nextLink.

En este ejemplo se devuelve una dirección URL nextLink que indica la existencia de páginas de datos adicionales para recuperar en la sesión. El parámetro de consulta $select de la solicitud inicial se codifica en la dirección URL nextLink.

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users(displayName,givenName,surname)",
  "@odata.nextLink":"https://graph.microsoft.com/beta/users/delta?$skiptoken=oEBwdSP6uehIAxQOWq_3Ksh_TLol6KIm3stvdc6hGhZRi1hQ7Spe__dpvm3U4zReE4CYXC2zOtaKdi7KHlUtC2CbRiBIUwOxPKLa",
  "value": [
    {
      "displayName":"Testuser1",
      "givenName":"John",
      "surname":"Doe",
      "id":"ffff7b1a-13b6-477b-8c0c-380905cd99f7"
    },
    {
      "displayName":"Testuser2",
      "givenName":"Jane",
      "surname":"Doe",
      "id":"605d1257-ffff-40b6-8e6f-528a53f5dc55"
    }
  ]
}
```

## <a name="nextlink-request"></a>solicitud de nextLink

La segunda solicitud especifica el `skipToken` devuelto de la respuesta anterior. Tenga en cuenta que el parámetro `$select` no es indispensable, pues `skipToken` lo codifica y lo incluye.

``` http
GET https://graph.microsoft.com/beta/users/delta?$skiptoken=oEBwdSP6uehIAxQOWq_3Ksh_TLol6KIm3stvdc6hGhZRi1hQ7Spe__dpvm3U4zReE4CYXC2zOtaKdi7KHlUtC2CbRiBIUwOxPKLa
```

## <a name="nextlink-response"></a>respuesta de nextLink

La respuesta contiene un `nextLink` y otro `skipToken`, indicando que hay más usuarios disponibles. Sigue realizando solicitudes con la dirección URL nextLink hasta obtener como respuesta una dirección URL deltaLink.

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/beta/users/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjtQ5LOhVoS7qQG_wdVCHHlbQpga7",
  "value": [
    {
      "displayName":"Testuser3",
      "givenName":"Pat",
      "surname":"Doe",
      "id":"d8c37826-ffff-4cae-b348-e2725b1e814b"
    },
    {
      "displayName":"Testuser4",
      "givenName":"Meghan",
      "surname":"Doe",
      "id":"8b1ee412-cd8f-4d59-ffff-24010edb9f1f"
    }
  ]
}
```

## <a name="final-nextlink-request"></a>solicitud de nextLink final

La tercera solicitud continúa usando el último `skipToken` devuelto desde la última solicitud de sincronización. 

``` http
GET https://graph.microsoft.com/beta/users/delta?$skiptoken=oEBwdSP6uehIAxQOWq_3Ksh_TLol6KIm3stvdc6hGhaOYDE2VPA4vxIPA90-P6OzGd6Rvku5fDgBRIGS
```

## <a name="final-nextlink-response"></a>respuesta de nextLink final

Cuando se devuelve la dirección URL deltaLink, no hay más datos sobre el estado existente del recurso para devolver. Para las solicitudes futuras, la aplicación usa la dirección URL deltaLink para obtener información sobre los cambios en el recurso. Guarde `deltaToken` y utilícelo en la dirección URL de solicitud para descubrir cambios a usuarios. 

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/beta/users/delta?$deltatoken=oEcOySpF_hWYmTIUZBOIfPzcwisr_rPe8o9M54L45qEXQGmvQC6T2dbL-9O7nSU-njKhFiGlAZqewNAThmCVnNxqPu5gOBegrm1CaVZ-ZtFZ2tPOAO98OD9y0ao460",
  "value": [
    {
      "displayName":"Testuser5",
      "givenName":"Al",
      "surname":"Doe",
      "id":"25dcffff-959e-4ece-9973-e5d9b800e8cc"
    },
    {
      "displayName":"Testuser6",
      "givenName":"Sam",
      "surname":"Doe",
      "id":"f6ede700-27d0-4c42-bfb9-4dffff43c74a"
    }
  ]
}
```

## <a name="deltalink-request"></a>solicitud de deltaLink

Con el `deltaToken` de la [última respuesta](#final-nextlink-response), podrá obtener usuarios cambiados (agregados, eliminados o actualizados) desde la última solicitud.

``` http
GET https://graph.microsoft.com/beta/users/delta?$deltatoken=oEcOySpF_hWYmTIUZBOIfPzcwisr_rPe8o9M54L45qEXQGmvQC6T2dbL-9O7nSU-njKhFiGlAZqewNAThmCVnNxqPu5gOBegrm1CaVZ-ZtFZ2tPOAO98OD9y0ao460
```

## <a name="deltalink-response"></a>respuesta de deltaLink

Si no ha habido cambios, se devuelve el mismo `deltatoken` sin resultados.

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/beta/users/delta?$deltatoken=oEcOySpF_hWYmTIUZBOIfPzcwisr_rPe8o9M54L45qEXQGmvQC6T2dbL-9O7nSU-njKhFiGlAZqewNAThmCVnNxqPu5gOBegrm1CaVZ-ZtFZ2tPOAO98OD9y0ao460",
  "value": []
}
```

Si se han producido cambios, se devuelve el mismo `deltatoken` con una colección de usuarios cambiados.

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/beta/users/delta?$deltatoken=oEcOySpF_hWYmTIUZBOIfPzcwisr_rPe8o9M54L45qEXQGmvQC6T2dbL-9O7nSU-njKhFiGlAZqewNAThmCVnNxqPu5gOBegrm1CaVZ-ZtFZ2tPOAO98OD9y0ao460",
  "value": [
    {
      "displayName":"Testuser7",
      "givenName":"Joe",
      "surname":"Doe",
      "id":"25dcffff-959e-4ece-9973-e5d9b800e8cc"
    },
    {
      "removed":"changed",
      "id":"8ffff70c-1c63-4860-b963-e34ec660931d"
    }
}
```
## <a name="see-also"></a>Vea también
Información general sobre [Consulta de delta de Microsoft Graph](../concepts/delta_query_overview.md).