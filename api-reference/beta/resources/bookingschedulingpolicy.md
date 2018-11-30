---
title: tipo de recurso bookingSchedulingPolicy
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 7a16e9a2ec4e64978dd3c20f7510cfd42d76e826
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086568"
---
# <a name="bookingschedulingpolicy-resource-type"></a>tipo de recurso bookingSchedulingPolicy

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Representa el conjunto de directivas que determinan cómo se deben crear citas en un calendario de Microsoft Bookings.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
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