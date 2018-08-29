---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enumerar los subsitios de un sitio de SharePoint
ms.openlocfilehash: 873b3666352e7e90dc7ffeccdfe984b384f857f2
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23265424"
---
# <a name="enumerate-subsites"></a><span data-ttu-id="aedb1-102">Enumerar subsitios</span><span class="sxs-lookup"><span data-stu-id="aedb1-102">Enumerate subsites</span></span>

<span data-ttu-id="aedb1-103">Obtener una colección de subsitios definidos para un objeto [site][].</span><span class="sxs-lookup"><span data-stu-id="aedb1-103">Get a collection of subsites defined for a [site][].</span></span>

[site]: ../resources/site.md

## <a name="permissions"></a><span data-ttu-id="aedb1-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="aedb1-105">Permissions</span></span>

<span data-ttu-id="aedb1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="aedb1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="aedb1-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aedb1-108">Permission type</span></span>      | <span data-ttu-id="aedb1-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aedb1-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="aedb1-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aedb1-110">Delegated (work or school account)</span></span> | <span data-ttu-id="aedb1-111">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aedb1-111">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="aedb1-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aedb1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="aedb1-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aedb1-113">Not supported.</span></span>    |
|<span data-ttu-id="aedb1-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aedb1-114">Application</span></span> | <span data-ttu-id="aedb1-115">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aedb1-115">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="aedb1-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aedb1-116">HTTP request</span></span>

<!-- { "blockType": "request", "name": "list-subsites", "scopes": "sites.read.all", "tags": "service.sharepoint" } -->

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/sites
```

## <a name="response"></a><span data-ttu-id="aedb1-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aedb1-117">Response</span></span>

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
