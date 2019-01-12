---
title: Trabajar con sitios de SharePoint en Microsoft Graph
description: 'La API de SharePoint en Microsoft Graph admite los siguientes escenarios principales:'
localization_priority: Priority
ms.prod: sharepoint
ms.openlocfilehash: de3c4b91f0e53a9a4efaf135fc91364b1802b2ec
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946914"
---
# <a name="working-with-sharepoint-sites-in-microsoft-graph"></a><span data-ttu-id="1e78d-103">Trabajar con sitios de SharePoint en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="1e78d-103">Working with SharePoint sites in Microsoft Graph</span></span>

<span data-ttu-id="1e78d-104">La API de SharePoint en Microsoft Graph admite los siguientes escenarios principales:</span><span class="sxs-lookup"><span data-stu-id="1e78d-104">The SharePoint API in Microsoft Graph supports the following core scenarios:</span></span>

* <span data-ttu-id="1e78d-105">Acceso a los **sitios**, las **listas** y las **unidades** (bibliotecas de documentos) de SharePoint</span><span class="sxs-lookup"><span data-stu-id="1e78d-105">Access to SharePoint **sites**, **lists**, and **drives** (document libraries)</span></span>
* <span data-ttu-id="1e78d-106">Soporte de solo lectura de los recursos del **sitio** (sin capacidad para crear nuevos sitios)</span><span class="sxs-lookup"><span data-stu-id="1e78d-106">Read-only support for **site** resources (no ability to create new sites)</span></span>
* <span data-ttu-id="1e78d-107">Compatibilidad de lectura y escritura para recursos **list**, **listItem** y **driveItem**</span><span class="sxs-lookup"><span data-stu-id="1e78d-107">Read-write support for **lists**, **listItems**, and **driveItems**</span></span>
* <span data-ttu-id="1e78d-108">Recursos de dirección por la ruta de acceso relativa, URL o id. de SharePoint</span><span class="sxs-lookup"><span data-stu-id="1e78d-108">Address resources by SharePoint ID, URL, or relative path</span></span>

<span data-ttu-id="1e78d-109">La API de SharePoint expone tres tipos principales de recursos:</span><span class="sxs-lookup"><span data-stu-id="1e78d-109">The SharePoint API exposes three major resource types:</span></span>

* <span data-ttu-id="1e78d-110">[Site](site.md) _(objeto de nivel superior)_</span><span class="sxs-lookup"><span data-stu-id="1e78d-110">[Site](site.md) _(top-level object)_</span></span>
* [<span data-ttu-id="1e78d-111">Lista</span><span class="sxs-lookup"><span data-stu-id="1e78d-111">List</span></span>](list.md)
* [<span data-ttu-id="1e78d-112">ListItem</span><span class="sxs-lookup"><span data-stu-id="1e78d-112">ListItem</span></span>](listitem.md)

<span data-ttu-id="1e78d-113">A continuación se muestra un ejemplo de un recurso listItem.</span><span class="sxs-lookup"><span data-stu-id="1e78d-113">The following is an example of a listItem resource.</span></span>

```json
{
  "fields": {
    "Title": "Access card",
    "Employee": "Ryan Gregg",
    "EmployeeId": "10",
    "CardSerial": "01235492",
    "Alias": "RGregg",
    "ID": 1,
    "ContentType": "Item",
    "Modified": "2016-09-19T23:15:25-07:00",
    "Created": "2016-09-19T23:15:25-07:00"
  },
  "createdBy": {
    "user": {
      "id": "b757fdcb-0271-4807-b243-504139e4ba04",
      "displayName": "Ryan Gregg"
    }
  },
  "createdDateTime": "2016-09-20T06:15:25Z",
  "eTag": "48e941c3-9515-4c48-9760-c07c90c79d48,1",
  "id": "4",
  "lastModifiedBy": {
    "user": {
      "id": "b757fdcb-0271-4807-b243-504139e4ba04",
      "displayName": "Ryan Gregg"
    }
  },
  "lastModifiedDateTime": "2016-09-20T06:15:25Z",
}
```

<span data-ttu-id="1e78d-114">Los recursos exponen los datos de tres maneras diferentes:</span><span class="sxs-lookup"><span data-stu-id="1e78d-114">Resources expose data in three different ways:</span></span>

* <span data-ttu-id="1e78d-115">_Propiedades_ (como **id** y **name**) exponen valores simples.</span><span class="sxs-lookup"><span data-stu-id="1e78d-115">_Properties_ (like **id** and **name**) expose simple values.</span></span>
* <span data-ttu-id="1e78d-116">_Facetas_ (como **fields** y **createdBy**) exponen valores complejos.</span><span class="sxs-lookup"><span data-stu-id="1e78d-116">_Facets_ (like **fields** and **createdBy**) expose complex values.</span></span>
* <span data-ttu-id="1e78d-117">_Referencias_ (como **items**) indican colecciones de otros recursos.</span><span class="sxs-lookup"><span data-stu-id="1e78d-117">_References_ (like **items**) point to collections of other resources.</span></span>

