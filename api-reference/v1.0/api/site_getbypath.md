---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener un sitio de SharePoint mediante la ruta de acceso
ms.openlocfilehash: 789d4b3f24818a8bc5a06d0c6c14c0002f58f142
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="get-a-site-resource-by-path"></a><span data-ttu-id="128bd-102">Obtener un recurso de sitio mediante la ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="128bd-102">Get a site resource by path</span></span>

<span data-ttu-id="128bd-p101">Recupera las propiedades y relaciones de un recurso [site][]. Un recurso **site** representa un sitio de grupo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="128bd-p101">Retrieve properties and relationships for a [site][] resource. A **site** resource represents a team site in SharePoint.</span></span>

[site]: ../resources/site.md

<span data-ttu-id="128bd-106">Además de recuperar un [sitio mediante id.](site_get.md), puede recuperar un sitio basándose en la ruta de URL relativa del servidor.</span><span class="sxs-lookup"><span data-stu-id="128bd-106">In addition to retrieving a [site by ID](site_get.md) you can retrieve a site based on server-relative URL path.</span></span>

* <span data-ttu-id="128bd-107">Nombre de host de la colección de sitios (contoso.sharepoint.com)</span><span class="sxs-lookup"><span data-stu-id="128bd-107">Site collection hostname (contoso.sharepoint.com)</span></span>
* <span data-ttu-id="128bd-108">Ruta de sitio, relativa al nombre de host del servidor.</span><span class="sxs-lookup"><span data-stu-id="128bd-108">Site path, relative to server hostname.</span></span>

<span data-ttu-id="128bd-109">También hay un identificador de sitio reservado, `root`, que siempre hace referencia al sitio raíz para un destino especificado de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="128bd-109">There is also a reserved site identifier, `root`, which always references the root site for a given target, as follows:</span></span>

* <span data-ttu-id="128bd-110">`/sites/root`: El sitio raíz del inquilino.</span><span class="sxs-lookup"><span data-stu-id="128bd-110">`/sites/root`: The tenant root site.</span></span>
* <span data-ttu-id="128bd-111">`/groups/{group-id}/sites/root`: Sitio del grupo.</span><span class="sxs-lookup"><span data-stu-id="128bd-111">`/groups/{group-id}/sites/root`: The group's team site.</span></span>

## <a name="permissions"></a><span data-ttu-id="128bd-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="128bd-112">Permissions</span></span>

<span data-ttu-id="128bd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="128bd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="128bd-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="128bd-115">Permission type</span></span>      | <span data-ttu-id="128bd-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="128bd-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="128bd-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="128bd-117">Delegated (work or school account)</span></span> | <span data-ttu-id="128bd-118">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="128bd-118">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="128bd-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="128bd-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="128bd-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="128bd-120">Not supported.</span></span>    |
|<span data-ttu-id="128bd-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="128bd-121">Application</span></span> | <span data-ttu-id="128bd-122">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="128bd-122">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="128bd-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="128bd-123">HTTP Request</span></span>

<span data-ttu-id="128bd-124">Para obtener acceso al sitio de SharePoint de raíz con una ruta relativa:</span><span class="sxs-lookup"><span data-stu-id="128bd-124">To access the root SharePoint site with a relative path:</span></span>

<!-- { "blockType": "request", "name": "get-site-by-hostname-and-path", "scopes": "service.sharepoint sites.read.all" } -->

```http
GET /sites/{hostname}:/{relative-path}
```

## <a name="http-response"></a><span data-ttu-id="128bd-125">Respuesta HTTP</span><span class="sxs-lookup"><span data-stu-id="128bd-125">HTTP Response</span></span>

<span data-ttu-id="128bd-126">Este método devuelve un recurso [site][] para el sitio al que se hace referencia mediante el identificador único.</span><span class="sxs-lookup"><span data-stu-id="128bd-126">This method returns a [site][] resource for the site referenced by the unique identifier.</span></span>

<!-- { "blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.site" } -->

```http
HTTP/1.1 200 OK

{
  "id": "contoso.sharepoint.com,2C712604-1370-44E7-A1F5-426573FDA80A,2D2244C3-251A-49EA-93A8-39E1C3A060FE",
  "owner": {
    "user": { 
      "displayName": "Daron Spektor",
      "id": "5280E7FE-DC7A-4486-9490-E790D81DFEB3"
    }
  },
  "displayName": "OneDrive Team Site",
  "name": "1drvteam",
  "createdDateTime": "2017-05-09T20:56:00Z",
  "lastModifiedDateTime": "2017-05-09T20:56:01Z",
  "webUrl": "https://contoso.sharepoint.com/teams/1drvteam"
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Sites/Get by path"
} -->
