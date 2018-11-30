---
title: Tipo de recurso DriveItemVersion
description: El recurso **DriveItemVersion** representa una versión específica de un DriveItem.
ms.openlocfilehash: e257e800b0ac8ad4d94027f9c8040ffb3b20ea90
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030237"
---
# <a name="driveitemversion-resource-type"></a><span data-ttu-id="daef7-103">Tipo de recurso DriveItemVersion</span><span class="sxs-lookup"><span data-stu-id="daef7-103">DriveItemVersion resource type</span></span>

<span data-ttu-id="daef7-104">El recurso **DriveItemVersion** representa una versión específica de un objeto [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="daef7-104">The **DriveItemVersion** resource represents a specific version of a [DriveItem](driveitem.md).</span></span>


## <a name="tasks-on-driveitemversion-resources"></a><span data-ttu-id="daef7-105">Tareas en recursos DriveItemVersion</span><span class="sxs-lookup"><span data-stu-id="daef7-105">Tasks on DriveItemVersion resources</span></span>

<span data-ttu-id="daef7-106">Las tareas siguientes están disponibles para los recursos driveItemVersion.</span><span class="sxs-lookup"><span data-stu-id="daef7-106">The following tasks are available for driveItemVersion resources.</span></span>

|            <span data-ttu-id="daef7-107">Tarea común</span><span class="sxs-lookup"><span data-stu-id="daef7-107">Common task</span></span>             |         <span data-ttu-id="daef7-108">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="daef7-108">HTTP method</span></span>         |
| :--------------------------------- | :-------------------------- |
| <span data-ttu-id="daef7-109">[Enumerar versiones][version-list]</span><span class="sxs-lookup"><span data-stu-id="daef7-109">[List versions][version-list]</span></span>      | `GET /drive/items/{item-id}/versions`  |
| <span data-ttu-id="daef7-110">[Obtener versión][version-get]</span><span class="sxs-lookup"><span data-stu-id="daef7-110">[Get version][version-get]</span></span>         | `GET /drive/items/{item-id}/versions/{version-id}`     |
| <span data-ttu-id="daef7-111">[Obtener contenido][content-get]</span><span class="sxs-lookup"><span data-stu-id="daef7-111">[Get contents][content-get]</span></span>        | `GET /drive/items/{item-id}/versions/{version-id}/content` |
| <span data-ttu-id="daef7-112">[Restaurar versión][version-restore]</span><span class="sxs-lookup"><span data-stu-id="daef7-112">[Restore version][version-restore]</span></span> | `POST /drive/items/{item-id}/versions/{version-id}/restore` |

[version-list]: ../api/driveitem-list-versions.md
[version-get]: ../api/driveitemversion-get.md
[content-get]: ../api/driveitemversion-get-contents.md
[version-restore]: ../api/driveitemversion-restore.md

<span data-ttu-id="daef7-113">En la tabla anterior, los ejemplos usan `/drive`, pero hay varias solicitudes válidas.</span><span class="sxs-lookup"><span data-stu-id="daef7-113">In the previous table, the examples use `/drive`, but there are many valid requests.</span></span>

## <a name="json-representation"></a><span data-ttu-id="daef7-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="daef7-114">JSON representation</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.baseItemVersion",
  "@odata.type": "microsoft.graph.driveItemVersion",
  "@type.aka": "oneDrive.driveItemVersion"
}-->

```json
{
  "content": { "@odata.type": "Edm.Stream" },
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "publication": { "@odata.type": "microsoft.graph.publicationFacet" },
  "size": 12356
}
```

## <a name="properties"></a><span data-ttu-id="daef7-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="daef7-115">Properties</span></span>

|      <span data-ttu-id="daef7-116">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="daef7-116">Property name</span></span>       |                         <span data-ttu-id="daef7-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="daef7-117">Type</span></span>                         |                               <span data-ttu-id="daef7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="daef7-118">Description</span></span>                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| <span data-ttu-id="daef7-119">**id**</span><span class="sxs-lookup"><span data-stu-id="daef7-119">**id**</span></span>                   | <span data-ttu-id="daef7-120">string</span><span class="sxs-lookup"><span data-stu-id="daef7-120">string</span></span>                                               | <span data-ttu-id="daef7-121">El identificador de la versión.</span><span class="sxs-lookup"><span data-stu-id="daef7-121">The ID of the version.</span></span> <span data-ttu-id="daef7-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="daef7-122">Read-only.</span></span>                                       |
| <span data-ttu-id="daef7-123">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="daef7-123">**lastModifiedBy**</span></span>       | [<span data-ttu-id="daef7-124">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="daef7-124">IdentitySet</span></span>](../resources/identityset.md)           | <span data-ttu-id="daef7-125">Identidad del usuario que modificó por última vez la versión.</span><span class="sxs-lookup"><span data-stu-id="daef7-125">Identity of the user which last modified the version.</span></span> <span data-ttu-id="daef7-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="daef7-126">Read-only.</span></span>        |
| <span data-ttu-id="daef7-127">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="daef7-127">**lastModifiedDateTime**</span></span> | [<span data-ttu-id="daef7-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="daef7-128">DateTimeOffset</span></span>](../resources/timestamp.md)          | <span data-ttu-id="daef7-129">Fecha y hora de la última modificación de la versión.</span><span class="sxs-lookup"><span data-stu-id="daef7-129">Date and time the version was last modified.</span></span> <span data-ttu-id="daef7-130">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="daef7-130">Read-only.</span></span>                 |
| <span data-ttu-id="daef7-131">**publication**</span><span class="sxs-lookup"><span data-stu-id="daef7-131">**publication**</span></span>          | [<span data-ttu-id="daef7-132">PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="daef7-132">PublicationFacet</span></span>](../resources/publicationfacet.md) | <span data-ttu-id="daef7-133">Indica el estado de publicación de esta versión concreta.</span><span class="sxs-lookup"><span data-stu-id="daef7-133">Indicates the publication status of this particular version.</span></span> <span data-ttu-id="daef7-134">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="daef7-134">Read-only.</span></span> |
| <span data-ttu-id="daef7-135">**size**</span><span class="sxs-lookup"><span data-stu-id="daef7-135">**size**</span></span>                 | <span data-ttu-id="daef7-136">Int64</span><span class="sxs-lookup"><span data-stu-id="daef7-136">Int64</span></span>                                                | <span data-ttu-id="daef7-137">Indica el tamaño de la secuencia de contenido para esta versión del elemento.</span><span class="sxs-lookup"><span data-stu-id="daef7-137">Indicates the size of the content stream for this version of the item.</span></span>  |
| <span data-ttu-id="daef7-138">**content**</span><span class="sxs-lookup"><span data-stu-id="daef7-138">**content**</span></span>              | <span data-ttu-id="daef7-139">Secuencia</span><span class="sxs-lookup"><span data-stu-id="daef7-139">Stream</span></span>                                               | <span data-ttu-id="daef7-140">La secuencia de contenido para esta versión del elemento.</span><span class="sxs-lookup"><span data-stu-id="daef7-140">The content stream for this version of the item.</span></span>                        |

<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
