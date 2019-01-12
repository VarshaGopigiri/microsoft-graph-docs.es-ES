---
title: tipo de recurso deviceManagementScriptAssignment
description: Contiene propiedades que se usan para asignar una secuencia de comandos de administración de dispositivos a un grupo.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d335f31ceed7ca670981e7702b69950b7f5a864a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923897"
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
|id|Cadena|Clave de la entidad de asignación de grupo de secuencia de comandos de dispositivo administración.|
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





