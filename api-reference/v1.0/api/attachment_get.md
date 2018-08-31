# <a name="get-attachment"></a><span data-ttu-id="cfd4c-101">Obtener datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="cfd4c-101">Get attachment</span></span>

<span data-ttu-id="cfd4c-102">Lea las propiedades y relaciones de un archivo adjunto, conectado a un [evento](../resources/event.md), [mensaje](../resources/message.md), o [publicación](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="cfd4c-102">Read the properties and relationships of an attachment, attached to an [event](../resources/event.md), [message](../resources/message.md), or [post](../resources/post.md).</span></span> 

<span data-ttu-id="cfd4c-103">Los datos adjuntos pueden ser de uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="cfd4c-103">An attachment can be one of the following types:</span></span>

* <span data-ttu-id="cfd4c-104">Un archivo (recurso [fileAttachment](../resources/fileattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="cfd4c-104">A file ([fileAttachment](../resources/fileattachment.md) resource).</span></span>
* <span data-ttu-id="cfd4c-p101">Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md)). Puede usar `$expand` para obtener más propiedades del elemento. Vea un [ejemplo](#request-2) abajo.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-p101">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource). You can use `$expand` to further get the properties of that item. See an [example](#request-2) below.</span></span>
* <span data-ttu-id="cfd4c-108">Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceAttachment.md)).</span><span class="sxs-lookup"><span data-stu-id="cfd4c-108">A link to a file ([referenceAttachment](../resources/referenceAttachment.md) resource).</span></span>

<span data-ttu-id="cfd4c-109">Todos estos tipos de recursos de datos adjuntos se derivan del recurso [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="cfd4c-109">All these types of attachment resources are derived from the [attachment](../resources/attachment.md) resource.</span></span> 


## <a name="permissions"></a><span data-ttu-id="cfd4c-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="cfd4c-110">Permissions</span></span>
<span data-ttu-id="cfd4c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cfd4c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

* <span data-ttu-id="cfd4c-113">Si accede a datos adjuntos de mensajes: Mail.Read.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-113">If accessing attachments in messages: Mail.Read.</span></span>
* <span data-ttu-id="cfd4c-114">Si accede a datos adjuntos de eventos: Calendars.Read.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-114">If accessing attachments in events: Calendars.Read.</span></span>
* <span data-ttu-id="cfd4c-115">Si accede a datos adjuntos de publicaciones de grupo: Group.Read.All.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-115">If accessing attachments in group events or posts: Group.Read.All.</span></span>

<!--
* If accessing attachments in group events or posts: Group.Read.All.
-->

## <a name="http-request"></a><span data-ttu-id="cfd4c-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cfd4c-116">HTTP request</span></span>
<span data-ttu-id="cfd4c-117">Datos adjuntos de un [event](../resources/event.md) en el [calendar](../resources/calendar.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-117">Attachments for an [event](../resources/event.md) in the user's or group's default [calendar](../resources/calendar.md).</span></span>

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

<span data-ttu-id="cfd4c-118">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-118">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}/events/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments/{id}

GET /me/calendargroup/calendars/{id}/events/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="cfd4c-119">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-119">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="cfd4c-120">Datos adjuntos de un [message](../resources/message.md) en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-120">Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/messages/{id}/attachments/{id}
```
<span data-ttu-id="cfd4c-121">Datos adjuntos de un [message](../resources/message.md) contenido en una [mailFolder](../resources/mailfolder.md) de nivel superior en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-121">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/messages/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments/{id}
```
<span data-ttu-id="cfd4c-122">Datos adjuntos de un [message](../resources/message.md) contenidos en una carpeta secundaria de una [mailFolder](../resources/mailfolder.md) en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-122">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>  <span data-ttu-id="cfd4c-123">En el ejemplo siguiente se muestra un nivel de anidamiento, pero un mensaje puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-123">A contact contained in a child folder of a contactFolder. The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```
<span data-ttu-id="cfd4c-124">Datos adjuntos para un [post](../resources/post.md) de un [thread](../resources/conversationthread.md) perteneciente a una [conversation](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-124">Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts/{id}/attachments/{id}
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="cfd4c-125">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="cfd4c-125">Optional query parameters</span></span>
<span data-ttu-id="cfd4c-126">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-126">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="cfd4c-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cfd4c-127">Request headers</span></span>
| <span data-ttu-id="cfd4c-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="cfd4c-128">Name</span></span>       | <span data-ttu-id="cfd4c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="cfd4c-129">Type</span></span> | <span data-ttu-id="cfd4c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="cfd4c-130">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="cfd4c-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="cfd4c-131">Authorization</span></span>  | <span data-ttu-id="cfd4c-132">cadena</span><span class="sxs-lookup"><span data-stu-id="cfd4c-132">string</span></span>  | <span data-ttu-id="cfd4c-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cfd4c-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cfd4c-135">Request body</span></span>
<span data-ttu-id="cfd4c-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-136">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cfd4c-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cfd4c-137">Response</span></span>

<span data-ttu-id="cfd4c-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto **attachment** en el cuerpo de la respuesta. Se devuelven las propiedades de ese tipo de datos adjuntos: [fileAttachment](../resources/fileattachment.md), [itemAttachment](../resources/itemattachment.md) o [referenceAttachment](../resources/referenceAttachment.md).</span><span class="sxs-lookup"><span data-stu-id="cfd4c-p105">If successful, this method returns a `200 OK` response code and an **attachment** object in the response body. The properties of that type of attachment are returned: [fileAttachment](../resources/fileattachment.md), [itemAttachment](../resources/itemattachment.md), or [referenceAttachment](../resources/referenceAttachment.md).</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="cfd4c-140">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="cfd4c-140">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="cfd4c-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cfd4c-141">Request</span></span>
<span data-ttu-id="cfd4c-142">Este es un ejemplo de la solicitud para obtener un archivo adjunto en un evento.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-142">Here is an example of the request to get a file attachment on an event.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_file_attachment"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events/{id}/attachments/{id}
```

##### <a name="response"></a><span data-ttu-id="cfd4c-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cfd4c-143">Response</span></span>
<span data-ttu-id="cfd4c-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "contentBytes": "binary",
  "contentId": "null",
  "lastModifiedDateTime": "2016-01-01T12:00:00Z",
  "id": "id-value",
  "isInline": false,
  "name": "name-value",
  "size": 99
}
```
## <a name="example-item-attachment"></a><span data-ttu-id="cfd4c-147">Ejemplo (datos adjuntos de elemento)</span><span class="sxs-lookup"><span data-stu-id="cfd4c-147">Example (item attachment)</span></span>

##### <a name="request-1"></a><span data-ttu-id="cfd4c-148">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="cfd4c-148">Request 1</span></span>
<span data-ttu-id="cfd4c-p107">En el primer ejemplo se muestra cómo obtener los datos adjuntos de elemento de un mensaje. Se devuelven las propiedades de **itemAttachment**.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-p107">The first example shows how to get an item attachment on a message. The properties of the **itemAttachment** are returned.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADA1M-zAAA=", "AAMkADA1M-CJKtzmnlcqVgqI="],
  "name": "get_item_attachment"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/AAMkADA1M-zAAA=/attachments/AAMkADA1M-CJKtzmnlcqVgqI=
```

##### <a name="response-1"></a><span data-ttu-id="cfd4c-151">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="cfd4c-151">Response 1</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.itemAttachment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('d1a2fae9-db66-4cc9-8133-2184c77af1b8')/messages('AAMkADA1M-zAAA%3D')/attachments/$entity",
  "@odata.type":"#microsoft.graph.itemAttachment",
  "id":"AAMkADA1MCJKtzmnlcqVgqI=",
  "lastModifiedDateTime":"2017-07-21T00:20:34Z",
  "name":"Reminder - please bring laptop",
  "contentType":null,
  "size":32005,
  "isInline":false
}
```

##### <a name="request-2"></a><span data-ttu-id="cfd4c-152">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="cfd4c-152">Request 2</span></span>
<span data-ttu-id="cfd4c-p108">En el ejemplo siguiente se muestra cómo usar `$expand` para obtener las propiedades del elemento adjunto al mensaje. En este ejemplo, el elemento es un mensaje; también se devuelven las propiedades del mensaje adjunto.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-p108">The next example shows how to use `$expand` to get the properties of the item that is attached to the message. In this example, that item is a message; the properties of that attached message are also returned.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADA1M-zAAA=", "AAMkADA1M-CJKtzmnlcqVgqI="],
  "name": "get_and_expand_item_attachment"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/AAMkADA1M-zAAA=/attachments/AAMkADA1M-CJKtzmnlcqVgqI=/?$expand=microsoft.graph.itemattachment/item 
```

