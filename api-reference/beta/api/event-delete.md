---
title: Delete event
description: Elimina el evento.
ms.openlocfilehash: cb62f1b7593f4fffe0416fd8c2f81917440e897a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088083"
---
# <a name="delete-event"></a><span data-ttu-id="4c69e-103">Eliminar evento</span><span class="sxs-lookup"><span data-stu-id="4c69e-103">Delete event</span></span>

> <span data-ttu-id="4c69e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4c69e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4c69e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4c69e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4c69e-106">Elimina el evento.</span><span class="sxs-lookup"><span data-stu-id="4c69e-106">Delete event.</span></span>
## <a name="permissions"></a><span data-ttu-id="4c69e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4c69e-107">Permissions</span></span>
<span data-ttu-id="4c69e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4c69e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4c69e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4c69e-110">Permission type</span></span>      | <span data-ttu-id="4c69e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4c69e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4c69e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4c69e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="4c69e-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4c69e-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="4c69e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4c69e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4c69e-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4c69e-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="4c69e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4c69e-116">Application</span></span> | <span data-ttu-id="4c69e-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4c69e-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="4c69e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4c69e-118">HTTP request</span></span>
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
## <a name="request-headers"></a><span data-ttu-id="4c69e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4c69e-119">Request headers</span></span>
| <span data-ttu-id="4c69e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="4c69e-120">Name</span></span>       | <span data-ttu-id="4c69e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c69e-121">Type</span></span> | <span data-ttu-id="4c69e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c69e-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="4c69e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="4c69e-123">Authorization</span></span>  | <span data-ttu-id="4c69e-124">string</span><span class="sxs-lookup"><span data-stu-id="4c69e-124">string</span></span>  | <span data-ttu-id="4c69e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4c69e-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4c69e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4c69e-127">Request body</span></span>
<span data-ttu-id="4c69e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4c69e-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4c69e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c69e-129">Response</span></span>

<span data-ttu-id="4c69e-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4c69e-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4c69e-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c69e-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4c69e-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4c69e-133">Request</span></span>
<span data-ttu-id="4c69e-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c69e-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_event"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/events/{id}
```
##### <a name="response"></a><span data-ttu-id="4c69e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c69e-135">Response</span></span>
<span data-ttu-id="4c69e-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4c69e-136">Here is an example of the response.</span></span> 
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
