---
title: Tipo de recurso deviceCompliancePolicyAssignment
description: Asignación de directivas de cumplimiento de dispositivos.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 881153242e2af2aeafa39f30b6d303313083cbcf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980072"
---
# <a name="devicecompliancepolicyassignment-resource-type"></a>Tipo de recurso deviceCompliancePolicyAssignment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Asignación de directivas de cumplimiento de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceCompliancePolicyAssignments](../api/intune-deviceconfig-devicecompliancepolicyassignment-list.md)|Colección [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)|Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).|
|[Obtener deviceCompliancePolicyAssignment](../api/intune-deviceconfig-devicecompliancepolicyassignment-get.md)|[deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)|Lea las propiedades y las relaciones del objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).|
|[Crear deviceCompliancePolicyAssignment](../api/intune-deviceconfig-devicecompliancepolicyassignment-create.md)|[deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)|Cree un objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).|
|[Eliminar deviceCompliancePolicyAssignment](../api/intune-deviceconfig-devicecompliancepolicyassignment-delete.md)|Ninguna|Elimina un [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).|
|[Actualizar deviceCompliancePolicyAssignment](../api/intune-deviceconfig-devicecompliancepolicyassignment-update.md)|[deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)|Actualice las propiedades de un objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|Destino de la asignación de directivas de cumplimiento|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCompliancePolicyAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