<span data-ttu-id="1e78d-118">Puede ampliar las referencias en la dirección URL con el parámetro de consulta _expand_, por ejemplo, `?expand=fields`.</span><span class="sxs-lookup"><span data-stu-id="1e78d-118">You can expand references in your URL with the _expand_ query parameter; for example, `?expand=fields`.</span></span>
<span data-ttu-id="1e78d-119">Puede solicitar propiedades y facetas específicas con el parámetro de consulta _select_, por ejemplo, `?select=id,name`.</span><span class="sxs-lookup"><span data-stu-id="1e78d-119">You can request specific properties and facets with the _select_ query parameter; for example, `?select=id,name`.</span></span>
<span data-ttu-id="1e78d-120">De manera predeterminada, la mayoría de las propiedades y las facetas se devuelve mientras que todas las referencias se ocultan.</span><span class="sxs-lookup"><span data-stu-id="1e78d-120">By default, most properties and facets are returned while all references are hidden.</span></span>
<span data-ttu-id="1e78d-121">Por motivos de eficacia, recomendamos que especifique _select_ y _expand_ para que solo devuelvan los datos que le interesen.</span><span class="sxs-lookup"><span data-stu-id="1e78d-121">For efficiency, we recommend that you specify _select_ and _expand_ to only return the data you care about.</span></span>

## <a name="sharepoint-api-root-resources"></a><span data-ttu-id="1e78d-122">Recursos raíz de las API de SharePoint</span><span class="sxs-lookup"><span data-stu-id="1e78d-122">SharePoint API root resources</span></span>

<span data-ttu-id="1e78d-123">Los ejemplos siguientes son relativos al `https://graph.microsoft.com/v1.0`.</span><span class="sxs-lookup"><span data-stu-id="1e78d-123">The following examples are relative to `https://graph.microsoft.com/v1.0`.</span></span>

| <span data-ttu-id="1e78d-124">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="1e78d-124">Path</span></span>                                   | <span data-ttu-id="1e78d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e78d-125">Description</span></span>
|:---------------------------------------|:------------------------------------
| <span data-ttu-id="1e78d-126">/sites/root</span><span class="sxs-lookup"><span data-stu-id="1e78d-126">/sites/root</span></span>                            | <span data-ttu-id="1e78d-127">[Sitio][] predeterminado de la organización.</span><span class="sxs-lookup"><span data-stu-id="1e78d-127">Organization's default [site][].</span></span>
| <span data-ttu-id="1e78d-128">/sites/{site-id}</span><span class="sxs-lookup"><span data-stu-id="1e78d-128">/sites/{site-id}</span></span>                       | <span data-ttu-id="1e78d-129">Acceso a un [sitio][] específico por su id.</span><span class="sxs-lookup"><span data-stu-id="1e78d-129">Access a specific [site][] by its ID.</span></span>
| <span data-ttu-id="1e78d-130">/sites/{site-id}/drive</span><span class="sxs-lookup"><span data-stu-id="1e78d-130">/sites/{site-id}/drive</span></span>                 | <span data-ttu-id="1e78d-131">Acceso a la [unidad](drive.md) predeterminada (biblioteca de documentos) para este [sitio][].</span><span class="sxs-lookup"><span data-stu-id="1e78d-131">Access the default [drive](drive.md) (document library) for the given [site][].</span></span>
| <span data-ttu-id="1e78d-132">/sites/{site-id}/drives</span><span class="sxs-lookup"><span data-stu-id="1e78d-132">/sites/{site-id}/drives</span></span>                | <span data-ttu-id="1e78d-133">Enumerar las [unidades](drive.md) (bibliotecas de documentos) en el [sitio][].</span><span class="sxs-lookup"><span data-stu-id="1e78d-133">Enumerate the [drives](drive.md) (document libraries) under the [site][].</span></span>
| <span data-ttu-id="1e78d-134">/sites/{site-id}/sites</span><span class="sxs-lookup"><span data-stu-id="1e78d-134">/sites/{site-id}/sites</span></span>                 | <span data-ttu-id="1e78d-135">Enumerar los sitios secundarios en [sitio][].</span><span class="sxs-lookup"><span data-stu-id="1e78d-135">Enumerate the sub-sites under the [site][].</span></span>
| <span data-ttu-id="1e78d-136">/sites/{site-id}/lists</span><span class="sxs-lookup"><span data-stu-id="1e78d-136">/sites/{site-id}/lists</span></span>                 | <span data-ttu-id="1e78d-137">Enumerar las [listas](list.md) en el [sitio](site.md).</span><span class="sxs-lookup"><span data-stu-id="1e78d-137">Enumerate the [lists](list.md) under the [site](site.md).</span></span>
| <span data-ttu-id="1e78d-138">/sites/{site-id}/lists/{list-id}/items</span><span class="sxs-lookup"><span data-stu-id="1e78d-138">/sites/{site-id}/lists/{list-id}/items</span></span> | <span data-ttu-id="1e78d-139">Enumerar los [listItems](listitem.md) en la [lista](list.md).</span><span class="sxs-lookup"><span data-stu-id="1e78d-139">Enumerate the [listItems](listitem.md) under the [list](list.md).</span></span>
| <span data-ttu-id="1e78d-140">/groups/{group-id}/sites/root</span><span class="sxs-lookup"><span data-stu-id="1e78d-140">/groups/{group-id}/sites/root</span></span>          | <span data-ttu-id="1e78d-141">Acceso a un [sitio][] de equipo de grupo.</span><span class="sxs-lookup"><span data-stu-id="1e78d-141">Access a group's team [site][].</span></span>

