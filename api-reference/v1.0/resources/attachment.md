---
title: Tipo de recurso attachment
description: Puede agregar contenido relacionado a un evento
ms.openlocfilehash: 418d8d4e60d12fed5a54f994e14e996c65731926
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030591"
---
# <a name="attachment-resource-type"></a><span data-ttu-id="e3e3f-103">Tipo de recurso attachment</span><span class="sxs-lookup"><span data-stu-id="e3e3f-103">attachment resource type</span></span>

<span data-ttu-id="e3e3f-104">Puede agregar contenido relacionado a un [evento](../resources/event.md), [mensaje](../resources/message.md) o [publicación](../resources/post.md) en forma de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-104">You can add related content to an [event](../resources/event.md), [message](../resources/message.md), or [post](../resources/post.md) in the form of an attachment.</span></span>

<span data-ttu-id="e3e3f-105">**datos adjuntos** es el recurso base para los siguientes tipos de datos adjuntos derivados:</span><span class="sxs-lookup"><span data-stu-id="e3e3f-105">**attachment** is the base resource for the following derived types of attachments:</span></span>

* <span data-ttu-id="e3e3f-106">Un archivo (recurso [fileAttachment](../resources/fileattachment.md))</span><span class="sxs-lookup"><span data-stu-id="e3e3f-106">A file ([fileAttachment](../resources/fileattachment.md) resource)</span></span>
* <span data-ttu-id="e3e3f-107">Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md))</span><span class="sxs-lookup"><span data-stu-id="e3e3f-107">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource)</span></span>
* <span data-ttu-id="e3e3f-108">Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceattachment.md))</span><span class="sxs-lookup"><span data-stu-id="e3e3f-108">A link to a file ([referenceAttachment](../resources/referenceattachment.md) resource)</span></span>


## <a name="methods"></a><span data-ttu-id="e3e3f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e3e3f-109">Methods</span></span>

<span data-ttu-id="e3e3f-110">Los métodos siguientes se aplican a cualquiera de los tipos derivados de los datos adjuntos (**fileAttachment**, **itemAttachment** o **referenceAttachment**).</span><span class="sxs-lookup"><span data-stu-id="e3e3f-110">The following methods apply to any of the derived types of attachments (**fileAttachment**, **itemAttachment**, or **referenceAttachment**).</span></span>

