---
title: tipo de recurso privilegedAccess
description: " Por ejemplo, `privilegedAccess/azureResources` representa PIM administración con privilegios de acceso a los recursos de Azure."
localization_priority: Normal
ms.openlocfilehash: f4166fb539d627730c68c7e039fd8d672ff4c785
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810055"
---
# <a name="privilegedaccess-resource-type"></a>tipo de recurso privilegedAccess

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un grupo de funcionalidades proporcionadas por el servicio de administración de identidad con privilegios (PIM). Instancias diferentes de `privilegedAccess` representan diferentes proveedores administrados por PIM; Por ejemplo, `privilegedAccess/azureResources` representa PIM administración con privilegios de acceso a los recursos de Azure.


`privilegedAccess`es de sólo lectura por ahora. No `POST`, `PUT`, `PATCH`, o `DELETE` operaciones son compatibles con el `privilegedAccess` conjunto de entidades.

## <a name="properties"></a>Propiedades
| Propiedad  | Tipo      |Descripción|
|:----------|:----------|:----------|
|id         |Cadena     |El identificador del proveedor administrado por PIM.|
|displayName|Cadena     |El nombre para mostrar del proveedor administrado por PIM.|


## <a name="relationships"></a>Relaciones
| Relación   | Tipo                                         |Description|
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
