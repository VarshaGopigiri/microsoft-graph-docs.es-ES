---
title: tipo de recurso windowsProtectionState
description: Entidad de estado de protección de dispositivo.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7f15044f597fb04e98571de7aec8796e9a9ddf74
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27954529"
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
|id|Cadena|El identificador único para el objeto de estado de protección de dispositivo. Esto es el identificador de dispositivo del dispositivo|
|malwareProtectionEnabled|Booleano|Protección contra malware está habilitado o no|
|deviceState|[windowsDeviceHealthState](../resources/intune-devices-windowsdevicehealthstate.md)|Estado del equipo (como clean o pendiente de examen completo o pendientes reinicio etcetera). Los valores posibles son: `clean`, `fullScanPending`, `rebootPending`, `manualStepsPending`, `offlineScanPending`, `critical`.|
|realTimeProtectionEnabled|Booleano|¿Protección en tiempo real está habilitada o no?|
|networkInspectionSystemEnabled|Booleano|¿Sistema de control de red habilitado o no?|
|quickScanOverdue|Booleano|¿Rápido examinar vencidas o no?|
|fullScanOverdue|Booleano|¿Total de examen vencida o no?|
|signatureUpdateOverdue|Booleano|¿Firma caducada o no?|
|rebootRequired|Booleano|¿Es necesario reiniciar o no?|
|fullScanRequired|Booleano|¿Examen completo o no necesario?|
|engineVersion|Cadena|Versión del motor de actual extremo protección|
|signatureVersion|Cadena|Versión actual de las definiciones de malware|
|antiMalwareVersion|Cadena|Actual de protección contra malware versión|
|lastQuickScanDateTime|DateTimeOffset|Fecha y hora último análisis rápido|
|lastFullScanDateTime|DateTimeOffset|Fecha y hora último análisis rápido|
|lastQuickScanSignatureVersion|Cadena|Última versión de firma de análisis rápido|
|lastFullScanSignatureVersion|Cadena|Última versión de firma de examen completo|
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





