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
# <a name="plannerplandetails-resource-type"></a><span data-ttu-id="43084-104">Tipo de recurso plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="43084-104">plannerPlanDetails resource type</span></span>

> <span data-ttu-id="43084-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="43084-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="43084-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="43084-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="43084-p103">El recurso **plannerPlanDetails** representa la información adicional de un plan. Cada objeto [plan](plannerplan.md) tiene un objeto details.</span><span class="sxs-lookup"><span data-stu-id="43084-p103">The **plannerPlanDetails** resource represents the additional information about a plan. Each [plan](plannerplan.md) object has a details object.</span></span>


## <a name="methods"></a><span data-ttu-id="43084-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="43084-109">Methods</span></span>

| <span data-ttu-id="43084-110">Método</span><span class="sxs-lookup"><span data-stu-id="43084-110">Method</span></span>           | <span data-ttu-id="43084-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43084-111">Return Type</span></span>    |<span data-ttu-id="43084-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="43084-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="43084-113">Obtener plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="43084-113">Get plannerPlanDetails</span></span>](../api/plannerplandetails-get.md) | [<span data-ttu-id="43084-114">plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="43084-114">plannerPlanDetails</span></span>](plannerplandetails.md) |<span data-ttu-id="43084-115">Lea las propiedades y relaciones de un objeto **plannerPlanDetails** .</span><span class="sxs-lookup"><span data-stu-id="43084-115">Read the properties and relationships of a **plannerPlanDetails** object.</span></span>|
|[<span data-ttu-id="43084-116">Update</span><span class="sxs-lookup"><span data-stu-id="43084-116">Update</span></span>](../api/plannerplandetails-update.md) | [<span data-ttu-id="43084-117">plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="43084-117">plannerPlanDetails</span></span>](plannerplandetails.md)    |<span data-ttu-id="43084-118">Actualizar un objeto **plannerPlanDetails** .</span><span class="sxs-lookup"><span data-stu-id="43084-118">Update a **plannerPlanDetails** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="43084-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="43084-119">Properties</span></span>
| <span data-ttu-id="43084-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="43084-120">Property</span></span>     | <span data-ttu-id="43084-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="43084-121">Type</span></span>   |<span data-ttu-id="43084-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="43084-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="43084-123">categoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="43084-123">categoryDescriptions</span></span>|[<span data-ttu-id="43084-124">plannerCategoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="43084-124">plannerCategoryDescriptions</span></span>](plannercategorydescriptions.md)|<span data-ttu-id="43084-125">Objeto que especifica las descripciones de las seis categorías que pueden estar asociadas a las tareas del plan</span><span class="sxs-lookup"><span data-stu-id="43084-125">An object that specifies the descriptions of the six categories that can be associated with tasks in the plan</span></span>|
|<span data-ttu-id="43084-126">id</span><span class="sxs-lookup"><span data-stu-id="43084-126">id</span></span>|<span data-ttu-id="43084-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="43084-127">String</span></span>| <span data-ttu-id="43084-128">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="43084-128">Read-only.</span></span> <span data-ttu-id="43084-129">El identificador de los detalles del plan.</span><span class="sxs-lookup"><span data-stu-id="43084-129">The ID of the plan details.</span></span> <span data-ttu-id="43084-130">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="43084-130">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="43084-131">[Validación de formato](tasks-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="43084-131">[Format validation](tasks-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="43084-132">sharedWith</span><span class="sxs-lookup"><span data-stu-id="43084-132">sharedWith</span></span>|[<span data-ttu-id="43084-133">plannerUserIds</span><span class="sxs-lookup"><span data-stu-id="43084-133">plannerUserIds</span></span>](planneruserids.md)|<span data-ttu-id="43084-134">El conjunto de identificadores que este plan se comparte con la de usuario.</span><span class="sxs-lookup"><span data-stu-id="43084-134">The set of user IDs that this plan is shared with.</span></span> <span data-ttu-id="43084-135">Si usa grupos de Office 365, use los grupos de API para administrar la pertenencia a grupos para compartir el plan [del grupo](group.md) .</span><span class="sxs-lookup"><span data-stu-id="43084-135">If you are using Office 365 Groups, use the groups API to manage group membership to share the [group's](group.md) plan.</span></span> <span data-ttu-id="43084-136">También puede agregar a los miembros existentes del grupo a esta colección, aunque no es necesario en orden para que tengan acceso el plan de propiedad del grupo.</span><span class="sxs-lookup"><span data-stu-id="43084-136">You can also add existing members of the group to this collection, although it is not required in order for them to access the plan owned by the group.</span></span> |
|<span data-ttu-id="43084-137">contextDetails</span><span class="sxs-lookup"><span data-stu-id="43084-137">contextDetails</span></span>|[<span data-ttu-id="43084-138">plannerPlanContextDetailsCollection</span><span class="sxs-lookup"><span data-stu-id="43084-138">plannerPlanContextDetailsCollection</span></span>](plannerplancontextdetailscollection.md)|<span data-ttu-id="43084-139">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="43084-139">Read-only.</span></span> <span data-ttu-id="43084-140">Una colección de información adicional asociada con las entradas de [plannerPlanContext](plannerplancontext.md) que se definen para el contenedor de [plannerPlan](plannerplan.md) .</span><span class="sxs-lookup"><span data-stu-id="43084-140">A collection of additional information associated with [plannerPlanContext](plannerplancontext.md) entries that are defined for the [plannerPlan](plannerplan.md) container.</span></span> |

## <a name="relationships"></a><span data-ttu-id="43084-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="43084-141">Relationships</span></span>
<span data-ttu-id="43084-142">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="43084-142">None.</span></span>


## <a name="json-representation"></a><span data-ttu-id="43084-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="43084-143">JSON representation</span></span>
<span data-ttu-id="43084-144">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="43084-144">The following is a JSON representation of the resource.</span></span>

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
