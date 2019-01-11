---
title: tipo de recurso deviceConfigurationTargetedUserAndDevice
description: Conflicto de resumen para un conjunto de directivas de configuración del dispositivo.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 46355f78f23060ecc901c3f98f0e3f7d13101d1e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809628"
---
# <a name="deviceconfigurationtargeteduseranddevice-resource-type"></a>tipo de recurso deviceConfigurationTargetedUserAndDevice

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Conflicto de resumen para un conjunto de directivas de configuración del dispositivo.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|deviceId|Cadena|El identificador del dispositivo en el registro.|
|deviceName|Cadena|El nombre del dispositivo en el registro.|
|userId|Cadena|El identificador del usuario en el registro.|
|userDisplayName|Cadena|El nombre para mostrar del usuario en el registro|
|userPrincipalName|Cadena|El UPN del usuario en el registro.|
|lastCheckinDateTime|DateTimeOffset|Última hora de protección para este par de usuario/dispositivo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceConfigurationTargetedUserAndDevice"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationTargetedUserAndDevice",
  "deviceId": "String",
  "deviceName": "String",
  "userId": "String",
  "userDisplayName": "String",
  "userPrincipalName": "String",
  "lastCheckinDateTime": "String (timestamp)"
}
```





