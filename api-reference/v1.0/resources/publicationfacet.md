---
title: Tipo de recurso PublicationFacet
description: El recurso **publicationFacet** proporciona información detallada sobre el estado publicado de un recurso driveItemVersion o driveItem.
ms.openlocfilehash: 429ec649dc9f511a4012e6790842fdd774bead8b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029163"
---
# <a name="publicationfacet-resource-type"></a><span data-ttu-id="76037-103">Tipo de recurso PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="76037-103">PublicationFacet resource type</span></span>

<span data-ttu-id="76037-104">El recurso **publicationFacet** proporciona información detallada sobre el estado publicado de un recurso [driveItemVersion](driveitemversion.md) o [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="76037-104">The **publicationFacet** resource provides details on the published status of a [driveItemVersion](driveitemversion.md) or [driveItem](driveitem.md) resource.</span></span>

## <a name="json-representation"></a><span data-ttu-id="76037-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="76037-105">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.publicationFacet"
}-->

```json
{
  "level": "published | checkout",
  "versionId": "string"
}
```

## <a name="properties"></a><span data-ttu-id="76037-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="76037-106">Properties</span></span>

|   <span data-ttu-id="76037-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="76037-107">Property</span></span>    |  <span data-ttu-id="76037-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="76037-108">Type</span></span>  | <span data-ttu-id="76037-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="76037-109">Description</span></span> |
| :------------ | :----- | :---------- |
| <span data-ttu-id="76037-110">**level**</span><span class="sxs-lookup"><span data-stu-id="76037-110">**level**</span></span>     | <span data-ttu-id="76037-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="76037-111">String</span></span> | <span data-ttu-id="76037-112">El estado de publicación de este documento.</span><span class="sxs-lookup"><span data-stu-id="76037-112">The state of publication for this document.</span></span> <span data-ttu-id="76037-113">`published` o `checkout`.</span><span class="sxs-lookup"><span data-stu-id="76037-113">Either `published` or `checkout`.</span></span> <span data-ttu-id="76037-114">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="76037-114">Read-only.</span></span>  |
| <span data-ttu-id="76037-115">**versionId**</span><span class="sxs-lookup"><span data-stu-id="76037-115">**versionId**</span></span> | <span data-ttu-id="76037-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="76037-116">String</span></span> | <span data-ttu-id="76037-117">El identificador único de la versión que está visible para el llamador actual.</span><span class="sxs-lookup"><span data-stu-id="76037-117">The unique identifier for the version that is visible to the current caller.</span></span> <span data-ttu-id="76037-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="76037-118">Read-only.</span></span>  |


<!-- {
  "type": "#page.annotation",
  "description": "The photo facet provides details about the camera and settings on the camera for photos.",
  "keywords": "camera make,camera model, exposure, f-stop, iso",
  "section": "documentation",
  "suppressions": [
    " Warning: /api-reference/v1.0/resources/publicationfacet.md:
      Found potential enums in resource example that weren't defined in a table:(published,checkout) are in resource, but () are in table"
  ],
  "tocPath": "Facets/Photo"
} -->
