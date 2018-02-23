# <a name="targetedmanagedappprotection-resource-type"></a>Tipo de recurso targetedManagedAppProtection

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directiva que se usa para configurar las opciones de administración detallada destinada a grupos de seguridad específicos

Hereda de [managedAppProtection](../resources/intune_mam_managedappprotection.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar targetedManagedAppProtections](../api/intune_mam_targetedmanagedappprotection_list.md)|Colección [targetedManagedAppProtection](../resources/intune_mam_targetedmanagedappprotection.md)|Enumere las propiedades y los relaciones de los objetos [targetedManagedAppProtection](../resources/intune_mam_targetedmanagedappprotection.md).|
|[Obtener targetedManagedAppProtection](../api/intune_mam_targetedmanagedappprotection_get.md)|[targetedManagedAppProtection](../resources/intune_mam_targetedmanagedappprotection.md)|Lea las propiedades y las relaciones del objeto [targetedManagedAppProtection](../resources/intune_mam_targetedmanagedappprotection.md).|
|[Acción assign](../api/intune_mam_targetedmanagedappprotection_assign.md)|Ninguno|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|Cadena|Nombre para mostrar de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|description|Cadena|La descripción de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|lastModifiedDateTime|DateTimeOffset|Última vez que se modificó la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|id|Cadena|Clave de la entidad. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|versión|Cadena|Versión de la entidad. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|periodOfflineBeforeAccessCheck|Duración|El período tras el cual se comprueba el acceso cuando el dispositivo no está conectado a Internet. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|periodOnlineBeforeAccessCheck|Duración|El período tras el cual se comprueba el acceso cuando el dispositivo está conectado a Internet. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|allowedInboundDataTransferSources|Cadena|Orígenes desde los que permite la transferencia de datos. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md). Los valores posibles son: `allApps`, `managedApps` y `none`.|
|allowedOutboundDataTransferDestinations|Cadena|Destinos a los que permite la transferencia de datos. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md). Los valores posibles son: `allApps`, `managedApps` y `none`.|
|organizationalCredentialsRequired|Booleano|Indica si son necesarias las credenciales de la organización para usar la aplicación. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|allowedOutboundClipboardSharingLevel|Cadena|El nivel al que puede compartirse el Portapapeles entre aplicaciones en el dispositivo administrado. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md). Los valores posibles son: `allApps`, `managedAppsWithPasteIn`, `managedApps` y `blocked`.|
|dataBackupBlocked|Booleano|Indica si se bloquea la copia de seguridad de los datos de la aplicación administrada. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|deviceComplianceRequired|Booleano|Indica si se requiere el cumplimiento del dispositivo. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|managedBrowserToOpenLinksRequired|Booleano|Indica si se deberían abrir los vínculos de Internet en la aplicación del explorador administrado. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|saveAsBlocked|Booleano|Indica si los usuarios pueden usar el elemento de menú "Guardar como" para guardar una copia de los archivos protegidos. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|periodOfflineBeforeWipeIsEnforced|Duración|La cantidad de tiempo que una aplicación puede estar desconectada de Internet antes de que se borren los datos administrados. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|pinRequired|Booleano|Indica si se requiere un PIN de nivel de aplicación. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|maximumPinRetries|Int32|Número máximo de intentos de reintento de PIN incorrecto antes de que se borre la aplicación administrada. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|simplePinBlocked|Booleano|Indica si simplePin está bloqueado. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|minimumPinLength|Int32|Longitud mínima de PIN necesaria para un PIN de nivel de aplicación si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|pinCharacterSet|Cadena|Conjunto de caracteres que se puede usar para un PIN de nivel de aplicación si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md). Los valores posibles son: `numeric` y `alphanumericAndSymbol`.|
|periodBeforePinReset|Duración|TimePeriod antes de que se deba restablecer el PIN de todos los niveles si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|allowedDataStorageLocations|Colección de cadenas|Ubicaciones de almacenamiento de datos en las que un usuario puede almacenar datos administrados. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|contactSyncBlocked|Booleano|Indica si se pueden sincronizar los contactos en el dispositivo del usuario. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|printBlocked|Booleano|Indica si se puede imprimir desde las aplicaciones administradas. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|fingerprintBlocked|Booleano|Indica si se permite el uso del lector de huella digital en lugar de un PIN si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|disableAppPinIfDevicePinIsSet|Booleano|Indica si es necesario el uso del PIN de la aplicación si se establece el PIN del dispositivo. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|minimumRequiredOsVersion|Cadena|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|minimumWarningOsVersion|Cadena|Las versiones anteriores a la versión especificada provocarán un mensaje de advertencia en la aplicación administrada que intenta obtener acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|minimumRequiredAppVersion|Cadena|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|minimumWarningAppVersion|Cadena|Las versiones anteriores a la versión especificada provocarán un mensaje de advertencia en la aplicación administrada. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|isAssigned|Booleano|Indica si la directiva se implementará en los grupos de inclusión o no.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md)|Propiedad de navegación a la lista de inclusión y exclusión de los grupos en los que se implementará la directiva.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.targetedManagedAppProtection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.targetedManagedAppProtection",
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
  "isAssigned": true
}
```



