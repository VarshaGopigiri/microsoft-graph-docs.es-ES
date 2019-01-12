---
title: Tipo de recurso deviceComplianceDeviceStatus
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d730a811ce3f62045ebb6b46954f64bc5f53d8ff
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986232"
---
# <a name="devicecompliancedevicestatus-resource-type"></a>Tipo de recurso deviceComplianceDeviceStatus

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceComplianceDeviceStatuses](../api/intune-deviceconfig-devicecompliancedevicestatus-list.md)|Colección [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md)|Enumere las propiedades y las relaciones de los objetos [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md).|
|[Obtener deviceComplianceDeviceStatus](../api/intune-deviceconfig-devicecompliancedevicestatus-get.md)|[deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md)|Lea las propiedades y las relaciones del objeto [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md).|
|[Crear deviceComplianceDeviceStatus](../api/intune-deviceconfig-devicecompliancedevicestatus-create.md)|[deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md)|Cree un objeto [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md).|
|[Eliminar deviceComplianceDeviceStatus](../api/intune-deviceconfig-devicecompliancedevicestatus-delete.md)|Ninguna|Elimina un [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md).|
|[Actualizar deviceComplianceDeviceStatus](../api/intune-deviceconfig-devicecompliancedevicestatus-update.md)|[deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md)|Actualice las propiedades de un objeto [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|deviceDisplayName|String|Nombre de dispositivo de DevicePolicyStatus.|
|userName|Cadena|El nombre de usuario que se está notificando|
|deviceModel|Cadena|El modelo de dispositivo que se está notificando|
|complianceGracePeriodExpirationDateTime|DateTimeOffset|La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo|
|status|[complianceStatus](../resources/intune-shared-compliancestatus.md)|Estado de cumplimiento del informe de directiva. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.|
|lastReportedDateTime|DateTimeOffset|Fecha y hora de la última modificación del informe de directiva.|
|userPrincipalName|Cadena|UserPrincipalName.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceComplianceDeviceStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceComplianceDeviceStatus",
  "id": "String (identifier)",
  "deviceDisplayName": "String",
  "userName": "String",
  "deviceModel": "String",
  "complianceGracePeriodExpirationDateTime": "String (timestamp)",
  "status": "String",
  "lastReportedDateTime": "String (timestamp)",
  "userPrincipalName": "String"
}
```



