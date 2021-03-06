---
title: Tipo de recurso androidCompliancePolicy
description: Esta clase contiene la configuración de cumplimiento para Android.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0c3455767e30b83decdd99e73bb918ed5efcb38a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851201"
---
# <a name="androidcompliancepolicy-resource-type"></a>Tipo de recurso androidCompliancePolicy

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Esta clase contiene la configuración de cumplimiento para Android.

Hereda de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar androidCompliancePolicies](../api/intune-deviceconfig-androidcompliancepolicy-list.md)|Colección [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md)|Enumere las propiedades y las relaciones de los objetos [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md).|
|[Obtener androidCompliancePolicy](../api/intune-deviceconfig-androidcompliancepolicy-get.md)|[androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md)|Lea las propiedades y las relaciones del objeto [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md).|
|[Crear androidCompliancePolicy](../api/intune-deviceconfig-androidcompliancepolicy-create.md)|[androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md)|Cree un objeto [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md).|
|[Eliminar androidCompliancePolicy](../api/intune-deviceconfig-androidcompliancepolicy-delete.md)|Ninguna|Elimina un [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md).|
|[Actualizar androidCompliancePolicy](../api/intune-deviceconfig-androidcompliancepolicy-update.md)|[androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md)|Actualice las propiedades de un objeto [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|roleScopeTagIds|Colección String|Lista de etiquetas de ámbito para esta instancia de entidad. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|id|Cadena|Clave de la entidad. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|passwordRequired|Booleano|Exigir una contraseña para desbloquear el dispositivo.|
|passwordMinimumLength|Int32|Longitud mínima de la contraseña. Valores válidos de 4 a 16|
|passwordRequiredType|[androidRequiredPasswordType](../resources/intune-deviceconfig-androidrequiredpasswordtype.md)|Tipo de caracteres de contraseña. Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.|
|passwordMinutesOfInactivityBeforeLock|Int32|Minutos de inactividad antes de que sea necesaria una contraseña.|
|passwordExpirationDays|Int32|Número de días antes de que expire la contraseña. Valores válidos de 1 a 65535|
|passwordPreviousPasswordBlockCount|Int32|Número de contraseñas anteriores que bloquear.|
|securityPreventInstallAppsFromUnknownSources|Booleano|Exigir que los dispositivos impidan la instalación de aplicaciones de orígenes desconocidos.|
|securityDisableUsbDebugging|Booleano|Deshabilitar la depuración USB en dispositivos Android.|
|securityRequireVerifyApps|Booleano|Exigir que la característica Verificar aplicaciones de Android esté activada.|
|deviceThreatProtectionEnabled|Booleano|Exigir que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.|
|deviceThreatProtectionRequiredSecurityLevel|[deviceThreatProtectionLevel](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento. Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.|
|securityBlockJailbrokenDevices|Booleano|No pueden usarse dispositivos con jailbreak o rooting.|
|osMinimumVersion|Cadena|Versión mínima de Android.|
|osMaximumVersion|Cadena|Versión máxima de Android.|
|minAndroidSecurityPatchLevel|Cadena|Nivel de revisión de seguridad mínimo de Android.|
|storageRequireEncryption|Booleano|Exigir cifrado en dispositivos Android.|
|securityRequireSafetyNetAttestationBasicIntegrity|Booleano|Exigir que el dispositivo supere la comprobación de integridad básica de SafetyNet.|
|securityRequireSafetyNetAttestationCertifiedDevice|Booleano|Exigir que el dispositivo supere la comprobación de dispositivos certificados de SafetyNet.|
|securityRequireGooglePlayServices|Booleano|Exigir que Google Play Services esté instalado y habilitado en el dispositivo.|
|securityRequireUpToDateSecurityProviders|Booleano|Exigir que el dispositivo tenga los proveedores de seguridad actualizados. El dispositivo requerirá que Google Play Services esté instalado y habilitado.|
|securityRequireCompanyPortalAppIntegrity|Booleano|Exigir que el dispositivo supere la comprobación de integridad en tiempo de ejecución de la aplicación cliente del Portal de empresa.|
|conditionStatementId|Cadena|Identificador de instrucción de condición.|
|restrictedApps|Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)|Requiere que el dispositivo no contar con las aplicaciones especificadas instaladas. Esta colección puede contener un máximo de 10 000 elementos.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|scheduledActionsForRule|Colección [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md)|La lista de acción programada para esta regla. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)|
|deviceStatuses|Colección [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md)|Lista de DeviceComplianceDeviceStatus. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)|
|userStatuses|Colección [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md)|Lista de DeviceComplianceUserStatus. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)|
|deviceStatusOverview|[deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md)|Información general sobre el estado de dispositivos del cumplimiento de dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)|
|userStatusOverview|[deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md)|Información general sobre el estado de usuarios del cumplimiento de dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Resumen de dispositivo sobre el estado de configuración de cumplimiento. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)|
|asignaciones|Colección [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)|El conjunto de asignaciones para esta directiva de cumplimiento. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidCompliancePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidCompliancePolicy",
  "roleScopeTagIds": [
    "String"
  ],
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024,
  "passwordRequired": true,
  "passwordMinimumLength": 1024,
  "passwordRequiredType": "String",
  "passwordMinutesOfInactivityBeforeLock": 1024,
  "passwordExpirationDays": 1024,
  "passwordPreviousPasswordBlockCount": 1024,
  "securityPreventInstallAppsFromUnknownSources": true,
  "securityDisableUsbDebugging": true,
  "securityRequireVerifyApps": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "String",
  "securityBlockJailbrokenDevices": true,
  "osMinimumVersion": "String",
  "osMaximumVersion": "String",
  "minAndroidSecurityPatchLevel": "String",
  "storageRequireEncryption": true,
  "securityRequireSafetyNetAttestationBasicIntegrity": true,
  "securityRequireSafetyNetAttestationCertifiedDevice": true,
  "securityRequireGooglePlayServices": true,
  "securityRequireUpToDateSecurityProviders": true,
  "securityRequireCompanyPortalAppIntegrity": true,
  "conditionStatementId": "String",
  "restrictedApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ]
}
```





