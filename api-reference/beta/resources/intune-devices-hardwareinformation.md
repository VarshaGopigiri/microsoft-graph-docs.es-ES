---
title: tipo de recurso hardwareInformation
description: Información de hardware de un dispositivo determinado.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 2684f1ff7e7a6407942ac61fae7d45ead16820d2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831830"
---
# <a name="hardwareinformation-resource-type"></a>tipo de recurso hardwareInformation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Información de hardware de un dispositivo determinado.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|serialNumber|Cadena|Número de serie.|
|totalStorageSpace|Int64|Espacio de almacenamiento total del dispositivo.|
|freeStorageSpace|Int64|Espacio de almacenamiento libre del dispositivo.|
|imei|Cadena|IMEI|
|meid|Cadena|MEID|
|manufacturer|Cadena|Fabricante del dispositivo.|
|model|Cadena|Modelo del dispositivo.|
|phoneNumber|Cadena|Número de teléfono del dispositivo.|
|subscriberCarrier|Cadena|Operador de suscriptor del dispositivo|
|cellularTechnology|Cadena|Tecnología de telefonía móvil del dispositivo|
|wifiMac|Cadena|Dirección MAC de WiFi del dispositivo|
|operatingSystemLanguage|Cadena|Idioma del sistema operativo del dispositivo|
|isSupervised|Booleano|Modo de supervisión del dispositivo|
|isEncrypted|Booleano|Estado de cifrado del dispositivo|
|isSharedDevice|Booleano|IPad compartida|
|sharedDeviceCachedUsers|colección de [sharedAppleDeviceUser](../resources/intune-devices-sharedappledeviceuser.md)|Todos los usuarios en el dispositivo de Apple compartido|
|tpmSpecificationVersion|Cadena|Cadena que especifica la versión de la especificación.|
|operatingSystemEdition|Cadena|Cadena que especifica la edición del sistema operativo.|
|deviceFullQualifiedDomainName|Cadena|Devuelve el nombre de dominio completo del dispositivo (si hay alguno). Si el dispositivo no está unido a un dominio, devuelve una cadena vacía. |
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





