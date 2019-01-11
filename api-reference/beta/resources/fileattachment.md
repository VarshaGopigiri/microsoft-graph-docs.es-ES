---
title: Tipo de recurso fileAttachment
description: Un archivo (como un archivo de texto o un documento de Word) adjunto a un evento
localization_priority: Normal
ms.openlocfilehash: 7f7270bd5392e2d880daeb45491f4c65e9fca198
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27869282"
---
# <a name="fileattachment-resource-type"></a><span data-ttu-id="7ed9a-103">Tipo de recurso fileAttachment</span><span class="sxs-lookup"><span data-stu-id="7ed9a-103">fileAttachment resource type</span></span>

> <span data-ttu-id="7ed9a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7ed9a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7ed9a-106">Un archivo (como un archivo de texto o un documento de Word) adjunto a un [evento](../resources/event.md), [mensaje](../resources/message.md), [tarea de Outlook](../resources/outlooktask.md)o [Publicar](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="7ed9a-106">A file (such as a text file or Word document) attached to an [event](../resources/event.md), [message](../resources/message.md), [Outlook task](../resources/outlooktask.md), or [post](../resources/post.md).</span></span> <span data-ttu-id="7ed9a-107">La propiedad **contentBytes** contiene el contenido con codificación base64 del archivo.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-107">The  **contentBytes** property contains the base64-encoded contents of the file.</span></span>  

<span data-ttu-id="7ed9a-108">Al crear un archivo adjunto, incluya lo siguiente en el cuerpo de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="7ed9a-108">When creating a file attachment, include the following in the request body:</span></span>

* `"@odata.type": "#microsoft.graph.fileAttachment"`
* <span data-ttu-id="7ed9a-109">Las propiedades requeridas **name** y **contentBytes**.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-109">The required properties **name** and **contentBytes**.</span></span>

<span data-ttu-id="7ed9a-110">Derivadas de [attachment](attachment.md).</span><span class="sxs-lookup"><span data-stu-id="7ed9a-110">Derived from [attachment](attachment.md).</span></span>

## <a name="methods"></a><span data-ttu-id="7ed9a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="7ed9a-111">Methods</span></span>

| <span data-ttu-id="7ed9a-112">Método</span><span class="sxs-lookup"><span data-stu-id="7ed9a-112">Method</span></span>       | <span data-ttu-id="7ed9a-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ed9a-113">Return Type</span></span>  |<span data-ttu-id="7ed9a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ed9a-114">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="7ed9a-115">Get</span><span class="sxs-lookup"><span data-stu-id="7ed9a-115">Get</span></span>](../api/attachment-get.md) | [<span data-ttu-id="7ed9a-116">fileAttachment</span><span class="sxs-lookup"><span data-stu-id="7ed9a-116">fileAttachment</span></span>](fileattachment.md) |<span data-ttu-id="7ed9a-117">Lea las propiedades y las relaciones del objeto fileAttachment.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-117">Read properties and relationships of fileAttachment object.</span></span>|
|[<span data-ttu-id="7ed9a-118">Eliminar</span><span class="sxs-lookup"><span data-stu-id="7ed9a-118">Delete</span></span>](../api/attachment-delete.md) | <span data-ttu-id="7ed9a-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7ed9a-119">None</span></span> |<span data-ttu-id="7ed9a-120">Elimine el objeto fileAttachment.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-120">Delete fileAttachment object.</span></span> |

