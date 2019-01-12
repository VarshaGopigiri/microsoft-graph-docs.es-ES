---
title: Tipo de recurso planner
description: El recurso **planner** es el punto de entrada para el modelo de objetos de Planner. Devuelve un recurso **planner** singleton.  No contiene ninguna propiedad utilizable.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: f6d25238436b79dec0397df1d005e67e6b17239a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27955138"
---
# <a name="planner-resource-type"></a>Tipo de recurso planner

El recurso **planner** es el punto de entrada para el modelo de objetos de Planner. Devuelve un recurso **planner** singleton.  No contiene ninguna propiedad utilizable.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear plannerBucket](../api/planner-post-buckets.md) |[plannerBucket](plannerbucket.md)| Crear un nuevo **plannerBucket** publicándolo en la colección de depósitos.|
|[Crear plannerPlan](../api/planner-post-plans.md) |[plannerPlan](plannerplan.md)| Crear un nuevo **plannerPlan** publicándolo en la colección de planes.|
|[Crear plannerTask](../api/planner-post-tasks.md) |[plannerTask](plannertask.md)| Crear una nueva **plannerTask** publicándola en la colección de tareas.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|buckets|Colección [plannerBucket](plannerbucket.md)| Solo lectura. Admite valores NULL. Devuelve una colección de los depósitos especificados|
|plans|Colección [plannerPlan](plannerplan.md)| Solo lectura. Admite valores NULL. Devuelve una colección de los planes especificados|
|tasks|Colección [plannerTask](plannertask.md)| Solo lectura. Admite valores NULL. Devuelve una colección de las tareas especificadas|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.planner"
}-->

```json
{
}
```

## <a name="example"></a>Ejemplo

El recurso de **Organizador** está disponible en la raíz del gráfico.

<!--{
  "blockType": "request"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner
```

<!--{
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.planner"
}-->
```json
HTTP/1.1 200 OK
Content-type: application/json

{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "planner resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
