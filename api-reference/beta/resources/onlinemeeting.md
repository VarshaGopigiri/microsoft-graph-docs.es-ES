---
title: tipo de recurso onlineMeeting
description: Captura información acerca de la reunión, incluida la dirección URL de la combinación, la lista de los asistentes y la descripción.
ms.openlocfilehash: 73e45f7f2c04df469f2c2fb0faf1c8a0f8680a64
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084087"
---
# <a name="onlinemeeting-resource-type"></a><span data-ttu-id="140b3-103">tipo de recurso onlineMeeting</span><span class="sxs-lookup"><span data-stu-id="140b3-103">onlineMeeting resource type</span></span>

> <span data-ttu-id="140b3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="140b3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="140b3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="140b3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="140b3-106">Captura información acerca de la reunión, incluida la dirección URL de la combinación, la lista de los asistentes y la descripción.</span><span class="sxs-lookup"><span data-stu-id="140b3-106">Captures information about the meeting, including the join URL, the attendees list, and the description.</span></span>

## <a name="methods"></a><span data-ttu-id="140b3-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="140b3-107">Methods</span></span>

| <span data-ttu-id="140b3-108">Método</span><span class="sxs-lookup"><span data-stu-id="140b3-108">Method</span></span>         | <span data-ttu-id="140b3-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="140b3-109">Return Type</span></span> | <span data-ttu-id="140b3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="140b3-110">Description</span></span> |
|:---------------|:--------|:----------|
| [<span data-ttu-id="140b3-111">Obtener onlineMeeting</span><span class="sxs-lookup"><span data-stu-id="140b3-111">Get onlineMeeting</span></span>](../api/onlinemeeting-get.md) | [<span data-ttu-id="140b3-112">onlineMeeting</span><span class="sxs-lookup"><span data-stu-id="140b3-112">onlineMeeting</span></span>](onlinemeeting.md) | <span data-ttu-id="140b3-113">Leer las propiedades y las relaciones del objeto onlineMeeting.</span><span class="sxs-lookup"><span data-stu-id="140b3-113">Read properties and relationships of onlineMeeting object.</span></span> |

## <a name="properties"></a><span data-ttu-id="140b3-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="140b3-114">Properties</span></span>

