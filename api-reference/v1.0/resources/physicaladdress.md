---
title: Tipo de recurso physicalAddress
description: Representa la dirección postal de un recurso, como un contacto o un evento.
localization_priority: Normal
ms.openlocfilehash: 2bbfc3f38d4d353d370b9c8ba859b06cc2e4398b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866013"
---
# <a name="physicaladdress-resource-type"></a><span data-ttu-id="d0daa-103">Tipo de recurso physicalAddress</span><span class="sxs-lookup"><span data-stu-id="d0daa-103">physicalAddress resource type</span></span>

<span data-ttu-id="d0daa-104">Representa la dirección postal de un recurso, como un contacto o un evento.</span><span class="sxs-lookup"><span data-stu-id="d0daa-104">Represents the street address of a resource such as a contact or event.</span></span>


## <a name="properties"></a><span data-ttu-id="d0daa-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0daa-105">Properties</span></span>
| <span data-ttu-id="d0daa-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0daa-106">Property</span></span>     | <span data-ttu-id="d0daa-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0daa-107">Type</span></span>   |<span data-ttu-id="d0daa-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0daa-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d0daa-109">city</span><span class="sxs-lookup"><span data-stu-id="d0daa-109">city</span></span>|<span data-ttu-id="d0daa-110">String</span><span class="sxs-lookup"><span data-stu-id="d0daa-110">String</span></span>|<span data-ttu-id="d0daa-111">Ciudad.</span><span class="sxs-lookup"><span data-stu-id="d0daa-111">The city.</span></span>|
|<span data-ttu-id="d0daa-112">countryOrRegion</span><span class="sxs-lookup"><span data-stu-id="d0daa-112">countryOrRegion</span></span>|<span data-ttu-id="d0daa-113">String</span><span class="sxs-lookup"><span data-stu-id="d0daa-113">String</span></span>|<span data-ttu-id="d0daa-p101">País o región. Se trata de un valor de cadena de formato libre, por ejemplo, "Estados Unidos".</span><span class="sxs-lookup"><span data-stu-id="d0daa-p101">The country or region. It's a free-format string value, for example, "United States".</span></span>|
|<span data-ttu-id="d0daa-116">postalCode</span><span class="sxs-lookup"><span data-stu-id="d0daa-116">postalCode</span></span>|<span data-ttu-id="d0daa-117">String</span><span class="sxs-lookup"><span data-stu-id="d0daa-117">String</span></span>|<span data-ttu-id="d0daa-118">Código postal.</span><span class="sxs-lookup"><span data-stu-id="d0daa-118">The postal code.</span></span>|
|<span data-ttu-id="d0daa-119">state</span><span class="sxs-lookup"><span data-stu-id="d0daa-119">state</span></span>|<span data-ttu-id="d0daa-120">String</span><span class="sxs-lookup"><span data-stu-id="d0daa-120">String</span></span>|<span data-ttu-id="d0daa-121">Estado.</span><span class="sxs-lookup"><span data-stu-id="d0daa-121">The state.</span></span>|
|<span data-ttu-id="d0daa-122">street</span><span class="sxs-lookup"><span data-stu-id="d0daa-122">street</span></span>|<span data-ttu-id="d0daa-123">String</span><span class="sxs-lookup"><span data-stu-id="d0daa-123">String</span></span>|<span data-ttu-id="d0daa-124">Calle.</span><span class="sxs-lookup"><span data-stu-id="d0daa-124">The street.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d0daa-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d0daa-125">JSON representation</span></span>

<span data-ttu-id="d0daa-126">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d0daa-126">Here is a JSON representation of the resource</span></span>

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
