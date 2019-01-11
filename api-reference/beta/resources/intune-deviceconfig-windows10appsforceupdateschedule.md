---
title: tipo de recurso windows10AppsForceUpdateSchedule
description: Programación de actualización de Windows 10 force para aplicaciones
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: ef8a0583bd02a62a4461a3415aae86833e24e948
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811238"
---
# <a name="windows10appsforceupdateschedule-resource-type"></a>tipo de recurso windows10AppsForceUpdateSchedule

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Programación de actualización de Windows 10 force para aplicaciones
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|startDateTime|DateTimeOffset|Reinicie la hora de inicio para la fuerza.|
|recurrence|[windows10AppsUpdateRecurrence](../resources/intune-deviceconfig-windows10appsupdaterecurrence.md)|Programación de periodicidad. Los valores posibles son: `none`, `daily`, `weekly` y `monthly`.|
|runImmediatelyIfAfterStartDateTime|Booleano|Si es true, ejecuta la tarea inmediatamente si StartDateTime se encuentra en el pasado, else, se ejecuta a la siguiente repetición.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windows10AppsForceUpdateSchedule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10AppsForceUpdateSchedule",
  "startDateTime": "String (timestamp)",
  "recurrence": "String",
  "runImmediatelyIfAfterStartDateTime": true
}
```





