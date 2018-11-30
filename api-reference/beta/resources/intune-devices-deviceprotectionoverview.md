---
title: tipo de recurso deviceProtectionOverview
description: Información de hardware de un dispositivo determinado.
ms.openlocfilehash: 81252fdf60c1de129a615b075968e0e6f1eca943
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088484"
---
# <a name="deviceprotectionoverview-resource-type"></a>tipo de recurso deviceProtectionOverview

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Información de hardware de un dispositivo determinado.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|totalReportedDeviceCount|Int32|Recuento total del dispositivo.|
|inactiveThreatAgentDeviceCount|Int32|Dispositivo con recuento de agente de amenaza inactivos|
|unknownStateThreatAgentDeviceCount|Int32|Dispositivo con el estado del agente de amenaza como count desconocido.|
|pendingSignatureUpdateDeviceCount|Int32|Dispositivo con recuento de firma anterior.|
|cleanDeviceCount|Int32|Limpieza de recuento de dispositivo.|
|pendingFullScanDeviceCount|Int32|Recuento de dispositivo pendiente examen completo.|
|pendingRestartDeviceCount|Int32|Recuento de reinicio pendiente de dispositivo.|
|pendingManualStepsDeviceCount|Int32|Recuento de pasos manuales pendiente de dispositivo.|
|pendingOfflineScanDeviceCount|Int32|Recuento de dispositivo de análisis sin conexión pendiente.|
|criticalFailuresDeviceCount|Int32|Recuento de errores críticos de dispositivo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceProtectionOverview"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceProtectionOverview",
  "totalReportedDeviceCount": 1024,
  "inactiveThreatAgentDeviceCount": 1024,
  "unknownStateThreatAgentDeviceCount": 1024,
  "pendingSignatureUpdateDeviceCount": 1024,
  "cleanDeviceCount": 1024,
  "pendingFullScanDeviceCount": 1024,
  "pendingRestartDeviceCount": 1024,
  "pendingManualStepsDeviceCount": 1024,
  "pendingOfflineScanDeviceCount": 1024,
  "criticalFailuresDeviceCount": 1024
}
```





