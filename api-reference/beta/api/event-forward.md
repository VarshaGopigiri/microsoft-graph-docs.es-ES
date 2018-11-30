---
title: 'evento: hacia delante'
description: 'Esta acción permite que el organizador o el Asistente de un evento de reunión para desviar la '
ms.openlocfilehash: 09a98f82e72eef7b223dfccb1f4433c3206f0f7f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083021"
---
# <a name="event-forward"></a><span data-ttu-id="dfc9f-103">evento: hacia delante</span><span class="sxs-lookup"><span data-stu-id="dfc9f-103">event: forward</span></span>

> <span data-ttu-id="dfc9f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dfc9f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dfc9f-106">Esta acción permite que el organizador o el Asistente de un [evento](../resources/event.md) de reunión para reenviar la convocatoria de reunión a un destinatario nuevo.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-106">This action allows the organizer or attendee of a meeting [event](../resources/event.md) to forward the meeting request to a new recipient.</span></span> 

<span data-ttu-id="dfc9f-107">Si el evento de reunión se transfiere desde el buzón de Office 365 de un asistente a otro destinatario, esta acción también envía un mensaje para notificar el organizador de la transferencia y agrega al destinatario a la copia del organizador del evento de reunión.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-107">If the meeting event is forwarded from an attendee's Office 365 mailbox to another recipient, this action also sends a message to notify the organizer of the forwarding, and adds the recipient to the organizer's copy of the meeting event.</span></span> <span data-ttu-id="dfc9f-108">Esta conveniencia no está disponible al reenviar desde una cuenta de Outlook.com.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-108">This convenience is not available when forwarding from an Outlook.com account.</span></span>


## <a name="permissions"></a><span data-ttu-id="dfc9f-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="dfc9f-109">Permissions</span></span>
<span data-ttu-id="dfc9f-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dfc9f-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dfc9f-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dfc9f-112">Permission type</span></span>      | <span data-ttu-id="dfc9f-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dfc9f-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dfc9f-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dfc9f-114">Delegated (work or school account)</span></span> | <span data-ttu-id="dfc9f-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="dfc9f-115">Calendars.Read</span></span>    |
|<span data-ttu-id="dfc9f-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dfc9f-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dfc9f-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="dfc9f-117">Calendars.Read</span></span>    |
|<span data-ttu-id="dfc9f-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dfc9f-118">Application</span></span> | <span data-ttu-id="dfc9f-119">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="dfc9f-119">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="dfc9f-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dfc9f-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events/{id}/forward
POST /users/{id | userPrincipalName}/events/{id}/forward
POST /groups/{id}/events/{id}/forward

POST /me/calendar/events/{id}/forward
POST /users/{id | userPrincipalName}/calendar/events/{id}/forward
POST /groups/{id}/calendar/events/{id}/forward

POST /me/calendars/{id}/events/{id}/forward
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/forward

POST /me/calendargroup/calendars/{id}/events/{id}/forward
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/forward

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/forward
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/forward
```
## <a name="request-headers"></a><span data-ttu-id="dfc9f-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dfc9f-121">Request headers</span></span>
| <span data-ttu-id="dfc9f-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="dfc9f-122">Name</span></span>       | <span data-ttu-id="dfc9f-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="dfc9f-123">Type</span></span> | <span data-ttu-id="dfc9f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfc9f-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="dfc9f-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="dfc9f-125">Authorization</span></span>  | <span data-ttu-id="dfc9f-126">string</span><span class="sxs-lookup"><span data-stu-id="dfc9f-126">string</span></span>  | <span data-ttu-id="dfc9f-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="dfc9f-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="dfc9f-129">Content-Type</span></span> | <span data-ttu-id="dfc9f-130">string</span><span class="sxs-lookup"><span data-stu-id="dfc9f-130">string</span></span>  | <span data-ttu-id="dfc9f-p105">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-p105">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dfc9f-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dfc9f-133">Request body</span></span>
<span data-ttu-id="dfc9f-134">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-134">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="dfc9f-135">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dfc9f-135">Parameter</span></span>    | <span data-ttu-id="dfc9f-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="dfc9f-136">Type</span></span>   |<span data-ttu-id="dfc9f-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfc9f-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dfc9f-138">Comment</span><span class="sxs-lookup"><span data-stu-id="dfc9f-138">Comment</span></span>|<span data-ttu-id="dfc9f-139">String</span><span class="sxs-lookup"><span data-stu-id="dfc9f-139">String</span></span>|<span data-ttu-id="dfc9f-p106">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-p106">A comment to include. Can be an empty string.</span></span>|
|<span data-ttu-id="dfc9f-142">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="dfc9f-142">ToRecipients</span></span>|<span data-ttu-id="dfc9f-143">Colección [recipient](../resources/recipient.md)</span><span class="sxs-lookup"><span data-stu-id="dfc9f-143">[recipient](../resources/recipient.md) collection</span></span>|<span data-ttu-id="dfc9f-144">La lista de destinatarios a la que se reenviará el evento.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-144">The list of recipients to forward the event to.</span></span>|

## <a name="response"></a><span data-ttu-id="dfc9f-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dfc9f-145">Response</span></span>

<span data-ttu-id="dfc9f-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-p107">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dfc9f-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dfc9f-148">Example</span></span>
<span data-ttu-id="dfc9f-149">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-149">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="dfc9f-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dfc9f-150">Request</span></span>
<span data-ttu-id="dfc9f-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-151">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "event_forward"
}-->
```http
POST https://graph.microsoft.com/beta/me/events/{id}/forward
Content-type: application/json
Content-length: 56

{
  "ToRecipients":[
      {
        "emailAddress": {
          "address":"danas@contoso.onmicrosoft.com",
          "name":"Dana Swope"
        }
      }
     ],
  "Comment": "Dana, hope you can make this meeting." 
}

```

##### <a name="response"></a><span data-ttu-id="dfc9f-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dfc9f-152">Response</span></span>
<span data-ttu-id="dfc9f-153">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-153">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "event: forward",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
