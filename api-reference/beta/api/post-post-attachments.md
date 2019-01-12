---
title: Agregar datos adjuntos
description: Utilice esta API para agregar datos adjuntos a una entrada. Desde allí
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: bbc4779e7e7a482e3a1e402219855042781d07db
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980450"
---
# <a name="add-attachment"></a><span data-ttu-id="6f1d7-104">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="6f1d7-104">Add attachment</span></span>

> <span data-ttu-id="6f1d7-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6f1d7-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6f1d7-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6f1d7-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6f1d7-p103">Use esta API para agregar un objeto [attachment](../resources/attachment.md) a una publicación. Puesto que actualmente hay un límite de 4 MB en el tamaño total de cada solicitud REST, esto limita el tamaño de los datos adjuntos que agregar a menos de 4 MB.</span><span class="sxs-lookup"><span data-stu-id="6f1d7-p103">Use this API to add an [attachment](../resources/attachment.md) to a post. Since there is currently a limit of 4MB on the total size of each REST request, this limits the size of the attachment you can add to under 4MB.</span></span>

<span data-ttu-id="6f1d7-109">Los datos adjuntos pueden ser de uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6f1d7-109">An attachment can be one of the following types:</span></span>

* <span data-ttu-id="6f1d7-110">Un archivo (recurso [fileAttachment](../resources/fileattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="6f1d7-110">A file ([fileAttachment](../resources/fileattachment.md) resource).</span></span>
* <span data-ttu-id="6f1d7-111">Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="6f1d7-111">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource).</span></span>
* <span data-ttu-id="6f1d7-112">Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="6f1d7-112">A link to a file ([referenceAttachment](../resources/referenceattachment.md) resource).</span></span>

<span data-ttu-id="6f1d7-113">Todos estos tipos de recursos de datos adjuntos se derivan del recurso [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="6f1d7-113">All these types of attachment resources are derived from the [attachment](../resources/attachment.md) resource.</span></span> 

## <a name="permissions"></a><span data-ttu-id="6f1d7-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="6f1d7-114">Permissions</span></span>
<span data-ttu-id="6f1d7-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6f1d7-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6f1d7-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6f1d7-117">Permission type</span></span>      | <span data-ttu-id="6f1d7-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6f1d7-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6f1d7-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6f1d7-119">Delegated (work or school account)</span></span> | <span data-ttu-id="6f1d7-120">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6f1d7-120">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="6f1d7-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6f1d7-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6f1d7-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6f1d7-122">Not supported.</span></span>    |
|<span data-ttu-id="6f1d7-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6f1d7-123">Application</span></span> | <span data-ttu-id="6f1d7-124">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6f1d7-124">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6f1d7-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6f1d7-125">HTTP request</span></span>
<span data-ttu-id="6f1d7-126"><!-- { "blockType": "ignored" } -->Datos adjuntos de una [entrada](../resources/post.md) en un [subproceso](../resources/conversationthread.md) que pertenecen a una [conversación](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="6f1d7-126"><!-- { "blockType": "ignored" } --> Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
```http
POST /groups/{id}/threads/{id}/posts/{id}/attachments
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments
```
## <a name="request-headers"></a><span data-ttu-id="6f1d7-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6f1d7-127">Request headers</span></span>
| <span data-ttu-id="6f1d7-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f1d7-128">Header</span></span>       | <span data-ttu-id="6f1d7-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6f1d7-129">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="6f1d7-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="6f1d7-130">Authorization</span></span>  | <span data-ttu-id="6f1d7-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f1d7-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="6f1d7-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6f1d7-133">Request body</span></span>
<span data-ttu-id="6f1d7-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="6f1d7-134">In the request body, supply a JSON representation of [Attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="6f1d7-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f1d7-135">Response</span></span>

<span data-ttu-id="6f1d7-136">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f1d7-136">If successful, this method returns `201 Created` response code and [Attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="6f1d7-137">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="6f1d7-137">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="6f1d7-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f1d7-138">Request</span></span>
<span data-ttu-id="6f1d7-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f1d7-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_file_attachment_from_post"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/threads/{id}/posts/{id}/attachments
Content-type: application/json
Content-length: 142

{
  "@odata.type": "#microsoft.graph.fileAttachment",
  "name": "name-value",
  "contentBytes": "contentBytes-value"
}
```

<span data-ttu-id="6f1d7-140">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="6f1d7-140">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="6f1d7-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f1d7-141">Response</span></span>
<span data-ttu-id="6f1d7-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6f1d7-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "lastModifiedDateTime": "2016-10-19T10:37:00Z",
  "name": "name-value",
  "contentType": "contentType-value",
  "size": 99,
  "isInline": true,
  "id": "id-value"
}
```

## <a name="example-item-attachment"></a><span data-ttu-id="6f1d7-145">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="6f1d7-145">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="6f1d7-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f1d7-146">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "create_item_attachment_from_post"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/threads/{id}/posts/{id}/attachments
Content-type: application/json
Content-length: 100

{
  "@odata.type": "#microsoft.graph.itemAttachment",
  "name": "name-value",
  "item": { }
}
```

##### <a name="response"></a><span data-ttu-id="6f1d7-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f1d7-147">Response</span></span>
<span data-ttu-id="6f1d7-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6f1d7-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "lastModifiedDateTime": "2016-10-19T10:37:00Z",
  "name": "name-value",
  "contentType": "contentType-value",
  "size": 99,
  "isInline": true,
  "id": "id-value"
}
```


## <a name="example-reference-attachment"></a><span data-ttu-id="6f1d7-151">Ejemplo (datos adjuntos de referencia)</span><span class="sxs-lookup"><span data-stu-id="6f1d7-151">Example (reference attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="6f1d7-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f1d7-152">Request</span></span>
<span data-ttu-id="6f1d7-153">Este es un ejemplo de una solicitud que agrega un dato adjunto de referencia a una entrada existente.</span><span class="sxs-lookup"><span data-stu-id="6f1d7-153">Here is an example of a request that adds a reference attachment to an existing post.</span></span>
<span data-ttu-id="6f1d7-154">Los puntos de datos adjuntos en una carpeta de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="6f1d7-154">The attachment points to a folder on OneDrive.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_reference_attachment_from_post",
  "@odata.type": "microsoft.graph.referenceAttachment"
}-->

```
POST https://graph.microsoft.com/beta/groups/c75831bdfad/threads/AAQkAGF97XEKhULw/posts/AAMkAGFcAAA/attachments
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

##### <a name="response"></a><span data-ttu-id="6f1d7-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f1d7-155">Response</span></span>
<span data-ttu-id="6f1d7-156">Este es un ejemplo de una respuesta completa.</span><span class="sxs-lookup"><span data-stu-id="6f1d7-156">Here is an example of a full response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.referenceAttachment"
} -->
```http
HTTP 201 Created

{
  "@odata.context": "https://graph.microsoft.com/beta/groups/c75831bdfad/threads/AAQkAGF97XEKhULw/posts/AAMkAGFcAAA/attachments/$entity",
  "@odata.type": "#microsoft.graph.referenceAttachment",
  "id": "AAMkAGE1Mg72tgf7hJp0PICVGCc0g=",
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
