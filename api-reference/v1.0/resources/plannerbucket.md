---
title: Tipo de recurso plannerBucket
description: ) para las tareas de un plan de Office 365. Está contenida en un plannerPlan y puede tener una colección de plannerTasks.
author: TarkanSevilmis
localization_priority: Normal
ms.prod: planner
ms.openlocfilehash: 8cfc25e5554b20d4f808c8929b53549f4c44d7a2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982837"
---
# <a name="plannerbucket-resource-type"></a>Tipo de recurso plannerBucket

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
|id|String| Solo lectura. Identificador del depósito de. Es 28 caracteres de largo y entre mayúsculas y minúsculas. [Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.|
|name|String|Nombre del depósito.|
|orderHint|String|Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define tal como se describe [aquí](planner-order-hint-format.md).|
|planId|String|Id. de plan al que pertenece el depósito.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|tasks|Colección [plannerTask](plannertask.md)| Solo lectura. Admite valores NULL. Colección de tareas del depósito.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
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
