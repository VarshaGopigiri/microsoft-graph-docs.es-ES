---
title: tipo de recurso androidWorkProfileGeneralDeviceConfiguration
description: Configuración de dispositivo general de perfil de trabajo Android.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a8f64683e391296befae8c33a7aaa3c28629ca33
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880188"
---
# <a name="androidworkprofilegeneraldeviceconfiguration-resource-type"></a>tipo de recurso androidWorkProfileGeneralDeviceConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de dispositivo general de perfil de trabajo Android.

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista androidWorkProfileGeneralDeviceConfigurations](../api/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration-list.md)|colección de [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md)|Propiedades de la lista y relaciones de los objetos [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .|
|[Obtener androidWorkProfileGeneralDeviceConfiguration](../api/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration-get.md)|[androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md)|Leer las propiedades y las relaciones del objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .|
|[Crear androidWorkProfileGeneralDeviceConfiguration](../api/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration-create.md)|[androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md)|Crear un nuevo objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .|
|[Eliminar androidWorkProfileGeneralDeviceConfiguration](../api/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration-delete.md)|Ninguno|Elimina un [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md).|
|[Actualizar androidWorkProfileGeneralDeviceConfiguration](../api/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration-update.md)|[androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md)|Actualizar las propiedades de un objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|passwordBlockFingerprintUnlock|Booleano|Indica si se va a impedir el desbloqueo por huella dactilar.|
|passwordBlockTrustAgents|Booleano|Indica si se van a bloquear Smart Lock y otros agentes de confianza.|
|passwordExpirationDays|Int32|Número de días antes de que expire la contraseña. Valores válidos de 1 a 365|
|passwordMinimumLength|Int32|Longitud mínima de las contraseñas. Valores válidos de 4 a 16|
|passwordMinutesOfInactivityBeforeScreenTimeout|Int32|Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.|
|passwordPreviousPasswordBlockCount|Int32|Número de contraseñas anteriores que bloquear. Valores válidos de 0 a 24|
|passwordSignInFailureCountBeforeFactoryReset|Int32|Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica. Valores válidos de 4 a 11|
|passwordRequiredType|[androidWorkProfileRequiredPasswordType](../resources/intune-deviceconfig-androidworkprofilerequiredpasswordtype.md)|Tipo de contraseña que es necesario. Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.|
|workProfileDataSharingType|[androidWorkProfileCrossProfileDataSharingType](../resources/intune-deviceconfig-androidworkprofilecrossprofiledatasharingtype.md)|Tipo de datos de uso compartido está permitido. Los valores posibles son: `deviceDefault`, `preventAny`, `allowPersonalToWork` y `noRestrictions`.|
|workProfileBlockNotificationsWhileDeviceLocked|Booleano|Indica si se deben bloquear las notificaciones al dispositivo bloqueado.|
|workProfileBlockAddingAccounts|Booleano|Impedir que los usuarios agregar o quitar cuentas en el perfil de trabajo.|
|workProfileBluetoothEnableContactSharing|Booleano|Permitir que los dispositivos bluetooth tener acceso a los contactos de la empresa.|
|workProfileBlockScreenCapture|Booleano|Captura de pantalla de bloque en el perfil de trabajo.|
|workProfileBlockCrossProfileCallerId|Booleano|Identificador de autor de la llamada de perfil bloque para mostrar trabajo en perfil personal.|
|workProfileBlockCamera|Booleano|Cámara de perfil de trabajo de bloque.|
|workProfileBlockCrossProfileContactsSearch|Booleano|Disponibilidad de los contactos del perfil de trabajo bloque en perfil personal.|
|workProfileBlockCrossProfileCopyPaste|Booleano|Valor booleano que indica si la opción no permitir la entre perfil copiado y pegado está habilitado.|
|workProfileDefaultAppPermissionPolicy|[androidWorkProfileDefaultAppPermissionPolicyType](../resources/intune-deviceconfig-androidworkprofiledefaultapppermissionpolicytype.md)|Tipo de contraseña que es necesario. Los valores posibles son: `deviceDefault`, `prompt`, `autoGrant` y `autoDeny`.|
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
|workProfilePasswordRequiredType|[androidWorkProfileRequiredPasswordType](../resources/intune-deviceconfig-androidworkprofilerequiredpasswordtype.md)|Tipo de contraseña de perfil de trabajo que se requiere. Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.|
|workProfileRequirePassword|Booleano|Se requiere contraseña o no para el perfil de trabajo|
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
  "@odata.type": "microsoft.graph.androidWorkProfileGeneralDeviceConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidWorkProfileGeneralDeviceConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "passwordBlockFingerprintUnlock": true,
  "passwordBlockTrustAgents": true,
  "passwordExpirationDays": 1024,
  "passwordMinimumLength": 1024,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 1024,
  "passwordPreviousPasswordBlockCount": 1024,
  "passwordSignInFailureCountBeforeFactoryReset": 1024,
  "passwordRequiredType": "String",
  "workProfileDataSharingType": "String",
  "workProfileBlockNotificationsWhileDeviceLocked": true,
  "workProfileBlockAddingAccounts": true,
  "workProfileBluetoothEnableContactSharing": true,
  "workProfileBlockScreenCapture": true,
  "workProfileBlockCrossProfileCallerId": true,
  "workProfileBlockCamera": true,
  "workProfileBlockCrossProfileContactsSearch": true,
  "workProfileBlockCrossProfileCopyPaste": true,
  "workProfileDefaultAppPermissionPolicy": "String",
  "workProfilePasswordBlockFingerprintUnlock": true,
  "workProfilePasswordBlockTrustAgents": true,
  "workProfilePasswordExpirationDays": 1024,
  "workProfilePasswordMinimumLength": 1024,
  "workProfilePasswordMinNumericCharacters": 1024,
  "workProfilePasswordMinNonLetterCharacters": 1024,
  "workProfilePasswordMinLetterCharacters": 1024,
  "workProfilePasswordMinLowerCaseCharacters": 1024,
  "workProfilePasswordMinUpperCaseCharacters": 1024,
  "workProfilePasswordMinSymbolCharacters": 1024,
  "workProfilePasswordMinutesOfInactivityBeforeScreenTimeout": 1024,
  "workProfilePasswordPreviousPasswordBlockCount": 1024,
  "workProfilePasswordSignInFailureCountBeforeFactoryReset": 1024,
  "workProfilePasswordRequiredType": "String",
  "workProfileRequirePassword": true,
  "securityRequireVerifyApps": true
}
```



