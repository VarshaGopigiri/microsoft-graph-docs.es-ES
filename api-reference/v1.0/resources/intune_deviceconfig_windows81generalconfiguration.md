# <a name="windows81generalconfiguration-resource-type"></a>Tipo de recurso windows81GeneralConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso windows81GeneralConfiguration.

Hereda de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windows81GeneralConfigurations](../api/intune_deviceconfig_windows81generalconfiguration_list.md)|Colección [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md).|
|[Obtener windows81GeneralConfiguration](../api/intune_deviceconfig_windows81generalconfiguration_get.md)|[windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md)|Lea las propiedades y las relaciones del objeto [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md).|
|[Crear windows81GeneralConfiguration](../api/intune_deviceconfig_windows81generalconfiguration_create.md)|[windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md)|Cree un objeto [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md).|
|[Eliminar windows81GeneralConfiguration](../api/intune_deviceconfig_windows81generalconfiguration_delete.md)|Ninguno|Elimina un [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md).|
|[Actualizar windows81GeneralConfiguration](../api/intune_deviceconfig_windows81generalconfiguration_update.md)|[windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md)|Actualice las propiedades de un objeto [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|description|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|versión|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|accountsBlockAddingNonMicrosoftAccountEmail|Booleano|Indica si se va a impedir que el usuario agregue cuentas de correo electrónico en el dispositivo que no están asociadas con una cuenta de Microsoft.|
|applyOnlyToWindows81|Booleano|Valor que indica si esta directiva se aplica solo a Windows 8.1. Esta propiedad es de solo lectura.|
|browserBlockAutofill|Booleano|Indica si se va a bloquear el autorrelleno.|
|browserBlockAutomaticDetectionOfIntranetSites|Booleano|Indica si se va a bloquear la detección automática de sitios de Intranet.|
|browserBlockEnterpriseModeAccess|Booleano|Indica si se va a bloquear el acceso al modo de empresa.|
|browserBlockJavaScript|Booleano|Indica si se va a impedir que el usuario use JavaScript.|
|browserBlockPlugins|Booleano|Indica si se van a bloquear los complementos.|
|browserBlockPopups|Booleano|Indica si se van a bloquear los elementos emergentes.|
|browserBlockSendingDoNotTrackHeader|Booleano|Indica si se va a impedir que el usuario envíe el encabezado Do Not Track.|
|browserBlockSingleWordEntryOnIntranetSites|Booleano|Indica si se va a bloquear la entrada de palabra única en el sitio de la intranet.|
|browserRequireSmartScreen|Booleano|Indica si se va a exigir que el usuario use el filtro de pantalla inteligente.|
|browserEnterpriseModeSiteListLocation|Cadena|Ubicación de la lista de sitios del modo de empresa. Puede ser un archivo local, la red local o la ubicación http.|
|browserInternetSecurityLevel|[internetSiteSecurityLevel](../resources/intune_deviceconfig_internetsitesecuritylevel.md)|Nivel de seguridad de Internet. Los valores posibles son: `userDefined`, `medium`, `mediumHigh` y `high`.|
|browserIntranetSecurityLevel|[siteSecurityLevel](../resources/intune_deviceconfig_sitesecuritylevel.md)|Nivel de seguridad de la intranet. Los valores posibles son: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh` y `high`.|
|browserLoggingReportLocation|Cadena|La ubicación del informe de registro.|
|browserRequireHighSecurityForRestrictedSites|Booleano|Indica si se va a exigir alta seguridad para los sitios restringidos.|
|browserRequireFirewall|Booleano|Indica si se va a requerir un firewall.|
|browserRequireFraudWarning|Booleano|Indica si se va a requerir una advertencia de fraude.|
|browserTrustedSitesSecurityLevel|[siteSecurityLevel](../resources/intune_deviceconfig_sitesecuritylevel.md)|Nivel de seguridad de los sitios de confianza. Los valores posibles son: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh` y `high`.|
|cellularBlockDataRoaming|Booleano|Indica si se va a bloquear la itinerancia de datos.|
|diagnosticsBlockDataSubmission|Booleano|Indica si se va a bloquear el envío de datos de diagnóstico.|
|passwordBlockPicturePasswordAndPin|Booleano|Indica si se va a impedir que el usuario use una contraseña de imágenes y un PIN.|
|passwordExpirationDays|Int32|Expiración de la contraseña en días.|
|passwordMinimumLength|Int32|La longitud mínima de contraseña.|
|passwordMinutesOfInactivityBeforeScreenTimeout|Int32|Los minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.|
|passwordMinimumCharacterSetCount|Int32|El número de los juegos de caracteres necesarios en la contraseña.|
|passwordPreviousPasswordBlockCount|Int32|Número de contraseñas anteriores que impide su reutilización. Valores válidos de 0 a 24|
|passwordRequiredType|[requiredPasswordType](../resources/intune_deviceconfig_requiredpasswordtype.md)|Tipo de contraseña necesaria. Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.|
|passwordSignInFailureCountBeforeFactoryReset|Int32|El número de errores de inicio de sesión antes del restablecimiento de fábrica.|
|storageRequireDeviceEncryption|Booleano|Indica si se va a requerir el cifrado en un dispositivo móvil.|
|updatesRequireAutomaticUpdates|Booleano|Indica si se van a requerir las actualizaciones automáticas.|
|userAccountControlSettings|[windowsUserAccountControlSettings](../resources/intune_deviceconfig_windowsuseraccountcontrolsettings.md)|Configuración de control de la cuenta de usuario. Los valores posibles son: `userDefined`, `alwaysNotify`, `notifyOnAppChanges`, `notifyOnAppChangesWithoutDimming` y `neverNotify`.|
|workFoldersUrl|Cadena|La dirección URL de las carpetas de trabajo.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md)|La lista de tareas para el perfil de configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceStatuses|Colección [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md)|Estado de instalación de configuración del dispositivo por dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|userStatuses|Colección [deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md)|Estado de instalación de configuración de dispositivo por usuario. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune_deviceconfig_deviceconfigurationdeviceoverview.md)|Información general sobre el estado de dispositivos de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md)|Información general sobre el estado de usuarios de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md)|Resumen de dispositivo sobre el estado de configuración de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windows81GeneralConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows81GeneralConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "accountsBlockAddingNonMicrosoftAccountEmail": true,
  "applyOnlyToWindows81": true,
  "browserBlockAutofill": true,
  "browserBlockAutomaticDetectionOfIntranetSites": true,
  "browserBlockEnterpriseModeAccess": true,
  "browserBlockJavaScript": true,
  "browserBlockPlugins": true,
  "browserBlockPopups": true,
  "browserBlockSendingDoNotTrackHeader": true,
  "browserBlockSingleWordEntryOnIntranetSites": true,
  "browserRequireSmartScreen": true,
  "browserEnterpriseModeSiteListLocation": "String",
  "browserInternetSecurityLevel": "String",
  "browserIntranetSecurityLevel": "String",
  "browserLoggingReportLocation": "String",
  "browserRequireHighSecurityForRestrictedSites": true,
  "browserRequireFirewall": true,
  "browserRequireFraudWarning": true,
  "browserTrustedSitesSecurityLevel": "String",
  "cellularBlockDataRoaming": true,
  "diagnosticsBlockDataSubmission": true,
  "passwordBlockPicturePasswordAndPin": true,
  "passwordExpirationDays": 1024,
  "passwordMinimumLength": 1024,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 1024,
  "passwordMinimumCharacterSetCount": 1024,
  "passwordPreviousPasswordBlockCount": 1024,
  "passwordRequiredType": "String",
  "passwordSignInFailureCountBeforeFactoryReset": 1024,
  "storageRequireDeviceEncryption": true,
  "updatesRequireAutomaticUpdates": true,
  "userAccountControlSettings": "String",
  "workFoldersUrl": "String"
}
```



