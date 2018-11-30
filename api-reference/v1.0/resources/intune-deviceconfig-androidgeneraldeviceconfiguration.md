---
title: Tipo de recurso androidGeneralDeviceConfiguration
description: Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso androidGeneralDeviceConfiguration.
ms.openlocfilehash: aa9df8e1cf7e845f2d55b89f70bd6c7ecbf17d84
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030641"
---
# <a name="androidgeneraldeviceconfiguration-resource-type"></a>Tipo de recurso androidGeneralDeviceConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso androidGeneralDeviceConfiguration.

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar androidGeneralDeviceConfigurations](../api/intune-deviceconfig-androidgeneraldeviceconfiguration-list.md)|Colección [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md).|
|[Obtener androidGeneralDeviceConfiguration](../api/intune-deviceconfig-androidgeneraldeviceconfiguration-get.md)|[androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md)|Lea las propiedades y las relaciones del objeto [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md).|
|[Crear androidGeneralDeviceConfiguration](../api/intune-deviceconfig-androidgeneraldeviceconfiguration-create.md)|[androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md)|Cree un objeto [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md).|
|[Eliminar androidGeneralDeviceConfiguration](../api/intune-deviceconfig-androidgeneraldeviceconfiguration-delete.md)|Ninguno|Elimina un [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md).|
|[Actualizar androidGeneralDeviceConfiguration](../api/intune-deviceconfig-androidgeneraldeviceconfiguration-update.md)|[androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md)|Actualice las propiedades de un objeto [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|appsBlockClipboardSharing|Booleano|Indica si se va a bloquear el uso compartido del Portapapeles para copiar y pegar entre aplicaciones.|
|appsBlockCopyPaste|Booleano|Indica si se va a impedir copiar y pegar en las aplicaciones.|
|appsBlockYouTube|Booleano|Indica si se va a bloquear la aplicación YouTube.|
|bluetoothBlocked|Booleano|Indica si se va a bloquear Bluetooth.|
|cameraBlocked|Booleano|Indica si se va a bloquear el uso de la cámara.|
|cellularBlockDataRoaming|Booleano|Indica si se va a bloquear la itinerancia de datos.|
|cellularBlockMessaging|Booleano|Indica si se va a bloquear la mensajería SMS/MMS.|
|cellularBlockVoiceRoaming|Booleano|Indica si se va a bloquear la itinerancia de voz.|
|cellularBlockWiFiTethering|Booleano|Indica si se va a bloquear la sincronización de tethering Wi-Fi.|
|compliantAppsList|Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)|Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType). Esta colección puede contener un máximo de 10 000 elementos.|
|compliantAppListType|[appListType](../resources/intune-deviceconfig-applisttype.md)|Tipo de lista que se encuentra en la CompliantAppsList. Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.|
|diagnosticDataBlockSubmission|Booleano|Indica si se va a bloquear el envío de datos de diagnóstico.|
|locationServicesBlocked|Booleano|Indica si se van a bloquear los servicios de ubicación.|
|googleAccountBlockAutoSync|Booleano|Indica si se va a bloquear la sincronización automática de cuentas de Google.|
|googlePlayStoreBlocked|Booleano|Indica si se va a bloquear la aplicación Google Play Store.|
|kioskModeBlockSleepButton|Booleano|Indica si se va a bloquear el botón de suspensión de pantalla durante el modo de pantalla completa.|
|kioskModeBlockVolumeButtons|Booleano|Indica si se van a bloquear los botones de volumen durante el modo de pantalla completa.|
|kioskModeApps|Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)|Lista de aplicaciones que se podrán ejecutar cuando el dispositivo esté en modo de pantalla completa. Esta colección puede contener un máximo de 500 elementos.|
|nfcBlocked|Booleano|Indica si se va a bloquear la transmisión de datos en proximidad.|
|passwordBlockFingerprintUnlock|Booleano|Indica si se va a impedir el desbloqueo por huella dactilar.|
|passwordBlockTrustAgents|Booleano|Indica si se van a bloquear Smart Lock y otros agentes de confianza.|
|passwordExpirationDays|Int32|Número de días antes de que expire la contraseña. Valores válidos de 1 a 365|
|passwordMinimumLength|Int32|Longitud mínima de las contraseñas. Valores válidos de 4 a 16|
|passwordMinutesOfInactivityBeforeScreenTimeout|Int32|Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.|
|passwordPreviousPasswordBlockCount|Int32|Número de contraseñas anteriores que bloquear. Valores válidos de 0 a 24|
|passwordSignInFailureCountBeforeFactoryReset|Int32|Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica. Valores válidos de 4 a 11|
|passwordRequiredType|[androidRequiredPasswordType](../resources/intune-deviceconfig-androidrequiredpasswordtype.md)|Tipo de contraseña que es necesario. Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.|
|passwordRequired|Booleano|Indica si se va a requerir una contraseña.|
|powerOffBlocked|Booleano|Indica si se va a bloquear el apagado del dispositivo.|
|factoryResetBlocked|Booleano|Indica si se va a impedir que el usuario realice un restablecimiento de fábrica.|
|screenCaptureBlocked|Booleano|Indica si se van a impedir las capturas de pantalla.|
|deviceSharingAllowed|Booleano|Indica si se va a permitir el modo de uso compartido del dispositivo.|
|storageBlockGoogleBackup|Booleano|Indica si se va a bloquear Google Backup.|
|storageBlockRemovableStorage|Booleano|Indica si se va a bloquear el uso de almacenamiento extraíble.|
|storageRequireDeviceEncryption|Booleano|Indica si se va a requerir cifrado del dispositivo.|
|storageRequireRemovableStorageEncryption|Booleano|Indica si se va a requerir cifrado del almacenamiento extraíble.|
|voiceAssistantBlocked|Booleano|Indica si se va a bloquear el uso del asistente de voz.|
|voiceDialingBlocked|Booleano|Indica si se va a bloquear la marcación por voz.|
|webBrowserBlockPopups|Booleano|Indica si se van a bloquear los elementos emergentes en el explorador web.|
|webBrowserBlockAutofill|Booleano|Indica si se va a bloquear la característica de autorrellenado del explorador web.|
|webBrowserBlockJavaScript|Booleano|Indica si se va a bloquear JavaScript en el explorador web.|
|webBrowserBlocked|Booleano|Indica si se va a bloquear el explorador web.|
|webBrowserCookieSettings|[webBrowserCookieSettings](../resources/intune-deviceconfig-webbrowsercookiesettings.md)|Configuración de cookies en el explorador web. Los valores posibles son: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited` y `allowAlways`.|
|wiFiBlocked|Booleano|Indica si se va a bloquear la sincronización de Wi-Fi.|
|appsInstallAllowList|Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)|Lista de aplicaciones que se pueden instalar en el dispositivo KNOX. Esta colección puede contener un máximo de 500 elementos.|
|appsLaunchBlockList|Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)|Lista de aplicaciones cuyo inicio en el dispositivo KNOX está bloqueado. Esta colección puede contener un máximo de 500 elementos.|
|appsHideList|Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)|Lista de aplicaciones que se ocultarán en el dispositivo KNOX. Esta colección puede contener un máximo de 500 elementos.|
|securityRequireVerifyApps|Booleano|Requiere que la característica Verificar aplicaciones de Android esté activada.|

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
  "@odata.type": "microsoft.graph.androidGeneralDeviceConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidGeneralDeviceConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "appsBlockClipboardSharing": true,
  "appsBlockCopyPaste": true,
  "appsBlockYouTube": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "cellularBlockDataRoaming": true,
  "cellularBlockMessaging": true,
  "cellularBlockVoiceRoaming": true,
  "cellularBlockWiFiTethering": true,
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
  "locationServicesBlocked": true,
  "googleAccountBlockAutoSync": true,
  "googlePlayStoreBlocked": true,
  "kioskModeBlockSleepButton": true,
  "kioskModeBlockVolumeButtons": true,
  "kioskModeApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "nfcBlocked": true,
  "passwordBlockFingerprintUnlock": true,
  "passwordBlockTrustAgents": true,
  "passwordExpirationDays": 1024,
  "passwordMinimumLength": 1024,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 1024,
  "passwordPreviousPasswordBlockCount": 1024,
  "passwordSignInFailureCountBeforeFactoryReset": 1024,
  "passwordRequiredType": "String",
  "passwordRequired": true,
  "powerOffBlocked": true,
  "factoryResetBlocked": true,
  "screenCaptureBlocked": true,
  "deviceSharingAllowed": true,
  "storageBlockGoogleBackup": true,
  "storageBlockRemovableStorage": true,
  "storageRequireDeviceEncryption": true,
  "storageRequireRemovableStorageEncryption": true,
  "voiceAssistantBlocked": true,
  "voiceDialingBlocked": true,
  "webBrowserBlockPopups": true,
  "webBrowserBlockAutofill": true,
  "webBrowserBlockJavaScript": true,
  "webBrowserBlocked": true,
  "webBrowserCookieSettings": "String",
  "wiFiBlocked": true,
  "appsInstallAllowList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "appsLaunchBlockList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "appsHideList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "securityRequireVerifyApps": true
}
```



