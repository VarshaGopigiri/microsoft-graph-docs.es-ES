---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Archivo
ms.openlocfilehash: bd0cd6ea5f5ee2225392aa61c2dda9b30e2ffbca
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089198"
---
# <a name="file-resource-type"></a><span data-ttu-id="fa3a2-102">Tipo de recurso File</span><span class="sxs-lookup"><span data-stu-id="fa3a2-102">File resource type</span></span>

> <span data-ttu-id="fa3a2-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fa3a2-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fa3a2-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fa3a2-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fa3a2-105">El recurso **File** agrupa en una sola estructura los elementos de datos relacionados con archivos.</span><span class="sxs-lookup"><span data-stu-id="fa3a2-105">The **File** resource groups file-related data items into a single structure.</span></span>

<span data-ttu-id="fa3a2-p102">Si un [**DriveItem**](driveitem.md) tiene una faceta **file** no null, el elemento representa un archivo. Además de otras propiedades, los archivos tienen una relación **content** que contiene la secuencia de bytes del archivo.</span><span class="sxs-lookup"><span data-stu-id="fa3a2-p102">If a [**DriveItem**](driveitem.md) has a non-null **file** facet, the item represents an file. In addition to other properties, files have a **content** relationship which contains the byte stream of the file.</span></span>

## <a name="json-representation"></a><span data-ttu-id="fa3a2-108">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fa3a2-108">JSON representation</span></span>

<span data-ttu-id="fa3a2-109">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fa3a2-109">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="fa3a2-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fa3a2-110">Properties</span></span>

| <span data-ttu-id="fa3a2-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fa3a2-111">Property</span></span> | <span data-ttu-id="fa3a2-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa3a2-112">Type</span></span>                    | <span data-ttu-id="fa3a2-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa3a2-113">Description</span></span>                                                                                                                                      |
|:---------|:------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa3a2-114">algoritmos hash</span><span class="sxs-lookup"><span data-stu-id="fa3a2-114">hashes</span></span>   | [<span data-ttu-id="fa3a2-115">HashesType</span><span class="sxs-lookup"><span data-stu-id="fa3a2-115">HashesType</span></span>](hashes.md) | <span data-ttu-id="fa3a2-p103">Algoritmos hash de contenido binario del archivo, si están disponibles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fa3a2-p103">Hashes of the file's binary content, if available. Read-only.</span></span>                                                                                    |
| <span data-ttu-id="fa3a2-118">mimeType</span><span class="sxs-lookup"><span data-stu-id="fa3a2-118">mimeType</span></span> | <span data-ttu-id="fa3a2-119">string</span><span class="sxs-lookup"><span data-stu-id="fa3a2-119">string</span></span>                  | <span data-ttu-id="fa3a2-p104">Tipo MIME para el archivo. Viene determinado por la lógica del servidor y puede que no sea el valor proporcionado cuando el archivo se cargó. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fa3a2-p104">The MIME type for the file. This is determined by logic on the server and might not be the value provided when the file was uploaded. Read-only.</span></span> |

## <a name="remarks"></a><span data-ttu-id="fa3a2-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa3a2-123">Remarks</span></span> 

<span data-ttu-id="fa3a2-124">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="fa3a2-124">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The file facet describes properties of a file",
  "keywords": "file,item,facet",
  "section": "documentation",
  "tocPath": "Facets/File"
} -->
