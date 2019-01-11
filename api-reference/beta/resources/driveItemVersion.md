---
author: rgregg
ms.author: rgregg
ms.date: 09/17/2017
title: DriveItemVersion
localization_priority: Normal
ms.openlocfilehash: 4267a82cc2dee7f0b9b301e13073f32cf95c6844
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27841744"
---
# <a name="driveitemversion-resource-type"></a><span data-ttu-id="969e0-102">Tipo de recurso DriveItemVersion</span><span class="sxs-lookup"><span data-stu-id="969e0-102">DriveItemVersion resource type</span></span>

> <span data-ttu-id="969e0-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="969e0-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="969e0-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="969e0-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="969e0-105">El recurso **DriveItemVersion** representa una versión específica de un objeto [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="969e0-105">The **DriveItemVersion** resource represents a specific version of a [DriveItem](driveitem.md).</span></span>


## <a name="tasks-on-driveitemversion-resources"></a><span data-ttu-id="969e0-106">Tareas en recursos DriveItemVersion</span><span class="sxs-lookup"><span data-stu-id="969e0-106">Tasks on DriveItemVersion resources</span></span>

<span data-ttu-id="969e0-107">Las tareas siguientes están disponibles para los recursos driveItemVersion.</span><span class="sxs-lookup"><span data-stu-id="969e0-107">The following tasks are available for driveItemVersion resources.</span></span>

|            <span data-ttu-id="969e0-108">Tarea común</span><span class="sxs-lookup"><span data-stu-id="969e0-108">Common task</span></span>             |         <span data-ttu-id="969e0-109">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="969e0-109">HTTP method</span></span>         |
| :--------------------------------- | :-------------------------- |
| <span data-ttu-id="969e0-110">[Enumerar versiones][version-list]</span><span class="sxs-lookup"><span data-stu-id="969e0-110">[List versions][version-list]</span></span>      | `GET /drive/items/{item-id}/versions`  |
| <span data-ttu-id="969e0-111">[Obtener versión][version-get]</span><span class="sxs-lookup"><span data-stu-id="969e0-111">[Get version][version-get]</span></span>         | `GET /drive/items/{item-id}/versions/{version-id}`     |
| <span data-ttu-id="969e0-112">[Obtener contenido][content-get]</span><span class="sxs-lookup"><span data-stu-id="969e0-112">[Get contents][content-get]</span></span>        | `GET /drive/items/{item-id}/versions/{version-id}/content` |
| <span data-ttu-id="969e0-113">[Restaurar versión][version-restore]</span><span class="sxs-lookup"><span data-stu-id="969e0-113">[Restore version][version-restore]</span></span> | `POST /drive/items/{item-id}/versions/{version-id}/restore` |

[version-list]: ../api/driveitem-list-versions.md
[version-get]: ../api/driveitemversion-get.md
[content-get]: ../api/driveitemversion-get-contents.md
[version-restore]: ../api/driveitemversion-restore.md

<span data-ttu-id="969e0-114">En la tabla anterior, los ejemplos usan `/drive`, pero hay varias solicitudes válidas.</span><span class="sxs-lookup"><span data-stu-id="969e0-114">In the previous table, the examples use `/drive`, but there are many valid requests.</span></span>

## <a name="json-representation"></a><span data-ttu-id="969e0-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="969e0-115">JSON representation</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.driveItemVersion", "@type.aka": "oneDrive.driveItemVersion" } -->

```json
{
  "content": { "@odata.type": "Edm.Stream" },
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "publication": { "@odata.type": "microsoft.graph.publicationFacet" }
}
```

## <a name="properties"></a><span data-ttu-id="969e0-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="969e0-116">Properties</span></span>

|      <span data-ttu-id="969e0-117">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="969e0-117">Property name</span></span>       |                         <span data-ttu-id="969e0-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="969e0-118">Type</span></span>                         |                               <span data-ttu-id="969e0-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="969e0-119">Description</span></span>                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| <span data-ttu-id="969e0-120">**id**</span><span class="sxs-lookup"><span data-stu-id="969e0-120">**id**</span></span>                   | <span data-ttu-id="969e0-121">string</span><span class="sxs-lookup"><span data-stu-id="969e0-121">string</span></span>                                               | <span data-ttu-id="969e0-122">El identificador de la versión.</span><span class="sxs-lookup"><span data-stu-id="969e0-122">The ID of the version.</span></span> <span data-ttu-id="969e0-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="969e0-123">Read-only.</span></span>                                       |
| <span data-ttu-id="969e0-124">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="969e0-124">**lastModifiedBy**</span></span>       | [<span data-ttu-id="969e0-125">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="969e0-125">IdentitySet</span></span>](../resources/identityset.md)           | <span data-ttu-id="969e0-126">Identidad del usuario que modificó por última vez la versión.</span><span class="sxs-lookup"><span data-stu-id="969e0-126">Identity of the user which last modified the version.</span></span> <span data-ttu-id="969e0-127">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="969e0-127">Read-only.</span></span>        |
| <span data-ttu-id="969e0-128">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="969e0-128">**lastModifiedDateTime**</span></span> | [<span data-ttu-id="969e0-129">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="969e0-129">DateTimeOffset</span></span>](../resources/timestamp.md)          | <span data-ttu-id="969e0-130">Fecha y hora de la última modificación de la versión.</span><span class="sxs-lookup"><span data-stu-id="969e0-130">Date and time the version was last modified.</span></span> <span data-ttu-id="969e0-131">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="969e0-131">Read-only.</span></span>                 |
| <span data-ttu-id="969e0-132">**publication**</span><span class="sxs-lookup"><span data-stu-id="969e0-132">**publication**</span></span>          | [<span data-ttu-id="969e0-133">PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="969e0-133">PublicationFacet</span></span>](../resources/publicationfacet.md) | <span data-ttu-id="969e0-134">Indica el estado de publicación de esta versión concreta.</span><span class="sxs-lookup"><span data-stu-id="969e0-134">Indicates the publication status of this particular version.</span></span> <span data-ttu-id="969e0-135">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="969e0-135">Read-only.</span></span> |
| <span data-ttu-id="969e0-136">**size**</span><span class="sxs-lookup"><span data-stu-id="969e0-136">**size**</span></span>                 | <span data-ttu-id="969e0-137">Int64</span><span class="sxs-lookup"><span data-stu-id="969e0-137">Int64</span></span>                                                | <span data-ttu-id="969e0-138">Indica el tamaño de la secuencia de contenido para esta versión del elemento.</span><span class="sxs-lookup"><span data-stu-id="969e0-138">Indicates the size of the content stream for this version of the item.</span></span>  |

## <a name="relationships"></a><span data-ttu-id="969e0-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="969e0-139">Relationships</span></span>

<span data-ttu-id="969e0-140">En la tabla siguiente, se definen las relaciones que tiene el recurso **driveItemVersion** con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="969e0-140">The following table defines the relationships that the **driveItemVersion** resource has to other resources.</span></span>

| <span data-ttu-id="969e0-141">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="969e0-141">Relationship name</span></span> |  <span data-ttu-id="969e0-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="969e0-142">Type</span></span>  |            <span data-ttu-id="969e0-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="969e0-143">Description</span></span>             |
| :---------------- | :----- | :--------------------------------- |
| <span data-ttu-id="969e0-144">**content**</span><span class="sxs-lookup"><span data-stu-id="969e0-144">**content**</span></span>       | <span data-ttu-id="969e0-145">Secuencia</span><span class="sxs-lookup"><span data-stu-id="969e0-145">Stream</span></span> | <span data-ttu-id="969e0-146">La secuencia de contenido de la versión.</span><span class="sxs-lookup"><span data-stu-id="969e0-146">The content stream of the version.</span></span> |

<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
