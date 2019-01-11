---
title: 'event: accept'
description: Acepte el evento especificado en un calendario del usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 0ff048863f1e2077967c995e7e8806f6df7716ca
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814885"
---
# <a name="event-accept"></a><span data-ttu-id="fb199-103">event: accept</span><span class="sxs-lookup"><span data-stu-id="fb199-103">event: accept</span></span>

<span data-ttu-id="fb199-104">Acepte el [evento](../resources/event.md) especificado en un [calendario](../resources/calendar.md)de usuario.</span><span class="sxs-lookup"><span data-stu-id="fb199-104">Accept the specified [event](../resources/event.md) in a user [calendar](../resources/calendar.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="fb199-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="fb199-105">Permissions</span></span>
<span data-ttu-id="fb199-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fb199-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fb199-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fb199-108">Permission type</span></span>      | <span data-ttu-id="fb199-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fb199-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fb199-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fb199-110">Delegated (work or school account)</span></span> | <span data-ttu-id="fb199-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb199-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="fb199-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fb199-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fb199-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb199-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="fb199-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fb199-114">Application</span></span> | <span data-ttu-id="fb199-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb199-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="fb199-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fb199-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events/{id}/accept
POST /users/{id | userPrincipalName}/events/{id}/accept

POST /me/calendar/events/{id}/accept
POST /users/{id | userPrincipalName}/calendar/events/{id}/accept

POST /me/calendars/{id}/events/{id}/accept
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/accept

POST /me/calendargroup/calendars/{id}/events/{id}/accept
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/accept

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/accept
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/accept
```
## <a name="request-headers"></a><span data-ttu-id="fb199-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fb199-117">Request headers</span></span>
| <span data-ttu-id="fb199-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb199-118">Name</span></span>       | <span data-ttu-id="fb199-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb199-119">Type</span></span> | <span data-ttu-id="fb199-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb199-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="fb199-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="fb199-121">Authorization</span></span>  | <span data-ttu-id="fb199-122">string</span><span class="sxs-lookup"><span data-stu-id="fb199-122">string</span></span>  | <span data-ttu-id="fb199-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fb199-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fb199-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="fb199-125">Content-Type</span></span> | <span data-ttu-id="fb199-126">string</span><span class="sxs-lookup"><span data-stu-id="fb199-126">string</span></span>  | <span data-ttu-id="fb199-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fb199-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fb199-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fb199-129">Request body</span></span>
<span data-ttu-id="fb199-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="fb199-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="fb199-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fb199-131">Parameter</span></span>    | <span data-ttu-id="fb199-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb199-132">Type</span></span>   |<span data-ttu-id="fb199-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb199-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fb199-134">comment</span><span class="sxs-lookup"><span data-stu-id="fb199-134">comment</span></span>|<span data-ttu-id="fb199-135">String</span><span class="sxs-lookup"><span data-stu-id="fb199-135">String</span></span>|<span data-ttu-id="fb199-p104">Texto incluido en la respuesta. Opcional.</span><span class="sxs-lookup"><span data-stu-id="fb199-p104">Text included in the response. Optional.</span></span>|
|<span data-ttu-id="fb199-138">sendResponse</span><span class="sxs-lookup"><span data-stu-id="fb199-138">sendResponse</span></span>|<span data-ttu-id="fb199-139">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb199-139">Boolean</span></span>|<span data-ttu-id="fb199-p105">`true` si se va a enviar una respuesta al organizador; de lo contrario, `false`. Opcional. El valor predeterminado es `true`.</span><span class="sxs-lookup"><span data-stu-id="fb199-p105">`true` if a response is to be sent to the organizer; otherwise, `false`. Optional. Default is `true`.</span></span>|

## <a name="response"></a><span data-ttu-id="fb199-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb199-143">Response</span></span>

<span data-ttu-id="fb199-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb199-p106">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fb199-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb199-146">Example</span></span>
<span data-ttu-id="fb199-147">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="fb199-147">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="fb199-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fb199-148">Request</span></span>
<span data-ttu-id="fb199-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fb199-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "event_accept"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/accept
Content-type: application/json
Content-length: 56

{
  "comment": "comment-value",
  "sendResponse": true
}
```

##### <a name="response"></a><span data-ttu-id="fb199-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb199-150">Response</span></span>
<span data-ttu-id="fb199-151">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb199-151">Here is an example of the response.</span></span>
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
  "description": "event: accept",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
