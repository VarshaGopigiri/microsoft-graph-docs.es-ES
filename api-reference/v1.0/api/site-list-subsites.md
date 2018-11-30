---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enumerar los subsitios de un sitio de SharePoint
ms.openlocfilehash: a26c2f592c11760b822c80a7e37749823a5172aa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029688"
---
# <a name="enumerate-subsites"></a><span data-ttu-id="b7979-102">Enumerar subsitios</span><span class="sxs-lookup"><span data-stu-id="b7979-102">Enumerate subsites</span></span>

<span data-ttu-id="b7979-103">Obtener una colección de subsitios definidos para un objeto [site][].</span><span class="sxs-lookup"><span data-stu-id="b7979-103">Get a collection of subsites defined for a [site][].</span></span>

[site]: ../resources/site.md

## <a name="permissions"></a><span data-ttu-id="b7979-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b7979-105">Permissions</span></span>

<span data-ttu-id="b7979-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b7979-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b7979-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b7979-108">Permission type</span></span>      | <span data-ttu-id="b7979-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b7979-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b7979-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b7979-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b7979-111">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b7979-111">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="b7979-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b7979-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b7979-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b7979-113">Not supported.</span></span>    |
|<span data-ttu-id="b7979-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b7979-114">Application</span></span> | <span data-ttu-id="b7979-115">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b7979-115">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b7979-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b7979-116">HTTP request</span></span>

<!-- { "blockType": "request", "name": "list-subsites", "scopes": "sites.read.all", "tags": "service.sharepoint" } -->

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/sites
```

## <a name="response"></a><span data-ttu-id="b7979-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7979-117">Response</span></span>

<!-- { "blockType": "response", "@type": "microsoft.graph.site", "isCollection": true, "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "contoso.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,712a596e-90a1-49e3-9b48-bfa80bee8740",
      "name": "Team A Subsite",
      "description": "",
      "createdDateTime": "2016-10-18T03:05:59Z",
      "lastModifiedDateTime": "2016-10-18T10:40:59Z",
      "webUrl": "https://contoso.sharepoint.com/sites/site/subsiteA"
    },
    {
      "id": "contoso.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,0271110f-634f-4300-a841-3a8a2e851851",
      "name": "Team B Subsite",
      "description": "",
      "createdDateTime": "2016-10-18T03:05:59Z",
      "lastModifiedDateTime": "2016-10-18T10:40:59Z",
      "webUrl": "https://contoso.sharepoint.com/sites/site/subsiteB"
    }
  ]
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Sites/List subsites"
} -->
