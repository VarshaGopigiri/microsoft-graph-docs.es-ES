---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Eliminados
ms.openlocfilehash: 6a51d858f529e65820d7bc55bb7ec8fec80186d4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029017"
---
# <a name="deleted-facet"></a><span data-ttu-id="b9673-102">Faceta Deleted</span><span class="sxs-lookup"><span data-stu-id="b9673-102">Deleted facet</span></span>

<span data-ttu-id="b9673-p101">El recurso **Deleted** indica que el elemento se ha eliminado. En esta versión de la API, la presencia (no null) del valor de recurso indica que el archivo se eliminó. Un valor null (o ausente) indica que el archivo no se elimina.</span><span class="sxs-lookup"><span data-stu-id="b9673-p101">The **Deleted** resource indicates that the item has been deleted. In this version of the API, the presence (non-null) of the resource value indicates that the file was deleted. A null (or missing) value indicates that the file is not deleted.</span></span>

<span data-ttu-id="b9673-106">Consulte el artículo sobre cómo [ver los cambios de un elemento](../api/driveitem-delta.md) para obtener más información sobre el seguimiento de los cambios y la búsqueda de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b9673-106">See [view changes for an item](../api/driveitem-delta.md) for more information on tracking changes and finding deleted items.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b9673-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b9673-107">JSON representation</span></span>

<span data-ttu-id="b9673-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b9673-108">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="b9673-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9673-109">Properties</span></span>

| <span data-ttu-id="b9673-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b9673-110">Property</span></span> | <span data-ttu-id="b9673-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9673-111">Type</span></span>   | <span data-ttu-id="b9673-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9673-112">Description</span></span>                               |
|:---------|:-------|:------------------------------------------|
| <span data-ttu-id="b9673-113">state</span><span class="sxs-lookup"><span data-stu-id="b9673-113">state</span></span>    | <span data-ttu-id="b9673-114">String</span><span class="sxs-lookup"><span data-stu-id="b9673-114">String</span></span> | <span data-ttu-id="b9673-115">Representa el estado del elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="b9673-115">Represents the state of the deleted item.</span></span> |

## <a name="remarks"></a><span data-ttu-id="b9673-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b9673-116">Remarks</span></span> 

<span data-ttu-id="b9673-117">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="b9673-117">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The deleted facet providers properties about deleted items",
  "keywords": "deleted,delete,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Deleted"
} -->
