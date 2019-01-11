---
title: Tipo de recurso deviceManagementSettings
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f973f2645b37375641bc536b5ace0fa508fb0b0e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854421"
---
# <a name="devicemanagementsettings-resource-type"></a>Tipo de recurso deviceManagementSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|deviceComplianceCheckinThresholdDays|Int32|El número de días que se permite a un dispositivo continuar sin registrarse para seguir siendo compatible. Valores válidos de 0 a 120|
|isScheduledActionEnabled|Booleano|Es la característica que está o no habilitada para la acción programada para la regla.|
|secureByDefault|Booleano|Cuando es true, el dispositivo debe ser no compatible cuando no hay ninguna directiva de cumplimiento dirigida|
|enhancedJailBreak|Booleano|Es la característica habilitada o no para la detección de jailbreak de mejorada.|
|deviceInactivityBeforeRetirementInDay|Int32|Cuando el dispositivo no busca un número especificado de días, es posible que se quiten los datos de la compañía y el dispositivo no estará en administración. Valores válidos 30 a 270|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceManagementSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementSettings",
  "deviceComplianceCheckinThresholdDays": 1024,
  "isScheduledActionEnabled": true,
  "secureByDefault": true,
  "enhancedJailBreak": true,
  "deviceInactivityBeforeRetirementInDay": 1024
}
```





