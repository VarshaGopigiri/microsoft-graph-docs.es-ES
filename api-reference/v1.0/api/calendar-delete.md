---
title: Eliminar calendario
description: Elimina un calendario que no sea el predeterminado.
author: angelgolfer-ms
ms.openlocfilehash: 2285287911fcca961304c8b46d3508db554f95a9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359244"
---
# <a name="delete-calendar"></a><span data-ttu-id="a0f25-103">Eliminar calendario</span><span class="sxs-lookup"><span data-stu-id="a0f25-103">Delete calendar</span></span>

<span data-ttu-id="a0f25-104">Elimina un calendario que no sea el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a0f25-104">Delete a calendar other than the default calendar.</span></span>
## <a name="permissions"></a><span data-ttu-id="a0f25-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a0f25-105">Permissions</span></span>
<span data-ttu-id="a0f25-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a0f25-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a0f25-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a0f25-108">Permission type</span></span>      | <span data-ttu-id="a0f25-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a0f25-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a0f25-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a0f25-110">Delegated (work or school account)</span></span> | <span data-ttu-id="a0f25-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a0f25-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="a0f25-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a0f25-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a0f25-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a0f25-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="a0f25-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a0f25-114">Application</span></span> | <span data-ttu-id="a0f25-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a0f25-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="a0f25-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a0f25-116">HTTP request</span></span>
<span data-ttu-id="a0f25-117"><!-- { "blockType": "ignored" } -->[Calendario](../resources/calendar.md) de un usuario que no sea el calendario predeterminado en el valor predeterminado [calendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="a0f25-117"><!-- { "blockType": "ignored" } --> A user's [calendar](../resources/calendar.md) other than the default calendar in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendars/{id}

DELETE /me/calendarGroup/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="a0f25-118">Un [calendar](../resources/calendar.md) que no sea el calendario predeterminado de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="a0f25-118">A [calendar](../resources/calendar.md) other than the default calendar, in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendarGroups/{id}/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="request-headers"></a><span data-ttu-id="a0f25-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a0f25-119">Request headers</span></span>
| <span data-ttu-id="a0f25-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="a0f25-120">Name</span></span>           |  <span data-ttu-id="a0f25-121">Type</span><span class="sxs-lookup"><span data-stu-id="a0f25-121">Type</span></span>    | <span data-ttu-id="a0f25-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0f25-122">Description</span></span>|
|:---------------|:---------|:----------|
| <span data-ttu-id="a0f25-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a0f25-123">Authorization</span></span>  |  <span data-ttu-id="a0f25-124">string</span><span class="sxs-lookup"><span data-stu-id="a0f25-124">string</span></span>  | <span data-ttu-id="a0f25-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0f25-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a0f25-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a0f25-127">Request body</span></span>
<span data-ttu-id="a0f25-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a0f25-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a0f25-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0f25-129">Response</span></span>

<span data-ttu-id="a0f25-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0f25-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a0f25-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0f25-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a0f25-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a0f25-133">Request</span></span>
<span data-ttu-id="a0f25-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a0f25-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_calendar"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/calendar
```
##### <a name="response"></a><span data-ttu-id="a0f25-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0f25-135">Response</span></span>
<span data-ttu-id="a0f25-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0f25-136">Here is an example of the response.</span></span> 
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
