---
title: Tipo de recurso deviceConfigurationAssignment
description: La entidad de asignación de la configuración de dispositivo asigna un grupo AAD a una configuración de dispositivo específico.
author: tfitzmac
ms.openlocfilehash: 26afc67312ab8544b395b5e20b89a01558fc75d9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306247"
---
# <a name="deviceconfigurationassignment-resource-type"></a>Tipo de recurso deviceConfigurationAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

La entidad de asignación de la configuración de dispositivo asigna un grupo AAD a una configuración de dispositivo específico.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceConfigurationAssignments](../api/intune-deviceconfig-deviceconfigurationassignment-list.md)|Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|Enumere las propiedades y las relaciones de los objetos [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).|
|[Obtener deviceConfigurationAssignment](../api/intune-deviceconfig-deviceconfigurationassignment-get.md)|[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|Lea las propiedades y las relaciones del objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).|
|[Crear deviceConfigurationAssignment](../api/intune-deviceconfig-deviceconfigurationassignment-create.md)|[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|Cree un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).|
|[Eliminar deviceConfigurationAssignment](../api/intune-deviceconfig-deviceconfigurationassignment-delete.md)|Ninguna|Elimina un [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).|
|[Actualizar deviceConfigurationAssignment](../api/intune-deviceconfig-deviceconfigurationassignment-update.md)|[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|Actualice las propiedades de un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|La clave de la asignación.|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|El destino de la tarea para la configuración del dispositivo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



