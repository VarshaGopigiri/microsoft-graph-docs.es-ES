---
title: tipo de recurso physicalOfficeAddress
description: Representa la dirección de la empresa de un recurso, como un contacto o un evento.
ms.openlocfilehash: 472e4dfd03670f5fd4ff6b5c5c53342fff5c391a
ms.sourcegitcommit: f3d479edf03935d0edbbc7668a65f7cde2a56c92
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/15/2018
ms.locfileid: "27284101"
---
# <a name="physicalofficeaddress-resource-type"></a><span data-ttu-id="20c09-103">tipo de recurso physicalOfficeAddress</span><span class="sxs-lookup"><span data-stu-id="20c09-103">physicalOfficeAddress resource type</span></span>

<span data-ttu-id="20c09-104">Representa la dirección de la empresa de un recurso, como un contacto de la organización.</span><span class="sxs-lookup"><span data-stu-id="20c09-104">Represents the business address of a resource such as an organizational contact.</span></span>

## <a name="properties"></a><span data-ttu-id="20c09-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20c09-105">Properties</span></span>

| <span data-ttu-id="20c09-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="20c09-106">Property</span></span>     | <span data-ttu-id="20c09-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="20c09-107">Type</span></span>   |<span data-ttu-id="20c09-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="20c09-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="20c09-109">city</span><span class="sxs-lookup"><span data-stu-id="20c09-109">city</span></span>|<span data-ttu-id="20c09-110">String</span><span class="sxs-lookup"><span data-stu-id="20c09-110">String</span></span>|<span data-ttu-id="20c09-111">Ciudad.</span><span class="sxs-lookup"><span data-stu-id="20c09-111">The city.</span></span>|
|<span data-ttu-id="20c09-112">countryOrRegion</span><span class="sxs-lookup"><span data-stu-id="20c09-112">countryOrRegion</span></span>|<span data-ttu-id="20c09-113">String</span><span class="sxs-lookup"><span data-stu-id="20c09-113">String</span></span>|<span data-ttu-id="20c09-p101">País o región. Se trata de un valor de cadena de formato libre, por ejemplo, "Estados Unidos".</span><span class="sxs-lookup"><span data-stu-id="20c09-p101">The country or region. It's a free-format string value, for example, "United States".</span></span>|
|<span data-ttu-id="20c09-116">officeLocation</span><span class="sxs-lookup"><span data-stu-id="20c09-116">officeLocation</span></span>  | <span data-ttu-id="20c09-117">String</span><span class="sxs-lookup"><span data-stu-id="20c09-117">String</span></span> | <span data-ttu-id="20c09-118">Ubicación de la oficina como el número de generación de cubos y office para un contacto de la organización.</span><span class="sxs-lookup"><span data-stu-id="20c09-118">Office location such as building and office number for an organizational contact.</span></span>  |
|<span data-ttu-id="20c09-119">postalCode</span><span class="sxs-lookup"><span data-stu-id="20c09-119">postalCode</span></span>|<span data-ttu-id="20c09-120">String</span><span class="sxs-lookup"><span data-stu-id="20c09-120">String</span></span>|<span data-ttu-id="20c09-121">Código postal.</span><span class="sxs-lookup"><span data-stu-id="20c09-121">The postal code.</span></span>|
|<span data-ttu-id="20c09-122">state</span><span class="sxs-lookup"><span data-stu-id="20c09-122">state</span></span>|<span data-ttu-id="20c09-123">String</span><span class="sxs-lookup"><span data-stu-id="20c09-123">String</span></span>|<span data-ttu-id="20c09-124">Estado.</span><span class="sxs-lookup"><span data-stu-id="20c09-124">The state.</span></span>|
|<span data-ttu-id="20c09-125">street</span><span class="sxs-lookup"><span data-stu-id="20c09-125">street</span></span>|<span data-ttu-id="20c09-126">String</span><span class="sxs-lookup"><span data-stu-id="20c09-126">String</span></span>|<span data-ttu-id="20c09-127">Calle.</span><span class="sxs-lookup"><span data-stu-id="20c09-127">The street.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="20c09-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="20c09-128">JSON representation</span></span>

<span data-ttu-id="20c09-129">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="20c09-129">Here is a JSON representation of the resource</span></span>

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
