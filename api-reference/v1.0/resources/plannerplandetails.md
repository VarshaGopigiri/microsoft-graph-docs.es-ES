---
title: Tipo de recurso plannerPlanDetails
description: El recurso **plannerPlanDetails** representa la información adicional de un plan. Cada objeto plan tiene un objeto details.
ms.openlocfilehash: eac0082c72e46101d8d02367f8c13aef5e921d17
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029170"
---
# <a name="plannerplandetails-resource-type"></a><span data-ttu-id="e1b9b-104">Tipo de recurso plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="e1b9b-104">plannerPlanDetails resource type</span></span>


<span data-ttu-id="e1b9b-p102">El recurso **plannerPlanDetails** representa la información adicional de un plan. Cada objeto [plan](plannerplan.md) tiene un objeto details.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-p102">The **plannerPlanDetails** resource represents the additional information about a plan. Each [plan](plannerplan.md) object has a details object.</span></span>


## <a name="methods"></a><span data-ttu-id="e1b9b-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="e1b9b-107">Methods</span></span>

| <span data-ttu-id="e1b9b-108">Método</span><span class="sxs-lookup"><span data-stu-id="e1b9b-108">Method</span></span>           | <span data-ttu-id="e1b9b-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1b9b-109">Return Type</span></span>    |<span data-ttu-id="e1b9b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1b9b-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e1b9b-111">Obtener plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="e1b9b-111">Get plannerPlanDetails</span></span>](../api/plannerplandetails-get.md) | [<span data-ttu-id="e1b9b-112">plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="e1b9b-112">plannerPlanDetails</span></span>](plannerplandetails.md) |<span data-ttu-id="e1b9b-113">Leer las propiedades y las relaciones del objeto **plannerPlanDetails**.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-113">Read properties and relationships of **plannerPlanDetails** object.</span></span>|
|[<span data-ttu-id="e1b9b-114">Update</span><span class="sxs-lookup"><span data-stu-id="e1b9b-114">Update</span></span>](../api/plannerplandetails-update.md) | [<span data-ttu-id="e1b9b-115">plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="e1b9b-115">plannerPlanDetails</span></span>](plannerplandetails.md)    |<span data-ttu-id="e1b9b-116">Actualizar el objeto **plannerPlanDetails**.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-116">Update **plannerPlanDetails** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="e1b9b-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e1b9b-117">Properties</span></span>
| <span data-ttu-id="e1b9b-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e1b9b-118">Property</span></span>     | <span data-ttu-id="e1b9b-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1b9b-119">Type</span></span>   |<span data-ttu-id="e1b9b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1b9b-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e1b9b-121">categoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="e1b9b-121">categoryDescriptions</span></span>|[<span data-ttu-id="e1b9b-122">plannerCategoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="e1b9b-122">plannerCategoryDescriptions</span></span>](plannercategorydescriptions.md)|<span data-ttu-id="e1b9b-123">Objeto que especifica las descripciones de las seis categorías que pueden estar asociadas a las tareas del plan</span><span class="sxs-lookup"><span data-stu-id="e1b9b-123">An object that specifies the descriptions of the six categories that can be associated with tasks in the plan</span></span>|
|<span data-ttu-id="e1b9b-124">id</span><span class="sxs-lookup"><span data-stu-id="e1b9b-124">id</span></span>|<span data-ttu-id="e1b9b-125">String</span><span class="sxs-lookup"><span data-stu-id="e1b9b-125">String</span></span>| <span data-ttu-id="e1b9b-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-126">Read-only.</span></span> <span data-ttu-id="e1b9b-127">Identificador de los detalles del plan.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-127">ID of the plan details.</span></span> <span data-ttu-id="e1b9b-128">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-128">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="e1b9b-129">[Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-129">[Format validation](planner-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="e1b9b-130">sharedWith</span><span class="sxs-lookup"><span data-stu-id="e1b9b-130">sharedWith</span></span>|[<span data-ttu-id="e1b9b-131">plannerUserIds</span><span class="sxs-lookup"><span data-stu-id="e1b9b-131">plannerUserIds</span></span>](planneruserids.md)|<span data-ttu-id="e1b9b-p104">Conjunto de identificadores de usuario con el que se comparte este plan. Si está aprovechando los grupos de Office 365, use la API de grupos para administrar la pertenencia a los grupos a fin de compartir el plan del [grupo](group.md). También puede agregar los miembros existentes del grupo a esta colección, aunque no es necesario que obtengan acceso al plan propiedad del grupo.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-p104">Set of user ids that this plan is shared with. If you are leveraging Office 365 Groups, use the Groups API to manage group membership to share the [group's](group.md) plan. You can also add existing members of the group to this collection though it is not required for them to access the plan owned by the group.</span></span> |

## <a name="relationships"></a><span data-ttu-id="e1b9b-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e1b9b-135">Relationships</span></span>
<span data-ttu-id="e1b9b-136">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e1b9b-136">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="e1b9b-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e1b9b-137">JSON representation</span></span>
<span data-ttu-id="e1b9b-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-138">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.plannerPlanDetails"
}-->

```json
{
  "categoryDescriptions": {"@odata.type": "microsoft.graph.plannerCategoryDescriptions"},
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