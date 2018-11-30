---
title: Tipo de recurso reminder
description: Un aviso para un evento en un calendario del usuario.
ms.openlocfilehash: 131de8772c6b4fa400ab0f48197430611030c255
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032083"
---
# <a name="reminder-resource-type"></a><span data-ttu-id="90a11-103">Tipo de recurso reminder</span><span class="sxs-lookup"><span data-stu-id="90a11-103">reminder resource type</span></span>

<span data-ttu-id="90a11-104">Un aviso para un [evento](event.md) en un [calendario](calendar.md)de usuario.</span><span class="sxs-lookup"><span data-stu-id="90a11-104">A reminder for an [event](event.md) in a user [calendar](calendar.md).</span></span>

## <a name="properties"></a><span data-ttu-id="90a11-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="90a11-105">Properties</span></span>
| <span data-ttu-id="90a11-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="90a11-106">Property</span></span>     | <span data-ttu-id="90a11-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="90a11-107">Type</span></span>   |<span data-ttu-id="90a11-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="90a11-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="90a11-109">changeKey</span><span class="sxs-lookup"><span data-stu-id="90a11-109">changeKey</span></span>|<span data-ttu-id="90a11-110">String</span><span class="sxs-lookup"><span data-stu-id="90a11-110">String</span></span>|<span data-ttu-id="90a11-p101">Identifica la versión del aviso. Cada vez que cambia el aviso, cambia también **changeKey**. Permite que Exchange aplique los cambios a la versión correcta del objeto.</span><span class="sxs-lookup"><span data-stu-id="90a11-p101">Identifies the version of the reminder. Every time the reminder is changed, **changeKey** changes as well. This allows Exchange to apply changes to the correct version of the object.</span></span>|
|<span data-ttu-id="90a11-114">eventEndTime</span><span class="sxs-lookup"><span data-stu-id="90a11-114">eventEndTime</span></span>|[<span data-ttu-id="90a11-115">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="90a11-115">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="90a11-116">Fecha, hora y zona horaria en que finaliza el evento.</span><span class="sxs-lookup"><span data-stu-id="90a11-116">The date, time and time zone that the event ends.</span></span>|
|<span data-ttu-id="90a11-117">eventId</span><span class="sxs-lookup"><span data-stu-id="90a11-117">eventId</span></span>|<span data-ttu-id="90a11-118">String</span><span class="sxs-lookup"><span data-stu-id="90a11-118">String</span></span>|<span data-ttu-id="90a11-p102">Identificador único del evento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="90a11-p102">The unique ID of the event. Read only.</span></span>|
|<span data-ttu-id="90a11-121">eventLocation</span><span class="sxs-lookup"><span data-stu-id="90a11-121">eventLocation</span></span>|[<span data-ttu-id="90a11-122">Location</span><span class="sxs-lookup"><span data-stu-id="90a11-122">Location</span></span>](location.md)|<span data-ttu-id="90a11-123">Ubicación del evento.</span><span class="sxs-lookup"><span data-stu-id="90a11-123">The location of the event.</span></span>|
|<span data-ttu-id="90a11-124">eventStartTime</span><span class="sxs-lookup"><span data-stu-id="90a11-124">eventStartTime</span></span>|[<span data-ttu-id="90a11-125">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="90a11-125">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="90a11-126">Fecha, hora y zona horaria en que comienza el evento.</span><span class="sxs-lookup"><span data-stu-id="90a11-126">The date, time, and time zone that the event starts.</span></span>|
|<span data-ttu-id="90a11-127">eventSubject</span><span class="sxs-lookup"><span data-stu-id="90a11-127">eventSubject</span></span>|<span data-ttu-id="90a11-128">String</span><span class="sxs-lookup"><span data-stu-id="90a11-128">String</span></span>|<span data-ttu-id="90a11-129">Texto de la línea de asunto del evento.</span><span class="sxs-lookup"><span data-stu-id="90a11-129">The text of the event's subject line.</span></span>|
|<span data-ttu-id="90a11-130">eventWebLink</span><span class="sxs-lookup"><span data-stu-id="90a11-130">eventWebLink</span></span>|<span data-ttu-id="90a11-131">String</span><span class="sxs-lookup"><span data-stu-id="90a11-131">String</span></span>|<span data-ttu-id="90a11-132">Dirección URL para abrir el evento en Outlook en la web.</span><span class="sxs-lookup"><span data-stu-id="90a11-132">The URL to open the event in Outlook on the web.</span></span><br/><br/><span data-ttu-id="90a11-p103">El evento se abrirá en el navegador si está conectado a su buzón mediante Outlook en la web. Se le pedirá que inicie sesión si no la ha iniciado ya en el navegador.</span><span class="sxs-lookup"><span data-stu-id="90a11-p103">The event will open in the browser if you are logged in to your mailbox via Outlook on the web. You will be prompted to login if you are not already logged in with the browser.</span></span><br/><br/><span data-ttu-id="90a11-135">Se puede acceder a esta dirección URL desde un iFrame.</span><span class="sxs-lookup"><span data-stu-id="90a11-135">This URL can be accessed from within an iFrame.</span></span>|
|<span data-ttu-id="90a11-136">reminderFireTime</span><span class="sxs-lookup"><span data-stu-id="90a11-136">reminderFireTime</span></span>|[<span data-ttu-id="90a11-137">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="90a11-137">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="90a11-138">Fecha, hora y zona horaria en que se establece que se produzca el aviso.</span><span class="sxs-lookup"><span data-stu-id="90a11-138">The date, time, and time zone that the reminder is set to occur.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="90a11-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="90a11-139">JSON representation</span></span>

<span data-ttu-id="90a11-140">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="90a11-140">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.reminder"
}-->

```json
{
  "changeKey": "string",
  "eventEndTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "eventId": "string",
  "eventLocation": {"@odata.type": "microsoft.graph.location"},
  "eventStartTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "eventSubject": "string",
  "eventWebLink": "string",
  "reminderFireTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "reminder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->