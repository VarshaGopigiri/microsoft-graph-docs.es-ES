---
title: Tipo de recurso windowsUpdateScheduledInstall
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 4a8943fa0275d8b9e5a668be207c90304f22a327
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340918"
---
# <a name="windowsupdatescheduledinstall-resource-type"></a>Tipo de recurso windowsUpdateScheduledInstall

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado

Hereda de [windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|scheduledInstallDay|[weeklySchedule](../resources/intune-deviceconfig-weeklyschedule.md)|Programada instalar día de la semana. Los valores posibles son: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday` y `saturday`.|
|scheduledInstallTime|TimeOfDay|Hora de instalación programada durante el día|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsUpdateScheduledInstall"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUpdateScheduledInstall",
  "scheduledInstallDay": "String",
  "scheduledInstallTime": "String (time of day)"
}
```



