---
title: Agregar datos adjuntos
description: Utilice esta API para agregar datos adjuntos a una entrada. Desde allí
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: cca12c8d8ed3658e0087327dda87443de63a1982
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845797"
---
# <a name="add-attachment"></a><span data-ttu-id="f8551-104">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="f8551-104">Add attachment</span></span>

<span data-ttu-id="f8551-p102">Use esta API para agregar un objeto [attachment](../resources/attachment.md) a una publicación. Puesto que actualmente hay un límite de 4 MB en el tamaño total de cada solicitud REST, esto limita el tamaño de los datos adjuntos que agregar a menos de 4 MB.</span><span class="sxs-lookup"><span data-stu-id="f8551-p102">Use this API to add an [attachment](../resources/attachment.md) to a post. Since there is currently a limit of 4MB on the total size of each REST request, this limits the size of the attachment you can add to under 4MB.</span></span>

<span data-ttu-id="f8551-107">Los datos adjuntos pueden ser de uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f8551-107">An attachment can be one of the following types:</span></span>

* <span data-ttu-id="f8551-108">Un archivo (recurso [fileAttachment](../resources/fileattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="f8551-108">A file ([fileAttachment](../resources/fileattachment.md) resource).</span></span>
* <span data-ttu-id="f8551-109">Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="f8551-109">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource).</span></span>
* <span data-ttu-id="f8551-110">Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="f8551-110">A link to a file ([referenceAttachment](../resources/referenceattachment.md) resource).</span></span>

<span data-ttu-id="f8551-111">Todos estos tipos de recursos de datos adjuntos se derivan del recurso [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="f8551-111">All these types of attachment resources are derived from the [attachment](../resources/attachment.md) resource.</span></span> 

## <a name="permissions"></a><span data-ttu-id="f8551-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="f8551-112">Permissions</span></span>
<span data-ttu-id="f8551-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f8551-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f8551-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f8551-115">Permission type</span></span>      | <span data-ttu-id="f8551-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f8551-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f8551-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f8551-117">Delegated (work or school account)</span></span> | <span data-ttu-id="f8551-118">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f8551-118">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="f8551-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f8551-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f8551-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f8551-120">Not supported.</span></span>    |
|<span data-ttu-id="f8551-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f8551-121">Application</span></span> | <span data-ttu-id="f8551-122">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f8551-122">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f8551-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f8551-123">HTTP request</span></span>
<span data-ttu-id="f8551-124"><!-- { "blockType": "ignored" } -->Datos adjuntos de una [entrada](../resources/post.md) en un [subproceso](../resources/conversationthread.md) que pertenecen a una [conversación](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="f8551-124"><!-- { "blockType": "ignored" } --> Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
```http
POST /groups/{id}/threads/{id}/posts/{id}/attachments
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments
```
## <a name="request-headers"></a><span data-ttu-id="f8551-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f8551-125">Request headers</span></span>
| <span data-ttu-id="f8551-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8551-126">Header</span></span>       | <span data-ttu-id="f8551-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f8551-127">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="f8551-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="f8551-128">Authorization</span></span>  | <span data-ttu-id="f8551-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f8551-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="f8551-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f8551-131">Request body</span></span>
<span data-ttu-id="f8551-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="f8551-132">In the request body, supply a JSON representation of [Attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="f8551-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8551-133">Response</span></span>

<span data-ttu-id="f8551-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8551-134">If successful, this method returns `201 Created` response code and [Attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="f8551-135">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="f8551-135">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="f8551-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f8551-136">Request</span></span>
<span data-ttu-id="f8551-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f8551-137">Here is an example of the request.</span></span>
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
  "contentBytes": "base64-contentBytes-value"
}
```

<span data-ttu-id="f8551-138">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="f8551-138">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="f8551-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8551-139">Response</span></span>
<span data-ttu-id="f8551-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f8551-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="example-item-attachment"></a><span data-ttu-id="f8551-143">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="f8551-143">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="f8551-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f8551-144">Request</span></span>
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

##### <a name="response"></a><span data-ttu-id="f8551-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8551-145">Response</span></span>
<span data-ttu-id="f8551-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f8551-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
