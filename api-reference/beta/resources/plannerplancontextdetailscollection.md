---
title: tipo de recurso plannerPlanContextDetailsCollection
description: " el valor es el objeto plannerPlanContextDetails."
ms.openlocfilehash: 843be37ae0abc73de19e72c655b18834b7f5c03e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088576"
---
# <a name="plannerplancontextdetailscollection-resource-type"></a><span data-ttu-id="8d709-103">tipo de recurso plannerPlanContextDetailsCollection</span><span class="sxs-lookup"><span data-stu-id="8d709-103">plannerPlanContextDetailsCollection resource type</span></span>

> <span data-ttu-id="8d709-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8d709-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8d709-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8d709-105">Use of these APIs in production applications is not supported.</span></span>


<span data-ttu-id="8d709-106">El recurso **plannerPlanContextDetailsCollection** representa la colección de contextos externos al que está vinculado un plan.</span><span class="sxs-lookup"><span data-stu-id="8d709-106">The **plannerPlanContextDetailsCollection** resource represents the collection of external contexts to which a plan is linked.</span></span> <span data-ttu-id="8d709-107">Este recurso es un tipo abierto y forma parte del objeto [plannerPlanDetails](plannerplandetails.md) .</span><span class="sxs-lookup"><span data-stu-id="8d709-107">This resource is an open type and is part of the [plannerPlanDetails](plannerplandetails.md) object.</span></span> <span data-ttu-id="8d709-108">El nombre de la propiedad en el par de valor de la propiedad es un identificador específicas de la aplicación del contexto. el valor es el objeto [plannerPlanContextDetails](plannerplancontextdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="8d709-108">The property name in the property-value pair is an app-specific identifier of the context; the value is the [plannerPlanContextDetails](plannerplancontextdetails.md) object.</span></span>


## <a name="properties"></a><span data-ttu-id="8d709-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8d709-109">Properties</span></span>
<span data-ttu-id="8d709-110">Las propiedades de un tipo abierto pueden definirse por el cliente.</span><span class="sxs-lookup"><span data-stu-id="8d709-110">Properties of an open type can be defined by the client.</span></span> <span data-ttu-id="8d709-111">En este caso, el cliente debe utilizar un identificador distintivo que representa el contexto externo como el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8d709-111">In this case, the client should use a distinctive identifier that represents the external context as the property name.</span></span> <span data-ttu-id="8d709-112">Los valores de propiedad deben ser [plannerPlanContextDetails](plannerplancontextdetails.md) objetos.</span><span class="sxs-lookup"><span data-stu-id="8d709-112">The property values must be [plannerPlanContextDetails](plannerplancontextdetails.md) objects.</span></span> <span data-ttu-id="8d709-113">En función de OData, nombres de propiedad de tipos abiertos no pueden contener los siguientes caracteres: `.`, `:`, `@`, `%`.</span><span class="sxs-lookup"><span data-stu-id="8d709-113">Based on OData, property names in open types cannot contain the following characters: `.`, `:`, `@`, `%`.</span></span> <span data-ttu-id="8d709-114">Estos caracteres que deba estar codificado con el formato de codificación de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="8d709-114">These characters need to be encoded with URL encoding format.</span></span> <span data-ttu-id="8d709-115">Para quitar un elemento en la lista de favoritos, el valor debe quitarse de la colección [plannerPlanContextCollection](plannerplancontextcollection.md) en su lugar, que quitará automáticamente la entrada en este objeto.</span><span class="sxs-lookup"><span data-stu-id="8d709-115">To remove an item in the favorites list, the value needs to be removed from the [plannerPlanContextCollection](plannerplancontextcollection.md) collection instead, which will automatically remove the entry in this object.</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlanContextDetailsCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->