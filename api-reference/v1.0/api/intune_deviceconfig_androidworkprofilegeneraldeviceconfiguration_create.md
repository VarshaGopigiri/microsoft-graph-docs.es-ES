# <a name="create-androidworkprofilegeneraldeviceconfiguration"></a>Crear androidWorkProfileGeneralDeviceConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Crear un nuevo objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune_deviceconfig_androidworkprofilegeneraldeviceconfiguration.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

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
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidWorkProfileGeneralDeviceConfiguration.

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidWorkProfileGeneralDeviceConfiguration.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|passwordBlockFingerprintUnlock|Booleano|Indica si se va a impedir el desbloqueo por huella dactilar.|
|passwordBlockTrustAgents|Booleano|Indica si se van a bloquear Smart Lock y otros agentes de confianza.|
|passwordExpirationDays|Int32|Número de días antes de que expire la contraseña. Valores válidos de 1 a 365|
|passwordMinimumLength|Int32|Longitud mínima de las contraseñas. Valores válidos de 4 a 16|
|passwordMinutesOfInactivityBeforeScreenTimeout|Int32|Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.|
|passwordPreviousPasswordBlockCount|Int32|Número de contraseñas anteriores que bloquear. Valores válidos de 0 a 24|
|passwordSignInFailureCountBeforeFactoryReset|Int32|Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica. Valores válidos de 4 a 11|
|passwordRequiredType|[androidWorkProfileRequiredPasswordType](../resources/intune_deviceconfig_androidworkprofilerequiredpasswordtype.md)|Tipo de contraseña que es necesario. Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.|
|workProfileDataSharingType|[androidWorkProfileCrossProfileDataSharingType](../resources/intune_deviceconfig_androidworkprofilecrossprofiledatasharingtype.md)|Tipo de datos de uso compartido está permitido. Los valores posibles son: `deviceDefault`, `preventAny`, `allowPersonalToWork` y `noRestrictions`.|
|workProfileBlockNotificationsWhileDeviceLocked|Booleano|Indica si se deben bloquear las notificaciones al dispositivo bloqueado.|
|workProfileBlockAddingAccounts|Booleano|Impedir que los usuarios agregar o quitar cuentas en el perfil de trabajo.|
|workProfileBluetoothEnableContactSharing|Booleano|Permitir que los dispositivos bluetooth tener acceso a los contactos de la empresa.|
|workProfileBlockScreenCapture|Booleano|Captura de pantalla de bloque en el perfil de trabajo.|
|workProfileBlockCrossProfileCallerId|Booleano|Identificador de autor de la llamada de perfil bloque para mostrar trabajo en perfil personal.|
|workProfileBlockCamera|Booleano|Cámara de perfil de trabajo de bloque.|
|workProfileBlockCrossProfileContactsSearch|Booleano|Disponibilidad de los contactos del perfil de trabajo bloque en perfil personal.|
|workProfileBlockCrossProfileCopyPaste|Booleano|Valor booleano que indica si la opción no permitir la entre perfil copiado y pegado está habilitado.|
|workProfileDefaultAppPermissionPolicy|[androidWorkProfileDefaultAppPermissionPolicyType](../resources/intune_deviceconfig_androidworkprofiledefaultapppermissionpolicytype.md)|Tipo de contraseña que es necesario. Los valores posibles son: `deviceDefault`, `prompt`, `autoGrant` y `autoDeny`.|
|workProfilePasswordBlockFingerprintUnlock|Booleano|Indica si se deben bloquear la huella digital de desbloqueo para el perfil de trabajo.|
|workProfilePasswordBlockTrustAgents|Booleano|Indica si se deben bloquear bloqueo inteligentes y otros agentes de confianza para el perfil de trabajo.|
|workProfilePasswordExpirationDays|Int32|Expira el número de días antes de la contraseña de perfil de trabajo. Valores válidos de 1 a 365|
|workProfilePasswordMinimumLength|Int32|Longitud mínima de contraseña de perfil de trabajo. Valores válidos de 4 a 16|
|workProfilePasswordMinNumericCharacters|Int32|Nº mínimo de caracteres numéricos que requiere en contraseña de perfil de trabajo. Valores válidos de 1 a 10|
|workProfilePasswordMinNonLetterCharacters|Int32|Nº mínimo de caracteres que no sea una letra requeridas contraseña de perfil de trabajo. Valores válidos de 1 a 10|
|workProfilePasswordMinLetterCharacters|Int32|Nº mínimo de caracteres de letra requeridas contraseña de perfil de trabajo. Valores válidos de 1 a 10|
|workProfilePasswordMinLowerCaseCharacters|Int32|Nº mínimo de caracteres minúsculas requeridas contraseña de perfil de trabajo. Valores válidos de 1 a 10|
|workProfilePasswordMinUpperCaseCharacters|Int32|Nº mínimo de caracteres en mayúsculas requeridas contraseña de perfil de trabajo. Valores válidos de 1 a 10|
|workProfilePasswordMinSymbolCharacters|Int32|Nº mínimo de símbolos requeridas contraseña de perfil de trabajo. Valores válidos de 1 a 10|
|workProfilePasswordMinutesOfInactivityBeforeScreenTimeout|Int32|Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.|
|workProfilePasswordPreviousPasswordBlockCount|Int32|Número de contraseñas de perfil de trabajo anterior a bloquear. Valores válidos de 0 a 24|
|workProfilePasswordSignInFailureCountBeforeFactoryReset|Int32|Número de errores permitidos antes de que se ha quitado el perfil de trabajo y todos los datos corporativos eliminados de inicio de sesión. Valores válidos de 4 a 11|
|workProfilePasswordRequiredType|[androidWorkProfileRequiredPasswordType](../resources/intune_deviceconfig_androidworkprofilerequiredpasswordtype.md)|Tipo de contraseña de perfil de trabajo que se requiere. Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.|
|workProfileRequirePassword|Booleano|Se requiere contraseña o no para el perfil de trabajo|
|securityRequireVerifyApps|Booleano|Requerir que la característica Verificar aplicaciones de Android esté activada.|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune_deviceconfig_androidworkprofilegeneraldeviceconfiguration.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1831

