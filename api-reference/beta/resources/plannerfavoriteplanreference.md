---
title: tipo de recurso plannerFavoritePlanReference
description: 'El recurso **plannerFavoritePlanReference** escriba representa una referencia a un plannerPlan que se ha marcado como un favorito por el usuario. '
ms.openlocfilehash: bd399572dfce54ee7e46da6af60eb661484519de
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085012"
---
# <a name="plannerfavoriteplanreference-resource-type"></a><span data-ttu-id="ce816-103">tipo de recurso plannerFavoritePlanReference</span><span class="sxs-lookup"><span data-stu-id="ce816-103">plannerFavoritePlanReference resource type</span></span>

> <span data-ttu-id="ce816-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ce816-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ce816-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ce816-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ce816-106">El recurso **plannerFavoritePlanReference** escriba representa una referencia a un [plannerPlan](plannerplan.md) que se ha marcado como un favorito por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ce816-106">The **plannerFavoritePlanReference** resource type repesents a reference to a [plannerPlan](plannerplan.md) that has been marked as a favorite by the user.</span></span> <span data-ttu-id="ce816-107">Los clientes deben tener en cuenta que las entradas de **plannerFavoritePlanReference** pueden hacer referencia a **plannerPlans** que se eliminan, que ya no se puede obtener acceso el usuario, o que se han actualizado con un título diferente.</span><span class="sxs-lookup"><span data-stu-id="ce816-107">Clients should note that **plannerFavoritePlanReference** entries can reference **plannerPlans** that are deleted, that the user can no longer access, or that have been updated with a different title.</span></span>

<span data-ttu-id="ce816-108">Se recomienda que los clientes notificar a los usuarios cuando hay discrepancias y mantener actualizadas las entradas.</span><span class="sxs-lookup"><span data-stu-id="ce816-108">We recommend that clients notify users when there are discrepancies and keep the entries up to date.</span></span>


## <a name="properties"></a><span data-ttu-id="ce816-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce816-109">Properties</span></span>
| <span data-ttu-id="ce816-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ce816-110">Property</span></span>     | <span data-ttu-id="ce816-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce816-111">Type</span></span>   |<span data-ttu-id="ce816-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce816-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ce816-113">orderHint</span><span class="sxs-lookup"><span data-stu-id="ce816-113">orderHint</span></span>|<span data-ttu-id="ce816-114">String</span><span class="sxs-lookup"><span data-stu-id="ce816-114">String</span></span>|<span data-ttu-id="ce816-p103">Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define en [Using order hints in Planner](planner-order-hint-format.md) (Usar sugerencias de orden en Planner).</span><span class="sxs-lookup"><span data-stu-id="ce816-p103">Hint used to order items of this type in a list view. The format is defined in [Using order hints in Planner](planner-order-hint-format.md).</span></span>|
|<span data-ttu-id="ce816-117">planTitle</span><span class="sxs-lookup"><span data-stu-id="ce816-117">planTitle</span></span>|<span data-ttu-id="ce816-118">String</span><span class="sxs-lookup"><span data-stu-id="ce816-118">String</span></span>|<span data-ttu-id="ce816-119">Título del plan en el momento en que el usuario marca como favorito.</span><span class="sxs-lookup"><span data-stu-id="ce816-119">Title of the plan at the time the user marked it as a favorite.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="ce816-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ce816-120">JSON representation</span></span>

<span data-ttu-id="ce816-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ce816-121">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerFavoritePlanReference"
}-->

```json
{
  "orderHint": "String",
  "planTitle": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerFavoritePlanReference resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->