<span data-ttu-id="1e78d-p102">Los sitios también pueden dirigirse a través de la ruta al utilizar el nombre de host de SharePoint, seguido de dos puntos y la ruta de acceso relativa al sitio. Opcionalmente, puede hacer la transición de vuelta mientras dirige el modelo de recursos al colocar otro signo de dos puntos al final.</span><span class="sxs-lookup"><span data-stu-id="1e78d-p102">Sites can also be addressed by path by using the SharePoint hostname, followed by a colon and the relative path to the site. You can optionally transition back to addressing the resource model by putting another colon at the end.</span></span>

| <span data-ttu-id="1e78d-144">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="1e78d-144">Path</span></span>                                           | <span data-ttu-id="1e78d-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e78d-145">Description</span></span>
|:-----------------------------------------------|:-----------------------------------
| <span data-ttu-id="1e78d-146">/sites/contoso.sharepoint.com:/teams/hr</span><span class="sxs-lookup"><span data-stu-id="1e78d-146">/sites/contoso.sharepoint.com:/teams/hr</span></span>        | <span data-ttu-id="1e78d-147">El sitio asociadohttps://contoso.sharepoint.com/teams/hr</span><span class="sxs-lookup"><span data-stu-id="1e78d-147">The site associated with https://contoso.sharepoint.com/teams/hr</span></span>
| <span data-ttu-id="1e78d-148">/sites/contoso.sharepoint.com:/teams/hr:/drive</span><span class="sxs-lookup"><span data-stu-id="1e78d-148">/sites/contoso.sharepoint.com:/teams/hr:/drive</span></span> | <span data-ttu-id="1e78d-149">Acceso a la [unidad](drive.md) predeterminada para este sitio.</span><span class="sxs-lookup"><span data-stu-id="1e78d-149">Access the default [drive](drive.md) for this site.</span></span>

## <a name="note-for-existing-sharepoint-developers"></a><span data-ttu-id="1e78d-150">Nota para los desarrolladores de SharePoint existentes</span><span class="sxs-lookup"><span data-stu-id="1e78d-150">Note for existing SharePoint developers</span></span>

<span data-ttu-id="1e78d-p103">La API de SharePoint de Microsoft Graph tiene algunas diferencias clave con las API de CSOM. El recurso del [sitio][] se asigna a `SPWeb`. El [sitio][] raíz (`SPWeb`) en un sitio de la colección tiene una faceta de [colecciónDeSitios](sitecollection.md), que contiene información acerca de `SPSite`. Debido a que los identificadores para los sitios solo son únicos dentro de su colección de sitios, el direccionamiento a un sitio a través del id. requiere proporcionar el identificador de la colección de sitios y el identificador del sitio.</span><span class="sxs-lookup"><span data-stu-id="1e78d-p103">The Microsoft Graph SharePoint API has a few key differences with the CSOM APIs. The [site][] resource maps to `SPWeb`. The root [site][] (`SPWeb`) in a site collection has a [siteCollection](sitecollection.md) facet, which contains information about the `SPSite`. Because IDs for sites are only unique within their site collection, addressing a site by ID requires providing both the site collection identifier and the site identifier.</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{hostname},{spsite-id},{spweb-id}/
```
<span data-ttu-id="1e78d-155">Una dirección URL creada solo con el nombre de host apuntará al sitio raíz (`SPWeb`) en la colección de sitios predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1e78d-155">A URL constructed with only the hostname will point to the root site (`SPWeb`) in the default site collection.</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{hostname}
```

<span data-ttu-id="1e78d-156">Una dirección URL creada solo con el nombre de host y el id. de siteCollection (`SPSite`) apuntará al sitio raíz (`SPWeb`) en la colección de sitios predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1e78d-156">A URL constructed with only the hostname and siteCollection (`SPSite`) ID will point to the root site (`SPWeb`) in the given site collection.</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{hostname},{spsite-id}
```

[site]: site.md
[list]: list.md
[drive]: drive.md
[siteCollection]: sitecollection.md

<!-- {
  "type": "#page.annotation",
  "description": "Getting started programming with the SharePoint API",
  "keywords": "getting started sharepoint rest api programming C# ios android rest http",
  "section": "documentation",
  "tocPath": "Getting Started",
  "tocIndex": -100
} -->
