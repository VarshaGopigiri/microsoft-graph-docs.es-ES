---
title: tipo de recurso bookingCurrency
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 7e2289bfa6c6aac62f12d7321d06caaafbc41f8c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956006"
---
# <a name="bookingcurrency-resource-type"></a><span data-ttu-id="e7bed-104">tipo de recurso bookingCurrency</span><span class="sxs-lookup"><span data-stu-id="e7bed-104">bookingCurrency resource type</span></span>

 > <span data-ttu-id="e7bed-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e7bed-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e7bed-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e7bed-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="e7bed-107">Representa una moneda monetaria compatible con un [bookingBusiness](bookingbusiness.md).</span><span class="sxs-lookup"><span data-stu-id="e7bed-107">Represents a monetary currency supported by a [bookingBusiness](bookingbusiness.md).</span></span>


## <a name="methods"></a><span data-ttu-id="e7bed-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e7bed-108">Methods</span></span>

| <span data-ttu-id="e7bed-109">Método</span><span class="sxs-lookup"><span data-stu-id="e7bed-109">Method</span></span>           | <span data-ttu-id="e7bed-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7bed-110">Return Type</span></span>    |<span data-ttu-id="e7bed-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7bed-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e7bed-112">Lista bookingCurrencies</span><span class="sxs-lookup"><span data-stu-id="e7bed-112">List bookingCurrencies</span></span>](../api/bookingcurrency-list.md) | <span data-ttu-id="e7bed-113">colección de [bookingCurrency](bookingcurrency.md)</span><span class="sxs-lookup"><span data-stu-id="e7bed-113">[bookingCurrency](bookingcurrency.md) collection</span></span> |<span data-ttu-id="e7bed-114">Obtener una lista de objetos de **bookingCurrency** disponibles para una empresa de Microsoft Bookings.</span><span class="sxs-lookup"><span data-stu-id="e7bed-114">Get a list of **bookingCurrency** objects available to a Microsoft Bookings business.</span></span>|
|[<span data-ttu-id="e7bed-115">Obtener bookingCurrency</span><span class="sxs-lookup"><span data-stu-id="e7bed-115">Get bookingCurrency</span></span>](../api/bookingcurrency-get.md) | [<span data-ttu-id="e7bed-116">bookingCurrency</span><span class="sxs-lookup"><span data-stu-id="e7bed-116">bookingCurrency</span></span>](bookingcurrency.md) |<span data-ttu-id="e7bed-117">Obtener las propiedades de un objeto **bookingCurrency** .</span><span class="sxs-lookup"><span data-stu-id="e7bed-117">Get the properties of a **bookingCurrency** object.</span></span>|


## <a name="properties"></a><span data-ttu-id="e7bed-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7bed-118">Properties</span></span>
| <span data-ttu-id="e7bed-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7bed-119">Property</span></span>     | <span data-ttu-id="e7bed-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7bed-120">Type</span></span>   |<span data-ttu-id="e7bed-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7bed-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e7bed-122">id</span><span class="sxs-lookup"><span data-stu-id="e7bed-122">id</span></span>|<span data-ttu-id="e7bed-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="e7bed-123">String</span></span>| <span data-ttu-id="e7bed-124">Un código de moneda de 3 caracteres, basado en [ISO 4217](https://www.iso.org/iso-4217-currency-codes.html).</span><span class="sxs-lookup"><span data-stu-id="e7bed-124">A 3-character currency code, based on [ISO 4217](https://www.iso.org/iso-4217-currency-codes.html).</span></span> <span data-ttu-id="e7bed-125">Por ejemplo, el código de moneda para el dólar estadounidense es USD, y para el Dólar australiano es AUD.</span><span class="sxs-lookup"><span data-stu-id="e7bed-125">For example, the currency code for the US dollar is USD, and for the Australian dollar is AUD.</span></span> <span data-ttu-id="e7bed-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e7bed-126">Read-only.</span></span>|
|<span data-ttu-id="e7bed-127">símbolo</span><span class="sxs-lookup"><span data-stu-id="e7bed-127">symbol</span></span>|<span data-ttu-id="e7bed-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="e7bed-128">String</span></span>| <span data-ttu-id="e7bed-129">El símbolo de moneda.</span><span class="sxs-lookup"><span data-stu-id="e7bed-129">The currency symbol.</span></span> <span data-ttu-id="e7bed-130">Por ejemplo, el símbolo de moneda para el dólar estadounidense y para el Dólar australiano es $.</span><span class="sxs-lookup"><span data-stu-id="e7bed-130">For example, the currency symbol for the US dollar and for the Australian dollar is $.</span></span>  |

## <a name="relationships"></a><span data-ttu-id="e7bed-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e7bed-131">Relationships</span></span>
<span data-ttu-id="e7bed-132">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e7bed-132">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="e7bed-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e7bed-133">JSON representation</span></span>

<span data-ttu-id="e7bed-134">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e7bed-134">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingCurrency"
}-->

```json
{
  "id": "String (identifier)",
  "symbol": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingCurrency resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
