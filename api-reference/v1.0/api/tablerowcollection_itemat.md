# <a name="tablerowcollection-itemat"></a>TableRowCollection: ItemAt

Obtiene una fila en función de su posición en la colección.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/rows/itemAt
POST /workbook/worksheets/{id|name}/tables/{id|name}/rows/itemAt

```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | {token} de portador. Obligatorio. |
| Workbook-Session-Id  | Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|index|Int32|Valor del índice del objeto que se va a recuperar. Indizado con cero.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorkbookTableRow](../resources/tablerow.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
Aquí tiene un ejemplo de cómo llamar a esta API.
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "tablerowcollection_itemat",
  "idempotent": true,
  "@type": "requestBodyResourceFor.tablerowcollection_itemat"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/rows/itemAt
Content-type: application/json
Content-length: 20

{
  "index": 4
}
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTableRow"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableRowCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->