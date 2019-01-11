---
title: 'event: dismissReminder'
description: Descartar un aviso que se haya desencadenado para un evento de un calendario del usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 1165dbf036848ee01ad80a1080a01e9b344fc399
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811574"
---
# <a name="event-dismissreminder"></a><span data-ttu-id="9a3ff-103">event: dismissReminder</span><span class="sxs-lookup"><span data-stu-id="9a3ff-103">event: dismissReminder</span></span>

<span data-ttu-id="9a3ff-104">Descartar un aviso que desencadena un [evento](../resources/event.md) de un [calendario](../resources/calendar.md)de usuario.</span><span class="sxs-lookup"><span data-stu-id="9a3ff-104">Dismiss a reminder that has been triggered for an [event](../resources/event.md) in a user [calendar](../resources/calendar.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="9a3ff-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="9a3ff-105">Permissions</span></span>
<span data-ttu-id="9a3ff-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9a3ff-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9a3ff-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9a3ff-108">Permission type</span></span>      | <span data-ttu-id="9a3ff-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9a3ff-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9a3ff-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9a3ff-110">Delegated (work or school account)</span></span> | <span data-ttu-id="9a3ff-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9a3ff-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="9a3ff-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9a3ff-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9a3ff-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9a3ff-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="9a3ff-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9a3ff-114">Application</span></span> | <span data-ttu-id="9a3ff-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9a3ff-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="9a3ff-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9a3ff-116">HTTP request</span></span>

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

## <a name="request-headers"></a><span data-ttu-id="9a3ff-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9a3ff-117">Request headers</span></span>
| <span data-ttu-id="9a3ff-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="9a3ff-118">Name</span></span>       | <span data-ttu-id="9a3ff-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a3ff-119">Type</span></span> | <span data-ttu-id="9a3ff-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a3ff-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="9a3ff-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="9a3ff-121">Authorization</span></span>  | <span data-ttu-id="9a3ff-122">string</span><span class="sxs-lookup"><span data-stu-id="9a3ff-122">string</span></span>  | <span data-ttu-id="9a3ff-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a3ff-p102">Bearer {token}. Required.</span></span> |

<br/>

## <a name="response"></a><span data-ttu-id="9a3ff-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a3ff-125">Response</span></span>

<span data-ttu-id="9a3ff-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a3ff-p103">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9a3ff-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9a3ff-128">Example</span></span>

<span data-ttu-id="9a3ff-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9a3ff-129">Here is an example of how to call this API.</span></span>

### <a name="request"></a><span data-ttu-id="9a3ff-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9a3ff-130">Request</span></span>
<span data-ttu-id="9a3ff-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a3ff-131">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "event_dismissreminder"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/dismissReminder
```

<br/>

### <a name="response"></a><span data-ttu-id="9a3ff-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a3ff-132">Response</span></span>
<span data-ttu-id="9a3ff-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a3ff-133">Here is an example of the response.</span></span>

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
