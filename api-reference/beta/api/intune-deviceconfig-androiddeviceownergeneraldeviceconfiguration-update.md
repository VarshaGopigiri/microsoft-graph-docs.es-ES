---
title: Actualizar androidDeviceOwnerGeneralDeviceConfiguration
description: Actualizar las propiedades de un objeto androidDeviceOwnerGeneralDeviceConfiguration.
author: tfitzmac
ms.openlocfilehash: bf81569d5af7e223ff24e34bc031a19633d22edd
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340099"
---
# <a name="update-androiddeviceownergeneraldeviceconfiguration"></a>Actualizar androidDeviceOwnerGeneralDeviceConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualizar las propiedades de un objeto [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementConfiguration.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|roleScopeTagIds|Colección String|Lista de etiquetas de ámbito para esta instancia de entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|supportsScopeTags|Boolean|Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito. No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito. Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure. Esta propiedad es de sólo lectura. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|accountsBlockModification|Boolean|Indica si está deshabilitada la opción Agregar o quitar cuentas de.|
|appsAllowInstallFromUnknownSources|Boolean|Indica si se permite al usuario para habilitar la configuración de orígenes desconocidos.|
|appsAutoUpdatePolicy|[androidDeviceOwnerAppAutoUpdatePolicyType](../resources/intune-deviceconfig-androiddeviceownerappautoupdatepolicytype.md)|Indica el valor de la directiva de actualización automática de aplicación. Los valores posibles son: `notConfigured`, `userChoice`, `never`, `wiFiOnly` y `always`.|
|appsDefaultPermissionPolicy|[androidDeviceOwnerDefaultAppPermissionPolicyType](../resources/intune-deviceconfig-androiddeviceownerdefaultapppermissionpolicytype.md)|Indica la directiva de permisos para las solicitudes de permisos en tiempo de ejecución si uno no se ha definido para la aplicación en concreto. Los valores posibles son: `deviceDefault`, `prompt`, `autoGrant` y `autoDeny`.|
|bluetoothBlockConfiguration|Boolean|Indica si se deben bloquear un usuario desde la configuración de bluetooth.|
|bluetoothBlockContactSharing|Boolean|Indica si se va a bloquear un usuario de uso compartido de contactos a través de bluetooth o no.|
|cameraBlocked|Boolean|Indica si se va a deshabilitar el uso de la cámara o no.|
|cellularBlockWiFiTethering|Booleano|Indica si se va a bloquear el tethering Wi-Fi.|
|dataRoamingBlocked|Boolean|Indica si se deben bloquear un usuario de movilidad de datos.|
|dateTimeConfigurationBlocked|Boolean|Indica si se deben bloquear el usuario cambie manualmente la fecha o la hora en el dispositivo|
|factoryResetDeviceAdministratorEmails|Colección String|Lista de correos electrónicos de la cuenta de Google que serán necesarios para autenticar una vez fábrica restablecer antes de que se puede configurar un dispositivo.|
|factoryResetBlocked|Boolean|Indica si está deshabilitada la opción de restablecimiento de fábrica en configuración.|
|kioskModeApps|Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)|Una lista de aplicaciones administradas que se mostrará cuando el dispositivo está en modo de pantalla completa. Esta colección puede contener un máximo de 500 elementos.|
|microphoneForceMute|Boolean|Indica si se deben bloquear del audio del micrófono en el dispositivo.|
|networkEscapeHatchAllowed|Boolean|Indica si el dispositivo permitirá que se conectan a una conexión de red temporal en tiempo de inicio.|
|nfcBlockOutgoingBeam|Boolean|Indica si se deben bloquear carretera saliente CNC.|
|passwordBlockKeyguard|Boolean|Indica si está deshabilitada la keyguard.|
|passwordExpirationDays|Int32|Indica la cantidad de tiempo en segundos que se puede establecer una contraseña para antes de que caduque y se le solicitará una contraseña nueva. Valores válidos de 1 a 365|
|passwordMinimumLength|Int32|Indica la longitud mínima de la contraseña requerida en el dispositivo. Valores válidos de 4 a 16|
|passwordMinutesOfInactivityBeforeScreenTimeout|Int32|Milisegundos de inactividad antes de agote el tiempo de la pantalla.|
|passwordPreviousPasswordCountToBlock|Int32|Indica la longitud del historial de contraseñas, donde el usuario no podrá escribir una nueva contraseña que es el mismo que el de las contraseñas en el historial. Valores válidos de 0 a 24|
|passwordRequiredType|[androidDeviceOwnerRequiredPasswordType](../resources/intune-deviceconfig-androiddeviceownerrequiredpasswordtype.md)|Indica la calidad mínima de la contraseña necesaria en el dispositivo. Los valores posibles son: `deviceDefault`, `required`, `numeric`, `numericComplex`, `alphabetic`, `alphanumeric` y `alphanumericWithSymbols`.|
|passwordSignInFailureCountBeforeFactoryReset|Int32|Indica el número de veces que un usuario puede escribir una contraseña incorrecta antes de que se borre el dispositivo. Valores válidos de 4 a 11|
|safeBootBlocked|Boolean|Indica si al reiniciar que el dispositivo en Inicio seguro está deshabilitado.|
|screenCaptureBlocked|Boolean|Indica si se va a deshabilitar la capacidad de realizar capturas de pantalla o no.|
|securityAllowDebuggingFeatures|Boolean|Indica si desea impedir que el usuario de habilitación de características de depuración en el dispositivo o no.|
|securityRequireVerifyApps|Boolean|Indica si o no comprobar aplicaciones es necesario.|
|statusBarBlocked|Boolean|Indica si el estado o barra está deshabilitada, incluidas las notificaciones, la configuración rápida y otros superposiciones de pantalla.|
|stayOnModes|colección de [androidDeviceOwnerBatteryPluggedMode](../resources/intune-deviceconfig-androiddeviceownerbatterypluggedmode.md)|Lista de los modos en que la pantalla del dispositivo permanecerá enciende. Esta colección puede contener un máximo de 4 elementos. Los valores posibles son: `notConfigured`, `ac`, `usb` y `wireless`.|
|storageAllowUsb|Boolean|Indica si se debe o no permitir el almacenamiento masivo USB.|
|storageBlockExternalMedia|Boolean|Indica si se deben bloquear medios externos.|
|storageBlockUsbFileTransfer|Boolean|Indica si se deben bloquear la transferencia de archivos USB.|
|systemUpdateWindowStartMinutesAfterMidnight|Int32|Indica el número de minutos después de la medianoche que inicia la ventana de actualización del sistema. Valores válidos 0 y 1440.|
|systemUpdateWindowEndMinutesAfterMidnight|Int32|Indica el número de minutos después de la medianoche que termina la ventana de actualización del sistema. Valores válidos 0 y 1440.|
|systemUpdateInstallType|[androidDeviceOwnerSystemUpdateInstallType](../resources/intune-deviceconfig-androiddeviceownersystemupdateinstalltype.md)|El tipo de configuración de la actualización del sistema. Los valores posibles son: `deviceDefault`, `postpone`, `windowed` y `automatic`.|
|usersBlockAdd|Boolean|Indica si está deshabilitada la opción Agregar usuarios y perfiles de.|
|usersBlockRemove|Boolean|Indica si desea deshabilitar la eliminación de otros usuarios desde el dispositivo o no.|
|volumeBlockAdjustment|Boolean|Indica si o no ajustar que el volumen principal está deshabilitado.|
|wifiBlockEditConfigurations|Boolean|Indica si desea impedir que el usuario de edición de la configuración de conexión wifi o no.|
|wifiBlockEditPolicyDefinedConfigurations|Boolean|Indica si desea impedir que el usuario acaba las redes definidas por la directiva de edición o no.|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 2073

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountsBlockModification": true,
  "appsAllowInstallFromUnknownSources": true,
  "appsAutoUpdatePolicy": "userChoice",
  "appsDefaultPermissionPolicy": "prompt",
  "bluetoothBlockConfiguration": true,
  "bluetoothBlockContactSharing": true,
  "cameraBlocked": true,
  "cellularBlockWiFiTethering": true,
  "dataRoamingBlocked": true,
  "dateTimeConfigurationBlocked": true,
  "factoryResetDeviceAdministratorEmails": [
    "Factory Reset Device Administrator Emails value"
  ],
  "factoryResetBlocked": true,
  "kioskModeApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "microphoneForceMute": true,
  "networkEscapeHatchAllowed": true,
  "nfcBlockOutgoingBeam": true,
  "passwordBlockKeyguard": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordCountToBlock": 4,
  "passwordRequiredType": "required",
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "safeBootBlocked": true,
  "screenCaptureBlocked": true,
  "securityAllowDebuggingFeatures": true,
  "securityRequireVerifyApps": true,
  "statusBarBlocked": true,
  "stayOnModes": [
    "ac"
  ],
  "storageAllowUsb": true,
  "storageBlockExternalMedia": true,
  "storageBlockUsbFileTransfer": true,
  "systemUpdateWindowStartMinutesAfterMidnight": 11,
  "systemUpdateWindowEndMinutesAfterMidnight": 9,
  "systemUpdateInstallType": "postpone",
  "usersBlockAdd": true,
  "usersBlockRemove": true,
  "volumeBlockAdjustment": true,
  "wifiBlockEditConfigurations": true,
  "wifiBlockEditPolicyDefinedConfigurations": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2264

