---
title: tipo de recurso scheduleItem
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: a7a31f47cde92549a72299b22a40b10c6f7845c6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088540"
---
# <a name="scheduleitem-resource-type"></a>tipo de recurso scheduleItem

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Un elemento que se describe la disponibilidad de un usuario correspondiente a un evento real en el calendario del usuario de forma predeterminada. En este artículo se aplica a así como un recurso.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|finalización |[dateTimeTimeZone](datetimetimezone.md) |La fecha, hora y zona horaria que finaliza el evento correspondiente. |
|isPrivate |Booleano |La sensibilidad del evento correspondiente. Es True si el evento está marcado como `private`, false en caso contrario. |
|location |String | La ubicación donde se conservan o atendido desde el evento correspondiente. Opcional.|
|inicio |[dateTimeTimeZone](datetimetimezone.md) |La fecha, hora y zona horaria que se inicia el evento correspondiente. |
|status |String | El estado de disponibilidad del usuario o recurso durante el evento correspondiente. Los valores posibles son: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`. |
|subject |String | Línea de asunto del evento correspondiente. Opcional.|


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.scheduleItem"
}-->

```json
{
  "end": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "isPrivate": true,
  "location": "String",
  "start": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "status": "String",
  "subject": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "scheduleItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->