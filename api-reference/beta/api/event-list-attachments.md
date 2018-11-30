---
title: List attachments
description: Recupera una lista de objetos attachment asociados a un evento.
ms.openlocfilehash: cc632ab14bf2c64628cdf5177da5601f4b04f4d0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084647"
---
# <a name="list-attachments"></a><span data-ttu-id="e5c84-103">List attachments</span><span class="sxs-lookup"><span data-stu-id="e5c84-103">List attachments</span></span>

> <span data-ttu-id="e5c84-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e5c84-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e5c84-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e5c84-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e5c84-106">Recupera una lista de objetos [attachment](../resources/attachment.md) asociados a un evento.</span><span class="sxs-lookup"><span data-stu-id="e5c84-106">Retrieve a list of [attachment](../resources/attachment.md) objects attached to an event.</span></span>

## <a name="permissions"></a><span data-ttu-id="e5c84-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e5c84-107">Permissions</span></span>
<span data-ttu-id="e5c84-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e5c84-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e5c84-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e5c84-110">Permission type</span></span>      | <span data-ttu-id="e5c84-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e5c84-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e5c84-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e5c84-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e5c84-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="e5c84-113">Calendars.Read</span></span>    |
|<span data-ttu-id="e5c84-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e5c84-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e5c84-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="e5c84-115">Calendars.Read</span></span>    |
|<span data-ttu-id="e5c84-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e5c84-116">Application</span></span> | <span data-ttu-id="e5c84-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="e5c84-117">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="e5c84-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e5c84-118">HTTP request</span></span>
<span data-ttu-id="e5c84-119">Los datos adjuntos para un [evento](../resources/event.md) en el usuario de forma predeterminada [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="e5c84-119">Attachments for an [event](../resources/event.md) in the user's default [calendar](../resources/calendar.md).</span></span>

<!--
Attachments for an [event](../resources/event.md) in the user's or group's default [calendar](../resources/calendar.md).
-->
<!-- { "blockType": "ignored" } -->
```http
GET /me/events/{id}/attachments
GET /users/{id | userPrincipalName}/events/{id}/attachments

GET /me/calendar/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendar/events/{id}/attachments
```

<!--
GET /groups/{id}/events/{id}/attachments
GET /groups/{id}/calendar/events/{id}/attachments
-->

<span data-ttu-id="e5c84-120">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="e5c84-120">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments

GET /me/calendargroup/calendars/{id}/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments
```
<span data-ttu-id="e5c84-121">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="e5c84-121">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e5c84-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e5c84-122">Optional query parameters</span></span>
<span data-ttu-id="e5c84-123">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5c84-123">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="e5c84-124">En concreto, puede usar el $expanda parámetro de consulta para incluir todos los datos adjuntos de (evento) en línea con el resto de las propiedades de evento.</span><span class="sxs-lookup"><span data-stu-id="e5c84-124">In particular, you can use the $expand query parameter to include all of the event attachments inline with the rest of the event properties.</span></span> <span data-ttu-id="e5c84-125">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e5c84-125">For example:</span></span>

```
GET https://graph.microsoft.com/beta/me/events/{id}?$expand=attachments
```


## <a name="request-headers"></a><span data-ttu-id="e5c84-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5c84-126">Request headers</span></span>
| <span data-ttu-id="e5c84-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="e5c84-127">Name</span></span>       | <span data-ttu-id="e5c84-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5c84-128">Type</span></span> | <span data-ttu-id="e5c84-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5c84-129">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e5c84-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="e5c84-130">Authorization</span></span>  | <span data-ttu-id="e5c84-131">string</span><span class="sxs-lookup"><span data-stu-id="e5c84-131">string</span></span>  | <span data-ttu-id="e5c84-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e5c84-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e5c84-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e5c84-134">Request body</span></span>
<span data-ttu-id="e5c84-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e5c84-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e5c84-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5c84-136">Response</span></span>

<span data-ttu-id="e5c84-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5c84-137">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e5c84-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5c84-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e5c84-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e5c84-139">Request</span></span>
<span data-ttu-id="e5c84-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5c84-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/beta/me/events/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="e5c84-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5c84-141">Response</span></span>
<span data-ttu-id="e5c84-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e5c84-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "value": [
    {
      "@odata.type": "#Microsoft.OutlookServices.FileAttachment",
      "contentType": "contentType-value",
      "contentLocation": "contentLocation-value",
      "contentBytes": "contentBytes-value",
      "contentId": "null",
      "lastModifiedDateTime": "2016-10-19T10:37:00Z",
      "id": "id-value",
      "isInline": false,
      "isContactPhoto": false,
      "name": "name-value",
      "size": 99
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List attachments",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->