# <a name="uploadsession-resource-type"></a>Tipo de recurso UploadSession

El recurso **UploadSession** proporciona información sobre cómo cargar archivos grandes en las bibliotecas de documentos de OneDrive, OneDrive para la Empresa o SharePoint.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "uploadUrl", "nextExpectedRanges" ],
  "@odata.type": "microsoft.graph.uploadSession"
}-->

```json
{
  "expirationDateTime": "timestamp",
  "nextExpectedRanges": ["string"],
  "uploadUrl": "url"
}

```
## <a name="properties"></a>Propiedades


| Propiedad             | Tipo              |Descripción|
|:-------------------|:------------------|:----------|
| expirationDateTime | DateTimeOffset    | La fecha y hora en UTC en que caducará la sesión de carga. Debe cargarse el archivo completo antes de esta fecha de expiración. |
| nextExpectedRanges | Colección string | Una colección de intervalos de bytes que el servidor no encuentra para el archivo. Estos intervalos están indexados con cero y tienen el formato "inicio-fin" (p. ej. "0-26" para indicar los 27 primeros bytes del archivo). |
| uploadUrl          | String            | El extremo de la dirección URL que acepta las solicitudes PUT de los intervalos de bytes del archivo. |

## <a name="additional-resources"></a>Recursos adicionales

Consulte [Upload large files with an upload session](../api/item_createUploadSession.md) (Cargar archivos grandes con una sesión de carga) para obtener más información sobre cómo cargar archivos mediante una sesión de carga.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "uploadSession resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->