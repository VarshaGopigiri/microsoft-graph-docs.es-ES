---
title: Tipo de recurso referenceAttachment
description: Vínculo a un archivo (como un archivo de texto o un documento de Word) en una unidad en la nube de OneDrive para la Empresa o en otras ubicaciones de almacenamiento compatibles asociadas a un evento, mensaje o publicación.
ms.openlocfilehash: b3604791c7e06d4f765a81263e1f6afe51743390
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032401"
---
# <a name="referenceattachment-resource-type"></a><span data-ttu-id="26c71-103">Tipo de recurso referenceAttachment</span><span class="sxs-lookup"><span data-stu-id="26c71-103">referenceAttachment resource type</span></span>

<span data-ttu-id="26c71-104">Vínculo a un archivo (como un archivo de texto o un documento de Word) en una unidad en la nube de OneDrive para la Empresa o en otras ubicaciones de almacenamiento compatibles asociadas a un evento, mensaje o publicación.</span><span class="sxs-lookup"><span data-stu-id="26c71-104">A link to a file (such as a text file or Word document) on a OneDrive for Business cloud drive or other supported storage locations, attached to an event, message, or post.</span></span>

<span data-ttu-id="26c71-105">Derivado de [attachment](attachment.md).</span><span class="sxs-lookup"><span data-stu-id="26c71-105">Derived from [attachment](attachment.md).</span></span>

## <a name="methods"></a><span data-ttu-id="26c71-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="26c71-106">Methods</span></span>

| <span data-ttu-id="26c71-107">Método</span><span class="sxs-lookup"><span data-stu-id="26c71-107">Method</span></span>       | <span data-ttu-id="26c71-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26c71-108">Return Type</span></span>  |<span data-ttu-id="26c71-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="26c71-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="26c71-110">Get</span><span class="sxs-lookup"><span data-stu-id="26c71-110">Get</span></span>](../api/attachment-get.md) | [<span data-ttu-id="26c71-111">referenceAttachment</span><span class="sxs-lookup"><span data-stu-id="26c71-111">referenceAttachment</span></span>](referenceattachment.md) |<span data-ttu-id="26c71-112">Lee las propiedades y relaciones del objeto referenceAttachment.</span><span class="sxs-lookup"><span data-stu-id="26c71-112">Read properties and relationships of referenceAttachment object.</span></span>|
|[<span data-ttu-id="26c71-113">Delete</span><span class="sxs-lookup"><span data-stu-id="26c71-113">Delete</span></span>](../api/attachment-delete.md) | <span data-ttu-id="26c71-114">None</span><span class="sxs-lookup"><span data-stu-id="26c71-114">None</span></span> |<span data-ttu-id="26c71-115">Elimina el objeto referenceAttachment.</span><span class="sxs-lookup"><span data-stu-id="26c71-115">Delete referenceAttachment object.</span></span> |

## <a name="properties"></a><span data-ttu-id="26c71-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26c71-116">Properties</span></span>
| <span data-ttu-id="26c71-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26c71-117">Property</span></span>     | <span data-ttu-id="26c71-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="26c71-118">Type</span></span>   |<span data-ttu-id="26c71-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="26c71-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="26c71-120">contentType</span><span class="sxs-lookup"><span data-stu-id="26c71-120">contentType</span></span>|<span data-ttu-id="26c71-121">String</span><span class="sxs-lookup"><span data-stu-id="26c71-121">String</span></span>|<span data-ttu-id="26c71-122">El tipo de contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="26c71-122">The content type of the attachment.</span></span>|
|<span data-ttu-id="26c71-123">id</span><span class="sxs-lookup"><span data-stu-id="26c71-123">id</span></span>|<span data-ttu-id="26c71-124">String</span><span class="sxs-lookup"><span data-stu-id="26c71-124">String</span></span>|<span data-ttu-id="26c71-p101">Identificador de los datos adjuntos  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="26c71-p101">The attachment ID.  Read-only.</span></span>|
|<span data-ttu-id="26c71-127">isInline</span><span class="sxs-lookup"><span data-stu-id="26c71-127">isInline</span></span>|<span data-ttu-id="26c71-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="26c71-128">Boolean</span></span>|<span data-ttu-id="26c71-129">Se establece en true si los datos adjuntos aparecen en insertados en el cuerpo del objeto embedding.</span><span class="sxs-lookup"><span data-stu-id="26c71-129">Set to true if the attachment appears inline in the body of the embedding object.</span></span>|
|<span data-ttu-id="26c71-130">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="26c71-130">lastModifiedDateTime</span></span>|<span data-ttu-id="26c71-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="26c71-131">DateTimeOffset</span></span>|<span data-ttu-id="26c71-p102">Fecha y hora de la última modificación de los datos adjuntos. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="26c71-p102">The date and time when the attachment was last modified. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="26c71-135">name</span><span class="sxs-lookup"><span data-stu-id="26c71-135">name</span></span>|<span data-ttu-id="26c71-136">String</span><span class="sxs-lookup"><span data-stu-id="26c71-136">String</span></span>|<span data-ttu-id="26c71-p103">Texto que aparece debajo del icono que representa al archivo adjunto incrustado. No tiene que ser el nombre de archivo real.</span><span class="sxs-lookup"><span data-stu-id="26c71-p103">The text that is displayed below the icon representing the embedded attachment. This does not need to be the actual file name.</span></span>|
|<span data-ttu-id="26c71-139">size</span><span class="sxs-lookup"><span data-stu-id="26c71-139">size</span></span>|<span data-ttu-id="26c71-140">Int32</span><span class="sxs-lookup"><span data-stu-id="26c71-140">Int32</span></span>|<span data-ttu-id="26c71-141">Tamaño en bytes de los metadatos almacenados en el mensaje del archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="26c71-141">The size of the metadata that is stored on the message for the attachment in bytes.</span></span> <span data-ttu-id="26c71-142">Este valor no indica el tamaño del archivo real.</span><span class="sxs-lookup"><span data-stu-id="26c71-142">This value does not indicate the size of the actual file.</span></span>|

## <a name="relationships"></a><span data-ttu-id="26c71-143">Relaciones</span><span class="sxs-lookup"><span data-stu-id="26c71-143">Relationships</span></span>
<span data-ttu-id="26c71-144">Ninguno</span><span class="sxs-lookup"><span data-stu-id="26c71-144">None</span></span>



## <a name="json-representation"></a><span data-ttu-id="26c71-145">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="26c71-145">JSON representation</span></span>

<span data-ttu-id="26c71-146">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="26c71-146">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.attachment",
  "@odata.type": "microsoft.graph.referenceAttachment"
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
  "description": "referenceAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
