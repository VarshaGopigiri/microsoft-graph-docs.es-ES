# <a name="check-member-groups"></a>Comprobar grupos de miembro

Comprueba la pertenencia en una lista especificada de grupos y devuelve de la lista los grupos de los que el objeto especificado de usuario, grupo o directorio sea miembro. Esta función es transitiva.

## <a name="prerequisites"></a>Requisitos previos
Se requieren los siguientes **ámbitos** para ejecutar esta API: 
- _User.Read.All_ Y _Group.Read.All_
- _Directory.Read.All_

> Nota: Los ámbitos de permiso se muestran por orden de privilegio mínimo necesario.

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /me/checkMemberGroups
POST /users/{id | userPrincipalName}/checkMemberGroups
POST /groups/{id}/checkMemberGroups
POST /directoryObjects/{id}/checkMemberGroups
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |
| Content-Type  | application/json  |

## <a name="request-body"></a>Cuerpo de solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|groupIds|String|Colección que contiene los identificadores de objeto de los grupos en los que se comprueba la pertenencia. Pueden especificarse hasta 20 grupos.|

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto de colección String en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "directoryobject_checkmembergroups"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/checkMemberGroups
Content-type: application/json

{
  "groupIds": [
        "fee2c45b-915a-4a64-b130-f4eb9e75525e",
        "4fe90ae7-065a-478b-9400-e0a0e1cbd540"
  ]
}
```

##### <a name="response"></a>Respuesta
Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
        "fee2c45b-915a-4a64-b130-f4eb9e75525e"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject: checkMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
