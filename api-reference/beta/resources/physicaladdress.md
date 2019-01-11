---
title: Tipo de recurso physicalAddress
description: Representa la dirección postal de un recurso, como un contacto o un evento.
localization_priority: Normal
ms.openlocfilehash: 3a656046cc23394fc8cff9100eb5ad2289050b25
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823586"
---
# <a name="physicaladdress-resource-type"></a><span data-ttu-id="1ca79-103">Tipo de recurso physicalAddress</span><span class="sxs-lookup"><span data-stu-id="1ca79-103">physicalAddress resource type</span></span>

<span data-ttu-id="1ca79-104">Representa la dirección postal de un recurso, como un contacto o un evento.</span><span class="sxs-lookup"><span data-stu-id="1ca79-104">Represents the street address of a resource such as a contact or event.</span></span>


## <a name="properties"></a><span data-ttu-id="1ca79-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1ca79-105">Properties</span></span>
| <span data-ttu-id="1ca79-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1ca79-106">Property</span></span>     | <span data-ttu-id="1ca79-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="1ca79-107">Type</span></span>   |<span data-ttu-id="1ca79-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ca79-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1ca79-109">type</span><span class="sxs-lookup"><span data-stu-id="1ca79-109">type</span></span>|<span data-ttu-id="1ca79-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="1ca79-110">String</span></span>|<span data-ttu-id="1ca79-111">El tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="1ca79-111">The type of address.</span></span> <span data-ttu-id="1ca79-112">Los valores posibles son: `unknown`, `home`, `business` y `other`.</span><span class="sxs-lookup"><span data-stu-id="1ca79-112">Possible values are: `unknown`, `home`, `business`, `other`.</span></span>|
|<span data-ttu-id="1ca79-113">postOfficeBox</span><span class="sxs-lookup"><span data-stu-id="1ca79-113">postOfficeBox</span></span>|<span data-ttu-id="1ca79-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="1ca79-114">String</span></span>|<span data-ttu-id="1ca79-115">El número de apartado de correos.</span><span class="sxs-lookup"><span data-stu-id="1ca79-115">The post office box number.</span></span>|
|<span data-ttu-id="1ca79-116">ciudad</span><span class="sxs-lookup"><span data-stu-id="1ca79-116">city</span></span>|<span data-ttu-id="1ca79-117">String</span><span class="sxs-lookup"><span data-stu-id="1ca79-117">String</span></span>|<span data-ttu-id="1ca79-118">Ciudad.</span><span class="sxs-lookup"><span data-stu-id="1ca79-118">The city.</span></span>|
|<span data-ttu-id="1ca79-119">countryOrRegion</span><span class="sxs-lookup"><span data-stu-id="1ca79-119">countryOrRegion</span></span>|<span data-ttu-id="1ca79-120">String</span><span class="sxs-lookup"><span data-stu-id="1ca79-120">String</span></span>|<span data-ttu-id="1ca79-p102">País o región. Se trata de un valor de cadena de formato libre, por ejemplo, "Estados Unidos".</span><span class="sxs-lookup"><span data-stu-id="1ca79-p102">The country or region. It's a free-format string value, for example, "United States".</span></span>|
|<span data-ttu-id="1ca79-123">postalCode</span><span class="sxs-lookup"><span data-stu-id="1ca79-123">postalCode</span></span>|<span data-ttu-id="1ca79-124">String</span><span class="sxs-lookup"><span data-stu-id="1ca79-124">String</span></span>|<span data-ttu-id="1ca79-125">Código postal.</span><span class="sxs-lookup"><span data-stu-id="1ca79-125">The postal code.</span></span>|
|<span data-ttu-id="1ca79-126">state</span><span class="sxs-lookup"><span data-stu-id="1ca79-126">state</span></span>|<span data-ttu-id="1ca79-127">String</span><span class="sxs-lookup"><span data-stu-id="1ca79-127">String</span></span>|<span data-ttu-id="1ca79-128">Estado.</span><span class="sxs-lookup"><span data-stu-id="1ca79-128">The state.</span></span>|
|<span data-ttu-id="1ca79-129">street</span><span class="sxs-lookup"><span data-stu-id="1ca79-129">street</span></span>|<span data-ttu-id="1ca79-130">String</span><span class="sxs-lookup"><span data-stu-id="1ca79-130">String</span></span>|<span data-ttu-id="1ca79-131">Calle.</span><span class="sxs-lookup"><span data-stu-id="1ca79-131">The street.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1ca79-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1ca79-132">JSON representation</span></span>

<span data-ttu-id="1ca79-133">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="1ca79-133">Here is a JSON representation of the resource</span></span>

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
