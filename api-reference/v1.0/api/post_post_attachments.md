# <a name="add-attachment"></a><span data-ttu-id="cef9f-101">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="cef9f-101">Add attachment</span></span>

<span data-ttu-id="cef9f-p101">Use esta API para agregar un objeto [attachment](../resources/attachment.md) a una publicación. Puesto que actualmente hay un límite de 4 MB en el tamaño total de cada solicitud REST, esto limita el tamaño de los datos adjuntos que agregar a menos de 4 MB.</span><span class="sxs-lookup"><span data-stu-id="cef9f-p101">Use this API to add an [attachment](../resources/attachment.md) to a post. Since there is currently a limit of 4MB on the total size of each REST request, this limits the size of the attachment you can add to under 4MB.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cef9f-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cef9f-104">Prerequisites</span></span>
<span data-ttu-id="cef9f-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="cef9f-105">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="cef9f-106">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cef9f-106">Group.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="cef9f-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cef9f-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="cef9f-108">Datos adjuntos para un [post](../resources/post.md) de un [thread](../resources/conversationthread.md) perteneciente a una [conversation](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="cef9f-108">Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
```http
POST /groups/{id}/threads/{id}/posts/{id}/attachments
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments
```
## <a name="request-headers"></a><span data-ttu-id="cef9f-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cef9f-109">Request headers</span></span>
| <span data-ttu-id="cef9f-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cef9f-110">Header</span></span>       | <span data-ttu-id="cef9f-111">Valor</span><span class="sxs-lookup"><span data-stu-id="cef9f-111">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="cef9f-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="cef9f-112">Authorization</span></span>  | <span data-ttu-id="cef9f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cef9f-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="cef9f-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cef9f-115">Request body</span></span>
<span data-ttu-id="cef9f-116">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="cef9f-116">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="cef9f-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cef9f-117">Response</span></span>

<span data-ttu-id="cef9f-118">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cef9f-118">If successful, this method returns `201, Created` response code and [Attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="cef9f-119">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="cef9f-119">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="cef9f-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cef9f-120">Request</span></span>
<span data-ttu-id="cef9f-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cef9f-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_file_attachment_from_post"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts/{id}/attachments
Content-type: application/json
Content-length: 142

{
  "@odata.type": "#microsoft.graph.fileAttachment",
  "name": "name-value",
  "contentBytes": "contentBytes-value"
}
```

<span data-ttu-id="cef9f-122">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="cef9f-122">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="cef9f-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cef9f-123">Response</span></span>
<span data-ttu-id="cef9f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cef9f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 162

{
  "lastModifiedDateTime": "datetime-value",
  "name": "name-value",
  "contentType": "contentType-value",
  "size": 99,
  "isInline": true,
  "id": "id-value"
}
```

## <a name="example-item-attachment"></a><span data-ttu-id="cef9f-127">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="cef9f-127">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="cef9f-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cef9f-128">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "create_item_attachment_from_post"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts/{id}/attachments
Content-type: application/json
Content-length: 100

{
  "@odata.type": "#microsoft.graph.itemAttachment",
  "name": "name-value",
  "item": { }
}
```

##### <a name="response"></a><span data-ttu-id="cef9f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cef9f-129">Response</span></span>
<span data-ttu-id="cef9f-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cef9f-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 162

{
  "lastModifiedDateTime": "datetime-value",
  "name": "name-value",
  "contentType": "contentType-value",
  "size": 99,
  "isInline": true,
  "id": "id-value"
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
