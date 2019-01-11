---
title: tipo de recurso targetResourceServicePrincipal
description: Indica la ServicePrincipalId para el recurso que resulta afectada la actividad de auditoría. Deriva el recurso targetResource.
localization_priority: Normal
ms.openlocfilehash: 37bd63851ca9169afb669c710ef4cb2c150ea615
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839602"
---
# <a name="targetresourceserviceprincipal-resource-type"></a><span data-ttu-id="41051-104">tipo de recurso targetResourceServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="41051-104">targetResourceServicePrincipal resource type</span></span>
<span data-ttu-id="41051-105">Indica la ServicePrincipalId para el recurso que resulta afectada la actividad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="41051-105">Indicates the ServicePrincipalId for the resource that impacted the audit activity.</span></span> <span data-ttu-id="41051-106">Deriva el recurso [targetResource](targetresource.md) .</span><span class="sxs-lookup"><span data-stu-id="41051-106">Derived from the [targetResource](targetresource.md) resource.</span></span>



## <a name="properties"></a><span data-ttu-id="41051-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41051-107">Properties</span></span>
| <span data-ttu-id="41051-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="41051-108">Property</span></span>     | <span data-ttu-id="41051-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="41051-109">Type</span></span>   |<span data-ttu-id="41051-110">Description</span><span class="sxs-lookup"><span data-stu-id="41051-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="41051-111">appId</span><span class="sxs-lookup"><span data-stu-id="41051-111">appId</span></span>|<span data-ttu-id="41051-112">cadena</span><span class="sxs-lookup"><span data-stu-id="41051-112">String</span></span>|<span data-ttu-id="41051-113">Indica el identificador único de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41051-113">Indicates the Unique Id of the application.</span></span> <span data-ttu-id="41051-114">Hace referencia al identificador de la aplicación para una aplicación de específico.</span><span class="sxs-lookup"><span data-stu-id="41051-114">Refers to App Id for a specfic app.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="41051-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="41051-115">JSON representation</span></span>

<span data-ttu-id="41051-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="41051-116">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.targetResourceServicePrincipal"
}-->

```json
{
  "appId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "targetResourceServicePrincipal resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
