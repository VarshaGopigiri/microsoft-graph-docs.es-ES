---
title: Agregar datos adjuntos
description: 'Use esta API para agregar un objeto attachment a un mensaje. '
author: angelgolfer-ms
ms.openlocfilehash: 868ce046a37d027c675b005cef013892deffe2a3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314619"
---
# <a name="add-attachment"></a><span data-ttu-id="6efec-103">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="6efec-103">Add attachment</span></span>

<span data-ttu-id="6efec-104">Use esta API para agregar un objeto [attachment](../resources/attachment.md) a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="6efec-104">Use this API to add an [attachment](../resources/attachment.md) to a message.</span></span> 

<span data-ttu-id="6efec-105">Los datos adjuntos pueden ser de uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6efec-105">An attachment can be one of the following types:</span></span>

* <span data-ttu-id="6efec-106">Un archivo (recurso [fileAttachment](../resources/fileattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="6efec-106">A file ([fileAttachment](../resources/fileattachment.md) resource).</span></span>
* <span data-ttu-id="6efec-107">Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="6efec-107">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource).</span></span>
* <span data-ttu-id="6efec-108">Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceattachment.md)).</span><span class="sxs-lookup"><span data-stu-id="6efec-108">A link to a file ([referenceAttachment](../resources/referenceattachment.md) resource).</span></span>

<span data-ttu-id="6efec-109">Todos estos tipos de recursos de datos adjuntos se derivan del recurso [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="6efec-109">All these types of attachment resources are derived from the [attachment](../resources/attachment.md) resource.</span></span> 

<span data-ttu-id="6efec-110">Puede agregar datos adjuntos a un mensaje existente publicándolos en su colección de datos adjuntos, o puede agregar datos adjuntos a un mensaje que se [crea y envía en el acto](../api/user-sendmail.md).</span><span class="sxs-lookup"><span data-stu-id="6efec-110">You can add an attachment to an existing message by posting to its attachments collection, or you can add an attachment to a message that is being [created and sent on the fly](../api/user-sendmail.md).</span></span>

<span data-ttu-id="6efec-111">Puesto que actualmente hay un límite de 4 MB en el tamaño total de cada solicitud REST, esto limita el tamaño de los datos adjuntos que agregar a menos de 4 MB.</span><span class="sxs-lookup"><span data-stu-id="6efec-111">Since there is currently a limit of 4MB on the total size of each REST request, this limits the size of the attachment you can add to under 4MB.</span></span>
## <a name="permissions"></a><span data-ttu-id="6efec-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="6efec-112">Permissions</span></span>
<span data-ttu-id="6efec-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6efec-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6efec-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6efec-115">Permission type</span></span>      | <span data-ttu-id="6efec-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6efec-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6efec-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6efec-117">Delegated (work or school account)</span></span> | <span data-ttu-id="6efec-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6efec-118">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6efec-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6efec-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6efec-120">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6efec-120">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6efec-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6efec-121">Application</span></span> | <span data-ttu-id="6efec-122">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6efec-122">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="6efec-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6efec-123">HTTP request</span></span>
<span data-ttu-id="6efec-124"><!-- { "blockType": "ignored" } -->Datos adjuntos de un [mensaje](../resources/message.md) en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="6efec-124"><!-- { "blockType": "ignored" } --> Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
```http
POST /me/messages/{id}/attachments
POST /users/{id | userPrincipalName}/messages/{id}/attachments
```
<span data-ttu-id="6efec-125">Datos adjuntos de un [message](../resources/message.md) contenido en una [mailFolder](../resources/mailfolder.md) de nivel superior en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="6efec-125">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
```http
POST /me/mailFolders/{id}/messages/{id}/attachments
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments
```
<span data-ttu-id="6efec-p102">Datos adjuntos de un [message](../resources/message.md) contenido en una carpeta secundaria de una [mailFolder](../resources/mailfolder.md) en el buzón de un usuario.  El ejemplo siguiente muestra un nivel de anidamiento, pero un mensaje puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="6efec-p102">Attachments for a [message](../resources/message.md) contained in a child folder of a [mailFolder](../resources/mailfolder.md) in a user's mailbox.  The example below shows one level of nesting, but a message can be located in a child of a child and so on.</span></span>
```http
POST /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
POST /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```
## <a name="request-headers"></a><span data-ttu-id="6efec-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6efec-128">Request headers</span></span>
| <span data-ttu-id="6efec-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="6efec-129">Name</span></span>       | <span data-ttu-id="6efec-130">Type</span><span class="sxs-lookup"><span data-stu-id="6efec-130">Type</span></span> | <span data-ttu-id="6efec-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="6efec-131">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6efec-132">Autorización</span><span class="sxs-lookup"><span data-stu-id="6efec-132">Authorization</span></span>  | <span data-ttu-id="6efec-133">string</span><span class="sxs-lookup"><span data-stu-id="6efec-133">string</span></span>  | <span data-ttu-id="6efec-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6efec-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6efec-136">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6efec-136">Content-Type</span></span> | <span data-ttu-id="6efec-137">string</span><span class="sxs-lookup"><span data-stu-id="6efec-137">string</span></span>  | <span data-ttu-id="6efec-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6efec-p104">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6efec-140">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6efec-140">Request body</span></span>
<span data-ttu-id="6efec-141">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="6efec-141">In the request body, supply a JSON representation of [Attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="6efec-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6efec-142">Response</span></span>

<span data-ttu-id="6efec-143">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6efec-143">If successful, this method returns `201 Created` response code and [Attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="6efec-144">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="6efec-144">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="6efec-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6efec-145">Request</span></span>
<span data-ttu-id="6efec-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6efec-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkpsDRVK"],
  "name": "create_file_attachment_from_message"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/AAMkpsDRVK/attachments
Content-type: application/json
Content-length: 142

{
  "@odata.type": "#microsoft.graph.fileAttachment",
  "name": "smile",
  "contentBytes": "base64R0lGODdhEAYEAA7"
}
```

<span data-ttu-id="6efec-147">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="6efec-147">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="6efec-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6efec-148">Response</span></span>
<span data-ttu-id="6efec-149">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6efec-149">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.fileAttachment"
} -->
```http
HTTP 201 Created
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
    "contentBytes": "base64R0lGODdhEAYEAA7"
}

```

## <a name="example-item-attachment"></a><span data-ttu-id="6efec-150">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="6efec-150">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="6efec-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6efec-151">Request</span></span>
<span data-ttu-id="6efec-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6efec-152">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkpsDRVK"],
  "name": "create_item_attachment_from_message"
}-->

```
POST https://graph.microsoft.com/v1.0/me/messages/AAMkpsDRVK/attachments
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

##### <a name="response"></a><span data-ttu-id="6efec-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6efec-153">Response</span></span>
<span data-ttu-id="6efec-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6efec-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Attachment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
