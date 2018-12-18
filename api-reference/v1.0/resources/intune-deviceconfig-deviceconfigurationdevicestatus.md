---
title: Tipo de recurso deviceConfigurationDeviceStatus
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 1ea36f7c936220148f751e155ede9ec7bb731cd8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306436"
---
# <a name="deviceconfigurationdevicestatus-resource-type"></a>Tipo de recurso deviceConfigurationDeviceStatus

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceConfigurationDeviceStatuses](../api/intune-deviceconfig-deviceconfigurationdevicestatus-list.md)|Colección [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|Enumere las propiedades y las relaciones de los objetos [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md).|
|[Obtener deviceConfigurationDeviceStatus](../api/intune-deviceconfig-deviceconfigurationdevicestatus-get.md)|[deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|Lea las propiedades y las relaciones del objeto [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md).|
|[Crear deviceConfigurationDeviceStatus](../api/intune-deviceconfig-deviceconfigurationdevicestatus-create.md)|[deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|Cree un objeto [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md).|
|[Eliminar deviceConfigurationDeviceStatus](../api/intune-deviceconfig-deviceconfigurationdevicestatus-delete.md)|Ninguna|Elimina un [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|
|[Actualizar deviceConfigurationDeviceStatus](../api/intune-deviceconfig-deviceconfigurationdevicestatus-update.md)|[deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|Actualice las propiedades de un objeto [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|deviceDisplayName|String|Nombre de dispositivo de DevicePolicyStatus.|
|userName|String|El nombre de usuario que se está notificando|
|deviceModel|String|El modelo de dispositivo que se está notificando|
|complianceGracePeriodExpirationDateTime|DateTimeOffset|La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo|
|status|[complianceStatus](../resources/intune-shared-compliancestatus.md)|Estado de cumplimiento del informe de directiva. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.|
|lastReportedDateTime|DateTimeOffset|Fecha y hora de la última modificación del informe de directiva.|
|userPrincipalName|String|UserPrincipalName.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationDeviceStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStatus",
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



