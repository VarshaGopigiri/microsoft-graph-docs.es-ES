---
title: Tipo de recurso attachment
description: Puede agregar contenido relacionado a un evento
ms.openlocfilehash: f0bb9ec37d2fe3d034dce9532ad316d371c4937e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090479"
---
# <a name="attachment-resource-type"></a><span data-ttu-id="8dead-103">Tipo de recurso attachment</span><span class="sxs-lookup"><span data-stu-id="8dead-103">attachment resource type</span></span>

> <span data-ttu-id="8dead-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8dead-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8dead-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8dead-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8dead-106">Puede agregar contenido relacionado a un [evento](../resources/event.md), [mensaje](../resources/message.md), [tarea de Outlook](../resources/outlooktask.md)o [registrar](../resources/post.md) en el formulario de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8dead-106">You can add related content to an [event](../resources/event.md), [message](../resources/message.md), [Outlook task](../resources/outlooktask.md), or [post](../resources/post.md) in the form of an attachment.</span></span>

<span data-ttu-id="8dead-107">**datos adjuntos** es el recurso base para los siguientes tipos de datos adjuntos derivados:</span><span class="sxs-lookup"><span data-stu-id="8dead-107">**attachment** is the base resource for the following derived types of attachments:</span></span>

* <span data-ttu-id="8dead-108">Un archivo (recurso [fileAttachment](../resources/fileattachment.md))</span><span class="sxs-lookup"><span data-stu-id="8dead-108">A file ([fileAttachment](../resources/fileattachment.md) resource)</span></span>
* <span data-ttu-id="8dead-109">Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md))</span><span class="sxs-lookup"><span data-stu-id="8dead-109">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource)</span></span>
* <span data-ttu-id="8dead-110">Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceattachment.md))</span><span class="sxs-lookup"><span data-stu-id="8dead-110">A link to a file ([referenceAttachment](../resources/referenceattachment.md) resource)</span></span>

## <a name="methods"></a><span data-ttu-id="8dead-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="8dead-111">Methods</span></span>

<span data-ttu-id="8dead-112">Los métodos siguientes se aplican a cualquiera de los tipos derivados de los datos adjuntos (**fileAttachment**, **itemAttachment** o **referenceAttachment**).</span><span class="sxs-lookup"><span data-stu-id="8dead-112">The following methods apply to any of the derived types of attachments (**fileAttachment**, **itemAttachment**, or **referenceAttachment**).</span></span>

