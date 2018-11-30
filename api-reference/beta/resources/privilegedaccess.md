---
title: tipo de recurso privilegedAccess
description: " Por ejemplo, `privilegedAccess/azureResources` representa PIM administración con privilegios de acceso a los recursos de Azure."
ms.openlocfilehash: af109c0cc355bfb282630d21cd02bb463b944f38
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090771"
---
# <a name="privilegedaccess-resource-type"></a>tipo de recurso privilegedAccess

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un grupo de funcionalidades proporcionadas por el servicio de administración de identidad con privilegios (PIM). Instancias diferentes de `privilegedAccess` representan diferentes proveedores administrados por PIM; Por ejemplo, `privilegedAccess/azureResources` representa PIM administración con privilegios de acceso a los recursos de Azure.


`privilegedAccess`es de sólo lectura por ahora. No `POST`, `PUT`, `PATCH`, o `DELETE` operaciones son compatibles con el `privilegedAccess` conjunto de entidades.

## <a name="properties"></a>Propiedades
| Propiedad  | Tipo      |Descripción|
|:----------|:----------|:----------|
|id         |String     |El identificador del proveedor administrado por PIM.|
|displayName|String     |El nombre para mostrar del proveedor administrado por PIM.|


## <a name="relationships"></a>Relaciones
| Relación   | Tipo                                         |Descripción|
|:---------------|:---------------------------------------------|:----------|
|recursos       |colección de [governanceResource](../resources/governanceresource.md)            |Una colección de recursos para el proveedor.|
|roleAssignments |colección de [governanceRoleAssignment](../resources/governanceroleassignment.md)|Una colección de asignaciones de roles para el proveedor.|
|roleDefinitions |colección de [governanceRoleDefinition](../resources/governanceroledefinition.md)|Una colección de definiciones de rol para el proveedor.|
|roleAssignmentRequests |colección de [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md)|Una colección de solicitudes de asignación de rol para el proveedor.|
|roleSettings |colección de [governanceRoleSetting](../resources/governancerolesetting.md)|Una colección de configuración de las funciones para el proveedor.|


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedAccess"
}-->

```json
{
  "id": "String (identifier)",
  "displayName": "String",
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedAccess",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
