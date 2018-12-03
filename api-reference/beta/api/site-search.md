---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Buscar sitios de SharePoint por palabra clave
ms.openlocfilehash: c3c5ba005521e3405018e9b9403976297046f242
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091170"
---
# <a name="search-for-sites"></a><span data-ttu-id="62ac3-102">Buscar sitios</span><span class="sxs-lookup"><span data-stu-id="62ac3-102">Search for sites</span></span>

> <span data-ttu-id="62ac3-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="62ac3-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="62ac3-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="62ac3-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="62ac3-105">Busque en el inquilino de SharePoint [sitios][] que coincidan con las palabras clave proporcionadas.</span><span class="sxs-lookup"><span data-stu-id="62ac3-105">Search across a SharePoint tenant for [sites][] that match provided keywords.</span></span>

[sites]: ../resources/site.md

## <a name="permissions"></a><span data-ttu-id="62ac3-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="62ac3-107">Permissions</span></span>

<span data-ttu-id="62ac3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="62ac3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="62ac3-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="62ac3-110">Permission type</span></span>                        | <span data-ttu-id="62ac3-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="62ac3-111">Permissions (from least to most privileged)</span></span>
|:--------------------------------------|:-------------------------------------
|<span data-ttu-id="62ac3-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="62ac3-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="62ac3-113">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="62ac3-113">Sites.Read.All, Sites.ReadWrite.All</span></span>
|<span data-ttu-id="62ac3-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="62ac3-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="62ac3-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="62ac3-115">Not supported.</span></span>
|<span data-ttu-id="62ac3-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="62ac3-116">Application</span></span>                            | <span data-ttu-id="62ac3-117">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="62ac3-117">Sites.Read.All, Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="62ac3-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="62ac3-118">HTTP request</span></span>

<!-- { "blockType": "request", "name": "search-sites", "scopes": "service.sharepoint sites.readwrite.all" } -->

```http
GET https://graph.microsoft.com/beta/sites?search={query}
```

## <a name="response"></a><span data-ttu-id="62ac3-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62ac3-119">Response</span></span>

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