| <span data-ttu-id="e3e3f-111">Método</span><span class="sxs-lookup"><span data-stu-id="e3e3f-111">Method</span></span>       | <span data-ttu-id="e3e3f-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3e3f-112">Return Type</span></span>  |<span data-ttu-id="e3e3f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3e3f-113">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e3e3f-114">Obtener datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="e3e3f-114">Get attachment</span></span>](../api/attachment-get.md) | [<span data-ttu-id="e3e3f-115">dato adjunto</span><span class="sxs-lookup"><span data-stu-id="e3e3f-115">attachment</span></span>](attachment.md) |<span data-ttu-id="e3e3f-116">Lea las propiedades y relaciones de un archivo adjunto, conectado a un evento, mensaje o publicación.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-116">Read the properties and relationships of an attachment, attached to an event, message, or post.</span></span>|
|[<span data-ttu-id="e3e3f-117">Agregar datos adjuntos a un evento</span><span class="sxs-lookup"><span data-stu-id="e3e3f-117">Add attachment to an event</span></span>](../api/event-post-attachments.md) | [<span data-ttu-id="e3e3f-118">attachment</span><span class="sxs-lookup"><span data-stu-id="e3e3f-118">attachment</span></span>](attachment.md) |<span data-ttu-id="e3e3f-119">Agregue un archivo, elemento o vínculo adjunto a un evento.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-119">Add a file, item, or link attachment to an event.</span></span>|
|[<span data-ttu-id="e3e3f-120">Agregar datos adjuntos a un mensaje</span><span class="sxs-lookup"><span data-stu-id="e3e3f-120">Add attachment to a message</span></span>](../api/message-post-attachments.md) | [<span data-ttu-id="e3e3f-121">attachment</span><span class="sxs-lookup"><span data-stu-id="e3e3f-121">attachment</span></span>](attachment.md) |<span data-ttu-id="e3e3f-122">Agregue un archivo, elemento o vínculo adjunto a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-122">Add a file, item, or link attachment to a message.</span></span>|
|[<span data-ttu-id="e3e3f-123">Agregar datos adjuntos a una publicación</span><span class="sxs-lookup"><span data-stu-id="e3e3f-123">Add attachment to a post</span></span>](../api/post-post-attachments.md) | [<span data-ttu-id="e3e3f-124">attachment</span><span class="sxs-lookup"><span data-stu-id="e3e3f-124">attachment</span></span>](attachment.md) |<span data-ttu-id="e3e3f-125">Agregue un archivo, elemento o vínculo adjunto a una publicación.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-125">Add a file, item, or link attachment to a post.</span></span>|
|[<span data-ttu-id="e3e3f-126">Mostrar los datos adjuntos de un evento</span><span class="sxs-lookup"><span data-stu-id="e3e3f-126">List attachments of an event</span></span>](../api/event-list-attachments.md) | <span data-ttu-id="e3e3f-127">Colección [attachment](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="e3e3f-127">[attachment](attachment.md) collection</span></span> | <span data-ttu-id="e3e3f-128">Obtenga una lista de los datos adjuntos de un evento.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-128">Get a list of attachments for an event.</span></span> |
|[<span data-ttu-id="e3e3f-129">Mostrar los datos adjuntos de un mensaje</span><span class="sxs-lookup"><span data-stu-id="e3e3f-129">List attachments of a message</span></span>](../api/message-list-attachments.md) | <span data-ttu-id="e3e3f-130">Colección [attachment](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="e3e3f-130">[attachment](attachment.md) collection</span></span> | <span data-ttu-id="e3e3f-131">Obtenga una lista de los datos adjuntos de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-131">Get a list of attachments for a message.</span></span> |
|[<span data-ttu-id="e3e3f-132">Mostrar los datos adjuntos de una publicación</span><span class="sxs-lookup"><span data-stu-id="e3e3f-132">List attachments of a post</span></span>](../api/post-list-attachments.md) | <span data-ttu-id="e3e3f-133">Colección [attachment](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="e3e3f-133">[attachment](attachment.md) collection</span></span> | <span data-ttu-id="e3e3f-134">Obtenga una lista de los datos adjuntos de una publicación.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-134">Get a list of attachments for a post.</span></span> |
|[<span data-ttu-id="e3e3f-135">Eliminar</span><span class="sxs-lookup"><span data-stu-id="e3e3f-135">Delete</span></span>](../api/attachment-delete.md) | <span data-ttu-id="e3e3f-136">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e3e3f-136">None</span></span> |<span data-ttu-id="e3e3f-137">Eliminar datos adjuntos en un evento, un mensaje o una publicación.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-137">Delete an attachment on an event, message, or post.</span></span> |

## <a name="properties"></a><span data-ttu-id="e3e3f-138">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e3e3f-138">Properties</span></span>

<span data-ttu-id="e3e3f-p101">A continuación se muestran las propiedades base de cualquier recurso de datos adjuntos. Haga referencia al tipo específico de dato adjunto ([fileAttachment](../resources/fileattachment.md), [itemAttachment](../resources/itemattachment.md) o [referenceAttachment](../resources/referenceattachment.md)) para ver propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-p101">The following are the base properties of any attachment resource. Refer to the specific type of attachment ([fileAttachment](../resources/fileattachment.md), [itemAttachment](../resources/itemattachment.md), or [referenceAttachment](../resources/referenceattachment.md)) for additional properties.</span></span>

| <span data-ttu-id="e3e3f-141">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e3e3f-141">Property</span></span>     | <span data-ttu-id="e3e3f-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3e3f-142">Type</span></span>   |<span data-ttu-id="e3e3f-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3e3f-143">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e3e3f-144">contentType</span><span class="sxs-lookup"><span data-stu-id="e3e3f-144">contentType</span></span>|<span data-ttu-id="e3e3f-145">String</span><span class="sxs-lookup"><span data-stu-id="e3e3f-145">String</span></span>|<span data-ttu-id="e3e3f-146">El tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-146">The MIME type.</span></span>|
|<span data-ttu-id="e3e3f-147">id</span><span class="sxs-lookup"><span data-stu-id="e3e3f-147">id</span></span>|<span data-ttu-id="e3e3f-148">String</span><span class="sxs-lookup"><span data-stu-id="e3e3f-148">String</span></span>| <span data-ttu-id="e3e3f-149">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-149">Read-only.</span></span>|
|<span data-ttu-id="e3e3f-150">isInline</span><span class="sxs-lookup"><span data-stu-id="e3e3f-150">isInline</span></span>|<span data-ttu-id="e3e3f-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="e3e3f-151">Boolean</span></span>|<span data-ttu-id="e3e3f-152">`true` si los datos adjuntos son datos adjuntos en línea; de lo contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-152">`true` if the attachment is an inline attachment; otherwise, `false`.</span></span>|
|<span data-ttu-id="e3e3f-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e3e3f-153">lastModifiedDateTime</span></span>|<span data-ttu-id="e3e3f-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e3e3f-154">DateTimeOffset</span></span>|<span data-ttu-id="e3e3f-p102">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="e3e3f-p102">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="e3e3f-157">name</span><span class="sxs-lookup"><span data-stu-id="e3e3f-157">name</span></span>|<span data-ttu-id="e3e3f-158">String</span><span class="sxs-lookup"><span data-stu-id="e3e3f-158">String</span></span>|<span data-ttu-id="e3e3f-159">El nombre de archivo de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-159">The attachment's file name.</span></span>|
|<span data-ttu-id="e3e3f-160">size</span><span class="sxs-lookup"><span data-stu-id="e3e3f-160">size</span></span>|<span data-ttu-id="e3e3f-161">Int32</span><span class="sxs-lookup"><span data-stu-id="e3e3f-161">Int32</span></span>|<span data-ttu-id="e3e3f-162">La longitud en bytes de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e3e3f-162">The length of the attachment in bytes.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e3e3f-163">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e3e3f-163">Relationships</span></span>
<span data-ttu-id="e3e3f-164">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e3e3f-164">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="e3e3f-165">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e3e3f-165">JSON representation</span></span>

<span data-ttu-id="e3e3f-166">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e3e3f-166">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "abstract": true,
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.attachment"
}-->

```json
{
  "contentType": "string",
  "id": "string (identifier)",
  "isInline": true,
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "size": 1024
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
