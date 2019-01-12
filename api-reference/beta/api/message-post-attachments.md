---
title: Agregar datos adjuntos
description: 'Use esta API para agregar un objeto attachment a un mensaje. '
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: fc24c0a444c07dc8fb8e33814498fe5454b1b3fa
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991905"
---
# <a name="add-attachment"></a><span data-ttu-id="9c3e9-103">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="9c3e9-103">Add attachment</span></span>

> <span data-ttu-id="9c3e9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9c3e9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9c3e9-106">Use esta API para agregar un objeto [attachment](../resources/attachment.md) a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-106">Use this API to add an [attachment](../resources/attachment.md) to a message.</span></span> 

<span data-ttu-id="9c3e9-107">Los datos adjuntos pueden ser de uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9c3e9-107">An attachment can be one of the following types:</span></span>

* <span data-ttu-id="9c3e9-108">Un archivo (recurso [fileAttachment](../resources/fileattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="9c3e9-108">A file ([fileAttachment](../resources/fileattachment.md) resource).</span></span>
* <span data-ttu-id="9c3e9-109">Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="9c3e9-109">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource).</span></span>
* <span data-ttu-id="9c3e9-110">Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="9c3e9-110">A link to a file ([referenceAttachment](../resources/referenceattachment.md) resource).</span></span>

<span data-ttu-id="9c3e9-111">Todos estos tipos de recursos de datos adjuntos se derivan del recurso [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="9c3e9-111">All these types of attachment resources are derived from the [attachment](../resources/attachment.md) resource.</span></span> 

<span data-ttu-id="9c3e9-112">Puede agregar datos adjuntos a un mensaje existente mediante la publicación de su colección de datos adjuntos, o a un nuevo mensaje que se va a [elaborado](../api/user-post-messages.md)o [creado y enviado sobre la marcha](../api/user-sendmail.md).</span><span class="sxs-lookup"><span data-stu-id="9c3e9-112">You can add an attachment to an existing message by posting to its attachments collection, or to a new message that is being [drafted](../api/user-post-messages.md), or [created and sent on the fly](../api/user-sendmail.md).</span></span>

<span data-ttu-id="9c3e9-113">Puesto que actualmente hay un límite de 4 MB en el tamaño total de cada solicitud REST, esto limita el tamaño de los datos adjuntos que agregar a menos de 4 MB.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-113">Since there is currently a limit of 4MB on the total size of each REST request, this limits the size of the attachment you can add to under 4MB.</span></span>
## <a name="permissions"></a><span data-ttu-id="9c3e9-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="9c3e9-114">Permissions</span></span>
<span data-ttu-id="9c3e9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9c3e9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9c3e9-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9c3e9-117">Permission type</span></span>      | <span data-ttu-id="9c3e9-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9c3e9-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9c3e9-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9c3e9-119">Delegated (work or school account)</span></span> | <span data-ttu-id="9c3e9-120">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9c3e9-120">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="9c3e9-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9c3e9-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9c3e9-122">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9c3e9-122">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="9c3e9-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9c3e9-123">Application</span></span> | <span data-ttu-id="9c3e9-124">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9c3e9-124">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="9c3e9-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9c3e9-125">HTTP request</span></span>
<span data-ttu-id="9c3e9-126"><!-- { "blockType": "ignored" } -->Datos adjuntos de un [mensaje](../resources/message.md) en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-126"><!-- { "blockType": "ignored" } --> Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
```http
POST /me/messages/{id}/attachments
POST /users/{id | userPrincipalName}/messages/{id}/attachments
```
<span data-ttu-id="9c3e9-127">Datos adjuntos de un [message](../resources/message.md) contenido en una [mailFolder](../resources/mailfolder.md) de nivel superior en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-127">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
```http
POST /me/mailFolders/{id}/messages/{id}/attachments
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments
```
<span data-ttu-id="9c3e9-p103">Datos adjuntos de un [message](../resources/message.md) contenido en una carpeta secundaria de una [mailFolder](../resources/mailfolder.md) en el buzón de un usuario.  El ejemplo siguiente muestra un nivel de anidamiento, pero un mensaje puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-p103">Attachments for a [message](../resources/message.md) contained in a child folder of a [mailFolder](../resources/mailfolder.md) in a user's mailbox.  The example below shows one level of nesting, but a message can be located in a child of a child and so on.</span></span>
```http
POST /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
POST /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```
## <a name="request-headers"></a><span data-ttu-id="9c3e9-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9c3e9-130">Request headers</span></span>
| <span data-ttu-id="9c3e9-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="9c3e9-131">Name</span></span>       | <span data-ttu-id="9c3e9-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c3e9-132">Type</span></span> | <span data-ttu-id="9c3e9-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c3e9-133">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="9c3e9-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="9c3e9-134">Authorization</span></span>  | <span data-ttu-id="9c3e9-135">string</span><span class="sxs-lookup"><span data-stu-id="9c3e9-135">string</span></span>  | <span data-ttu-id="9c3e9-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9c3e9-138">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9c3e9-138">Content-Type</span></span> | <span data-ttu-id="9c3e9-139">string</span><span class="sxs-lookup"><span data-stu-id="9c3e9-139">string</span></span>  | <span data-ttu-id="9c3e9-p105">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-p105">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9c3e9-142">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9c3e9-142">Request body</span></span>
<span data-ttu-id="9c3e9-143">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="9c3e9-143">In the request body, supply a JSON representation of [Attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="9c3e9-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c3e9-144">Response</span></span>

<span data-ttu-id="9c3e9-145">Si tiene éxito, este método devuelve `201 Created` código de respuesta y el objeto de [datos adjuntos](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-145">If successful, this method returns `201 Created` response code and the [Attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="9c3e9-146">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="9c3e9-146">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="9c3e9-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9c3e9-147">Request</span></span>
<span data-ttu-id="9c3e9-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_file_attachment_from_message"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages/AAMkpsDRVK/attachments
Content-type: application/json
Content-length: 142

{
  "@odata.type": "#microsoft.graph.fileAttachment",
  "name": "smile",
  "contentBytes": "R0lGODdhEAYEAA7"
}
```

<span data-ttu-id="9c3e9-149">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="9c3e9-149">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="9c3e9-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c3e9-150">Response</span></span>
<span data-ttu-id="9c3e9-151">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-151">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.fileAttachment"
} -->
```http
HTTP/1.1 201 Created
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

## <a name="example-item-attachment"></a><span data-ttu-id="9c3e9-152">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="9c3e9-152">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="9c3e9-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9c3e9-153">Request</span></span>
<span data-ttu-id="9c3e9-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-154">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_item_attachment_from_message"
}-->

```
POST https://graph.microsoft.com/beta/me/messages/AAMkpsDRVK/attachments
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

##### <a name="response"></a><span data-ttu-id="9c3e9-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c3e9-155">Response</span></span>
<span data-ttu-id="9c3e9-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="example-reference-attachment"></a><span data-ttu-id="9c3e9-159">Ejemplo (datos adjuntos de referencia)</span><span class="sxs-lookup"><span data-stu-id="9c3e9-159">Example (reference attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="9c3e9-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9c3e9-160">Request</span></span>
<span data-ttu-id="9c3e9-161">Este es un ejemplo de una solicitud que agrega un dato adjunto de referencia a un mensaje existente.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-161">Here is an example of a request that adds a reference attachment to an existing message.</span></span>
<span data-ttu-id="9c3e9-162">Los puntos de datos adjuntos en una carpeta de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-162">The attachment points to a folder on OneDrive.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_reference_attachment_from_message",
  "@odata.type": "microsoft.graph.referenceAttachment"
}-->

```
POST https://graph.microsoft.com/beta/me/messages/AAMkAGE1M88AADUv0uFAAA=/attachments
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

##### <a name="response"></a><span data-ttu-id="9c3e9-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c3e9-163">Response</span></span>
<span data-ttu-id="9c3e9-164">Este es un ejemplo de una respuesta completa.</span><span class="sxs-lookup"><span data-stu-id="9c3e9-164">Here is an example of a full response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.referenceAttachment"
} -->
```http
HTTP 201 Created

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#users/ddfcd489-628b-40d7-b48b-57002df800e5/messages/AAMkAGE1M88AADUv0uFAAA%3D/attachments/$entity",
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
