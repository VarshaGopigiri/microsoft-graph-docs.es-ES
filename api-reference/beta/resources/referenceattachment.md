---
title: Tipo de recurso referenceAttachment
description: 'Un vínculo a una carpeta o archivo (como un archivo de texto o un documento de Word) en un OneDrive para la unidad de negocio en la nube o en otras ubicaciones de almacenamiento compatibles, adjunto '
ms.openlocfilehash: e9885c3a0e5c7f723303d7d6461f4c07dbed6bf6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088920"
---
# <a name="referenceattachment-resource-type"></a><span data-ttu-id="d9d88-103">Tipo de recurso referenceAttachment</span><span class="sxs-lookup"><span data-stu-id="d9d88-103">referenceAttachment resource type</span></span>

> <span data-ttu-id="d9d88-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d9d88-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d9d88-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d9d88-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d9d88-106">Un vínculo a una carpeta o archivo (como un archivo de texto o un documento de Word) en un OneDrive para la unidad de negocio en la nube, u otra compatible con ubicaciones de almacenamiento conectadas a un [evento](../resources/event.md), [mensaje](../resources/message.md), [tarea de Outlook](../resources/outlooktask.md)o [registrar](../resources/post.md) .</span><span class="sxs-lookup"><span data-stu-id="d9d88-106">A link to a folder or file (such as a text file or Word document) on a OneDrive for Business cloud drive, or other supported storage locations, attached to an [event](../resources/event.md), [message](../resources/message.md), [Outlook task](../resources/outlooktask.md), or [post](../resources/post.md) .</span></span>

<span data-ttu-id="d9d88-107">Derivado de [attachment](attachment.md).</span><span class="sxs-lookup"><span data-stu-id="d9d88-107">Derived from [attachment](attachment.md).</span></span>

## <a name="methods"></a><span data-ttu-id="d9d88-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9d88-108">Methods</span></span>

| <span data-ttu-id="d9d88-109">Método</span><span class="sxs-lookup"><span data-stu-id="d9d88-109">Method</span></span>       | <span data-ttu-id="d9d88-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9d88-110">Return Type</span></span>  |<span data-ttu-id="d9d88-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9d88-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d9d88-112">Get</span><span class="sxs-lookup"><span data-stu-id="d9d88-112">Get</span></span>](../api/attachment-get.md) | [<span data-ttu-id="d9d88-113">referenceAttachment</span><span class="sxs-lookup"><span data-stu-id="d9d88-113">referenceAttachment</span></span>](referenceattachment.md) |<span data-ttu-id="d9d88-114">Lee las propiedades y relaciones del objeto referenceAttachment.</span><span class="sxs-lookup"><span data-stu-id="d9d88-114">Read properties and relationships of referenceAttachment object.</span></span>|
|[<span data-ttu-id="d9d88-115">Delete</span><span class="sxs-lookup"><span data-stu-id="d9d88-115">Delete</span></span>](../api/attachment-delete.md) | <span data-ttu-id="d9d88-116">None</span><span class="sxs-lookup"><span data-stu-id="d9d88-116">None</span></span> |<span data-ttu-id="d9d88-117">Elimina el objeto referenceAttachment.</span><span class="sxs-lookup"><span data-stu-id="d9d88-117">Delete referenceAttachment object.</span></span> |

