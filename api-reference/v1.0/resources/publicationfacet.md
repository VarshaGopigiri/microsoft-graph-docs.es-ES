---
title: Tipo de recurso PublicationFacet
description: El recurso **publicationFacet** proporciona información detallada sobre el estado publicado de un recurso driveItemVersion o driveItem.
localization_priority: Normal
ms.openlocfilehash: 3d722f56cf1d587483c672fb7a1b7c05abd3671b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810532"
---
# <a name="publicationfacet-resource-type"></a><span data-ttu-id="0b5ae-103">Tipo de recurso PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="0b5ae-103">PublicationFacet resource type</span></span>

<span data-ttu-id="0b5ae-104">El recurso **publicationFacet** proporciona información detallada sobre el estado publicado de un recurso [driveItemVersion](driveitemversion.md) o [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="0b5ae-104">The **publicationFacet** resource provides details on the published status of a [driveItemVersion](driveitemversion.md) or [driveItem](driveitem.md) resource.</span></span>

## <a name="json-representation"></a><span data-ttu-id="0b5ae-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0b5ae-105">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="0b5ae-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b5ae-106">Properties</span></span>

|   <span data-ttu-id="0b5ae-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0b5ae-107">Property</span></span>    |  <span data-ttu-id="0b5ae-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b5ae-108">Type</span></span>  | <span data-ttu-id="0b5ae-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b5ae-109">Description</span></span> |
| :------------ | :----- | :---------- |
| <span data-ttu-id="0b5ae-110">**level**</span><span class="sxs-lookup"><span data-stu-id="0b5ae-110">**level**</span></span>     | <span data-ttu-id="0b5ae-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="0b5ae-111">String</span></span> | <span data-ttu-id="0b5ae-112">El estado de publicación de este documento.</span><span class="sxs-lookup"><span data-stu-id="0b5ae-112">The state of publication for this document.</span></span> <span data-ttu-id="0b5ae-113">`published` o `checkout`.</span><span class="sxs-lookup"><span data-stu-id="0b5ae-113">Either `published` or `checkout`.</span></span> <span data-ttu-id="0b5ae-114">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0b5ae-114">Read-only.</span></span>  |
| <span data-ttu-id="0b5ae-115">**versionId**</span><span class="sxs-lookup"><span data-stu-id="0b5ae-115">**versionId**</span></span> | <span data-ttu-id="0b5ae-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="0b5ae-116">String</span></span> | <span data-ttu-id="0b5ae-117">El identificador único de la versión que está visible para el llamador actual.</span><span class="sxs-lookup"><span data-stu-id="0b5ae-117">The unique identifier for the version that is visible to the current caller.</span></span> <span data-ttu-id="0b5ae-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0b5ae-118">Read-only.</span></span>  |


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
