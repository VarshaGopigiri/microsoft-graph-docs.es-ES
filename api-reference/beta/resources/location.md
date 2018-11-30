---
title: Tipo de recurso Location
description: Representa información de ubicación de un evento.
ms.openlocfilehash: fec075d37bfb2d7eca80f5007db53801dda96ed8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083238"
---
# <a name="location-resource-type"></a><span data-ttu-id="fe584-103">Tipo de recurso Location</span><span class="sxs-lookup"><span data-stu-id="fe584-103">Location resource type</span></span>

> <span data-ttu-id="fe584-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fe584-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fe584-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fe584-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fe584-106">Representa información de ubicación de un [event](event.md).</span><span class="sxs-lookup"><span data-stu-id="fe584-106">Represents location information of an [event](event.md).</span></span>

<span data-ttu-id="fe584-107">Hay varias maneras de crear eventos de calendario, por ejemplo, a través de una aplicación con la API de REST [crear evento](../api/user-post-events.md) o manualmente con la interfaz de usuario de Outlook.</span><span class="sxs-lookup"><span data-stu-id="fe584-107">There are multiple ways to create events in a calendar, for example, through an app using the [create event](../api/user-post-events.md) REST API, or manually using the Outlook user interface.</span></span> <span data-ttu-id="fe584-108">Al crear un evento con la interfaz de usuario, puede especificar la ubicación como texto sin formato (por ejemplo, "bar de Harry") o elegirla en la lista de salas proporcionada por Outlook, [Bing Autosuggest](https://blogs.bing.com/search/2013/02/20/a-look-at-autosuggest/) o [Búsqueda local de Bing](https://blogs.bing.com/search/2010/08/17/local-search-on-m-bing-com/).</span><span class="sxs-lookup"><span data-stu-id="fe584-108">When you create an event using the user interface, you can specify the location as plain text (for example, "Harry's Bar"), or from the rooms list provided by Outlook, [Bing Autosuggest](https://blogs.bing.com/search/2013/02/20/a-look-at-autosuggest/), or [Bing local search](https://blogs.bing.com/search/2010/08/17/local-search-on-m-bing-com/).</span></span> 

<span data-ttu-id="fe584-109">Según cómo se cree el evento, se espera que Outlook establezca la propiedad **locationType** de solo lectura de manera distinta.</span><span class="sxs-lookup"><span data-stu-id="fe584-109">Depending on how an event is created, expect Outlook to set the read-only **locationType** property differently.</span></span> 

| <span data-ttu-id="fe584-110">Cómo se creó el evento</span><span class="sxs-lookup"><span data-stu-id="fe584-110">How event was created</span></span>  | <span data-ttu-id="fe584-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fe584-111">Property</span></span>   | <span data-ttu-id="fe584-112">Valor esperado</span><span class="sxs-lookup"><span data-stu-id="fe584-112">Expected value</span></span> |
|:----------|:-------|:--------------------------------|
| <span data-ttu-id="fe584-113">API de REST [crear evento](../api/user-post-events.md)</span><span class="sxs-lookup"><span data-stu-id="fe584-113">[create event](../api/user-post-events.md) REST API</span></span> | <span data-ttu-id="fe584-114">**locationType**</span><span class="sxs-lookup"><span data-stu-id="fe584-114">**locationType**</span></span> | `default` |
| <span data-ttu-id="fe584-115">Interfaz de usuario de Outlook</span><span class="sxs-lookup"><span data-stu-id="fe584-115">User interface in Outlook</span></span> | <span data-ttu-id="fe584-116">**locationType**</span><span class="sxs-lookup"><span data-stu-id="fe584-116">**locationType**</span></span> | <span data-ttu-id="fe584-117">Uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="fe584-117">One of the following:</span></span> <ul><li><span data-ttu-id="fe584-118">`default` en el caso de una ubicación especificada como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="fe584-118">`default` for a location entered as plain text.</span></span></li><li><span data-ttu-id="fe584-119">`conferenceRoom` en el caso de una sala proporcionada por la lista de salas de Outlook.</span><span class="sxs-lookup"><span data-stu-id="fe584-119">`conferenceRoom` for a room provided by the Outlook rooms list.</span></span></li><li><span data-ttu-id="fe584-120">O, cualquiera de esta lista (`homeAddress`, `businessAddress`, `geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `localBusiness` o `postalAddress`) en el caso de una ubicación de Bing Autosuggest o de Búsqueda local de Bing.</span><span class="sxs-lookup"><span data-stu-id="fe584-120">Or, any of this list - `homeAddress`, `businessAddress`,`geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `localBusiness`, `postalAddress` - for a location from Bing Autosuggest or Bing local search.</span></span></li></ul> |




## <a name="properties"></a><span data-ttu-id="fe584-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fe584-121">Properties</span></span>
| <span data-ttu-id="fe584-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fe584-122">Property</span></span>  | <span data-ttu-id="fe584-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="fe584-123">Type</span></span>   | <span data-ttu-id="fe584-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe584-124">Description</span></span>                                                     |
|:----------|:-------|:----------------------------------------------------------------|
| <span data-ttu-id="fe584-125">address</span><span class="sxs-lookup"><span data-stu-id="fe584-125">address</span></span> | [<span data-ttu-id="fe584-126">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="fe584-126">physicalAddress</span></span>](physicaladdress.md) |<span data-ttu-id="fe584-127">Dirección postal de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="fe584-127">The street address of the location.</span></span> |
| <span data-ttu-id="fe584-128">coordinates</span><span class="sxs-lookup"><span data-stu-id="fe584-128">coordinates</span></span> | [<span data-ttu-id="fe584-129">outlookGeoCoordinates</span><span class="sxs-lookup"><span data-stu-id="fe584-129">outlookGeoCoordinates</span></span>](outlookgeocoordinates.md) | <span data-ttu-id="fe584-130">Coordenadas geográficas y elevación de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="fe584-130">The geographic coordinates and elevation of the location.</span></span> |
| <span data-ttu-id="fe584-131">displayName</span><span class="sxs-lookup"><span data-stu-id="fe584-131">displayName</span></span>  | <span data-ttu-id="fe584-132">String</span><span class="sxs-lookup"><span data-stu-id="fe584-132">String</span></span> | <span data-ttu-id="fe584-133">Nombre asociado a la ubicación.</span><span class="sxs-lookup"><span data-stu-id="fe584-133">The name associated with the location.</span></span>                       |
| <span data-ttu-id="fe584-134">locationEmailAddress</span><span class="sxs-lookup"><span data-stu-id="fe584-134">locationEmailAddress</span></span> | <span data-ttu-id="fe584-135">String</span><span class="sxs-lookup"><span data-stu-id="fe584-135">String</span></span> | <span data-ttu-id="fe584-136">Dirección de correo electrónico opcional de la ubicación</span><span class="sxs-lookup"><span data-stu-id="fe584-136">Optional email address of the location.</span></span> |
| <span data-ttu-id="fe584-137">locationUri</span><span class="sxs-lookup"><span data-stu-id="fe584-137">locationUri</span></span> | <span data-ttu-id="fe584-138">String</span><span class="sxs-lookup"><span data-stu-id="fe584-138">String</span></span> | <span data-ttu-id="fe584-139">URI opcional que representa la ubicación.</span><span class="sxs-lookup"><span data-stu-id="fe584-139">Optional URI representing the location.</span></span> |
| <span data-ttu-id="fe584-140">locationType</span><span class="sxs-lookup"><span data-stu-id="fe584-140">locationType</span></span> | <span data-ttu-id="fe584-141">String</span><span class="sxs-lookup"><span data-stu-id="fe584-141">String</span></span> | <span data-ttu-id="fe584-142">Tipo de ubicación.</span><span class="sxs-lookup"><span data-stu-id="fe584-142">The type of location.</span></span> <span data-ttu-id="fe584-143">Los valores posibles son: `conferenceRoom`, `homeAddress`, `businessAddress`, `geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `default`, `localBusiness` y `postalAddress`.</span><span class="sxs-lookup"><span data-stu-id="fe584-143">Possible values are: `default`, `conferenceRoom`, `homeAddress`, `businessAddress`,`geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `localBusiness`, `postalAddress`.</span></span> <span data-ttu-id="fe584-144">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fe584-144">Read-only.</span></span>|
| <span data-ttu-id="fe584-145">uniqueId</span><span class="sxs-lookup"><span data-stu-id="fe584-145">uniqueId</span></span> | <span data-ttu-id="fe584-146">String</span><span class="sxs-lookup"><span data-stu-id="fe584-146">String</span></span> | <span data-ttu-id="fe584-147">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="fe584-147">For internal use only.</span></span>|
| <span data-ttu-id="fe584-148">uniqueIdType</span><span class="sxs-lookup"><span data-stu-id="fe584-148">uniqueIdType</span></span> | <span data-ttu-id="fe584-149">String</span><span class="sxs-lookup"><span data-stu-id="fe584-149">String</span></span> | <span data-ttu-id="fe584-150">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="fe584-150">For internal use only.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="fe584-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fe584-151">JSON representation</span></span>

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
