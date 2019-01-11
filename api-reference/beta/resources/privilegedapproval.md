---
title: tipo de recurso privilegedApproval
description: Representa una aprobación que se solicita en con privilegios de administración de identidades para obtener en una función.
localization_priority: Normal
ms.openlocfilehash: dee8cffba02270308c6786b2549b66aa5ad9dfa8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27868351"
---
# <a name="privilegedapproval-resource-type"></a>tipo de recurso privilegedApproval

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una aprobación que se solicita en con privilegios de administración de identidades para obtener en una función.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener privilegedApproval](../api/privilegedapproval-get.md) | [privilegedApproval](privilegedapproval.md) |Leer las propiedades y las relaciones del objeto privilegedApproval.|
|[Objetos de lista de privilegedApproval](../api/privilegedapproval-list.md) | colección de [privilegedApproval](privilegedapproval.md)|Obtener la colección de privilegedApproval.|
|[Crear privilegedApproval](../api/privilegedapproval-post-privilegedapproval.md) | [privilegedApproval](privilegedapproval.md)    |Crear objeto privilegedApproval. |
|[Actualizar privilegedApproval](../api/privilegedapproval-update.md) | [privilegedApproval](privilegedapproval.md) |Actualizar el objeto privilegedApproval. |
|[Myrequests](../api/privilegedapproval-myrequests.md)|[privilegedApproval](privilegedapproval.md)|Obtenga las solicitudes de aprobación del solicitante.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|approvalDuration|Duración||
|approvalState|string| Los valores posibles son: `pending`, `approved`, `denied`, `aborted` y `canceled`.|
|approvalType|Cadena||
|approverReason|Cadena||
|endDateTime|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|id|Cadena| Solo lectura.|
|requestorReason|Cadena||
|identificador de función|Cadena||
|startDateTime|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|userId|String||

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Description|
|:---------------|:--------|:----------|
|roleInfo|[privilegedRole](privilegedrole.md)| Solo lectura. Admite valores NULL.|
|solicitud|[privilegedRoleAssignmentRequest](privilegedroleassignmentrequest.md)| Solo lectura. La solicitud de asignación de roles para este objeto de aprobación|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedApproval"
}-->

```json
{
  "approvalDuration": "string (timestamp)",
  "approvalState": "string",
  "approvalType": "string",
  "approverReason": "String",
  "endDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "requestorReason": "String",
  "roleId": "String",
  "startDateTime": "String (timestamp)",
  "userId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedApproval resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