| <span data-ttu-id="140b3-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="140b3-115">Property</span></span>                  | <span data-ttu-id="140b3-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="140b3-116">Type</span></span>                                                   | <span data-ttu-id="140b3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="140b3-117">Description</span></span>                                                                                                                |
| :------------------------ | :----------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="140b3-118">accessLevel</span><span class="sxs-lookup"><span data-stu-id="140b3-118">accessLevel</span></span>               | <span data-ttu-id="140b3-119">String</span><span class="sxs-lookup"><span data-stu-id="140b3-119">String</span></span>                                                 | <span data-ttu-id="140b3-120">El nivel de acceso que controla la admisión a la reunión en línea.</span><span class="sxs-lookup"><span data-stu-id="140b3-120">The access level that controls admission to the online meeting.</span></span> <span data-ttu-id="140b3-121">Los valores posibles son: `everyone`, `invited`, `locked`, `sameEnterprise` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="140b3-121">Possible values are: `everyone`, `invited`, `locked`, `sameEnterprise`, `unknown`.</span></span> |
| <span data-ttu-id="140b3-122">Audioconferencia</span><span class="sxs-lookup"><span data-stu-id="140b3-122">audioConferencing</span></span>         | [<span data-ttu-id="140b3-123">Audioconferencia</span><span class="sxs-lookup"><span data-stu-id="140b3-123">audioConferencing</span></span>](audioconferencing.md)              | <span data-ttu-id="140b3-124">Representa la información de acceso telefónica de un onlineMeeting.</span><span class="sxs-lookup"><span data-stu-id="140b3-124">Represents phone access information for an onlineMeeting.</span></span> |
| <span data-ttu-id="140b3-125">canceledDateTime</span><span class="sxs-lookup"><span data-stu-id="140b3-125">canceledDateTime</span></span>          | <span data-ttu-id="140b3-126">DateTime</span><span class="sxs-lookup"><span data-stu-id="140b3-126">DateTime</span></span>                                               | <span data-ttu-id="140b3-127">La hora cuando se canceló la reunión.</span><span class="sxs-lookup"><span data-stu-id="140b3-127">The time when the meeting was canceled.</span></span> |
| <span data-ttu-id="140b3-128">chatInfo</span><span class="sxs-lookup"><span data-stu-id="140b3-128">chatInfo</span></span>                  | [<span data-ttu-id="140b3-129">chatInfo</span><span class="sxs-lookup"><span data-stu-id="140b3-129">chatInfo</span></span>](chatinfo.md)                                | <span data-ttu-id="140b3-130">El chat asociado a esta reunión.</span><span class="sxs-lookup"><span data-stu-id="140b3-130">The chat associated with this meeting.</span></span> |
| <span data-ttu-id="140b3-131">creationDateTime</span><span class="sxs-lookup"><span data-stu-id="140b3-131">creationDateTime</span></span>          | <span data-ttu-id="140b3-132">DateTime</span><span class="sxs-lookup"><span data-stu-id="140b3-132">DateTime</span></span>                                               | <span data-ttu-id="140b3-133">La hora de creación de la reunión.</span><span class="sxs-lookup"><span data-stu-id="140b3-133">The time when the meeting was created.</span></span> <span data-ttu-id="140b3-134">ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="140b3-134">Readonly.</span></span>
| <span data-ttu-id="140b3-135">endDateTime</span><span class="sxs-lookup"><span data-stu-id="140b3-135">endDateTime</span></span>               | <span data-ttu-id="140b3-136">DateTime</span><span class="sxs-lookup"><span data-stu-id="140b3-136">DateTime</span></span>                                               | <span data-ttu-id="140b3-137">Hora de finalización de la reunión.</span><span class="sxs-lookup"><span data-stu-id="140b3-137">End time of the meeting.</span></span> |
| <span data-ttu-id="140b3-138">entryExitAnnouncement</span><span class="sxs-lookup"><span data-stu-id="140b3-138">entryExitAnnouncement</span></span>     | <span data-ttu-id="140b3-139">Booleano</span><span class="sxs-lookup"><span data-stu-id="140b3-139">Boolean</span></span>                                                | <span data-ttu-id="140b3-140">El estado de anuncios de asistencia para la reunión en línea.</span><span class="sxs-lookup"><span data-stu-id="140b3-140">The attendance announcements status for the online meeting.</span></span> <span data-ttu-id="140b3-141">Cuando se habilitan los anuncios de asistencia, la reunión en línea anunciar los nombres de la combinación de participantswho la reunión a través de audio.</span><span class="sxs-lookup"><span data-stu-id="140b3-141">When attendance announcements are enabled, the online meeting will announce the names of the participantswho join the meeting through audio.</span></span> |
| <span data-ttu-id="140b3-142">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="140b3-142">expirationDateTime</span></span>        | <span data-ttu-id="140b3-143">DateTime</span><span class="sxs-lookup"><span data-stu-id="140b3-143">DateTime</span></span>                                               | <span data-ttu-id="140b3-144">La fecha de la hora Universal coordinada (UTC) y la hora después de la cual absoluta se puede eliminar la reunión en línea.</span><span class="sxs-lookup"><span data-stu-id="140b3-144">The absolute Coordinated Universal Time (UTC) date and time after which the online meeting can be deleted.</span></span> <span data-ttu-id="140b3-145">El día y la hora deben estar comprendido entre un año antes y diez años después, la fecha y hora actuales en el servidor.</span><span class="sxs-lookup"><span data-stu-id="140b3-145">The day and time must be between one year before, and ten years after, the current date and time on the server.</span></span> |
| <span data-ttu-id="140b3-146">id</span><span class="sxs-lookup"><span data-stu-id="140b3-146">id</span></span>                        | <span data-ttu-id="140b3-147">String</span><span class="sxs-lookup"><span data-stu-id="140b3-147">String</span></span>                                                 | <span data-ttu-id="140b3-148">El identificador asociado con la reunión en línea.</span><span class="sxs-lookup"><span data-stu-id="140b3-148">The ID associated with the online meeting.</span></span> <span data-ttu-id="140b3-149">Usar en una solicitud GET HTTP como el identificador.</span><span class="sxs-lookup"><span data-stu-id="140b3-149">Used in a GET HTTP request as the ID.</span></span> <span data-ttu-id="140b3-150">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="140b3-150">Read-only.</span></span> <span data-ttu-id="140b3-151">Servidor que se generó.</span><span class="sxs-lookup"><span data-stu-id="140b3-151">Server generated.</span></span> |
| <span data-ttu-id="140b3-152">isCancelled</span><span class="sxs-lookup"><span data-stu-id="140b3-152">isCancelled</span></span>               | <span data-ttu-id="140b3-153">Booleano</span><span class="sxs-lookup"><span data-stu-id="140b3-153">Boolean</span></span>                                                | <span data-ttu-id="140b3-154">Si se ha cancelado la reunión.</span><span class="sxs-lookup"><span data-stu-id="140b3-154">Whether the meeting has been canceled.</span></span> |
| <span data-ttu-id="140b3-155">joinUrl</span><span class="sxs-lookup"><span data-stu-id="140b3-155">joinUrl</span></span>                   | <span data-ttu-id="140b3-156">String</span><span class="sxs-lookup"><span data-stu-id="140b3-156">String</span></span>                                                 | <span data-ttu-id="140b3-157">La dirección URL que se usa cuando se se unió a la reunión en línea desde la web.</span><span class="sxs-lookup"><span data-stu-id="140b3-157">The URL that is used when the online meeting is joined from the web.</span></span> |
| <span data-ttu-id="140b3-158">meetingType</span><span class="sxs-lookup"><span data-stu-id="140b3-158">meetingType</span></span>               | <span data-ttu-id="140b3-159">String</span><span class="sxs-lookup"><span data-stu-id="140b3-159">String</span></span>                                                 | <span data-ttu-id="140b3-160">Los valores posibles son: `meetNow`, `scheduled`, `recurring`,`broadcast`</span><span class="sxs-lookup"><span data-stu-id="140b3-160">Possible values are: `meetNow`, `scheduled`, `recurring`, `broadcast`</span></span> |
| <span data-ttu-id="140b3-161">participants</span><span class="sxs-lookup"><span data-stu-id="140b3-161">participants</span></span>              | [<span data-ttu-id="140b3-162">meetingParticipants</span><span class="sxs-lookup"><span data-stu-id="140b3-162">meetingParticipants</span></span>](meetingparticipants.md)          | <span data-ttu-id="140b3-163">Los participantes asociados a la reunión en línea.</span><span class="sxs-lookup"><span data-stu-id="140b3-163">The participants associated with the online meeting.</span></span>  <span data-ttu-id="140b3-164">Esto incluye el organizador y los asistentes.</span><span class="sxs-lookup"><span data-stu-id="140b3-164">This includes the organizer and the attendees.</span></span> |
| <span data-ttu-id="140b3-165">startDateTime</span><span class="sxs-lookup"><span data-stu-id="140b3-165">startDateTime</span></span>             | <span data-ttu-id="140b3-166">DateTime</span><span class="sxs-lookup"><span data-stu-id="140b3-166">DateTime</span></span>                                               | <span data-ttu-id="140b3-167">Hora de inicio de la reunión.</span><span class="sxs-lookup"><span data-stu-id="140b3-167">Start time of the meeting.</span></span> |
| <span data-ttu-id="140b3-168">subject</span><span class="sxs-lookup"><span data-stu-id="140b3-168">subject</span></span>                   | <span data-ttu-id="140b3-169">String</span><span class="sxs-lookup"><span data-stu-id="140b3-169">String</span></span>                                                 | <span data-ttu-id="140b3-170">El asunto de la reunión en línea.</span><span class="sxs-lookup"><span data-stu-id="140b3-170">The subject of the online meeting.</span></span> |

## <a name="relationships"></a><span data-ttu-id="140b3-171">Relaciones</span><span class="sxs-lookup"><span data-stu-id="140b3-171">Relationships</span></span>
<span data-ttu-id="140b3-172">Ninguno</span><span class="sxs-lookup"><span data-stu-id="140b3-172">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="140b3-173">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="140b3-173">JSON representation</span></span>

<span data-ttu-id="140b3-174">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="140b3-174">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onlineMeeting"
}-->
```json
{
  "accessLevel": "everyone | invited | locked | sameEnterprise",
  "audioConferencing": {"@odata.type": "#microsoft.graph.audioConferencing"},
  "canceledDateTime": "String (timestamp)",
  "chatInfo": {"@odata.type": "#microsoft.graph.chatInfo"},
  "creationDateTime": "String (timestamp)",
  "endDateTime": "String (timestamp)",
  "entryExitAnnouncement": true,
  "expirationDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "isCancelled": false,
  "joinUrl": "String",
  "meetingType": "meetNow | scheduled | recurring | broadcast",
  "participants": {"@odata.type": "#microsoft.graph.meetingParticipants"},
  "startDateTime": "String (timestamp)",
  "subject": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onlineMeeting resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
