---
title: Agregar datos adjuntos
description: Utilice esta API para agregar datos adjuntos a un evento. Desde allí
ms.openlocfilehash: 6a5d07c8cbbeab6895a38d915c2fcdfa9e2e5c50
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085329"
---
# <a name="add-attachment"></a><span data-ttu-id="8ed2c-104">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="8ed2c-104">Add attachment</span></span>

> <span data-ttu-id="8ed2c-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8ed2c-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8ed2c-p103">Use esta API para agregar un objeto [attachment](../resources/attachment.md) a un evento. Puesto que actualmente hay un límite de 4 MB en el tamaño total de cada solicitud REST, esto limita el tamaño de los datos adjuntos que agregar a menos de 4 MB.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-p103">Use this API to add an [attachment](../resources/attachment.md) to an event. Since there is currently a limit of 4MB on the total size of each REST request, this limits the size of the attachment you can add to under 4MB.</span></span>
## <a name="permissions"></a><span data-ttu-id="8ed2c-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="8ed2c-109">Permissions</span></span>
<span data-ttu-id="8ed2c-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8ed2c-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8ed2c-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8ed2c-112">Permission type</span></span>      | <span data-ttu-id="8ed2c-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8ed2c-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8ed2c-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8ed2c-114">Delegated (work or school account)</span></span> | <span data-ttu-id="8ed2c-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8ed2c-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="8ed2c-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8ed2c-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8ed2c-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8ed2c-117">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="8ed2c-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8ed2c-118">Application</span></span> | <span data-ttu-id="8ed2c-119">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8ed2c-119">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="8ed2c-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8ed2c-120">HTTP request</span></span>
<span data-ttu-id="8ed2c-121">Los datos adjuntos para un [evento](../resources/event.md) en el usuario de forma predeterminada [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="8ed2c-121">Attachments for an [event](../resources/event.md) in the user's default [calendar](../resources/calendar.md).</span></span>

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

<span data-ttu-id="8ed2c-122">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-122">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/calendars/{id}/events/{id}/attachments
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments

POST /me/calendargroup/calendars/{id}/events/{id}/attachments
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments
```
<span data-ttu-id="8ed2c-123">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-123">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments
```
## <a name="request-headers"></a><span data-ttu-id="8ed2c-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8ed2c-124">Request headers</span></span>
| <span data-ttu-id="8ed2c-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="8ed2c-125">Name</span></span>       | <span data-ttu-id="8ed2c-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ed2c-126">Type</span></span> | <span data-ttu-id="8ed2c-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ed2c-127">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="8ed2c-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="8ed2c-128">Authorization</span></span>  | <span data-ttu-id="8ed2c-129">string</span><span class="sxs-lookup"><span data-stu-id="8ed2c-129">string</span></span>  | <span data-ttu-id="8ed2c-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8ed2c-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8ed2c-132">Content-Type</span></span> | <span data-ttu-id="8ed2c-133">string</span><span class="sxs-lookup"><span data-stu-id="8ed2c-133">string</span></span>  | <span data-ttu-id="8ed2c-p106">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-p106">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8ed2c-136">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="8ed2c-136">Request body</span></span>
<span data-ttu-id="8ed2c-137">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="8ed2c-137">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="8ed2c-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ed2c-138">Response</span></span>

<span data-ttu-id="8ed2c-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-139">If successful, this method returns `201 Created` response code and [attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="8ed2c-140">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="8ed2c-140">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="8ed2c-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8ed2c-141">Request</span></span>
<span data-ttu-id="8ed2c-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_file_attachment_from_event"
}-->
```http
POST https://graph.microsoft.com/beta/me/events('AAMkAGI1AAAt9AHjAAA=')/attachments 
Content-type: application/json
Content-length: 151

{
    "@odata.type": "#microsoft.graph.fileAttachment",
    "name": "menu.txt",
    "contentBytes": "bWFjIGFuZCBjaGVlc2UgdG9kYXk="   
}
```

<span data-ttu-id="8ed2c-143">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="8ed2c-143">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="8ed2c-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ed2c-144">Response</span></span>
<span data-ttu-id="8ed2c-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP 201 Created
Content-Length: 735

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('cd209b0b-3f83-4c35-82d2-d88a61820480')/events('AAMkAGI1AAAt9AHjAAA%3D')/attachments/$entity",
    "@odata.type":"#microsoft.graph.fileAttachment",
    "id":"AAMkAGI1AAAt9AHjAAABEgAQAEdBogju-MJEu6Ngg-1_W0g=",
    "lastModifiedDateTime":"2017-04-15T03:21:49Z",
    "name":"menu.txt",
    "contentType":"text/plain",
    "size":178,
    "isInline":false,
    "contentId":null,
    "contentLocation":null,
    "contentBytes":"bWFjIGFuZCBjaGVlc2UgdG9kYXk="
}
```

## <a name="example-item-attachment"></a><span data-ttu-id="8ed2c-148">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="8ed2c-148">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="8ed2c-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8ed2c-149">Request</span></span>

<span data-ttu-id="8ed2c-150">Este es un ejemplo que adjunta un evento con otro evento como datos adjuntos del elemento.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-150">Here is an example which attaches an event with another event as an item attachment.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_item_attachment_from_event"
}-->
```http
POST https://graph.microsoft.com/beta/me/events/{AAMkAGI1AAAt9AHjAAA=}/attachments
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

