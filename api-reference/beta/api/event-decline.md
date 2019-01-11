---
title: 'event: decline'
description: Rechazar la invitación para el evento especificado en un calendario del usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 218ca79b05507fc63ba6f45e2fcb5dd4a0835361
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866958"
---
# <a name="event-decline"></a><span data-ttu-id="38c0f-103">event: decline</span><span class="sxs-lookup"><span data-stu-id="38c0f-103">event: decline</span></span>

> <span data-ttu-id="38c0f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="38c0f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="38c0f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="38c0f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="38c0f-106">Rechazar la invitación para el [evento](../resources/event.md) especificado en un [calendario](../resources/calendar.md)de usuario.</span><span class="sxs-lookup"><span data-stu-id="38c0f-106">Decline invitation to the specified [event](../resources/event.md) in a user [calendar](../resources/calendar.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="38c0f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="38c0f-107">Permissions</span></span>
<span data-ttu-id="38c0f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="38c0f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="38c0f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="38c0f-110">Permission type</span></span>      | <span data-ttu-id="38c0f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="38c0f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="38c0f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="38c0f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="38c0f-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="38c0f-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="38c0f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="38c0f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="38c0f-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="38c0f-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="38c0f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="38c0f-116">Application</span></span> | <span data-ttu-id="38c0f-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="38c0f-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="38c0f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="38c0f-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/events/{id}/decline
POST /users/{id | userPrincipalName}/events/{id}/decline

POST /me/calendar/events/{id}/decline
POST /users/{id | userPrincipalName}/calendar/events/{id}/decline

POST /me/calendars/{id}/events/{id}/decline
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/decline

POST /me/calendargroup/calendars/{id}/events/{id}/decline
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/decline

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/decline
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/decline
```

<br/>

## <a name="request-headers"></a><span data-ttu-id="38c0f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="38c0f-119">Request headers</span></span>

| <span data-ttu-id="38c0f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="38c0f-120">Name</span></span>       | <span data-ttu-id="38c0f-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="38c0f-121">Type</span></span> | <span data-ttu-id="38c0f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="38c0f-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="38c0f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="38c0f-123">Authorization</span></span>  | <span data-ttu-id="38c0f-124">string</span><span class="sxs-lookup"><span data-stu-id="38c0f-124">string</span></span>  | <span data-ttu-id="38c0f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="38c0f-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="38c0f-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="38c0f-127">Content-Type</span></span> | <span data-ttu-id="38c0f-128">string</span><span class="sxs-lookup"><span data-stu-id="38c0f-128">string</span></span>  | <span data-ttu-id="38c0f-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="38c0f-p104">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="38c0f-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="38c0f-131">Request body</span></span>

<span data-ttu-id="38c0f-132">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="38c0f-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="38c0f-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="38c0f-133">Parameter</span></span>    | <span data-ttu-id="38c0f-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="38c0f-134">Type</span></span>   |<span data-ttu-id="38c0f-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="38c0f-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="38c0f-136">comment</span><span class="sxs-lookup"><span data-stu-id="38c0f-136">comment</span></span>|<span data-ttu-id="38c0f-137">String</span><span class="sxs-lookup"><span data-stu-id="38c0f-137">String</span></span>|<span data-ttu-id="38c0f-p105">Texto incluido en la respuesta. Opcional.</span><span class="sxs-lookup"><span data-stu-id="38c0f-p105">Text included in the response. Optional.</span></span>|
|<span data-ttu-id="38c0f-140">sendResponse</span><span class="sxs-lookup"><span data-stu-id="38c0f-140">sendResponse</span></span>|<span data-ttu-id="38c0f-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="38c0f-141">Boolean</span></span>|<span data-ttu-id="38c0f-p106">`true` si se va a enviar una respuesta al organizador; de lo contrario, `false`. Opcional. El valor predeterminado es `true`.</span><span class="sxs-lookup"><span data-stu-id="38c0f-p106">`true` if a response is to be sent to the organizer; otherwise, `false`. Optional. Default is `true`.</span></span>|

## <a name="response"></a><span data-ttu-id="38c0f-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38c0f-145">Response</span></span>

<span data-ttu-id="38c0f-p107">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38c0f-p107">If successful, this method returns a `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="38c0f-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38c0f-148">Example</span></span>

<span data-ttu-id="38c0f-149">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="38c0f-149">Here is an example of how to call this API.</span></span>

### <a name="request"></a><span data-ttu-id="38c0f-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38c0f-150">Request</span></span>

<span data-ttu-id="38c0f-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="38c0f-151">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "event_decline"
}-->

```http
POST https://graph.microsoft.com/beta/me/events/{id}/decline
Content-type: application/json
Content-length: 56

{
  "comment": "comment-value",
  "sendResponse": true
}
```

### <a name="response"></a><span data-ttu-id="38c0f-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38c0f-152">Response</span></span>

<span data-ttu-id="38c0f-153">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38c0f-153">Here is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "event: decline",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
