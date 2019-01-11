---
title: tipo de recurso governanceRoleAssignmentRequest
description: Representa la solicitud para operaciones de asignación de rol de administración de identidades de Privilegd.
localization_priority: Normal
ms.openlocfilehash: 036e44a34d3c5373bcedba305eba6bd686c28601
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885095"
---
# <a name="governanceroleassignmentrequest-resource-type"></a>tipo de recurso governanceRoleAssignmentRequest

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la solicitud para operaciones de asignación de rol de administración de identidades de Privilegd.

`governanceRoleAssignmentRequest`se utiliza una entidad modelar vale para administrar el ciclo de vida de las asignaciones de roles. Representa la intención o la decisión de los usuarios y administradores y también proporciona la flexibilidad necesaria para permitir la implementación de schduling periódico, puertas de aprobación y así sucesivamente, con respecto a exponer directamente `POST`, `PUT`, y `DELETE` operaciones en `governanceRoleAssignment`.

## <a name="methods"></a>Métodos

| Método          |Tipo de valor devuelto  |Descripción|
|:------------|:--------|:--------|
|[Get](../api/governanceroleassignmentrequest-get.md) | [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md)|Obtener una solicitud de asignación de rol especificada por Id.  
|[List](../api/governanceroleassignmentrequest-list.md) | colección de [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md)|Obtenga las solicitudes de asignación de roles en un recurso.|
|[Create](../api/governanceroleassignmentrequest-post.md)|  [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md)|Cree una solicitud para administrar el ciclo de vida de la asignación de rol nuevo o existente.|
|[Cancel](../api/governanceroleassignmentrequest-cancel.md)|  |Cancelar una solicitud de asignación de roles pendiente.|
|[Update](../api/governanceroleassignmentrequest-update.md)| [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md)|Los administradores de actualizar las decisiones en las solicitudes de si las solicitudes se encuentran en estado de `PendingAdminDecision`.|

## <a name="properties"></a>Propiedades
| Propiedad                  | Tipo          |Descripción|
|:--------------------------|:--------------|:----------|
|id                         |Cadena         |El identificador de la solicitud de asignación de rol.|
|resourceId                 |Cadena         |Necesario. El identificador del recurso que está asociada la solicitud de asignación de rol.|
|roleDefinitionId           |Cadena         |Necesario. El identificador de la definición de roles que está asociada la solicitud de asignación de rol.|
|///SubjectID                  |Cadena         |Necesario. El identificador del sujeto que está asociada la solicitud de asignación de rol.|
|type                       |Cadena         |Necesario. Que representa el tipo de la operación en la asignación de roles. El valor puede ser <ul><li>`AdminAdd`: Administradores asignación a usuarios o grupos a roles;</li><li>`UserAdd`: Los usuarios activar asignaciones optan;</li><li> `AdminUpdate`: Administradores cambiar las asignaciones de roles existentes</li><li>`AdminRemove`: Administradores quitar usuarios o grupos de roles;<li>`UserRemove`: Los usuarios desactivación las asignaciones de activas;<li>`UserExtend`: Usuarios solicitud para ampliar sus asignaciones a punto de expirar;</li><li>`AdminExtend`: Administradores ampliación las asignaciones a punto de expirar.</li><li>`UserRenew`: Solicitud los usuarios renovar sus asignaciones que han expirado;</li><li>`AdminRenew`: Administradores ampliación las asignaciones a punto de expirar.</li></ul>|
|assignmentState|Cadena  |Necesario. El estado de la asignación. El valor puede ser <ul><li> `Eligible`para asignación optan</li><li> `Active`-Si está asignada directamente `Active` por los administradores, o activado en una asignación optan por los usuarios.</li></ul>|
|requestedDateTime          |DateTimeOffset |Solo lectura. La solicitud de creación de tiempo. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|programación                   |[governanceSchedule](governanceschedule.md)|El objeto de programación de la solicitud de asignación de rol.|
|motivo                     |Cadena         |Un mensaje proporcionado por los usuarios y los administradores cuando crea la solicitud acerca de por qué es necesario.|
|status                     |[governanceRoleAssignmentRequestStatus](governanceroleassignmentrequeststatus.md)         |El estado de la solicitud de asignación de rol.|
|linkedEligibleRoleAssignmentId|Cadena        |Si se trata de una solicitud de activación de rol, representa el identificador de la `eligible assignment` que se hace referencia; De lo contrario, el valor es `null`. |



## <a name="relationships"></a>Relaciones
| Relación | Tipo                                |Descripción|
|:-------------|:----------------------------------|:----------|
|resource      |[governanceResource](../resources/governanceresource.md)            |Solo lectura. El recurso que se pretende la solicitud. |
|roleDefinition|[governanceRoleDefinition](../resources/governanceroledefinition.md)|Solo lectura. La definición de roles que se pretende la solicitud. |
|subject       |[governanceSubject](../resources/governancesubject.md)|Solo lectura. La entidad de seguridad de usuario o grupo.|

### <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
}-->

```json
{
  "id": "String (identifier)",
  "resourceId": "String",
  "roleDefinitionId": "String",
  "subjectId": "String",
  "type": "String",
  "assignmentState": "String",
  "reason": "String",
  "requestedDateTime": "String (timestamp)",
  "schedule": {"@odata.type": "microsoft.graph.governanceSchedule"},
  "status": {"@odata.type": "microsoft.graph.governanceRoleAssignmentRequestStatus"},
  "linkedEligibleRoleAssignmentId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceRoleAssignmentRequest",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
