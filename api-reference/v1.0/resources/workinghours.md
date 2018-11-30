---
title: Tipo de recurso workingHours
description: Representa los días de la semana y las horas de la zona horaria específica en la que trabaja el usuario.
ms.openlocfilehash: 23b24536ffc86feb261a17c0847e5c15ffc25922
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032089"
---
# <a name="workinghours-resource-type"></a>Tipo de recurso workingHours

Representa los días de la semana y las horas de la zona horaria específica en la que trabaja el usuario.

Tener acceso al horario laboral de un usuario resulta útil en escenarios en los que se administran la planeación de recursos o actividades. Puede [obtener](../api/user-get-mailboxsettings.md#request-3) y [establecer](../api/user-update-mailboxsettings.md#request-2) el horario laboral de un usuario como parte de la [configuración de buzón](mailboxsettings.md) del usuario. 

Puede establecer una zona horaria para el horario laboral distinta de la zona horaria que haya configurado en el cliente de Outlook. Esto puede resultar útil, por ejemplo, si se desplaza a una zona horaria distinta de aquella en la que habitualmente trabaja. Puede establecer el cliente de Outlook  
en la zona horaria de destino para que los valores de hora de Outlook se muestren en la hora local mientras está allí.
Cuando otras personas solicitan reuniones de trabajo con usted en su lugar de trabajo habitual, aún pueden respetar su horario laboral en la zona horaria correspondiente.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| daysOfWeek | colección de dayOfWeek | Días de la semana en los que el usuario trabaja. |
| startTime | Edm.TimeOfDay | Hora del día en la que el usuario empieza a trabajar. |
| endTime | Edm.TimeOfDay | Hora del día en la que el usuario deja de trabajar. |
| timeZone | [timeZoneBase](timezonebase.md) | Zona horaria a la que se aplica el horario laboral. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workingHours"
}-->

```json
{
  "daysOfWeek": ["string"],
  "startTime": "TimeOfDay",
  "endTime": "TimeOfDay",
  "timeZone": {"@odata.type": "microsoft.graph.timeZoneBase"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "workingHours resource",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/workinghours.md/microsoft.graph.workingHours/daysOfWeek:
      Inconsistent types between parameter (String) and table (Object)"
  ],
  "tocPath": ""
}-->