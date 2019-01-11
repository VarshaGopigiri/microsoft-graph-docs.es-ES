---
title: Tipo de recurso plannerBucket
description: ) para las tareas de un plan de Office 365. Está contenida en un plannerPlan y puede tener una colección de plannerTasks.
author: TarkanSevilmis
localization_priority: Normal
ms.openlocfilehash: 4868fb3925fa3ae94571d5cc93b0da12434b00dd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27808123"
---
# <a name="plannerbucket-resource-type"></a>Tipo de recurso plannerBucket

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **plannerBucket** representa un depósito (o "columna personalizada") para las tareas de un plan de Office 365. Se encuentra en un [plannerPlan](plannerplan.md) y puede tener una colección de [plannerTasks](plannertask.md).



## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener plannerBucket](../api/plannerbucket-get.md) | [plannerBucket](plannerbucket.md) |Leer las propiedades y las relaciones del objeto **plannerBucket**.|
|[Enumerar plannerTasks](../api/plannerbucket-list-tasks.md) |Colección [plannerTask](plannertask.md)| Obtenga una colección de objetos **plannerTask**.|
|[Create](../api/planner-post-buckets.md) | [plannerBucket](plannerbucket.md)   | Crear un nuevo objeto **plannerBucket**. |
|[Update](../api/plannerbucket-update.md) | [plannerBucket](plannerbucket.md)   |Actualizar el objeto **plannerBucket**. |
|[Delete](../api/plannerbucket-delete.md) | Ninguno |Eliminar el objeto **plannerBucket**. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| Solo lectura. Identificador del depósito de. Es 28 caracteres de largo y entre mayúsculas y minúsculas. [Validación de formato](tasks-identifiers-disclaimer.md) se realiza en el servicio.|
|name|Cadena|Nombre del depósito.|
|orderHint|Cadena|Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define tal como se describe [aquí](planner-order-hint-format.md).|
|planId|Cadena|Id. de plan al que pertenece el depósito.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|tasks|Colección [plannerTask](plannertask.md)| Solo lectura. Admite valores NULL. Colección de tareas del depósito.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerBucket"
}-->

```json
{
  "id": "String (identifier)",
  "name": "String",
  "orderHint": "String",
  "planId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerBucket resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
