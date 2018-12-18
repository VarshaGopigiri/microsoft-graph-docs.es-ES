---
title: Obtener identificadores inmutables para recursos de Outlook
description: 'Los elementos de Outlook (mensajes, eventos, contactos, tareas) tienen un comportamiento interesante que probablemente no ha observado nunca o le ha provocado gran frustración: el cambio de ID. No sucede con frecuencia, solo si se mueve el elemento, pero puede provocar problemas reales para las aplicaciones que almacenan identificadores sin conexión para su uso posterior. Los identificadores inmutables permiten que la aplicación obtenga un ID que no cambia durante toda la duración del elemento.'
author: angelgolfer-ms
ms.openlocfilehash: 34d88ed2cbc39902f1240757367beb112cc007b4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315200"
---
# <a name="get-immutable-identifiers-for-outlook-resources"></a><span data-ttu-id="37a81-105">Obtener identificadores inmutables para recursos de Outlook</span><span class="sxs-lookup"><span data-stu-id="37a81-105">Get immutable identifiers for Outlook resources</span></span>

<span data-ttu-id="37a81-106">Los elementos de Outlook (mensajes, eventos, contactos, tareas) tienen un comportamiento interesante que probablemente no ha observado nunca o le ha provocado gran frustración: el cambio de ID.</span><span class="sxs-lookup"><span data-stu-id="37a81-106">Outlook items (messages, events, contacts, tasks) have an interesting behavior that you've probably either never noticed or has caused you significant frustration: their IDs change.</span></span> <span data-ttu-id="37a81-107">No sucede con frecuencia, solo si se mueve el elemento, pero puede provocar problemas reales para las aplicaciones que almacenan identificadores sin conexión para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="37a81-107">It doesn't happen often, only if the item is moved, but it can cause real problems for apps that store IDs offline for later use.</span></span> <span data-ttu-id="37a81-108">Los identificadores inmutables permiten que la aplicación obtenga un ID que no cambia durante toda la duración del elemento.</span><span class="sxs-lookup"><span data-stu-id="37a81-108">Immutable identifiers enables your application to obtain an ID that does not change for the lifetime of the item.</span></span>

> <span data-ttu-id="37a81-109">**Importante:** Los identificadores inmutables son solo disponibles en la versión /beta de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="37a81-109">**Important:** Immutable identifiers are only avaiable on the /beta version in Microsoft Graph.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="37a81-110">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="37a81-110">How it works</span></span>

<span data-ttu-id="37a81-111">El Identificador inmutable es una característica opcional de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="37a81-111">Immutable ID is an optional feature for Microsoft Graph.</span></span> <span data-ttu-id="37a81-112">Para habilitarla, la aplicación debe enviar un encabezado HTTP adicional en sus solicitudes de API:</span><span class="sxs-lookup"><span data-stu-id="37a81-112">To opt in, your application needs to send an additional HTTP header in your API requests:</span></span>

```http
Prefer: IdType="ImmutableId"
```

<span data-ttu-id="37a81-113">Este encabezado solo se aplica a la solicitud en la que está incluido.</span><span class="sxs-lookup"><span data-stu-id="37a81-113">This header only applies to the request it is included with.</span></span> <span data-ttu-id="37a81-114">Si quiere usar siempre identificadores inmutables, debe incluir este encabezado en cada solicitud de API.</span><span class="sxs-lookup"><span data-stu-id="37a81-114">If you want to always use immutable IDs, you must include this header with every API request.</span></span>

## <a name="lifetime-of-immutable-ids"></a><span data-ttu-id="37a81-115">Duración de los ID inmutables</span><span class="sxs-lookup"><span data-stu-id="37a81-115">Lifetime of Immutable IDs</span></span>

<span data-ttu-id="37a81-116">Un identificador inmutable de un elemento no cambiará siempre y cuando el elemento permanece en el mismo buzón.</span><span class="sxs-lookup"><span data-stu-id="37a81-116">An item's immutable ID will not change so long as the item stays in the same mailbox.</span></span> <span data-ttu-id="37a81-117">Eso significa que el identificador inmutable no cambiará si el elemento se mueve a otra carpeta del buzón.</span><span class="sxs-lookup"><span data-stu-id="37a81-117">That means that immutable ID will NOT change if the item is moved to a different folder in the mailbox.</span></span> <span data-ttu-id="37a81-118">Pero, el identificador inmutable cambiará si:</span><span class="sxs-lookup"><span data-stu-id="37a81-118">However, the immutable ID will change if:</span></span>

