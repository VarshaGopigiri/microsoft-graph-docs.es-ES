---
title: Crear defaultManagedAppProtection
description: Crear un objeto defaultManagedAppProtection.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d479fa5dcb1df66bb67cd6e1d7ae550ff408fd43
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890415"
---
# <a name="create-defaultmanagedappprotection"></a>Crear defaultManagedAppProtection

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Crear un objeto [defaultManagedAppProtection](../resources/intune-mam-defaultmanagedappprotection.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementApps.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/defaultManagedAppProtections
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto defaultManagedAppProtection.

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto defaultManagedAppProtection.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|Cadena|Nombre para mostrar de la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|descripción|Cadena|Descripción de la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|createdDateTime|DateTimeOffset|Fecha y hora de creación de la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|lastModifiedDateTime|DateTimeOffset|Última vez que se modificó la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|id|Cadena|Clave de la entidad. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|version|Cadena|Versión de la entidad. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|periodOfflineBeforeAccessCheck|Duración|Período tras el cual se comprueba el acceso cuando el dispositivo no está conectado a Internet. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|periodOnlineBeforeAccessCheck|Duración|Período tras el cual se comprueba el acceso cuando el dispositivo está conectado a Internet. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|allowedInboundDataTransferSources|[managedAppDataTransferLevel](../resources/intune-mam-managedappdatatransferlevel.md)|Orígenes desde los que se permite la transferencia de datos. Se hereda de [managedAppProtection](../resources/intune-mam-managedappprotection.md). Los valores posibles son: `allApps`, `managedApps` y `none`.|
|allowedOutboundDataTransferDestinations|[managedAppDataTransferLevel](../resources/intune-mam-managedappdatatransferlevel.md)|Destinos a los que se permite la transferencia de datos. Se hereda de [managedAppProtection](../resources/intune-mam-managedappprotection.md). Los valores posibles son: `allApps`, `managedApps` y `none`.|
|organizationalCredentialsRequired|Booleano|Indica si son necesarias las credenciales de la organización para usar la aplicación. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|allowedOutboundClipboardSharingLevel|[managedAppClipboardSharingLevel](../resources/intune-mam-managedappclipboardsharinglevel.md)|Nivel al que puede compartirse el Portapapeles entre aplicaciones en el dispositivo administrado. Se hereda de [managedAppProtection](../resources/intune-mam-managedappprotection.md). Los valores posibles son: `allApps`, `managedAppsWithPasteIn`, `managedApps` y `blocked`.|
|dataBackupBlocked|Booleano|Indica si se bloquea la copia de seguridad de los datos de una aplicación administrada. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|deviceComplianceRequired|Booleano|Indica si se requiere el cumplimiento del dispositivo. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|managedBrowserToOpenLinksRequired|Booleano|Indica si se deben abrir los vínculos de Internet en la aplicación del explorador administrado. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|saveAsBlocked|Booleano|Indica si los usuarios pueden usar el elemento de menú "Guardar como" para guardar una copia de los archivos protegidos. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|periodOfflineBeforeWipeIsEnforced|Duración|Cantidad de tiempo que una aplicación puede estar desconectada de Internet antes de que se borren los datos administrados. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|pinRequired|Booleano|Indica si se requiere un PIN de nivel de aplicación. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|maximumPinRetries|Int32|Número máximo de reintentos de pin incorrecto intentos antes de la aplicación administrada se bloquea o se borre. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|simplePinBlocked|Booleano|Indica si simplePin está bloqueado. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|minimumPinLength|Int32|Longitud mínima de PIN necesaria para un PIN de nivel de aplicación si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|pinCharacterSet|[managedAppPinCharacterSet](../resources/intune-mam-managedapppincharacterset.md)|Conjunto de caracteres que se puede usar para un PIN de nivel de aplicación si PinRequired se establece en True. Se hereda de [managedAppProtection](../resources/intune-mam-managedappprotection.md). Los valores posibles son: `numeric` y `alphanumericAndSymbol`.|
|periodBeforePinReset|Duración|TimePeriod antes de que se deba restablecer el PIN de todos los niveles si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|allowedDataStorageLocations|colección de [managedAppDataStorageLocation](../resources/intune-mam-managedappdatastoragelocation.md)|Ubicaciones de almacenamiento de datos en las que un usuario puede almacenar datos administrados. Se hereda de [managedAppProtection](../resources/intune-mam-managedappprotection.md). Los valores posibles son: `oneDriveForBusiness`, `sharePoint` y `localStorage`.|
|contactSyncBlocked|Booleano|Indica si se pueden sincronizar los contactos en el dispositivo del usuario. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|printBlocked|Booleano|Indica si se puede imprimir desde las aplicaciones administradas. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|fingerprintBlocked|Booleano|Indica si se permite el uso del lector de huellas digitales en lugar de un PIN si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|disableAppPinIfDevicePinIsSet|Booleano|Indica si es necesario el uso del PIN de la aplicación si se establece el PIN del dispositivo. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|minimumRequiredOsVersion|Cadena|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|minimumWarningOsVersion|Cadena|Las versiones anteriores a la versión especificada provocarán un mensaje de advertencia en la aplicación administrada que intenta obtener acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|minimumRequiredAppVersion|Cadena|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|minimumWarningAppVersion|Cadena|Las versiones anteriores a la versión especificada provocarán un mensaje de advertencia en la aplicación administrada. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|minimumWipeOsVersion|Cadena|Versiones de que menor o igual que la versión especificada borrar la aplicación administrada y los datos de la compañía asociada. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|minimumWipeAppVersion|Cadena|Versiones de que menor o igual que la versión especificada borrar la aplicación administrada y los datos de la compañía asociada. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|appActionIfDeviceComplianceRequired|[managedAppRemediationAction](../resources/intune-mam-managedappremediationaction.md)|Define el comportamiento de una aplicación administrada, bloquear o borrado, cuando el dispositivo ya sea con en la raíz o jailbroken, si se establece DeviceComplianceRequired en true. Se hereda de [managedAppProtection](../resources/intune-mam-managedappprotection.md). Los valores posibles son: `block` y `wipe`.|
|appActionIfMaximumPinRetriesExceeded|[managedAppRemediationAction](../resources/intune-mam-managedappremediationaction.md)|Define un comportamiento de una aplicación administrada, bloquear o borrar, según el número máximo de reintentos de pin incorrecto. Se hereda de [managedAppProtection](../resources/intune-mam-managedappprotection.md). Los valores posibles son: `block` y `wipe`.|
|pinRequiredInsteadOfBiometricTimeout|Duración|Tiempo de espera en minutos para un pin de la aplicación en lugar de código de acceso que no sean biométrica Inherited desde [managedAppProtection](../resources/intune-mam-managedappprotection.md)|
|appDataEncryptionType|[managedAppDataEncryptionType](../resources/intune-mam-managedappdataencryptiontype.md)|Tipo de cifrado que debe usarse para los datos en una aplicación administrada. (sólo iOS). Los valores posibles son: `useDeviceSettings`, `afterDeviceRestart`, `whenDeviceLockedExceptOpenFiles` y `whenDeviceLocked`.|
|screenCaptureBlocked|Booleano|Indica si se bloquea la captura de pantalla. (Solo para Android).|
|encryptAppData|Booleano|Indica si se deben cifrar los datos de la aplicación administrada. (Solo para Android).|
|disableAppEncryptionIfDeviceEncryptionIsEnabled|Booleano|Cuando esta opción está habilitada, cifrado de nivel de aplicación está deshabilitado si está habilitado el cifrado de nivel de dispositivo. (Solo para Android).|
|minimumRequiredSdkVersion|Cadena|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía. (sólo iOS)|
|customSettings|Colección [keyValuePair](../resources/intune-shared-keyvaluepair.md)|Conjunto de pares de clave de cadena y valor de cadena que se va a enviar a los usuarios afectados, sin modificar por este servicio.|
|deployedAppCount|Int32|Número de aplicaciones en las que se implementará la directiva actual.|
|minimumRequiredPatchVersion|Cadena|Definir el nivel más antiguo de revisión de seguridad de Android necesario para que un usuario pueda tener acceso seguro a la aplicación. (Solo para Android).|
|minimumWarningPatchVersion|Cadena|Definir el nivel más antiguo de revisión de seguridad de Android recomendado para que un usuario pueda tener acceso seguro a la aplicación. (Solo para Android).|
|exemptedAppProtocols|Colección [keyValuePair](../resources/intune-shared-keyvaluepair.md)|iOS aplicaciones en esta lista será exentos de la directiva y podrán recibir datos desde aplicaciones administradas. (sólo iOS)|
|exemptedAppPackages|Colección [keyValuePair](../resources/intune-shared-keyvaluepair.md)|Android paquetes de aplicación en esta lista serán exentos de la directiva y podrán recibir datos desde aplicaciones administradas. (Solo para Android).|
|faceIdBlocked|Booleano|Indica si se permite el uso de FaceID en lugar de un PIN si PinRequired se establece en True. (sólo iOS)|
|minimumWipeSdkVersion|Cadena|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía.|
|minimumWipePatchVersion|Cadena|Revisión de seguridad para Android de nivel menor o igual que el valor especificado limpie la aplicación administrada y los datos de la compañía asociada. (Solo para Android).|
|allowedIosDeviceModels|Cadena|Permite la lista de modelos de dispositivo separados de punto y coma, como una cadena, para la aplicación administrada para que funcione. (sólo iOS)|
|appActionIfIosDeviceModelNotAllowed|[managedAppRemediationAction](../resources/intune-mam-managedappremediationaction.md)|Define el comportamiento de una aplicación administrada, bloquear o borrado, si el modelo de dispositivo especificado no está permitido. (sólo iOS). Los valores posibles son: `block` y `wipe`.|
|allowedAndroidDeviceManufacturers|Cadena|Lista de separados por punto y coma de los fabricantes de dispositivos permitidos, como una cadena, para la aplicación administrada para que funcione. (Solo para Android).|
|appActionIfAndroidDeviceManufacturerNotAllowed|[managedAppRemediationAction](../resources/intune-mam-managedappremediationaction.md)|Define el comportamiento de una aplicación administrada, bloquear o borrado, si el fabricante del dispositivo especificado no está permitido. (Sólo android). Los valores posibles son: `block` y `wipe`.|
|thirdPartyKeyboardsBlocked|Booleano|Define si se permiten que los teclados de otros fabricantes al tener acceso a una aplicación administrada. (sólo iOS)|
|filterOpenInToOnlyManagedApps|Booleano|Define si se admite la operación de abrir desde la aplicación administrada para las ubicaciones de uso compartido de archivos seleccionadas. Esta configuración sólo se aplica cuando AllowedOutboundDataTransferDestinations está establecido en ManagedApps y DisableProtectionOfManagedOutboundOpenInData se establece en False. (sólo iOS)|
|disableProtectionOfManagedOutboundOpenInData|Booleano|Deshabilitar la protección de datos que se transfieren a otras aplicaciones a través de la opción de apertura de IOS. Esta configuración sólo se permite que sea True cuando AllowedOutboundDataTransferDestinations está establecido en ManagedApps. (sólo iOS)|
|protectInboundDataFromUnknownSources|Booleano|Proteger los datos entrantes de origen desconocido. Esta configuración sólo se permite que sea True cuando AllowedInboundDataTransferSources está establecido en AllApps. (sólo iOS)|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [defaultManagedAppProtection](../resources/intune-mam-defaultmanagedappprotection.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/defaultManagedAppProtections
Content-type: application/json
Content-length: 3219

{
  "@odata.type": "#microsoft.graph.defaultManagedAppProtection",
  "displayName": "Display Name value",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": "Version value",
  "periodOfflineBeforeAccessCheck": "-PT17.1357909S",
  "periodOnlineBeforeAccessCheck": "PT35.0018757S",
  "allowedInboundDataTransferSources": "managedApps",
  "allowedOutboundDataTransferDestinations": "managedApps",
  "organizationalCredentialsRequired": true,
  "allowedOutboundClipboardSharingLevel": "managedAppsWithPasteIn",
  "dataBackupBlocked": true,
  "deviceComplianceRequired": true,
  "managedBrowserToOpenLinksRequired": true,
  "saveAsBlocked": true,
  "periodOfflineBeforeWipeIsEnforced": "-PT3M22.1587532S",
  "pinRequired": true,
  "maximumPinRetries": 1,
  "simplePinBlocked": true,
  "minimumPinLength": 0,
  "pinCharacterSet": "alphanumericAndSymbol",
  "periodBeforePinReset": "PT3M29.6631862S",
  "allowedDataStorageLocations": [
    "sharePoint"
  ],
  "contactSyncBlocked": true,
  "printBlocked": true,
  "fingerprintBlocked": true,
  "disableAppPinIfDevicePinIsSet": true,
  "minimumRequiredOsVersion": "Minimum Required Os Version value",
  "minimumWarningOsVersion": "Minimum Warning Os Version value",
  "minimumRequiredAppVersion": "Minimum Required App Version value",
  "minimumWarningAppVersion": "Minimum Warning App Version value",
  "minimumWipeOsVersion": "Minimum Wipe Os Version value",
  "minimumWipeAppVersion": "Minimum Wipe App Version value",
  "appActionIfDeviceComplianceRequired": "wipe",
  "appActionIfMaximumPinRetriesExceeded": "wipe",
  "pinRequiredInsteadOfBiometricTimeout": "-PT3M9.8396734S",
  "appDataEncryptionType": "afterDeviceRestart",
  "screenCaptureBlocked": true,
  "encryptAppData": true,
  "disableAppEncryptionIfDeviceEncryptionIsEnabled": true,
  "minimumRequiredSdkVersion": "Minimum Required Sdk Version value",
  "customSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ],
  "deployedAppCount": 0,
  "minimumRequiredPatchVersion": "Minimum Required Patch Version value",
  "minimumWarningPatchVersion": "Minimum Warning Patch Version value",
  "exemptedAppProtocols": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ],
  "exemptedAppPackages": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ],
  "faceIdBlocked": true,
  "minimumWipeSdkVersion": "Minimum Wipe Sdk Version value",
  "minimumWipePatchVersion": "Minimum Wipe Patch Version value",
  "allowedIosDeviceModels": "Allowed Ios Device Models value",
  "appActionIfIosDeviceModelNotAllowed": "wipe",
  "allowedAndroidDeviceManufacturers": "Allowed Android Device Manufacturers value",
  "appActionIfAndroidDeviceManufacturerNotAllowed": "wipe",
  "thirdPartyKeyboardsBlocked": true,
  "filterOpenInToOnlyManagedApps": true,
  "disableProtectionOfManagedOutboundOpenInData": true,
  "protectInboundDataFromUnknownSources": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 3327

{
  "@odata.type": "#microsoft.graph.defaultManagedAppProtection",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "id": "77064c51-4c51-7706-514c-0677514c0677",
  "version": "Version value",
  "periodOfflineBeforeAccessCheck": "-PT17.1357909S",
  "periodOnlineBeforeAccessCheck": "PT35.0018757S",
  "allowedInboundDataTransferSources": "managedApps",
  "allowedOutboundDataTransferDestinations": "managedApps",
  "organizationalCredentialsRequired": true,
  "allowedOutboundClipboardSharingLevel": "managedAppsWithPasteIn",
  "dataBackupBlocked": true,
  "deviceComplianceRequired": true,
  "managedBrowserToOpenLinksRequired": true,
  "saveAsBlocked": true,
  "periodOfflineBeforeWipeIsEnforced": "-PT3M22.1587532S",
  "pinRequired": true,
  "maximumPinRetries": 1,
  "simplePinBlocked": true,
  "minimumPinLength": 0,
  "pinCharacterSet": "alphanumericAndSymbol",
  "periodBeforePinReset": "PT3M29.6631862S",
  "allowedDataStorageLocations": [
    "sharePoint"
  ],
  "contactSyncBlocked": true,
  "printBlocked": true,
  "fingerprintBlocked": true,
  "disableAppPinIfDevicePinIsSet": true,
  "minimumRequiredOsVersion": "Minimum Required Os Version value",
  "minimumWarningOsVersion": "Minimum Warning Os Version value",
  "minimumRequiredAppVersion": "Minimum Required App Version value",
  "minimumWarningAppVersion": "Minimum Warning App Version value",
  "minimumWipeOsVersion": "Minimum Wipe Os Version value",
  "minimumWipeAppVersion": "Minimum Wipe App Version value",
  "appActionIfDeviceComplianceRequired": "wipe",
  "appActionIfMaximumPinRetriesExceeded": "wipe",
  "pinRequiredInsteadOfBiometricTimeout": "-PT3M9.8396734S",
  "appDataEncryptionType": "afterDeviceRestart",
  "screenCaptureBlocked": true,
  "encryptAppData": true,
  "disableAppEncryptionIfDeviceEncryptionIsEnabled": true,
  "minimumRequiredSdkVersion": "Minimum Required Sdk Version value",
  "customSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ],
  "deployedAppCount": 0,
  "minimumRequiredPatchVersion": "Minimum Required Patch Version value",
  "minimumWarningPatchVersion": "Minimum Warning Patch Version value",
  "exemptedAppProtocols": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ],
  "exemptedAppPackages": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ],
  "faceIdBlocked": true,
  "minimumWipeSdkVersion": "Minimum Wipe Sdk Version value",
  "minimumWipePatchVersion": "Minimum Wipe Patch Version value",
  "allowedIosDeviceModels": "Allowed Ios Device Models value",
  "appActionIfIosDeviceModelNotAllowed": "wipe",
  "allowedAndroidDeviceManufacturers": "Allowed Android Device Manufacturers value",
  "appActionIfAndroidDeviceManufacturerNotAllowed": "wipe",
  "thirdPartyKeyboardsBlocked": true,
  "filterOpenInToOnlyManagedApps": true,
  "disableProtectionOfManagedOutboundOpenInData": true,
  "protectInboundDataFromUnknownSources": true
}
```





