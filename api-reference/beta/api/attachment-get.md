---
title: Obtener datos adjuntos
description: 'Leer las propiedades y relaciones de los datos adjuntos, adjunto a un evento '
ms.openlocfilehash: a432e4f3fb98062a701e4c6e7b177145faa65e1e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084701"
---
# <a name="get-attachment"></a><span data-ttu-id="9e7e8-103">Obtener datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="9e7e8-103">Get attachment</span></span>

> <span data-ttu-id="9e7e8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9e7e8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9e7e8-106">Lea las propiedades y relaciones de los datos adjuntos, conectado a un [evento](../resources/event.md), [mensaje](../resources/message.md), [tarea de Outlook](../resources/outlooktask.md)o [registrar](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="9e7e8-106">Read the properties and relationships of an attachment, attached to an [event](../resources/event.md), [message](../resources/message.md), [Outlook task](../resources/outlooktask.md), or [post](../resources/post.md).</span></span> 

<span data-ttu-id="9e7e8-107">Los datos adjuntos pueden ser de uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9e7e8-107">An attachment can be one of the following types:</span></span>

* <span data-ttu-id="9e7e8-108">Un archivo (recurso [fileAttachment](../resources/fileattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="9e7e8-108">A file ([fileAttachment](../resources/fileattachment.md) resource).</span></span>
* <span data-ttu-id="9e7e8-p102">Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md)). Puede usar `$expand` para obtener más propiedades del elemento. Vea un [ejemplo](#request-2) abajo.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-p102">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource). You can use `$expand` to further get the properties of that item. See an [example](#request-2) below.</span></span>
* <span data-ttu-id="9e7e8-112">Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="9e7e8-112">A link to a file ([referenceAttachment](../resources/referenceattachment.md) resource).</span></span>

<span data-ttu-id="9e7e8-113">Todos estos tipos de recursos de datos adjuntos se derivan del recurso [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="9e7e8-113">All these types of attachment resources are derived from the [attachment](../resources/attachment.md) resource.</span></span> 

## <a name="permissions"></a><span data-ttu-id="9e7e8-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="9e7e8-114">Permissions</span></span>
<span data-ttu-id="9e7e8-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9e7e8-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

* <span data-ttu-id="9e7e8-117">Si obtiene acceso a los datos adjuntos en los mensajes: Mail.Read</span><span class="sxs-lookup"><span data-stu-id="9e7e8-117">If accessing attachments in messages: Mail.Read</span></span>
* <span data-ttu-id="9e7e8-118">Si obtiene acceso a los datos adjuntos en eventos: Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="9e7e8-118">If accessing attachments in events: Calendars.Read</span></span>
* <span data-ttu-id="9e7e8-119">Si obtiene acceso a los datos adjuntos en las tareas de Outlook: Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="9e7e8-119">If accessing attachments in Outlook tasks: Tasks.Read</span></span>
* <span data-ttu-id="9e7e8-120">Si obtiene acceso a los datos adjuntos en entradas de grupo: Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="9e7e8-120">If accessing attachments in group posts: Group.Read.All</span></span>
<!--
* If accessing attachments in group events or posts: Group.Read.All
-->

## <a name="http-request"></a><span data-ttu-id="9e7e8-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9e7e8-121">HTTP request</span></span>
<span data-ttu-id="9e7e8-122">Los datos adjuntos para un [evento](../resources/event.md) en el usuario de forma predeterminada [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="9e7e8-122">Attachments for an [event](../resources/event.md) in the user's default [calendar](../resources/calendar.md).</span></span>

<!--
Attachments for an [event](../resources/event.md) in the user's or group's default [calendar](../resources/calendar.md).
-->
<!-- { "blockType": "ignored" } -->
```http
GET /me/events/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/events/{id}/attachments/{id}

GET /me/calendar/{id}/events/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/calendar/events/{id}/attachments/{id}
```

<!--
GET /groups/{id}/events/{id}/attachments/{id}
GET /groups/{id}/calendar/events/{id}/attachments/{id}
-->

<span data-ttu-id="9e7e8-123">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-123">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}/events/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments/{id}

GET /me/calendargroup/calendars/{id}/events/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="9e7e8-124">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-124">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="9e7e8-125">Datos adjuntos de un [message](../resources/message.md) en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-125">Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/messages/{id}/attachments/{id}
```
<span data-ttu-id="9e7e8-126">Datos adjuntos de un [message](../resources/message.md) contenido en una [mailFolder](../resources/mailfolder.md) de nivel superior en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-126">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/messages/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments/{id}
```
<span data-ttu-id="9e7e8-127">Datos adjuntos de un [mensaje de](../resources/message.md) contenidos en una carpeta secundaria de un [mailFolder](../resources/mailfolder.md) en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-127">Attachments for a [message](../resources/message.md) contained in a child folder of a [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>  <span data-ttu-id="9e7e8-128">En el ejemplo siguiente se muestra un nivel de anidamiento, pero un mensaje puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-128">The example below shows one level of nesting, but a message can be located in a child of a child and so on.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```

<span data-ttu-id="9e7e8-129">Datos adjuntos para una [tarea de Outlook](../resources/outlooktask.md) en el buzón del usuario, o en un grupo de tareas o la carpeta de la tarea especificada.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-129">Attachments for an [Outlook task](../resources/outlooktask.md) in the user's mailbox, or in a specified task folder or task group.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/tasks/<id>/attachments/{id}
GET /users/<id>/outlook/tasks/<id>/attachments/{id}

GET /me/outlook/taskFolders/<id>/tasks/<id>/attachments/{id}
GET /users/<id>/outlook/taskFolders/<id>/tasks/<id>/attachments/{id}

GET /me/outlook/taskGroups/<id>/taskFolders/<id>/tasks/<id>/attachments/{id}
GET /users/<id>/outlook/taskGroups/<id>/taskFolders/<id>/tasks/<id>/attachments/{id}
```

<span data-ttu-id="9e7e8-130">Datos adjuntos para un [post](../resources/post.md) de un [thread](../resources/conversationthread.md) perteneciente a una [conversation](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-130">Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts/{id}/attachments/{id}
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="9e7e8-131">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9e7e8-131">Optional query parameters</span></span>
<span data-ttu-id="9e7e8-132">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-132">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="9e7e8-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9e7e8-133">Request headers</span></span>
| <span data-ttu-id="9e7e8-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="9e7e8-134">Name</span></span>       | <span data-ttu-id="9e7e8-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="9e7e8-135">Type</span></span> | <span data-ttu-id="9e7e8-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e7e8-136">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="9e7e8-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="9e7e8-137">Authorization</span></span>  | <span data-ttu-id="9e7e8-138">string</span><span class="sxs-lookup"><span data-stu-id="9e7e8-138">string</span></span>  | <span data-ttu-id="9e7e8-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9e7e8-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9e7e8-141">Request body</span></span>
<span data-ttu-id="9e7e8-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9e7e8-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9e7e8-143">Response</span></span>

<span data-ttu-id="9e7e8-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-144">If successful, this method returns a `200 OK` response code and [attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="9e7e8-145">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="9e7e8-145">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="9e7e8-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9e7e8-146">Request</span></span>
<span data-ttu-id="9e7e8-147">Este es un ejemplo de la solicitud para obtener un archivo adjunto en un evento.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-147">Here is an example of the request to get a file attachment on an event.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_file_attachment"
}-->
```http
GET https://graph.microsoft.com/beta/me/events/{id}/attachments/{id}
```

##### <a name="response"></a><span data-ttu-id="9e7e8-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9e7e8-148">Response</span></span>
<span data-ttu-id="9e7e8-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.fileAttachment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 199

{
  "@odata.type": "#microsoft.graph.fileAttachment",
  "contentType": "contentType-value",
  "contentLocation": "contentLocation-value",
  "contentBytes": "contentBytes-value",
  "contentId": "null",
  "lastModifiedDateTime": "2016-01-01T12:00:00Z",
  "id": "id-value",
  "isInline": false,
  "name": "name-value",
  "size": 99
}
```
## <a name="example-item-attachment"></a><span data-ttu-id="9e7e8-152">Ejemplo (datos adjuntos de elemento)</span><span class="sxs-lookup"><span data-stu-id="9e7e8-152">Example (item attachment)</span></span>

##### <a name="request-1"></a><span data-ttu-id="9e7e8-153">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="9e7e8-153">Request 1</span></span>
<span data-ttu-id="9e7e8-p107">En el primer ejemplo se muestra cómo obtener los datos adjuntos de elemento de un mensaje. Se devuelven las propiedades de **itemAttachment**.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-p107">The first example shows how to get an item attachment on a message. The properties of the **itemAttachment** are returned.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_item_attachment"
}-->
```http
GET https://graph.microsoft.com/beta/me/messages('AAMkADA1M-zAAA=')/attachments('AAMkADA1M-CJKtzmnlcqVgqI=')
```

##### <a name="response-1"></a><span data-ttu-id="9e7e8-156">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="9e7e8-156">Response 1</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.itemAttachment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('d1a2fae9-db66-4cc9-8133-2184c77af1b8')/messages('AAMkADA1M-zAAA%3D')/attachments/$entity",
  "@odata.type":"#microsoft.graph.itemAttachment",
  "id":"AAMkADA1MCJKtzmnlcqVgqI=",
  "lastModifiedDateTime":"2017-07-21T00:20:34Z",
  "name":"Reminder - please bring laptop",
  "contentType":null,
  "size":32005,
  "isInline":false
}
```


##### <a name="request-2"></a><span data-ttu-id="9e7e8-157">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="9e7e8-157">Request 2</span></span>
<span data-ttu-id="9e7e8-p108">En el ejemplo siguiente se muestra cómo usar `$expand` para obtener las propiedades del elemento adjunto al mensaje. En este ejemplo, el elemento es un mensaje; también se devuelven las propiedades del mensaje adjunto.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-p108">The next example shows how to use `$expand` to get the properties of the item that is attached to the message. In this example, that item is a message; the properties of that attached message are also returned.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_and_expand_item_attachment"
}-->
```http
GET https://graph.microsoft.com/beta/me/messages('AAMkADA1M-zAAA=')/attachments('AAMkADA1M-CJKtzmnlcqVgqI=')/?$expand=microsoft.graph.itemattachment/item 
```

##### <a name="response-2"></a><span data-ttu-id="9e7e8-160">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="9e7e8-160">Response 2</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.itemAttachment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('d1a2fae9-db66-4cc9-8133-2184c77af1b8')/messages('AAMkADA1M-zAAA%3D')/attachments/$entity",
  "@odata.type":"#microsoft.graph.itemAttachment",
  "id":"AAMkADA1MCJKtzmnlcqVgqI=",
  "lastModifiedDateTime":"2017-07-21T00:20:34Z",
  "name":"Reminder - please bring laptop",
  "contentType":null,
  "size":32005,
  "isInline":false,
  "item@odata.context":"https://graph.microsoft.com/beta/$metadata#users('d1a2fae9-db66-4cc9-8133-2184c77af1b8')/messages('AAMkADA1M-zAAA%3D')/attachments('AAMkADA1M-CJKtzmnlcqVgqI%3D')/microsoft.graph.itemAttachment/item/$entity",
  "item":{
    "@odata.type":"#microsoft.graph.message",
    "id":"",
    "createdDateTime":"2017-07-21T00:20:41Z",
    "lastModifiedDateTime":"2017-07-21T00:20:34Z",
    "receivedDateTime":"2017-07-21T00:19:55Z",
    "sentDateTime":"2017-07-21T00:19:52Z",
    "hasAttachments":false,
    "internetMessageId":"<BY2PR15MB05189A084C01F466709E414F9CA40@BY2PR15MB0518.namprd15.prod.outlook.com>",
    "subject":"Reminder - please bring laptop",
    "importance":"normal",
    "conversationId":"AAQkADA1MzMyOGI4LTlkZDctNDkzYy05M2RiLTdiN2E1NDE3MTRkOQAQAMG_NSCMBqdKrLa2EmR-lO0=",
    "conversationIndex":"AQHTAbcSwb41IIwGp0qstrYSZH+U7Q==",
    "isDeliveryReceiptRequested":false,
    "isReadReceiptRequested":false,
    "isRead":false,
    "isDraft":false,
    "webLink":"https://outlook.office365.com/owa/?ItemID=AAMkADA1M3MTRkOQAAAA%3D%3D&exvsurl=1&viewmodel=ReadMessageItem",
    "body":{
      "contentType":"html",
      "content":"<html><head>\r\n</head>\r\n<body>\r\n</body>\r\n</html>"
    },
    "sender":{
      "emailAddress":{
        "name":"Adele Vance",
        "address":"AdeleV@contoso.onmicrosoft.com"
      }
    },
    "from":{
      "emailAddress":{
        "name":"Adele Vance",
        "address":"AdeleV@contoso.onmicrosoft.com"
      }
    },
    "toRecipients":[
      {
        "emailAddress":{
          "name":"Alex Wilbur",
          "address":"AlexW@contoso.onmicrosoft.com"
        }
      }
    ],
    "ccRecipients":[
      {
        "emailAddress":{
          "name":"Adele Vance",
          "address":"AdeleV@contoso.onmicrosoft.com"
        }
      }
    ],
    "flag":{
      "flagStatus":"notFlagged"
    }
  }
}
```


## <a name="example-reference-attachment"></a><span data-ttu-id="9e7e8-161">Ejemplo (datos adjuntos de referencia)</span><span class="sxs-lookup"><span data-stu-id="9e7e8-161">Example (reference attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="9e7e8-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9e7e8-162">Request</span></span>
<span data-ttu-id="9e7e8-163">Este es un ejemplo de la solicitud para obtener un archivo adjunto de referencia en un evento.</span><span class="sxs-lookup"><span data-stu-id="9e7e8-163">Here is an example of the request to get a reference attachment on an event.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_reference_attachment"
}-->
```http
GET https://graph.microsoft.com/beta/me/events/AAMkAGE1M88AADUv0uAAAG=/attachments/AAMkAGE1Mg72tgf7hJp0PICVGCc0g=
```

##### <a name="response"></a><span data-ttu-id="9e7e8-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9e7e8-164">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.referenceAttachment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

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
  "description": "Get attachment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
