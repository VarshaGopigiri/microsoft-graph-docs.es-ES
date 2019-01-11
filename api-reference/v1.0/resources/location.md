---
title: Tipo de recurso Location
description: Representa información de ubicación de un evento.
localization_priority: Normal
ms.openlocfilehash: 553634aec386798ac17e00b83883c54a99c0f9ca
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879803"
---
# <a name="location-resource-type"></a><span data-ttu-id="e7ecf-103">Tipo de recurso Location</span><span class="sxs-lookup"><span data-stu-id="e7ecf-103">Location resource type</span></span>

<span data-ttu-id="e7ecf-104">Representa información de ubicación de un [event](event.md).</span><span class="sxs-lookup"><span data-stu-id="e7ecf-104">Represents location information of an [event](event.md).</span></span>

<span data-ttu-id="e7ecf-105">Hay varias maneras de crear eventos de calendario, por ejemplo, a través de una aplicación con la API de REST [crear evento](../api/user-post-events.md) o manualmente con la interfaz de usuario de Outlook.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-105">There are multiple ways to create events in a calendar, for example, through an app using the [create event](../api/user-post-events.md) REST API, or manually using the Outlook user interface.</span></span> <span data-ttu-id="e7ecf-106">Al crear un evento con la interfaz de usuario, puede especificar la ubicación como texto sin formato (por ejemplo, "bar de Harry") o elegirla en la lista de salas proporcionada por Outlook, [Bing Autosuggest](https://blogs.bing.com/search/2013/02/20/a-look-at-autosuggest/) o [Búsqueda local de Bing](https://blogs.bing.com/search/2010/08/17/local-search-on-m-bing-com/).</span><span class="sxs-lookup"><span data-stu-id="e7ecf-106">When you create an event using the user interface, you can specify the location as plain text (for example, "Harry's Bar"), or from the rooms list provided by Outlook, [Bing Autosuggest](https://blogs.bing.com/search/2013/02/20/a-look-at-autosuggest/), or [Bing local search](https://blogs.bing.com/search/2010/08/17/local-search-on-m-bing-com/).</span></span> 

<span data-ttu-id="e7ecf-107">Según cómo se cree el evento, se espera que Outlook establezca la propiedad **locationType** de solo lectura de manera distinta.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-107">Depending on how an event is created, expect Outlook to set the read-only **locationType** property differently.</span></span> 

