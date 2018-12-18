---
title: Agregar datos adjuntos
description: Use esta API para crear datos adjuntos.
author: angelgolfer-ms
ms.openlocfilehash: 4e0b2cb19737071b20269e4fab602dc10395a6b2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27317965"
---
# <a name="add-attachment"></a><span data-ttu-id="98168-103">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="98168-103">Add attachment</span></span>

<span data-ttu-id="98168-104">Use esta API para crear datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="98168-104">Use this API to create a new Attachment.</span></span>

<span data-ttu-id="98168-105">Los datos adjuntos pueden ser de uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="98168-105">An attachment can be one of the following types:</span></span>

* <span data-ttu-id="98168-106">Un archivo (recurso [fileAttachment](../resources/fileattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="98168-106">A file ([fileAttachment](../resources/fileattachment.md) resource).</span></span>
* <span data-ttu-id="98168-107">Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="98168-107">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource).</span></span>
* <span data-ttu-id="98168-108">Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="98168-108">A link to a file ([referenceAttachment](../resources/referenceattachment.md) resource).</span></span>

<span data-ttu-id="98168-109">Todos estos tipos de recursos de datos adjuntos se derivan del recurso [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="98168-109">All these types of attachment resources are derived from the [attachment](../resources/attachment.md) resource.</span></span> 

## <a name="permissions"></a><span data-ttu-id="98168-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="98168-110">Permissions</span></span>
<span data-ttu-id="98168-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="98168-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="98168-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="98168-113">Permission type</span></span>      | <span data-ttu-id="98168-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="98168-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="98168-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="98168-115">Delegated (work or school account)</span></span> | <span data-ttu-id="98168-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="98168-116">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="98168-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="98168-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="98168-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="98168-118">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="98168-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="98168-119">Application</span></span> | <span data-ttu-id="98168-120">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="98168-120">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="98168-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="98168-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/attachments
POST /users/{id | userPrincipalName}/messages/{id}/attachments
```
## <a name="request-headers"></a><span data-ttu-id="98168-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="98168-122">Request headers</span></span>
| <span data-ttu-id="98168-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="98168-123">Name</span></span>       | <span data-ttu-id="98168-124">Type</span><span class="sxs-lookup"><span data-stu-id="98168-124">Type</span></span> | <span data-ttu-id="98168-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="98168-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="98168-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="98168-126">Authorization</span></span>  | <span data-ttu-id="98168-127">string</span><span class="sxs-lookup"><span data-stu-id="98168-127">string</span></span>  | <span data-ttu-id="98168-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="98168-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="98168-130">Content-Type</span><span class="sxs-lookup"><span data-stu-id="98168-130">Content-Type</span></span> | <span data-ttu-id="98168-131">string</span><span class="sxs-lookup"><span data-stu-id="98168-131">string</span></span>  | <span data-ttu-id="98168-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="98168-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="98168-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="98168-134">Request body</span></span>
<span data-ttu-id="98168-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="98168-135">In the request body, supply a JSON representation of [Attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="98168-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98168-136">Response</span></span>

<span data-ttu-id="98168-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98168-137">If successful, this method returns `201 Created` response code and [Attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="98168-138">Ejemplo (datos adjuntos de archivo)</span><span class="sxs-lookup"><span data-stu-id="98168-138">Example (File attachment)</span></span>
##### <a name="request"></a><span data-ttu-id="98168-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98168-139">Request</span></span>
<span data-ttu-id="98168-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98168-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_file_attachment_from_eventmessage"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/attachments
Content-type: application/json
Content-length: 142

{
  "@odata.type": "microsoft.graph.fileAttachment",
  "name": "name-value",
  "contentType": "contentType-value",
  "isInline": false,
  "contentLocation": "contentLocation-value",
  "contentBytes": "base64-contentBytes-value"
}
```

<span data-ttu-id="98168-141">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="98168-141">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="98168-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98168-142">Response</span></span>
<span data-ttu-id="98168-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="98168-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP/1.1 201 Created
```

## <a name="example-item-attachment"></a><span data-ttu-id="98168-146">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="98168-146">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="98168-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98168-147">Request</span></span>
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

##### <a name="response"></a><span data-ttu-id="98168-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98168-148">Response</span></span>
<span data-ttu-id="98168-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="98168-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
