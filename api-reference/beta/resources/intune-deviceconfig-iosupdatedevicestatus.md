---
title: Tipo de recurso iosUpdateDeviceStatus
description: Todavía no documentado
ms.openlocfilehash: d033f0a06293ea95223e5d4d5f0095ffdccc479f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089637"
---
# <a name="iosupdatedevicestatus-resource-type"></a>Tipo de recurso iosUpdateDeviceStatus

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosUpdateDeviceStatuses](../api/intune-deviceconfig-iosupdatedevicestatus-list.md)|Colección [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md)|Enumere las propiedades y las relaciones de los objetos [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).|
|[Obtener iosUpdateDeviceStatus](../api/intune-deviceconfig-iosupdatedevicestatus-get.md)|[iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md)|Lea las propiedades y las relaciones del objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).|
|[Crear iosUpdateDeviceStatus](../api/intune-deviceconfig-iosupdatedevicestatus-create.md)|[iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md)|Cree un objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).|
|[Eliminar iosUpdateDeviceStatus](../api/intune-deviceconfig-iosupdatedevicestatus-delete.md)|Ninguna|Elimina un [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).|
|[Actualizar iosUpdateDeviceStatus](../api/intune-deviceconfig-iosupdatedevicestatus-update.md)|[iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md)|Actualice las propiedades de un objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|installStatus|[iosUpdatesInstallStatus](../resources/intune-deviceconfig-iosupdatesinstallstatus.md)|Estado de la instalación del informe de directiva. Los valores posibles son: `success`, `available`, `idle`, `unknown`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.|
|osVersion|String|La versión del dispositivo que se está notificando.|
|deviceId|String|El identificador del dispositivo que se está notificando.|
|userId|String|El identificador del usuario que se está notificando.|
|deviceDisplayName|String|Nombre de dispositivo de DevicePolicyStatus.|
|userName|String|El nombre de usuario que se está notificando|
|deviceModel|String|El modelo de dispositivo que se está notificando|
|platform|Int32|Plataforma del dispositivo que se notifica|
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
  "@odata.type": "microsoft.graph.iosUpdateDeviceStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosUpdateDeviceStatus",
  "id": "String (identifier)",
  "installStatus": "String",
  "osVersion": "String",
  "deviceId": "String",
  "userId": "String",
  "deviceDisplayName": "String",
  "userName": "String",
  "deviceModel": "String",
  "platform": 1024,
  "complianceGracePeriodExpirationDateTime": "String (timestamp)",
  "status": "String",
  "lastReportedDateTime": "String (timestamp)",
  "userPrincipalName": "String"
}
```





