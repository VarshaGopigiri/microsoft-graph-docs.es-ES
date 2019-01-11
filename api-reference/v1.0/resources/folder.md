---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Carpeta
localization_priority: Normal
ms.openlocfilehash: fab5db026b47aa84f7d097a19782b70eac6b6064
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821423"
---
# <a name="folder-resource-type"></a><span data-ttu-id="7b5dc-102">Tipo de recurso Folder</span><span class="sxs-lookup"><span data-stu-id="7b5dc-102">Folder resource type</span></span>

<span data-ttu-id="7b5dc-p101">El recurso **Folder** agrupa en una sola estructura los datos relacionados con carpetas de un elemento. [**DriveItems**](driveitem.md) con una faceta **folder** no null son contenedores para otros DriveItems.</span><span class="sxs-lookup"><span data-stu-id="7b5dc-p101">The **Folder** resource groups folder-related data on an item into a single structure. [**DriveItems**](driveitem.md) with a non-null **folder** facet are containers for other DriveItems.</span></span>

## <a name="json-representation"></a><span data-ttu-id="7b5dc-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7b5dc-105">JSON representation</span></span>

<span data-ttu-id="7b5dc-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7b5dc-106">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="7b5dc-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b5dc-107">Properties</span></span>

| <span data-ttu-id="7b5dc-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7b5dc-108">Property</span></span>       | <span data-ttu-id="7b5dc-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b5dc-109">Type</span></span>           | <span data-ttu-id="7b5dc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b5dc-110">Description</span></span>
|:---------------|:---------------|:-------------------------------------------
| <span data-ttu-id="7b5dc-111">**childCount**</span><span class="sxs-lookup"><span data-stu-id="7b5dc-111">**childCount**</span></span> | <span data-ttu-id="7b5dc-112">Int32</span><span class="sxs-lookup"><span data-stu-id="7b5dc-112">Int32</span></span>          | <span data-ttu-id="7b5dc-113">Número de elementos secundarios que se incluyen inmediatamente dentro de este contenedor.</span><span class="sxs-lookup"><span data-stu-id="7b5dc-113">Number of children contained immediately within this container.</span></span>
| <span data-ttu-id="7b5dc-114">**view**</span><span class="sxs-lookup"><span data-stu-id="7b5dc-114">**view**</span></span>       | <span data-ttu-id="7b5dc-115">[folderView][]</span><span class="sxs-lookup"><span data-stu-id="7b5dc-115">[folderView][]</span></span> | <span data-ttu-id="7b5dc-116">Una colección de propiedades que definen la vista recomendada de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="7b5dc-116">A collection of properties defining the recommended view for the folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b5dc-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b5dc-117">Remarks</span></span> 

<span data-ttu-id="7b5dc-118">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem][].</span><span class="sxs-lookup"><span data-stu-id="7b5dc-118">For more information about the facets on a DriveItem, see [DriveItem][].</span></span>

[folderView]: folderview.md
[DriveItem]: driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "The Folder facet describes properties of a folder",
  "keywords": "folder,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Folder"
} -->
