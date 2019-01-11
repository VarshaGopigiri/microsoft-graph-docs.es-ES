---
title: Tipo de recurso fileAttachment
description: 'Un archivo (como un archivo de texto o un documento de Word) conectado a un evento, mensaje o post. El **contentBytes** '
localization_priority: Priority
ms.openlocfilehash: 81de7a12ca371158d7f6369861a8a197fd544821
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870059"
---
# <a name="fileattachment-resource-type"></a><span data-ttu-id="ac354-104">Tipo de recurso fileAttachment</span><span class="sxs-lookup"><span data-stu-id="ac354-104">fileAttachment resource type</span></span>

<span data-ttu-id="ac354-p102">Un archivo (como un archivo de texto o un documento de Word) adjunto a un evento, mensaje o publicación. La propiedad **contentBytes** contiene el contenido codificado en base64 del archivo.</span><span class="sxs-lookup"><span data-stu-id="ac354-p102">A file (such as a text file or Word document) attached to an event, message or post. The  **contentBytes** property contains the base64-encoded contents of the file.</span></span>  

<span data-ttu-id="ac354-107">Al crear un archivo adjunto, incluya lo siguiente en el cuerpo de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="ac354-107">When creating a file attachment, include the following in the request body:</span></span>

* `"@odata.type": "#microsoft.graph.fileAttachment"`
* <span data-ttu-id="ac354-108">Las propiedades requeridas **name** y **contentBytes**.</span><span class="sxs-lookup"><span data-stu-id="ac354-108">The required properties **name** and **contentBytes**.</span></span>

<span data-ttu-id="ac354-109">Derivadas de [attachment](attachment.md).</span><span class="sxs-lookup"><span data-stu-id="ac354-109">Derived from [attachment](attachment.md).</span></span>

## <a name="methods"></a><span data-ttu-id="ac354-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ac354-110">Methods</span></span>

| <span data-ttu-id="ac354-111">Método</span><span class="sxs-lookup"><span data-stu-id="ac354-111">Method</span></span>       | <span data-ttu-id="ac354-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac354-112">Return Type</span></span>  |<span data-ttu-id="ac354-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac354-113">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ac354-114">Get</span><span class="sxs-lookup"><span data-stu-id="ac354-114">Get</span></span>](../api/attachment-get.md) | [<span data-ttu-id="ac354-115">fileAttachment</span><span class="sxs-lookup"><span data-stu-id="ac354-115">fileAttachment</span></span>](fileattachment.md) |<span data-ttu-id="ac354-116">Lea las propiedades y las relaciones del objeto fileAttachment.</span><span class="sxs-lookup"><span data-stu-id="ac354-116">Read properties and relationships of fileAttachment object.</span></span>|
|[<span data-ttu-id="ac354-117">Eliminar</span><span class="sxs-lookup"><span data-stu-id="ac354-117">Delete</span></span>](../api/attachment-delete.md) | <span data-ttu-id="ac354-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ac354-118">None</span></span> |<span data-ttu-id="ac354-119">Elimine el objeto fileAttachment.</span><span class="sxs-lookup"><span data-stu-id="ac354-119">Delete fileAttachment object.</span></span> |

## <a name="properties"></a><span data-ttu-id="ac354-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ac354-120">Properties</span></span>
| <span data-ttu-id="ac354-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac354-121">Property</span></span>     | <span data-ttu-id="ac354-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac354-122">Type</span></span>   |<span data-ttu-id="ac354-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac354-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ac354-124">contentBytes</span><span class="sxs-lookup"><span data-stu-id="ac354-124">contentBytes</span></span>|<span data-ttu-id="ac354-125">Binario</span><span class="sxs-lookup"><span data-stu-id="ac354-125">Binary</span></span>|<span data-ttu-id="ac354-126">El contenido del archivo codificado en base64.</span><span class="sxs-lookup"><span data-stu-id="ac354-126">The base64-encoded contents of the file.</span></span>|
|<span data-ttu-id="ac354-127">contentId</span><span class="sxs-lookup"><span data-stu-id="ac354-127">contentId</span></span>|<span data-ttu-id="ac354-128">String</span><span class="sxs-lookup"><span data-stu-id="ac354-128">String</span></span>|<span data-ttu-id="ac354-129">El identificador de los datos de adjuntos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ac354-129">The ID of the attachment in the Exchange store.</span></span>|
|<span data-ttu-id="ac354-130">contentLocation</span><span class="sxs-lookup"><span data-stu-id="ac354-130">contentLocation</span></span>|<span data-ttu-id="ac354-131">String</span><span class="sxs-lookup"><span data-stu-id="ac354-131">String</span></span>|<span data-ttu-id="ac354-132">El identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ac354-132">The Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>|
|<span data-ttu-id="ac354-133">contentType</span><span class="sxs-lookup"><span data-stu-id="ac354-133">contentType</span></span>|<span data-ttu-id="ac354-134">String</span><span class="sxs-lookup"><span data-stu-id="ac354-134">String</span></span>|<span data-ttu-id="ac354-135">El tipo de contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ac354-135">The content type of the attachment.</span></span>|
|<span data-ttu-id="ac354-136">id</span><span class="sxs-lookup"><span data-stu-id="ac354-136">id</span></span>|<span data-ttu-id="ac354-137">String</span><span class="sxs-lookup"><span data-stu-id="ac354-137">String</span></span>|<span data-ttu-id="ac354-138">El identificador de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ac354-138">The attachment ID.</span></span>|
|<span data-ttu-id="ac354-139">isInline</span><span class="sxs-lookup"><span data-stu-id="ac354-139">isInline</span></span>|<span data-ttu-id="ac354-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="ac354-140">Boolean</span></span>|<span data-ttu-id="ac354-141">Se establece en true si se trata de datos adjuntos en línea.</span><span class="sxs-lookup"><span data-stu-id="ac354-141">Set to true if this is an inline attachment.</span></span>|
|<span data-ttu-id="ac354-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ac354-142">lastModifiedDateTime</span></span>|<span data-ttu-id="ac354-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ac354-143">DateTimeOffset</span></span>|<span data-ttu-id="ac354-144">La fecha y hora de la última modificación de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ac354-144">The date and time when the attachment was last modified.</span></span>|
|<span data-ttu-id="ac354-145">name</span><span class="sxs-lookup"><span data-stu-id="ac354-145">name</span></span>|<span data-ttu-id="ac354-146">String</span><span class="sxs-lookup"><span data-stu-id="ac354-146">String</span></span>|<span data-ttu-id="ac354-147">El nombre que representa el texto que aparece debajo del icono que representa el archivo adjunto insertado. No tiene que ser el nombre de archivo real.</span><span class="sxs-lookup"><span data-stu-id="ac354-147">The name representing the text that is displayed below the icon representing the embedded attachment.This does not need to be the actual file name.</span></span>|
|<span data-ttu-id="ac354-148">size</span><span class="sxs-lookup"><span data-stu-id="ac354-148">size</span></span>|<span data-ttu-id="ac354-149">Int32</span><span class="sxs-lookup"><span data-stu-id="ac354-149">Int32</span></span>|<span data-ttu-id="ac354-150">El tamaño en bytes de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ac354-150">The size in bytes of the attachment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ac354-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ac354-151">Relationships</span></span>
<span data-ttu-id="ac354-152">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ac354-152">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="ac354-153">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ac354-153">JSON representation</span></span>

<span data-ttu-id="ac354-154">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ac354-154">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.attachment",
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
