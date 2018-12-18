---
title: tipo de recurso deviceManagementScript
description: Intune proporcionará al cliente la capacidad de ejecutar sus secuencias de comandos de Powershell en los dispositivos de Azure Active Directory se unió a windows inscritos 10. La secuencia de comandos se puede ejecutar una vez o periódicamente.
author: tfitzmac
ms.openlocfilehash: f35a0b4159c84535c4696f7b57c8486b866504b6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27351425"
---
# <a name="devicemanagementscript-resource-type"></a>tipo de recurso deviceManagementScript

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Intune proporcionará al cliente la capacidad de ejecutar sus secuencias de comandos de Powershell en los dispositivos de Azure Active Directory se unió a windows inscritos 10. La secuencia de comandos se puede ejecutar una vez o periódicamente.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista deviceManagementScripts](../api/intune-devices-devicemanagementscript-list.md)|colección de [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md)|Propiedades de la lista y relaciones de los objetos [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) .|
|[Obtener deviceManagementScript](../api/intune-devices-devicemanagementscript-get.md)|[deviceManagementScript](../resources/intune-devices-devicemanagementscript.md)|Leer las propiedades y las relaciones del objeto [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) .|
|[Crear deviceManagementScript](../api/intune-devices-devicemanagementscript-create.md)|[deviceManagementScript](../resources/intune-devices-devicemanagementscript.md)|Crear un nuevo objeto [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) .|
|[Eliminar deviceManagementScript](../api/intune-devices-devicemanagementscript-delete.md)|Ninguno|Elimina un [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md).|
|[Actualizar deviceManagementScript](../api/intune-devices-devicemanagementscript-update.md)|[deviceManagementScript](../resources/intune-devices-devicemanagementscript.md)|Actualizar las propiedades de un objeto [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) .|
|[Acción assign](../api/intune-devices-devicemanagementscript-assign.md)|Ninguno|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único para la secuencia de comandos de administración de dispositivos.|
|displayName|String|Nombre de la secuencia de comandos de administración de dispositivos.|
|descripción|String|Descripción opcional de la secuencia de comandos de administración de dispositivos.|
|runSchedule|[runSchedule](../resources/intune-devices-runschedule.md)|El intervalo para ejecutar la secuencia de comandos. Si no ha definido la secuencia de comandos se ejecutará una vez|
|scriptContent|Binario|El contenido de la secuencia de comandos.|
|createdDateTime|DateTimeOffset|La fecha y hora de que creación de la secuencia de comandos de administración de dispositivos.|
|lastModifiedDateTime|DateTimeOffset|La fecha y hora de que última modificación de la secuencia de comandos de administración de dispositivos.|
|runAsAccount|[runAsAccountType](../resources/intune-shared-runasaccounttype.md)|Indica el tipo de la secuencia de comandos de administración de dispositivos se ejecuta en el contexto de ejecución. Los valores posibles son: `system` y `user`.|
|enforceSignatureCheck|Boolean|Indicar si se debe comprobar la firma de la secuencia de comandos.|
|fileName|String|Nombre de archivo de secuencia de comandos.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|groupAssignments|colección de [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md)|La lista de las asignaciones de grupo para la secuencia de comandos de administración de dispositivos.|
|asignaciones|colección de [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)|La lista de las asignaciones de grupo para la secuencia de comandos de administración de dispositivos.|
|runSummary|[deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md)|Resumen de secuencia de comandos de administración de dispositivos de ejecución.|
|deviceRunStates|colección de [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md)|Lista de los Estados de ejecución para esta secuencia de comandos en todos los dispositivos.|
|userRunStates|colección de [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md)|Lista de los Estados de ejecución para esta secuencia de comandos a través de todos los usuarios.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementScript"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementScript",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "runSchedule": {
    "@odata.type": "microsoft.graph.runSchedule"
  },
  "scriptContent": "binary",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "runAsAccount": "String",
  "enforceSignatureCheck": true,
  "fileName": "String"
}
```





