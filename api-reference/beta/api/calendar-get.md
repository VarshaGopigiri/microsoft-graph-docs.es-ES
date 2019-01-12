---
title: Obtener calendario
description: 'Obtiene las propiedades y relaciones de un objeto de calendario. El calendario puede ser una de un usuario '
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: d54d408966e359a99c16c91113ea5ba7eebb3d1d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990635"
---
# <a name="get-calendar"></a><span data-ttu-id="610d9-104">Obtener calendario</span><span class="sxs-lookup"><span data-stu-id="610d9-104">Get calendar</span></span>

> <span data-ttu-id="610d9-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="610d9-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="610d9-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="610d9-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="610d9-107">Obtiene las propiedades y relaciones de un objeto de [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="610d9-107">Get the properties and relationships of a [calendar](../resources/calendar.md) object.</span></span> <span data-ttu-id="610d9-108">El calendario puede ser de un [usuario](../resources/user.md) o el calendario predeterminado de un [grupo](../resources/group.md) de Office 365.</span><span class="sxs-lookup"><span data-stu-id="610d9-108">The calendar can be one for a [user](../resources/user.md), or the default calendar of an Office 365 [group](../resources/group.md).</span></span>

<span data-ttu-id="610d9-109">Hay dos escenarios donde una aplicación puede obtener el calendario de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="610d9-109">There are two scenarios where an app can get another user's calendar:</span></span>

* <span data-ttu-id="610d9-110">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="610d9-110">If the app has application permissions, or,</span></span>
* <span data-ttu-id="610d9-111">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido un calendario con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="610d9-111">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a calendar with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="610d9-112">Consulte los [Detalles y un ejemplo](/graph/outlook-get-shared-events-calendars).</span><span class="sxs-lookup"><span data-stu-id="610d9-112">See [details and an example](/graph/outlook-get-shared-events-calendars).</span></span>


## <a name="permissions"></a><span data-ttu-id="610d9-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="610d9-113">Permissions</span></span>
<span data-ttu-id="610d9-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="610d9-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="610d9-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="610d9-116">Permission type</span></span>      | <span data-ttu-id="610d9-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="610d9-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="610d9-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="610d9-118">Delegated (work or school account)</span></span> | <span data-ttu-id="610d9-119">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="610d9-119">Calendars.Read</span></span>    |
|<span data-ttu-id="610d9-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="610d9-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="610d9-121">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="610d9-121">Calendars.Read</span></span>    |
|<span data-ttu-id="610d9-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="610d9-122">Application</span></span> | <span data-ttu-id="610d9-123">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="610d9-123">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="610d9-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="610d9-124">HTTP request</span></span>
<span data-ttu-id="610d9-125"><!-- { "blockType": "ignored" } -->Un usuario o del grupo predeterminado de [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="610d9-125"><!-- { "blockType": "ignored" } --> A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
GET /me/calendar
GET /users/{id | userPrincipalName}/calendar
GET /groups/{id}/calendar
```
<span data-ttu-id="610d9-126">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="610d9-126">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendars/{id}
GET /users/{id | userPrincipalName}/calendars/{id}

GET /me/calendarGroup/calendars/{id}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="610d9-127">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="610d9-127">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendarGroups/{id}/calendars/{id}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="610d9-128">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="610d9-128">Optional query parameters</span></span>
<span data-ttu-id="610d9-129">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="610d9-129">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="610d9-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="610d9-130">Request headers</span></span>
| <span data-ttu-id="610d9-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="610d9-131">Name</span></span>       | <span data-ttu-id="610d9-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="610d9-132">Type</span></span> | <span data-ttu-id="610d9-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="610d9-133">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="610d9-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="610d9-134">Authorization</span></span>  | <span data-ttu-id="610d9-135">string</span><span class="sxs-lookup"><span data-stu-id="610d9-135">string</span></span>  | <span data-ttu-id="610d9-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="610d9-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="610d9-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="610d9-138">Request body</span></span>
<span data-ttu-id="610d9-139">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="610d9-139">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="610d9-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="610d9-140">Response</span></span>

<span data-ttu-id="610d9-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="610d9-141">If successful, this method returns a `200 OK` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="610d9-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="610d9-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="610d9-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="610d9-143">Request</span></span>
<span data-ttu-id="610d9-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="610d9-144">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_calendar"
}-->
```http
GET https://graph.microsoft.com/beta/me/calendar
```

##### <a name="response"></a><span data-ttu-id="610d9-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="610d9-145">Response</span></span>
<span data-ttu-id="610d9-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="610d9-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#me/calendars/$entity",
    "@odata.id": "https://graph.microsoft.com/beta/users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/calendars('AAMkAGI2TGuLAAA=')",
    "id": "AAMkAGI2TGuLAAA=",
    "name": "Calendar",
    "color": "auto",
    "isDefaultCalendar": false,
    "changeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+w==",
    "canShare":true,
    "canViewPrivateItems":true,
    "hexColor": "",
    "isShared":false,
    "isSharedWithMe":false,
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
