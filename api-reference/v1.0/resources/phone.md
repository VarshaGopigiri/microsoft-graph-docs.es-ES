---
title: Tipo de recurso phone
description: Representa un número de teléfono.
ms.openlocfilehash: 1293b1f84d9e73f5d92c9b6f6b078b5f39126e33
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031579"
---
# <a name="phone-resource-type"></a><span data-ttu-id="dc2b6-103">Tipo de recurso phone</span><span class="sxs-lookup"><span data-stu-id="dc2b6-103">phone resource type</span></span>

<span data-ttu-id="dc2b6-104">Representa un número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="dc2b6-104">Represents a phone number.</span></span>


## <a name="properties"></a><span data-ttu-id="dc2b6-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc2b6-105">Properties</span></span>
| <span data-ttu-id="dc2b6-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dc2b6-106">Property</span></span>     | <span data-ttu-id="dc2b6-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc2b6-107">Type</span></span>   |<span data-ttu-id="dc2b6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc2b6-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dc2b6-109">number</span><span class="sxs-lookup"><span data-stu-id="dc2b6-109">number</span></span>|<span data-ttu-id="dc2b6-110">string</span><span class="sxs-lookup"><span data-stu-id="dc2b6-110">string</span></span>|<span data-ttu-id="dc2b6-111">El número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="dc2b6-111">The phone number.</span></span>|
|<span data-ttu-id="dc2b6-112">type</span><span class="sxs-lookup"><span data-stu-id="dc2b6-112">type</span></span>|<span data-ttu-id="dc2b6-113">phoneType</span><span class="sxs-lookup"><span data-stu-id="dc2b6-113">phoneType</span></span>|<span data-ttu-id="dc2b6-114">El tipo de número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="dc2b6-114">The type of phone number.</span></span> <span data-ttu-id="dc2b6-115">Los valores posibles son: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span><span class="sxs-lookup"><span data-stu-id="dc2b6-115">The possible values are: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="dc2b6-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dc2b6-116">JSON representation</span></span>

<span data-ttu-id="dc2b6-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="dc2b6-117">Here is a JSON representation of the resource.</span></span>

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