## <a name="properties"></a><span data-ttu-id="d9d88-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9d88-118">Properties</span></span>
| <span data-ttu-id="d9d88-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9d88-119">Property</span></span>     | <span data-ttu-id="d9d88-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9d88-120">Type</span></span>   |<span data-ttu-id="d9d88-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9d88-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d9d88-122">contentType</span><span class="sxs-lookup"><span data-stu-id="d9d88-122">contentType</span></span>|<span data-ttu-id="d9d88-123">String</span><span class="sxs-lookup"><span data-stu-id="d9d88-123">String</span></span>|<span data-ttu-id="d9d88-124">El tipo de contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d9d88-124">The content type of the attachment.</span></span> <span data-ttu-id="d9d88-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d9d88-125">Optional.</span></span>|
|<span data-ttu-id="d9d88-126">id</span><span class="sxs-lookup"><span data-stu-id="d9d88-126">id</span></span>|<span data-ttu-id="d9d88-127">String</span><span class="sxs-lookup"><span data-stu-id="d9d88-127">String</span></span>|<span data-ttu-id="d9d88-p103">Identificador de los datos adjuntos  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9d88-p103">The attachment ID.  Read-only.</span></span>|
|<span data-ttu-id="d9d88-130">isFolder</span><span class="sxs-lookup"><span data-stu-id="d9d88-130">isFolder</span></span>|<span data-ttu-id="d9d88-131">Booleano</span><span class="sxs-lookup"><span data-stu-id="d9d88-131">Boolean</span></span>|<span data-ttu-id="d9d88-132">Especifica si los datos adjuntos son un vínculo a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d9d88-132">Specifies whether the attachment is a link to a folder.</span></span> <span data-ttu-id="d9d88-133">Debe establecer como true si **sourceUrl** es un vínculo a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d9d88-133">Must set this to true if **sourceUrl** is a link to a folder.</span></span> <span data-ttu-id="d9d88-134">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d9d88-134">Optional.</span></span>|
|<span data-ttu-id="d9d88-135">isInline</span><span class="sxs-lookup"><span data-stu-id="d9d88-135">isInline</span></span>|<span data-ttu-id="d9d88-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="d9d88-136">Boolean</span></span>|<span data-ttu-id="d9d88-137">Se establece en true si los datos adjuntos aparecen en insertados en el cuerpo del objeto embedding.</span><span class="sxs-lookup"><span data-stu-id="d9d88-137">Set to true if the attachment appears inline in the body of the embedding object.</span></span> <span data-ttu-id="d9d88-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d9d88-138">Optional.</span></span>|
|<span data-ttu-id="d9d88-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d9d88-139">lastModifiedDateTime</span></span>|<span data-ttu-id="d9d88-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d9d88-140">DateTimeOffset</span></span>|<span data-ttu-id="d9d88-141">La fecha y hora de la última modificación de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d9d88-141">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="d9d88-142">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="d9d88-142">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="d9d88-143">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="d9d88-143">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span> <span data-ttu-id="d9d88-144">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d9d88-144">Optional.</span></span>|
|<span data-ttu-id="d9d88-145">name</span><span class="sxs-lookup"><span data-stu-id="d9d88-145">name</span></span>|<span data-ttu-id="d9d88-146">String</span><span class="sxs-lookup"><span data-stu-id="d9d88-146">String</span></span>|<span data-ttu-id="d9d88-147">El texto que se muestra debajo del icono que representa al archivo adjunto incrustado.</span><span class="sxs-lookup"><span data-stu-id="d9d88-147">The text that is displayed below the icon representing the embedded attachment.</span></span> <span data-ttu-id="d9d88-148">Esto no necesita ser el nombre de archivo real.</span><span class="sxs-lookup"><span data-stu-id="d9d88-148">This does not need to be the actual file name.</span></span> <span data-ttu-id="d9d88-149">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d9d88-149">Required.</span></span>|
|<span data-ttu-id="d9d88-150">permiso</span><span class="sxs-lookup"><span data-stu-id="d9d88-150">permission</span></span>|<span data-ttu-id="d9d88-151">ReferenceAttachmentPermissions</span><span class="sxs-lookup"><span data-stu-id="d9d88-151">ReferenceAttachmentPermissions</span></span>|<span data-ttu-id="d9d88-152">Especifica los permisos concedidos para los datos adjuntos con el tipo de proveedor en **tipo de proveedor**.</span><span class="sxs-lookup"><span data-stu-id="d9d88-152">Specifies the permissions granted for the attachment by the type of provider in **providerType**.</span></span> <span data-ttu-id="d9d88-153">Los valores posibles son: `other`, `view`, `edit`, `anonymousView`, `anonymousEdit`, `organizationView` y `organizationEdit`.</span><span class="sxs-lookup"><span data-stu-id="d9d88-153">Possible values are: `other`, `view`, `edit`, `anonymousView`, `anonymousEdit`, `organizationView`, `organizationEdit`.</span></span> <span data-ttu-id="d9d88-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d9d88-154">Optional.</span></span>|
|<span data-ttu-id="d9d88-155">previewUrl</span><span class="sxs-lookup"><span data-stu-id="d9d88-155">previewUrl</span></span>|<span data-ttu-id="d9d88-156">String</span><span class="sxs-lookup"><span data-stu-id="d9d88-156">String</span></span>|<span data-ttu-id="d9d88-157">Se aplica a un adjunto de referencia de una imagen - dirección URL para obtener una imagen de vista previa.</span><span class="sxs-lookup"><span data-stu-id="d9d88-157">Applies to only a reference attachment of an image - URL to get a preview image.</span></span> <span data-ttu-id="d9d88-158">Use **thumbnailUrl** y **previewUrl** sólo cuando **sourceUrl** identifica un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="d9d88-158">Use **thumbnailUrl** and **previewUrl** only when **sourceUrl** identifies an image file.</span></span> <span data-ttu-id="d9d88-159">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d9d88-159">Optional.</span></span>|
|<span data-ttu-id="d9d88-160">tipo de proveedor</span><span class="sxs-lookup"><span data-stu-id="d9d88-160">providerType</span></span>|<span data-ttu-id="d9d88-161">ReferenceAttachmentProviders</span><span class="sxs-lookup"><span data-stu-id="d9d88-161">ReferenceAttachmentProviders</span></span>|<span data-ttu-id="d9d88-162">El tipo de proveedor que admite un dato adjunto de este contentType.</span><span class="sxs-lookup"><span data-stu-id="d9d88-162">The type of provider that supports an attachment of this contentType.</span></span> <span data-ttu-id="d9d88-163">Los valores posibles son: `other`, `oneDriveBusiness`, `oneDriveConsumer` y `dropbox`.</span><span class="sxs-lookup"><span data-stu-id="d9d88-163">Possible values are: `other`, `oneDriveBusiness`, `oneDriveConsumer`, `dropbox`.</span></span> <span data-ttu-id="d9d88-164">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d9d88-164">Optional.</span></span>|
|<span data-ttu-id="d9d88-165">size</span><span class="sxs-lookup"><span data-stu-id="d9d88-165">size</span></span>|<span data-ttu-id="d9d88-166">Int32</span><span class="sxs-lookup"><span data-stu-id="d9d88-166">Int32</span></span>|<span data-ttu-id="d9d88-167">El tamaño de los metadatos en bytes que se almacenan en el mensaje para los datos adjuntos de referencia.</span><span class="sxs-lookup"><span data-stu-id="d9d88-167">The size of the metadata in bytes that is stored on the message for the reference attachment.</span></span> <span data-ttu-id="d9d88-168">Este valor no indica el tamaño del archivo real.</span><span class="sxs-lookup"><span data-stu-id="d9d88-168">This value does not indicate the size of the actual file.</span></span> <span data-ttu-id="d9d88-169">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d9d88-169">Optional.</span></span>|
|<span data-ttu-id="d9d88-170">sourceUrl</span><span class="sxs-lookup"><span data-stu-id="d9d88-170">sourceUrl</span></span>|<span data-ttu-id="d9d88-171">String</span><span class="sxs-lookup"><span data-stu-id="d9d88-171">String</span></span>|<span data-ttu-id="d9d88-172">URL para obtener el contenido del archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="d9d88-172">URL to get the attachment content.</span></span> <span data-ttu-id="d9d88-173">Si se trata de una dirección URL a una carpeta, a continuación, para que la carpeta que se muestre correctamente en Outlook o Outlook en la web, establecer **isFolder** en true.</span><span class="sxs-lookup"><span data-stu-id="d9d88-173">If this is a URL to a folder, then for the folder to be displayed correctly in Outlook or Outlook on the web, set **isFolder** to true.</span></span> <span data-ttu-id="d9d88-174">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d9d88-174">Required.</span></span>|
|<span data-ttu-id="d9d88-175">thumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="d9d88-175">thumbnailUrl</span></span>|<span data-ttu-id="d9d88-176">String</span><span class="sxs-lookup"><span data-stu-id="d9d88-176">String</span></span>|<span data-ttu-id="d9d88-177">Se aplica a un adjunto de referencia de una imagen - dirección URL para obtener una imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="d9d88-177">Applies to only a reference attachment of an image - URL to get a thumbnail image.</span></span> <span data-ttu-id="d9d88-178">Use **thumbnailUrl** y **previewUrl** sólo cuando **sourceUrl** identifica un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="d9d88-178">Use **thumbnailUrl** and **previewUrl** only when **sourceUrl** identifies an image file.</span></span> <span data-ttu-id="d9d88-179">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d9d88-179">Optional.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d9d88-180">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d9d88-180">Relationships</span></span>
<span data-ttu-id="d9d88-181">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d9d88-181">None</span></span>



## <a name="json-representation"></a><span data-ttu-id="d9d88-182">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d9d88-182">JSON representation</span></span>

<span data-ttu-id="d9d88-183">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d9d88-183">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.referenceAttachment"
}-->

```json
{
  "contentType": "string",
  "id": "string (identifier)",
  "isFolder": true,
  "isInline": true,
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "permission": "string",
  "previewUrl": "string",
  "providerType": "string",
  "size": 1024,
  "sourceUrl": "string",
  "thumbnailUrl": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "referenceAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
