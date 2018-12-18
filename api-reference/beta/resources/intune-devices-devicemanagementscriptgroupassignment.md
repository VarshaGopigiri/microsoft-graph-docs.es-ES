---
title: tipo de recurso deviceManagementScriptGroupAssignment
description: Contiene propiedades que se usan para asignar una secuencia de comandos de administración de dispositivos a un grupo.
author: tfitzmac
ms.openlocfilehash: 446e293ee3d4c0cc2071f6a93e01bcdf8cf72a2c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27345944"
---
# <a name="devicemanagementscriptgroupassignment-resource-type"></a>tipo de recurso deviceManagementScriptGroupAssignment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene propiedades que se usan para asignar una secuencia de comandos de administración de dispositivos a un grupo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista deviceManagementScriptGroupAssignments](../api/intune-devices-devicemanagementscriptgroupassignment-list.md)|colección de [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md)|Propiedades de la lista y relaciones de los objetos [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md) .|
|[Obtener deviceManagementScriptGroupAssignment](../api/intune-devices-devicemanagementscriptgroupassignment-get.md)|[deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md)|Leer las propiedades y las relaciones del objeto [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md) .|
|[Crear deviceManagementScriptGroupAssignment](../api/intune-devices-devicemanagementscriptgroupassignment-create.md)|[deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md)|Crear un nuevo objeto [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md) .|
|[Eliminar deviceManagementScriptGroupAssignment](../api/intune-devices-devicemanagementscriptgroupassignment-delete.md)|Ninguno|Elimina un [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md).|
|[Actualizar deviceManagementScriptGroupAssignment](../api/intune-devices-devicemanagementscriptgroupassignment-update.md)|[deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md)|Actualizar las propiedades de un objeto [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad de asignación de grupo de secuencia de comandos de dispositivo administración.|
|targetGroupId|String|El identificador de grupo de Active Directory de Azure, nuestro destino son la secuencia de comandos.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementScriptGroupAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementScriptGroupAssignment",
  "id": "String (identifier)",
  "targetGroupId": "String"
}
```