##### <a name="response"></a><span data-ttu-id="8ed2c-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ed2c-151">Response</span></span>
<span data-ttu-id="8ed2c-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#me/events('AAMkAGI1AAAt9AHjAAA=')/attachments/$entity",
    "@odata.type":"#microsoft.graph.itemAttachment",
    "@odata.id":"https://graph.microsoft.com/beta/users('fdcbcf34-2505-4d07-be5b-0a55b699d157@41a5b830-45ac-4f1b-9bfc-baafa3b7db2e')/events('AAMkAGI1AAAt9AHjAAA=')/attachments('AAMkADNkN2Jp5JVnQIe9r0=')",
    "id":"AAMkADNkNJp5JVnQIe9r0=",
    "lastModifiedDateTime":"2016-12-01T22:27:13Z",
    "name":"Holiday event",
    "contentType":null,
    "size":2473,
    "isInline":false
}
```

## <a name="example-reference-attachment"></a><span data-ttu-id="8ed2c-155">Ejemplo (datos adjuntos de referencia)</span><span class="sxs-lookup"><span data-stu-id="8ed2c-155">Example (reference attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="8ed2c-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8ed2c-156">Request</span></span>
<span data-ttu-id="8ed2c-157">Este es un ejemplo de una solicitud que agrega un dato adjunto de referencia a un evento existente.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-157">Here is an example of a request that adds a reference attachment to an existing event.</span></span>
<span data-ttu-id="8ed2c-158">Los puntos de datos adjuntos en una carpeta de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-158">The attachment points to a folder on OneDrive.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_reference_attachment_from_event",
  "@odata.type": "microsoft.graph.referenceAttachment"
}-->

```
POST https://graph.microsoft.com/beta/me/events/AAMkAGE1M88AADUv0uAAAG=/attachments
Content-type: application/json
Content-length: 319

{ 
    "@odata.type": "#microsoft.graph.referenceAttachment", 
    "name": "Personal pictures", 
    "sourceUrl": "https://contoso.com/personal/mario_contoso_net/Documents/Pics", 
    "providerType": "oneDriveConsumer", 
    "permission": "Edit", 
    "isFolder": "True" 
} 
```

##### <a name="response"></a><span data-ttu-id="8ed2c-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ed2c-159">Response</span></span>
<span data-ttu-id="8ed2c-160">Este es un ejemplo de una respuesta completa.</span><span class="sxs-lookup"><span data-stu-id="8ed2c-160">Here is an example of a full response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.referenceAttachment"
} -->
```http
HTTP 201 Created

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#users/ddfcd489-628b-40d7-b48b-57002df800e5/events/AAMkAGE1M88AADUv0uAAAG%3D/attachments/$entity",
  "@odata.type": "#microsoft.graph.referenceAttachment",
  "id": "AAMkAGE1Mg72tgf7hJp0PCGVCIc0g=",
  "lastModifiedDateTime": "2016-03-12T06:04:38Z",
  "name": "Personal pictures",
  "contentType": null,
  "size": 382,
  "isInline": false,
  "sourceUrl": "https://contoso.com/personal/mario_contoso_net/Documents/Pics",
  "providerType": "oneDriveConsumer",
  "thumbnailUrl": null,
  "previewUrl": null,
  "permission": "edit",
  "isFolder": true
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