## <a name="properties"></a><span data-ttu-id="7ed9a-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ed9a-121">Properties</span></span>
| <span data-ttu-id="7ed9a-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7ed9a-122">Property</span></span>     | <span data-ttu-id="7ed9a-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="7ed9a-123">Type</span></span>   |<span data-ttu-id="7ed9a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ed9a-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7ed9a-125">contentBytes</span><span class="sxs-lookup"><span data-stu-id="7ed9a-125">contentBytes</span></span>|<span data-ttu-id="7ed9a-126">Binario</span><span class="sxs-lookup"><span data-stu-id="7ed9a-126">Binary</span></span>|<span data-ttu-id="7ed9a-127">El contenido del archivo codificado en base64.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-127">The base64-encoded contents of the file.</span></span>|
|<span data-ttu-id="7ed9a-128">contentId</span><span class="sxs-lookup"><span data-stu-id="7ed9a-128">contentId</span></span>|<span data-ttu-id="7ed9a-129">String</span><span class="sxs-lookup"><span data-stu-id="7ed9a-129">String</span></span>|<span data-ttu-id="7ed9a-130">El identificador de los datos de adjuntos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-130">The ID of the attachment in the Exchange store.</span></span>|
|<span data-ttu-id="7ed9a-131">contentLocation</span><span class="sxs-lookup"><span data-stu-id="7ed9a-131">contentLocation</span></span>|<span data-ttu-id="7ed9a-132">String</span><span class="sxs-lookup"><span data-stu-id="7ed9a-132">String</span></span>|<span data-ttu-id="7ed9a-133">El identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-133">The Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>|
|<span data-ttu-id="7ed9a-134">contentType</span><span class="sxs-lookup"><span data-stu-id="7ed9a-134">contentType</span></span>|<span data-ttu-id="7ed9a-135">String</span><span class="sxs-lookup"><span data-stu-id="7ed9a-135">String</span></span>|<span data-ttu-id="7ed9a-136">El tipo de contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-136">The content type of the attachment.</span></span>|
|<span data-ttu-id="7ed9a-137">id</span><span class="sxs-lookup"><span data-stu-id="7ed9a-137">id</span></span>|<span data-ttu-id="7ed9a-138">String</span><span class="sxs-lookup"><span data-stu-id="7ed9a-138">String</span></span>|<span data-ttu-id="7ed9a-139">El identificador de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-139">The attachment ID.</span></span>|
|<span data-ttu-id="7ed9a-140">isInline</span><span class="sxs-lookup"><span data-stu-id="7ed9a-140">isInline</span></span>|<span data-ttu-id="7ed9a-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="7ed9a-141">Boolean</span></span>|<span data-ttu-id="7ed9a-142">Se establece en true si se trata de datos adjuntos en línea.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-142">Set to true if this is an inline attachment.</span></span>|
|<span data-ttu-id="7ed9a-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7ed9a-143">lastModifiedDateTime</span></span>|<span data-ttu-id="7ed9a-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7ed9a-144">DateTimeOffset</span></span>|<span data-ttu-id="7ed9a-145">La fecha y hora de la última modificación de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-145">The date and time when the attachment was last modified.</span></span>|
|<span data-ttu-id="7ed9a-146">name</span><span class="sxs-lookup"><span data-stu-id="7ed9a-146">name</span></span>|<span data-ttu-id="7ed9a-147">String</span><span class="sxs-lookup"><span data-stu-id="7ed9a-147">String</span></span>|<span data-ttu-id="7ed9a-148">El nombre que representa el texto que aparece debajo del icono que representa el archivo adjunto insertado. No tiene que ser el nombre de archivo real.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-148">The name representing the text that is displayed below the icon representing the embedded attachment.This does not need to be the actual file name.</span></span>|
|<span data-ttu-id="7ed9a-149">size</span><span class="sxs-lookup"><span data-stu-id="7ed9a-149">size</span></span>|<span data-ttu-id="7ed9a-150">Int32</span><span class="sxs-lookup"><span data-stu-id="7ed9a-150">Int32</span></span>|<span data-ttu-id="7ed9a-151">El tamaño en bytes de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-151">The size in bytes of the attachment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7ed9a-152">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7ed9a-152">Relationships</span></span>
<span data-ttu-id="7ed9a-153">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7ed9a-153">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="7ed9a-154">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7ed9a-154">JSON representation</span></span>

<span data-ttu-id="7ed9a-155">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7ed9a-155">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileAttachment"
}-->

```json
{
  "contentBytes": "binary",
  "contentId": "string",
  "contentLocation": "string",
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
  "description": "fileAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
