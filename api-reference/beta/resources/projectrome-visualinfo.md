---
title: tipo de recurso visualInfo
description: Un tipo complejo para que representa la propiedad **visualElements** en el objeto de actividad.
localization_priority: Normal
ms.prod: project-rome
ms.openlocfilehash: 3bc26d7eb63d07d857783e5392337b88124ec685
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27963734"
---
# <a name="visualinfo-resource-type"></a>tipo de recurso visualInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un tipo complejo para que representa la propiedad **visualElements** en el objeto de [actividad](../resources/projectrome-activity.md) .

Cada actividad del usuario se mostrarán en la escala de tiempo como una tarjeta adaptable. Animamos a los programadores de la aplicación para proporcionar una tarjeta personalizada que captura la esencia de la actividad que tuvo lugar en la aplicación. Esto es posible, ya que proporciona una tarjeta de JSON personalizada en la propiedad de contenido.

Además de metadatos visual con una tarjeta adaptable, la aplicación puede especificar los metadatos de contenido: datos que se usó para generar inferencias en la actividad de usuario con el fin de ofrecer nuevas actividades para futura subcontratación vuelva. Esto es posible mediante el uso de propiedad de contentInfo de la actividad para proporcionar un objeto JSON que aprovecha las propiedades schema.org para describir el contenido.

Si no se proporciona una ficha personalizada, se generará una tarjeta simple mediante las propiedades de texto de presentación y una descripción. Se recomiendan las tarjetas personalizadas para demostrar el mejor contenido desde dentro de la aplicación.

## <a name="properties"></a>Propiedades

|Nombre | Tipo | Descripción|
|:----|:------|:-----------|
|texto de presentación | Cadena | Obligatorio. Breve descripción de texto de la actividad de usuario único (por ejemplo, el nombre de documento en los casos donde una actividad hace referencia a la creación de documentos)|
|descripción | Cadena | Opcional. Descripción de texto más larga de la actividad de usuario único (ejemplo: nombre, primera oración y metadatos de documentos)|
|backgroundColor | Cadena | Opcional. Color de fondo utilizado para representar la actividad en la interfaz de usuario - color de marca para el origen de la aplicación de la actividad. Debe ser un color hexadecimal válido|
|content | Objeto JSON sin tipo | Opcional. Fragmento personalizado de datos - objeto JSON se usa para proporcionar contenido personalizado para representar la actividad en la interfaz de usuario del Shell de Windows|
|atribución | [imageInfo](../resources/projectrome-imageinfo.md) | Opcional. Objeto JSON usado para representar un icono que representa la aplicación que se usa para generar la actividad|

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
    "@data.type": "microsoft.graph.visualInfo",
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
        "@data.type": "microsoft.graph.Json"
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
