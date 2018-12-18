---
title: 'event: dismissReminder'
description: Descartar un aviso que se haya desencadenado para un evento de un calendario del usuario.
author: angelgolfer-ms
ms.openlocfilehash: 22c3860beb563c39a252e941d464e8ce1671783c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304175"
---
# <a name="event-dismissreminder"></a><span data-ttu-id="2cd49-103">event: dismissReminder</span><span class="sxs-lookup"><span data-stu-id="2cd49-103">event: dismissReminder</span></span>

> <span data-ttu-id="2cd49-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2cd49-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2cd49-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2cd49-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2cd49-106">Descartar un aviso que desencadena un [evento](../resources/event.md) de un [calendario](../resources/calendar.md)de usuario.</span><span class="sxs-lookup"><span data-stu-id="2cd49-106">Dismiss a reminder that has been triggered for an [event](../resources/event.md) in a user [calendar](../resources/calendar.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="2cd49-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="2cd49-107">Permissions</span></span>
<span data-ttu-id="2cd49-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2cd49-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2cd49-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2cd49-110">Permission type</span></span>      | <span data-ttu-id="2cd49-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2cd49-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2cd49-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2cd49-112">Delegated (work or school account)</span></span> | <span data-ttu-id="2cd49-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2cd49-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="2cd49-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2cd49-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2cd49-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2cd49-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="2cd49-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2cd49-116">Application</span></span> | <span data-ttu-id="2cd49-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2cd49-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="2cd49-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2cd49-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

```http
POST /me/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/events/{id}/dismissReminder

POST /me/calendar/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/calendar/events/{id}/dismissReminder

POST /me/calendars/{id}/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/dismissReminder

POST /me/calendargroup/calendars/{id}/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/dismissReminder

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/dismissReminder
```

## <a name="request-headers"></a><span data-ttu-id="2cd49-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2cd49-119">Request headers</span></span>

| <span data-ttu-id="2cd49-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="2cd49-120">Name</span></span>       | <span data-ttu-id="2cd49-121">Type</span><span class="sxs-lookup"><span data-stu-id="2cd49-121">Type</span></span> | <span data-ttu-id="2cd49-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cd49-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="2cd49-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2cd49-123">Authorization</span></span>  | <span data-ttu-id="2cd49-124">string</span><span class="sxs-lookup"><span data-stu-id="2cd49-124">string</span></span>  | <span data-ttu-id="2cd49-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2cd49-p103">Bearer {token}. Required.</span></span> |


## <a name="response"></a><span data-ttu-id="2cd49-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2cd49-127">Response</span></span>

<span data-ttu-id="2cd49-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2cd49-p104">If successful, this method returns a `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2cd49-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2cd49-130">Example</span></span>

<span data-ttu-id="2cd49-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2cd49-131">Here is an example of how to call this API.</span></span>

### <a name="request"></a><span data-ttu-id="2cd49-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2cd49-132">Request</span></span>
<span data-ttu-id="2cd49-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2cd49-133">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "event_dismissreminder"
}-->

```http
POST https://graph.microsoft.com/beta/me/events/{id}/dismissReminder
```

### <a name="response"></a><span data-ttu-id="2cd49-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2cd49-134">Response</span></span>
<span data-ttu-id="2cd49-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2cd49-135">Here is an example of the response.</span></span>

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
  "description": "event: dismissReminder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
