---
title: Tipo de recurso phone
description: Representa un número de teléfono.
localization_priority: Normal
ms.openlocfilehash: 6c34033b0895f81619589e7500441fc655842995
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805064"
---
# <a name="phone-resource-type"></a><span data-ttu-id="92a72-103">Tipo de recurso phone</span><span class="sxs-lookup"><span data-stu-id="92a72-103">phone resource type</span></span>

<span data-ttu-id="92a72-104">Representa un número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="92a72-104">Represents a phone number.</span></span>


## <a name="properties"></a><span data-ttu-id="92a72-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="92a72-105">Properties</span></span>
| <span data-ttu-id="92a72-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="92a72-106">Property</span></span>     | <span data-ttu-id="92a72-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="92a72-107">Type</span></span>   |<span data-ttu-id="92a72-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="92a72-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="92a72-109">number</span><span class="sxs-lookup"><span data-stu-id="92a72-109">number</span></span>|<span data-ttu-id="92a72-110">string</span><span class="sxs-lookup"><span data-stu-id="92a72-110">string</span></span>|<span data-ttu-id="92a72-111">El número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="92a72-111">The phone number.</span></span>|
|<span data-ttu-id="92a72-112">type</span><span class="sxs-lookup"><span data-stu-id="92a72-112">type</span></span>|<span data-ttu-id="92a72-113">phoneType</span><span class="sxs-lookup"><span data-stu-id="92a72-113">phoneType</span></span>|<span data-ttu-id="92a72-114">El tipo de número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="92a72-114">The type of phone number.</span></span> <span data-ttu-id="92a72-115">Los valores posibles son: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span><span class="sxs-lookup"><span data-stu-id="92a72-115">The possible values are: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="92a72-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="92a72-116">JSON representation</span></span>

<span data-ttu-id="92a72-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="92a72-117">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.phone"
}-->

```json
{
  "number": "string",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "phone resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