- <span data-ttu-id="37a81-119">El usuario mueve el elemento a un buzón de archivo</span><span class="sxs-lookup"><span data-stu-id="37a81-119">The user moves the item to an archive mailbox</span></span>
- <span data-ttu-id="37a81-120">El usuario exporta el elemento (a un archivo PST, como un archivo MSG, etc.) y vuelve a importarlo a su buzón</span><span class="sxs-lookup"><span data-stu-id="37a81-120">The user exports the item (to a PST, as an MSG file, etc.) and re-imports it into their mailbox</span></span>

## <a name="items-that-support-immutable-id"></a><span data-ttu-id="37a81-121">Elementos que admiten el identificador inmutable</span><span class="sxs-lookup"><span data-stu-id="37a81-121">Items that support immutable ID</span></span>

<span data-ttu-id="37a81-122">Los siguientes elementos admiten los identificadores inmutables:</span><span class="sxs-lookup"><span data-stu-id="37a81-122">The following items support immutable IDs:</span></span>

- [<span data-ttu-id="37a81-123">Tipo de recurso message</span><span class="sxs-lookup"><span data-stu-id="37a81-123">message resource type</span></span>](/graph/api/resources/message?view=graph-rest-beta)
- [<span data-ttu-id="37a81-124">Tipo de recurso attachment</span><span class="sxs-lookup"><span data-stu-id="37a81-124">attachment resource type</span></span>](/graph/api/resources/attachment?view=graph-rest-beta)
- [<span data-ttu-id="37a81-125">Tipo de recurso event</span><span class="sxs-lookup"><span data-stu-id="37a81-125">event resource type</span></span>](/graph/api/resources/event?view=graph-rest-beta)
- [<span data-ttu-id="37a81-126">Tipo de recurso eventMessage</span><span class="sxs-lookup"><span data-stu-id="37a81-126">eventMessage resource type</span></span>](/graph/api/resources/eventmessage?view=graph-rest-beta)
- [<span data-ttu-id="37a81-127">Tipo de recurso contact</span><span class="sxs-lookup"><span data-stu-id="37a81-127">contact resource type</span></span>](/graph/api/resources/contact?view=graph-rest-beta)
- [<span data-ttu-id="37a81-128">Tipo de recurso outlookTask</span><span class="sxs-lookup"><span data-stu-id="37a81-128">outlookTask resource type</span></span>](/graph/api/resources/outlooktask?view=graph-rest-beta)

<span data-ttu-id="37a81-129">Los tipos de contenedor (mailFolder, calendario, etc.) no admiten los identificadores inmutables, pero sus identificadores normales ya eran constantes.</span><span class="sxs-lookup"><span data-stu-id="37a81-129">Container types (mailFolder, calendar, etc.) do not support immutable ID, but their regular IDs were already constant.</span></span>

## <a name="immutable-id-with-change-notifications"></a><span data-ttu-id="37a81-130">El identificador inmutable con las notificaciones de cambios</span><span class="sxs-lookup"><span data-stu-id="37a81-130">Immutable ID with change notifications</span></span>

<span data-ttu-id="37a81-131">Puede solicitar que Microsoft Graph envíe ID inmutables en las notificaciones de cambios incluyendo el encabezado `Prefer: IdType="ImmutableId"` al [crear una suscripción](/graph/api/subscription-post-subscriptions?view=graph-rest-beta).</span><span class="sxs-lookup"><span data-stu-id="37a81-131">You can request that Microsoft Graph send immutable IDs in change notifications by including the `Prefer: IdType="ImmutableId"` header when [creating a subscription](/graph/api/subscription-post-subscriptions?view=graph-rest-beta).</span></span> <span data-ttu-id="37a81-132">Las suscripciones existentes creadas sin el encabezado seguirán usando el formato ID predeterminado.</span><span class="sxs-lookup"><span data-stu-id="37a81-132">Existing subscriptions created without the header will continue to use the default ID format.</span></span> <span data-ttu-id="37a81-133">Para pasar de una suscripción existente a usar identificadores inmutables, debe eliminarlos y volver a crearlos con el encabezado.</span><span class="sxs-lookup"><span data-stu-id="37a81-133">In order to switch existing subscriptions to use immutable IDs, you must delete and recreate them using the header.</span></span>

