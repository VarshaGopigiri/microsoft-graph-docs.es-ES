---
title: tipo de recurso bookingSchedulingPolicy
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 15f9e0dea22a7cfb5eab437bcc023fe3387bb2ea
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805366"
---
# <a name="bookingschedulingpolicy-resource-type"></a>tipo de recurso bookingSchedulingPolicy

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Representa el conjunto de directivas que determinan cómo se deben crear citas en un calendario de Microsoft Bookings.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|allowStaffSelection|Booleano|True si se debe permitir a los clientes elegir a una persona específica para la reserva.|
|maximumAdvance|Duración|Número máximo de días de antelación que se puede realizar una reserva. Sigue el formato [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) .|
|minimumLeadTime|Duración|La cantidad mínima de tiempo antes de la cual se deben realizar reservas y cancelaciones. Sigue el formato [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) .|
|sendConfirmationsToOwner|Booleano| True para notificar a la empresa a través de correo electrónico cuando se cree o modifique una reserva. Utilice la dirección de correo electrónico especificada en la propiedad de **correo electrónico** de la entidad **bookingBusiness** para el negocio. |
|timeSlotInterval|Duración|Duración de cada franja horaria, indicada en formato [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) .|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingSchedulingPolicy"
}-->

```json
{
  "allowStaffSelection": true,
  "maximumAdvance": "String (timestamp)",
  "minimumLeadTime": "String (timestamp)",
  "sendConfirmationsToOwner": true,
  "timeSlotInterval": "String (timestamp)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingSchedulingPolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
