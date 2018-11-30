---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Buscar sitios de SharePoint por palabra clave
ms.openlocfilehash: 8022a49cd545f99df74157f80a133e3e5174a964
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032622"
---
# <a name="search-for-sites"></a><span data-ttu-id="b4deb-102">Buscar sitios</span><span class="sxs-lookup"><span data-stu-id="b4deb-102">Search for sites</span></span>

<span data-ttu-id="b4deb-103">Busque en el inquilino de SharePoint [sitios][] que coincidan con las palabras clave proporcionadas.</span><span class="sxs-lookup"><span data-stu-id="b4deb-103">Search across a SharePoint tenant for [sites][] that match provided keywords.</span></span>

[sites]: ../resources/site.md

## <a name="permissions"></a><span data-ttu-id="b4deb-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b4deb-105">Permissions</span></span>

<span data-ttu-id="b4deb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b4deb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b4deb-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b4deb-108">Permission type</span></span>                        | <span data-ttu-id="b4deb-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b4deb-109">Permissions (from least to most privileged)</span></span>
|:--------------------------------------|:-------------------------------------
|<span data-ttu-id="b4deb-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b4deb-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="b4deb-111">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4deb-111">Sites.Read.All, Sites.ReadWrite.All</span></span>
|<span data-ttu-id="b4deb-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b4deb-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b4deb-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4deb-113">Not supported.</span></span>
|<span data-ttu-id="b4deb-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b4deb-114">Application</span></span>                            | <span data-ttu-id="b4deb-115">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4deb-115">Sites.Read.All, Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="b4deb-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b4deb-116">HTTP request</span></span>

<!-- { "blockType": "request", "name": "search-sites", "scopes": "sites.readwrite.all", "tags": "service.sharepoint" } -->

```http
GET /sites?search={query}
```

## <a name="response"></a><span data-ttu-id="b4deb-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4deb-117">Response</span></span>

<!-- { "blockType": "response", "@type": "Collection(microsoft.graph.site)", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "contoso.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,712a596e-90a1-49e3-9b48-bfa80bee8740",
      "name": "Team A Site",
      "description": "",
      "createdDateTime": "2016-10-18T03:05:59Z",
      "lastModifiedDateTime": "2016-10-18T10:40:59Z",
      "webUrl": "https://contoso.sharepoint.com/sites/siteA"
    },
    {
      "id": "contoso.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,0271110f-634f-4300-a841-3a8a2e851851",
      "name": "Team B Site",
      "description": "",
      "createdDateTime": "2016-10-18T03:05:59Z",
      "lastModifiedDateTime": "2016-10-18T10:40:59Z",
      "webUrl": "https://contoso.sharepoint.com/sites/siteB"
    }
  ]
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Sites/Search"
} -->
