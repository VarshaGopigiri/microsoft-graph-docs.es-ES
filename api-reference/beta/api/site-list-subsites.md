---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enumerar los subsitios de un sitio de SharePoint
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 0632f250e38d20cb1975effea752177dff9f8569
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949993"
---
# <a name="enumerate-subsites"></a><span data-ttu-id="34b13-102">Enumerar subsitios</span><span class="sxs-lookup"><span data-stu-id="34b13-102">Enumerate subsites</span></span>

> <span data-ttu-id="34b13-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="34b13-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="34b13-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="34b13-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="34b13-105">Obtener una colección de subsitios definidos para un objeto [site][].</span><span class="sxs-lookup"><span data-stu-id="34b13-105">Get a collection of subsites defined for a [site][].</span></span>

[site]: ../resources/site.md

## <a name="permissions"></a><span data-ttu-id="34b13-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="34b13-107">Permissions</span></span>

<span data-ttu-id="34b13-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="34b13-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="34b13-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="34b13-110">Permission type</span></span>      | <span data-ttu-id="34b13-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="34b13-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="34b13-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="34b13-112">Delegated (work or school account)</span></span> | <span data-ttu-id="34b13-113">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="34b13-113">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="34b13-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="34b13-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="34b13-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="34b13-115">Not supported.</span></span>    |
|<span data-ttu-id="34b13-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="34b13-116">Application</span></span> | <span data-ttu-id="34b13-117">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="34b13-117">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="34b13-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="34b13-118">HTTP request</span></span>

<!-- { "blockType": "request", "name": "list-subsites", "scopes": "service.sharepoint sites.read.all" } -->

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/sites
```

## <a name="response"></a><span data-ttu-id="34b13-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34b13-119">Response</span></span>

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
