---
title: tipo de recurso governanceRoleDefinition
description: Representa las definiciones de roles. Para obtener recursos de Azure, puede representar funciones de RBAC Azure, como propietario, lector, Colaborador, etcetera.
ms.openlocfilehash: 057d74276b41abad47eb60ce48a99f1160c401ef
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084781"
---
# <a name="governanceroledefinition-resource-type"></a>tipo de recurso governanceRoleDefinition

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción. 


Representa las definiciones de roles. Para obtener recursos de Azure, puede representar funciones de RBAC Azure, como propietario, lector, Colaborador, etcetera.


## <a name="methods"></a>Métodos

| Método          | Tipo de valor devuelto |Descripción|
|:---------------|:--------|:--------|:----------|
|[List](../api/governanceroledefinition-list.md) | colección de [governanceRoleDefinition](../resources/governanceroledefinition.md) |Una colección de definiciones de roles en un recurso de la lista.|
|[Get](../api/governanceroledefinition-get.md) | [governanceRoleDefinition](../resources/governanceroledefinition.md) |Leer las propiedades y las relaciones de una entidad de definición de rol especificado por id.|
No `POST`, `PUT`, `PATCH`, `DELETE` es compatible con `roleDefinitions` conjunto de entidades por ahora.
## <a name="properties"></a>Propiedades
| Propiedad  | Tipo      |Descripción|
|:----|:----------|:----------|:----------|
|id         |String     |El identificador de la definición de roles. |
|resourceId |Cadena     |Necesario. El identificador de recurso asociado a la definición de roles. |
|externalId   |String     |El identificador externo de la definición de roles.|
|displayName|String     |El nombre para mostrar de la definición de roles.|
|subjectCount|Int32     |Opcional. El número de asuntos que se asignan al rol. Representa el estado de acceso del solicitante para el recurso. Para obtener la propiedad, por favor, use explícitamente `$select=subjectCount` en la consulta.|
|eligibleAssignmentCount|Int32|Opcional. El número de asignaciones de roles optan asociado con la definición de roles. Para obtener la propiedad, por favor, use explícitamente `$select=eligibleAssignmentCount` en la consulta.|
|activeAssignmentCount|Int32    |Opcional. El número de asignaciones de rol activo asociado con la definición de roles.  Para obtener la propiedad, por favor, use explícitamente `$select=activeAssignmentCount` en la consulta.|


## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|resource|[governanceResource](../resources/governanceresource.md)|Solo lectura. El recurso asociado para la definición de roles.|
|roleSetting|[governanceRoleSetting](../resources/governancerolesetting.md)|Configuración de la función asociada para la definición de roles.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceRoleDefinition"
}-->

```json
{
  "id": "String (identifier)",
  "resourceId": "String",
  "externalId": "String",
  "displayName": "String",
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceRoleDefinition",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->