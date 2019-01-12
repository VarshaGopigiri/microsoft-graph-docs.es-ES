---
title: tipo de recurso bookingReminder
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 17cd444b8656c30e8f8966ab14571876ef9354fe
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27936700"
---
# <a name="bookingreminder-resource-type"></a>tipo de recurso bookingReminder

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Representa cuándo y a quienes se debe enviar un recordatorio de correo electrónico.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|message|String|El mensaje en el aviso.|
|desplazamiento|Duración|La cantidad de tiempo antes del inicio de una cita que se debe enviar el aviso. Se mostrará en formato [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) .|
|destinatarios|Cadena| Las personas que shouold recibir el aviso. Los valores posibles son: `allAttendees`, `staff` y `customer`.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingReminder"
}-->

```json
{
  "message": "String",
  "offset": "String (timestamp)",
  "recipients": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingReminder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
