---
title: tipo de recurso privilegedRoleAssignment
description: 'Representa una asignación de roles con privilegios de un usuario concreto. '
ms.openlocfilehash: 40cfe6487184171fc0d120f9a0e2cd98070f96f0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085254"
---
# <a name="privilegedroleassignment-resource-type"></a>tipo de recurso privilegedRoleAssignment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una asignación de roles con privilegios de un usuario concreto. 


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Colección de listas de privilegedRoleAssignment](../api/privilegedroleassignment-list.md) | colección de [privilegedRoleAssignment](privilegedroleassignment.md)|Obtener la colección de objetos privilegedRoleAssignment.|
|[Obtener privilegedRoleAssignment](../api/privilegedroleassignment-get.md) | [privilegedRoleAssignment](privilegedroleassignment.md) |Leer las propiedades y las relaciones del objeto privilegedRoleAssignment.|
|[Crear asignación](../api/privilegedroleassignment-post-privilegedroleassignments.md) |[privilegedRoleAssignment](privilegedroleassignment.md)| Crear una nueva asignación de la publicación de la colección de asignaciones.|
|[Delete](../api/privilegedroleassignment-delete.md) | Ninguno |Eliminar el objeto privilegedRoleAssignment. |
|[makePermanent](../api/privilegedroleassignment-makepermanent.md)|[privilegedRoleAssignment](privilegedroleassignment.md)|Hacer que la asignación de rol como permanente.|
|[makeEligible](../api/privilegedroleassignment-makeeligible.md)|[privilegedRoleAssignment](privilegedroleassignment.md)|Hacer que la asignación de rol como elegibles.|
|[Mi](../api/privilegedroleassignment-my.md)|colección de [privilegedRoleAssignment](privilegedroleassignment.md)|Obtener las asignaciones de roles con privilegios del usuario actual.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|expirationDateTime|dateTimeOffset|La estructura de DateTime de UTC cuando la asignación de roles con privilegios temporal caducará. Para la asignación de rol permanente, el valor es null.|
|id|string| El identificador único para la asignación de roles con privilegios. Solo lectura. Está en el formato de 'userId_roleId', donde userId es la cadena GUID para el identificador de usuario de Azure AD y el identificador de función es la cadena GUID para el identificador de rol de administrador de Azure.|
|isElevated|boolean|**true** si se activa la asignación de roles. **false** si se desactiva la asignación de roles.|
|resultMessage|string|Mensaje de resultado establecido por el servicio.|
|identificador de función|string|Identificador de rol. GUID en formato de cadena.|
|userId|string|Identificador de usuario. GUID en formato de cadena.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|roleInfo|[privilegedRole](privilegedrole.md)| Solo lectura. Admite valores NULL. La información de la función asociada.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedRoleAssignment"
}-->

```json
{
  "expirationDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "isElevated": true,
  "resultMessage": "string",
  "roleId": "string",
  "userId": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRoleAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->