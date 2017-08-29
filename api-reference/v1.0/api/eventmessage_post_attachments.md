# <a name="add-attachment"></a><span data-ttu-id="fae59-101">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="fae59-101">Add attachment</span></span>

<span data-ttu-id="fae59-102">Usa esta API para crear nuevos datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="fae59-102">Use this API to create a new Attachment.</span></span>
## <a name="permissions"></a><span data-ttu-id="fae59-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="fae59-103">Permissions</span></span>
<span data-ttu-id="fae59-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fae59-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="fae59-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fae59-106">Permission type</span></span>      | <span data-ttu-id="fae59-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fae59-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fae59-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fae59-108">Delegated (work or school account)</span></span> | <span data-ttu-id="fae59-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fae59-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="fae59-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fae59-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fae59-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fae59-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="fae59-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fae59-112">Application</span></span> | <span data-ttu-id="fae59-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fae59-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="fae59-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fae59-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/attachments
POST /users/{id | userPrincipalName}/messages/{id}/attachments
```
## <a name="request-headers"></a><span data-ttu-id="fae59-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fae59-115">Request headers</span></span>
| <span data-ttu-id="fae59-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="fae59-116">Name</span></span>       | <span data-ttu-id="fae59-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="fae59-117">Type</span></span> | <span data-ttu-id="fae59-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="fae59-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="fae59-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="fae59-119">Authorization</span></span>  | <span data-ttu-id="fae59-120">string</span><span class="sxs-lookup"><span data-stu-id="fae59-120">string</span></span>  | <span data-ttu-id="fae59-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fae59-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fae59-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="fae59-123">Content-Type</span></span> | <span data-ttu-id="fae59-124">string</span><span class="sxs-lookup"><span data-stu-id="fae59-124">string</span></span>  | <span data-ttu-id="fae59-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fae59-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fae59-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fae59-127">Request body</span></span>
<span data-ttu-id="fae59-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="fae59-128">In the request body, supply a JSON representation of [Attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="fae59-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fae59-129">Response</span></span>

<span data-ttu-id="fae59-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fae59-130">If successful, this method returns `201, Created` response code and [Attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="fae59-131">Ejemplo (datos adjuntos de archivo)</span><span class="sxs-lookup"><span data-stu-id="fae59-131">Example (File attachment)</span></span>
##### <a name="request"></a><span data-ttu-id="fae59-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fae59-132">Request</span></span>
<span data-ttu-id="fae59-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fae59-133">Here is an example of the request.</span></span>
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

<span data-ttu-id="fae59-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="fae59-134">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="fae59-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fae59-135">Response</span></span>
<span data-ttu-id="fae59-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fae59-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP/1.1 201 Created
```

## <a name="example-item-attachment"></a><span data-ttu-id="fae59-139">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="fae59-139">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="fae59-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fae59-140">Request</span></span>
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

##### <a name="response"></a><span data-ttu-id="fae59-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fae59-141">Response</span></span>
<span data-ttu-id="fae59-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fae59-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
