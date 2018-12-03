---
title: tipo de recurso windowsIdentityProtectionConfiguration
description: Esta entidad ofrece descripciones de los métodos declarados, propiedades y relaciones expuestas por Windows Hello para la empresa.
ms.openlocfilehash: 0ac5c291dd85d3ac94378a74ee879bfab2685827
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083118"
---
# <a name="windowsidentityprotectionconfiguration-resource-type"></a>tipo de recurso windowsIdentityProtectionConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Esta entidad ofrece descripciones de los métodos declarados, propiedades y relaciones expuestas por Windows Hello para la empresa.

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista windowsIdentityProtectionConfigurations](../api/intune-deviceconfig-windowsidentityprotectionconfiguration-list.md)|colección de [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md)|Propiedades de la lista y relaciones de los objetos [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) .|
|[Obtener windowsIdentityProtectionConfiguration](../api/intune-deviceconfig-windowsidentityprotectionconfiguration-get.md)|[windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md)|Leer las propiedades y las relaciones del objeto [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) .|
|[Crear windowsIdentityProtectionConfiguration](../api/intune-deviceconfig-windowsidentityprotectionconfiguration-create.md)|[windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md)|Crear un nuevo objeto [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) .|
|[Eliminar windowsIdentityProtectionConfiguration](../api/intune-deviceconfig-windowsidentityprotectionconfiguration-delete.md)|Ninguno|Elimina un [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md).|
|[Actualizar windowsIdentityProtectionConfiguration](../api/intune-deviceconfig-windowsidentityprotectionconfiguration-update.md)|[windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md)|Actualizar las propiedades de un objeto [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|roleScopeTagIds|Colección String|Lista de etiquetas de ámbito para esta instancia de entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|supportsScopeTags|Booleano|Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito. No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito. Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure. Esta propiedad es de sólo lectura. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|enhancedAntiSpoofingForFacialFeaturesEnabled|Booleano|Valor booleano que se usa para permitir mejorada contra la suplantación de reconocimiento de característica faciales acerca de la autenticación de Windows Hola cara.|
|pinMinimumLength|Int32|Valor entero que establece el número mínimo de caracteres necesarios para el Windows Hello de PIN de negocio. Los valores válidos son de 4 a 127 inclusive y menor o igual que el valor establecido para el PIN máximo. Valores válidos 4 a 127|
|pinMaximumLength|Int32|Valor entero que establece el número máximo de caracteres permitidos para el trabajo PIN. Los valores válidos son de 4 a 127 inclusive y mayor o igual que el valor establecido para el PIN mínimo. Valores válidos 4 a 127|
|pinUppercaseCharactersUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Este valor configura el uso de caracteres en mayúsculas en el Windows Hello para profesionales PIN. Los valores posibles son: `blocked`, `required` y `allowed`.|
|pinLowercaseCharactersUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Este valor configura el uso de caracteres en minúsculas en el Windows Hello para profesionales PIN. Los valores posibles son: `blocked`, `required` y `allowed`.|
|pinSpecialCharactersUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Controla la capacidad de usar caracteres especiales en el Windows Hello para profesionales PIN. Los valores posibles son: `blocked`, `required` y `allowed`.|
|pinExpirationInDays|Int32|Valor entero especifica el período (en días) que se puede usar un NIP antes de que el sistema requiere que el usuario que la cambie. Los valores válidos son 0 a 730 inclusive. Valores válidos de 0 a 730.|
|pinPreviousBlockCount|Int32|Controla la capacidad para impedir que los usuarios utilicen más allá de los PIN. Esto se debe establecer entre 0 y 50, ambos inclusive, y el PIN del usuario actual se incluye en ese número. Si se establece en 0, anterior no se almacenan los PIN. No se conserva el historial de PIN a través de un PIN restablecer. Valores válidos de 0 a 50.|
|pinRecoveryEnabled|Booleano|Valor booleano que permite a un usuario cambiar su PIN mediante el Windows Hello para servicio de recuperación de PIN de negocio.|
|securityDeviceRequired|Booleano|Controla si se debe requerir un módulo de plataforma segura (TPM) para aprovisionamiento Windows Hello para la empresa. Un TPM proporciona una ventaja de seguridad adicional en que los datos almacenados en él no se puede usar en otros dispositivos. Si se establece en False, todos los dispositivos pueden aprovisionar Windows Hello para la empresa, incluso si no hay un TPM utilizable.|
|unlockWithBiometricsEnabled|Booleano|Controla el uso de gestos biométricas, como cara y de huella digital, como una alternativa a la Windows Hola de PIN de negocio.  Si se establece en False, biométricas gestos no se permite. Los usuarios aún deben configurar un PIN como una copia de seguridad en caso de errores.|
|useCertificatesForOnPremisesAuthEnabled|Booleano|Valor booleano que permite Windows Hello para la empresa a usar certificados para autenticar los recursos locales.|
|windowsHelloForBusinessBlocked|Booleano|Valor booleano que bloquea Windows Hello para la empresa como un método para iniciar sesión en Windows.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
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
  "@odata.type": "microsoft.graph.windowsIdentityProtectionConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsIdentityProtectionConfiguration",
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
  "enhancedAntiSpoofingForFacialFeaturesEnabled": true,
  "pinMinimumLength": 1024,
  "pinMaximumLength": 1024,
  "pinUppercaseCharactersUsage": "String",
  "pinLowercaseCharactersUsage": "String",
  "pinSpecialCharactersUsage": "String",
  "pinExpirationInDays": 1024,
  "pinPreviousBlockCount": 1024,
  "pinRecoveryEnabled": true,
  "securityDeviceRequired": true,
  "unlockWithBiometricsEnabled": true,
  "useCertificatesForOnPremisesAuthEnabled": true,
  "windowsHelloForBusinessBlocked": true
}
```





