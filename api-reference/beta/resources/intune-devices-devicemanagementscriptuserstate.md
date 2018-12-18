---
title: tipo de recurso deviceManagementScriptUserState
description: Contiene las propiedades de usuario de ejecución de la secuencia de comandos de administración de dispositivos.
author: tfitzmac
ms.openlocfilehash: acce3d40d390c22d848b9ee3f8c94c997ae6da12
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301214"
---
# <a name="devicemanagementscriptuserstate-resource-type"></a>tipo de recurso deviceManagementScriptUserState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades de usuario de ejecución de la secuencia de comandos de administración de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista deviceManagementScriptUserStates](../api/intune-devices-devicemanagementscriptuserstate-list.md)|colección de [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md)|Propiedades de la lista y relaciones de los objetos [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md) .|
|[Obtener deviceManagementScriptUserState](../api/intune-devices-devicemanagementscriptuserstate-get.md)|[deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md)|Leer las propiedades y las relaciones del objeto [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md) .|
|[Crear deviceManagementScriptUserState](../api/intune-devices-devicemanagementscriptuserstate-create.md)|[deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md)|Crear un nuevo objeto [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md) .|
|[Eliminar deviceManagementScriptUserState](../api/intune-devices-devicemanagementscriptuserstate-delete.md)|Ninguno|Elimina un [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md).|
|[Actualizar deviceManagementScriptUserState](../api/intune-devices-devicemanagementscriptuserstate-update.md)|[deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md)|Actualizar las propiedades de un objeto [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad de estado de usuario de secuencia de comandos de dispositivo administración.|
|successDeviceCount|Int32|Recuento de éxito de dispositivo para el usuario específico.|
|errorDeviceCount|Int32|Número de dispositivo de error de usuario específico.|
|userPrincipalName|String|Nombre de principio de usuario del usuario específico.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|deviceRunStates|colección de [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md)|Lista de los Estados de ejecución para esta secuencia de comandos en todos los dispositivos de usuario específico.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementScriptUserState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementScriptUserState",
  "id": "String (identifier)",
  "successDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "userPrincipalName": "String"
}
```





