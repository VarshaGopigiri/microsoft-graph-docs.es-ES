---
title: Tipo de recurso reminder
description: Un aviso para un evento en un calendario del usuario.
ms.openlocfilehash: e7b7e2266b5959c6aa4927ecad52e24342d607e4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086458"
---
# <a name="reminder-resource-type"></a><span data-ttu-id="1518f-103">Tipo de recurso reminder</span><span class="sxs-lookup"><span data-stu-id="1518f-103">reminder resource type</span></span>

> <span data-ttu-id="1518f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1518f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1518f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1518f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1518f-106">Un aviso para un [evento](event.md) en un [calendario](calendar.md)de usuario.</span><span class="sxs-lookup"><span data-stu-id="1518f-106">A reminder for an [event](event.md) in a user [calendar](calendar.md).</span></span>

## <a name="properties"></a><span data-ttu-id="1518f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1518f-107">Properties</span></span>
| <span data-ttu-id="1518f-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1518f-108">Property</span></span>     | <span data-ttu-id="1518f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="1518f-109">Type</span></span>   |<span data-ttu-id="1518f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1518f-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1518f-111">changeKey</span><span class="sxs-lookup"><span data-stu-id="1518f-111">changeKey</span></span>|<span data-ttu-id="1518f-112">String</span><span class="sxs-lookup"><span data-stu-id="1518f-112">String</span></span>|<span data-ttu-id="1518f-p102">Identifica la versión del aviso. Cada vez que cambia el aviso, cambia también **changeKey**. Permite que Exchange aplique los cambios a la versión correcta del objeto.</span><span class="sxs-lookup"><span data-stu-id="1518f-p102">Identifies the version of the reminder. Every time the reminder is changed, **changeKey** changes as well. This allows Exchange to apply changes to the correct version of the object.</span></span>|
|<span data-ttu-id="1518f-116">eventEndTime</span><span class="sxs-lookup"><span data-stu-id="1518f-116">eventEndTime</span></span>|[<span data-ttu-id="1518f-117">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="1518f-117">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="1518f-118">Fecha, hora y zona horaria en que finaliza el evento.</span><span class="sxs-lookup"><span data-stu-id="1518f-118">The date, time and time zone that the event ends.</span></span>|
|<span data-ttu-id="1518f-119">eventId</span><span class="sxs-lookup"><span data-stu-id="1518f-119">eventId</span></span>|<span data-ttu-id="1518f-120">String</span><span class="sxs-lookup"><span data-stu-id="1518f-120">String</span></span>|<span data-ttu-id="1518f-p103">Identificador único del evento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1518f-p103">The unique ID of the event. Read only.</span></span>|
|<span data-ttu-id="1518f-123">eventLocation</span><span class="sxs-lookup"><span data-stu-id="1518f-123">eventLocation</span></span>|[<span data-ttu-id="1518f-124">Location</span><span class="sxs-lookup"><span data-stu-id="1518f-124">Location</span></span>](location.md)|<span data-ttu-id="1518f-125">Ubicación del evento.</span><span class="sxs-lookup"><span data-stu-id="1518f-125">The location of the event.</span></span>|
|<span data-ttu-id="1518f-126">eventStartTime</span><span class="sxs-lookup"><span data-stu-id="1518f-126">eventStartTime</span></span>|[<span data-ttu-id="1518f-127">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="1518f-127">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="1518f-128">Fecha, hora y zona horaria en que comienza el evento.</span><span class="sxs-lookup"><span data-stu-id="1518f-128">The date, time, and time zone that the event starts.</span></span>|
|<span data-ttu-id="1518f-129">eventSubject</span><span class="sxs-lookup"><span data-stu-id="1518f-129">eventSubject</span></span>|<span data-ttu-id="1518f-130">String</span><span class="sxs-lookup"><span data-stu-id="1518f-130">String</span></span>|<span data-ttu-id="1518f-131">Texto de la línea de asunto del evento.</span><span class="sxs-lookup"><span data-stu-id="1518f-131">The text of the event's subject line.</span></span>|
|<span data-ttu-id="1518f-132">eventWebLink</span><span class="sxs-lookup"><span data-stu-id="1518f-132">eventWebLink</span></span>|<span data-ttu-id="1518f-133">String</span><span class="sxs-lookup"><span data-stu-id="1518f-133">String</span></span>|<span data-ttu-id="1518f-134">Dirección URL para abrir el evento en Outlook en la web.</span><span class="sxs-lookup"><span data-stu-id="1518f-134">The URL to open the event in Outlook on the web.</span></span><br/><br/><span data-ttu-id="1518f-p104">El evento se abrirá en el navegador si está conectado a su buzón mediante Outlook en la web. Se le pedirá que inicie sesión si no la ha iniciado ya en el navegador.</span><span class="sxs-lookup"><span data-stu-id="1518f-p104">The event will open in the browser if you are logged in to your mailbox via Outlook on the web. You will be prompted to login if you are not already logged in with the browser.</span></span><br/><br/><span data-ttu-id="1518f-137">Se puede acceder a esta dirección URL desde un iFrame.</span><span class="sxs-lookup"><span data-stu-id="1518f-137">This URL can be accessed from within an iFrame.</span></span>|
|<span data-ttu-id="1518f-138">reminderFireTime</span><span class="sxs-lookup"><span data-stu-id="1518f-138">reminderFireTime</span></span>|[<span data-ttu-id="1518f-139">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="1518f-139">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="1518f-140">Fecha, hora y zona horaria en que se establece que se produzca el aviso.</span><span class="sxs-lookup"><span data-stu-id="1518f-140">The date, time, and time zone that the reminder is set to occur.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1518f-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1518f-141">JSON representation</span></span>

<span data-ttu-id="1518f-142">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="1518f-142">Here is a JSON representation of the resource</span></span>

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