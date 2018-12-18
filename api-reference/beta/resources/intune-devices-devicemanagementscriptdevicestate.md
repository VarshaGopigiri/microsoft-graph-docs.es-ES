---
title: tipo de recurso deviceManagementScriptDeviceState
description: Contiene las propiedades de dispositivo de estado de la secuencia de comandos de administración de dispositivos de ejecución.
author: tfitzmac
ms.openlocfilehash: 5667de5351ea3130ab0c3e00a55013ada66ed01a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337327"
---
# <a name="devicemanagementscriptdevicestate-resource-type"></a>tipo de recurso deviceManagementScriptDeviceState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades de dispositivo de estado de la secuencia de comandos de administración de dispositivos de ejecución.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista deviceManagementScriptDeviceStates](../api/intune-devices-devicemanagementscriptdevicestate-list.md)|colección de [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md)|Propiedades de la lista y relaciones de los objetos [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) .|
|[Obtener deviceManagementScriptDeviceState](../api/intune-devices-devicemanagementscriptdevicestate-get.md)|[deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md)|Leer las propiedades y las relaciones del objeto [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) .|
|[Crear deviceManagementScriptDeviceState](../api/intune-devices-devicemanagementscriptdevicestate-create.md)|[deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md)|Crear un nuevo objeto [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) .|
|[Eliminar deviceManagementScriptDeviceState](../api/intune-devices-devicemanagementscriptdevicestate-delete.md)|Ninguno|Elimina un [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md).|
|[Actualizar deviceManagementScriptDeviceState](../api/intune-devices-devicemanagementscriptdevicestate-update.md)|[deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md)|Actualizar las propiedades de un objeto [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad de estado de dispositivo de secuencia de comandos de dispositivo administración.|
|runState|[runState](../resources/intune-shared-runstate.md)|Estado de la última ejecución de la secuencia de comandos de administración de dispositivos. Los valores posibles son: `unknown`, `success` y `fail`.|
|resultMessage|String|Detalles de los resultados de la ejecución.|
|lastStateUpdateDateTime|DateTimeOffset|Última vez que se ejecuta la secuencia de comandos de administración de dispositivos.|
|errorCode|Int32|Código de error correspondiente a la ejecución de la secuencia de comandos de administración de dispositivos con errores.|
|errorDescription|Cadena|Descripción del error correspondiente a la ejecución de la secuencia de comandos de administración de dispositivos con errores.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|managedDevice|[managedDevice](../resources/intune-devices-manageddevice.md)|Los dispositivos administrados que se ejecuta la secuencia de comandos de administración de dispositivos.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementScriptDeviceState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementScriptDeviceState",
  "id": "String (identifier)",
  "runState": "String",
  "resultMessage": "String",
  "lastStateUpdateDateTime": "String (timestamp)",
  "errorCode": 1024,
  "errorDescription": "String"
}
```





