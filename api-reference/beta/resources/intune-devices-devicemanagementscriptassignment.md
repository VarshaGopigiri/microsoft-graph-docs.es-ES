---
title: tipo de recurso deviceManagementScriptAssignment
description: Contiene propiedades que se usan para asignar una secuencia de comandos de administración de dispositivos a un grupo.
ms.openlocfilehash: fb4be06fe36153cd9a015808823cf1e90d86a707
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090653"
---
# <a name="devicemanagementscriptassignment-resource-type"></a>tipo de recurso deviceManagementScriptAssignment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene propiedades que se usan para asignar una secuencia de comandos de administración de dispositivos a un grupo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista deviceManagementScriptAssignments](../api/intune-devices-devicemanagementscriptassignment-list.md)|colección de [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)|Propiedades de la lista y relaciones de los objetos [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) .|
|[Obtener deviceManagementScriptAssignment](../api/intune-devices-devicemanagementscriptassignment-get.md)|[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)|Leer las propiedades y las relaciones del objeto [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) .|
|[Crear deviceManagementScriptAssignment](../api/intune-devices-devicemanagementscriptassignment-create.md)|[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)|Crear un nuevo objeto [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) .|
|[Eliminar deviceManagementScriptAssignment](../api/intune-devices-devicemanagementscriptassignment-delete.md)|Ninguno|Elimina un [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md).|
|[Actualizar deviceManagementScriptAssignment](../api/intune-devices-devicemanagementscriptassignment-update.md)|[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)|Actualizar las propiedades de un objeto [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad de asignación de grupo de secuencia de comandos de dispositivo administración.|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|El identificador de grupo de Active Directory de Azure, nuestro destino son la secuencia de comandos.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementScriptAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementScriptAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





