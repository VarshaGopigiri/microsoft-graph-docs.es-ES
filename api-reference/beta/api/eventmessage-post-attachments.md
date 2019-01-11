---
title: Agregar datos adjuntos
description: Use esta API para crear datos adjuntos.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: e56da5a4b6f57506800e07e3f8e2b09ed7ef6f46
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824083"
---
# <a name="add-attachment"></a><span data-ttu-id="1d3fe-103">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="1d3fe-103">Add attachment</span></span>

> <span data-ttu-id="1d3fe-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d3fe-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d3fe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d3fe-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1d3fe-106">Use esta API para crear datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="1d3fe-106">Use this API to create a new Attachment.</span></span>

<span data-ttu-id="1d3fe-107">Los datos adjuntos pueden ser de uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1d3fe-107">An attachment can be one of the following types:</span></span>

* <span data-ttu-id="1d3fe-108">Un archivo (recurso [fileAttachment](../resources/fileattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="1d3fe-108">A file ([fileAttachment](../resources/fileattachment.md) resource).</span></span>
* <span data-ttu-id="1d3fe-109">Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="1d3fe-109">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource).</span></span>
* <span data-ttu-id="1d3fe-110">Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="1d3fe-110">A link to a file ([referenceAttachment](../resources/referenceattachment.md) resource).</span></span>

<span data-ttu-id="1d3fe-111">Todos estos tipos de recursos de datos adjuntos se derivan del recurso [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="1d3fe-111">All these types of attachment resources are derived from the [attachment](../resources/attachment.md) resource.</span></span> 

## <a name="permissions"></a><span data-ttu-id="1d3fe-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="1d3fe-112">Permissions</span></span>
<span data-ttu-id="1d3fe-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d3fe-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d3fe-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d3fe-115">Permission type</span></span>      | <span data-ttu-id="1d3fe-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d3fe-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1d3fe-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d3fe-117">Delegated (work or school account)</span></span> | <span data-ttu-id="1d3fe-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1d3fe-118">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="1d3fe-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d3fe-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1d3fe-120">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1d3fe-120">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="1d3fe-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d3fe-121">Application</span></span> | <span data-ttu-id="1d3fe-122">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1d3fe-122">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="1d3fe-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d3fe-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/attachments
POST /users/{id|userPrincipalName}/messages/{id}/attachments
```
## <a name="request-headers"></a><span data-ttu-id="1d3fe-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d3fe-124">Request headers</span></span>
| <span data-ttu-id="1d3fe-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="1d3fe-125">Name</span></span>       | <span data-ttu-id="1d3fe-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d3fe-126">Type</span></span> | <span data-ttu-id="1d3fe-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d3fe-127">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="1d3fe-128">Autorización</span><span class="sxs-lookup"><span data-stu-id="1d3fe-128">Authorization</span></span>  | <span data-ttu-id="1d3fe-129">string</span><span class="sxs-lookup"><span data-stu-id="1d3fe-129">string</span></span>  | <span data-ttu-id="1d3fe-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1d3fe-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1d3fe-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1d3fe-132">Content-Type</span></span> | <span data-ttu-id="1d3fe-133">string</span><span class="sxs-lookup"><span data-stu-id="1d3fe-133">string</span></span>  | <span data-ttu-id="1d3fe-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1d3fe-p104">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1d3fe-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d3fe-136">Request body</span></span>
<span data-ttu-id="1d3fe-137">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="1d3fe-137">In the request body, supply a JSON representation of [Attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="1d3fe-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d3fe-138">Response</span></span>

<span data-ttu-id="1d3fe-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d3fe-139">If successful, this method returns `201 Created` response code and [Attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="1d3fe-140">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="1d3fe-140">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="1d3fe-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d3fe-141">Request</span></span>
<span data-ttu-id="1d3fe-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d3fe-142">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="1d3fe-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d3fe-143">Response</span></span>
<span data-ttu-id="1d3fe-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d3fe-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP 201 Created
```


## <a name="example-item-attachment"></a><span data-ttu-id="1d3fe-147">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="1d3fe-147">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="1d3fe-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d3fe-148">Request</span></span>

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

##### <a name="response"></a><span data-ttu-id="1d3fe-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d3fe-149">Response</span></span>
<span data-ttu-id="1d3fe-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d3fe-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