{
  "@odata.type": "#microsoft.graph.androidWorkProfileGeneralDeviceConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passwordBlockFingerprintUnlock": true,
  "passwordBlockTrustAgents": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "lowSecurityBiometric",
  "workProfileDataSharingType": "preventAny",
  "workProfileBlockNotificationsWhileDeviceLocked": true,
  "workProfileBlockAddingAccounts": true,
  "workProfileBluetoothEnableContactSharing": true,
  "workProfileBlockScreenCapture": true,
  "workProfileBlockCrossProfileCallerId": true,
  "workProfileBlockCamera": true,
  "workProfileBlockCrossProfileContactsSearch": true,
  "workProfileBlockCrossProfileCopyPaste": true,
  "workProfileDefaultAppPermissionPolicy": "prompt",
  "workProfilePasswordBlockFingerprintUnlock": true,
  "workProfilePasswordBlockTrustAgents": true,
  "workProfilePasswordExpirationDays": 1,
  "workProfilePasswordMinimumLength": 0,
  "workProfilePasswordMinNumericCharacters": 7,
  "workProfilePasswordMinNonLetterCharacters": 9,
  "workProfilePasswordMinLetterCharacters": 6,
  "workProfilePasswordMinLowerCaseCharacters": 9,
  "workProfilePasswordMinUpperCaseCharacters": 9,
  "workProfilePasswordMinSymbolCharacters": 6,
  "workProfilePasswordMinutesOfInactivityBeforeScreenTimeout": 9,
  "workProfilePasswordPreviousPasswordBlockCount": 13,
  "workProfilePasswordSignInFailureCountBeforeFactoryReset": 7,
  "workProfilePasswordRequiredType": "lowSecurityBiometric",
  "workProfileRequirePassword": true,
  "securityRequireVerifyApps": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 2003

{
  "@odata.type": "#microsoft.graph.androidWorkProfileGeneralDeviceConfiguration",
  "id": "6decda7e-da7e-6dec-7eda-ec6d7edaec6d",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passwordBlockFingerprintUnlock": true,
  "passwordBlockTrustAgents": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "lowSecurityBiometric",
  "workProfileDataSharingType": "preventAny",
  "workProfileBlockNotificationsWhileDeviceLocked": true,
  "workProfileBlockAddingAccounts": true,
  "workProfileBluetoothEnableContactSharing": true,
  "workProfileBlockScreenCapture": true,
  "workProfileBlockCrossProfileCallerId": true,
  "workProfileBlockCamera": true,
  "workProfileBlockCrossProfileContactsSearch": true,
  "workProfileBlockCrossProfileCopyPaste": true,
  "workProfileDefaultAppPermissionPolicy": "prompt",
  "workProfilePasswordBlockFingerprintUnlock": true,
  "workProfilePasswordBlockTrustAgents": true,
  "workProfilePasswordExpirationDays": 1,
  "workProfilePasswordMinimumLength": 0,
  "workProfilePasswordMinNumericCharacters": 7,
  "workProfilePasswordMinNonLetterCharacters": 9,
  "workProfilePasswordMinLetterCharacters": 6,
  "workProfilePasswordMinLowerCaseCharacters": 9,
  "workProfilePasswordMinUpperCaseCharacters": 9,
  "workProfilePasswordMinSymbolCharacters": 6,
  "workProfilePasswordMinutesOfInactivityBeforeScreenTimeout": 9,
  "workProfilePasswordPreviousPasswordBlockCount": 13,
  "workProfilePasswordSignInFailureCountBeforeFactoryReset": 7,
  "workProfilePasswordRequiredType": "lowSecurityBiometric",
  "workProfileRequirePassword": true,
  "securityRequireVerifyApps": true
}
```



