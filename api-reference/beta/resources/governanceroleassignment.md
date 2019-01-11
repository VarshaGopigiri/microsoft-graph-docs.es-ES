---
title: tipo de recurso governanceRoleAssignment
description: Representa la asignación de un usuario o grupo a una función.
localization_priority: Normal
ms.openlocfilehash: d873b122f319ca82882727f065818b33f7f9d44d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882694"
---
# <a name="governanceroleassignment-resource-type"></a>tipo de recurso governanceRoleAssignment
> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la asignación de un usuario o grupo a una función.

Administración de identidad con privilegios (PIM) admite dos tipos de asignaciones:

1. Asignación activa - representa el acceso directo/activa a los recursos.
2. Asignación optan - representa una fase intermedia de acceso con privilegios a los recursos entre sin acceso y el acceso directo. Los administradores pueden asignar a los usuarios o grupos a `eligible assignment` de antemano y cada vez que se necesita el acceso, `activation` en el `eligible assignment` es necesario para obtener el acceso instantáneo a los recursos para varias horas. Después de la activación, un `active assignment` se creará para que los miembros de los usuarios o grupos indicar el estado activado.

## <a name="methods"></a>Métodos

| Método          | Tipo de valor devuelto |Descripción|
|:------------|:--------|:--------|
|[Get](../api/governanceroleassignment-get.md) |  [governanceRoleAssignment](../resources/governanceroleassignment.md) |Leer las propiedades y las relaciones de una entidad de la asignación de rol.|
|[List](../api/governanceroleassignment-list.md) | colección de [governanceRoleAssignment](../resources/governanceroleassignment.md)|Una colección de asignaciones de roles en un recurso de la lista. |
|[Export](../api/governanceroleassignment-export.md) | secuencia de octetos |Descargue una colección de asignaciones de roles en un recurso y guardar como un `.csv` archivo.|

No `POST`, `PUT`, `PATCH`, o `DELETE` operaciones son compatibles con el `roleAssignments` conjunto de entidades. Cualquier crear, actualizar y eliminar operaciones en `governanceRoleAssignment` se realizan mediante `governanceRoleAssignmentRequest`.

## <a name="properties"></a>Propiedades
| Propiedad  | Tipo      |Descripción|
|:----------|:----------|:----------|
|id         |Cadena     |El identificador de la asignación de roles. Está en formato de GUID.|
|resourceId |Cadena     |Necesario. El identificador del recurso que está asociada la asignación de roles. |
|roleDefinitionId|Cadena|Necesario. El identificador de la definición de roles que está asociada la asignación de roles. |
|///SubjectID|Cadena       |Necesario. El identificador del sujeto que está asociada la asignación de roles. |
|linkedEligibleRoleAssignmentId|Cadena|Si se trata de un `active assignment` y creado debido a la activación en un `eligible assignment`, que representa el identificador de la que `eligible assignment`; De lo contrario, el valor es `null`. |
|externalId   |String     |El identificador externo el recurso que se usa para identificar la asignación de roles en el proveedor.|
|startDateTime|DateTimeOffset|La hora de inicio de la asignación de roles. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|endDateTime|DateTimeOffset|Para una asignación de roles de no permanente, es la hora cuando la asignación de rol caducará. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|assignmentState|Cadena  |El estado de la asignación. El valor puede ser <ul><li> `Eligible`para asignación optan</li><li> `Active`-Si está asignada directamente `Active` por los administradores, o activado en una asignación optan por los usuarios.</li></ul>|
|memberType|Cadena      |El tipo de miembro. El valor puede ser: <ul><li>`Inherited`-la asignación de roles se hereda de un ámbito de recurso primario</li><li>`Group`-la asignación de roles no se hereda, pero procede de la pertenencia de una asignación de grupo</li><li>`User`-ni se hereda la asignación de roles ni desde una asignación de grupo.</li></ul>|


## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|resource|[governanceResource](../resources/governanceresource.md)|Solo lectura. El recurso asociado a la asignación de roles. |
|roleDefinition|[governanceRoleDefinition](../resources/governanceroledefinition.md)|Solo lectura. La definición de roles asociada con la asignación de roles. |
|subject|[governanceSubject](../resources/governancesubject.md)|Solo lectura. Asunto asociado con la asignación de roles. |
|linkedEligibleRoleAssignment|[governanceRoleAssignment](../resources/governanceroleassignment.md)|Solo lectura. Si se trata de un `active assignment` y creado debido a la activación en un `eligible assignment`, que representa el objeto del que `eligible assignment`; De lo contrario, el valor es `null`. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.


<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceRoleAssignment"
}-->

```json
{
  "id": "String (identifier)",
  "resourceId": "String",
  "roleDefinitionId": "String",
  "subjectId": "String",
  "linkedEligibleRoleAssignmentId": "String",
  "externalId": "String",
  "startDateTime": "String (timestamp)",
  "endDateTime": "String (timestamp)",
  "assignmentState": "String",
  "memberType": "String",
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceRoleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
