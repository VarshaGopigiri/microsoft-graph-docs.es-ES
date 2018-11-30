---
title: Tipo de recurso physicalAddress
description: Representa la dirección postal de un recurso, como un contacto o un evento.
ms.openlocfilehash: 819240be3eb9a088fde43390fbb1d1d4af1fd30c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089743"
---
# <a name="physicaladdress-resource-type"></a><span data-ttu-id="4b3e9-103">Tipo de recurso physicalAddress</span><span class="sxs-lookup"><span data-stu-id="4b3e9-103">physicalAddress resource type</span></span>

<span data-ttu-id="4b3e9-104">Representa la dirección postal de un recurso, como un contacto o un evento.</span><span class="sxs-lookup"><span data-stu-id="4b3e9-104">Represents the street address of a resource such as a contact or event.</span></span>


## <a name="properties"></a><span data-ttu-id="4b3e9-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4b3e9-105">Properties</span></span>
| <span data-ttu-id="4b3e9-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4b3e9-106">Property</span></span>     | <span data-ttu-id="4b3e9-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b3e9-107">Type</span></span>   |<span data-ttu-id="4b3e9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b3e9-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4b3e9-109">type</span><span class="sxs-lookup"><span data-stu-id="4b3e9-109">type</span></span>|<span data-ttu-id="4b3e9-110">String</span><span class="sxs-lookup"><span data-stu-id="4b3e9-110">String</span></span>|<span data-ttu-id="4b3e9-111">El tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="4b3e9-111">The type of address.</span></span> <span data-ttu-id="4b3e9-112">Los valores posibles son: `unknown`, `home`, `business` y `other`.</span><span class="sxs-lookup"><span data-stu-id="4b3e9-112">Possible values are: `unknown`, `home`, `business`, `other`.</span></span>|
|<span data-ttu-id="4b3e9-113">postOfficeBox</span><span class="sxs-lookup"><span data-stu-id="4b3e9-113">postOfficeBox</span></span>|<span data-ttu-id="4b3e9-114">String</span><span class="sxs-lookup"><span data-stu-id="4b3e9-114">String</span></span>|<span data-ttu-id="4b3e9-115">El número de apartado de correos.</span><span class="sxs-lookup"><span data-stu-id="4b3e9-115">The post office box number.</span></span>|
|<span data-ttu-id="4b3e9-116">ciudad</span><span class="sxs-lookup"><span data-stu-id="4b3e9-116">city</span></span>|<span data-ttu-id="4b3e9-117">String</span><span class="sxs-lookup"><span data-stu-id="4b3e9-117">String</span></span>|<span data-ttu-id="4b3e9-118">Ciudad.</span><span class="sxs-lookup"><span data-stu-id="4b3e9-118">The city.</span></span>|
|<span data-ttu-id="4b3e9-119">countryOrRegion</span><span class="sxs-lookup"><span data-stu-id="4b3e9-119">countryOrRegion</span></span>|<span data-ttu-id="4b3e9-120">String</span><span class="sxs-lookup"><span data-stu-id="4b3e9-120">String</span></span>|<span data-ttu-id="4b3e9-p102">País o región. Se trata de un valor de cadena de formato libre, por ejemplo, "Estados Unidos".</span><span class="sxs-lookup"><span data-stu-id="4b3e9-p102">The country or region. It's a free-format string value, for example, "United States".</span></span>|
|<span data-ttu-id="4b3e9-123">postalCode</span><span class="sxs-lookup"><span data-stu-id="4b3e9-123">postalCode</span></span>|<span data-ttu-id="4b3e9-124">String</span><span class="sxs-lookup"><span data-stu-id="4b3e9-124">String</span></span>|<span data-ttu-id="4b3e9-125">Código postal.</span><span class="sxs-lookup"><span data-stu-id="4b3e9-125">The postal code.</span></span>|
|<span data-ttu-id="4b3e9-126">state</span><span class="sxs-lookup"><span data-stu-id="4b3e9-126">state</span></span>|<span data-ttu-id="4b3e9-127">String</span><span class="sxs-lookup"><span data-stu-id="4b3e9-127">String</span></span>|<span data-ttu-id="4b3e9-128">Estado.</span><span class="sxs-lookup"><span data-stu-id="4b3e9-128">The state.</span></span>|
|<span data-ttu-id="4b3e9-129">street</span><span class="sxs-lookup"><span data-stu-id="4b3e9-129">street</span></span>|<span data-ttu-id="4b3e9-130">String</span><span class="sxs-lookup"><span data-stu-id="4b3e9-130">String</span></span>|<span data-ttu-id="4b3e9-131">Calle.</span><span class="sxs-lookup"><span data-stu-id="4b3e9-131">The street.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4b3e9-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4b3e9-132">JSON representation</span></span>

<span data-ttu-id="4b3e9-133">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4b3e9-133">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.physicalAddress"
}-->

```json
{
  "type": "string",
  "postOfficeBox": "string",
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
