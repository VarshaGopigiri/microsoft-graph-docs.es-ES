---
title: tipo de recurso deviceConfigurationTargetedUserAndDevice
description: Conflicto de resumen para un conjunto de directivas de configuración del dispositivo.
author: tfitzmac
ms.openlocfilehash: 04b0e31d0f3f099389e4901eb654139d286f4bd8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27345244"
---
# <a name="deviceconfigurationtargeteduseranddevice-resource-type"></a>tipo de recurso deviceConfigurationTargetedUserAndDevice

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Conflicto de resumen para un conjunto de directivas de configuración del dispositivo.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|deviceId|String|El identificador del dispositivo en el registro.|
|deviceName|String|El nombre del dispositivo en el registro.|
|userId|String|El identificador del usuario en el registro.|
|userDisplayName|String|El nombre para mostrar del usuario en el registro|
|userPrincipalName|String|El UPN del usuario en el registro.|
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





