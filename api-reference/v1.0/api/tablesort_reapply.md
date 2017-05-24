# <a name="tablesort-reapply"></a>TableSort: reapply

Vuelve a aplicar los parámetros de ordenación actuales a la tabla.
## <a name="prerequisites"></a>Requisitos previos
Se requieren los siguientes **ámbitos** para ejecutar esta API: 

    * Files.ReadWrite

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/reapply
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/reapply

```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Autorización  | Portador {código}|


## <a name="request-body"></a>Cuerpo de la solicitud

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
Aquí tiene un ejemplo de cómo llamar a esta API.
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "tablesort_reapply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/reapply
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableSort: reapply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->