---
title: Agregar datos adjuntos
description: Utilice esta API para agregar datos adjuntos a un evento. Desde allí
ms.openlocfilehash: e64a012738c0b742c83e6baa247746daaf16dcdf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031502"
---
# <a name="add-attachment"></a><span data-ttu-id="64a87-104">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="64a87-104">Add attachment</span></span>

<span data-ttu-id="64a87-p102">Use esta API para agregar un objeto [attachment](../resources/attachment.md) a un evento. Puesto que actualmente hay un límite de 4 MB en el tamaño total de cada solicitud REST, esto limita el tamaño de los datos adjuntos que agregar a menos de 4 MB.</span><span class="sxs-lookup"><span data-stu-id="64a87-p102">Use this API to add an [attachment](../resources/attachment.md) to an event. Since there is currently a limit of 4MB on the total size of each REST request, this limits the size of the attachment you can add to under 4MB.</span></span>
## <a name="permissions"></a><span data-ttu-id="64a87-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="64a87-107">Permissions</span></span>
<span data-ttu-id="64a87-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="64a87-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="64a87-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="64a87-110">Permission type</span></span>      | <span data-ttu-id="64a87-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="64a87-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="64a87-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="64a87-112">Delegated (work or school account)</span></span> | <span data-ttu-id="64a87-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="64a87-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="64a87-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="64a87-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="64a87-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="64a87-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="64a87-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="64a87-116">Application</span></span> | <span data-ttu-id="64a87-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="64a87-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="64a87-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="64a87-118">HTTP request</span></span>
<span data-ttu-id="64a87-119">Los datos adjuntos para un [evento](../resources/event.md) en el usuario de forma predeterminada [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="64a87-119">Attachments for an [event](../resources/event.md) in the user's default [calendar](../resources/calendar.md).</span></span>

<!--
Attachments for an [event](../resources/event.md) in the user's or group's default [calendar](../resources/calendar.md).
-->
<!-- { "blockType": "ignored" } -->
```http
POST /me/events/{id}/attachments
POST /users/{id | userPrincipalName}/events/{id}/attachments

POST /me/calendar/events/{id}/attachments
POST /users/{id | userPrincipalName}/calendar/events/{id}/attachments
```

<!--
POST /groups/{id}/events/{id}/attachments
POST /groups/{id}/calendar/events/{id}/attachments
-->

<span data-ttu-id="64a87-120">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="64a87-120">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/calendars/{id}/events/{id}/attachments
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments

POST /me/calendargroup/calendars/{id}/events/{id}/attachments
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments
```
<span data-ttu-id="64a87-121">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="64a87-121">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments
```
## <a name="request-headers"></a><span data-ttu-id="64a87-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="64a87-122">Request headers</span></span>
| <span data-ttu-id="64a87-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="64a87-123">Name</span></span>       | <span data-ttu-id="64a87-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="64a87-124">Type</span></span> | <span data-ttu-id="64a87-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="64a87-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="64a87-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="64a87-126">Authorization</span></span>  | <span data-ttu-id="64a87-127">string</span><span class="sxs-lookup"><span data-stu-id="64a87-127">string</span></span>  | <span data-ttu-id="64a87-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="64a87-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="64a87-130">Content-Type</span><span class="sxs-lookup"><span data-stu-id="64a87-130">Content-Type</span></span> | <span data-ttu-id="64a87-131">string</span><span class="sxs-lookup"><span data-stu-id="64a87-131">string</span></span>  | <span data-ttu-id="64a87-p105">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="64a87-p105">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="64a87-134">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="64a87-134">Request body</span></span>
<span data-ttu-id="64a87-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="64a87-135">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="64a87-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64a87-136">Response</span></span>

<span data-ttu-id="64a87-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64a87-137">If successful, this method returns `201 Created` response code and [attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="64a87-138">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="64a87-138">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="64a87-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="64a87-139">Request</span></span>
<span data-ttu-id="64a87-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64a87-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkAGI1AAAt9AHjAAA="],
  "name": "create_file_attachment_from_event"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/AAMkAGI1AAAt9AHjAAA=/attachments
Content-type: application/json
Content-length: 151

{
    "@odata.type": "#microsoft.graph.fileAttachment",
    "name": "menu.txt",
    "contentBytes": "base64bWFjIGFuZCBjaGVlc2UgdG9kYXk="   
}
```

<span data-ttu-id="64a87-141">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="64a87-141">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="64a87-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64a87-142">Response</span></span>
<span data-ttu-id="64a87-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64a87-143">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP 201 Created
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('cd209b0b-3f83-4c35-82d2-d88a61820480')/events('AAMkAGI1AAAt9AHjAAA%3D')/attachments/$entity",
    "@odata.type":"#microsoft.graph.fileAttachment",
    "id":"AAMkAGI1AAAt9AHjAAABEgAQAEdBogju-MJEu6Ngg-1_W0g=",
    "lastModifiedDateTime":"2017-04-15T03:21:49Z",
    "name":"menu.txt",
    "contentType":"text/plain",
    "size":178,
    "isInline":false,
    "contentId":null,
    "contentLocation":null,
    "contentBytes":"base64bWFjIGFuZCBjaGVlc2UgdG9kYXk="
}
```

## <a name="example-item-attachment"></a><span data-ttu-id="64a87-144">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="64a87-144">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="64a87-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="64a87-145">Request</span></span>

<span data-ttu-id="64a87-146">Este es un ejemplo que adjunta un evento con otro evento como datos adjuntos del elemento.</span><span class="sxs-lookup"><span data-stu-id="64a87-146">Here is an example which attaches an event with another event as an item attachment.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkAGI1AAAt9AHjAAA="],
  "name": "create_item_attachment_from_event"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/AAMkAGI1AAAt9AHjAAA=/attachments
Content-type: application/json
Content-length: 600

{
  "@odata.type": "#microsoft.graph.itemAttachment",
  "name": "Holiday event", 
  "item": {
        "@odata.type": "microsoft.graph.event",
        "subject": "Discuss gifts for children",
        "body": {
            "contentType": "HTML",
            "content": "Let's look for funding!"
         },
         "start": {
             "dateTime": "2016-12-02T18:00:00",
             "timeZone": "Pacific Standard Time"
          },
          "end": {
             "dateTime": "2016-12-02T19:00:00",
             "timeZone": "Pacific Standard Time"
          }
    }
}
```

##### <a name="response"></a><span data-ttu-id="64a87-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64a87-147">Response</span></span>
<span data-ttu-id="64a87-148">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64a87-148">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP 201 Created
Content-type: application/json
Content-length: 162

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#me/events('AAMkAGI1AAAt9AHjAAA=')/attachments/$entity",
    "@odata.type":"#microsoft.graph.itemAttachment",
    "@odata.id":"https://graph.microsoft.com/v1.0/users('fdcbcf34-2505-4d07-be5b-0a55b699d157@41a5b830-45ac-4f1b-9bfc-baafa3b7db2e')/events('AAMkAGI1AAAt9AHjAAA=')/attachments('AAMkADNkN2Jp5JVnQIe9r0=')",
    "id":"AAMkADNkNJp5JVnQIe9r0=",
    "lastModifiedDateTime":"2016-12-01T22:27:13Z",
    "name":"Holiday event",
    "contentType":null,
    "size":2473,
    "isInline":false
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Attachment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
