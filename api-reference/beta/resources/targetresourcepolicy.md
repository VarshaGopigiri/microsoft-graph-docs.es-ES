---
title: tipo de recurso targetResourcePolicy
description: 'Indica la directiva que se ven afectada por la actividad de auditoría. Deriva el recurso targetResource.   '
ms.openlocfilehash: 20486c535d0df4b3745f5cfc3414b320a9374075
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088424"
---
# <a name="targetresourcepolicy-resource-type"></a><span data-ttu-id="f4059-104">tipo de recurso targetResourcePolicy</span><span class="sxs-lookup"><span data-stu-id="f4059-104">targetResourcePolicy resource type</span></span>
<span data-ttu-id="f4059-105">Indica la directiva que se ven afectada por la actividad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="f4059-105">Indicates the policy that was impacted by the audit activity.</span></span> <span data-ttu-id="f4059-106">Deriva el recurso [targetResource](targetresource.md) .</span><span class="sxs-lookup"><span data-stu-id="f4059-106">Derived from the [targetResource](targetresource.md) resource.</span></span>   



## <a name="properties"></a><span data-ttu-id="f4059-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4059-107">Properties</span></span>
| <span data-ttu-id="f4059-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f4059-108">Property</span></span>     | <span data-ttu-id="f4059-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4059-109">Type</span></span>   |<span data-ttu-id="f4059-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4059-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f4059-111">policyType</span><span class="sxs-lookup"><span data-stu-id="f4059-111">policyType</span></span>|<span data-ttu-id="f4059-112">String</span><span class="sxs-lookup"><span data-stu-id="f4059-112">String</span></span>|<span data-ttu-id="f4059-113">Indica el nombre de directiva que ha cambiado o se ha diseñado para cambiar</span><span class="sxs-lookup"><span data-stu-id="f4059-113">Indicates the Policy Name that changed or was targetted for change</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f4059-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f4059-114">JSON representation</span></span>

<span data-ttu-id="f4059-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f4059-115">Here is a JSON representation of the resource.</span></span>

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