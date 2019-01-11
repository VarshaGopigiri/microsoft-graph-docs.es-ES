---
title: Tipo de recurso BaseItemVersion
description: El recurso **baseItemVersion** representa una versión anterior de un elemento o una entidad.
localization_priority: Normal
ms.openlocfilehash: bd28f9c8dc5be2bc6422aca2eb756aba78b8e393
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876968"
---
# <a name="baseitemversion-resource-type"></a><span data-ttu-id="e1891-103">Tipo de recurso BaseItemVersion</span><span class="sxs-lookup"><span data-stu-id="e1891-103">BaseItemVersion resource type</span></span>

<span data-ttu-id="e1891-104">El recurso **baseItemVersion** representa una versión anterior de un elemento o una entidad.</span><span class="sxs-lookup"><span data-stu-id="e1891-104">The **baseItemVersion** resource represents a previous version of an item or entity.</span></span>


## <a name="json-representation"></a><span data-ttu-id="e1891-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e1891-105">JSON representation</span></span>

<!--{
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.baseItemVersion",
  "@type.aka": "oneDrive.baseItemVersion"
}-->

```json
{
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "publication": { "@odata.type": "microsoft.graph.publicationFacet" }
}
```

## <a name="properties"></a><span data-ttu-id="e1891-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e1891-106">Properties</span></span>

|      <span data-ttu-id="e1891-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="e1891-107">Property name</span></span>       |                         <span data-ttu-id="e1891-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1891-108">Type</span></span>                         |                               <span data-ttu-id="e1891-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1891-109">Description</span></span>                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| <span data-ttu-id="e1891-110">**id**</span><span class="sxs-lookup"><span data-stu-id="e1891-110">**id**</span></span>                   | <span data-ttu-id="e1891-111">string</span><span class="sxs-lookup"><span data-stu-id="e1891-111">string</span></span>                                               | <span data-ttu-id="e1891-112">El identificador de la versión.</span><span class="sxs-lookup"><span data-stu-id="e1891-112">The ID of the version.</span></span> <span data-ttu-id="e1891-113">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e1891-113">Read-only.</span></span>                                       |
| <span data-ttu-id="e1891-114">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="e1891-114">**lastModifiedBy**</span></span>       | [<span data-ttu-id="e1891-115">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="e1891-115">IdentitySet</span></span>](../resources/identityset.md)           | <span data-ttu-id="e1891-116">Identidad del usuario que modificó por última vez la versión.</span><span class="sxs-lookup"><span data-stu-id="e1891-116">Identity of the user which last modified the version.</span></span> <span data-ttu-id="e1891-117">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e1891-117">Read-only.</span></span>        |
| <span data-ttu-id="e1891-118">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="e1891-118">**lastModifiedDateTime**</span></span> | [<span data-ttu-id="e1891-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e1891-119">DateTimeOffset</span></span>](../resources/timestamp.md)          | <span data-ttu-id="e1891-120">Fecha y hora de la última modificación de la versión.</span><span class="sxs-lookup"><span data-stu-id="e1891-120">Date and time the version was last modified.</span></span> <span data-ttu-id="e1891-121">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e1891-121">Read-only.</span></span>                 |
| <span data-ttu-id="e1891-122">**publication**</span><span class="sxs-lookup"><span data-stu-id="e1891-122">**publication**</span></span>          | [<span data-ttu-id="e1891-123">PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="e1891-123">PublicationFacet</span></span>](../resources/publicationfacet.md) | <span data-ttu-id="e1891-124">Indica el estado de publicación de esta versión concreta.</span><span class="sxs-lookup"><span data-stu-id="e1891-124">Indicates the publication status of this particular version.</span></span> <span data-ttu-id="e1891-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e1891-125">Read-only.</span></span> |


<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
