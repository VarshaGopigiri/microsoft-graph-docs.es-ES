---
title: Tipo de recurso enrollmentConfigurationAssignment
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: fa509dccf336755bc37c2c64080e6438fcc6bc5d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340211"
---
# <a name="enrollmentconfigurationassignment-resource-type"></a>Tipo de recurso enrollmentConfigurationAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar enrollmentConfigurationAssignments](../api/intune-onboarding-enrollmentconfigurationassignment-list.md)|Colección [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md)|Enumere las propiedades y las relaciones de los objetos [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md).|
|[Obtener enrollmentConfigurationAssignment](../api/intune-onboarding-enrollmentconfigurationassignment-get.md)|[enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md)|Lea las propiedades y las relaciones del objeto [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md).|
|[Crear enrollmentConfigurationAssignment](../api/intune-onboarding-enrollmentconfigurationassignment-create.md)|[enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md)|Cree un objeto [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md).|
|[Eliminar enrollmentConfigurationAssignment](../api/intune-onboarding-enrollmentconfigurationassignment-delete.md)|Ninguna|Elimina un [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md).|
|[Actualizar enrollmentConfigurationAssignment](../api/intune-onboarding-enrollmentconfigurationassignment-update.md)|[enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md)|Actualice las propiedades de un objeto [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Todavía no documentado|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|Todavía no documentado|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.enrollmentConfigurationAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.enrollmentConfigurationAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



