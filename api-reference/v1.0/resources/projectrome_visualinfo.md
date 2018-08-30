# <a name="visualinfo-resource-type"></a>Tipo de recurso visualInfo

Un tipo complejo para que representa la propiedad **visualElements** en el objeto [activity](../resources/projectrome_activity.md).

Cada actividad del usuario se mostrará en la escala de tiempo como una tarjeta adaptable. Animamos a los programadores de la aplicación a proporcionar una tarjeta personalizada que capture la esencia de la actividad que tuvo lugar en la aplicación. Esto es posible, ya que proporciona una tarjeta de JSON personalizada en la propiedad de contenido.

Además de metadatos visuales con una tarjeta adaptable, la aplicación puede especificar los metadatos de contenido: datos que se usaron para generar inferencias en la actividad de usuario con el fin de ofrecer nuevas actividades para lograr futuro compromiso. Esto es posible mediante el uso de propiedad de contentInfo de la actividad para proporcionar un objeto JSON que aproveche las propiedades schema.org para describir el contenido.

Si no se proporciona una ficha personalizada, se generará una tarjeta simple mediante las propiedades displayText y description. Se recomiendan las tarjetas personalizadas para presentar el mejor contenido desde dentro de la aplicación.

## <a name="properties"></a>Propiedades

|Nombre | Tipo | Descripción|
|:----|:------|:-----------|
|displayText | Cadena | Necesario. Breve descripción de texto de la actividad de usuario único (por ejemplo, el nombre de documento en los casos donde una actividad hace referencia a la creación de documentos)|
|description | Cadena | Opcional. Descripción de texto más larga de la actividad de usuario único (ejemplo: nombre, primera oración y metadatos de documentos)|
|backgroundColor | Cadena | Opcional. Color de fondo utilizado para representar la actividad en la interfaz de usuario: color de marca para el origen de la aplicación de la actividad. Debe ser un color hexadecimal válido|
|content | Objeto JSON sin tipo | Opcional. Fragmento personalizado de datos: objeto JSON usado para proporcionar contenido personalizado para representar la actividad en la interfaz de usuario del núcleo de Windows|
|attribution | [imageInfo](../resources/projectrome_imageinfo.md) | Opcional. Objeto JSON usado para representar un icono que representa la aplicación que se usa para generar la actividad|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "attribution",
    "description",
    "backgroundColor",
    "content"
  ],
  "@odata.type": "microsoft.graph.visualInfo"
}-->

```json
{
    "@odata.type": "microsoft.graph.visualInfo",
    "attribution": {
        "@odata.type": "microsoft.graph.imageInfo",
        "iconUrl": "String (URL)",
        "alternateText": "String",
        "addImageQuery": "boolean"
    },
    "description": "String",
    "backgroundColor": "String",
    "displayText": "String",
    "content": {
        "@odata.type": "microsoft.graph.Json"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "visualinfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
