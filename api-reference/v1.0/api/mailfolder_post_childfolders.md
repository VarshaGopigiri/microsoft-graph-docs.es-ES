# <a name="create-mailfolder"></a>Create MailFolder

Use esta API para crear un objeto mailfolder secundario.

## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*
## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/mailFolders/{id}/childFolders
```

Especifique la carpeta principal en la dirección URL de consulta como identificador de la carpeta o el nombre de carpeta conocido `Inbox`, `Drafts`, `SentItems` o `DeletedItems`.

## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |
| Tipo de contenido  | application/json. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros. **displayName** es la única propiedad que se puede escribir de un objeto [MailFolder](../resources/mailfolder.md).

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName|String|Nombre para mostrar de la nueva carpeta.|

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "create_mailfolder_from_mailfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/{id}/childFolders
Content-type: application/json
Content-length: 159

{
  "displayName": "displayName-value",
}
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 179

{
  "displayName": "displayName-value",
  "parentFolderId": "parentFolderId-value",
  "childFolderCount": 99,
  "unreadItemCount": 99,
  "totalItemCount": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create MailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
