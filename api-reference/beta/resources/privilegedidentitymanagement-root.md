---
title: Administración de identidades de Azure con privilegios de AD
description: Aquí es la lista de los métodos proporcionados por el servicio de administración de identidades con privilegios.
localization_priority: Priority
ms.openlocfilehash: c1108711c96dd253f784a418a396ca30507c5f7d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884066"
---
# <a name="azure-ad-privileged-identity-management"></a>Administración de identidades de Azure con privilegios de AD

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Aquí es la lista de los métodos proporcionados por el servicio de [Administración de identidades con privilegios](https://azure.microsoft.com/en-us/documentation/articles/active-directory-privileged-identity-management-configure/) .

El servicio se fundamentan en OData. Para filtrar los resultados de la consulta, use el estándar OData ``$filter`` expresiones en los URI.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Lista privilegedOperationEvent](../api/privilegedoperationevent-list.md) | colección de [privilegedOperationEvent](privilegedoperationevent.md) |Obtener la colección de objetos privilegedOperationEvent. |
|[Obtener privilegedRole](../api/privilegedrole-get.md) |[privilegedRole](privilegedrole.md)| Obtenga un objeto privilegedRole.|
|[Lista privilegedRole](../api/privilegedrole-list.md) | colección de [privilegedRole](privilegedrole.md) |Obtener la colección de objetos privilegedRole. |
|[Asignaciones de funciones de lista](../api/privilegedrole-list-assignments.md) | colección de [privilegedRoleAssignment](privilegedroleassignment.md) |Obtener la colección privilegedRoleAssignment para la función determinada. Cada privilegedRoleAssignment representa una asignación de roles a un usuario.|
|[selfActivate](../api/privilegedrole-selfactivate.md) | [privilegedRoleAssignment](privilegedroleassignment.md) |Activar la función que se asigna al solicitante.|
|[selfDeactivate](../api/privilegedrole-selfdeactivate.md) | [privilegedRoleAssignment](privilegedroleassignment.md) |Desactivación de la función que se asigna al solicitante.|
|[Crear privilegedRoleAssignment](../api/privilegedroleassignment-post-privilegedroleassignments.md) |[privilegedRoleAssignment](privilegedroleassignment.md)| Para crear un nuevo privilegedRoleAssignment (asignación de rol), la publicación de la colección privilegedRoleAssignments.|
|[Lista privilegedRoleAssignment](../api/privilegedroleassignment-list.md) | colección de [privilegedRoleAssignment](privilegedroleassignment.md) |Obtener la colección de objetos privilegedRoleAssignment. La colección contiene todas las asignaciones de roles para la organización. Cada privilegedRoleAssignment representa una asignación de roles a un usuario. |
|[Obtener privilegedRoleAssignment](../api/privilegedroleassignment-get.md) | [privilegedRoleAssignment](privilegedroleassignment.md)|Obtener el objeto privilegedRoleAssignment con el identificador de asignación especificada. |
|[Eliminar privilegedRoleAssignment](../api/privilegedroleassignment-delete.md) | Ninguno. |Eliminar el objeto privilegedRoleAssignment. |
|[makePermanent](../api/privilegedroleassignment-makepermanent.md) | [privilegedRoleAssignment](privilegedroleassignment.md) |Hacer que la asignación de rol como permanente. |
|[makeEligible](../api/privilegedroleassignment-makeeligible.md) | [privilegedRoleAssignment](privilegedroleassignment.md) |Hacer que la asignación de rol como elegibles. |
|[Mi](../api/privilegedroleassignment-my.md) | colección de [privilegedRoleAssignment](privilegedroleassignment.md)|Obtener las asignaciones de funciones del solicitante. |
|[Obtener privilegedRoleSettings](../api/privilegedrolesettings-get.md) | [privilegedRoleSettings](../resources/privilegedrolesettings.md)|Recuperar las propiedades del objeto privilegedRoleSettings. |
|[Obtener privilegedRoleSummary](../api/privilegedrolesummary-get.md) | [privilegedRoleSummary](../resources/privilegedrolesummary.md)|Recupere el objeto privilegedRoleSummary. |
|[Obtener privilegedApproval](../api/privilegedapproval-get.md) |[privilegedApproval](privilegedapproval.md)| Obtenga un objeto privilegedApproval.|
|[Lista privilegedApproval](../api/privilegedapproval-list.md) | colección de [privilegedApproval](privilegedapproval.md) |Obtener la colección de objetos privilegedApproval. |
|[Crear privilegedApproval](../api/privilegedapproval-post-privilegedapproval.md) | [privilegedApproval](privilegedapproval.md)    |Crear objeto privilegedApproval. |
|[Actualizar privilegedApproval](../api/privilegedapproval-update.md) | [privilegedApproval](privilegedapproval.md) |Actualizar el objeto privilegedApproval. |
|[myrequests](../api/privilegedapproval-myrequests.md) | colección de [privilegedApproval](privilegedapproval.md)|Obtenga las solicitudes de aprobación del solicitante. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Service root",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
