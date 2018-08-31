# <a name="list-deleted-items-owned-by-a-user"></a>**Lista de los elementos eliminados que pertenecen a un usuario**

Recupera una lista de los elementos recientemente eliminados que pertenecen al usuario especificado.  

Actualmente, la funcionalidad de la lista de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) que pertenecen al usuario.

Se trata de una acción de servicio, por lo que no admite paginación.  La API devuelve hasta 1000 objetos eliminados que pertenecen al usuario, ordenados por id.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/en-us/graph/docs/concepts/permissions_reference).

| Tipo de permiso | Permisos (de menos a más privilegiados) |
| --- | --- |
| Delegado (cuenta profesional o educativa) | Group.Read.All, Group.ReadWrite.All |
| Delegado (cuenta personal de Microsoft) |  No admitida. |
| Aplicación | Group.Read.All, Group.ReadWrite.All  |

## <a name="http-request"></a>Solicitud HTTP

``` http
POST /directory/deletedItems/getUserOwnedObjects
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre          | Descripción               |
| ------------- | ------------------------- |
| Autorización | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud

```json
{
  "userId":"{id}",
  "type":"Group"
}
```

El cuerpo de la solicitud requiere los siguientes parámetros:

| Parámetro    | Tipo |Descripción|
|:---------------|:--------|:----------|
|userId|Cadena|Id. del propietario/a.|
|type|Cadena|Tipo de objetos para devolver; `Group` es actualmente el único valor admitido.|


## <a name="response"></a>Respuesta

`200 OK` devuelve con éxito solicitudes de códigos de respuesta; el objeto de la respuesta incluye propiedades de [directorio (elementos eliminados)](../resources/directory.md).

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

``` http
POST https://graph.microsoft.com/v1.0/directory/deletedItems/getUserOwnedObjects
Content-type: application/json
```

``` json
{
  "userId":"55ac777c-109e-4022-b58c-470c8fcb6892",
  "type":"group"
}
```

###### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: es posible que el objeto de respuesta que aparece aquí esté truncado para abreviar. Todas las propiedades admitidas se devuelven de llamadas reales.

``` http
HTTP/1.1 200
Content-type: application/json
Content-length: 1249

{
"value": [
          {
              "@odata.type": "#microsoft.graph.group",
              "id": "bfa7033a-7367-4644-85f5-95aaf385cbd7",
              "deletedDateTime": 2018-04-01T12:39:16Z,
              "classification": null,
              "createdDateTime": "2017-03-22T12:39:16Z",
              "description": null,
              "displayName": "Test",
              "groupTypes": [
                  "Unified"
              ],
              "mail": "Test@contoso.com",
              "mailEnabled": true,
              "mailNickname": "Test",
              "membershipRule": null,
              "membershipRuleProcessingState": null,
              "preferredDataLocation": null,
              "preferredLanguage": null,
              "proxyAddresses": [
                  "SMTP:Test@contoso.com"
              ],
              "renewedDateTime": "2017-09-22T22:30:39Z",
              "securityEnabled": false,
              "theme": null,
              "visibility": "Public"
          } 
        ]
 }
```