##### <a name="response-2"></a><span data-ttu-id="cfd4c-155">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="cfd4c-155">Response 2</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.itemAttachment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('d1a2fae9-db66-4cc9-8133-2184c77af1b8')/messages('AAMkADA1M-zAAA%3D')/attachments/$entity",
  "@odata.type":"#microsoft.graph.itemAttachment",
  "id":"AAMkADA1MCJKtzmnlcqVgqI=",
  "lastModifiedDateTime":"2017-07-21T00:20:34Z",
  "name":"Reminder - please bring laptop",
  "contentType":null,
  "size":32005,
  "isInline":false,
  "item@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('d1a2fae9-db66-4cc9-8133-2184c77af1b8')/messages('AAMkADA1M-zAAA%3D')/attachments('AAMkADA1M-CJKtzmnlcqVgqI%3D')/microsoft.graph.itemAttachment/item/$entity",
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
    ]
  }
}
```



## <a name="example-reference-attachment"></a><span data-ttu-id="cfd4c-156">Ejemplo (datos adjuntos de referencia)</span><span class="sxs-lookup"><span data-stu-id="cfd4c-156">Example (reference attachment)</span></span>
##### <a name="request"></a><span data-ttu-id="cfd4c-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cfd4c-157">Request</span></span>
<span data-ttu-id="cfd4c-158">Este es un ejemplo de la solicitud para obtener un archivo adjunto de referencia en un evento.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-158">Here is an example of the request to get a reference attachment on an event.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_reference_attachment"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events/{id}/attachments/{id}
```
##### <a name="response"></a><span data-ttu-id="cfd4c-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cfd4c-159">Response</span></span>
<span data-ttu-id="cfd4c-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cfd4c-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.referenceAttachment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "@odata.type": "#microsoft.graph.referenceAttachment",
  "contentType": "contentType-value",
  "lastModifiedDateTime": "datetime-value",
  "id": "id-value",
  "isInline": false,
  "name": "name-value",
  "size": 99,
}
```



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get attachment",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Error: get_and_expand_item_attachment/item:
      Property 'item' is of type Custom but has no custom members."
  ],
  "tocPath": ""
}-->
