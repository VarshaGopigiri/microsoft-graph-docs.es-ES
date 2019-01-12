---
title: Tipo de recurso DriveItemVersion
description: El recurso **DriveItemVersion** representa una versión específica de un DriveItem.
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 5b6e9ecd2c3c8ec14958cfa2645f8fb0dbfe30e8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949594"
---
# <a name="driveitemversion-resource-type"></a><span data-ttu-id="1481b-103">Tipo de recurso DriveItemVersion</span><span class="sxs-lookup"><span data-stu-id="1481b-103">DriveItemVersion resource type</span></span>

<span data-ttu-id="1481b-104">El recurso **DriveItemVersion** representa una versión específica de un objeto [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="1481b-104">The **DriveItemVersion** resource represents a specific version of a [DriveItem](driveitem.md).</span></span>


## <a name="tasks-on-driveitemversion-resources"></a><span data-ttu-id="1481b-105">Tareas en recursos DriveItemVersion</span><span class="sxs-lookup"><span data-stu-id="1481b-105">Tasks on DriveItemVersion resources</span></span>

<span data-ttu-id="1481b-106">Las tareas siguientes están disponibles para los recursos driveItemVersion.</span><span class="sxs-lookup"><span data-stu-id="1481b-106">The following tasks are available for driveItemVersion resources.</span></span>

|            <span data-ttu-id="1481b-107">Tarea común</span><span class="sxs-lookup"><span data-stu-id="1481b-107">Common task</span></span>             |         <span data-ttu-id="1481b-108">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="1481b-108">HTTP method</span></span>         |
| :--------------------------------- | :-------------------------- |
| <span data-ttu-id="1481b-109">[Enumerar versiones][version-list]</span><span class="sxs-lookup"><span data-stu-id="1481b-109">[List versions][version-list]</span></span>      | `GET /drive/items/{item-id}/versions`  |
| <span data-ttu-id="1481b-110">[Obtener versión][version-get]</span><span class="sxs-lookup"><span data-stu-id="1481b-110">[Get version][version-get]</span></span>         | `GET /drive/items/{item-id}/versions/{version-id}`     |
| <span data-ttu-id="1481b-111">[Obtener contenido][content-get]</span><span class="sxs-lookup"><span data-stu-id="1481b-111">[Get contents][content-get]</span></span>        | `GET /drive/items/{item-id}/versions/{version-id}/content` |
| <span data-ttu-id="1481b-112">[Restaurar versión][version-restore]</span><span class="sxs-lookup"><span data-stu-id="1481b-112">[Restore version][version-restore]</span></span> | `POST /drive/items/{item-id}/versions/{version-id}/restore` |

[version-list]: ../api/driveitem-list-versions.md
[version-get]: ../api/driveitemversion-get.md
[content-get]: ../api/driveitemversion-get-contents.md
[version-restore]: ../api/driveitemversion-restore.md

<span data-ttu-id="1481b-113">En la tabla anterior, los ejemplos usan `/drive`, pero hay varias solicitudes válidas.</span><span class="sxs-lookup"><span data-stu-id="1481b-113">In the previous table, the examples use `/drive`, but there are many valid requests.</span></span>

## <a name="json-representation"></a><span data-ttu-id="1481b-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1481b-114">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="1481b-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1481b-115">Properties</span></span>

|      <span data-ttu-id="1481b-116">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="1481b-116">Property name</span></span>       |                         <span data-ttu-id="1481b-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="1481b-117">Type</span></span>                         |                               <span data-ttu-id="1481b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="1481b-118">Description</span></span>                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| <span data-ttu-id="1481b-119">**id**</span><span class="sxs-lookup"><span data-stu-id="1481b-119">**id**</span></span>                   | <span data-ttu-id="1481b-120">string</span><span class="sxs-lookup"><span data-stu-id="1481b-120">string</span></span>                                               | <span data-ttu-id="1481b-121">El identificador de la versión.</span><span class="sxs-lookup"><span data-stu-id="1481b-121">The ID of the version.</span></span> <span data-ttu-id="1481b-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1481b-122">Read-only.</span></span>                                       |
| <span data-ttu-id="1481b-123">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="1481b-123">**lastModifiedBy**</span></span>       | [<span data-ttu-id="1481b-124">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="1481b-124">IdentitySet</span></span>](../resources/identityset.md)           | <span data-ttu-id="1481b-125">Identidad del usuario que modificó por última vez la versión.</span><span class="sxs-lookup"><span data-stu-id="1481b-125">Identity of the user which last modified the version.</span></span> <span data-ttu-id="1481b-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1481b-126">Read-only.</span></span>        |
| <span data-ttu-id="1481b-127">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="1481b-127">**lastModifiedDateTime**</span></span> | [<span data-ttu-id="1481b-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1481b-128">DateTimeOffset</span></span>](../resources/timestamp.md)          | <span data-ttu-id="1481b-129">Fecha y hora de la última modificación de la versión.</span><span class="sxs-lookup"><span data-stu-id="1481b-129">Date and time the version was last modified.</span></span> <span data-ttu-id="1481b-130">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1481b-130">Read-only.</span></span>                 |
| <span data-ttu-id="1481b-131">**publication**</span><span class="sxs-lookup"><span data-stu-id="1481b-131">**publication**</span></span>          | [<span data-ttu-id="1481b-132">PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="1481b-132">PublicationFacet</span></span>](../resources/publicationfacet.md) | <span data-ttu-id="1481b-133">Indica el estado de publicación de esta versión concreta.</span><span class="sxs-lookup"><span data-stu-id="1481b-133">Indicates the publication status of this particular version.</span></span> <span data-ttu-id="1481b-134">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1481b-134">Read-only.</span></span> |
| <span data-ttu-id="1481b-135">**size**</span><span class="sxs-lookup"><span data-stu-id="1481b-135">**size**</span></span>                 | <span data-ttu-id="1481b-136">Int64</span><span class="sxs-lookup"><span data-stu-id="1481b-136">Int64</span></span>                                                | <span data-ttu-id="1481b-137">Indica el tamaño de la secuencia de contenido para esta versión del elemento.</span><span class="sxs-lookup"><span data-stu-id="1481b-137">Indicates the size of the content stream for this version of the item.</span></span>  |
| <span data-ttu-id="1481b-138">**content**</span><span class="sxs-lookup"><span data-stu-id="1481b-138">**content**</span></span>              | <span data-ttu-id="1481b-139">Secuencia</span><span class="sxs-lookup"><span data-stu-id="1481b-139">Stream</span></span>                                               | <span data-ttu-id="1481b-140">La secuencia de contenido para esta versión del elemento.</span><span class="sxs-lookup"><span data-stu-id="1481b-140">The content stream for this version of the item.</span></span>                        |

<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