{
  "@odata.type": "#microsoft.graph.androidDeviceOwnerGeneralDeviceConfiguration",
  "id": "edad943d-943d-edad-3d94-aded3d94aded",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountsBlockModification": true,
  "appsAllowInstallFromUnknownSources": true,
  "appsAutoUpdatePolicy": "userChoice",
  "appsDefaultPermissionPolicy": "prompt",
  "bluetoothBlockConfiguration": true,
  "bluetoothBlockContactSharing": true,
  "cameraBlocked": true,
  "cellularBlockWiFiTethering": true,
  "dataRoamingBlocked": true,
  "dateTimeConfigurationBlocked": true,
  "factoryResetDeviceAdministratorEmails": [
    "Factory Reset Device Administrator Emails value"
  ],
  "factoryResetBlocked": true,
  "kioskModeApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "microphoneForceMute": true,
  "networkEscapeHatchAllowed": true,
  "nfcBlockOutgoingBeam": true,
  "passwordBlockKeyguard": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordCountToBlock": 4,
  "passwordRequiredType": "required",
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "safeBootBlocked": true,
  "screenCaptureBlocked": true,
  "securityAllowDebuggingFeatures": true,
  "securityRequireVerifyApps": true,
  "statusBarBlocked": true,
  "stayOnModes": [
    "ac"
  ],
  "storageAllowUsb": true,
  "storageBlockExternalMedia": true,
  "storageBlockUsbFileTransfer": true,
  "systemUpdateWindowStartMinutesAfterMidnight": 11,
  "systemUpdateWindowEndMinutesAfterMidnight": 9,
  "systemUpdateInstallType": "postpone",
  "usersBlockAdd": true,
  "usersBlockRemove": true,
  "volumeBlockAdjustment": true,
  "wifiBlockEditConfigurations": true,
  "wifiBlockEditPolicyDefinedConfigurations": true
}
```





