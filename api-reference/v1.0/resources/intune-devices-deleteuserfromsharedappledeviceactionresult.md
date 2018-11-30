---
title: Tipo de recurso deleteUserFromSharedAppleDeviceActionResult
description: Resultado de la acción Eliminar usuario del dispositivo Apple compartido
ms.openlocfilehash: dc21e22ca2e819835178a7cb2ed3aa824cd40004
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028654"
---
# <a name="deleteuserfromsharedappledeviceactionresult-resource-type"></a>Tipo de recurso deleteUserFromSharedAppleDeviceActionResult

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Resultado de la acción Eliminar usuario del dispositivo Apple compartido

Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|actionName|Cadena|Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)|
|actionState|[actionState](../resources/intune-devices-actionstate.md)|Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md). Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.|
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



