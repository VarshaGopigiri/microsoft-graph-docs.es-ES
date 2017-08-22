# <a name="add-attachment"></a><span data-ttu-id="ef105-101">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="ef105-101">Add attachment</span></span>

<span data-ttu-id="ef105-102">Use esta API para crear nuevos datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ef105-102">Use this API to create a new Attachment.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ef105-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ef105-103">Prerequisites</span></span>
<span data-ttu-id="ef105-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:  _Mail.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="ef105-104">The following **scopes** are required to execute this API: _Mail.ReadWrite_</span></span>
## <a name="http-request"></a><span data-ttu-id="ef105-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ef105-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/attachments
POST /users/{id | userPrincipalName}/messages/{id}/attachments
```
## <a name="request-headers"></a><span data-ttu-id="ef105-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ef105-106">Request headers</span></span>
| <span data-ttu-id="ef105-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="ef105-107">Name</span></span>       | <span data-ttu-id="ef105-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ef105-108">Type</span></span> | <span data-ttu-id="ef105-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef105-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="ef105-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="ef105-110">Authorization</span></span>  | <span data-ttu-id="ef105-111">string</span><span class="sxs-lookup"><span data-stu-id="ef105-111">string</span></span>  | <span data-ttu-id="ef105-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ef105-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ef105-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ef105-114">Content-Type</span></span> | <span data-ttu-id="ef105-115">string</span><span class="sxs-lookup"><span data-stu-id="ef105-115">string</span></span>  | <span data-ttu-id="ef105-p102">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ef105-p102">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ef105-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ef105-118">Request body</span></span>
<span data-ttu-id="ef105-119">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="ef105-119">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="ef105-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef105-120">Response</span></span>

<span data-ttu-id="ef105-121">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef105-121">If successful, this method returns `201, Created` response code and [Attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="ef105-122">Ejemplo (datos adjuntos de archivo)</span><span class="sxs-lookup"><span data-stu-id="ef105-122">Example (File attachment)</span></span>
##### <a name="request"></a><span data-ttu-id="ef105-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ef105-123">Request</span></span>
<span data-ttu-id="ef105-124">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ef105-124">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_file_attachment_from_eventmessage"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/attachments
Content-type: application/json
Content-length: 142

{
  "@odata.type": "#Microsoft.OutlookServices.FileAttachment",
  "name": "name-value",
  "contentType": "contentType-value",
  "isInline": false,
  "contentLocation": "contentLocation-value",
  "contentBytes": "contentBytes-value"
}
```

<span data-ttu-id="ef105-125">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="ef105-125">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="ef105-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef105-126">Response</span></span>
<span data-ttu-id="ef105-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ef105-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP/1.1 201 Created
```

## <a name="example-item-attachment"></a><span data-ttu-id="ef105-130">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="ef105-130">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="ef105-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ef105-131">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "create_item_attachment_from_eventmessage"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/attachments
Content-type: application/json
Content-length: 100

{
  "@odata.type": "#Microsoft.OutlookServices.ItemAttachment",
  "name": "name-value",
  "item": "message or event entity"
}
```

##### <a name="response"></a><span data-ttu-id="ef105-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef105-132">Response</span></span>
<span data-ttu-id="ef105-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ef105-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP/1.1 201 Created
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
