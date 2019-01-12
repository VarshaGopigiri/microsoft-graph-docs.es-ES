---
title: Agregar datos adjuntos
description: Use esta API para crear datos adjuntos.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: d2e2de9e8e7e328f2e0cabc1df8fdf7dcd7b4856
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965918"
---
# <a name="add-attachment"></a><span data-ttu-id="a17b4-103">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="a17b4-103">Add attachment</span></span>

> <span data-ttu-id="a17b4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a17b4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a17b4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a17b4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a17b4-106">Use esta API para crear datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a17b4-106">Use this API to create a new Attachment.</span></span>

<span data-ttu-id="a17b4-107">Los datos adjuntos pueden ser de uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a17b4-107">An attachment can be one of the following types:</span></span>

* <span data-ttu-id="a17b4-108">Un archivo (recurso [fileAttachment](../resources/fileattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="a17b4-108">A file ([fileAttachment](../resources/fileattachment.md) resource).</span></span>
* <span data-ttu-id="a17b4-109">Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="a17b4-109">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource).</span></span>
* <span data-ttu-id="a17b4-110">Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="a17b4-110">A link to a file ([referenceAttachment](../resources/referenceattachment.md) resource).</span></span>

<span data-ttu-id="a17b4-111">Todos estos tipos de recursos de datos adjuntos se derivan del recurso [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="a17b4-111">All these types of attachment resources are derived from the [attachment](../resources/attachment.md) resource.</span></span> 

## <a name="permissions"></a><span data-ttu-id="a17b4-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="a17b4-112">Permissions</span></span>
<span data-ttu-id="a17b4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a17b4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a17b4-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a17b4-115">Permission type</span></span>      | <span data-ttu-id="a17b4-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a17b4-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a17b4-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a17b4-117">Delegated (work or school account)</span></span> | <span data-ttu-id="a17b4-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a17b4-118">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="a17b4-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a17b4-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a17b4-120">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a17b4-120">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="a17b4-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a17b4-121">Application</span></span> | <span data-ttu-id="a17b4-122">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a17b4-122">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="a17b4-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a17b4-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/attachments
POST /users/{id|userPrincipalName}/messages/{id}/attachments
```
## <a name="request-headers"></a><span data-ttu-id="a17b4-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a17b4-124">Request headers</span></span>
| <span data-ttu-id="a17b4-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="a17b4-125">Name</span></span>       | <span data-ttu-id="a17b4-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="a17b4-126">Type</span></span> | <span data-ttu-id="a17b4-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="a17b4-127">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="a17b4-128">Autorización</span><span class="sxs-lookup"><span data-stu-id="a17b4-128">Authorization</span></span>  | <span data-ttu-id="a17b4-129">string</span><span class="sxs-lookup"><span data-stu-id="a17b4-129">string</span></span>  | <span data-ttu-id="a17b4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a17b4-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a17b4-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a17b4-132">Content-Type</span></span> | <span data-ttu-id="a17b4-133">string</span><span class="sxs-lookup"><span data-stu-id="a17b4-133">string</span></span>  | <span data-ttu-id="a17b4-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a17b4-p104">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a17b4-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a17b4-136">Request body</span></span>
<span data-ttu-id="a17b4-137">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="a17b4-137">In the request body, supply a JSON representation of [Attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="a17b4-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a17b4-138">Response</span></span>

<span data-ttu-id="a17b4-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a17b4-139">If successful, this method returns `201 Created` response code and [Attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="a17b4-140">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="a17b4-140">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="a17b4-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a17b4-141">Request</span></span>
<span data-ttu-id="a17b4-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a17b4-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_file_attachment_from_eventmessage"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages/{id}/attachments
Content-type: application/json

{
  "@odata.type": "#Microsoft.OutlookServices.FileAttachment",
  "name": "name-value",
  "contentType": "contentType-value",
  "isInline": false,
  "contentLocation": "contentLocation-value",
  "contentBytes": "contentBytes-value"
}
```

##### <a name="response"></a><span data-ttu-id="a17b4-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a17b4-143">Response</span></span>
<span data-ttu-id="a17b4-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a17b4-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP 201 Created
```


## <a name="example-item-attachment"></a><span data-ttu-id="a17b4-147">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="a17b4-147">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="a17b4-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a17b4-148">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_item_attachment_from_eventmessage"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/attachments
Content-type: application/json

{
  "@odata.type": "#Microsoft.OutlookServices.ItemAttachment",
  "name": "name-value",
  "item": "message or event entity"
}
```

##### <a name="response"></a><span data-ttu-id="a17b4-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a17b4-149">Response</span></span>
<span data-ttu-id="a17b4-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a17b4-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP 201 Created
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
