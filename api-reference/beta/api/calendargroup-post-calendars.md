---
title: Create Calendar
description: Use esta API para crear un calendario en un grupo de calendarios para un usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: a70683b945745d809aca00a14d5592d598f51647
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966737"
---
# <a name="create-calendar"></a><span data-ttu-id="87eeb-103">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="87eeb-103">Create Calendar</span></span>

> <span data-ttu-id="87eeb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="87eeb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="87eeb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="87eeb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="87eeb-106">Use esta API para crear un calendario en un grupo de calendarios para un [usuario](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="87eeb-106">Use this API to create a new calendar in a calendar group for a [user](../resources/user.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="87eeb-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="87eeb-107">Permissions</span></span>

<span data-ttu-id="87eeb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="87eeb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="87eeb-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="87eeb-110">Permission type</span></span>                        | <span data-ttu-id="87eeb-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="87eeb-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="87eeb-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="87eeb-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="87eeb-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="87eeb-113">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="87eeb-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="87eeb-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="87eeb-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="87eeb-115">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="87eeb-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="87eeb-116">Application</span></span>                            | <span data-ttu-id="87eeb-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="87eeb-117">Calendars.ReadWrite</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="87eeb-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="87eeb-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

<span data-ttu-id="87eeb-119">[calendarGroup](../resources/calendargroup.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="87eeb-119">A user's default [calendarGroup](../resources/calendargroup.md).</span></span>

```http
POST /me/calendarGroup/calendars
POST /users/{id | userPrincipalName}/calendarGroup/calendars
```

<span data-ttu-id="87eeb-120">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="87eeb-120">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>

```http
POST /me/calendarGroups/{id}/calendars
POST /users/{id | userPrincipalName}/calendarGroups/{id}/calendars
```

## <a name="request-headers"></a><span data-ttu-id="87eeb-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="87eeb-121">Request headers</span></span>

| <span data-ttu-id="87eeb-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87eeb-122">Header</span></span>        | <span data-ttu-id="87eeb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="87eeb-123">Value</span></span>                       |
| :------------ | :-------------------------- |
| <span data-ttu-id="87eeb-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="87eeb-124">Authorization</span></span> | <span data-ttu-id="87eeb-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="87eeb-p103">Bearer {token}. Required.</span></span>   |
| <span data-ttu-id="87eeb-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="87eeb-127">Content-Type</span></span>  | <span data-ttu-id="87eeb-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="87eeb-p104">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="87eeb-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="87eeb-130">Request body</span></span>

<span data-ttu-id="87eeb-131">En el cuerpo de la solicitud, especifique una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="87eeb-131">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="87eeb-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="87eeb-132">Response</span></span>

<span data-ttu-id="87eeb-133">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="87eeb-133">If successful, this method returns `201 Created` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="87eeb-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="87eeb-134">Example</span></span>

##### <a name="request"></a><span data-ttu-id="87eeb-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="87eeb-135">Request</span></span>

<span data-ttu-id="87eeb-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="87eeb-136">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_calendar_from_calendargroup"
}-->

```http
POST https://graph.microsoft.com/beta/me/calendarGroups/{id}/calendars
Content-type: application/json
Content-length: 78

{
  "name": "name-value",
  "color": {
  }
}
```

<span data-ttu-id="87eeb-137">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="87eeb-137">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="87eeb-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="87eeb-138">Response</span></span>

<span data-ttu-id="87eeb-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="87eeb-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 98

{
  "name": "name-value",
  "color": {
  },
  "changeKey": "changeKey-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "Create Calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
