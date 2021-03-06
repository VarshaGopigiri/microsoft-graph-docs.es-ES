---
title: Tipo de recurso managedAppProtection
description: Directiva que se usa para configurar las opciones de administración detallada de un conjunto de aplicaciones específico
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ad18cf543fa34dc4e44e6afe747bd2da9bcc487a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939885"
---
# <a name="managedappprotection-resource-type"></a>Tipo de recurso managedAppProtection

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directiva que se usa para configurar las opciones de administración detallada de un conjunto de aplicaciones específico

Hereda de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedAppProtections](../api/intune-mam-managedappprotection-list.md)|Colección [managedAppProtection](../resources/intune-mam-managedappprotection.md)|Enumere las propiedades y las relaciones de los objetos [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|[Obtener managedAppProtection](../api/intune-mam-managedappprotection-get.md)|[managedAppProtection](../resources/intune-mam-managedappprotection.md)|Lea las propiedades y las relaciones del objeto [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|[Acción targetApps](../api/intune-mam-managedappprotection-targetapps.md)|Ninguno|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|Cadena|Nombre para mostrar de la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|descripción|Cadena|Descripción de la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|createdDateTime|DateTimeOffset|Fecha y hora de creación de la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|lastModifiedDateTime|DateTimeOffset|Última vez que se modificó la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|id|Cadena|Clave de la entidad. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|version|Cadena|Versión de la entidad. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|periodOfflineBeforeAccessCheck|Duración|El período tras el cual se comprueba el acceso cuando el dispositivo no está conectado a Internet.|
|periodOnlineBeforeAccessCheck|Duración|El período tras el cual se comprueba el acceso cuando el dispositivo está conectado a Internet.|
|allowedInboundDataTransferSources|[managedAppDataTransferLevel](../resources/intune-mam-managedappdatatransferlevel.md)|Orígenes desde los que permite la transferencia de datos. Los valores posibles son: `allApps`, `managedApps` y `none`.|
|allowedOutboundDataTransferDestinations|[managedAppDataTransferLevel](../resources/intune-mam-managedappdatatransferlevel.md)|Destinos a los que permite la transferencia de datos. Los valores posibles son: `allApps`, `managedApps` y `none`.|
|organizationalCredentialsRequired|Booleano|Indica si son necesarias las credenciales de la organización para usar la aplicación.|
|allowedOutboundClipboardSharingLevel|[managedAppClipboardSharingLevel](../resources/intune-mam-managedappclipboardsharinglevel.md)|El nivel al que puede compartirse el Portapapeles entre aplicaciones en el dispositivo administrado. Los valores posibles son: `allApps`, `managedAppsWithPasteIn`, `managedApps` y `blocked`.|
|dataBackupBlocked|Booleano|Indica si se bloquea la copia de seguridad de los datos de la aplicación administrada.|
|deviceComplianceRequired|Booleano|Indica si se requiere el cumplimiento del dispositivo.|
|managedBrowserToOpenLinksRequired|Booleano|Indica si se deberían abrir los vínculos de Internet en la aplicación del explorador administrado.|
|saveAsBlocked|Booleano|Indica si los usuarios pueden usar el elemento de menú "Guardar como" para guardar una copia de los archivos protegidos.|
|periodOfflineBeforeWipeIsEnforced|Duración|La cantidad de tiempo que una aplicación puede estar desconectada de Internet antes de que se borren los datos administrados.|
|pinRequired|Booleano|Indica si se requiere un PIN de nivel de aplicación.|
|maximumPinRetries|Int32|Número máximo de reintentos de pin incorrecto intentos antes de la aplicación administrada se bloquea o se borre.|
|simplePinBlocked|Booleano|Indica si simplePin está bloqueado.|
|minimumPinLength|Int32|Longitud mínima de PIN necesaria para un PIN de nivel de aplicación si PinRequired se establece en True|
|pinCharacterSet|[managedAppPinCharacterSet](../resources/intune-mam-managedapppincharacterset.md)|Conjunto de caracteres que se puede usar para un PIN de nivel de aplicación si PinRequired se establece en True. Los valores posibles son: `numeric` y `alphanumericAndSymbol`.|
|periodBeforePinReset|Duración|TimePeriod antes de que se deba restablecer el PIN de todos los niveles si PinRequired se establece en True.|
|allowedDataStorageLocations|colección de [managedAppDataStorageLocation](../resources/intune-mam-managedappdatastoragelocation.md)|Ubicaciones de almacenamiento de datos en las que un usuario puede almacenar datos administrados.|
|contactSyncBlocked|Booleano|Indica si se pueden sincronizar los contactos en el dispositivo del usuario.|
|printBlocked|Booleano|Indica si se puede imprimir desde las aplicaciones administradas.|
|fingerprintBlocked|Booleano|Indica si se permite el uso del lector de huella digital en lugar de un PIN si PinRequired se establece en True.|
|disableAppPinIfDevicePinIsSet|Booleano|Indica si es necesario el uso del PIN de la aplicación si se establece el PIN del dispositivo.|
|minimumRequiredOsVersion|Cadena|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía.|
|minimumWarningOsVersion|Cadena|Las versiones anteriores a la versión especificada provocarán un mensaje de advertencia en la aplicación administrada que intenta obtener acceso a los datos de la compañía.|
|minimumRequiredAppVersion|Cadena|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía.|
|minimumWarningAppVersion|Cadena|Las versiones anteriores a la versión especificada provocarán un mensaje de advertencia en la aplicación administrada.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppProtection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppProtection",
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
  "minimumWarningAppVersion": "String"
}
```

<!-- {
  "type": "#page.annotation",
  "suppressions": [
     "Warning: /api-reference/v1.0/resources/intune-mam-managedappprotection.md/microsoft.graph.managedAppProtection/allowedDataStorageLocations:
      Inconsistent types between parameter (String) and table (Object)"
  ],
}
-->


