---
title: 'event: tentativelyAccept'
description: Aceptar provisionalmente el evento especificado en un calendario del usuario.
author: angelgolfer-ms
ms.openlocfilehash: be22b88c444b3720eaf204bda3246d4b99b90623
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27335794"
---
# <a name="event-tentativelyaccept"></a><span data-ttu-id="764ae-103">event: tentativelyAccept</span><span class="sxs-lookup"><span data-stu-id="764ae-103">event: tentativelyAccept</span></span>

<span data-ttu-id="764ae-104">Aceptar provisionalmente el [evento](../resources/event.md) especificado en un [calendario](../resources/calendar.md)de usuario.</span><span class="sxs-lookup"><span data-stu-id="764ae-104">Tentatively accept the specified [event](../resources/event.md) in a user [calendar](../resources/calendar.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="764ae-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="764ae-105">Permissions</span></span>
<span data-ttu-id="764ae-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="764ae-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="764ae-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="764ae-108">Permission type</span></span>      | <span data-ttu-id="764ae-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="764ae-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="764ae-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="764ae-110">Delegated (work or school account)</span></span> | <span data-ttu-id="764ae-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="764ae-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="764ae-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="764ae-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="764ae-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="764ae-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="764ae-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="764ae-114">Application</span></span> | <span data-ttu-id="764ae-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="764ae-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="764ae-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="764ae-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events/{id}/tentativelyAccept
POST /users/{id | userPrincipalName}/events/{id}/tentativelyAccept

POST /me/calendar/events/{id}/tentativelyAccept
POST /users/{id | userPrincipalName}/calendar/events/{id}/tentativelyAccept

POST /me/calendars/{id}/events/{id}/tentativelyAccept
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/tentativelyAccept

POST /me/calendargroup/calendars/{id}/events/{id}/tentativelyAccept
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/tentativelyAccept

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/tentativelyAccept
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/tentativelyAccept
```
## <a name="request-headers"></a><span data-ttu-id="764ae-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="764ae-117">Request headers</span></span>
| <span data-ttu-id="764ae-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="764ae-118">Name</span></span>       | <span data-ttu-id="764ae-119">Type</span><span class="sxs-lookup"><span data-stu-id="764ae-119">Type</span></span> | <span data-ttu-id="764ae-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="764ae-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="764ae-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="764ae-121">Authorization</span></span>  | <span data-ttu-id="764ae-122">string</span><span class="sxs-lookup"><span data-stu-id="764ae-122">string</span></span>  | <span data-ttu-id="764ae-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="764ae-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="764ae-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="764ae-125">Content-Type</span></span> | <span data-ttu-id="764ae-126">string</span><span class="sxs-lookup"><span data-stu-id="764ae-126">string</span></span>  | <span data-ttu-id="764ae-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="764ae-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="764ae-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="764ae-129">Request body</span></span>
<span data-ttu-id="764ae-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="764ae-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="764ae-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="764ae-131">Parameter</span></span>    | <span data-ttu-id="764ae-132">Type</span><span class="sxs-lookup"><span data-stu-id="764ae-132">Type</span></span>   |<span data-ttu-id="764ae-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="764ae-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="764ae-134">comment</span><span class="sxs-lookup"><span data-stu-id="764ae-134">comment</span></span>|<span data-ttu-id="764ae-135">String</span><span class="sxs-lookup"><span data-stu-id="764ae-135">String</span></span>|<span data-ttu-id="764ae-p104">Texto incluido en la respuesta. Opcional.</span><span class="sxs-lookup"><span data-stu-id="764ae-p104">Text included in the response. Optional.</span></span>|
|<span data-ttu-id="764ae-138">sendResponse</span><span class="sxs-lookup"><span data-stu-id="764ae-138">sendResponse</span></span>|<span data-ttu-id="764ae-139">Boolean</span><span class="sxs-lookup"><span data-stu-id="764ae-139">Boolean</span></span>|<span data-ttu-id="764ae-p105">`true` si se va a enviar una respuesta al organizador; de lo contrario, `false`. Opcional. El valor predeterminado es `true`.</span><span class="sxs-lookup"><span data-stu-id="764ae-p105">`true` if a response is to be sent to the organizer; otherwise, `false`. Optional. Default is `true`.</span></span>|

## <a name="response"></a><span data-ttu-id="764ae-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="764ae-143">Response</span></span>

<span data-ttu-id="764ae-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="764ae-p106">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="764ae-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="764ae-146">Example</span></span>
<span data-ttu-id="764ae-147">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="764ae-147">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="764ae-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="764ae-148">Request</span></span>
<span data-ttu-id="764ae-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="764ae-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "event_tentativelyaccept"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/tentativelyAccept
Content-type: application/json
Content-length: 56

{
  "comment": "comment-value",
  "sendResponse": true
}
```

##### <a name="response"></a><span data-ttu-id="764ae-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="764ae-150">Response</span></span>
##### <a name="response"></a><span data-ttu-id="764ae-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="764ae-151">Response</span></span>
<span data-ttu-id="764ae-152">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="764ae-152">Here is an example of the response.</span></span>
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
  "description": "event: tentativelyAccept",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
