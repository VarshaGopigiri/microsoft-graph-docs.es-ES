---
title: Eliminar calendario
description: Elimina un calendario que no sea el predeterminado.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: f86f1618e36d221164caa65484344f2a3d177765
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922203"
---
# <a name="delete-calendar"></a><span data-ttu-id="60d08-103">Eliminar calendario</span><span class="sxs-lookup"><span data-stu-id="60d08-103">Delete calendar</span></span>

> <span data-ttu-id="60d08-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="60d08-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="60d08-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="60d08-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="60d08-106">Elimina un calendario que no sea el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="60d08-106">Delete a calendar other than the default calendar.</span></span>
## <a name="permissions"></a><span data-ttu-id="60d08-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="60d08-107">Permissions</span></span>
<span data-ttu-id="60d08-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="60d08-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="60d08-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="60d08-110">Permission type</span></span>      | <span data-ttu-id="60d08-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="60d08-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="60d08-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="60d08-112">Delegated (work or school account)</span></span> | <span data-ttu-id="60d08-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="60d08-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="60d08-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="60d08-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="60d08-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="60d08-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="60d08-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="60d08-116">Application</span></span> | <span data-ttu-id="60d08-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="60d08-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="60d08-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="60d08-118">HTTP request</span></span>
<span data-ttu-id="60d08-119"><!-- { "blockType": "ignored" } -->[Calendario](../resources/calendar.md) de un usuario que no sea el calendario predeterminado en el valor predeterminado [calendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="60d08-119"><!-- { "blockType": "ignored" } --> A user's [calendar](../resources/calendar.md) other than the default calendar in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendars/{id}

DELETE /me/calendarGroup/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="60d08-120">Un [calendar](../resources/calendar.md) que no sea el calendario predeterminado de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="60d08-120">A [calendar](../resources/calendar.md) other than the default calendar, in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendarGroups/{id}/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="request-headers"></a><span data-ttu-id="60d08-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="60d08-121">Request headers</span></span>
| <span data-ttu-id="60d08-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="60d08-122">Name</span></span>           |  <span data-ttu-id="60d08-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="60d08-123">Type</span></span>    | <span data-ttu-id="60d08-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="60d08-124">Description</span></span>|
|:---------------|:---------|:----------|
| <span data-ttu-id="60d08-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="60d08-125">Authorization</span></span>  |  <span data-ttu-id="60d08-126">string</span><span class="sxs-lookup"><span data-stu-id="60d08-126">string</span></span>  | <span data-ttu-id="60d08-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="60d08-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="60d08-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="60d08-129">Request body</span></span>
<span data-ttu-id="60d08-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="60d08-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="60d08-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60d08-131">Response</span></span>

<span data-ttu-id="60d08-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60d08-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="60d08-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="60d08-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="60d08-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="60d08-135">Request</span></span>
<span data-ttu-id="60d08-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="60d08-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_calendar"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/calendar
```
##### <a name="response"></a><span data-ttu-id="60d08-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60d08-137">Response</span></span>
<span data-ttu-id="60d08-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60d08-138">Here is an example of the response.</span></span> 
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
