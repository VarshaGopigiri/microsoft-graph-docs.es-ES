---
title: tipo de recurso targetResourcePolicy
description: 'Indica la directiva que se ven afectada por la actividad de auditoría. Deriva el recurso targetResource.   '
localization_priority: Normal
ms.openlocfilehash: 355e6ac11741a2aa7aeb780bdac4b7be373092af
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27813142"
---
# <a name="targetresourcepolicy-resource-type"></a><span data-ttu-id="3982e-104">tipo de recurso targetResourcePolicy</span><span class="sxs-lookup"><span data-stu-id="3982e-104">targetResourcePolicy resource type</span></span>
<span data-ttu-id="3982e-105">Indica la directiva que se ven afectada por la actividad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="3982e-105">Indicates the policy that was impacted by the audit activity.</span></span> <span data-ttu-id="3982e-106">Deriva el recurso [targetResource](targetresource.md) .</span><span class="sxs-lookup"><span data-stu-id="3982e-106">Derived from the [targetResource](targetresource.md) resource.</span></span>   



## <a name="properties"></a><span data-ttu-id="3982e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3982e-107">Properties</span></span>
| <span data-ttu-id="3982e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3982e-108">Property</span></span>     | <span data-ttu-id="3982e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3982e-109">Type</span></span>   |<span data-ttu-id="3982e-110">Description</span><span class="sxs-lookup"><span data-stu-id="3982e-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3982e-111">policyType</span><span class="sxs-lookup"><span data-stu-id="3982e-111">policyType</span></span>|<span data-ttu-id="3982e-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="3982e-112">String</span></span>|<span data-ttu-id="3982e-113">Indica el nombre de directiva que ha cambiado o se ha diseñado para cambiar</span><span class="sxs-lookup"><span data-stu-id="3982e-113">Indicates the Policy Name that changed or was targetted for change</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3982e-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3982e-114">JSON representation</span></span>

<span data-ttu-id="3982e-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3982e-115">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.targetResourcePolicy"
}-->

```json
{
  "policyType": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "targetResourcePolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
