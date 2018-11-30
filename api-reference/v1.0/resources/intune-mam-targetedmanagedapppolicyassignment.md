---
title: Tipo de recurso targetedManagedAppPolicyAssignment
description: El tipo para la implementación de aplicaciones o grupos.
ms.openlocfilehash: 06850c27b9f13a4613301a14ca7ba29e758be9ac
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032616"
---
# <a name="targetedmanagedapppolicyassignment-resource-type"></a>Tipo de recurso targetedManagedAppPolicyAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El tipo para la implementación de aplicaciones o grupos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar targetedManagedAppPolicyAssignments](../api/intune-mam-targetedmanagedapppolicyassignment-list.md)|Colección [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md)|Enumere las propiedades y los relaciones de los objetos [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).|
|[Obtener targetedManagedAppPolicyAssignment](../api/intune-mam-targetedmanagedapppolicyassignment-get.md)|[targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md)|Lea las propiedades y los relaciones del objeto [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).|
|[Eliminar targetedManagedAppPolicyAssignment](../api/intune-mam-targetedmanagedapppolicyassignment-delete.md)|Ninguna|Elimina un [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).|
|[Actualizar targetedManagedAppPolicyAssignment](../api/intune-mam-targetedmanagedapppolicyassignment-update.md)|[targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md)|Actualice las propiedades de un objeto [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Id|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|Identificador para la implementación de un grupo o una aplicación|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.targetedManagedAppPolicyAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.targetedManagedAppPolicyAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



