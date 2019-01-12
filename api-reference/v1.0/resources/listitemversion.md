---
title: Tipo de recurso ListItemVersion
description: El recurso **listItemVersion** representa una versión anterior de un recurso ListItem.
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 6e21be59b71a8f348931603c799ebbbe225e5d3f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951848"
---
# <a name="listitemversion-resource-type"></a><span data-ttu-id="b7236-103">Tipo de recurso ListItemVersion</span><span class="sxs-lookup"><span data-stu-id="b7236-103">ListItemVersion resource type</span></span>

<span data-ttu-id="b7236-104">El recurso **listItemVersion** representa una versión anterior de un recurso [ListItem](listitem.md).</span><span class="sxs-lookup"><span data-stu-id="b7236-104">The **listItemVersion** resource represents a previous version of a [ListItem](listitem.md) resource.</span></span>

## <a name="tasks-on-listitemversion-resources"></a><span data-ttu-id="b7236-105">Tareas en recursos ListItemVersion</span><span class="sxs-lookup"><span data-stu-id="b7236-105">Tasks on ListItemVersion resources</span></span>

<span data-ttu-id="b7236-106">Las tareas siguientes están disponibles para los recursos listItemVersion.</span><span class="sxs-lookup"><span data-stu-id="b7236-106">The following tasks are available for listItemVersion resources.</span></span>

|            <span data-ttu-id="b7236-107">Tarea común</span><span class="sxs-lookup"><span data-stu-id="b7236-107">Common task</span></span>             |         <span data-ttu-id="b7236-108">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="b7236-108">HTTP method</span></span>         |
| :--------------------------------- | :-------------------------- |
| <span data-ttu-id="b7236-109">[Enumerar versiones][version-list]</span><span class="sxs-lookup"><span data-stu-id="b7236-109">[List versions][version-list]</span></span>      | `GET /sites/{site-id}/items/{item-id}/versions`  |
| <span data-ttu-id="b7236-110">[Obtener versión][version-get]</span><span class="sxs-lookup"><span data-stu-id="b7236-110">[Get version][version-get]</span></span>         | `GET /sites/{site-id}/items/{item-id}/versions/{version-id}`     |
| <span data-ttu-id="b7236-111">[Restaurar versión][version-restore]</span><span class="sxs-lookup"><span data-stu-id="b7236-111">[Restore version][version-restore]</span></span> | `POST /sites/{site-id}/items/{item-id}/versions/{version-id}/restore` |

[version-list]: ../api/listitem-list-versions.md
[version-get]: ../api/listitemversion-get.md
[version-restore]: ../api/listitemversion-restore.md


## <a name="json-representation"></a><span data-ttu-id="b7236-112">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b7236-112">JSON representation</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.baseItemVersion",
  "@odata.type": "microsoft.graph.listItemVersion",
  "@type.aka": "oneDrive.baseItemVersion"
}-->

```json
{
  "fields": { "@odata.type": "microsoft.graph.fieldValueSet" },
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "published": { "@odata.type": "microsoft.graph.publicationFacet" }
}
```

## <a name="properties"></a><span data-ttu-id="b7236-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b7236-113">Properties</span></span>

|      <span data-ttu-id="b7236-114">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="b7236-114">Property name</span></span>       |                         <span data-ttu-id="b7236-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="b7236-115">Type</span></span>                         |                               <span data-ttu-id="b7236-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7236-116">Description</span></span>                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| <span data-ttu-id="b7236-117">**id**</span><span class="sxs-lookup"><span data-stu-id="b7236-117">**id**</span></span>                   | <span data-ttu-id="b7236-118">string</span><span class="sxs-lookup"><span data-stu-id="b7236-118">string</span></span>                                               | <span data-ttu-id="b7236-119">El identificador de la versión.</span><span class="sxs-lookup"><span data-stu-id="b7236-119">The ID of the version.</span></span> <span data-ttu-id="b7236-120">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b7236-120">Read-only.</span></span>                                       |
| <span data-ttu-id="b7236-121">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="b7236-121">**lastModifiedBy**</span></span>       | [<span data-ttu-id="b7236-122">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="b7236-122">IdentitySet</span></span>](../resources/identityset.md)           | <span data-ttu-id="b7236-123">Identidad del usuario que modificó por última vez la versión.</span><span class="sxs-lookup"><span data-stu-id="b7236-123">Identity of the user which last modified the version.</span></span> <span data-ttu-id="b7236-124">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b7236-124">Read-only.</span></span>        |
| <span data-ttu-id="b7236-125">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="b7236-125">**lastModifiedDateTime**</span></span> | [<span data-ttu-id="b7236-126">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b7236-126">DateTimeOffset</span></span>](../resources/timestamp.md)          | <span data-ttu-id="b7236-127">Fecha y hora de la última modificación de la versión.</span><span class="sxs-lookup"><span data-stu-id="b7236-127">Date and time the version was last modified.</span></span> <span data-ttu-id="b7236-128">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b7236-128">Read-only.</span></span>                 |
| <span data-ttu-id="b7236-129">**published**</span><span class="sxs-lookup"><span data-stu-id="b7236-129">**published**</span></span>            | [<span data-ttu-id="b7236-130">PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="b7236-130">PublicationFacet</span></span>](../resources/publicationfacet.md) | <span data-ttu-id="b7236-131">Indica el estado de publicación de esta versión concreta.</span><span class="sxs-lookup"><span data-stu-id="b7236-131">Indicates the publication status of this particular version.</span></span> <span data-ttu-id="b7236-132">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b7236-132">Read-only.</span></span> |


## <a name="relationships"></a><span data-ttu-id="b7236-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b7236-133">Relationships</span></span>

<span data-ttu-id="b7236-134">En la tabla siguiente, se definen las relaciones que tiene el recurso **driveItemVersion** con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="b7236-134">The following table defines the relationships that the **driveItemVersion** resource has to other resources.</span></span>

| <span data-ttu-id="b7236-135">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="b7236-135">Relationship name</span></span> |                      <span data-ttu-id="b7236-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="b7236-136">Type</span></span>                      |                               <span data-ttu-id="b7236-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7236-137">Description</span></span>                                |
| :---------------- | :--------------------------------------------- | :----------------------------------------------------------------------- |
| <span data-ttu-id="b7236-138">**fields**</span><span class="sxs-lookup"><span data-stu-id="b7236-138">**fields**</span></span>        | [<span data-ttu-id="b7236-139">FieldValueSet</span><span class="sxs-lookup"><span data-stu-id="b7236-139">FieldValueSet</span></span>](../resources/fieldvalueset.md) | <span data-ttu-id="b7236-140">Una colección de los campos y valores para esta versión del elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="b7236-140">A collection of the fields and values for this version of the list item.</span></span> |


<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
