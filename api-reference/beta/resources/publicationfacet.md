---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: PublicationFacet
localization_priority: Normal
ms.openlocfilehash: 4cb3a56b5bdb4c3e7c9fc9fe69c0b34cae134a0d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805610"
---
# <a name="publicationfacet-resource-type"></a><span data-ttu-id="5feb5-102">Tipo de recurso PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="5feb5-102">PublicationFacet resource type</span></span>

> <span data-ttu-id="5feb5-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5feb5-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5feb5-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5feb5-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5feb5-105">El recurso **publicationFacet** proporciona información detallada sobre el estado publicado de un recurso [driveItemVersion](driveitemversion.md) o [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="5feb5-105">The **publicationFacet** resource provides details on the published status of a [driveItemVersion](driveitemversion.md) or [driveItem](driveitem.md) resource.</span></span>

## <a name="json-representation"></a><span data-ttu-id="5feb5-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5feb5-106">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="5feb5-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5feb5-107">Properties</span></span>

|   <span data-ttu-id="5feb5-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5feb5-108">Property</span></span>    |  <span data-ttu-id="5feb5-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5feb5-109">Type</span></span>  | <span data-ttu-id="5feb5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5feb5-110">Description</span></span> |
| :------------ | :----- | :---------- |
| <span data-ttu-id="5feb5-111">**level**</span><span class="sxs-lookup"><span data-stu-id="5feb5-111">**level**</span></span>     | <span data-ttu-id="5feb5-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="5feb5-112">String</span></span> | <span data-ttu-id="5feb5-113">El estado de publicación de este documento.</span><span class="sxs-lookup"><span data-stu-id="5feb5-113">The state of publication for this document.</span></span> <span data-ttu-id="5feb5-114">`published` o `checkout`.</span><span class="sxs-lookup"><span data-stu-id="5feb5-114">Either `published` or `checkout`.</span></span> <span data-ttu-id="5feb5-115">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5feb5-115">Read-only.</span></span>  |
| <span data-ttu-id="5feb5-116">**versionId**</span><span class="sxs-lookup"><span data-stu-id="5feb5-116">**versionId**</span></span> | <span data-ttu-id="5feb5-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="5feb5-117">String</span></span> | <span data-ttu-id="5feb5-118">El identificador único de la versión que está visible para el llamador actual.</span><span class="sxs-lookup"><span data-stu-id="5feb5-118">The unique identifier for the version that is visible to the current caller.</span></span> <span data-ttu-id="5feb5-119">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5feb5-119">Read-only.</span></span>  |


<!-- {
  "type": "#page.annotation",
  "description": "The photo facet provides details about the camera and settings on the camera for photos.",
  "keywords": "camera make,camera model, exposure, f-stop, iso",
  "section": "documentation",
  "tocPath": "Facets/Photo"
} -->
