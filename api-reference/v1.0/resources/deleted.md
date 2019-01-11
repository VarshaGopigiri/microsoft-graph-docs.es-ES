---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Eliminados
localization_priority: Normal
ms.openlocfilehash: a35bc781555486603c0319c819aa019704e362d9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27886145"
---
# <a name="deleted-facet"></a><span data-ttu-id="2abe3-102">Faceta Deleted</span><span class="sxs-lookup"><span data-stu-id="2abe3-102">Deleted facet</span></span>

<span data-ttu-id="2abe3-p101">El recurso **Deleted** indica que el elemento se ha eliminado. En esta versión de la API, la presencia (no null) del valor de recurso indica que el archivo se eliminó. Un valor null (o ausente) indica que el archivo no se elimina.</span><span class="sxs-lookup"><span data-stu-id="2abe3-p101">The **Deleted** resource indicates that the item has been deleted. In this version of the API, the presence (non-null) of the resource value indicates that the file was deleted. A null (or missing) value indicates that the file is not deleted.</span></span>

<span data-ttu-id="2abe3-106">Consulte el artículo sobre cómo [ver los cambios de un elemento](../api/driveitem-delta.md) para obtener más información sobre el seguimiento de los cambios y la búsqueda de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="2abe3-106">See [view changes for an item](../api/driveitem-delta.md) for more information on tracking changes and finding deleted items.</span></span>

## <a name="json-representation"></a><span data-ttu-id="2abe3-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2abe3-107">JSON representation</span></span>

<span data-ttu-id="2abe3-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2abe3-108">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  "state"
  ],
  "@odata.type": "microsoft.graph.deleted"
}-->
```json
{
  "state": "string"
}
```
## <a name="properties"></a><span data-ttu-id="2abe3-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2abe3-109">Properties</span></span>

| <span data-ttu-id="2abe3-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2abe3-110">Property</span></span> | <span data-ttu-id="2abe3-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="2abe3-111">Type</span></span>   | <span data-ttu-id="2abe3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2abe3-112">Description</span></span>                               |
|:---------|:-------|:------------------------------------------|
| <span data-ttu-id="2abe3-113">state</span><span class="sxs-lookup"><span data-stu-id="2abe3-113">state</span></span>    | <span data-ttu-id="2abe3-114">String</span><span class="sxs-lookup"><span data-stu-id="2abe3-114">String</span></span> | <span data-ttu-id="2abe3-115">Representa el estado del elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="2abe3-115">Represents the state of the deleted item.</span></span> |

## <a name="remarks"></a><span data-ttu-id="2abe3-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2abe3-116">Remarks</span></span> 

<span data-ttu-id="2abe3-117">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="2abe3-117">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The deleted facet providers properties about deleted items",
  "keywords": "deleted,delete,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Deleted"
} -->
