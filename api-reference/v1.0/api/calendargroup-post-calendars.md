---
title: Create Calendar
description: Use esta API para crear un calendario en un grupo de calendarios para un usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: cdb24b32bfd23cf5c6c6cf41673b4f8fa0ff61dc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806940"
---
# <a name="create-calendar"></a><span data-ttu-id="88c5f-103">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="88c5f-103">Create Calendar</span></span>

<span data-ttu-id="88c5f-104">Use esta API para crear un calendario en un grupo de calendarios para un [usuario](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="88c5f-104">Use this API to create a new calendar in a calendar group for a [user](../resources/user.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="88c5f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="88c5f-105">Permissions</span></span>

<span data-ttu-id="88c5f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="88c5f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="88c5f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="88c5f-108">Permission type</span></span>                        | <span data-ttu-id="88c5f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="88c5f-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="88c5f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="88c5f-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="88c5f-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="88c5f-111">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="88c5f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="88c5f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="88c5f-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="88c5f-113">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="88c5f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="88c5f-114">Application</span></span>                            | <span data-ttu-id="88c5f-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="88c5f-115">Calendars.ReadWrite</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="88c5f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="88c5f-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

<span data-ttu-id="88c5f-117">[calendarGroup](../resources/calendargroup.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="88c5f-117">A user's default [calendarGroup](../resources/calendargroup.md).</span></span>

```http
POST /me/calendarGroup/calendars
POST /users/{id | userPrincipalName}/calendarGroup/calendars
```

<span data-ttu-id="88c5f-118">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="88c5f-118">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>

```http
POST /me/calendarGroups/{id}/calendars
POST /users/{id | userPrincipalName}/calendarGroups/{id}/calendars
```

## <a name="request-headers"></a><span data-ttu-id="88c5f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="88c5f-119">Request headers</span></span>

| <span data-ttu-id="88c5f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88c5f-120">Header</span></span>        | <span data-ttu-id="88c5f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="88c5f-121">Value</span></span>                       |
| :------------ | :-------------------------- |
| <span data-ttu-id="88c5f-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="88c5f-122">Authorization</span></span> | <span data-ttu-id="88c5f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="88c5f-p102">Bearer {token}. Required.</span></span>   |
| <span data-ttu-id="88c5f-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="88c5f-125">Content-Type</span></span>  | <span data-ttu-id="88c5f-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="88c5f-p103">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="88c5f-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="88c5f-128">Request body</span></span>

<span data-ttu-id="88c5f-129">En el cuerpo de la solicitud, especifique una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="88c5f-129">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="88c5f-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88c5f-130">Response</span></span>

<span data-ttu-id="88c5f-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88c5f-131">If successful, this method returns `201 Created` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="88c5f-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88c5f-132">Example</span></span>

##### <a name="request"></a><span data-ttu-id="88c5f-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="88c5f-133">Request</span></span>

<span data-ttu-id="88c5f-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88c5f-134">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_calendar_from_calendargroup"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/calendarGroups/{id}/calendars
Content-type: application/json
Content-length: 78

{
  "name": "name-value",
  "color": {
  }
}
```

<span data-ttu-id="88c5f-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="88c5f-135">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="88c5f-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88c5f-136">Response</span></span>

<span data-ttu-id="88c5f-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="88c5f-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
