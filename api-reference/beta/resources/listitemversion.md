---
author: rgregg
ms.author: rgregg
ms.date: 09/17/2017
title: ListItemVersion
ms.openlocfilehash: 7cda16159c6e5e58a0f60aef3c60198c7615f9e0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083228"
---
# <a name="listitemversion-resource-type"></a><span data-ttu-id="2986b-102">Tipo de recurso ListItemVersion</span><span class="sxs-lookup"><span data-stu-id="2986b-102">ListItemVersion resource type</span></span>

> <span data-ttu-id="2986b-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2986b-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2986b-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2986b-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2986b-105">El recurso **listItemVersion** representa una versión anterior de un recurso [ListItem](listitem.md).</span><span class="sxs-lookup"><span data-stu-id="2986b-105">The **listItemVersion** resource represents a previous version of a [ListItem](listitem.md) resource.</span></span>

## <a name="tasks-on-listitemversion-resources"></a><span data-ttu-id="2986b-106">Tareas en recursos ListItemVersion</span><span class="sxs-lookup"><span data-stu-id="2986b-106">Tasks on ListItemVersion resources</span></span>

<span data-ttu-id="2986b-107">Las tareas siguientes están disponibles para los recursos listItemVersion.</span><span class="sxs-lookup"><span data-stu-id="2986b-107">The following tasks are available for listItemVersion resources.</span></span>

|            <span data-ttu-id="2986b-108">Tarea común</span><span class="sxs-lookup"><span data-stu-id="2986b-108">Common task</span></span>             |         <span data-ttu-id="2986b-109">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="2986b-109">HTTP method</span></span>         |
| :--------------------------------- | :-------------------------- |
| <span data-ttu-id="2986b-110">[Enumerar versiones][version-list]</span><span class="sxs-lookup"><span data-stu-id="2986b-110">[List versions][version-list]</span></span>      | `GET /sites/{site-id}/items/{item-id}/versions`  |
| <span data-ttu-id="2986b-111">[Obtener versión][version-get]</span><span class="sxs-lookup"><span data-stu-id="2986b-111">[Get version][version-get]</span></span>         | `GET /sites/{site-id}/items/versions/{version-id}`     |
| <span data-ttu-id="2986b-112">[Restaurar versión][version-restore]</span><span class="sxs-lookup"><span data-stu-id="2986b-112">[Restore version][version-restore]</span></span> | `POST /sites/{site-id}/items/versions/{version-id}/restore` |

[version-list]: ../api/listitem-list-versions.md
[version-get]: ../api/listitemversion-get.md
[version-restore]: ../api/listitemversion-restore.md


## <a name="json-representation"></a><span data-ttu-id="2986b-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2986b-113">JSON representation</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.listItemVersion", "@type.aka": "oneDrive.baseItemVersion" } -->

```json
{
  "content": { "@odata.type": "Edm.Stream" },
  "fields": { "@odata.type": "microsoft.graph.fieldValueSet" },
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "published": { "@odata.type": "microsoft.graph.publicationFacet" }
}
```

## <a name="properties"></a><span data-ttu-id="2986b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2986b-114">Properties</span></span>

|      <span data-ttu-id="2986b-115">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="2986b-115">Property name</span></span>       |                         <span data-ttu-id="2986b-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="2986b-116">Type</span></span>                         |                               <span data-ttu-id="2986b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2986b-117">Description</span></span>                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| <span data-ttu-id="2986b-118">**id**</span><span class="sxs-lookup"><span data-stu-id="2986b-118">**id**</span></span>                   | <span data-ttu-id="2986b-119">string</span><span class="sxs-lookup"><span data-stu-id="2986b-119">string</span></span>                                               | <span data-ttu-id="2986b-120">El identificador de la versión.</span><span class="sxs-lookup"><span data-stu-id="2986b-120">The ID of the version.</span></span> <span data-ttu-id="2986b-121">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2986b-121">Read-only.</span></span>                                       |
| <span data-ttu-id="2986b-122">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="2986b-122">**lastModifiedBy**</span></span>       | [<span data-ttu-id="2986b-123">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="2986b-123">IdentitySet</span></span>](../resources/identityset.md)           | <span data-ttu-id="2986b-124">Identidad del usuario que modificó por última vez la versión.</span><span class="sxs-lookup"><span data-stu-id="2986b-124">Identity of the user which last modified the version.</span></span> <span data-ttu-id="2986b-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2986b-125">Read-only.</span></span>        |
| <span data-ttu-id="2986b-126">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="2986b-126">**lastModifiedDateTime**</span></span> | [<span data-ttu-id="2986b-127">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2986b-127">DateTimeOffset</span></span>](../resources/timestamp.md)          | <span data-ttu-id="2986b-128">Fecha y hora de la última modificación de la versión.</span><span class="sxs-lookup"><span data-stu-id="2986b-128">Date and time the version was last modified.</span></span> <span data-ttu-id="2986b-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2986b-129">Read-only.</span></span>                 |
| <span data-ttu-id="2986b-130">**published**</span><span class="sxs-lookup"><span data-stu-id="2986b-130">**published**</span></span>            | [<span data-ttu-id="2986b-131">PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="2986b-131">PublicationFacet</span></span>](../resources/publicationfacet.md) | <span data-ttu-id="2986b-132">Indica el estado de publicación de esta versión concreta.</span><span class="sxs-lookup"><span data-stu-id="2986b-132">Indicates the publication status of this particular version.</span></span> <span data-ttu-id="2986b-133">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2986b-133">Read-only.</span></span> |


## <a name="relationships"></a><span data-ttu-id="2986b-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2986b-134">Relationships</span></span>

<span data-ttu-id="2986b-135">En la tabla siguiente, se definen las relaciones que tiene el recurso **driveItemVersion** con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="2986b-135">The following table defines the relationships that the **driveItemVersion** resource has to other resources.</span></span>

| <span data-ttu-id="2986b-136">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="2986b-136">Relationship name</span></span> |                      <span data-ttu-id="2986b-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="2986b-137">Type</span></span>                      |                               <span data-ttu-id="2986b-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="2986b-138">Description</span></span>                                |
| :---------------- | :--------------------------------------------- | :----------------------------------------------------------------------- |
| <span data-ttu-id="2986b-139">**fields**</span><span class="sxs-lookup"><span data-stu-id="2986b-139">**fields**</span></span>        | [<span data-ttu-id="2986b-140">FieldValueSet</span><span class="sxs-lookup"><span data-stu-id="2986b-140">FieldValueSet</span></span>](../resources/fieldvalueset.md) | <span data-ttu-id="2986b-141">Una colección de los campos y valores para esta versión del elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="2986b-141">A collection of the fields and values for this version of the list item.</span></span> |


<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->