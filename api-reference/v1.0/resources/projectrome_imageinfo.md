# <a name="imageinfo-resource-type"></a>tipo de recurso imageInfo

Tipo complejo para representar la propiedad **attribution** del elemento [visualInfo](../resources/projectrome_visualinfo.md) del objeto [activity](../resources/projectrome_activity.md).

## <a name="properties"></a>Propiedades

|Nombre | Tipo | Descripción|
|:----|:-----|:-----------|
|iconUrl | Cadena | Opcional; URI que apunta a un icono que representa la aplicación utilizada para generar la actividad|
|alternateText | Cadena | Opcional; contenido accesible (texto alternativo) que se proporciona para la imagen|
|addImageQuery | Booleano | Opcional; parámetro utilizado para indicar que el servidor es capaz de representar imágenes dinámicamente en respuesta a parametrización. Por ejemplo: una imagen de contraste alto|

## <a name="json-representation"></a>Representación JSON

He aquí una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "iconUrl",
    "alternateText",
    "addImageQuery"
  ],
  "@odata.type": "microsoft.graph.imageInfo"
}-->

```json
{
    "@odata.type": "microsoft.graph.imageInfo",
    "iconUrl": "String (URL)",
    "alternateText": "String",
    "addImageQuery": "boolean"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "imageinfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->