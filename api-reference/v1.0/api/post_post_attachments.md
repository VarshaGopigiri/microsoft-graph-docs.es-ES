# <a name="add-attachment"></a><span data-ttu-id="59ac4-101">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="59ac4-101">Add attachment</span></span>

<span data-ttu-id="59ac4-p101">Use esta API para agregar un objeto [attachment](../resources/attachment.md) a una publicación. Puesto que actualmente hay un límite de 4 MB en el tamaño total de cada solicitud REST, esto limita el tamaño de los datos adjuntos que agregar a menos de 4 MB.</span><span class="sxs-lookup"><span data-stu-id="59ac4-p101">Use this API to add an [attachment](../resources/attachment.md) to a post. Since there is currently a limit of 4MB on the total size of each REST request, this limits the size of the attachment you can add to under 4MB.</span></span>

<span data-ttu-id="59ac4-104">Los datos adjuntos pueden ser de uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="59ac4-104">An attachment can be one of the following types:</span></span>

* <span data-ttu-id="59ac4-105">Un archivo (recurso [fileAttachment](../resources/fileattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="59ac4-105">A file ([fileAttachment](../resources/fileattachment.md) resource).</span></span>
* <span data-ttu-id="59ac4-106">Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="59ac4-106">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource).</span></span>
* <span data-ttu-id="59ac4-107">Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceAttachment.md)).</span><span class="sxs-lookup"><span data-stu-id="59ac4-107">A link to a file ([referenceAttachment](../resources/referenceAttachment.md) resource).</span></span>

<span data-ttu-id="59ac4-108">Todos estos tipos de recursos de datos adjuntos se derivan del recurso [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="59ac4-108">All these types of attachment resources are derived from the [attachment](../resources/attachment.md) resource.</span></span> 

## <a name="permissions"></a><span data-ttu-id="59ac4-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="59ac4-109">Permissions</span></span>
<span data-ttu-id="59ac4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="59ac4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="59ac4-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="59ac4-112">Permission type</span></span>      | <span data-ttu-id="59ac4-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="59ac4-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="59ac4-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="59ac4-114">Delegated (work or school account)</span></span> | <span data-ttu-id="59ac4-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="59ac4-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="59ac4-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="59ac4-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="59ac4-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59ac4-117">Not supported.</span></span>    |
|<span data-ttu-id="59ac4-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="59ac4-118">Application</span></span> | <span data-ttu-id="59ac4-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="59ac4-119">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="59ac4-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="59ac4-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="59ac4-121">Datos adjuntos para un [post](../resources/post.md) de un [thread](../resources/conversationthread.md) perteneciente a una [conversation](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="59ac4-121">Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
```http
POST /groups/{id}/threads/{id}/posts/{id}/attachments
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments
```
## <a name="request-headers"></a><span data-ttu-id="59ac4-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="59ac4-122">Request headers</span></span>
| <span data-ttu-id="59ac4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59ac4-123">Header</span></span>       | <span data-ttu-id="59ac4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="59ac4-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="59ac4-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="59ac4-125">Authorization</span></span>  | <span data-ttu-id="59ac4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="59ac4-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="59ac4-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="59ac4-128">Request body</span></span>
<span data-ttu-id="59ac4-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="59ac4-129">In the request body, supply a JSON representation of [Attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="59ac4-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59ac4-130">Response</span></span>

<span data-ttu-id="59ac4-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59ac4-131">If successful, this method returns `201 Created` response code and [Attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="59ac4-132">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="59ac4-132">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="59ac4-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="59ac4-133">Request</span></span>
<span data-ttu-id="59ac4-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="59ac4-134">Here is an example of the request.</span></span>
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

<span data-ttu-id="59ac4-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="59ac4-135">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="59ac4-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59ac4-136">Response</span></span>
<span data-ttu-id="59ac4-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="59ac4-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="example-item-attachment"></a><span data-ttu-id="59ac4-140">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="59ac4-140">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="59ac4-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="59ac4-141">Request</span></span>
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

##### <a name="response"></a><span data-ttu-id="59ac4-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59ac4-142">Response</span></span>
<span data-ttu-id="59ac4-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="59ac4-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
