# <a name="update-driveitem-properties"></a>Actualizar propiedades de DriveItem

Actualiza los metadatos de un [DriveItem](../resources/driveitem.md) por identificador o ruta de acceso.

También puede usar una actualización para [mover un elemento](item_move.md) a otro elemento primario actualizando la propiedad **parentReference** del elemento.

## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:

* Files.ReadWrite
* Files.ReadWrite.All
* Sites.ReadWrite.All

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/drive/items/{item-id}
PATCH /me/drive/root:/{item-path}
PATCH /drives/{drive-id}/items/{item-id}
PATCH /groups/{group-id}/drive/items/{item-id}
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre          | Tipo   | Descripción                                                                                                                                                         |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| if-match      | String | Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide la eTag actual en la carpeta, se devuelve una respuesta `412 Precondition Failed`. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de las propiedades que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento la aplicación no debe incluir propiedades que no hayan cambiado.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
Este ejemplo cambia el nombre del driveItem.

<!-- {
  "blockType": "request",
  "name": "update_item"
}-->
```http
PATCH /me/drive/items/{item-id}
Content-type: application/json

{
    "name": "new-file-name.docx"
}
```

##### <a name="response"></a>Respuesta

En el ejemplo siguiente se muestra la respuesta. Esta respuesta se trunca para mejorar la legibilidad.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "01NKDM7HMOJTVYMDOSXFDK2QJDXCDI3WUK",
    "name": "new-file-name.docx",
    "file": { }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update item",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Update item"
}-->
