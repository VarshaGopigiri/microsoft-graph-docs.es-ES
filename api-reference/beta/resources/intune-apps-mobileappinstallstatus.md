---
title: tipo de recurso mobileAppInstallStatus
description: Contiene las propiedades para el estado de instalación de una aplicación para un dispositivo móvil.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: cac5c94f0669f784bf4cdd020448e40799d53915
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982613"
---
# <a name="mobileappinstallstatus-resource-type"></a>tipo de recurso mobileAppInstallStatus

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades para el estado de instalación de una aplicación para un dispositivo móvil.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista mobileAppInstallStatuses](../api/intune-apps-mobileappinstallstatus-list.md)|colección de [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md)|Propiedades de la lista y relaciones de los objetos [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .|
|[Obtener mobileAppInstallStatus](../api/intune-apps-mobileappinstallstatus-get.md)|[mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md)|Leer las propiedades y las relaciones del objeto [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .|
|[Crear mobileAppInstallStatus](../api/intune-apps-mobileappinstallstatus-create.md)|[mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md)|Crear un nuevo objeto [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .|
|[Eliminar mobileAppInstallStatus](../api/intune-apps-mobileappinstallstatus-delete.md)|Ninguno|Elimina un [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md).|
|[Actualizar mobileAppInstallStatus](../api/intune-apps-mobileappinstallstatus-update.md)|[mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md)|Actualizar las propiedades de un objeto [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|deviceName|String|Nombre de dispositivo|
|deviceId|String|Identificador de dispositivo|
|lastSyncDateTime|DateTimeOffset|Fecha hora de última sincronización|
|mobileAppInstallStatusValue|[resultantAppState](../resources/intune-shared-resultantappstate.md)|El estado de instalación de la aplicación. Los valores posibles son: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown` y `notApplicable`.|
|installState|[resultantAppState](../resources/intune-shared-resultantappstate.md)|El estado de instalación de la aplicación. Los valores posibles son: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown` y `notApplicable`.|
|installStateDetail|[resultantAppStateDetail](../resources/intune-apps-resultantappstatedetail.md)|Detalle de estado de instalación de la aplicación. Los valores posibles son: `noAdditionalDetails`, `seeInstallErrorCode`, `seeUninstallErrorCode`, `pendingReboot`, `platformNotApplicable`, `minimumCpuSpeedNotMet`, `minimumLogicalProcessorCountNotMet`, `minimumPhysicalMemoryNotMet`, `minimumOsVersionNotMet`, `minimumDiskSpaceNotMet` y `processorArchitectureNotApplicable`.|
|errorCode|Int32|El error de código para la instalación o desinstalación de errores.|
|osVersion|String|Versión del sistema operativo|
|osDescription|String|Descripción del sistema operativo|
|userName|String|Nombre de usuario del dispositivo|
|userPrincipalName|String|Nombre principal de usuario|
|displayVersion|String|Versión legible humano de la aplicación|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|aplicación|[mobileApp](../resources/intune-apps-mobileapp.md)|El vínculo de navegación a la aplicación móvil.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppInstallStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppInstallStatus",
  "id": "String (identifier)",
  "deviceName": "String",
  "deviceId": "String",
  "lastSyncDateTime": "String (timestamp)",
  "mobileAppInstallStatusValue": "String",
  "installState": "String",
  "installStateDetail": "String",
  "errorCode": 1024,
  "osVersion": "String",
  "osDescription": "String",
  "userName": "String",
  "userPrincipalName": "String",
  "displayVersion": "String"
}
```





