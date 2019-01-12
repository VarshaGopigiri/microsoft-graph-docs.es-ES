---
title: 'event: dismissReminder'
description: Descartar un aviso que se haya desencadenado para un evento de un calendario del usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: cf2421db56babd394a3c011fb9bd4db9f83cb823
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990323"
---
# <a name="event-dismissreminder"></a><span data-ttu-id="3f4d6-103">event: dismissReminder</span><span class="sxs-lookup"><span data-stu-id="3f4d6-103">event: dismissReminder</span></span>

<span data-ttu-id="3f4d6-104">Descartar un aviso que desencadena un [evento](../resources/event.md) de un [calendario](../resources/calendar.md)de usuario.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-104">Dismiss a reminder that has been triggered for an [event](../resources/event.md) in a user [calendar](../resources/calendar.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="3f4d6-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="3f4d6-105">Permissions</span></span>
<span data-ttu-id="3f4d6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3f4d6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3f4d6-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3f4d6-108">Permission type</span></span>      | <span data-ttu-id="3f4d6-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3f4d6-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3f4d6-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3f4d6-110">Delegated (work or school account)</span></span> | <span data-ttu-id="3f4d6-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3f4d6-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="3f4d6-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3f4d6-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3f4d6-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3f4d6-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="3f4d6-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3f4d6-114">Application</span></span> | <span data-ttu-id="3f4d6-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3f4d6-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="3f4d6-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3f4d6-116">HTTP request</span></span>

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

<br/>

## <a name="request-headers"></a><span data-ttu-id="3f4d6-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3f4d6-117">Request headers</span></span>
| <span data-ttu-id="3f4d6-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="3f4d6-118">Name</span></span>       | <span data-ttu-id="3f4d6-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f4d6-119">Type</span></span> | <span data-ttu-id="3f4d6-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f4d6-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="3f4d6-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="3f4d6-121">Authorization</span></span>  | <span data-ttu-id="3f4d6-122">string</span><span class="sxs-lookup"><span data-stu-id="3f4d6-122">string</span></span>  | <span data-ttu-id="3f4d6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-p102">Bearer {token}. Required.</span></span> |

<br/>

## <a name="response"></a><span data-ttu-id="3f4d6-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f4d6-125">Response</span></span>

<span data-ttu-id="3f4d6-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-p103">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3f4d6-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f4d6-128">Example</span></span>

<span data-ttu-id="3f4d6-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-129">Here is an example of how to call this API.</span></span>

### <a name="request"></a><span data-ttu-id="3f4d6-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3f4d6-130">Request</span></span>
<span data-ttu-id="3f4d6-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-131">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "event_dismissreminder"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/dismissReminder
```

<br/>

### <a name="response"></a><span data-ttu-id="3f4d6-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f4d6-132">Response</span></span>
<span data-ttu-id="3f4d6-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-133">Here is an example of the response.</span></span>

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
