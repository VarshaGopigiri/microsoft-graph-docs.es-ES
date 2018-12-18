---
title: Tipo de recurso deleteUserFromSharedAppleDeviceActionResult
description: Resultado de la acción Eliminar usuario del dispositivo Apple compartido
author: tfitzmac
ms.openlocfilehash: 928d20603bc06d15e2e58c03d6ef611a9d57b42f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27319792"
---
# <a name="deleteuserfromsharedappledeviceactionresult-resource-type"></a>Tipo de recurso deleteUserFromSharedAppleDeviceActionResult

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Resultado de la acción Eliminar usuario del dispositivo Apple compartido

Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|actionName|Cadena|Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)|
|actionState|[actionState](../resources/intune-shared-actionstate.md)|Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md). Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.|
|startDateTime|DateTimeOffset|Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)|
|lastUpdatedDateTime|DateTimeOffset|Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)|
|userPrincipalName|cadena|Nombre principal de usuario del usuario que se va a eliminar.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deleteUserFromSharedAppleDeviceActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deleteUserFromSharedAppleDeviceActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "userPrincipalName": "String"
}
```





