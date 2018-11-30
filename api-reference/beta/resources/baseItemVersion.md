---
author: rgregg
ms.author: rgregg
ms.date: 09/17/2017
title: BaseItemVersion
ms.openlocfilehash: dfda19af6057bc1d6e1757d24f6a2c99979a8622
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083142"
---
# <a name="baseitemversion-resource-type"></a><span data-ttu-id="900d0-102">Tipo de recurso BaseItemVersion</span><span class="sxs-lookup"><span data-stu-id="900d0-102">BaseItemVersion resource type</span></span>

> <span data-ttu-id="900d0-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="900d0-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="900d0-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="900d0-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="900d0-105">El recurso **baseItemVersion** representa una versión anterior de un elemento o una entidad.</span><span class="sxs-lookup"><span data-stu-id="900d0-105">The **baseItemVersion** resource represents a previous version of an item or entity.</span></span>


## <a name="json-representation"></a><span data-ttu-id="900d0-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="900d0-106">JSON representation</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.baseItemVersion", "@type.aka": "oneDrive.baseItemVersion" } -->

```json
{
  "content": { "@odata.type": "Edm.Stream" },
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "publication": { "@odata.type": "microsoft.graph.publicationFacet" }
}
```

## <a name="properties"></a><span data-ttu-id="900d0-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="900d0-107">Properties</span></span>

|      <span data-ttu-id="900d0-108">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="900d0-108">Property name</span></span>       |                         <span data-ttu-id="900d0-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="900d0-109">Type</span></span>                         |                               <span data-ttu-id="900d0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="900d0-110">Description</span></span>                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| <span data-ttu-id="900d0-111">**id**</span><span class="sxs-lookup"><span data-stu-id="900d0-111">**id**</span></span>                   | <span data-ttu-id="900d0-112">string</span><span class="sxs-lookup"><span data-stu-id="900d0-112">string</span></span>                                               | <span data-ttu-id="900d0-113">El identificador de la versión.</span><span class="sxs-lookup"><span data-stu-id="900d0-113">The ID of the version.</span></span> <span data-ttu-id="900d0-114">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="900d0-114">Read-only.</span></span>                                       |
| <span data-ttu-id="900d0-115">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="900d0-115">**lastModifiedBy**</span></span>       | [<span data-ttu-id="900d0-116">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="900d0-116">IdentitySet</span></span>](../resources/identityset.md)           | <span data-ttu-id="900d0-117">Identidad del usuario que modificó por última vez la versión.</span><span class="sxs-lookup"><span data-stu-id="900d0-117">Identity of the user which last modified the version.</span></span> <span data-ttu-id="900d0-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="900d0-118">Read-only.</span></span>        |
| <span data-ttu-id="900d0-119">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="900d0-119">**lastModifiedDateTime**</span></span> | [<span data-ttu-id="900d0-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="900d0-120">DateTimeOffset</span></span>](../resources/timestamp.md)          | <span data-ttu-id="900d0-121">Fecha y hora de la última modificación de la versión.</span><span class="sxs-lookup"><span data-stu-id="900d0-121">Date and time the version was last modified.</span></span> <span data-ttu-id="900d0-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="900d0-122">Read-only.</span></span>                 |
| <span data-ttu-id="900d0-123">**publication**</span><span class="sxs-lookup"><span data-stu-id="900d0-123">**publication**</span></span>          | [<span data-ttu-id="900d0-124">PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="900d0-124">PublicationFacet</span></span>](../resources/publicationfacet.md) | <span data-ttu-id="900d0-125">Indica el estado de publicación de esta versión concreta.</span><span class="sxs-lookup"><span data-stu-id="900d0-125">Indicates the publication status of this particular version.</span></span> <span data-ttu-id="900d0-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="900d0-126">Read-only.</span></span> |


<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->