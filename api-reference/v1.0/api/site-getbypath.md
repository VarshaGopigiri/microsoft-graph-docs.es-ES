---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener un sitio de SharePoint mediante la ruta de acceso
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: baf8b4a8d319450d7558bdcf73c34dc7845d0c57
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27948810"
---
# <a name="get-a-site-resource-by-path"></a><span data-ttu-id="fdeba-102">Obtener un recurso de sitio mediante la ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="fdeba-102">Get a site resource by path</span></span>

<span data-ttu-id="fdeba-p101">Recupera las propiedades y relaciones de un recurso [site][]. Un recurso **site** representa un sitio de grupo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fdeba-p101">Retrieve properties and relationships for a [site][] resource. A **site** resource represents a team site in SharePoint.</span></span>

[site]: ../resources/site.md

<span data-ttu-id="fdeba-106">Además de recuperar un [sitio mediante id.](site-get.md), puede recuperar un sitio basándose en la ruta de URL relativa del servidor.</span><span class="sxs-lookup"><span data-stu-id="fdeba-106">In addition to retrieving a [site by ID](site-get.md) you can retrieve a site based on server-relative URL path.</span></span>

* <span data-ttu-id="fdeba-107">Nombre de host de la colección de sitios (contoso.sharepoint.com)</span><span class="sxs-lookup"><span data-stu-id="fdeba-107">Site collection hostname (contoso.sharepoint.com)</span></span>
* <span data-ttu-id="fdeba-108">Ruta de sitio, relativa al nombre de host del servidor.</span><span class="sxs-lookup"><span data-stu-id="fdeba-108">Site path, relative to server hostname.</span></span>

<span data-ttu-id="fdeba-109">También hay un identificador de sitio reservado, `root`, que siempre hace referencia al sitio raíz para un destino especificado de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="fdeba-109">There is also a reserved site identifier, `root`, which always references the root site for a given target, as follows:</span></span>

* <span data-ttu-id="fdeba-110">`/sites/root`: El sitio raíz del inquilino.</span><span class="sxs-lookup"><span data-stu-id="fdeba-110">`/sites/root`: The tenant root site.</span></span>
* <span data-ttu-id="fdeba-111">`/groups/{group-id}/sites/root`: Sitio del grupo.</span><span class="sxs-lookup"><span data-stu-id="fdeba-111">`/groups/{group-id}/sites/root`: The group's team site.</span></span>

## <a name="permissions"></a><span data-ttu-id="fdeba-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="fdeba-112">Permissions</span></span>

<span data-ttu-id="fdeba-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fdeba-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fdeba-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fdeba-115">Permission type</span></span>      | <span data-ttu-id="fdeba-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fdeba-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fdeba-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fdeba-117">Delegated (work or school account)</span></span> | <span data-ttu-id="fdeba-118">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fdeba-118">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="fdeba-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fdeba-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fdeba-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fdeba-120">Not supported.</span></span>    |
|<span data-ttu-id="fdeba-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fdeba-121">Application</span></span> | <span data-ttu-id="fdeba-122">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fdeba-122">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="fdeba-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fdeba-123">HTTP Request</span></span>

<span data-ttu-id="fdeba-124">Para obtener acceso al sitio de SharePoint de raíz con una ruta relativa:</span><span class="sxs-lookup"><span data-stu-id="fdeba-124">To access the root SharePoint site with a relative path:</span></span>

<!-- { "blockType": "request", "name": "get-site-by-hostname-and-path", "scopes": "sites.read.all", "tags": "service.sharepoint" } -->

```http
GET /sites/{hostname}:/{relative-path}
```

## <a name="response"></a><span data-ttu-id="fdeba-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fdeba-125">Response</span></span>

<span data-ttu-id="fdeba-126">Este método devuelve un recurso [site][] para el sitio al que se hace referencia mediante el identificador único.</span><span class="sxs-lookup"><span data-stu-id="fdeba-126">This method returns a [site][] resource for the site referenced by the unique identifier.</span></span>

<!-- { "blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.site" } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "contoso.sharepoint.com,2C712604-1370-44E7-A1F5-426573FDA80A,2D2244C3-251A-49EA-93A8-39E1C3A060FE",
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
  "suppressions": [
    "Warning: Couldn't serialize request for path /sites/{var}/children/{var} into EDMX: System.InvalidOperationException: Uri path requires navigating into unknown object hierarchy: missing property 'children' on 'site'. Possible issues:
         1) Doc bug where 'children' isn't defined on the resource.      2) Doc bug where 'children' is an example key and should instead be replaced with a placeholder like {item-id} or declared in the sampleKeys annotation.       3) Doc bug where 'site' is supposed to be an entity type, but is being treated as a complex because it (and its ancestors) are missing the keyProperty annotation
     at ApiDocs.Publishing.CSDL.CsdlWriter.ParseRequestTargetType(String requestPath, MethodCollection requestMethodCollection, EntityFramework edmx, IssueLogger issues) in D:/src/mds2/ApiDocs.Publishing/CSDL/CsdlWriter.cs:line 982
     at ApiDocs.Publishing.CSDL.CsdlWriter.ProcessRestRequestPaths(EntityFramework edmx, String[] baseUrlsToRemove, IssueLogger issues) in D:/src/mds2/ApiDocs.Publishing/CSDL/CsdlWriter.cs:line 653"
  ],
  "tocPath": "Sites/Get by path"
} -->
