---
title: Tipo de recurso ListItemVersion
description: El recurso **listItemVersion** representa una versión anterior de un recurso ListItem.
ms.openlocfilehash: f036ea217abe766806e7f3c6b24bee4394f54889
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028700"
---
# <a name="listitemversion-resource-type"></a><span data-ttu-id="a9928-103">Tipo de recurso ListItemVersion</span><span class="sxs-lookup"><span data-stu-id="a9928-103">ListItemVersion resource type</span></span>

<span data-ttu-id="a9928-104">El recurso **listItemVersion** representa una versión anterior de un recurso [ListItem](listitem.md).</span><span class="sxs-lookup"><span data-stu-id="a9928-104">The **listItemVersion** resource represents a previous version of a [ListItem](listitem.md) resource.</span></span>

## <a name="tasks-on-listitemversion-resources"></a><span data-ttu-id="a9928-105">Tareas en recursos ListItemVersion</span><span class="sxs-lookup"><span data-stu-id="a9928-105">Tasks on ListItemVersion resources</span></span>

<span data-ttu-id="a9928-106">Las tareas siguientes están disponibles para los recursos listItemVersion.</span><span class="sxs-lookup"><span data-stu-id="a9928-106">The following tasks are available for listItemVersion resources.</span></span>

|            <span data-ttu-id="a9928-107">Tarea común</span><span class="sxs-lookup"><span data-stu-id="a9928-107">Common task</span></span>             |         <span data-ttu-id="a9928-108">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="a9928-108">HTTP method</span></span>         |
| :--------------------------------- | :-------------------------- |
| <span data-ttu-id="a9928-109">[Enumerar versiones][version-list]</span><span class="sxs-lookup"><span data-stu-id="a9928-109">[List versions][version-list]</span></span>      | `GET /sites/{site-id}/items/{item-id}/versions`  |
| <span data-ttu-id="a9928-110">[Obtener versión][version-get]</span><span class="sxs-lookup"><span data-stu-id="a9928-110">[Get version][version-get]</span></span>         | `GET /sites/{site-id}/items/{item-id}/versions/{version-id}`     |
| <span data-ttu-id="a9928-111">[Restaurar versión][version-restore]</span><span class="sxs-lookup"><span data-stu-id="a9928-111">[Restore version][version-restore]</span></span> | `POST /sites/{site-id}/items/{item-id}/versions/{version-id}/restore` |

[version-list]: ../api/listitem-list-versions.md
[version-get]: ../api/listitemversion-get.md
[version-restore]: ../api/listitemversion-restore.md


## <a name="json-representation"></a><span data-ttu-id="a9928-112">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a9928-112">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="a9928-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9928-113">Properties</span></span>

|      <span data-ttu-id="a9928-114">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="a9928-114">Property name</span></span>       |                         <span data-ttu-id="a9928-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9928-115">Type</span></span>                         |                               <span data-ttu-id="a9928-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9928-116">Description</span></span>                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| <span data-ttu-id="a9928-117">**id**</span><span class="sxs-lookup"><span data-stu-id="a9928-117">**id**</span></span>                   | <span data-ttu-id="a9928-118">string</span><span class="sxs-lookup"><span data-stu-id="a9928-118">string</span></span>                                               | <span data-ttu-id="a9928-119">El identificador de la versión.</span><span class="sxs-lookup"><span data-stu-id="a9928-119">The ID of the version.</span></span> <span data-ttu-id="a9928-120">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a9928-120">Read-only.</span></span>                                       |
| <span data-ttu-id="a9928-121">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="a9928-121">**lastModifiedBy**</span></span>       | [<span data-ttu-id="a9928-122">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="a9928-122">IdentitySet</span></span>](../resources/identityset.md)           | <span data-ttu-id="a9928-123">Identidad del usuario que modificó por última vez la versión.</span><span class="sxs-lookup"><span data-stu-id="a9928-123">Identity of the user which last modified the version.</span></span> <span data-ttu-id="a9928-124">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a9928-124">Read-only.</span></span>        |
| <span data-ttu-id="a9928-125">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="a9928-125">**lastModifiedDateTime**</span></span> | [<span data-ttu-id="a9928-126">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a9928-126">DateTimeOffset</span></span>](../resources/timestamp.md)          | <span data-ttu-id="a9928-127">Fecha y hora de la última modificación de la versión.</span><span class="sxs-lookup"><span data-stu-id="a9928-127">Date and time the version was last modified.</span></span> <span data-ttu-id="a9928-128">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a9928-128">Read-only.</span></span>                 |
| <span data-ttu-id="a9928-129">**published**</span><span class="sxs-lookup"><span data-stu-id="a9928-129">**published**</span></span>            | [<span data-ttu-id="a9928-130">PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="a9928-130">PublicationFacet</span></span>](../resources/publicationfacet.md) | <span data-ttu-id="a9928-131">Indica el estado de publicación de esta versión concreta.</span><span class="sxs-lookup"><span data-stu-id="a9928-131">Indicates the publication status of this particular version.</span></span> <span data-ttu-id="a9928-132">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a9928-132">Read-only.</span></span> |


## <a name="relationships"></a><span data-ttu-id="a9928-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a9928-133">Relationships</span></span>

<span data-ttu-id="a9928-134">En la tabla siguiente, se definen las relaciones que tiene el recurso **driveItemVersion** con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="a9928-134">The following table defines the relationships that the **driveItemVersion** resource has to other resources.</span></span>

| <span data-ttu-id="a9928-135">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="a9928-135">Relationship name</span></span> |                      <span data-ttu-id="a9928-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9928-136">Type</span></span>                      |                               <span data-ttu-id="a9928-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9928-137">Description</span></span>                                |
| :---------------- | :--------------------------------------------- | :----------------------------------------------------------------------- |
| <span data-ttu-id="a9928-138">**fields**</span><span class="sxs-lookup"><span data-stu-id="a9928-138">**fields**</span></span>        | [<span data-ttu-id="a9928-139">FieldValueSet</span><span class="sxs-lookup"><span data-stu-id="a9928-139">FieldValueSet</span></span>](../resources/fieldvalueset.md) | <span data-ttu-id="a9928-140">Una colección de los campos y valores para esta versión del elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="a9928-140">A collection of the fields and values for this version of the list item.</span></span> |


<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
