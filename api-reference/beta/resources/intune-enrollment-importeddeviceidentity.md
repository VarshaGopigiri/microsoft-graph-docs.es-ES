---
title: tipo de recurso importedDeviceIdentity
description: El recurso importedDeviceIdentity representa una identidad única de hardware de un dispositivo que se ha almacenado previamente provisionalmente para inscripción previa a la configuración.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3c33069520913c7c750220ca8938459ba9bf96c2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811673"
---
# <a name="importeddeviceidentity-resource-type"></a>tipo de recurso importedDeviceIdentity

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso importedDeviceIdentity representa una identidad única de hardware de un dispositivo que se ha almacenado previamente provisionalmente para inscripción previa a la configuración.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista importedDeviceIdentities](../api/intune-enrollment-importeddeviceidentity-list.md)|colección de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)|Propiedades de la lista y relaciones de los objetos [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) .|
|[Obtener importedDeviceIdentity](../api/intune-enrollment-importeddeviceidentity-get.md)|[importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)|Leer las propiedades y las relaciones del objeto [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) .|
|[Crear importedDeviceIdentity](../api/intune-enrollment-importeddeviceidentity-create.md)|[importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)|Crear un nuevo objeto [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) .|
|[Eliminar importedDeviceIdentity](../api/intune-enrollment-importeddeviceidentity-delete.md)|Ninguno|Elimina un [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).|
|[Actualizar importedDeviceIdentity](../api/intune-enrollment-importeddeviceidentity-update.md)|[importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)|Actualizar las propiedades de un objeto [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) .|
|[acción importDeviceIdentityList](../api/intune-enrollment-importeddeviceidentity-importdeviceidentitylist.md)|colección de [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md)|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador de la identidad del dispositivo importada|
|importedDeviceIdentifier|Cadena|Identificador de dispositivo importada|
|importedDeviceIdentityType|[importedDeviceIdentityType](../resources/intune-enrollment-importeddeviceidentitytype.md)|Tipo de identidad de dispositivo importada. Los valores posibles son: `unknown`, `imei` y `serialNumber`.|
|lastModifiedDateTime|DateTimeOffset|DateTime última modificación de la descripción|
|createdDateTime|DateTimeOffset|Crear fecha hora del dispositivo|
|lastContactedDateTime|DateTimeOffset|Última vez fecha ponerse en contacto del dispositivo|
|descripción|Cadena|La descripción del dispositivo|
|enrollmentState|[enrollmentState](../resources/intune-enrollment-enrollmentstate.md)|El estado del dispositivo en Intune. Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.|
|platform|[plataforma](../resources/intune-enrollment-platform.md)|La plataforma del dispositivo. Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.importedDeviceIdentity"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.importedDeviceIdentity",
  "id": "String (identifier)",
  "importedDeviceIdentifier": "String",
  "importedDeviceIdentityType": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "lastContactedDateTime": "String (timestamp)",
  "description": "String",
  "enrollmentState": "String",
  "platform": "String"
}
```