| <span data-ttu-id="e7ecf-108">Cómo se creó el evento</span><span class="sxs-lookup"><span data-stu-id="e7ecf-108">How event was created</span></span>  | <span data-ttu-id="e7ecf-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7ecf-109">Property</span></span>   | <span data-ttu-id="e7ecf-110">Valor esperado</span><span class="sxs-lookup"><span data-stu-id="e7ecf-110">Expected value</span></span> |
|:----------|:-------|:--------------------------------|
| <span data-ttu-id="e7ecf-111">API de REST [crear evento](../api/user-post-events.md)</span><span class="sxs-lookup"><span data-stu-id="e7ecf-111">[create event](../api/user-post-events.md) REST API</span></span> | <span data-ttu-id="e7ecf-112">**locationType**</span><span class="sxs-lookup"><span data-stu-id="e7ecf-112">**locationType**</span></span> | `default` |
| <span data-ttu-id="e7ecf-113">Interfaz de usuario de Outlook</span><span class="sxs-lookup"><span data-stu-id="e7ecf-113">User interface in Outlook</span></span> | <span data-ttu-id="e7ecf-114">**locationType**</span><span class="sxs-lookup"><span data-stu-id="e7ecf-114">**locationType**</span></span> | <span data-ttu-id="e7ecf-115">Uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e7ecf-115">One of the following:</span></span> <ul><li><span data-ttu-id="e7ecf-116">`default` en el caso de una ubicación especificada como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-116">`default` for a location entered as plain text.</span></span></li><li><span data-ttu-id="e7ecf-117">`conferenceRoom` en el caso de una sala proporcionada por la lista de salas de Outlook.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-117">`conferenceRoom` for a room provided by the Outlook rooms list.</span></span></li><li><span data-ttu-id="e7ecf-118">O, cualquiera de esta lista (`homeAddress`, `businessAddress`, `geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `localBusiness` o `postalAddress`) en el caso de una ubicación de Bing Autosuggest o de Búsqueda local de Bing.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-118">Or, any of this list - `homeAddress`, `businessAddress`,`geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `localBusiness`, `postalAddress` - for a location from Bing Autosuggest or Bing local search.</span></span></li></ul> |

## <a name="properties"></a><span data-ttu-id="e7ecf-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7ecf-119">Properties</span></span>
| <span data-ttu-id="e7ecf-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7ecf-120">Property</span></span>  | <span data-ttu-id="e7ecf-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7ecf-121">Type</span></span>   | <span data-ttu-id="e7ecf-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7ecf-122">Description</span></span>                                                     |
|:----------|:-------|:----------------------------------------------------------------|
| <span data-ttu-id="e7ecf-123">address</span><span class="sxs-lookup"><span data-stu-id="e7ecf-123">address</span></span> | [<span data-ttu-id="e7ecf-124">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="e7ecf-124">physicalAddress</span></span>](physicaladdress.md) |<span data-ttu-id="e7ecf-125">Dirección postal de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-125">The street address of the location.</span></span> |
| <span data-ttu-id="e7ecf-126">coordinates</span><span class="sxs-lookup"><span data-stu-id="e7ecf-126">coordinates</span></span> | [<span data-ttu-id="e7ecf-127">outlookGeoCoordinates</span><span class="sxs-lookup"><span data-stu-id="e7ecf-127">outlookGeoCoordinates</span></span>](outlookgeocoordinates.md) | <span data-ttu-id="e7ecf-128">Coordenadas geográficas y elevación de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-128">The geographic coordinates and elevation of the location.</span></span> |
| <span data-ttu-id="e7ecf-129">displayName</span><span class="sxs-lookup"><span data-stu-id="e7ecf-129">displayName</span></span>  | <span data-ttu-id="e7ecf-130">String</span><span class="sxs-lookup"><span data-stu-id="e7ecf-130">String</span></span> | <span data-ttu-id="e7ecf-131">Nombre asociado a la ubicación.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-131">The name associated with the location.</span></span>                       |
| <span data-ttu-id="e7ecf-132">locationEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e7ecf-132">locationEmailAddress</span></span> | <span data-ttu-id="e7ecf-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="e7ecf-133">String</span></span> | <span data-ttu-id="e7ecf-134">Dirección de correo electrónico opcional de la ubicación</span><span class="sxs-lookup"><span data-stu-id="e7ecf-134">Optional email address of the location.</span></span>              |
| <span data-ttu-id="e7ecf-135">locationUri</span><span class="sxs-lookup"><span data-stu-id="e7ecf-135">locationUri</span></span> | <span data-ttu-id="e7ecf-136">String</span><span class="sxs-lookup"><span data-stu-id="e7ecf-136">String</span></span> | <span data-ttu-id="e7ecf-137">URI opcional que representa la ubicación.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-137">Optional URI representing the location.</span></span> |
| <span data-ttu-id="e7ecf-138">locationType</span><span class="sxs-lookup"><span data-stu-id="e7ecf-138">locationType</span></span> | <span data-ttu-id="e7ecf-139">locationType</span><span class="sxs-lookup"><span data-stu-id="e7ecf-139">locationType</span></span> | <span data-ttu-id="e7ecf-140">Tipo de ubicación.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-140">The type of location.</span></span> <span data-ttu-id="e7ecf-141">Los valores posibles son: `default`, `conferenceRoom`, `homeAddress`, `businessAddress`,`geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `localBusiness`, `postalAddress`.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-141">The possible values are: `default`, `conferenceRoom`, `homeAddress`, `businessAddress`,`geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `localBusiness`, `postalAddress`.</span></span> <span data-ttu-id="e7ecf-142">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-142">Read-only.</span></span>|
| <span data-ttu-id="e7ecf-143">uniqueId</span><span class="sxs-lookup"><span data-stu-id="e7ecf-143">uniqueId</span></span> | <span data-ttu-id="e7ecf-144">String</span><span class="sxs-lookup"><span data-stu-id="e7ecf-144">String</span></span> | <span data-ttu-id="e7ecf-145">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-145">For internal use only.</span></span>|
| <span data-ttu-id="e7ecf-146">uniqueIdType</span><span class="sxs-lookup"><span data-stu-id="e7ecf-146">uniqueIdType</span></span> | <span data-ttu-id="e7ecf-147">locationUniqueIdType</span><span class="sxs-lookup"><span data-stu-id="e7ecf-147">locationUniqueIdType</span></span> | <span data-ttu-id="e7ecf-148">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="e7ecf-148">For internal use only.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="e7ecf-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e7ecf-149">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.location"
}-->
```json
{
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "coordinates": {"@odata.type": "microsoft.graph.outlookGeoCoordinates"},
  "displayName": "string",
  "locationEmailAddress": "string",
  "locationUri": "string",
  "locationType": "string",
  "uniqueId": "string",
  "uniqueIdType": "string"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "location resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
