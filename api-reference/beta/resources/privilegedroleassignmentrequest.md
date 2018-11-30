---
title: tipo de recurso privilegedRoleAssignmentRequest
description: Representa la solicitud para operaciones de asignación de rol de administración de identidades de Privilegd.
ms.openlocfilehash: b715c88157a7df52dabcb4c746dfe70bc2523d18
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089590"
---
# <a name="privilegedroleassignmentrequest-resource-type"></a>tipo de recurso privilegedRoleAssignmentRequest

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la solicitud para operaciones de asignación de rol de administración de identidades de Privilegd.

`privilegedRoleAssignmentRequest`se utiliza una entidad modelar vale para administrar el ciclo de vida de las asignaciones de roles. Representa la intención o la decisión de los usuarios y administradores y también proporciona la flexibilidad necesaria para permitir la implementación de schduling periódico, puertas de aprobación y así sucesivamente, con respecto a exponer directamente `POST` y `LIST` operaciones, así como `MY` y `Cancel` funciona en `governanceRoleAssignment`.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto | Descripción |
|:-------------|:------------|:------------|
|[List](../api/privilegedroleassignmentrequest-list.md) | colección de [privilegedroleassignmentrequest](../resources/privilegedroleassignmentrequest.md)|Las solicitudes de asignación de rol de la lista.|
|[Create](../api/privilegedroleassignmentrequest-post.md)|  [privilegedroleassignmentrequest](../resources/privilegedroleassignmentrequest.md)|Cree una solicitud para administrar el ciclo de vida de la asignación de rol nuevo o existente.|
|[Cancelar](../api/privilegedroleassignmentrequest-cancel.md)|  |Cancelar una solicitud de asignación de roles pendiente.|
|[My](../api/privilegedroleassignmentrequest-my.md)|  |Obtener la solicitud de asignación de rol para requstor actual.|

## <a name="properties"></a>Propiedades

| Propiedad     | Tipo        | Descripción |
|:-------------|:------------|:------------|
|id|String| Solo lectura. El identificador de la solicitud de asignación de rol.|
|assignmentState|String| El estado de la asignación. El valor puede ser `Eligible` para asignación optan `Active` - si está asignada directamente `Active` por los administradores, o activado en una asignación optan por los usuarios.|
|duration|String| La duración de una asignación de roles.|
|motivo|String| El motivo de la asignación de roles.|
|requestedDateTime|DateTimeOffset| Solo lectura. La solicitud de creación de tiempo. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|identificador de función|String| El identificador de la función.|
|programación|[governanceSchedule](governanceschedule.md)| El objeto de programación de la solicitud de asignación de rol.|
|status|String| Lectura cascada.se el estado de la solicitud de asignación de rol. El valor puede ser `NotStarted`,`Completed`,`RequestedApproval`,`Scheduled`,`Approved`,`ApprovalDenied`,`ApprovalAborted`,`Cancelling`,`Cancelled`,`Revoked`,`RequestExpired`.|
|ticketNumber|String| TicketNumber para la asignación de roles. |
|ticketSystem|String| TicketSystem para la asignación de roles.|
|type|String| Que representa el tipo de la operación en la asignación de roles. El valor puede ser `AdminAdd`: administradores agregar usuarios a funciones; `UserAdd`: Los usuarios agregar las asignaciones de roles.|
|userId|String| El identificador del usuario.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo        | Descripción |
|:-------------|:------------|:------------|
|roleInfo|[privilegedRole](privilegedrole.md)| El objeto roleInfo de la solicitud de asignación de rol.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedRoleAssignmentRequest"
}-->

```json
{
  "assignmentState": "String",
  "duration": "String",
  "id": "String (identifier)",
  "reason": "String",
  "requestedDateTime": "String (timestamp)",
  "roleId": "String",
  "schedule": {"@odata.type": "microsoft.graph.governanceSchedule"},
  "status": "String",
  "ticketNumber": "String",
  "ticketSystem": "String",
  "type": "String",
  "userId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRoleAssignmentRequest resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->