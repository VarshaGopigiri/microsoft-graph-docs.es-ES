---
title: tipo de recurso targetResourceGroup
description: 'Indica el tipo de grupo que se ven afectado debido a la actividad de auditoría. Incluye los valores como los grupos unificados frente a Azure AD '
localization_priority: Normal
ms.openlocfilehash: 2cc7e0adb1a93394b64375d05dfb6a6e349bac55
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851187"
---
# <a name="targetresourcegroup-resource-type"></a><span data-ttu-id="62574-104">tipo de recurso targetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="62574-104">targetResourceGroup resource type</span></span>
<span data-ttu-id="62574-105">Indica el tipo de grupo que se ven afectado debido a la actividad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="62574-105">Indicates the type of group that was impacted due to the audit activity.</span></span> <span data-ttu-id="62574-106">Incluye los valores como los grupos unificados frente a Azure AD</span><span class="sxs-lookup"><span data-stu-id="62574-106">Includes values like unified groups versus Azure AD</span></span> 



## <a name="properties"></a><span data-ttu-id="62574-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="62574-107">Properties</span></span>
| <span data-ttu-id="62574-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="62574-108">Property</span></span>     | <span data-ttu-id="62574-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="62574-109">Type</span></span>   |<span data-ttu-id="62574-110">Description</span><span class="sxs-lookup"><span data-stu-id="62574-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="62574-111">groupType</span><span class="sxs-lookup"><span data-stu-id="62574-111">groupType</span></span>|<span data-ttu-id="62574-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="62574-112">String</span></span>| <span data-ttu-id="62574-113">Los valores posibles son: `unifiedGroups`, `azureAD` y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="62574-113">Possible values are: `unifiedGroups`, `azureAD`, `unknownFutureValue`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="62574-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="62574-114">JSON representation</span></span>

<span data-ttu-id="62574-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="62574-115">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.targetResourceGroup"
}-->

```json
{
  "groupType": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "targetResourceGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
