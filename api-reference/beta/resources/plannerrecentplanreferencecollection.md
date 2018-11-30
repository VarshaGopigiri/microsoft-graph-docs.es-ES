---
title: tipo de recurso plannerRecentPlanReferenceCollection
description: El recurso **plannerRecentPlanReferenceCollection** representa la colección de referencias a los planes que se han visto recientemente por un usuario. Este recurso es un tipo abierto y forma parte del objeto plannerUser. El nombre de la propiedad es el identificador del plan correspondiente. El valor en el par de valor de la propiedad es el objeto plannerRecentPlanReference.
ms.openlocfilehash: b22f7367a1826c95889b63a6884885ce49497c33
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090997"
---
# <a name="plannerrecentplanreferencecollection-resource-type"></a><span data-ttu-id="3eae1-106">tipo de recurso plannerRecentPlanReferenceCollection</span><span class="sxs-lookup"><span data-stu-id="3eae1-106">plannerRecentPlanReferenceCollection resource type</span></span>

> <span data-ttu-id="3eae1-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3eae1-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3eae1-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3eae1-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3eae1-109">El recurso **plannerRecentPlanReferenceCollection** representa la colección de referencias a los planes que se han visto recientemente por un usuario.</span><span class="sxs-lookup"><span data-stu-id="3eae1-109">The **plannerRecentPlanReferenceCollection** resource represents the collection of references to plans that were recently viewed by a user.</span></span> <span data-ttu-id="3eae1-110">Este recurso es un tipo abierto y forma parte del objeto [plannerUser](planneruser.md) .</span><span class="sxs-lookup"><span data-stu-id="3eae1-110">This resource is an open type and is part of the [plannerUser](planneruser.md) object.</span></span> <span data-ttu-id="3eae1-111">El nombre de la propiedad es el identificador del plan correspondiente.</span><span class="sxs-lookup"><span data-stu-id="3eae1-111">The property name is the ID of the corresponding plan.</span></span> <span data-ttu-id="3eae1-112">El valor en el par de valor de la propiedad es el objeto [plannerRecentPlanReference](plannerrecentplanreference.md) .</span><span class="sxs-lookup"><span data-stu-id="3eae1-112">The value in the property-value pair is the [plannerRecentPlanReference](plannerrecentplanreference.md) object.</span></span>
<span data-ttu-id="3eae1-113">Adición de referencias nuevo a esta colección se quitan automáticamente las entradas más antiguas cuando el tamaño de la colección supera un valor máximo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3eae1-113">Adding new references to this collection will automatically remove the oldest entries when the size of the collection exceeds a predetermined maximum value.</span></span>


## <a name="properties"></a><span data-ttu-id="3eae1-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3eae1-114">Properties</span></span>
<span data-ttu-id="3eae1-115">Puede definir las propiedades de este tipo abierto.</span><span class="sxs-lookup"><span data-stu-id="3eae1-115">You can define the properties of this open type.</span></span> <span data-ttu-id="3eae1-116">Los nombres de propiedad son `id` valores de recursos de [plannerPlan](plannerplan.md) y sus valores deben ser [plannerRecentPlanReference](plannerrecentplanreference.md) objetos.</span><span class="sxs-lookup"><span data-stu-id="3eae1-116">The property names are `id` values of [plannerPlan](plannerplan.md) resources and their values must be [plannerRecentPlanReference](plannerrecentplanreference.md) objects.</span></span> <span data-ttu-id="3eae1-117">Para quitar un elemento en la lista de favoritos, establezca el valor de la propiedad en `null`.</span><span class="sxs-lookup"><span data-stu-id="3eae1-117">To remove an item in the favorites list, set the value of the property to `null`.</span></span>


## <a name="json-representation"></a><span data-ttu-id="3eae1-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3eae1-118">JSON representation</span></span>

<span data-ttu-id="3eae1-119">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3eae1-119">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerRecentPlanReferenceCollection"
}-->

```json
{
  "7oTB5aMIAE2rVo-1N-L7RmQAGX2q": {
    "@odata.type": "microsoft.graph.plannerRecentPlanReference",
    "lastAccessedDateTime": "2017-12-02T22:49:46.155Z",
    "planTitle": "Purchase Workflow"
  },
  "iKNMHkk3vEWpSF7F7iZWIGQAAMMw": {
    "@odata.type": "microsoft.graph.plannerRecentPlanReference",
    "lastAccessedDateTime": "2017-12-03T21:59:28.975Z",
    "planTitle": "New Year's Office Party"
  }
}
```



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerRecentPlanReferenceCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
