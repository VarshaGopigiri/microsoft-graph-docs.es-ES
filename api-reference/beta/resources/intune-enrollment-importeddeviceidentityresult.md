---
title: tipo de recurso importedDeviceIdentityResult
description: El recurso importedDeviceIdentityResult representa el resultado de intentar importar una identidad de dispositivo.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7373ff0c0ec138b61552b61caea063a063a50ad1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981738"
---
# <a name="importeddeviceidentityresult-resource-type"></a>tipo de recurso importedDeviceIdentityResult

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso importedDeviceIdentityResult representa el resultado de intentar importar una identidad de dispositivo.

Hereda de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista importedDeviceIdentityResults](../api/intune-enrollment-importeddeviceidentityresult-list.md)|colección de [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md)|Propiedades de la lista y relaciones de los objetos [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) .|
|[Obtener importedDeviceIdentityResult](../api/intune-enrollment-importeddeviceidentityresult-get.md)|[importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md)|Leer las propiedades y las relaciones del objeto [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) .|
|[Crear importedDeviceIdentityResult](../api/intune-enrollment-importeddeviceidentityresult-create.md)|[importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md)|Crear un nuevo objeto [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) .|
|[Eliminar importedDeviceIdentityResult](../api/intune-enrollment-importeddeviceidentityresult-delete.md)|Ninguno|Elimina un [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md).|
|[Actualizar importedDeviceIdentityResult](../api/intune-enrollment-importeddeviceidentityresult-update.md)|[importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md)|Actualizar las propiedades de un objeto [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador de la identidad de dispositivo importada Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)|
|importedDeviceIdentifier|String|Identificador de dispositivo importada heredado de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)|
|importedDeviceIdentityType|[importedDeviceIdentityType](../resources/intune-enrollment-importeddeviceidentitytype.md)|Tipo de importados se hereda de identidad del dispositivo de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md). Los valores posibles son: `unknown`, `imei` y `serialNumber`.|
|lastModifiedDateTime|DateTimeOffset|DateTime última modificación de la descripción Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)|
|createdDateTime|DateTimeOffset|Crear fecha hora del dispositivo Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)|
|lastContactedDateTime|DateTimeOffset|Última vez fecha ponerse en contacto del dispositivo Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)|
|descripción|String|La descripción del dispositivo Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)|
|enrollmentState|[enrollmentState](../resources/intune-enrollment-enrollmentstate.md)|El estado del dispositivo en Intune se hereda de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md). Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.|
|platform|[plataforma](../resources/intune-enrollment-platform.md)|La plataforma del dispositivo. Se hereda de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md). Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.|
|status|Booleano|Estado de identidad de dispositivo importada|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.importedDeviceIdentityResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.importedDeviceIdentityResult",
  "id": "String (identifier)",
  "importedDeviceIdentifier": "String",
  "importedDeviceIdentityType": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "lastContactedDateTime": "String (timestamp)",
  "description": "String",
  "enrollmentState": "String",
  "platform": "String",
  "status": true
}
```





