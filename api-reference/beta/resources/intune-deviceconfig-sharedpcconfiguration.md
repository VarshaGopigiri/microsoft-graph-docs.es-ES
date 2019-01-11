---
title: Tipo de recurso sharedPCConfiguration
description: Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso sharedPCConfiguration.
localization_priority: Normal
ms.openlocfilehash: 8671d4a5241439eaec12e09e250eff1b2caa4592
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831139"
---
# <a name="sharedpcconfiguration-resource-type"></a>Tipo de recurso sharedPCConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso sharedPCConfiguration.

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar sharedPCConfigurations](../api/intune-deviceconfig-sharedpcconfiguration-list.md)|Colección [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md).|
|[Obtener sharedPCConfiguration](../api/intune-deviceconfig-sharedpcconfiguration-get.md)|[sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md)|Lea las propiedades y las relaciones del objeto [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md).|
|[Crear sharedPCConfiguration](../api/intune-deviceconfig-sharedpcconfiguration-create.md)|[sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md)|Cree un objeto [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md).|
|[Eliminar sharedPCConfiguration](../api/intune-deviceconfig-sharedpcconfiguration-delete.md)|Ninguna|Elimina un [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md).|
|[Actualizar sharedPCConfiguration](../api/intune-deviceconfig-sharedpcconfiguration-update.md)|[sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md)|Actualice las propiedades de un objeto [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|roleScopeTagIds|Colección String|Lista de etiquetas de ámbito para esta instancia de entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|supportsScopeTags|Booleano|Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito. No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito. Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure. Esta propiedad es de sólo lectura. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|accountManagerPolicy|[sharedPCAccountManagerPolicy](../resources/intune-deviceconfig-sharedpcaccountmanagerpolicy.md)|Especifica cómo se administran las cuentas en un equipo compartido. Solo se aplica cuando disableAccountManager es False.|
|allowedAccounts|[sharedPCAllowedAccountType](../resources/intune-deviceconfig-sharedpcallowedaccounttype.md)|Indica el tipo de cuentas que se pueden usar en un equipo compartido. Los valores posibles son: `guest` y `domain`.|
|localStorage|[Habilitación de](../resources/intune-shared-enablement.md)|Especifica si se permite el almacenamiento local en un equipo compartido. Los valores posibles son: `notConfigured`, `enabled` y `disabled`.|
|allowLocalStorage|Booleano|Especifica si se permite el almacenamiento local en un equipo compartido.|
|setAccountManager|[Habilitación de](../resources/intune-shared-enablement.md)|Deshabilita al administrador de cuentas para el modo de equipo compartido. Los valores posibles son: `notConfigured`, `enabled` y `disabled`.|
|disableAccountManager|Booleano|Deshabilita al administrador de cuentas para el modo de equipo compartido.|
|setEduPolicies|[Habilitación de](../resources/intune-shared-enablement.md)|Especifica si las directivas de entorno compartido predeterminado el ámbito educativo de PC deben ser habilitado o deshabilitado o no configuradas. Para Windows 10 RS2 y versiones posteriores, se aplicará esta directiva sin establecer Habilitado en true. Los valores posibles son: `notConfigured`, `enabled` y `disabled`.|
|disableEduPolicies|Booleano|Especifica si se deben deshabilitar las directivas predeterminadas de entorno educativo de equipo compartido. Para Windows 10 RS2 y versiones posteriores, se aplicará esta directiva sin establecer Habilitado en true.|
|setPowerPolicies|[Habilitación de](../resources/intune-shared-enablement.md)|Especifica si las directivas de power PC compartido predeterminado deben estar habilitado o deshabilitado. Los valores posibles son: `notConfigured`, `enabled` y `disabled`.|
|disablePowerPolicies|Booleano|Especifica si se deben deshabilitar las directivas predeterminadas de energía de equipo compartido.|
|signInOnResume|[Habilitación de](../resources/intune-shared-enablement.md)|Especifica el requisito para iniciar sesión en cada vez que el dispositivo se reactiva copia de seguridad del modo de suspensión. Los valores posibles son: `notConfigured`, `enabled` y `disabled`.|
|disableSignInOnResume|Booleano|Deshabilita el requisito de iniciar sesión siempre que el dispositivo salga del modo de suspensión.|
|enabled|Booleano|Habilita el modo de equipo compartido y se aplica a las directivas de equipo compartido.|
|idleTimeBeforeSleepInSeconds|Int32|Especifica el tiempo en segundos que un dispositivo debe permanecer inactivo antes de que el equipo pase al estado de suspensión. Si este valor se establece en 0 impide que se produzca el tiempo de espera en suspensión.|
|kioskAppDisplayName|Cadena|Especifica el texto para mostrar de la cuenta que se muestra en la pantalla de inicio de sesión que inicia la aplicación especificada por SetKioskAppUserModelId. Solo se aplica cuando se establece KioskAppUserModelId.|
|kioskAppUserModelId|Cadena|Especifica el identificador del modelo de usuario de la aplicación correspondiente a la aplicación para que se use con el acceso asignado.|
|maintenanceStartTime|TimeOfDay|Especifica la hora de inicio diaria de la hora de mantenimiento.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Description|
|:---|:---|:---|
|groupAssignments|colección de [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md)|La lista de asignaciones de grupo para el perfil de configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
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
  "@odata.type": "microsoft.graph.sharedPCConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.sharedPCConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "roleScopeTagIds": [
    "String"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "accountManagerPolicy": {
    "@odata.type": "microsoft.graph.sharedPCAccountManagerPolicy",
    "accountDeletionPolicy": "String",
    "cacheAccountsAboveDiskFreePercentage": 1024,
    "inactiveThresholdDays": 1024,
    "removeAccountsBelowDiskFreePercentage": 1024
  },
  "allowedAccounts": "String",
  "localStorage": "String",
  "allowLocalStorage": true,
  "setAccountManager": "String",
  "disableAccountManager": true,
  "setEduPolicies": "String",
  "disableEduPolicies": true,
  "setPowerPolicies": "String",
  "disablePowerPolicies": true,
  "signInOnResume": "String",
  "disableSignInOnResume": true,
  "enabled": true,
  "idleTimeBeforeSleepInSeconds": 1024,
  "kioskAppDisplayName": "String",
  "kioskAppUserModelId": "String",
  "maintenanceStartTime": "String (time of day)"
}
```