## <a name="immutable-id-with-delta-query"></a><span data-ttu-id="37a81-134">El identificador inmutable con consulta delta</span><span class="sxs-lookup"><span data-stu-id="37a81-134">Immutable ID with delta query</span></span>

<span data-ttu-id="37a81-135">Puede solicitar que Microsoft Graph devuelva identificadores inmutables en [respuestas de consultas delta](delta-query-overview.md) para los tipos de recursos admitidos, incluyendo el encabezado `Prefer: IdType="ImmutableId"`.</span><span class="sxs-lookup"><span data-stu-id="37a81-135">You can request that Microsoft Graph return immutable IDs in [delta query responses](delta-query-overview.md) for supported resource types by including the `Prefer: IdType="ImmutableId"` header.</span></span> <span data-ttu-id="37a81-136">Los valores `nextLink` y `deltaLink` devueltos por las consultas de delta son compatibles con ambos formatos ID, por lo que no es necesario volver a sincronizar la aplicación para aprovechar del ID inmutable.</span><span class="sxs-lookup"><span data-stu-id="37a81-136">The `nextLink` and `deltaLink` values returned by delta queries are compatible with both ID formats, so your application does not need to re-synchronize to take advantage of immutable ID.</span></span> <span data-ttu-id="37a81-137">Puede usar el encabezado para obtener los identificadores inmutables en el futuro y puede [actualizar el almacenamiento de la aplicación](#updating-existing-data) por separado.</span><span class="sxs-lookup"><span data-stu-id="37a81-137">You can use the header to get immutable IDs going forward, and you can [update your app's storage](#updating-existing-data) separately.</span></span>

## <a name="updating-existing-data"></a><span data-ttu-id="37a81-138">Actualizar los datos existentes</span><span class="sxs-lookup"><span data-stu-id="37a81-138">Updating existing data</span></span>

<span data-ttu-id="37a81-139">Si ya tiene una base de datos con miles de identificadores normales, puede migrar esos ID para usar el formato inmutable con la función [translateExchangeIds](/graph/api/user-translateexchangeids?view=graph-rest-beta).</span><span class="sxs-lookup"><span data-stu-id="37a81-139">If you've already got a database filled with thousands of regular IDs, you can migrate those IDs to immutable format using the [translateExchangeIds](/graph/api/user-translateexchangeids?view=graph-rest-beta) function.</span></span> <span data-ttu-id="37a81-140">Puede proporcionar una matriz de hasta 1000 identificadores para convertir en un formato de destino.</span><span class="sxs-lookup"><span data-stu-id="37a81-140">You can provide an array of up to 1000 IDs to be translated into a target format.</span></span>

> <span data-ttu-id="37a81-141">**Nota:** También puede usar `translateExchangeIds` para migrar aplicaciones de servicios Web Exchange a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="37a81-141">**Note:** You can also use `translateExchangeIds` to migrate Exchange Web Services applications to Microsoft Graph.</span></span>

### <a name="example"></a><span data-ttu-id="37a81-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37a81-142">Example</span></span>

<span data-ttu-id="37a81-143">En el ejemplo siguiente se convierte un ID de Graph normal a un ID de Graph inmutable.</span><span class="sxs-lookup"><span data-stu-id="37a81-143">The following example translates a normal Graph ID to an immutable Graph ID.</span></span>

#### <a name="request"></a><span data-ttu-id="37a81-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="37a81-144">Request</span></span>

```http
POST https://graph.microsoft.com/beta/me/translateExchangeIds

{
  "inputIds" :
  [
    "AQMkAGM2…"
  ],
  "targetIdType" : "restImmutableEntryId",
  "sourceIdType" : "restId"
}
```

#### <a name="response"></a><span data-ttu-id="37a81-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37a81-145">Response</span></span>

```http
HTTP 200 OK

{
  "value": [
    {
      "targetId": "AAkALgAA...",
      "sourceId": "AQMkAGM2..."
    }
  ]
}
```