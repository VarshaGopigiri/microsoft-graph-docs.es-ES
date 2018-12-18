---
title: tipo de recurso importedAppleDeviceIdentityResult
description: El recurso importedAppleDeviceIdentityResult representa el resultado de intentar importar las identidades de los dispositivos de Apple.
author: tfitzmac
ms.openlocfilehash: 650dfca3cba7800c2cdc9eb0087e9d67b8dc0b29
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344565"
---
# <a name="importedappledeviceidentityresult-resource-type"></a>tipo de recurso importedAppleDeviceIdentityResult

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso importedAppleDeviceIdentityResult representa el resultado de intentar importar las identidades de los dispositivos de Apple.

Hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista importedAppleDeviceIdentityResults](../api/intune-enrollment-importedappledeviceidentityresult-list.md)|colección de [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md)|Propiedades de la lista y relaciones de los objetos [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) .|
|[Obtener importedAppleDeviceIdentityResult](../api/intune-enrollment-importedappledeviceidentityresult-get.md)|[importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md)|Leer las propiedades y las relaciones del objeto [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) .|
|[Crear importedAppleDeviceIdentityResult](../api/intune-enrollment-importedappledeviceidentityresult-create.md)|[importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md)|Crear un nuevo objeto [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) .|
|[Eliminar importedAppleDeviceIdentityResult](../api/intune-enrollment-importedappledeviceidentityresult-delete.md)|Ninguno|Elimina un [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md).|
|[Actualizar importedAppleDeviceIdentityResult](../api/intune-enrollment-importedappledeviceidentityresult-update.md)|[importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md)|Actualizar las propiedades de un objeto [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|serialNumber|String|Número de serie del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|requestedEnrollmentProfileId|String|Administración de identificador de perfil de inscripción tenga la intención de aplicar al dispositivo durante la inscripción siguiente Inherited de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|requestedEnrollmentProfileAssignmentDateTime|DateTimeOffset|El perfil de tiempo de inscripción se asignó al dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|isSupervised|Boolean|Indica si el dispositivo de Apple es supervisado. Obtener más información se encuentra en: https://support.apple.com/en-us/HT202837 se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|discoverySource|[discoverySource](../resources/intune-enrollment-discoverysource.md)|Origen de detección del dispositivo de Apple. Se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md). Los valores posibles son: `unknown`, `adminImport` y `deviceEnrollmentProgram`.|
|createdDateTime|DateTimeOffset|Crear fecha hora del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|lastContactedDateTime|DateTimeOffset|Última vez fecha ponerse en contacto del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|descripción|String|La descripción del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|enrollmentState|[enrollmentState](../resources/intune-enrollment-enrollmentstate.md)|El estado del dispositivo en Intune se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md). Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.|
|platform|[plataforma](../resources/intune-enrollment-platform.md)|La plataforma del dispositivo. Se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md). Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.|
|status|Boolean|Estado de identidad de dispositivo importada|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.importedAppleDeviceIdentityResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.importedAppleDeviceIdentityResult",
  "id": "String (identifier)",
  "serialNumber": "String",
  "requestedEnrollmentProfileId": "String",
  "requestedEnrollmentProfileAssignmentDateTime": "String (timestamp)",
  "isSupervised": true,
  "discoverySource": "String",
  "createdDateTime": "String (timestamp)",
  "lastContactedDateTime": "String (timestamp)",
  "description": "String",
  "enrollmentState": "String",
  "platform": "String",
  "status": true
}
```





