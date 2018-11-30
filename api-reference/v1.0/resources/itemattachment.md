---
title: Tipo de recurso itemAttachment
description: 'Contacto, evento o mensaje que se adjunta a otro evento, mensaje o publicación.  '
ms.openlocfilehash: 79097b10327d895a41090e068a2fd8e9681df125
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030457"
---
# <a name="itemattachment-resource-type"></a><span data-ttu-id="0b0c3-103">Tipo de recurso itemAttachment</span><span class="sxs-lookup"><span data-stu-id="0b0c3-103">itemAttachment resource type</span></span>

<span data-ttu-id="0b0c3-104">Contacto, evento o mensaje que se adjunta a otro evento, mensaje o publicación.</span><span class="sxs-lookup"><span data-stu-id="0b0c3-104">A contact, event, or message that's attached to another event, message, or post.</span></span>  

<span data-ttu-id="0b0c3-105">Derivado de [attachment](attachment.md).</span><span class="sxs-lookup"><span data-stu-id="0b0c3-105">Derived from [attachment](attachment.md).</span></span>

## <a name="methods"></a><span data-ttu-id="0b0c3-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b0c3-106">Methods</span></span>

| <span data-ttu-id="0b0c3-107">Método</span><span class="sxs-lookup"><span data-stu-id="0b0c3-107">Method</span></span>       | <span data-ttu-id="0b0c3-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b0c3-108">Return Type</span></span>  |<span data-ttu-id="0b0c3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b0c3-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="0b0c3-110">Get</span><span class="sxs-lookup"><span data-stu-id="0b0c3-110">Get</span></span>](../api/attachment-get.md) | [<span data-ttu-id="0b0c3-111">itemAttachment</span><span class="sxs-lookup"><span data-stu-id="0b0c3-111">itemAttachment</span></span>](itemattachment.md) |<span data-ttu-id="0b0c3-112">Lee las propiedades y relaciones del objeto itemAttachment.</span><span class="sxs-lookup"><span data-stu-id="0b0c3-112">Read properties and relationships of itemAttachment object.</span></span>|
|[<span data-ttu-id="0b0c3-113">Delete</span><span class="sxs-lookup"><span data-stu-id="0b0c3-113">Delete</span></span>](../api/attachment-delete.md) | <span data-ttu-id="0b0c3-114">None</span><span class="sxs-lookup"><span data-stu-id="0b0c3-114">None</span></span> |<span data-ttu-id="0b0c3-115">Elimina el objeto itemAttachment.</span><span class="sxs-lookup"><span data-stu-id="0b0c3-115">Delete itemAttachment object.</span></span> |

## <a name="properties"></a><span data-ttu-id="0b0c3-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b0c3-116">Properties</span></span>
| <span data-ttu-id="0b0c3-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0b0c3-117">Property</span></span>     | <span data-ttu-id="0b0c3-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b0c3-118">Type</span></span>   |<span data-ttu-id="0b0c3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b0c3-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0b0c3-120">contentType</span><span class="sxs-lookup"><span data-stu-id="0b0c3-120">contentType</span></span>|<span data-ttu-id="0b0c3-121">String</span><span class="sxs-lookup"><span data-stu-id="0b0c3-121">String</span></span>|<span data-ttu-id="0b0c3-122">El tipo de contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0b0c3-122">The content type of the attachment.</span></span>|
|<span data-ttu-id="0b0c3-123">id</span><span class="sxs-lookup"><span data-stu-id="0b0c3-123">id</span></span>|<span data-ttu-id="0b0c3-124">String</span><span class="sxs-lookup"><span data-stu-id="0b0c3-124">String</span></span>| <span data-ttu-id="0b0c3-125">El identificador de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0b0c3-125">The attachment ID.</span></span>|
|<span data-ttu-id="0b0c3-126">isInline</span><span class="sxs-lookup"><span data-stu-id="0b0c3-126">isInline</span></span>|<span data-ttu-id="0b0c3-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b0c3-127">Boolean</span></span>|<span data-ttu-id="0b0c3-128">Se establece en true si los datos adjuntos están insertados, como una imagen incrustada en el cuerpo del elemento.</span><span class="sxs-lookup"><span data-stu-id="0b0c3-128">Set to true if the attachment is inline, such as an embedded image within the body of the item.</span></span>|
|<span data-ttu-id="0b0c3-129">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0b0c3-129">lastModifiedDateTime</span></span>|<span data-ttu-id="0b0c3-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0b0c3-130">DateTimeOffset</span></span>|<span data-ttu-id="0b0c3-131">Última fecha y hora en que se modificaron los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0b0c3-131">The last time and date that the attachment was modified.</span></span>|
|<span data-ttu-id="0b0c3-132">name</span><span class="sxs-lookup"><span data-stu-id="0b0c3-132">name</span></span>|<span data-ttu-id="0b0c3-133">String</span><span class="sxs-lookup"><span data-stu-id="0b0c3-133">String</span></span>|<span data-ttu-id="0b0c3-134">Nombre para mostrar de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0b0c3-134">The display name of the attachment.</span></span>|
|<span data-ttu-id="0b0c3-135">size</span><span class="sxs-lookup"><span data-stu-id="0b0c3-135">size</span></span>|<span data-ttu-id="0b0c3-136">Int32</span><span class="sxs-lookup"><span data-stu-id="0b0c3-136">Int32</span></span>|<span data-ttu-id="0b0c3-137">El tamaño en bytes de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0b0c3-137">The size in bytes of the attachment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="0b0c3-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0b0c3-138">Relationships</span></span>
| <span data-ttu-id="0b0c3-139">Relación</span><span class="sxs-lookup"><span data-stu-id="0b0c3-139">Relationship</span></span> | <span data-ttu-id="0b0c3-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b0c3-140">Type</span></span>   |<span data-ttu-id="0b0c3-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b0c3-141">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0b0c3-142">item</span><span class="sxs-lookup"><span data-stu-id="0b0c3-142">item</span></span>|[<span data-ttu-id="0b0c3-143">OutlookItem</span><span class="sxs-lookup"><span data-stu-id="0b0c3-143">OutlookItem</span></span>](outlookitem.md)|<span data-ttu-id="0b0c3-p101">Evento o mensaje adjunto. Propiedad de navegación.</span><span class="sxs-lookup"><span data-stu-id="0b0c3-p101">The attached message or event. Navigation property.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="0b0c3-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0b0c3-146">JSON representation</span></span>

<span data-ttu-id="0b0c3-147">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0b0c3-147">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "item"
  ],
  "baseType": "microsoft.graph.attachment",
  "@odata.type": "microsoft.graph.itemAttachment",
  "@odata.annotations": [
    {
      "property": "item",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "insertable": false,
        "searchable": false,
        "updatable": false
      }
    }
  ]
}-->

```json
{
  "contentType": "string",
  "id": "string (identifier)",
  "isInline": true,
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "size": 1024,
  "item": { "@odata.type": "microsoft.graph.outlookItem" }
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
