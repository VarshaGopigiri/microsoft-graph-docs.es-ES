---
title: Tipo de recurso physicalAddress
description: Representa la dirección postal de un recurso, como un contacto o un evento.
ms.openlocfilehash: eb2c1ea6a73d7f6eb5d3d43b877f50dc39a2b17e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030473"
---
# <a name="physicaladdress-resource-type"></a><span data-ttu-id="a1b78-103">Tipo de recurso physicalAddress</span><span class="sxs-lookup"><span data-stu-id="a1b78-103">physicalAddress resource type</span></span>

<span data-ttu-id="a1b78-104">Representa la dirección postal de un recurso, como un contacto o un evento.</span><span class="sxs-lookup"><span data-stu-id="a1b78-104">Represents the street address of a resource such as a contact or event.</span></span>


## <a name="properties"></a><span data-ttu-id="a1b78-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1b78-105">Properties</span></span>
| <span data-ttu-id="a1b78-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a1b78-106">Property</span></span>     | <span data-ttu-id="a1b78-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1b78-107">Type</span></span>   |<span data-ttu-id="a1b78-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1b78-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a1b78-109">city</span><span class="sxs-lookup"><span data-stu-id="a1b78-109">city</span></span>|<span data-ttu-id="a1b78-110">String</span><span class="sxs-lookup"><span data-stu-id="a1b78-110">String</span></span>|<span data-ttu-id="a1b78-111">Ciudad.</span><span class="sxs-lookup"><span data-stu-id="a1b78-111">The city.</span></span>|
|<span data-ttu-id="a1b78-112">countryOrRegion</span><span class="sxs-lookup"><span data-stu-id="a1b78-112">countryOrRegion</span></span>|<span data-ttu-id="a1b78-113">String</span><span class="sxs-lookup"><span data-stu-id="a1b78-113">String</span></span>|<span data-ttu-id="a1b78-p101">País o región. Se trata de un valor de cadena de formato libre, por ejemplo, "Estados Unidos".</span><span class="sxs-lookup"><span data-stu-id="a1b78-p101">The country or region. It's a free-format string value, for example, "United States".</span></span>|
|<span data-ttu-id="a1b78-116">postalCode</span><span class="sxs-lookup"><span data-stu-id="a1b78-116">postalCode</span></span>|<span data-ttu-id="a1b78-117">String</span><span class="sxs-lookup"><span data-stu-id="a1b78-117">String</span></span>|<span data-ttu-id="a1b78-118">Código postal.</span><span class="sxs-lookup"><span data-stu-id="a1b78-118">The postal code.</span></span>|
|<span data-ttu-id="a1b78-119">state</span><span class="sxs-lookup"><span data-stu-id="a1b78-119">state</span></span>|<span data-ttu-id="a1b78-120">String</span><span class="sxs-lookup"><span data-stu-id="a1b78-120">String</span></span>|<span data-ttu-id="a1b78-121">Estado.</span><span class="sxs-lookup"><span data-stu-id="a1b78-121">The state.</span></span>|
|<span data-ttu-id="a1b78-122">street</span><span class="sxs-lookup"><span data-stu-id="a1b78-122">street</span></span>|<span data-ttu-id="a1b78-123">String</span><span class="sxs-lookup"><span data-stu-id="a1b78-123">String</span></span>|<span data-ttu-id="a1b78-124">Calle.</span><span class="sxs-lookup"><span data-stu-id="a1b78-124">The street.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a1b78-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a1b78-125">JSON representation</span></span>

<span data-ttu-id="a1b78-126">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a1b78-126">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.physicalAddress"
}-->

```json
{
  "city": "string",
  "countryOrRegion": "string",
  "postalCode": "string",
  "state": "string",
  "street": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "physicalAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
