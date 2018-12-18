---
title: tipo de recurso windowsProtectionState
description: Entidad de estado de protección de dispositivo.
author: tfitzmac
ms.openlocfilehash: 636b969ddafde5976939df764ae1180e19a181c0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27328080"
---
# <a name="windowsprotectionstate-resource-type"></a>tipo de recurso windowsProtectionState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad de estado de protección de dispositivo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener windowsProtectionState](../api/intune-devices-windowsprotectionstate-get.md)|[windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md)|Leer las propiedades y las relaciones del objeto [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) .|
|[Actualizar windowsProtectionState](../api/intune-devices-windowsprotectionstate-update.md)|[windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md)|Actualizar las propiedades de un objeto [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|El identificador único para el objeto de estado de protección de dispositivo. Esto es el identificador de dispositivo del dispositivo|
|malwareProtectionEnabled|Boolean|Protección contra malware está habilitado o no|
|deviceState|[windowsDeviceHealthState](../resources/intune-devices-windowsdevicehealthstate.md)|Estado del equipo (como clean o pendiente de examen completo o pendientes reinicio etcetera). Los valores posibles son: `clean`, `fullScanPending`, `rebootPending`, `manualStepsPending`, `offlineScanPending`, `critical`.|
|realTimeProtectionEnabled|Boolean|¿Protección en tiempo real está habilitada o no?|
|networkInspectionSystemEnabled|Boolean|¿Sistema de control de red habilitado o no?|
|quickScanOverdue|Boolean|¿Rápido examinar vencidas o no?|
|fullScanOverdue|Boolean|¿Total de examen vencida o no?|
|signatureUpdateOverdue|Boolean|¿Firma caducada o no?|
|rebootRequired|Boolean|¿Es necesario reiniciar o no?|
|fullScanRequired|Boolean|¿Examen completo o no necesario?|
|engineVersion|String|Versión del motor de actual extremo protección|
|signatureVersion|String|Versión actual de las definiciones de malware|
|antiMalwareVersion|String|Actual de protección contra malware versión|
|lastQuickScanDateTime|DateTimeOffset|Fecha y hora último análisis rápido|
|lastFullScanDateTime|DateTimeOffset|Fecha y hora último análisis rápido|
|lastQuickScanSignatureVersion|String|Última versión de firma de análisis rápido|
|lastFullScanSignatureVersion|String|Última versión de firma de examen completo|
|lastReportedDateTime|DateTimeOffset|Último estado de mantenimiento de dispositivo el tiempo notificado|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|detectedMalwareState|colección de [windowsDeviceMalwareState](../resources/intune-devices-windowsdevicemalwarestate.md)|Lista de dispositivos de malware|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsProtectionState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsProtectionState",
  "id": "String (identifier)",
  "malwareProtectionEnabled": true,
  "deviceState": "String",
  "realTimeProtectionEnabled": true,
  "networkInspectionSystemEnabled": true,
  "quickScanOverdue": true,
  "fullScanOverdue": true,
  "signatureUpdateOverdue": true,
  "rebootRequired": true,
  "fullScanRequired": true,
  "engineVersion": "String",
  "signatureVersion": "String",
  "antiMalwareVersion": "String",
  "lastQuickScanDateTime": "String (timestamp)",
  "lastFullScanDateTime": "String (timestamp)",
  "lastQuickScanSignatureVersion": "String",
  "lastFullScanSignatureVersion": "String",
  "lastReportedDateTime": "String (timestamp)"
}
```





