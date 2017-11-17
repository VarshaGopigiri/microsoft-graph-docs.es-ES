---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Carpeta
ms.openlocfilehash: 664597297700f7af096ef30cfbd5342a45a6c157
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="folder-resource-type"></a><span data-ttu-id="bc648-102">Tipo de recurso Folder</span><span class="sxs-lookup"><span data-stu-id="bc648-102">Folder resource type</span></span>

<span data-ttu-id="bc648-103">El recurso **Folder** agrupa en una sola estructura los datos relacionados con carpetas de un elemento.</span><span class="sxs-lookup"><span data-stu-id="bc648-103">The **Folder** resource groups folder-related data on an item into a single structure. DriveItems with a non-null folder facet are containers for other DriveItems.</span></span> 
<span data-ttu-id="bc648-104">Los objetos [**DriveItems**](driveitem.md) con una faceta **folder** que no sea NULL son contenedores de otros objetos DriveItems.</span><span class="sxs-lookup"><span data-stu-id="bc648-104">The Folder resource groups folder-related data on an item into a single structure. [**DriveItems**](driveitem.md) with a non-null **folder** facet are containers for other DriveItems.</span></span>

## <a name="json-representation"></a><span data-ttu-id="bc648-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bc648-105">JSON representation</span></span>

<span data-ttu-id="bc648-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bc648-106">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.folder"
}-->

```json
{
  "childCount": 1024,
  "view": { "@odata.type": "microsoft.graph.folderView" }
}
```

## <a name="properties"></a><span data-ttu-id="bc648-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bc648-107">Properties</span></span>

| <span data-ttu-id="bc648-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bc648-108">Property</span></span>       | <span data-ttu-id="bc648-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc648-109">Type</span></span>           | <span data-ttu-id="bc648-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc648-110">Description</span></span>
|:---------------|:---------------|:-------------------------------------------
| <span data-ttu-id="bc648-111">**childCount**</span><span class="sxs-lookup"><span data-stu-id="bc648-111">**childCount**</span></span> | <span data-ttu-id="bc648-112">Int64</span><span class="sxs-lookup"><span data-stu-id="bc648-112">Int64</span></span>          | <span data-ttu-id="bc648-113">Número de elementos secundarios que se incluyen inmediatamente dentro de este contenedor.</span><span class="sxs-lookup"><span data-stu-id="bc648-113">Number of children contained immediately within this container.</span></span>
| <span data-ttu-id="bc648-114">**view**</span><span class="sxs-lookup"><span data-stu-id="bc648-114">**view**</span></span>       | <span data-ttu-id="bc648-115">[folderView][]</span><span class="sxs-lookup"><span data-stu-id="bc648-115">[folderView facet][]</span></span> | <span data-ttu-id="bc648-116">Una colección de propiedades que definen la vista recomendada de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="bc648-116">A collection of properties defining the recommended view for the folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc648-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc648-117">Remarks</span></span> 

<span data-ttu-id="bc648-118">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem][].</span><span class="sxs-lookup"><span data-stu-id="bc648-118">For more information about the facets on a DriveItem, see [DriveItem][].</span></span>

[folderView]: folderView.md
[DriveItem]: driveItem.md

<!-- {
  "type": "#page.annotation",
  "description": "The Folder facet describes properties of a folder",
  "keywords": "folder,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Folder"
} -->
