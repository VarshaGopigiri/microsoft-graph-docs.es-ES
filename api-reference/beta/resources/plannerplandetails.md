---
title: Tipo de recurso plannerPlanDetails
description: El recurso **plannerPlanDetails** representa la información adicional de un plan. Cada objeto plan tiene un objeto details.
localization_priority: Normal
ms.openlocfilehash: 117a2f69324180a7ef45dcf96c773f510bdbcb9d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860161"
---
# <a name="plannerplandetails-resource-type"></a>Tipo de recurso plannerPlanDetails

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **plannerPlanDetails** representa la información adicional de un plan. Cada objeto [plan](plannerplan.md) tiene un objeto details.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener plannerPlanDetails](../api/plannerplandetails-get.md) | [plannerPlanDetails](plannerplandetails.md) |Lea las propiedades y relaciones de un objeto **plannerPlanDetails** .|
|[Update](../api/plannerplandetails-update.md) | [plannerPlanDetails](plannerplandetails.md)    |Actualizar un objeto **plannerPlanDetails** . |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|categoryDescriptions|[plannerCategoryDescriptions](plannercategorydescriptions.md)|Objeto que especifica las descripciones de las seis categorías que pueden estar asociadas a las tareas del plan|
|id|Cadena| Solo lectura. El identificador de los detalles del plan. Es 28 caracteres de largo y entre mayúsculas y minúsculas. [Validación de formato](tasks-identifiers-disclaimer.md) se realiza en el servicio.|
|sharedWith|[plannerUserIds](planneruserids.md)|El conjunto de identificadores que este plan se comparte con la de usuario. Si usa grupos de Office 365, use los grupos de API para administrar la pertenencia a grupos para compartir el plan [del grupo](group.md) . También puede agregar a los miembros existentes del grupo a esta colección, aunque no es necesario en orden para que tengan acceso el plan de propiedad del grupo. |
|contextDetails|[plannerPlanContextDetailsCollection](plannerplancontextdetailscollection.md)|Solo lectura. Una colección de información adicional asociada con las entradas de [plannerPlanContext](plannerplancontext.md) que se definen para el contenedor de [plannerPlan](plannerplan.md) . |

## <a name="relationships"></a>Relaciones
Ninguna.


## <a name="json-representation"></a>Representación JSON
La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlanDetails"
}-->

```json
{
  "categoryDescriptions": {"@odata.type": "microsoft.graph.plannerCategoryDescriptions"},
  "contextDetails": {"@odata.type": "microsoft.graph.plannerPlanContextDetailsCollection"},
  "id": "String (identifier)",
  "sharedWith": {"@odata.type": "microsoft.graph.plannerUserIds"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlanDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
