---
title: tipo de recurso physicalOfficeAddress
description: Representa la dirección de la empresa de un recurso, como un contacto o un evento.
localization_priority: Normal
ms.openlocfilehash: bd4274e29b2ef0f9e7e8318528d18103be19fabc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817790"
---
# <a name="physicalofficeaddress-resource-type"></a><span data-ttu-id="f49bd-103">tipo de recurso physicalOfficeAddress</span><span class="sxs-lookup"><span data-stu-id="f49bd-103">physicalOfficeAddress resource type</span></span>

<span data-ttu-id="f49bd-104">Representa la dirección de la empresa de un recurso, como un contacto de la organización.</span><span class="sxs-lookup"><span data-stu-id="f49bd-104">Represents the business address of a resource such as an organizational contact.</span></span>

## <a name="properties"></a><span data-ttu-id="f49bd-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f49bd-105">Properties</span></span>

| <span data-ttu-id="f49bd-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f49bd-106">Property</span></span>     | <span data-ttu-id="f49bd-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f49bd-107">Type</span></span>   |<span data-ttu-id="f49bd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f49bd-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f49bd-109">city</span><span class="sxs-lookup"><span data-stu-id="f49bd-109">city</span></span>|<span data-ttu-id="f49bd-110">String</span><span class="sxs-lookup"><span data-stu-id="f49bd-110">String</span></span>|<span data-ttu-id="f49bd-111">Ciudad.</span><span class="sxs-lookup"><span data-stu-id="f49bd-111">The city.</span></span>|
|<span data-ttu-id="f49bd-112">countryOrRegion</span><span class="sxs-lookup"><span data-stu-id="f49bd-112">countryOrRegion</span></span>|<span data-ttu-id="f49bd-113">String</span><span class="sxs-lookup"><span data-stu-id="f49bd-113">String</span></span>|<span data-ttu-id="f49bd-p101">País o región. Se trata de un valor de cadena de formato libre, por ejemplo, "Estados Unidos".</span><span class="sxs-lookup"><span data-stu-id="f49bd-p101">The country or region. It's a free-format string value, for example, "United States".</span></span>|
|<span data-ttu-id="f49bd-116">officeLocation</span><span class="sxs-lookup"><span data-stu-id="f49bd-116">officeLocation</span></span>  | <span data-ttu-id="f49bd-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="f49bd-117">String</span></span> | <span data-ttu-id="f49bd-118">Ubicación de la oficina como el número de generación de cubos y office para un contacto de la organización.</span><span class="sxs-lookup"><span data-stu-id="f49bd-118">Office location such as building and office number for an organizational contact.</span></span>  |
|<span data-ttu-id="f49bd-119">postalCode</span><span class="sxs-lookup"><span data-stu-id="f49bd-119">postalCode</span></span>|<span data-ttu-id="f49bd-120">String</span><span class="sxs-lookup"><span data-stu-id="f49bd-120">String</span></span>|<span data-ttu-id="f49bd-121">Código postal.</span><span class="sxs-lookup"><span data-stu-id="f49bd-121">The postal code.</span></span>|
|<span data-ttu-id="f49bd-122">state</span><span class="sxs-lookup"><span data-stu-id="f49bd-122">state</span></span>|<span data-ttu-id="f49bd-123">String</span><span class="sxs-lookup"><span data-stu-id="f49bd-123">String</span></span>|<span data-ttu-id="f49bd-124">Estado.</span><span class="sxs-lookup"><span data-stu-id="f49bd-124">The state.</span></span>|
|<span data-ttu-id="f49bd-125">street</span><span class="sxs-lookup"><span data-stu-id="f49bd-125">street</span></span>|<span data-ttu-id="f49bd-126">String</span><span class="sxs-lookup"><span data-stu-id="f49bd-126">String</span></span>|<span data-ttu-id="f49bd-127">Calle.</span><span class="sxs-lookup"><span data-stu-id="f49bd-127">The street.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f49bd-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f49bd-128">JSON representation</span></span>

<span data-ttu-id="f49bd-129">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f49bd-129">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.physicalOfficeAddress"
}-->

```json
{
  "city": "string",
  "countryOrRegion": "string",
  "officeLocation": "string",
  "postalCode": "string",
  "state": "string",
  "street": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "physicalOfficeAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
