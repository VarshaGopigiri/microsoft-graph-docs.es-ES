---
title: tipo de recurso hardwareInformation
description: Información de hardware de un dispositivo determinado.
author: tfitzmac
ms.openlocfilehash: c483aa800d920a50392d21c326cd20dea7b72e18
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334527"
---
# <a name="hardwareinformation-resource-type"></a>tipo de recurso hardwareInformation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Información de hardware de un dispositivo determinado.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|serialNumber|String|Número de serie.|
|totalStorageSpace|Int64|Espacio de almacenamiento total del dispositivo.|
|freeStorageSpace|Int64|Espacio de almacenamiento libre del dispositivo.|
|imei|String|IMEI|
|meid|String|MEID|
|manufacturer|String|Fabricante del dispositivo.|
|model|String|Modelo del dispositivo.|
|phoneNumber|String|Número de teléfono del dispositivo.|
|subscriberCarrier|String|Operador de suscriptor del dispositivo|
|cellularTechnology|String|Tecnología de telefonía móvil del dispositivo|
|wifiMac|String|Dirección MAC de WiFi del dispositivo|
|operatingSystemLanguage|String|Idioma del sistema operativo del dispositivo|
|isSupervised|Boolean|Modo de supervisión del dispositivo|
|isEncrypted|Boolean|Estado de cifrado del dispositivo|
|isSharedDevice|Boolean|IPad compartida|
|sharedDeviceCachedUsers|colección de [sharedAppleDeviceUser](../resources/intune-devices-sharedappledeviceuser.md)|Todos los usuarios en el dispositivo de Apple compartido|
|tpmSpecificationVersion|String|Cadena que especifica la versión de la especificación.|
|operatingSystemEdition|String|Cadena que especifica la edición del sistema operativo.|
|deviceFullQualifiedDomainName|String|Devuelve el nombre de dominio completo del dispositivo (si hay alguno). Si el dispositivo no está unido a un dominio, devuelve una cadena vacía. |
|deviceGuardVirtualizationBasedSecurityHardwareRequirementState|[deviceGuardVirtualizationBasedSecurityHardwareRequirementState](../resources/intune-devices-deviceguardvirtualizationbasedsecurityhardwarerequirementstate.md)|Estado de requisitos de hardware de seguridad basada en la virtualización. Los valores posibles son: `meetHardwareRequirements`, `secureBootRequired`, `dmaProtectionRequired`, `hyperVNotSupportedForGuestVM` y `hyperVNotAvailable`.|
|deviceGuardVirtualizationBasedSecurityState|[deviceGuardVirtualizationBasedSecurityState](../resources/intune-devices-deviceguardvirtualizationbasedsecuritystate.md)|Estado de la seguridad basada en la virtualización. . Los valores posibles son: `running`, `rebootRequired`, `require64BitArchitecture`, `notLicensed`, `notConfigured`, `doesNotMeetHardwareRequirements` y `other`.|
|deviceGuardLocalSystemAuthorityCredentialGuardState|[deviceGuardLocalSystemAuthorityCredentialGuardState](../resources/intune-devices-deviceguardlocalsystemauthoritycredentialguardstate.md)|Estado de guard de credencial de autoridad del sistema (LSA) local. . Los valores posibles son: `running`, `rebootRequired`, `notLicensed`, `notConfigured` y `virtualizationBasedSecurityNotRunning`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.hardwareInformation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.hardwareInformation",
  "serialNumber": "String",
  "totalStorageSpace": 1024,
  "freeStorageSpace": 1024,
  "imei": "String",
  "meid": "String",
  "manufacturer": "String",
  "model": "String",
  "phoneNumber": "String",
  "subscriberCarrier": "String",
  "cellularTechnology": "String",
  "wifiMac": "String",
  "operatingSystemLanguage": "String",
  "isSupervised": true,
  "isEncrypted": true,
  "isSharedDevice": true,
  "sharedDeviceCachedUsers": [
    {
      "@odata.type": "microsoft.graph.sharedAppleDeviceUser",
      "userPrincipalName": "String",
      "dataToSync": true,
      "dataQuota": 1024,
      "dataUsed": 1024
    }
  ],
  "tpmSpecificationVersion": "String",
  "operatingSystemEdition": "String",
  "deviceFullQualifiedDomainName": "String",
  "deviceGuardVirtualizationBasedSecurityHardwareRequirementState": "String",
  "deviceGuardVirtualizationBasedSecurityState": "String",
  "deviceGuardLocalSystemAuthorityCredentialGuardState": "String"
}
```





