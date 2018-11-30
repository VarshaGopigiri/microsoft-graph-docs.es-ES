---
title: Tipo de recurso BaseItemVersion
description: El recurso **baseItemVersion** representa una versión anterior de un elemento o una entidad.
ms.openlocfilehash: c4fc95fd419bf8b2f20ab202874ca31a2b1d63f6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030084"
---
# <a name="baseitemversion-resource-type"></a><span data-ttu-id="23943-103">Tipo de recurso BaseItemVersion</span><span class="sxs-lookup"><span data-stu-id="23943-103">BaseItemVersion resource type</span></span>

<span data-ttu-id="23943-104">El recurso **baseItemVersion** representa una versión anterior de un elemento o una entidad.</span><span class="sxs-lookup"><span data-stu-id="23943-104">The **baseItemVersion** resource represents a previous version of an item or entity.</span></span>


## <a name="json-representation"></a><span data-ttu-id="23943-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="23943-105">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="23943-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23943-106">Properties</span></span>

|      <span data-ttu-id="23943-107">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="23943-107">Property name</span></span>       |                         <span data-ttu-id="23943-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="23943-108">Type</span></span>                         |                               <span data-ttu-id="23943-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="23943-109">Description</span></span>                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| <span data-ttu-id="23943-110">**id**</span><span class="sxs-lookup"><span data-stu-id="23943-110">**id**</span></span>                   | <span data-ttu-id="23943-111">string</span><span class="sxs-lookup"><span data-stu-id="23943-111">string</span></span>                                               | <span data-ttu-id="23943-112">El identificador de la versión.</span><span class="sxs-lookup"><span data-stu-id="23943-112">The ID of the version.</span></span> <span data-ttu-id="23943-113">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="23943-113">Read-only.</span></span>                                       |
| <span data-ttu-id="23943-114">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="23943-114">**lastModifiedBy**</span></span>       | [<span data-ttu-id="23943-115">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="23943-115">IdentitySet</span></span>](../resources/identityset.md)           | <span data-ttu-id="23943-116">Identidad del usuario que modificó por última vez la versión.</span><span class="sxs-lookup"><span data-stu-id="23943-116">Identity of the user which last modified the version.</span></span> <span data-ttu-id="23943-117">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="23943-117">Read-only.</span></span>        |
| <span data-ttu-id="23943-118">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="23943-118">**lastModifiedDateTime**</span></span> | [<span data-ttu-id="23943-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="23943-119">DateTimeOffset</span></span>](../resources/timestamp.md)          | <span data-ttu-id="23943-120">Fecha y hora de la última modificación de la versión.</span><span class="sxs-lookup"><span data-stu-id="23943-120">Date and time the version was last modified.</span></span> <span data-ttu-id="23943-121">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="23943-121">Read-only.</span></span>                 |
| <span data-ttu-id="23943-122">**publication**</span><span class="sxs-lookup"><span data-stu-id="23943-122">**publication**</span></span>          | [<span data-ttu-id="23943-123">PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="23943-123">PublicationFacet</span></span>](../resources/publicationfacet.md) | <span data-ttu-id="23943-124">Indica el estado de publicación de esta versión concreta.</span><span class="sxs-lookup"><span data-stu-id="23943-124">Indicates the publication status of this particular version.</span></span> <span data-ttu-id="23943-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="23943-125">Read-only.</span></span> |


<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
