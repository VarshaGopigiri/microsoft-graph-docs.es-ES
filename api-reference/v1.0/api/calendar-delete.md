---
title: Eliminar calendario
description: Elimina un calendario que no sea el predeterminado.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: af1fe9a0b13aeb20a269b39bac8966bcc31508b4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937421"
---
# <a name="delete-calendar"></a><span data-ttu-id="ad06e-103">Eliminar calendario</span><span class="sxs-lookup"><span data-stu-id="ad06e-103">Delete calendar</span></span>

<span data-ttu-id="ad06e-104">Elimina un calendario que no sea el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ad06e-104">Delete a calendar other than the default calendar.</span></span>
## <a name="permissions"></a><span data-ttu-id="ad06e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ad06e-105">Permissions</span></span>
<span data-ttu-id="ad06e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ad06e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ad06e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ad06e-108">Permission type</span></span>      | <span data-ttu-id="ad06e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ad06e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ad06e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ad06e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ad06e-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ad06e-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="ad06e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ad06e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ad06e-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ad06e-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="ad06e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ad06e-114">Application</span></span> | <span data-ttu-id="ad06e-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ad06e-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ad06e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ad06e-116">HTTP request</span></span>
<span data-ttu-id="ad06e-117"><!-- { "blockType": "ignored" } -->[Calendario](../resources/calendar.md) de un usuario que no sea el calendario predeterminado en el valor predeterminado [calendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="ad06e-117"><!-- { "blockType": "ignored" } --> A user's [calendar](../resources/calendar.md) other than the default calendar in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendars/{id}

DELETE /me/calendarGroup/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="ad06e-118">Un [calendar](../resources/calendar.md) que no sea el calendario predeterminado de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="ad06e-118">A [calendar](../resources/calendar.md) other than the default calendar, in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendarGroups/{id}/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="request-headers"></a><span data-ttu-id="ad06e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ad06e-119">Request headers</span></span>
| <span data-ttu-id="ad06e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="ad06e-120">Name</span></span>           |  <span data-ttu-id="ad06e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad06e-121">Type</span></span>    | <span data-ttu-id="ad06e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad06e-122">Description</span></span>|
|:---------------|:---------|:----------|
| <span data-ttu-id="ad06e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ad06e-123">Authorization</span></span>  |  <span data-ttu-id="ad06e-124">string</span><span class="sxs-lookup"><span data-stu-id="ad06e-124">string</span></span>  | <span data-ttu-id="ad06e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ad06e-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ad06e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ad06e-127">Request body</span></span>
<span data-ttu-id="ad06e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ad06e-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ad06e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad06e-129">Response</span></span>

<span data-ttu-id="ad06e-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad06e-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ad06e-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad06e-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ad06e-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ad06e-133">Request</span></span>
<span data-ttu-id="ad06e-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ad06e-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_calendar"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/calendar
```
##### <a name="response"></a><span data-ttu-id="ad06e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad06e-135">Response</span></span>
<span data-ttu-id="ad06e-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad06e-136">Here is an example of the response.</span></span> 
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
