---
title: tipo de recurso importedAppleDeviceIdentity
description: El recurso importedAppleDeviceIdentity representa la identidad del dispositivo importadas de un dispositivo de Apple.
ms.openlocfilehash: 8441d169e0e7aa1cbf9c79a017599cca1cc4aa04
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084574"
---
# <a name="importedappledeviceidentity-resource-type"></a>tipo de recurso importedAppleDeviceIdentity

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso importedAppleDeviceIdentity representa la identidad del dispositivo importadas de un dispositivo de Apple.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista importedAppleDeviceIdentities](../api/intune-enrollment-importedappledeviceidentity-list.md)|colección de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|Propiedades de la lista y relaciones de los objetos [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md) .|
|[Obtener importedAppleDeviceIdentity](../api/intune-enrollment-importedappledeviceidentity-get.md)|[importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|Leer las propiedades y las relaciones del objeto [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md) .|
|[Crear importedAppleDeviceIdentity](../api/intune-enrollment-importedappledeviceidentity-create.md)|[importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|Crear un nuevo objeto [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md) .|
|[Eliminar importedAppleDeviceIdentity](../api/intune-enrollment-importedappledeviceidentity-delete.md)|Ninguno|Elimina un [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).|
|[Actualizar importedAppleDeviceIdentity](../api/intune-enrollment-importedappledeviceidentity-update.md)|[importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|Actualizar las propiedades de un objeto [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md) .|
|[acción importAppleDeviceIdentityList](../api/intune-enrollment-importedappledeviceidentity-importappledeviceidentitylist.md)|colección de [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md)|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|serialNumber|String|Número de serie del dispositivo|
|requestedEnrollmentProfileId|String|Administración de identificador de perfil de inscripción tenga la intención de aplicar al dispositivo durante la inscripción siguiente|
|requestedEnrollmentProfileAssignmentDateTime|DateTimeOffset|El perfil de tiempo de inscripción se asignó al dispositivo|
|isSupervised|Booleano|Indica si el dispositivo de Apple es supervisado. Es más información en:https://support.apple.com/en-us/HT202837|
|discoverySource|[discoverySource](../resources/intune-enrollment-discoverysource.md)|Origen de detección del dispositivo de Apple. Los valores posibles son: `unknown`, `adminImport` y `deviceEnrollmentProgram`.|
|createdDateTime|DateTimeOffset|Crear fecha hora del dispositivo|
|lastContactedDateTime|DateTimeOffset|Última vez fecha ponerse en contacto del dispositivo|
|descripción|String|La descripción del dispositivo|
|enrollmentState|[enrollmentState](../resources/intune-enrollment-enrollmentstate.md)|El estado del dispositivo en Intune. Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.|
|platform|[plataforma](../resources/intune-enrollment-platform.md)|La plataforma del dispositivo. Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.importedAppleDeviceIdentity"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.importedAppleDeviceIdentity",
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
  "platform": "String"
}
```





