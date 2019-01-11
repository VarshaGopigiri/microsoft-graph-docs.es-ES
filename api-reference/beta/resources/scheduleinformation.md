---
title: tipo de recurso scheduleInformation
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: e535f5c2b47e810fc767cb29d0b24f28ed3c7bf0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828710"
---
# <a name="scheduleinformation-resource-type"></a>tipo de recurso scheduleInformation

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Representa la disponibilidad de un usuario, una lista de distribución o un recurso para un período de tiempo especificado.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|availabilityView |Cadena |Representa una vista combinada de disponibilidad de todos los elementos en `scheduleItems`. La vista se compone de intervalos de tiempo. Disponibilidad durante cada franja horaria se indica con: `0`= gratis, `1`= provisional, `2`= ocupado, `3`= fuera de la oficina, `4`= trabajar en otro lugar.|
|error |[freeBusyError](freebusyerror.md) |Información de error al intentar obtener la disponibilidad del usuario, la lista de distribución o el recurso. |
|scheduleId |Cadena |Una dirección SMTP del usuario, la lista de distribución o el recurso, que identifica una instancia de **scheduleInformation**. |
|scheduleItems |colección [scheduleItem](scheduleitem.md) |Contiene los elementos que describen la disponibilidad del usuario o recurso. |
|workingHours |[workingHours](workinghours.md) |Días de la semana y horas de la zona horaria específica en la que trabaja el usuario. Estos se establecen como parte de del usuario [mailboxSettings](mailboxsettings.md).|


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.scheduleInformation"
}-->

```json
{
  "availabilityView": "String",
  "error": {"@odata.type": "microsoft.graph.freeBusyError"},
  "scheduleId": "String",
  "scheduleItems": [{"@odata.type": "microsoft.graph.scheduleItem"}],
  "workingHours": {"@odata.type": "microsoft.graph.workingHours"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "scheduleInformation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
