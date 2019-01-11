---
title: Tipo de recurso itemAttachment
description: 'Contacto, evento o mensaje que se adjunta a otro evento, mensaje o publicación.  '
localization_priority: Priority
ms.openlocfilehash: df996175e545b78f4ca9a1b6271b9cb012ffffce
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853525"
---
# <a name="itemattachment-resource-type"></a><span data-ttu-id="d6e2f-103">Tipo de recurso itemAttachment</span><span class="sxs-lookup"><span data-stu-id="d6e2f-103">itemAttachment resource type</span></span>

<span data-ttu-id="d6e2f-104">Contacto, evento o mensaje que se adjunta a otro evento, mensaje o publicación.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-104">A contact, event, or message that's attached to another event, message, or post.</span></span>  

<span data-ttu-id="d6e2f-105">Derivado de [attachment](attachment.md).</span><span class="sxs-lookup"><span data-stu-id="d6e2f-105">Derived from [attachment](attachment.md).</span></span>

## <a name="methods"></a><span data-ttu-id="d6e2f-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="d6e2f-106">Methods</span></span>

| <span data-ttu-id="d6e2f-107">Método</span><span class="sxs-lookup"><span data-stu-id="d6e2f-107">Method</span></span>       | <span data-ttu-id="d6e2f-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6e2f-108">Return Type</span></span>  |<span data-ttu-id="d6e2f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6e2f-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d6e2f-110">Get</span><span class="sxs-lookup"><span data-stu-id="d6e2f-110">Get</span></span>](../api/attachment-get.md) | [<span data-ttu-id="d6e2f-111">itemAttachment</span><span class="sxs-lookup"><span data-stu-id="d6e2f-111">itemAttachment</span></span>](itemattachment.md) |<span data-ttu-id="d6e2f-112">Lee las propiedades y relaciones del objeto itemAttachment.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-112">Read properties and relationships of itemAttachment object.</span></span>|
|[<span data-ttu-id="d6e2f-113">Delete</span><span class="sxs-lookup"><span data-stu-id="d6e2f-113">Delete</span></span>](../api/attachment-delete.md) | <span data-ttu-id="d6e2f-114">None</span><span class="sxs-lookup"><span data-stu-id="d6e2f-114">None</span></span> |<span data-ttu-id="d6e2f-115">Elimina el objeto itemAttachment.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-115">Delete itemAttachment object.</span></span> |

## <a name="properties"></a><span data-ttu-id="d6e2f-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6e2f-116">Properties</span></span>
| <span data-ttu-id="d6e2f-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d6e2f-117">Property</span></span>     | <span data-ttu-id="d6e2f-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6e2f-118">Type</span></span>   |<span data-ttu-id="d6e2f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6e2f-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d6e2f-120">contentType</span><span class="sxs-lookup"><span data-stu-id="d6e2f-120">contentType</span></span>|<span data-ttu-id="d6e2f-121">String</span><span class="sxs-lookup"><span data-stu-id="d6e2f-121">String</span></span>|<span data-ttu-id="d6e2f-122">El tipo de contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-122">The content type of the attachment.</span></span>|
|<span data-ttu-id="d6e2f-123">id</span><span class="sxs-lookup"><span data-stu-id="d6e2f-123">id</span></span>|<span data-ttu-id="d6e2f-124">String</span><span class="sxs-lookup"><span data-stu-id="d6e2f-124">String</span></span>| <span data-ttu-id="d6e2f-125">El identificador de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-125">The attachment ID.</span></span>|
|<span data-ttu-id="d6e2f-126">isInline</span><span class="sxs-lookup"><span data-stu-id="d6e2f-126">isInline</span></span>|<span data-ttu-id="d6e2f-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="d6e2f-127">Boolean</span></span>|<span data-ttu-id="d6e2f-128">Se establece en true si los datos adjuntos están insertados, como una imagen incrustada en el cuerpo del elemento.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-128">Set to true if the attachment is inline, such as an embedded image within the body of the item.</span></span>|
|<span data-ttu-id="d6e2f-129">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d6e2f-129">lastModifiedDateTime</span></span>|<span data-ttu-id="d6e2f-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d6e2f-130">DateTimeOffset</span></span>|<span data-ttu-id="d6e2f-131">Última fecha y hora en que se modificaron los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-131">The last time and date that the attachment was modified.</span></span>|
|<span data-ttu-id="d6e2f-132">name</span><span class="sxs-lookup"><span data-stu-id="d6e2f-132">name</span></span>|<span data-ttu-id="d6e2f-133">String</span><span class="sxs-lookup"><span data-stu-id="d6e2f-133">String</span></span>|<span data-ttu-id="d6e2f-134">Nombre para mostrar de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-134">The display name of the attachment.</span></span>|
|<span data-ttu-id="d6e2f-135">size</span><span class="sxs-lookup"><span data-stu-id="d6e2f-135">size</span></span>|<span data-ttu-id="d6e2f-136">Int32</span><span class="sxs-lookup"><span data-stu-id="d6e2f-136">Int32</span></span>|<span data-ttu-id="d6e2f-137">El tamaño en bytes de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-137">The size in bytes of the attachment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d6e2f-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d6e2f-138">Relationships</span></span>
| <span data-ttu-id="d6e2f-139">Relación</span><span class="sxs-lookup"><span data-stu-id="d6e2f-139">Relationship</span></span> | <span data-ttu-id="d6e2f-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6e2f-140">Type</span></span>   |<span data-ttu-id="d6e2f-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6e2f-141">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d6e2f-142">item</span><span class="sxs-lookup"><span data-stu-id="d6e2f-142">item</span></span>|[<span data-ttu-id="d6e2f-143">OutlookItem</span><span class="sxs-lookup"><span data-stu-id="d6e2f-143">OutlookItem</span></span>](outlookitem.md)|<span data-ttu-id="d6e2f-p101">Evento o mensaje adjunto. Propiedad de navegación.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-p101">The attached message or event. Navigation property.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d6e2f-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d6e2f-146">JSON representation</span></span>

<span data-ttu-id="d6e2f-147">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d6e2f-147">Here is a JSON representation of the resource</span></span>

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
