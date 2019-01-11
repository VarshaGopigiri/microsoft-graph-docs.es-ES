---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Carpeta
localization_priority: Normal
ms.openlocfilehash: 98c477ebeda436c57db3eaac5cb062639a2447d2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856500"
---
# <a name="folder-resource-type"></a><span data-ttu-id="ea913-102">Tipo de recurso Folder</span><span class="sxs-lookup"><span data-stu-id="ea913-102">Folder resource type</span></span>

> <span data-ttu-id="ea913-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ea913-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ea913-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ea913-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ea913-p102">El recurso **Folder** agrupa en una sola estructura los datos relacionados con carpetas de un elemento. [**DriveItems**](driveitem.md) con una faceta **folder** no null son contenedores para otros DriveItems.</span><span class="sxs-lookup"><span data-stu-id="ea913-p102">The **Folder** resource groups folder-related data on an item into a single structure. [**DriveItems**](driveitem.md) with a non-null **folder** facet are containers for other DriveItems.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ea913-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ea913-107">JSON representation</span></span>

<span data-ttu-id="ea913-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ea913-108">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="ea913-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea913-109">Properties</span></span>

| <span data-ttu-id="ea913-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea913-110">Property</span></span>       | <span data-ttu-id="ea913-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea913-111">Type</span></span>           | <span data-ttu-id="ea913-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea913-112">Description</span></span>
|:---------------|:---------------|:-------------------------------------------
| <span data-ttu-id="ea913-113">**childCount**</span><span class="sxs-lookup"><span data-stu-id="ea913-113">**childCount**</span></span> | <span data-ttu-id="ea913-114">Int64</span><span class="sxs-lookup"><span data-stu-id="ea913-114">Int64</span></span>          | <span data-ttu-id="ea913-115">Número de elementos secundarios que se incluyen inmediatamente dentro de este contenedor.</span><span class="sxs-lookup"><span data-stu-id="ea913-115">Number of children contained immediately within this container.</span></span>
| <span data-ttu-id="ea913-116">**view**</span><span class="sxs-lookup"><span data-stu-id="ea913-116">**view**</span></span>       | <span data-ttu-id="ea913-117">[folderView][]</span><span class="sxs-lookup"><span data-stu-id="ea913-117">[folderView][]</span></span> | <span data-ttu-id="ea913-118">Una colección de propiedades que definen la vista recomendada de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="ea913-118">A collection of properties defining the recommended view for the folder.</span></span>


## <a name="remarks"></a><span data-ttu-id="ea913-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ea913-119">Remarks</span></span> 

<span data-ttu-id="ea913-120">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem][].</span><span class="sxs-lookup"><span data-stu-id="ea913-120">For more information about the facets on a DriveItem, see [DriveItem][].</span></span>

[folderView]: folderview.md
[DriveItem]: driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "folder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
