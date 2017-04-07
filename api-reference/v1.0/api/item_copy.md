# <a name="copy-a-driveitem"></a>Copiar un objeto DriveItem

Crea una copia de un objeto [driveItem](../resources/driveitem.md) (incluidos los elementos secundarios) en un nuevo elemento primario o con un nombre nuevo.

## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:

  * Files.ReadWrite

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->
```
POST /me/drive/items/{item-id}/copy
POST /me/drive/root:/{path}:/copy
POST /groups/{group-id}/drive/items/{item-id}/copy
```

## <a name="request-body"></a>Cuerpo de solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.


| Nombre            | Valor                                          | Descripción                                                                                                 |
|:----------------|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| parentReference | [ItemReference](../resources/itemreference.md) | Opcional. Referencia al elemento primario en que se creará la copia.                                         |
| name            | cadena                                         | Opcional. El nuevo nombre de la copia. Si no se proporciona, se usará el mismo nombre que el original.    |

**Nota:** _parentReference_ debe incluir un `id` o `path`, pero no ambos. Si se incluyen ambos, tienen que hacer referencia al mismo elemento o se producirá un error.

## <a name="example"></a>Ejemplo

<!-- { "blockType": "request", "name": "copy-item", "scopes": "files.readwrite" } -->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/copy
Content-Type: application/json

{
  "parentReference": {
    "path": "/drive/root:/Documents"
  },
  "name": "contoso plan.docx"
}
```

## <a name="response"></a>Respuesta

Devuelve detalles sobre cómo supervisar el progreso de la copia tras aceptar la solicitud.

<!-- { "blockType": "response" } -->
```http
HTTP/1.1 202 Accepted
```

## <a name="remarks"></a>Comentarios

En muchos casos, la operación de copia se realiza de forma asincrónica. La respuesta de la API solo indicará que la operación de copia se ha aceptado o rechazado, debido a que el nombre de archivo de destino ya está en uso.

**Nota:** La API no proporciona un método para saber si la copia fue correcta.

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Copy"
} -->
