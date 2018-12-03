---
title: Tipo de recurso windowsPhone81GeneralConfiguration
description: Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso windowsPhone81GeneralConfiguration.
ms.openlocfilehash: cd2126edcbc356584195d6cc640888f33ec48c97
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031826"
---
# <a name="windowsphone81generalconfiguration-resource-type"></a>Tipo de recurso windowsPhone81GeneralConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso windowsPhone81GeneralConfiguration.

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windowsPhone81GeneralConfigurations](../api/intune-deviceconfig-windowsphone81generalconfiguration-list.md)|Colección [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).|
|[Obtener windowsPhone81GeneralConfiguration](../api/intune-deviceconfig-windowsphone81generalconfiguration-get.md)|[windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md)|Lea las propiedades y los relaciones del objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).|
|[Crear windowsPhone81GeneralConfiguration](../api/intune-deviceconfig-windowsphone81generalconfiguration-create.md)|[windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md)|Cree un objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).|
|[Eliminar windowsPhone81GeneralConfiguration](../api/intune-deviceconfig-windowsphone81generalconfiguration-delete.md)|Ninguno|Elimina un [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).|
|[Actualizar windowsPhone81GeneralConfiguration](../api/intune-deviceconfig-windowsphone81generalconfiguration-update.md)|[windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md)|Actualice las propiedades de un objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|applyOnlyToWindowsPhone81|Booleano|Valor que indica si esta directiva se aplica solo a Windows Phone 8.1. Esta propiedad es de solo lectura.|
|appsBlockCopyPaste|Booleano|Indica si se va a impedir cortar y pegar.|
|bluetoothBlocked|Booleano|Indica si se va a bloquear Bluetooth.|
|cameraBlocked|Booleano|Indica si se va a bloquear la cámara.|
|cellularBlockWifiTethering|Booleano|Indica si se va a bloquear el tethering Wi-Fi. No tiene impacto si se bloquea el Wi-Fi.|
|compliantAppsList|Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)|Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType). Esta colección puede contener un máximo de 10 000 elementos.|
|compliantAppListType|[appListType](../resources/intune-deviceconfig-applisttype.md)|Lista que se encuentra en la AppComplianceList. Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.|
|diagnosticDataBlockSubmission|Booleano|Indica si se va a bloquear el envío de datos de diagnóstico.|
|emailBlockAddingAccounts|Booleano|Indica si se van a bloquear las cuentas de correo electrónico personalizadas.|
|locationServicesBlocked|Booleano|Indica si se van a bloquear los servicios de ubicación.|
|microsoftAccountBlocked|Booleano|Indica si se va a bloquear el uso de una cuenta de Microsoft.|
|nfcBlocked|Booleano|Indica si se va a bloquear la transmisión de datos en proximidad.|
|passwordBlockSimple|Booleano|Indica si se va a bloquear la sincronización del calendario.|
|passwordExpirationDays|Int32|Número de días antes de que expire la contraseña.|
|passwordMinimumLength|Int32|Longitud mínima de las contraseñas.|
|passwordMinutesOfInactivityBeforeScreenTimeout|Int32|Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.|
|passwordMinimumCharacterSetCount|Int32|Número de juegos de caracteres que debe contener una contraseña.|
|passwordPreviousPasswordBlockCount|Int32|Número de contraseñas anteriores que bloquear. Valores válidos de 0 a 24|
|passwordSignInFailureCountBeforeFactoryReset|Int32|Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.|
|passwordRequiredType|[requiredPasswordType](../resources/intune-deviceconfig-requiredpasswordtype.md)|Tipo de contraseña que es necesario. Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.|
|passwordRequired|Booleano|Indica si se va a requerir una contraseña.|
|screenCaptureBlocked|Booleano|Indica si se van a impedir las capturas de pantalla.|
|storageBlockRemovableStorage|Booleano|Indica si se va a impedir el almacenamiento extraíble.|
|storageRequireEncryption|Booleano|Indica si se va a requerir cifrado.|
|webBrowserBlocked|Booleano|Indica si se va a bloquear el explorador web.|
|wifiBlocked|Booleano|Indica si se va a bloquear el uso de Wi-Fi.|
|wifiBlockAutomaticConnectHotspots|Booleano|Indica si se va a bloquear automáticamente la conexión a zonas Wi-Fi. No tiene impacto si se bloquea el Wi-Fi.|
|wifiBlockHotspotReporting|Booleano|Indica si se van a bloquear los informes de zona Wi-Fi. No tiene impacto si se bloquea el Wi-Fi.|
|windowsStoreBlocked|Booleano|Indica si se va a bloquear la Tienda Windows.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|La lista de tareas para el perfil de configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceStatuses|Colección [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|Estado de instalación de configuración del dispositivo por dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|userStatuses|Colección [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)|Estado de instalación de configuración de dispositivo por usuario. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|Información general sobre el estado de dispositivos de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|Información general sobre el estado de usuarios de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Resumen de dispositivo sobre el estado de configuración de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsPhone81GeneralConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsPhone81GeneralConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "applyOnlyToWindowsPhone81": true,
  "appsBlockCopyPaste": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "cellularBlockWifiTethering": true,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "compliantAppListType": "String",
  "diagnosticDataBlockSubmission": true,
  "emailBlockAddingAccounts": true,
  "locationServicesBlocked": true,
  "microsoftAccountBlocked": true,
  "nfcBlocked": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 1024,
  "passwordMinimumLength": 1024,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 1024,
  "passwordMinimumCharacterSetCount": 1024,
  "passwordPreviousPasswordBlockCount": 1024,
  "passwordSignInFailureCountBeforeFactoryReset": 1024,
  "passwordRequiredType": "String",
  "passwordRequired": true,
  "screenCaptureBlocked": true,
  "storageBlockRemovableStorage": true,
  "storageRequireEncryption": true,
  "webBrowserBlocked": true,
  "wifiBlocked": true,
  "wifiBlockAutomaticConnectHotspots": true,
  "wifiBlockHotspotReporting": true,
  "windowsStoreBlocked": true
}
```