| <span data-ttu-id="8dead-113">Método</span><span class="sxs-lookup"><span data-stu-id="8dead-113">Method</span></span>       | <span data-ttu-id="8dead-114">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8dead-114">Return Type</span></span>  |<span data-ttu-id="8dead-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8dead-115">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="8dead-116">Obtener datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="8dead-116">Get attachment</span></span>](../api/attachment-get.md) | [<span data-ttu-id="8dead-117">dato adjunto</span><span class="sxs-lookup"><span data-stu-id="8dead-117">attachment</span></span>](attachment.md) |<span data-ttu-id="8dead-118">Lea las propiedades y relaciones de los datos adjuntos, conectado a un evento, mensaje, tarea de Outlook o posterior.</span><span class="sxs-lookup"><span data-stu-id="8dead-118">Read the properties and relationships of an attachment, attached to an event, message, Outlook task, or post.</span></span>|
|[<span data-ttu-id="8dead-119">Agregar datos adjuntos a un evento</span><span class="sxs-lookup"><span data-stu-id="8dead-119">Add attachment to an event</span></span>](../api/event-post-attachments.md) | [<span data-ttu-id="8dead-120">attachment</span><span class="sxs-lookup"><span data-stu-id="8dead-120">attachment</span></span>](attachment.md) |<span data-ttu-id="8dead-121">Agregue un archivo, elemento o vínculo adjunto a un evento.</span><span class="sxs-lookup"><span data-stu-id="8dead-121">Add a file, item, or link attachment to an event.</span></span>|
|[<span data-ttu-id="8dead-122">Agregar datos adjuntos a un mensaje</span><span class="sxs-lookup"><span data-stu-id="8dead-122">Add attachment to a message</span></span>](../api/message-post-attachments.md) | [<span data-ttu-id="8dead-123">attachment</span><span class="sxs-lookup"><span data-stu-id="8dead-123">attachment</span></span>](attachment.md) |<span data-ttu-id="8dead-124">Agregue un archivo, elemento o vínculo adjunto a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8dead-124">Add a file, item, or link attachment to a message.</span></span>|
|[<span data-ttu-id="8dead-125">Agregar datos adjuntos a una tarea de Outlook</span><span class="sxs-lookup"><span data-stu-id="8dead-125">Add attachment to an Outlook task</span></span>](../api/outlooktask-post-attachments.md) | [<span data-ttu-id="8dead-126">attachment</span><span class="sxs-lookup"><span data-stu-id="8dead-126">attachment</span></span>](attachment.md) |<span data-ttu-id="8dead-127">Agregar un archivo, el elemento o los datos adjuntos de vínculo a una tarea de Outlook.</span><span class="sxs-lookup"><span data-stu-id="8dead-127">Add a file, item, or link attachment to an Outlook task.</span></span>|
|[<span data-ttu-id="8dead-128">Agregar datos adjuntos a una publicación</span><span class="sxs-lookup"><span data-stu-id="8dead-128">Add attachment to a post</span></span>](../api/post-post-attachments.md) | [<span data-ttu-id="8dead-129">attachment</span><span class="sxs-lookup"><span data-stu-id="8dead-129">attachment</span></span>](attachment.md) |<span data-ttu-id="8dead-130">Agregue un archivo, elemento o vínculo adjunto a una publicación.</span><span class="sxs-lookup"><span data-stu-id="8dead-130">Add a file, item, or link attachment to a post.</span></span>|
|[<span data-ttu-id="8dead-131">Mostrar los datos adjuntos de un evento</span><span class="sxs-lookup"><span data-stu-id="8dead-131">List attachments of an event</span></span>](../api/event-list-attachments.md) | <span data-ttu-id="8dead-132">Colección [attachment](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="8dead-132">[attachment](attachment.md) collection</span></span> | <span data-ttu-id="8dead-133">Obtenga una lista de los datos adjuntos de un evento.</span><span class="sxs-lookup"><span data-stu-id="8dead-133">Get a list of attachments for an event.</span></span> |
|[<span data-ttu-id="8dead-134">Mostrar los datos adjuntos de un mensaje</span><span class="sxs-lookup"><span data-stu-id="8dead-134">List attachments of a message</span></span>](../api/message-list-attachments.md) | <span data-ttu-id="8dead-135">Colección [attachment](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="8dead-135">[attachment](attachment.md) collection</span></span> | <span data-ttu-id="8dead-136">Obtenga una lista de los datos adjuntos de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8dead-136">Get a list of attachments for a message.</span></span> |
|[<span data-ttu-id="8dead-137">Datos adjuntos de la lista de una tarea de Outlook</span><span class="sxs-lookup"><span data-stu-id="8dead-137">List attachments of an Outlook task</span></span>](../api/outlooktask-list-attachments.md) | <span data-ttu-id="8dead-138">Colección de [datos adjuntos](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="8dead-138">[attachment](attachment.md) collection</span></span> | <span data-ttu-id="8dead-139">Obtener una lista de datos adjuntos para una tarea de Outlook.</span><span class="sxs-lookup"><span data-stu-id="8dead-139">Get a list of attachments for an Outlook task.</span></span> |
|[<span data-ttu-id="8dead-140">Mostrar los datos adjuntos de una publicación</span><span class="sxs-lookup"><span data-stu-id="8dead-140">List attachments of a post</span></span>](../api/post-list-attachments.md) | <span data-ttu-id="8dead-141">Colección [attachment](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="8dead-141">[attachment](attachment.md) collection</span></span> | <span data-ttu-id="8dead-142">Obtenga una lista de los datos adjuntos de una publicación.</span><span class="sxs-lookup"><span data-stu-id="8dead-142">Get a list of attachments for a post.</span></span> |
|[<span data-ttu-id="8dead-143">Eliminar</span><span class="sxs-lookup"><span data-stu-id="8dead-143">Delete</span></span>](../api/attachment-delete.md) | <span data-ttu-id="8dead-144">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8dead-144">None</span></span> |<span data-ttu-id="8dead-145">Eliminar un dato adjunto en un evento, el mensaje, la tarea de Outlook o el post.</span><span class="sxs-lookup"><span data-stu-id="8dead-145">Delete an attachment on an event, message, Outlook task, or post.</span></span> |

## <a name="properties"></a><span data-ttu-id="8dead-146">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8dead-146">Properties</span></span>

<span data-ttu-id="8dead-p102">A continuación se muestran las propiedades base de cualquier recurso de datos adjuntos. Haga referencia al tipo específico de dato adjunto ([fileAttachment](../resources/fileattachment.md), [itemAttachment](../resources/itemattachment.md) o [referenceAttachment](../resources/referenceattachment.md)) para ver propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="8dead-p102">The following are the base properties of any attachment resource. Refer to the specific type of attachment ([fileAttachment](../resources/fileattachment.md), [itemAttachment](../resources/itemattachment.md), or [referenceAttachment](../resources/referenceattachment.md)) for additional properties.</span></span>

| <span data-ttu-id="8dead-149">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8dead-149">Property</span></span>     | <span data-ttu-id="8dead-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="8dead-150">Type</span></span>   |<span data-ttu-id="8dead-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="8dead-151">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8dead-152">contentType</span><span class="sxs-lookup"><span data-stu-id="8dead-152">contentType</span></span>|<span data-ttu-id="8dead-153">String</span><span class="sxs-lookup"><span data-stu-id="8dead-153">String</span></span>|<span data-ttu-id="8dead-154">El tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="8dead-154">The MIME type.</span></span>|
|<span data-ttu-id="8dead-155">id</span><span class="sxs-lookup"><span data-stu-id="8dead-155">id</span></span>|<span data-ttu-id="8dead-156">String</span><span class="sxs-lookup"><span data-stu-id="8dead-156">String</span></span>| <span data-ttu-id="8dead-157">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8dead-157">Read-only.</span></span>|
|<span data-ttu-id="8dead-158">isInline</span><span class="sxs-lookup"><span data-stu-id="8dead-158">isInline</span></span>|<span data-ttu-id="8dead-159">Boolean</span><span class="sxs-lookup"><span data-stu-id="8dead-159">Boolean</span></span>|<span data-ttu-id="8dead-160">`true` si los datos adjuntos son datos adjuntos en línea; de lo contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="8dead-160">`true` if the attachment is an inline attachment; otherwise, `false`.</span></span>|
|<span data-ttu-id="8dead-161">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8dead-161">lastModifiedDateTime</span></span>|<span data-ttu-id="8dead-162">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8dead-162">DateTimeOffset</span></span>|<span data-ttu-id="8dead-p103">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="8dead-p103">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="8dead-165">name</span><span class="sxs-lookup"><span data-stu-id="8dead-165">name</span></span>|<span data-ttu-id="8dead-166">String</span><span class="sxs-lookup"><span data-stu-id="8dead-166">String</span></span>|<span data-ttu-id="8dead-167">Nombre para mostrar de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8dead-167">The display name of the attachment.</span></span> <span data-ttu-id="8dead-168">Esto no necesita ser el nombre de archivo real.</span><span class="sxs-lookup"><span data-stu-id="8dead-168">This does not need to be the actual file name.</span></span>|
|<span data-ttu-id="8dead-169">size</span><span class="sxs-lookup"><span data-stu-id="8dead-169">size</span></span>|<span data-ttu-id="8dead-170">Int32</span><span class="sxs-lookup"><span data-stu-id="8dead-170">Int32</span></span>|<span data-ttu-id="8dead-171">La longitud en bytes de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8dead-171">The length of the attachment in bytes.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8dead-172">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8dead-172">Relationships</span></span>
<span data-ttu-id="8dead-173">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8dead-173">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="8dead-174">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8dead-174">JSON representation</span></span>

<span data-ttu-id="8dead-175">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8dead-175">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
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
