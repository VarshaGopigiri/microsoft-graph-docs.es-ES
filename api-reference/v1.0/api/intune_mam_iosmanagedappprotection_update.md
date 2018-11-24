# <a name="update-iosmanagedappprotection"></a>Actualizar iosManagedAppProtection

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementApps.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No compatible.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|String|Nombre para mostrar de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|description|String|Descripción de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|createdDateTime|DateTimeOffset|Fecha y hora de creación de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|lastModifiedDateTime|DateTimeOffset|Última vez que se modificó la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|id|String|Clave de la entidad. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|version|String|Versión de la entidad. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|periodOfflineBeforeAccessCheck|Duración|Período tras el cual se comprueba el acceso cuando el dispositivo no está conectado a Internet. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|periodOnlineBeforeAccessCheck|Duración|Período tras el cual se comprueba el acceso cuando el dispositivo está conectado a Internet. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|allowedInboundDataTransferSources|[managedAppDataTransferLevel](../resources/intune_mam_managedappdatatransferlevel.md)|Orígenes desde los que se permite la transferencia de datos. Se hereda de [managedAppProtection](../resources/intune_mam_managedappprotection.md). Los valores posibles son: `allApps`, `managedApps` y `none`.|
|allowedOutboundDataTransferDestinations|[managedAppDataTransferLevel](../resources/intune_mam_managedappdatatransferlevel.md)|Destinos a los que se permite la transferencia de datos. Se hereda de [managedAppProtection](../resources/intune_mam_managedappprotection.md). Los valores posibles son: `allApps`, `managedApps` y `none`.|
|organizationalCredentialsRequired|Booleano|Indica si son necesarias las credenciales de la organización para usar la aplicación. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|allowedOutboundClipboardSharingLevel|[managedAppClipboardSharingLevel](../resources/intune_mam_managedappclipboardsharinglevel.md)|Nivel al que puede compartirse el Portapapeles entre aplicaciones en el dispositivo administrado. Se hereda de [managedAppProtection](../resources/intune_mam_managedappprotection.md). Los valores posibles son: `allApps`, `managedAppsWithPasteIn`, `managedApps` y `blocked`.|
|dataBackupBlocked|Booleano|Indica si se bloquea la copia de seguridad de los datos de una aplicación administrada. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|deviceComplianceRequired|Booleano|Indica si se requiere el cumplimiento del dispositivo. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|managedBrowserToOpenLinksRequired|Booleano|Indica si se deben abrir los vínculos de Internet en la aplicación del explorador administrado. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|saveAsBlocked|Booleano|Indica si los usuarios pueden usar el elemento de menú "Guardar como" para guardar una copia de los archivos protegidos. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|periodOfflineBeforeWipeIsEnforced|Duración|Cantidad de tiempo que una aplicación puede estar desconectada de Internet antes de que se borren los datos administrados. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|pinRequired|Booleano|Indica si se requiere un PIN de nivel de aplicación. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|maximumPinRetries|Int32|Número máximo de reintentos de pin incorrecto intentos antes de la aplicación administrada se bloquea o se borre. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|simplePinBlocked|Booleano|Indica si simplePin está bloqueado. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|minimumPinLength|Int32|Longitud mínima de PIN necesaria para un PIN de nivel de aplicación si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|pinCharacterSet|[managedAppPinCharacterSet](../resources/intune_mam_managedapppincharacterset.md)|Conjunto de caracteres que se puede usar para un PIN de nivel de aplicación si PinRequired se establece en True. Se hereda de [managedAppProtection](../resources/intune_mam_managedappprotection.md). Los valores posibles son: `numeric` y `alphanumericAndSymbol`.|
|periodBeforePinReset|Duración|TimePeriod antes de que se deba restablecer el PIN de todos los niveles si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|allowedDataStorageLocations|colección de [managedAppDataStorageLocation](../resources/intune_mam_managedappdatastoragelocation.md)|Ubicaciones de almacenamiento de datos en las que un usuario puede almacenar datos administrados. Se hereda de [managedAppProtection](../resources/intune_mam_managedappprotection.md). Los valores posibles son: `oneDriveForBusiness`, `sharePoint` y `localStorage`.|
|contactSyncBlocked|Booleano|Indica si se pueden sincronizar los contactos en el dispositivo del usuario. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|printBlocked|Booleano|Indica si se puede imprimir desde las aplicaciones administradas. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|fingerprintBlocked|Booleano|Indica si se permite el uso del lector de huellas digitales en lugar de un PIN si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|disableAppPinIfDevicePinIsSet|Booleano|Indica si es necesario el uso del PIN de la aplicación si se establece el PIN del dispositivo. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|minimumRequiredOsVersion|String|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|minimumWarningOsVersion|String|Las versiones anteriores a la versión especificada provocarán un mensaje de advertencia en la aplicación administrada que intenta obtener acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|minimumRequiredAppVersion|String|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|minimumWarningAppVersion|String|Las versiones anteriores a la versión especificada provocarán un mensaje de advertencia en la aplicación administrada. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md).|
|isAssigned|Booleano|Indica si la directiva se implementará en los grupos de inclusión. Heredado de [targetedManagedAppProtection](../resources/intune_mam_targetedmanagedappprotection.md)|
|appDataEncryptionType|[managedAppDataEncryptionType](../resources/intune_mam_managedappdataencryptiontype.md)|Tipo de cifrado que debe usarse para los datos en una aplicación administrada. Los valores posibles son: `useDeviceSettings`, `afterDeviceRestart`, `whenDeviceLockedExceptOpenFiles` y `whenDeviceLocked`.|
|minimumRequiredSdkVersion|String|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía.|
|deployedAppCount|Int32|Número de aplicaciones en las que se implementará la directiva actual.|
|faceIdBlocked|Booleano|Indica si se permite el uso de FaceID en lugar de un PIN si PinRequired se establece en True.|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}
Content-type: application/json
Content-length: 1568

{
  "@odata.type": "#microsoft.graph.iosManagedAppProtection",
  "displayName": "Display Name value",
  "description": "Description value",
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
  "isAssigned": true,
  "appDataEncryptionType": "afterDeviceRestart",
  "minimumRequiredSdkVersion": "Minimum Required Sdk Version value",
  "deployedAppCount": 0,
  "faceIdBlocked": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1740

{
  "@odata.type": "#microsoft.graph.iosManagedAppProtection",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "id": "5bc789cb-89cb-5bc7-cb89-c75bcb89c75b",
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
  "isAssigned": true,
  "appDataEncryptionType": "afterDeviceRestart",
  "minimumRequiredSdkVersion": "Minimum Required Sdk Version value",
  "deployedAppCount": 0,
  "faceIdBlocked": true
}
```



