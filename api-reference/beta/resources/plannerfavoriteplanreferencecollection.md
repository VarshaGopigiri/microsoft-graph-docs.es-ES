---
title: tipo de recurso plannerFavoritePlanReferenceCollection
description: " el valor es el objeto plannerFavoritePlanReference."
ms.openlocfilehash: 78544e17604a0938cc0e88969e2542fc26bdff1b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089249"
---
# <a name="plannerfavoriteplanreferencecollection-resource-type"></a><span data-ttu-id="2f41b-103">tipo de recurso plannerFavoritePlanReferenceCollection</span><span class="sxs-lookup"><span data-stu-id="2f41b-103">plannerFavoritePlanReferenceCollection resource type</span></span>

> <span data-ttu-id="2f41b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2f41b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2f41b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2f41b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2f41b-106">El recurso **plannerFavoritePlanReferenceCollection** representa la colección de referencias a los planes que están marcadas como un favorito por un usuario.</span><span class="sxs-lookup"><span data-stu-id="2f41b-106">The **plannerFavoritePlanReferenceCollection** resource represents the collection of references to plans that are marked as a favorite by a user.</span></span> <span data-ttu-id="2f41b-107">Este recurso es un tipo abierto y forma parte del objeto [plannerUser](planneruser.md) .</span><span class="sxs-lookup"><span data-stu-id="2f41b-107">This resource is an open type and is part of the [plannerUser](planneruser.md) object.</span></span> <span data-ttu-id="2f41b-108">El nombre de la propiedad en el par de valor de la propiedad es el identificador del plan correspondiente; el valor es el objeto [plannerFavoritePlanReference](plannerfavoriteplanreference.md) .</span><span class="sxs-lookup"><span data-stu-id="2f41b-108">The property name in the property-value pair is the ID of the corresponding plan; the value is the [plannerFavoritePlanReference](plannerfavoriteplanreference.md) object.</span></span>


## <a name="properties"></a><span data-ttu-id="2f41b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2f41b-109">Properties</span></span>
<span data-ttu-id="2f41b-110">Puede definir las propiedades de este tipo abierto.</span><span class="sxs-lookup"><span data-stu-id="2f41b-110">You can define the properties of this open type.</span></span> <span data-ttu-id="2f41b-111">Los nombres de propiedad son `id` valores de recursos de [plannerPlan](plannerplan.md) y sus valores deben ser [plannerFavoritePlanReference](plannerfavoriteplanreference.md) objetos.</span><span class="sxs-lookup"><span data-stu-id="2f41b-111">The property names are `id` values of [plannerPlan](plannerplan.md) resources and their values must be [plannerFavoritePlanReference](plannerfavoriteplanreference.md) objects.</span></span> <span data-ttu-id="2f41b-112">Para quitar un elemento en la lista de favoritos, establezca el valor de la propiedad en `null`.</span><span class="sxs-lookup"><span data-stu-id="2f41b-112">To remove an item in the favorites list, set the value of the property to `null`.</span></span>


## <a name="json-representation"></a><span data-ttu-id="2f41b-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2f41b-113">JSON representation</span></span>

<span data-ttu-id="2f41b-114">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="2f41b-114">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerFavoritePlanReferenceCollection"
}-->

```json
{
  "jd8S5gOaFk2S8aWCIAJz42QAAxtD": {
    "@odata.type": "microsoft.graph.plannerFavoritePlanReference",
    "orderHint": "8586866870001551087",
    "planTitle": "Customer reviews"
  },
  "uZWtCtli30CGoWLIWSat1mQAC0ai": {
    "@odata.type": "microsoft.graph.plannerFavoritePlanReference",
    "orderHint": "8586848705198093378",
    "planTitle": "Order Management (December 2017)"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerFavoritePlanReferenceCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
