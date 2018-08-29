# <a name="location-resource-type"></a><span data-ttu-id="189b8-101">Tipo de recurso Location</span><span class="sxs-lookup"><span data-stu-id="189b8-101">Location resource type</span></span>

<span data-ttu-id="189b8-102">Representa información de ubicación de un [event](event.md).</span><span class="sxs-lookup"><span data-stu-id="189b8-102">Represents location information of an [event](event.md).</span></span>

<span data-ttu-id="189b8-103">Hay varias maneras de crear eventos de calendario, por ejemplo, a través de una aplicación con la API de REST [crear evento](../api/user_post_events.md) o manualmente con la interfaz de usuario de Outlook.</span><span class="sxs-lookup"><span data-stu-id="189b8-103">There are multiple ways to create events in a calendar, for example, through an app using the [create event](../api/user_post_events.md) REST API, or manually using the Outlook user interface.</span></span> <span data-ttu-id="189b8-104">Al crear un evento con la interfaz de usuario, puede especificar la ubicación como texto sin formato (por ejemplo, "bar de Harry") o elegirla en la lista de salas proporcionada por Outlook, [Bing Autosuggest](https://blogs.bing.com/search/2013/02/20/a-look-at-autosuggest/) o [Búsqueda local de Bing](https://blogs.bing.com/search/2010/08/17/local-search-on-m-bing-com/).</span><span class="sxs-lookup"><span data-stu-id="189b8-104">When you create an event using the user interface, you can specify the location as plain text (for example, "Harry's Bar"), or from the rooms list provided by Outlook, [Bing Autosuggest](https://blogs.bing.com/search/2013/02/20/a-look-at-autosuggest/), or [Bing local search](https://blogs.bing.com/search/2010/08/17/local-search-on-m-bing-com/).</span></span> 

<span data-ttu-id="189b8-105">Según cómo se cree el evento, se espera que Outlook establezca la propiedad **locationType** de solo lectura de manera distinta.</span><span class="sxs-lookup"><span data-stu-id="189b8-105">Depending on how an event is created, expect Outlook to set the read-only **locationType** property differently.</span></span> 

| <span data-ttu-id="189b8-106">Cómo se creó el evento</span><span class="sxs-lookup"><span data-stu-id="189b8-106">How event was created</span></span>  | <span data-ttu-id="189b8-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="189b8-107">Property</span></span>   | <span data-ttu-id="189b8-108">Valor esperado</span><span class="sxs-lookup"><span data-stu-id="189b8-108">Expected value</span></span> |
|:----------|:-------|:--------------------------------|
| <span data-ttu-id="189b8-109">API de REST [crear evento](../api/user_post_events.md)</span><span class="sxs-lookup"><span data-stu-id="189b8-109">[create event](../api/user_post_events.md) REST API</span></span> | <span data-ttu-id="189b8-110">**locationType**</span><span class="sxs-lookup"><span data-stu-id="189b8-110">**locationType**</span></span> | `default` |
| <span data-ttu-id="189b8-111">Interfaz de usuario de Outlook</span><span class="sxs-lookup"><span data-stu-id="189b8-111">User interface in Outlook</span></span> | <span data-ttu-id="189b8-112">**locationType**</span><span class="sxs-lookup"><span data-stu-id="189b8-112">**locationType**</span></span> | <span data-ttu-id="189b8-113">Uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="189b8-113">One of the following:</span></span> <ul><li><span data-ttu-id="189b8-114">`default` en el caso de una ubicación especificada como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="189b8-114">`default` for a location entered as plain text.</span></span></li><li><span data-ttu-id="189b8-115">`conferenceRoom` en el caso de una sala proporcionada por la lista de salas de Outlook.</span><span class="sxs-lookup"><span data-stu-id="189b8-115">`conferenceRoom` for a room provided by the Outlook rooms list.</span></span></li><li><span data-ttu-id="189b8-116">O, cualquiera de esta lista (`homeAddress`, `businessAddress`, `geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `localBusiness` o `postalAddress`) en el caso de una ubicación de Bing Autosuggest o de Búsqueda local de Bing.</span><span class="sxs-lookup"><span data-stu-id="189b8-116">Or, any of this list - `homeAddress`, `businessAddress`,`geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `localBusiness`, `postalAddress` - for a location from Bing Autosuggest or Bing local search.</span></span></li></ul> |

## <a name="properties"></a><span data-ttu-id="189b8-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="189b8-117">Properties</span></span>
| <span data-ttu-id="189b8-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="189b8-118">Property</span></span>  | <span data-ttu-id="189b8-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="189b8-119">Type</span></span>   | <span data-ttu-id="189b8-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="189b8-120">Description</span></span>                                                     |
|:----------|:-------|:----------------------------------------------------------------|
| <span data-ttu-id="189b8-121">address</span><span class="sxs-lookup"><span data-stu-id="189b8-121">address</span></span> | [<span data-ttu-id="189b8-122">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="189b8-122">physicalAddress</span></span>](physicaladdress.md) |<span data-ttu-id="189b8-123">Dirección postal de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="189b8-123">The street address of the location.</span></span> |
| <span data-ttu-id="189b8-124">coordinates</span><span class="sxs-lookup"><span data-stu-id="189b8-124">coordinates</span></span> | [<span data-ttu-id="189b8-125">outlookGeoCoordinates</span><span class="sxs-lookup"><span data-stu-id="189b8-125">outlookGeoCoordinates</span></span>](outlookgeocoordinates.md) | <span data-ttu-id="189b8-126">Coordenadas geográficas y elevación de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="189b8-126">The geographic coordinates and elevation of the location.</span></span> |
| <span data-ttu-id="189b8-127">displayName</span><span class="sxs-lookup"><span data-stu-id="189b8-127">displayName</span></span>  | <span data-ttu-id="189b8-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="189b8-128">String</span></span> | <span data-ttu-id="189b8-129">Nombre asociado a la ubicación.</span><span class="sxs-lookup"><span data-stu-id="189b8-129">The name associated with the location.</span></span>                       |
| <span data-ttu-id="189b8-130">locationEmailAddress</span><span class="sxs-lookup"><span data-stu-id="189b8-130">locationEmailAddress</span></span> | <span data-ttu-id="189b8-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="189b8-131">String</span></span> | <span data-ttu-id="189b8-132">Dirección de correo electrónico opcional de la ubicación</span><span class="sxs-lookup"><span data-stu-id="189b8-132">Optional email address of the location.</span></span>              |
| <span data-ttu-id="189b8-133">locationUri</span><span class="sxs-lookup"><span data-stu-id="189b8-133">locationUri</span></span> | <span data-ttu-id="189b8-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="189b8-134">String</span></span> | <span data-ttu-id="189b8-135">URI opcional que representa la ubicación.</span><span class="sxs-lookup"><span data-stu-id="189b8-135">Optional URI representing the location.</span></span> |
| <span data-ttu-id="189b8-136">locationType</span><span class="sxs-lookup"><span data-stu-id="189b8-136">locationType</span></span> | <span data-ttu-id="189b8-137">locationType</span><span class="sxs-lookup"><span data-stu-id="189b8-137">locationType</span></span> | <span data-ttu-id="189b8-138">Tipo de ubicación.</span><span class="sxs-lookup"><span data-stu-id="189b8-138">The type of location.</span></span> <span data-ttu-id="189b8-139">Los valores posibles son: `default`, `conferenceRoom`, `homeAddress`, `businessAddress`,`geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `localBusiness` y `postalAddress`.</span><span class="sxs-lookup"><span data-stu-id="189b8-139">The possible values are `default`, `conferenceRoom`, `homeAddress`, `businessAddress`, `geoCoordinates`, `streetAddress`, `hotel`, `restaurant`, `localBusiness`, `postalAddress`, , or .</span></span> <span data-ttu-id="189b8-140">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="189b8-140">Read-only.</span></span>|
| <span data-ttu-id="189b8-141">uniqueId</span><span class="sxs-lookup"><span data-stu-id="189b8-141">uniqueId</span></span> | <span data-ttu-id="189b8-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="189b8-142">String</span></span> | <span data-ttu-id="189b8-143">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="189b8-143">For internal use only.</span></span>|
| <span data-ttu-id="189b8-144">uniqueIdType</span><span class="sxs-lookup"><span data-stu-id="189b8-144">uniqueIdType</span></span> | <span data-ttu-id="189b8-145">locationUniqueIdType</span><span class="sxs-lookup"><span data-stu-id="189b8-145">locationUniqueIdType values</span></span> | <span data-ttu-id="189b8-146">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="189b8-146">For internal use only.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="189b8-147">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="189b8-147">JSON representation</span></span>

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
