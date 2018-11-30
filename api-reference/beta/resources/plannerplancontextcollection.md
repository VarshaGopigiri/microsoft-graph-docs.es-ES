---
title: tipo de recurso plannerPlanContextCollection
description: El recurso **plannerPlanContextCollection** representa la colección de contextos externos al que está vinculado un plan. Este recurso es un tipo abierto y forma parte del objeto plannerPlan. El valor en el par de valor de la propiedad es el objeto plannerPlanContext.
ms.openlocfilehash: ae17e604bf3d59b7b825fe36a8f93f05d5cc835f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086822"
---
# <a name="plannerplancontextcollection-resource-type"></a><span data-ttu-id="c6335-105">tipo de recurso plannerPlanContextCollection</span><span class="sxs-lookup"><span data-stu-id="c6335-105">plannerPlanContextCollection resource type</span></span>

> <span data-ttu-id="c6335-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c6335-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c6335-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c6335-107">Use of these APIs in production applications is not supported.</span></span>


<span data-ttu-id="c6335-108">El recurso **plannerPlanContextCollection** representa la colección de contextos externos al que está vinculado un plan.</span><span class="sxs-lookup"><span data-stu-id="c6335-108">The **plannerPlanContextCollection** resource represents the collection of external contexts to which a plan is linked.</span></span> <span data-ttu-id="c6335-109">Este recurso es un tipo abierto y forma parte del objeto [plannerPlan](plannerplan.md) .</span><span class="sxs-lookup"><span data-stu-id="c6335-109">This resource is an open type and is part of the [plannerPlan](plannerplan.md) object.</span></span> <span data-ttu-id="c6335-110">El valor en el par de valor de la propiedad es el objeto [plannerPlanContext](plannerplancontext.md) .</span><span class="sxs-lookup"><span data-stu-id="c6335-110">The value in the property-value pair is the [plannerPlanContext](plannerplancontext.md) object.</span></span>


## <a name="properties"></a><span data-ttu-id="c6335-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c6335-111">Properties</span></span>
<span data-ttu-id="c6335-112">Puede definir las propiedades de este tipo abierto.</span><span class="sxs-lookup"><span data-stu-id="c6335-112">You can define the properties of this open type.</span></span> <span data-ttu-id="c6335-113">Los valores de propiedad deben ser distintivo identificador que representa el contexto externo como el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c6335-113">The property values should be distinctive identifier that represents the external context as the property name.</span></span> <span data-ttu-id="c6335-114">Los valores de propiedad deben ser [plannerPlanContext](plannerplancontext.md) objetos.</span><span class="sxs-lookup"><span data-stu-id="c6335-114">The property values must be [plannerPlanContext](plannerplancontext.md) objects.</span></span> <span data-ttu-id="c6335-115">En función de los requisitos de OData, nombres de propiedad de tipos abiertos no pueden contener los siguientes caracteres: `.`, `:`, `%`, `@`.</span><span class="sxs-lookup"><span data-stu-id="c6335-115">Based on OData requirements, property names in open types cannot contain the following characters: `.`, `:`, `%`, `@`.</span></span> <span data-ttu-id="c6335-116">Estos caracteres que necesite se codifican mediante la codificación de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="c6335-116">These characters need to be encoded using URL encoding.</span></span> <span data-ttu-id="c6335-117">Para quitar un elemento en la lista de favoritos, establezca el valor de la propiedad en `null`.</span><span class="sxs-lookup"><span data-stu-id="c6335-117">To remove an item in the favorites list, set the value of the property to `null`.</span></span>

## <a name="json-representation"></a><span data-ttu-id="c6335-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c6335-118">JSON representation</span></span>

<span data-ttu-id="c6335-119">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="c6335-119">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlanContextCollection"
}-->

```json
{
  "48#19%3Ad128c63941b24733951ea7defd81e550%40thread%2Eskype19%3Ad128c63941b24733951ea7defd81e550%40thread%2Eskype": {
    "@odata.type": "#microsoft.graph.plannerPlanContext",
    "associationType": "Board",
    "createdDateTime": "2015-10-14T00:57:28.4698344Z",
    "displayNameSegments": [
        "Finance Team",
        "Budget Plans"
    ],
    "ownerAppId": "5e3ce6c0-2b1f-4285-8d4b-75ee78787346"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlanContextCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
