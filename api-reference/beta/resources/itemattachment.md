---
title: Tipo de recurso itemAttachment
description: Un contacto, evento o mensaje que está unido a otro evento,
ms.openlocfilehash: fd8638a7d263c2ebbe09c77f717af989e1dd5a0e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088570"
---
# <a name="itemattachment-resource-type"></a><span data-ttu-id="870e2-103">Tipo de recurso itemAttachment</span><span class="sxs-lookup"><span data-stu-id="870e2-103">itemAttachment resource type</span></span>

> <span data-ttu-id="870e2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="870e2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="870e2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="870e2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="870e2-106">Un contacto, evento o mensaje que está unido a otro [evento](../resources/event.md), [mensaje](../resources/message.md), [tarea de Outlook](../resources/outlooktask.md)o [Publicar](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="870e2-106">A contact, event, or message that's attached to another [event](../resources/event.md), [message](../resources/message.md), [Outlook task](../resources/outlooktask.md), or [post](../resources/post.md).</span></span>  

<span data-ttu-id="870e2-107">Derivado de [attachment](attachment.md).</span><span class="sxs-lookup"><span data-stu-id="870e2-107">Derived from [attachment](attachment.md).</span></span>

## <a name="methods"></a><span data-ttu-id="870e2-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="870e2-108">Methods</span></span>

| <span data-ttu-id="870e2-109">Método</span><span class="sxs-lookup"><span data-stu-id="870e2-109">Method</span></span>       | <span data-ttu-id="870e2-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="870e2-110">Return Type</span></span>  |<span data-ttu-id="870e2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="870e2-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="870e2-112">Get</span><span class="sxs-lookup"><span data-stu-id="870e2-112">Get</span></span>](../api/attachment-get.md) | [<span data-ttu-id="870e2-113">itemAttachment</span><span class="sxs-lookup"><span data-stu-id="870e2-113">itemAttachment</span></span>](itemattachment.md) |<span data-ttu-id="870e2-114">Lee las propiedades y relaciones del objeto itemAttachment.</span><span class="sxs-lookup"><span data-stu-id="870e2-114">Read properties and relationships of itemAttachment object.</span></span>|
|[<span data-ttu-id="870e2-115">Delete</span><span class="sxs-lookup"><span data-stu-id="870e2-115">Delete</span></span>](../api/attachment-delete.md) | <span data-ttu-id="870e2-116">None</span><span class="sxs-lookup"><span data-stu-id="870e2-116">None</span></span> |<span data-ttu-id="870e2-117">Elimina el objeto itemAttachment.</span><span class="sxs-lookup"><span data-stu-id="870e2-117">Delete itemAttachment object.</span></span> |

## <a name="properties"></a><span data-ttu-id="870e2-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="870e2-118">Properties</span></span>
| <span data-ttu-id="870e2-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="870e2-119">Property</span></span>     | <span data-ttu-id="870e2-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="870e2-120">Type</span></span>   |<span data-ttu-id="870e2-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="870e2-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="870e2-122">contentType</span><span class="sxs-lookup"><span data-stu-id="870e2-122">contentType</span></span>|<span data-ttu-id="870e2-123">String</span><span class="sxs-lookup"><span data-stu-id="870e2-123">String</span></span>|<span data-ttu-id="870e2-124">El tipo de contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="870e2-124">The content type of the attachment.</span></span>|
|<span data-ttu-id="870e2-125">id</span><span class="sxs-lookup"><span data-stu-id="870e2-125">id</span></span>|<span data-ttu-id="870e2-126">String</span><span class="sxs-lookup"><span data-stu-id="870e2-126">String</span></span>| <span data-ttu-id="870e2-127">El identificador de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="870e2-127">The attachment ID.</span></span>|
|<span data-ttu-id="870e2-128">isInline</span><span class="sxs-lookup"><span data-stu-id="870e2-128">isInline</span></span>|<span data-ttu-id="870e2-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="870e2-129">Boolean</span></span>|<span data-ttu-id="870e2-130">Se establece en true si los datos adjuntos están insertados, como una imagen incrustada en el cuerpo del elemento.</span><span class="sxs-lookup"><span data-stu-id="870e2-130">Set to true if the attachment is inline, such as an embedded image within the body of the item.</span></span>|
|<span data-ttu-id="870e2-131">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="870e2-131">lastModifiedDateTime</span></span>|<span data-ttu-id="870e2-132">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="870e2-132">DateTimeOffset</span></span>|<span data-ttu-id="870e2-133">Última fecha y hora en que se modificaron los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="870e2-133">The last time and date that the attachment was modified.</span></span>|
|<span data-ttu-id="870e2-134">name</span><span class="sxs-lookup"><span data-stu-id="870e2-134">name</span></span>|<span data-ttu-id="870e2-135">String</span><span class="sxs-lookup"><span data-stu-id="870e2-135">String</span></span>|<span data-ttu-id="870e2-136">Nombre para mostrar de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="870e2-136">The display name of the attachment.</span></span>|
|<span data-ttu-id="870e2-137">size</span><span class="sxs-lookup"><span data-stu-id="870e2-137">size</span></span>|<span data-ttu-id="870e2-138">Int32</span><span class="sxs-lookup"><span data-stu-id="870e2-138">Int32</span></span>|<span data-ttu-id="870e2-139">El tamaño en bytes de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="870e2-139">The size in bytes of the attachment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="870e2-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="870e2-140">Relationships</span></span>
| <span data-ttu-id="870e2-141">Relación</span><span class="sxs-lookup"><span data-stu-id="870e2-141">Relationship</span></span> | <span data-ttu-id="870e2-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="870e2-142">Type</span></span>   |<span data-ttu-id="870e2-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="870e2-143">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="870e2-144">item</span><span class="sxs-lookup"><span data-stu-id="870e2-144">item</span></span>|[<span data-ttu-id="870e2-145">OutlookItem</span><span class="sxs-lookup"><span data-stu-id="870e2-145">OutlookItem</span></span>](outlookitem.md)|<span data-ttu-id="870e2-146">El contacto adjunto, mensaje o evento.</span><span class="sxs-lookup"><span data-stu-id="870e2-146">The attached contact, message or event.</span></span> <span data-ttu-id="870e2-147">Propiedad de navegación.</span><span class="sxs-lookup"><span data-stu-id="870e2-147">Navigation property.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="870e2-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="870e2-148">JSON representation</span></span>

<span data-ttu-id="870e2-149">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="870e2-149">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "item"
  ],
  "@odata.type": "microsoft.graph.itemAttachment"
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
  "description": "itemAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
