---
title: Tipo de recurso iosManagedAppProtection
description: Directiva que se usa para configurar las opciones de administración detallada destinada a grupos de seguridad específicos y para un conjunto de aplicaciones determinado en un dispositivo iOS
ms.openlocfilehash: e0f38dc23d41b05be5f2e2e2a94edb19f199a1c5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029809"
---
# <a name="iosmanagedappprotection-resource-type"></a>Tipo de recurso iosManagedAppProtection

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directiva que se usa para configurar las opciones de administración detallada destinada a grupos de seguridad específicos y para un conjunto de aplicaciones determinado en un dispositivo iOS

Hereda de [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosManagedAppProtections](../api/intune-mam-iosmanagedappprotection-list.md)|Colección [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md)|Enumere las propiedades y las relaciones de los objetos [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md).|
|[Obtener iosManagedAppProtection](../api/intune-mam-iosmanagedappprotection-get.md)|[iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md)|Lea las propiedades y las relaciones del objeto [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md).|
|[Crear iosManagedAppProtection](../api/intune-mam-iosmanagedappprotection-create.md)|[iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md)|Cree un objeto [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md).|
|[Eliminar iosManagedAppProtection](../api/intune-mam-iosmanagedappprotection-delete.md)|Ninguno|Elimina un [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md).|
|[Actualizar iosManagedAppProtection](../api/intune-mam-iosmanagedappprotection-update.md)|[iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md)|Actualice las propiedades de un objeto [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|String|Nombre para mostrar de la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|descripción|String|Descripción de la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|createdDateTime|DateTimeOffset|Fecha y hora de creación de la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|lastModifiedDateTime|DateTimeOffset|Última vez que se modificó la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|id|String|Clave de la entidad. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|version|String|Versión de la entidad. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
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
|allowedDataStorageLocations|colección de [managedAppDataStorageLocation](../resources/intune-mam-managedappdatastoragelocation.md)|Ubicaciones de almacenamiento de datos en las que un usuario puede almacenar datos administrados. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md)|
|contactSyncBlocked|Booleano|Indica si se pueden sincronizar los contactos en el dispositivo del usuario. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|printBlocked|Booleano|Indica si se puede imprimir desde las aplicaciones administradas. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|fingerprintBlocked|Booleano|Indica si se permite el uso del lector de huellas digitales en lugar de un PIN si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|disableAppPinIfDevicePinIsSet|Booleano|Indica si es necesario el uso del PIN de la aplicación si se establece el PIN del dispositivo. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|minimumRequiredOsVersion|String|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|minimumWarningOsVersion|String|Las versiones anteriores a la versión especificada provocarán un mensaje de advertencia en la aplicación administrada que intenta obtener acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|minimumRequiredAppVersion|String|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|minimumWarningAppVersion|String|Las versiones anteriores a la versión especificada provocarán un mensaje de advertencia en la aplicación administrada. Heredado de [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|isAssigned|Booleano|Indica si la directiva se implementará en los grupos de inclusión. Heredado de [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md)|
|appDataEncryptionType|[managedAppDataEncryptionType](../resources/intune-mam-managedappdataencryptiontype.md)|Tipo de cifrado que debe usarse para los datos en una aplicación administrada. Los valores posibles son: `useDeviceSettings`, `afterDeviceRestart`, `whenDeviceLockedExceptOpenFiles` y `whenDeviceLocked`.|
|minimumRequiredSdkVersion|String|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía.|
|deployedAppCount|Int32|Número de aplicaciones en las que se implementará la directiva actual.|
|faceIdBlocked|Booleano|Indica si se permite el uso de FaceID en lugar de un PIN si PinRequired se establece en True.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md)|Propiedad de navegación a la lista de inclusión y exclusión de los grupos en los que se implementará la directiva. Heredado de [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md)|
|aplicaciones|Colección [managedMobileApp](../resources/intune-mam-managedmobileapp.md)|Lista de aplicaciones en las que se implementará la directiva.|
|deploymentSummary|[managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md)|Propiedad de navegación para el resumen de implementación de la configuración.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosManagedAppProtection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosManagedAppProtection",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String",
  "periodOfflineBeforeAccessCheck": "String (duration)",
  "periodOnlineBeforeAccessCheck": "String (duration)",
  "allowedInboundDataTransferSources": "String",
  "allowedOutboundDataTransferDestinations": "String",
  "organizationalCredentialsRequired": true,
  "allowedOutboundClipboardSharingLevel": "String",
  "dataBackupBlocked": true,
  "deviceComplianceRequired": true,
  "managedBrowserToOpenLinksRequired": true,
  "saveAsBlocked": true,
  "periodOfflineBeforeWipeIsEnforced": "String (duration)",
  "pinRequired": true,
  "maximumPinRetries": 1024,
  "simplePinBlocked": true,
  "minimumPinLength": 1024,
  "pinCharacterSet": "String",
  "periodBeforePinReset": "String (duration)",
  "allowedDataStorageLocations": [
    "String"
  ],
  "contactSyncBlocked": true,
  "printBlocked": true,
  "fingerprintBlocked": true,
  "disableAppPinIfDevicePinIsSet": true,
  "minimumRequiredOsVersion": "String",
  "minimumWarningOsVersion": "String",
  "minimumRequiredAppVersion": "String",
  "minimumWarningAppVersion": "String",
  "isAssigned": true,
  "appDataEncryptionType": "String",
  "minimumRequiredSdkVersion": "String",
  "deployedAppCount": 1024,
  "faceIdBlocked": true
}
```

<!-- {
  "type": "#page.annotation",
  "suppressions": [
     "Warning: /api-reference/v1.0/resources/intune-mam-iosmanagedappprotection.md/microsoft.graph.iosManagedAppProtection/allowedDataStorageLocations:
      Inconsistent types between parameter (String) and table (Object)"
  ],
}
-->



