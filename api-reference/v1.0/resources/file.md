---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Archivo
ms.openlocfilehash: 2201533457863c3cac6b7a9463f80e37bd5a569a
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23267468"
---
# <a name="file-resource-type"></a><span data-ttu-id="befff-102">Tipo de recurso File</span><span class="sxs-lookup"><span data-stu-id="befff-102">File resource type</span></span>

<span data-ttu-id="befff-103">El recurso **File** agrupa en una sola estructura los elementos de datos relacionados con archivos.</span><span class="sxs-lookup"><span data-stu-id="befff-103">The **File** resource groups file-related data items into a single structure.</span></span>

<span data-ttu-id="befff-p101">Si un [**DriveItem**](driveitem.md) tiene una faceta **file** no null, el elemento representa un archivo. Además de otras propiedades, los archivos tienen una relación **content** que contiene la secuencia de bytes del archivo.</span><span class="sxs-lookup"><span data-stu-id="befff-p101">If a [**DriveItem**](driveitem.md) has a non-null **file** facet, the item represents an file. In addition to other properties, files have a **content** relationship which contains the byte stream of the file.</span></span>

## <a name="json-representation"></a><span data-ttu-id="befff-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="befff-106">JSON representation</span></span>

<span data-ttu-id="befff-107">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="befff-107">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@odata.type": "microsoft.graph.file"
}-->

```json
{
  "hashes": {"@odata.type": "microsoft.graph.hashes"},
  "mimeType": "string"
}
```

## <a name="properties"></a><span data-ttu-id="befff-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="befff-108">Properties</span></span>

| <span data-ttu-id="befff-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="befff-109">Property</span></span> | <span data-ttu-id="befff-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="befff-110">Type</span></span>                    | <span data-ttu-id="befff-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="befff-111">Description</span></span>                                                                                                                                      |
|:---------|:------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="befff-112">hashes</span><span class="sxs-lookup"><span data-stu-id="befff-112">hashes</span></span>   | [<span data-ttu-id="befff-113">Hashes</span><span class="sxs-lookup"><span data-stu-id="befff-113">Hashes</span></span>](hashes.md) | <span data-ttu-id="befff-p102">Algoritmos hash de contenido binario del archivo, si están disponibles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="befff-p102">Hashes of the file's binary content, if available. Read-only.</span></span>                                                                                    |
| <span data-ttu-id="befff-116">mimeType</span><span class="sxs-lookup"><span data-stu-id="befff-116">mimeType</span></span> | <span data-ttu-id="befff-117">cadena</span><span class="sxs-lookup"><span data-stu-id="befff-117">string</span></span>                  | <span data-ttu-id="befff-p103">Tipo MIME para el archivo. Viene determinado por la lógica del servidor y puede que no sea el valor proporcionado cuando el archivo se cargó. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="befff-p103">The MIME type for the file. This is determined by logic on the server and might not be the value provided when the file was uploaded. Read-only.</span></span> |

## <a name="remarks"></a><span data-ttu-id="befff-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="befff-121">Remarks</span></span> 

<span data-ttu-id="befff-122">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="befff-122">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The file facet describes properties of a file",
  "keywords": "file,item,facet",
  "section": "documentation",
  "tocPath": "Facets/File"
} -->
