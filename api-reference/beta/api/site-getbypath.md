---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener un sitio de SharePoint mediante la ruta de acceso
localization_priority: Normal
ms.openlocfilehash: 09d9aef99f552079e8e5e4f7d0d260964a182786
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821535"
---
# <a name="get-a-site-resource-by-path"></a><span data-ttu-id="ba345-102">Obtener un recurso de sitio mediante la ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="ba345-102">Get a site resource by path</span></span>

> <span data-ttu-id="ba345-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ba345-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ba345-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ba345-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ba345-p102">Recupera las propiedades y relaciones de un recurso [site][]. Un recurso **site** representa un sitio de grupo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ba345-p102">Retrieve properties and relationships for a [site][] resource. A **site** resource represents a team site in SharePoint.</span></span>

[site]: ../resources/site.md

<span data-ttu-id="ba345-108">Además de recuperar un [sitio mediante id.](site-get.md), puede recuperar un sitio basándose en la ruta de URL relativa del servidor.</span><span class="sxs-lookup"><span data-stu-id="ba345-108">In addition to retrieving a [site by ID](site-get.md) you can retrieve a site based on server-relative URL path.</span></span>

* <span data-ttu-id="ba345-109">Nombre de host de la colección de sitios (contoso.sharepoint.com)</span><span class="sxs-lookup"><span data-stu-id="ba345-109">Site collection hostname (contoso.sharepoint.com)</span></span>
* <span data-ttu-id="ba345-110">Ruta de sitio, relativa al nombre de host del servidor.</span><span class="sxs-lookup"><span data-stu-id="ba345-110">Site path, relative to server hostname.</span></span>

<span data-ttu-id="ba345-111">También hay un identificador de sitio reservado, `root`, que siempre hace referencia al sitio raíz para un destino especificado de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="ba345-111">There is also a reserved site identifier, `root`, which always references the root site for a given target, as follows:</span></span>

* <span data-ttu-id="ba345-112">`/sites/root`: El sitio raíz del inquilino.</span><span class="sxs-lookup"><span data-stu-id="ba345-112">`/sites/root`: The tenant root site.</span></span>
* <span data-ttu-id="ba345-113">`/groups/{group-id}/sites/root`: Sitio del grupo.</span><span class="sxs-lookup"><span data-stu-id="ba345-113">`/groups/{group-id}/sites/root`: The group's team site.</span></span>

## <a name="permissions"></a><span data-ttu-id="ba345-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="ba345-114">Permissions</span></span>

<span data-ttu-id="ba345-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ba345-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ba345-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ba345-117">Permission type</span></span>      | <span data-ttu-id="ba345-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ba345-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ba345-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ba345-119">Delegated (work or school account)</span></span> | <span data-ttu-id="ba345-120">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ba345-120">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="ba345-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ba345-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ba345-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ba345-122">Not supported.</span></span>    |
|<span data-ttu-id="ba345-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ba345-123">Application</span></span> | <span data-ttu-id="ba345-124">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ba345-124">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ba345-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ba345-125">HTTP Request</span></span>

<span data-ttu-id="ba345-126">Para obtener acceso al sitio de SharePoint de raíz con una ruta relativa:</span><span class="sxs-lookup"><span data-stu-id="ba345-126">To access the root SharePoint site with a relative path:</span></span>

<!-- { "blockType": "request", "name": "get-site-by-hostname-and-path", "scopes": "service.sharepoint sites.read.all" } -->

```http
GET /sites/{hostname}:/{relative-path}
```

## <a name="response"></a><span data-ttu-id="ba345-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba345-127">Response</span></span>

<span data-ttu-id="ba345-128">Este método devuelve un recurso [site][] para el sitio al que se hace referencia mediante el identificador único.</span><span class="sxs-lookup"><span data-stu-id="ba345-128">This method returns a [site][] resource for the site referenced by the unique identifier.</span></span>

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
