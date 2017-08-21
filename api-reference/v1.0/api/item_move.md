# <a name="move-a-driveitem"></a>Mover un objeto DriveItem

Para mover un objeto DriveItem a un nuevo elemento primario, la aplicación solicita actualizar la **parentReference** del objeto DriveItem que se moverá. Este es un caso especial del método [Update](item_update.md). La aplicación puede mover un elemento a un nuevo contenedor y actualizar otras propiedades del elemento en una sola solicitud.

No se pueden mover elementos entre [Drives](../resources/drive.md) con esta solicitud.

## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:

* Files.ReadWrite
* Files.ReadWrite.All
* Sites.ReadWrite.All


## <a name="http-request"></a>Solicitud HTTP

```http
PATCH /me/drive/items/{item-id}
PATCH /me/drive/root:/{item-path}
PATCH /drives/{drive-id}/items/{item-id}
PATCH /groups/{group-id}/drive/{item-id}
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre          | Tipo   | Descripción                                                                                                                                                         |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| if-match      | String | Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide la eTag actual en la carpeta, se devuelve una respuesta `412 Precondition Failed`. |


## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione el nuevo valor de la propiedad **parentReference**. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

**Nota:** Al mover elementos a la raíz de un OneDrive, no puede usar la sintaxis `"id:" "root"`. Tendrá que usar el identificador real de la carpeta raíz o usar `{"path": "/drive/root"}` para la referencia primaria.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
En este ejemplo, se mueve un elemento especificado mediante {item-id} a la carpeta **Documentos** del OneDrive del usuario.

<!-- {
  "blockType": "request",
  "name": "update_item"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{item-id}
Content-type: application/json

{
    "name": "new-item-name",
    "parentReference" : {"path": "/drive/root:/Documents"}
}
```

##### <a name="response"></a>Respuesta

En el ejemplo siguiente se muestra la respuesta.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "0123456789abc",
    "name": "new-item-name",
    "folder": { "childCount": 3 },
  "parentReference": {
    "id": "507DE6D5-0201-496A-AA87-5E2563247982",
    "path": "/drive/root:/Documents"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Move item",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
