---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Carpeta
ms.openlocfilehash: 834b2cd7c81a947ca1e6d4619f39a8533677e6c3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089207"
---
# <a name="folder-resource-type"></a><span data-ttu-id="37649-102">Tipo de recurso Folder</span><span class="sxs-lookup"><span data-stu-id="37649-102">Folder resource type</span></span>

> <span data-ttu-id="37649-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="37649-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="37649-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="37649-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="37649-p102">El recurso **Folder** agrupa en una sola estructura los datos relacionados con carpetas de un elemento. [**DriveItems**](driveitem.md) con una faceta **folder** no null son contenedores para otros DriveItems.</span><span class="sxs-lookup"><span data-stu-id="37649-p102">The **Folder** resource groups folder-related data on an item into a single structure. [**DriveItems**](driveitem.md) with a non-null **folder** facet are containers for other DriveItems.</span></span>

## <a name="json-representation"></a><span data-ttu-id="37649-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="37649-107">JSON representation</span></span>

<span data-ttu-id="37649-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="37649-108">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="37649-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="37649-109">Properties</span></span>

| <span data-ttu-id="37649-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="37649-110">Property</span></span>       | <span data-ttu-id="37649-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="37649-111">Type</span></span>           | <span data-ttu-id="37649-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="37649-112">Description</span></span>
|:---------------|:---------------|:-------------------------------------------
| <span data-ttu-id="37649-113">**childCount**</span><span class="sxs-lookup"><span data-stu-id="37649-113">**childCount**</span></span> | <span data-ttu-id="37649-114">Int64</span><span class="sxs-lookup"><span data-stu-id="37649-114">Int64</span></span>          | <span data-ttu-id="37649-115">Número de elementos secundarios que se incluyen inmediatamente dentro de este contenedor.</span><span class="sxs-lookup"><span data-stu-id="37649-115">Number of children contained immediately within this container.</span></span>
| <span data-ttu-id="37649-116">**view**</span><span class="sxs-lookup"><span data-stu-id="37649-116">**view**</span></span>       | <span data-ttu-id="37649-117">[folderView][]</span><span class="sxs-lookup"><span data-stu-id="37649-117">[folderView][]</span></span> | <span data-ttu-id="37649-118">Una colección de propiedades que definen la vista recomendada de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="37649-118">A collection of properties defining the recommended view for the folder.</span></span>


## <a name="remarks"></a><span data-ttu-id="37649-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37649-119">Remarks</span></span> 

<span data-ttu-id="37649-120">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem][].</span><span class="sxs-lookup"><span data-stu-id="37649-120">For more information about the facets on a DriveItem, see [DriveItem][].</span></span>

[folderView]: folderview.md
[DriveItem]: driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "folder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
