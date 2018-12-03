---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: ItemReference
ms.openlocfilehash: 3af3af4b366c61119ba48aaebdc461e356f23464
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028854"
---
# <a name="itemreference-resource-type"></a><span data-ttu-id="43af3-102">Tipo de recurso ItemReference</span><span class="sxs-lookup"><span data-stu-id="43af3-102">ItemReference resource type</span></span>

<span data-ttu-id="43af3-103">El recurso **ItemReference** proporciona información necesaria para dirigir un [DriveItem](driveitem.md) a través de la API.</span><span class="sxs-lookup"><span data-stu-id="43af3-103">The **ItemReference** resource provides information necessary to address a [DriveItem](driveitem.md) via the API.</span></span>

## <a name="json-representation"></a><span data-ttu-id="43af3-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="43af3-104">JSON representation</span></span>

<span data-ttu-id="43af3-105">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="43af3-105">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "path", "shareId", "sharepointIds" ],
  "@odata.type": "microsoft.graph.itemReference"
}-->

```json
{
  "driveId": "string",
  "driveType": "personal | business | documentLibrary",
  "id": "string",
  "name": "string",
  "path": "string",
  "shareId": "string",
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" }
}
```

## <a name="properties"></a><span data-ttu-id="43af3-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="43af3-106">Properties</span></span>

| <span data-ttu-id="43af3-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="43af3-107">Property</span></span>      | <span data-ttu-id="43af3-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="43af3-108">Type</span></span>              | <span data-ttu-id="43af3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="43af3-109">Description</span></span>
|:--------------|:------------------|:-----------------------------------------
| <span data-ttu-id="43af3-110">driveId</span><span class="sxs-lookup"><span data-stu-id="43af3-110">driveId</span></span>       | <span data-ttu-id="43af3-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="43af3-111">String</span></span>            | <span data-ttu-id="43af3-p101">Identificador único de la instancia de la unidad que contiene el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="43af3-p101">Unique identifier of the drive instance that contains the item. Read-only.</span></span>
| <span data-ttu-id="43af3-114">driveType</span><span class="sxs-lookup"><span data-stu-id="43af3-114">driveType</span></span>     | <span data-ttu-id="43af3-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="43af3-115">String</span></span>            | <span data-ttu-id="43af3-116">Identifica el tipo de unidad.</span><span class="sxs-lookup"><span data-stu-id="43af3-116">Identifies the type of drive.</span></span> <span data-ttu-id="43af3-117">Consulte el recurso [drive][] para ver los valores.</span><span class="sxs-lookup"><span data-stu-id="43af3-117">See [drive][] resource for values.</span></span>
| <span data-ttu-id="43af3-118">id</span><span class="sxs-lookup"><span data-stu-id="43af3-118">id</span></span>            | <span data-ttu-id="43af3-119">String</span><span class="sxs-lookup"><span data-stu-id="43af3-119">String</span></span>            | <span data-ttu-id="43af3-p103">Identificador único del elemento en la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="43af3-p103">Unique identifier of the item in the drive. Read-only.</span></span>
| <span data-ttu-id="43af3-122">name</span><span class="sxs-lookup"><span data-stu-id="43af3-122">name</span></span>          | <span data-ttu-id="43af3-123">String</span><span class="sxs-lookup"><span data-stu-id="43af3-123">String</span></span>            | <span data-ttu-id="43af3-p104">El nombre del elemento al que se hace referencia. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="43af3-p104">The name of the item being referenced. Read-only.</span></span>
| <span data-ttu-id="43af3-126">path</span><span class="sxs-lookup"><span data-stu-id="43af3-126">path</span></span>          | <span data-ttu-id="43af3-127">String</span><span class="sxs-lookup"><span data-stu-id="43af3-127">String</span></span>            | <span data-ttu-id="43af3-p105">Ruta de acceso que se puede usar para navegar hasta el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="43af3-p105">Path that can be used to navigate to the item. Read-only.</span></span>
| <span data-ttu-id="43af3-130">shareId</span><span class="sxs-lookup"><span data-stu-id="43af3-130">shareId</span></span>       | <span data-ttu-id="43af3-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="43af3-131">String</span></span>            | <span data-ttu-id="43af3-132">Un identificador único para un recurso compartido al que se puede tener acceso a través de la API [Shares][].</span><span class="sxs-lookup"><span data-stu-id="43af3-132">A unique identifier for a shared resource that can be accessed via the [Shares][] API.</span></span>
| <span data-ttu-id="43af3-133">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="43af3-133">sharepointIds</span></span> | <span data-ttu-id="43af3-134">[sharepointIds][]</span><span class="sxs-lookup"><span data-stu-id="43af3-134">[sharepointIds][]</span></span> | <span data-ttu-id="43af3-p106">Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="43af3-p106">Returns identifiers useful for SharePoint REST compatibility. Read-only.</span></span>

[drive]: ../resources/drive.md
[sharepointIds]: ../resources/sharepointids.md
[Shares]: ../api/shares-get.md

## <a name="remarks"></a><span data-ttu-id="43af3-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43af3-140">Remarks</span></span>

<span data-ttu-id="43af3-141">Para resolver un **driveItem** de un recurso **itemReference**, cree una dirección URL con el formato:</span><span class="sxs-lookup"><span data-stu-id="43af3-141">To address a **driveItem** from an **itemReference** resource, construct a URL of the format:</span></span>

```http
GET https://graph.microsoft.com/v1.0/drives/{driveId}/items/{id}
```

<span data-ttu-id="43af3-142">El valor **path** es una ruta de acceso de API relativa a la unidad de destino, por ejemplo: `/drive/root:/Documents/myfile.docx`.</span><span class="sxs-lookup"><span data-stu-id="43af3-142">The **path** value is an API path relative to the target drive, for example: `/drive/root:/Documents/myfile.docx`.</span></span>

<span data-ttu-id="43af3-143">Para recuperar la ruta de acceso legible de una ruta de navegación, puede ignorar todo hasta la primera `:` en la cadena de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="43af3-143">To retrieve the human-readable path for a breadcrumb, you can safely ignore everything up to the first `:` in the path string.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ItemReference returns a pointer to another item.",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/itemreference.md:
      Found potential enums in resource example that weren't defined in a table:(personal,business,documentLibrary) are in resource, but () are in table"
  ],
  "tocPath": "Resources/ItemReference"
} -->
