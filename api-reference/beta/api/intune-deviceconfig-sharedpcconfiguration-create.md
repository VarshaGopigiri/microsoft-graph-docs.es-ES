---
title: Crear sharedPCConfiguration
description: Crear un objeto sharedPCConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 605c0dae9ee65f81527247dfca818d51b1728544
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27926207"
---
# <a name="create-sharedpcconfiguration"></a>Crear sharedPCConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Crear un objeto [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md).
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
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto sharedPCConfiguration.

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto sharedPCConfiguration.

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



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1179

{
  "@odata.type": "#microsoft.graph.sharedPCConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountManagerPolicy": {
    "@odata.type": "microsoft.graph.sharedPCAccountManagerPolicy",
    "accountDeletionPolicy": "diskSpaceThreshold",
    "cacheAccountsAboveDiskFreePercentage": 4,
    "inactiveThresholdDays": 5,
    "removeAccountsBelowDiskFreePercentage": 5
  },
  "allowedAccounts": "domain",
  "localStorage": "enabled",
  "allowLocalStorage": true,
  "setAccountManager": "enabled",
  "disableAccountManager": true,
  "setEduPolicies": "enabled",
  "disableEduPolicies": true,
  "setPowerPolicies": "enabled",
  "disablePowerPolicies": true,
  "signInOnResume": "enabled",
  "disableSignInOnResume": true,
  "enabled": true,
  "idleTimeBeforeSleepInSeconds": 12,
  "kioskAppDisplayName": "Kiosk App Display Name value",
  "kioskAppUserModelId": "Kiosk App User Model Id value",
  "maintenanceStartTime": "11:59:24.7240000"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1287

{
  "@odata.type": "#microsoft.graph.sharedPCConfiguration",
  "id": "5206be3b-be3b-5206-3bbe-06523bbe0652",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountManagerPolicy": {
    "@odata.type": "microsoft.graph.sharedPCAccountManagerPolicy",
    "accountDeletionPolicy": "diskSpaceThreshold",
    "cacheAccountsAboveDiskFreePercentage": 4,
    "inactiveThresholdDays": 5,
    "removeAccountsBelowDiskFreePercentage": 5
  },
  "allowedAccounts": "domain",
  "localStorage": "enabled",
  "allowLocalStorage": true,
  "setAccountManager": "enabled",
  "disableAccountManager": true,
  "setEduPolicies": "enabled",
  "disableEduPolicies": true,
  "setPowerPolicies": "enabled",
  "disablePowerPolicies": true,
  "signInOnResume": "enabled",
  "disableSignInOnResume": true,
  "enabled": true,
  "idleTimeBeforeSleepInSeconds": 12,
  "kioskAppDisplayName": "Kiosk App Display Name value",
  "kioskAppUserModelId": "Kiosk App User Model Id value",
  "maintenanceStartTime": "11:59:24.7240000"
}
```





