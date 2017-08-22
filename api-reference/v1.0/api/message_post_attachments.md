# <a name="add-attachment"></a><span data-ttu-id="34852-101">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="34852-101">Add attachment</span></span>

<span data-ttu-id="34852-102">Use esta API para agregar un objeto [attachment](../resources/attachment.md) a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="34852-102">Use this API to add an [attachment](../resources/attachment.md) to a message.</span></span> 

<span data-ttu-id="34852-103">Puede agregar datos adjuntos a un mensaje existente publicándolos en su colección de datos adjuntos, o puede agregar datos adjuntos a un mensaje que se [crea y envía en el acto](../api/user_sendmail.md).</span><span class="sxs-lookup"><span data-stu-id="34852-103">You can add an attachment to an existing message by posting to its attachments collection, or you can add an attachment to a message that is being [created and sent on the fly](../api/user_sendmail.md).</span></span>

<span data-ttu-id="34852-104">Puesto que actualmente hay un límite de 4 MB en el tamaño total de cada solicitud REST, esto limita el tamaño de los datos adjuntos que agregar a menos de 4 MB.</span><span class="sxs-lookup"><span data-stu-id="34852-104">Since there is currently a limit of 4MB on the total size of each REST request, this limits the size of the attachment you can add to under 4MB.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="34852-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="34852-105">Prerequisites</span></span>
<span data-ttu-id="34852-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="34852-106">One of the following **scopes** is required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="34852-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="34852-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="34852-108">Datos adjuntos de un [message](../resources/message.md) en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="34852-108">Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
```http
POST /me/messages/{id}/attachments
POST /users/{id | userPrincipalName}/messages/{id}/attachments
```
<span data-ttu-id="34852-109">Datos adjuntos de un [message](../resources/message.md) contenido en una [mailFolder](../resources/mailfolder.md) de nivel superior en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="34852-109">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
```http
POST /me/mailFolders/{id}/messages/{id}/attachments
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments
```
<span data-ttu-id="34852-p101">Datos adjuntos de un [message](../resources/message.md) contenido en una carpeta secundaria de una [mailFolder](../resources/mailfolder.md) en el buzón de un usuario.  El ejemplo siguiente muestra un nivel de anidamiento, pero un mensaje puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="34852-p101">Attachments for a [message](../resources/message.md) contained in a child folder of a [mailFolder](../resources/mailfolder.md) in a user's mailbox.  The example below shows one level of nesting, but a message can be located in a child of a child and so on.</span></span>
```http
POST /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
POST /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```
## <a name="request-headers"></a><span data-ttu-id="34852-112">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="34852-112">Request headers</span></span>
| <span data-ttu-id="34852-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="34852-113">Name</span></span>       | <span data-ttu-id="34852-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="34852-114">Type</span></span> | <span data-ttu-id="34852-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="34852-115">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="34852-116">Authorization</span><span class="sxs-lookup"><span data-stu-id="34852-116">Authorization</span></span>  | <span data-ttu-id="34852-117">string</span><span class="sxs-lookup"><span data-stu-id="34852-117">string</span></span>  | <span data-ttu-id="34852-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="34852-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="34852-120">Content-Type</span><span class="sxs-lookup"><span data-stu-id="34852-120">Content-Type</span></span> | <span data-ttu-id="34852-121">string</span><span class="sxs-lookup"><span data-stu-id="34852-121">string</span></span>  | <span data-ttu-id="34852-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="34852-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="34852-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="34852-124">Request body</span></span>
<span data-ttu-id="34852-125">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="34852-125">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="34852-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34852-126">Response</span></span>

<span data-ttu-id="34852-127">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34852-127">If successful, this method returns `201, Created` response code and [Attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="34852-128">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="34852-128">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="34852-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34852-129">Request</span></span>
<span data-ttu-id="34852-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="34852-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_file_attachment_from_message"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/AAMkpsDRVK/attachments
Content-type: application/json
Content-length: 142

{
  "@odata.type": "#microsoft.graph.fileAttachment",
  "name": "smile",
  "contentBytes": "R0lGODdhEAYEAA7"
}
```

<span data-ttu-id="34852-131">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="34852-131">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="34852-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34852-132">Response</span></span>
<span data-ttu-id="34852-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34852-133">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.fileAttachment"
} -->
```http
HTTP 201 Created
Content-type: application/json
Content-length: 202

{
    "id": "AAMkADNkN2R",
    "lastModifiedDateTime": "2017-01-26T08:48:28Z",
    "name": "smile",
    "contentType": "image/gif",
    "size": 1008,
    "isInline": false,
    "contentId": null,
    "contentLocation": null,
    "contentBytes": "R0lGODdhEAYEAA7"
}

```

## <a name="example-item-attachment"></a><span data-ttu-id="34852-134">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="34852-134">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="34852-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34852-135">Request</span></span>
<span data-ttu-id="34852-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="34852-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_item_attachment_from_message"
}-->

```
POST https://graph.microsoft.com/v1.0/me/messages/AAMkpsDRVK/attachments
Content-type: application/json
Content-length: 200

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

##### <a name="response"></a><span data-ttu-id="34852-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34852-137">Response</span></span>
<span data-ttu-id="34852-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="34852-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.itemAttachment"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 162

{
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
