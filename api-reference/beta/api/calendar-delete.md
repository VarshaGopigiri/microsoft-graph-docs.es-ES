---
title: Eliminar calendario
description: Elimina un calendario que no sea el predeterminado.
ms.openlocfilehash: 4d2d2e755a240e35f73a9c8e292d52441c14a25a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083382"
---
# <a name="delete-calendar"></a><span data-ttu-id="d2352-103">Eliminar calendario</span><span class="sxs-lookup"><span data-stu-id="d2352-103">Delete calendar</span></span>

> <span data-ttu-id="d2352-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d2352-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d2352-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d2352-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d2352-106">Elimina un calendario que no sea el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d2352-106">Delete a calendar other than the default calendar.</span></span>
## <a name="permissions"></a><span data-ttu-id="d2352-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d2352-107">Permissions</span></span>
<span data-ttu-id="d2352-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2352-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d2352-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2352-110">Permission type</span></span>      | <span data-ttu-id="d2352-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2352-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d2352-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2352-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d2352-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2352-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="d2352-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2352-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d2352-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2352-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="d2352-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2352-116">Application</span></span> | <span data-ttu-id="d2352-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2352-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="d2352-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2352-118">HTTP request</span></span>
<span data-ttu-id="d2352-119"><!-- { "blockType": "ignored" } -->[Calendario](../resources/calendar.md) de un usuario que no sea el calendario predeterminado en el valor predeterminado [calendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="d2352-119"><!-- { "blockType": "ignored" } --> A user's [calendar](../resources/calendar.md) other than the default calendar in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendars/{id}

DELETE /me/calendarGroup/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="d2352-120">Un [calendar](../resources/calendar.md) que no sea el calendario predeterminado de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="d2352-120">A [calendar](../resources/calendar.md) other than the default calendar, in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendarGroups/{id}/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="request-headers"></a><span data-ttu-id="d2352-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2352-121">Request headers</span></span>
| <span data-ttu-id="d2352-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="d2352-122">Name</span></span>           |  <span data-ttu-id="d2352-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2352-123">Type</span></span>    | <span data-ttu-id="d2352-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2352-124">Description</span></span>|
|:---------------|:---------|:----------|
| <span data-ttu-id="d2352-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="d2352-125">Authorization</span></span>  |  <span data-ttu-id="d2352-126">string</span><span class="sxs-lookup"><span data-stu-id="d2352-126">string</span></span>  | <span data-ttu-id="d2352-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2352-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d2352-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2352-129">Request body</span></span>
<span data-ttu-id="d2352-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d2352-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d2352-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2352-131">Response</span></span>

<span data-ttu-id="d2352-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2352-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2352-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2352-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d2352-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2352-135">Request</span></span>
<span data-ttu-id="d2352-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2352-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_calendar"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/calendar
```
##### <a name="response"></a><span data-ttu-id="d2352-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2352-137">Response</span></span>
<span data-ttu-id="d2352-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2352-138">Here is an example of the response.</span></span> 
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
  "description": "Delete calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->