# <a name="thumbnail-resource-type"></a>Tipo de recurso thumbnail

El tipo de recurso **thumbnail** representa una miniatura de una imagen, un vídeo, un documento o una carpeta en OneDrive que tiene una representación gráfica.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo   | Descripción                                  |
|:---------|:-------|:---------------------------------------------|
| height   | Int32  | Alto de la miniatura en píxeles.      |
| url      | String | Dirección URL usada para recuperar el contenido de la miniatura. |
| width    | Int32  | Ancho de la miniatura en píxeles.       |


## <a name="relationships"></a>Relaciones

| Nombre    | Tipo   | Descripción         |
|:--------|:-------|:--------------------|
| content | Stream | Secuencia del contenido. |


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": ["content", "height", "width"],
  "@odata.type": "microsoft.graph.thumbnail"
}-->

```json
{
  "url": "string",
  "height": 1024,
  "width": 1024,
  "content": "stream"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "thumbnail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
