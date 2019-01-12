---
title: Delete event
description: Elimina el evento.
author: angelgolfer-ms
localization_priority: Priority
ms.prod: outlook
ms.openlocfilehash: ae39e73a9aa81d1b86701017ef2805f33f7d4c17
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918387"
---
# <a name="delete-event"></a><span data-ttu-id="3224a-103">Delete event</span><span class="sxs-lookup"><span data-stu-id="3224a-103">Delete event</span></span>

<span data-ttu-id="3224a-104">Elimina el evento.</span><span class="sxs-lookup"><span data-stu-id="3224a-104">Delete event.</span></span>
## <a name="permissions"></a><span data-ttu-id="3224a-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="3224a-105">Permissions</span></span>
<span data-ttu-id="3224a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3224a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3224a-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3224a-108">Permission type</span></span>      | <span data-ttu-id="3224a-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3224a-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3224a-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3224a-110">Delegated (work or school account)</span></span> | <span data-ttu-id="3224a-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3224a-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="3224a-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3224a-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3224a-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3224a-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="3224a-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3224a-114">Application</span></span> | <span data-ttu-id="3224a-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3224a-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="3224a-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3224a-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/events/{id}
DELETE /users/{id | userPrincipalName}/events/{id}
DELETE /groups/{id}/events/{id}

DELETE /me/calendar/events/{id}
DELETE /users/{id | userPrincipalName}/calendar/events/{id}
DELETE /groups/{id}/calendar/events/{id}/

DELETE /me/calendars/{id}/events/{id}
DELETE /users/{id | userPrincipalName}/calendars/{id}/events/{id}

DELETE /me/calendargroup/calendars/{id}/events/{id}
DELETE /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}

DELETE /me/calendargroups/{id}/calendars/{id}/events/{id}
DELETE /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}
```
## <a name="request-headers"></a><span data-ttu-id="3224a-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3224a-117">Request headers</span></span>
| <span data-ttu-id="3224a-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="3224a-118">Name</span></span>       | <span data-ttu-id="3224a-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="3224a-119">Type</span></span> | <span data-ttu-id="3224a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3224a-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="3224a-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="3224a-121">Authorization</span></span>  | <span data-ttu-id="3224a-122">string</span><span class="sxs-lookup"><span data-stu-id="3224a-122">string</span></span>  | <span data-ttu-id="3224a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3224a-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3224a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3224a-125">Request body</span></span>
<span data-ttu-id="3224a-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3224a-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3224a-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3224a-127">Response</span></span>

<span data-ttu-id="3224a-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3224a-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3224a-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3224a-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3224a-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3224a-131">Request</span></span>
<span data-ttu-id="3224a-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3224a-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_event"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/events/{id}
```
##### <a name="response"></a><span data-ttu-id="3224a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3224a-133">Response</span></span>
<span data-ttu-id="3224a-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3224a-134">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
