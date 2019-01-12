---
title: Obtener calendario
description: 'Obtiene las propiedades y relaciones de un objeto de calendario. El calendario puede ser una de un usuario '
localization_priority: Priority
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 3b5f8ff95d6b8e77749acc4a7dececfb272e26dc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990449"
---
# <a name="get-calendar"></a><span data-ttu-id="6d9eb-104">Obtener calendario</span><span class="sxs-lookup"><span data-stu-id="6d9eb-104">Get calendar</span></span>

<span data-ttu-id="6d9eb-105">Obtiene las propiedades y relaciones de un objeto de [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="6d9eb-105">Get the properties and relationships of a [calendar](../resources/calendar.md) object.</span></span> <span data-ttu-id="6d9eb-106">El calendario puede ser de un [usuario](../resources/user.md) o el calendario predeterminado de un [grupo](../resources/group.md) de Office 365.</span><span class="sxs-lookup"><span data-stu-id="6d9eb-106">The calendar can be one for a [user](../resources/user.md), or the default calendar of an Office 365 [group](../resources/group.md).</span></span>

<span data-ttu-id="6d9eb-107">Hay dos escenarios donde una aplicación puede obtener el calendario de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="6d9eb-107">There are two scenarios where an app can get another user's calendar:</span></span>

* <span data-ttu-id="6d9eb-108">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="6d9eb-108">If the app has application permissions, or,</span></span>
* <span data-ttu-id="6d9eb-109">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido un calendario con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="6d9eb-109">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a calendar with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="6d9eb-110">Consulte los [Detalles y un ejemplo](/graph/outlook-get-shared-events-calendars).</span><span class="sxs-lookup"><span data-stu-id="6d9eb-110">See [details and an example](/graph/outlook-get-shared-events-calendars).</span></span>

## <a name="permissions"></a><span data-ttu-id="6d9eb-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="6d9eb-111">Permissions</span></span>
<span data-ttu-id="6d9eb-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6d9eb-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6d9eb-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6d9eb-114">Permission type</span></span>      | <span data-ttu-id="6d9eb-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6d9eb-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6d9eb-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6d9eb-116">Delegated (work or school account)</span></span> | <span data-ttu-id="6d9eb-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="6d9eb-117">Calendars.Read</span></span>    |
|<span data-ttu-id="6d9eb-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6d9eb-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6d9eb-119">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="6d9eb-119">Calendars.Read</span></span>    |
|<span data-ttu-id="6d9eb-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6d9eb-120">Application</span></span> | <span data-ttu-id="6d9eb-121">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="6d9eb-121">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="6d9eb-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6d9eb-122">HTTP request</span></span>
<span data-ttu-id="6d9eb-123"><!-- { "blockType": "ignored" } -->Un usuario o del grupo predeterminado de [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="6d9eb-123"><!-- { "blockType": "ignored" } --> A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
GET /me/calendar
GET /users/{id | userPrincipalName}/calendar
GET /groups/{id}/calendar
```
<span data-ttu-id="6d9eb-124">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6d9eb-124">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendars/{id}
GET /users/{id | userPrincipalName}/calendars/{id}

GET /me/calendarGroup/calendars/{id}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="6d9eb-125">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="6d9eb-125">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendarGroups/{id}/calendars/{id}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6d9eb-126">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6d9eb-126">Optional query parameters</span></span>
<span data-ttu-id="6d9eb-127">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d9eb-127">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="6d9eb-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6d9eb-128">Request headers</span></span>
| <span data-ttu-id="6d9eb-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="6d9eb-129">Name</span></span>       | <span data-ttu-id="6d9eb-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d9eb-130">Type</span></span> | <span data-ttu-id="6d9eb-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d9eb-131">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6d9eb-132">Autorización</span><span class="sxs-lookup"><span data-stu-id="6d9eb-132">Authorization</span></span>  | <span data-ttu-id="6d9eb-133">string</span><span class="sxs-lookup"><span data-stu-id="6d9eb-133">string</span></span>  | <span data-ttu-id="6d9eb-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6d9eb-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6d9eb-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6d9eb-136">Request body</span></span>
<span data-ttu-id="6d9eb-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6d9eb-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6d9eb-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d9eb-138">Response</span></span>

<span data-ttu-id="6d9eb-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d9eb-139">If successful, this method returns a `200 OK` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6d9eb-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d9eb-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6d9eb-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6d9eb-141">Request</span></span>
<span data-ttu-id="6d9eb-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d9eb-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendar"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendar
```
##### <a name="response"></a><span data-ttu-id="6d9eb-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d9eb-143">Response</span></span>
<span data-ttu-id="6d9eb-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6d9eb-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#me/calendars/$entity",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/calendars('AAMkAGI2TGuLAAA=')",
    "id": "AAMkAGI2TGuLAAA=",
    "name": "Calendar",
    "color": "auto",
    "changeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+w==",
    "canShare":true,
    "canViewPrivateItems":true,
    "canEdit":true,
    "owner":{
        "name":"Samantha Booth",
        "address":"samanthab@adatum.onmicrosoft.com"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
