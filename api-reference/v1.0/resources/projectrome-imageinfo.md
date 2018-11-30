---
title: tipo de recurso imageInfo
description: Un tipo complejo para que representa la propiedad **atribución** en el elemento visualInfo del objeto de actividad.
ms.openlocfilehash: 051338230850da7e754c5e8ad4f7d9c52fe17b32
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031528"
---
# <a name="imageinfo-resource-type"></a>tipo de recurso imageInfo

Un tipo complejo para que representa la propiedad **atribución** en el elemento [visualInfo](../resources/projectrome-visualinfo.md) del objeto de [actividad](../resources/projectrome-activity.md) .

## <a name="properties"></a>Propiedades

|Nombre | Tipo | Descripción|
|:----|:-----|:-----------|
|iconUrl | String | Opcional; URI que señala a un icono que representa la aplicación que se usa para generar la actividad|
|alternateText | String | Opcional; contenido accesible de texto alternativo para la imagen|
|addImageQuery | Booleano | Opcional; parámetro utilizado para indicar el servidor es capaz de procesar imagen dinámicamente en respuesta a parametrización. Por ejemplo: una imagen de contraste alto|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

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