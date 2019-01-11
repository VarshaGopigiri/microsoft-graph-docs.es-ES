---
title: Tipo de recurso plannerPlanDetails
description: El recurso **plannerPlanDetails** representa la información adicional de un plan. Cada objeto plan tiene un objeto details.
localization_priority: Normal
ms.openlocfilehash: 59064093b485b6c82bd5b2e0b59ca1868e8517e4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867742"
---
# <a name="plannerplandetails-resource-type"></a><span data-ttu-id="cf096-104">Tipo de recurso plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="cf096-104">plannerPlanDetails resource type</span></span>


<span data-ttu-id="cf096-p102">El recurso **plannerPlanDetails** representa la información adicional de un plan. Cada objeto [plan](plannerplan.md) tiene un objeto details.</span><span class="sxs-lookup"><span data-stu-id="cf096-p102">The **plannerPlanDetails** resource represents the additional information about a plan. Each [plan](plannerplan.md) object has a details object.</span></span>


## <a name="methods"></a><span data-ttu-id="cf096-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf096-107">Methods</span></span>

| <span data-ttu-id="cf096-108">Método</span><span class="sxs-lookup"><span data-stu-id="cf096-108">Method</span></span>           | <span data-ttu-id="cf096-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf096-109">Return Type</span></span>    |<span data-ttu-id="cf096-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf096-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="cf096-111">Obtener plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="cf096-111">Get plannerPlanDetails</span></span>](../api/plannerplandetails-get.md) | [<span data-ttu-id="cf096-112">plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="cf096-112">plannerPlanDetails</span></span>](plannerplandetails.md) |<span data-ttu-id="cf096-113">Leer las propiedades y las relaciones del objeto **plannerPlanDetails**.</span><span class="sxs-lookup"><span data-stu-id="cf096-113">Read properties and relationships of **plannerPlanDetails** object.</span></span>|
|[<span data-ttu-id="cf096-114">Update</span><span class="sxs-lookup"><span data-stu-id="cf096-114">Update</span></span>](../api/plannerplandetails-update.md) | [<span data-ttu-id="cf096-115">plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="cf096-115">plannerPlanDetails</span></span>](plannerplandetails.md)    |<span data-ttu-id="cf096-116">Actualizar el objeto **plannerPlanDetails**.</span><span class="sxs-lookup"><span data-stu-id="cf096-116">Update **plannerPlanDetails** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="cf096-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf096-117">Properties</span></span>
| <span data-ttu-id="cf096-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf096-118">Property</span></span>     | <span data-ttu-id="cf096-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf096-119">Type</span></span>   |<span data-ttu-id="cf096-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf096-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="cf096-121">categoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="cf096-121">categoryDescriptions</span></span>|[<span data-ttu-id="cf096-122">plannerCategoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="cf096-122">plannerCategoryDescriptions</span></span>](plannercategorydescriptions.md)|<span data-ttu-id="cf096-123">Objeto que especifica las descripciones de las seis categorías que pueden estar asociadas a las tareas del plan</span><span class="sxs-lookup"><span data-stu-id="cf096-123">An object that specifies the descriptions of the six categories that can be associated with tasks in the plan</span></span>|
|<span data-ttu-id="cf096-124">id</span><span class="sxs-lookup"><span data-stu-id="cf096-124">id</span></span>|<span data-ttu-id="cf096-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf096-125">String</span></span>| <span data-ttu-id="cf096-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cf096-126">Read-only.</span></span> <span data-ttu-id="cf096-127">Identificador de los detalles del plan.</span><span class="sxs-lookup"><span data-stu-id="cf096-127">ID of the plan details.</span></span> <span data-ttu-id="cf096-128">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cf096-128">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="cf096-129">[Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="cf096-129">[Format validation](planner-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="cf096-130">sharedWith</span><span class="sxs-lookup"><span data-stu-id="cf096-130">sharedWith</span></span>|[<span data-ttu-id="cf096-131">plannerUserIds</span><span class="sxs-lookup"><span data-stu-id="cf096-131">plannerUserIds</span></span>](planneruserids.md)|<span data-ttu-id="cf096-p104">Conjunto de identificadores de usuario con el que se comparte este plan. Si está aprovechando los grupos de Office 365, use la API de grupos para administrar la pertenencia a los grupos a fin de compartir el plan del [grupo](group.md). También puede agregar los miembros existentes del grupo a esta colección, aunque no es necesario que obtengan acceso al plan propiedad del grupo.</span><span class="sxs-lookup"><span data-stu-id="cf096-p104">Set of user ids that this plan is shared with. If you are leveraging Office 365 Groups, use the Groups API to manage group membership to share the [group's](group.md) plan. You can also add existing members of the group to this collection though it is not required for them to access the plan owned by the group.</span></span> |

## <a name="relationships"></a><span data-ttu-id="cf096-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cf096-135">Relationships</span></span>
<span data-ttu-id="cf096-136">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cf096-136">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="cf096-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cf096-137">JSON representation</span></span>
<span data-ttu-id="cf096-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cf096-138">Here is a JSON representation of the resource.</span></span>

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
