---
title: tipo de recurso directoryAudit
description: Este recurso representa los elementos de auditoría de Active directory y su colección
author: lleonard-msft
localization_priority: Priority
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 1f980208788731206dc58870635644a1f3edc4c7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991786"
---
# <a name="directoryaudit-resource-type"></a>tipo de recurso directoryAudit
Este recurso representa los elementos de auditoría de Active directory y su colección


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Lista directoryAudits](../api/directoryaudit-list.md) | [directoryAudit](directoryaudit.md) |Lista de los elementos de auditoría de Active directory en la colección y sus propiedades.|
|[Obtener directoryAudit](../api/directoryaudit-get.md) | [directoryAudit](directoryaudit.md) |Obtener un elemento de auditoría de directorio específica y sus propiedades.|


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|activityDateTime|DateTimeOffset|Indica la fecha y hora que se llevó a cabo la actividad. El tipo de marca de tiempo es siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|activityDisplayName|Cadena|Indica el nombre de la actividad o el nombre de la operación (por ejemplo "Crear usuario", "Agregar miembros al grupo"). Para obtener una lista de actividades que se registran, hacer referencia a la [lista de actividades de Azure Ad](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-activity-audit-logs#azure-ad-audit-activity-list).|
|additionalDetails|colección [keyValue](keyvalue.md)|Indica información adicional sobre la actividad.|
|.|String|Indica qué categoría de recurso que está dirigido por la actividad. (Por ejemplo: administración de usuario, grupo de administración etcetera..)|
|correlationId|GUID|Indica un identificador único que ayuda a relacionar actividades que abarcan varios servicios. Se puede usar para los registros de seguimiento a través de servicios.|
|id|Cadena| Indica el identificador único para la actividad. Esto es un GUID.|
|initiatedBy|[auditActivityInitiator](auditactivityinitiator.md)|Indica información sobre el usuario o aplicación iniciadas por la actividad.|
|loggedByService|Cadena|Indica información en el que la actividad iniciadas por el servicio (por ejemplo: administración de contraseñas sin intervención del administrador, directorios principales, B2C, los usuarios invitados, Microsoft Identity Manager, con privilegios de administración de identidades.|
|Resultado|string| Indica el resultado de la actividad. Los valores posibles son: `success`, `failure`, `timeout`, `unknownFutureValue`.||
|resultReason|Cadena|Indica el motivo del error si el resultado es "Error" o "tiempo de espera".|
|targetResources|colección de [targetResource](targetresource.md)|Indica información en la que el recurso se cambió debido a la actividad. Tipo de recurso de destino puede ser usuario, dispositivo, Active Directory, aplicación, rol, grupo, directiva u otra.

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directoryAudit"
}-->

```json
{
  "activityDateTime": "String (timestamp)",
  "activityDisplayName": "String",
  "additionalDetails": [{"@odata.type": "microsoft.graph.keyValue"}],
  "category": "String",
  "correlationId": "Guid",
  "id": "String (identifier)",
  "initiatedBy": {"@odata.type": "microsoft.graph.auditActivityInitiator"},
  "loggedByService": "String",
  "result": "string",
  "resultReason": "String",
  "targetResources": [{"@odata.type": "microsoft.graph.targetResource"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryAudit resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
