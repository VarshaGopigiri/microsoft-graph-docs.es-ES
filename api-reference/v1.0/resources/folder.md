---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Carpeta
ms.openlocfilehash: dc90624b14a88d06b45302f421a7e3fcfa802a67
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028650"
---
# <a name="folder-resource-type"></a><span data-ttu-id="f8315-102">Tipo de recurso Folder</span><span class="sxs-lookup"><span data-stu-id="f8315-102">Folder resource type</span></span>

<span data-ttu-id="f8315-p101">El recurso **Folder** agrupa en una sola estructura los datos relacionados con carpetas de un elemento. [**DriveItems**](driveitem.md) con una faceta **folder** no null son contenedores para otros DriveItems.</span><span class="sxs-lookup"><span data-stu-id="f8315-p101">The **Folder** resource groups folder-related data on an item into a single structure. [**DriveItems**](driveitem.md) with a non-null **folder** facet are containers for other DriveItems.</span></span>

## <a name="json-representation"></a><span data-ttu-id="f8315-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f8315-105">JSON representation</span></span>

<span data-ttu-id="f8315-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f8315-106">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="f8315-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f8315-107">Properties</span></span>

| <span data-ttu-id="f8315-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f8315-108">Property</span></span>       | <span data-ttu-id="f8315-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8315-109">Type</span></span>           | <span data-ttu-id="f8315-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8315-110">Description</span></span>
|:---------------|:---------------|:-------------------------------------------
| <span data-ttu-id="f8315-111">**childCount**</span><span class="sxs-lookup"><span data-stu-id="f8315-111">**childCount**</span></span> | <span data-ttu-id="f8315-112">Int32</span><span class="sxs-lookup"><span data-stu-id="f8315-112">Int32</span></span>          | <span data-ttu-id="f8315-113">Número de elementos secundarios que se incluyen inmediatamente dentro de este contenedor.</span><span class="sxs-lookup"><span data-stu-id="f8315-113">Number of children contained immediately within this container.</span></span>
| <span data-ttu-id="f8315-114">**view**</span><span class="sxs-lookup"><span data-stu-id="f8315-114">**view**</span></span>       | <span data-ttu-id="f8315-115">[folderView][]</span><span class="sxs-lookup"><span data-stu-id="f8315-115">[folderView][]</span></span> | <span data-ttu-id="f8315-116">Una colección de propiedades que definen la vista recomendada de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f8315-116">A collection of properties defining the recommended view for the folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8315-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8315-117">Remarks</span></span> 

<span data-ttu-id="f8315-118">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem][].</span><span class="sxs-lookup"><span data-stu-id="f8315-118">For more information about the facets on a DriveItem, see [DriveItem][].</span></span>

[folderView]: folderview.md
[DriveItem]: driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "The Folder facet describes properties of a folder",
  "keywords": "folder,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Folder"
} -->
