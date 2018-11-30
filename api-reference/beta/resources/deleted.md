---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Eliminados
ms.openlocfilehash: 5a0dd4132f39574f0af04282bd3f39bfd303eef1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084796"
---
# <a name="deleted-facet"></a><span data-ttu-id="b1f18-102">Faceta Deleted</span><span class="sxs-lookup"><span data-stu-id="b1f18-102">Deleted facet</span></span>

> <span data-ttu-id="b1f18-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b1f18-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b1f18-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b1f18-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b1f18-p102">El recurso **Deleted** indica que el elemento se ha eliminado. En esta versión de la API, la presencia (no null) del valor de recurso indica que el archivo se eliminó. Un valor null (o ausente) indica que el archivo no se elimina.</span><span class="sxs-lookup"><span data-stu-id="b1f18-p102">The **Deleted** resource indicates that the item has been deleted. In this version of the API, the presence (non-null) of the resource value indicates that the file was deleted. A null (or missing) value indicates that the file is not deleted.</span></span>

<span data-ttu-id="b1f18-108">Consulte el artículo sobre cómo [ver los cambios de un elemento](../api/driveitem-delta.md) para obtener más información sobre el seguimiento de los cambios y la búsqueda de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b1f18-108">See [view changes for an item](../api/driveitem-delta.md) for more information on tracking changes and finding deleted items.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b1f18-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b1f18-109">JSON representation</span></span>

<span data-ttu-id="b1f18-110">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b1f18-110">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="b1f18-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b1f18-111">Properties</span></span>

| <span data-ttu-id="b1f18-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b1f18-112">Property</span></span> | <span data-ttu-id="b1f18-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1f18-113">Type</span></span>   | <span data-ttu-id="b1f18-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1f18-114">Description</span></span>                               |
|:---------|:-------|:------------------------------------------|
| <span data-ttu-id="b1f18-115">state</span><span class="sxs-lookup"><span data-stu-id="b1f18-115">state</span></span>    | <span data-ttu-id="b1f18-116">String</span><span class="sxs-lookup"><span data-stu-id="b1f18-116">String</span></span> | <span data-ttu-id="b1f18-117">Representa el estado del elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="b1f18-117">Represents the state of the deleted item.</span></span> |

## <a name="remarks"></a><span data-ttu-id="b1f18-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1f18-118">Remarks</span></span> 

<span data-ttu-id="b1f18-119">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="b1f18-119">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The deleted facet providers properties about deleted items",
  "keywords": "deleted,delete,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Deleted"
} -->
