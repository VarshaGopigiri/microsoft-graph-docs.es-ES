---
title: Tipo de recurso deviceCompliancePolicy
description: 'Esta es la clase base para la directiva de cumplimiento. Las directivas de cumplimiento son específicas de la plataforma y las directivas de cumplimiento por plataforma individual se heredan desde ahí. '
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 85a82c981c16370603e3622f6536755bf9146343
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990400"
---
# <a name="devicecompliancepolicy-resource-type"></a>Tipo de recurso deviceCompliancePolicy

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Esta es la clase base para la directiva de cumplimiento. Las directivas de cumplimiento son específicas de la plataforma y las directivas de cumplimiento por plataforma individual se heredan desde ahí. 
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceCompliancePolicies](../api/intune-deviceconfig-devicecompliancepolicy-list.md)|Colección [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)|Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|[Obtener deviceCompliancePolicy](../api/intune-deviceconfig-devicecompliancepolicy-get.md)|[deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)|Lea las propiedades y las relaciones del objeto [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|[Acción assign](../api/intune-deviceconfig-devicecompliancepolicy-assign.md)|Colección [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)|Todavía no documentado|
|[Acción scheduleActionsForRules](../api/intune-deviceconfig-devicecompliancepolicy-scheduleactionsforrules.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto.|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo.|
|versión|Int32|Versión de la configuración del dispositivo.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|scheduledActionsForRule|Colección [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md)|La lista de acción programada para esta regla|
|deviceStatuses|Colección [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md)|Lista de DeviceComplianceDeviceStatus.|
|userStatuses|Colección [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md)|Lista de DeviceComplianceUserStatus.|
|deviceStatusOverview|[deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md)|Información general del estado de los dispositivos sobre el cumplimiento de dispositivos|
|userStatusOverview|[deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md)|Información general del estado de los usuarios sobre el cumplimiento de dispositivos|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Resumen de dispositivo del estado de configuración de cumplimiento|
|asignaciones|Colección [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)|El conjunto de asignaciones para esta directiva de cumplimiento.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCompliancePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicy",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024
}
```



