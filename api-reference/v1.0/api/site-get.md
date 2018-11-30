---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener un sitio de SharePoint
ms.openlocfilehash: 03edd76f6d6855d8b8d2271d2d99f8b39071710d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032181"
---
# <a name="get-a-site-resource"></a><span data-ttu-id="51796-102">Obtener un recurso site</span><span class="sxs-lookup"><span data-stu-id="51796-102">Get a site resource</span></span>

<span data-ttu-id="51796-p101">Recupera las propiedades y relaciones de un recurso [site][]. Un recurso **site** representa un sitio de grupo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="51796-p101">Retrieve properties and relationships for a [site][] resource. A **site** resource represents a team site in SharePoint.</span></span>

[site]: ../resources/site.md

<span data-ttu-id="51796-106">Un recurso **site** se resuelve con un identificador único compuesto de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="51796-106">A **site** is addressed be a unique identifier which is a composite ID of the following values:</span></span>

* <span data-ttu-id="51796-107">Nombre de host de la colección de sitios (contoso.sharepoint.com)</span><span class="sxs-lookup"><span data-stu-id="51796-107">Site collection hostname (contoso.sharepoint.com)</span></span>
* <span data-ttu-id="51796-108">Identificador único (GUID) de la colección de sitios</span><span class="sxs-lookup"><span data-stu-id="51796-108">Site collection unique ID (GUID)</span></span>
* <span data-ttu-id="51796-109">Identificador único (GUID) del sitio</span><span class="sxs-lookup"><span data-stu-id="51796-109">Site unique ID (GUID)</span></span>

<span data-ttu-id="51796-110">También hay un identificador de sitio reservado, `root`, que siempre hace referencia al sitio raíz de un destino especificado de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="51796-110">There is also a reserved site identifier, `root`, which always references the root site for a given target, as follows:</span></span>

* <span data-ttu-id="51796-111">`/sites/root`: El sitio raíz del inquilino.</span><span class="sxs-lookup"><span data-stu-id="51796-111">`/sites/root`: The tenant root site.</span></span>
* <span data-ttu-id="51796-112">`/groups/{group-id}/sites/root`: Sitio del grupo.</span><span class="sxs-lookup"><span data-stu-id="51796-112">`/groups/{group-id}/sites/root`: The group's team site.</span></span>

## <a name="permissions"></a><span data-ttu-id="51796-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="51796-113">Permissions</span></span>

<span data-ttu-id="51796-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="51796-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="51796-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="51796-116">Permission type</span></span>      | <span data-ttu-id="51796-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="51796-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="51796-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="51796-118">Delegated (work or school account)</span></span> | <span data-ttu-id="51796-119">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="51796-119">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="51796-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="51796-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="51796-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51796-121">Not supported.</span></span>    |
|<span data-ttu-id="51796-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="51796-122">Application</span></span> | <span data-ttu-id="51796-123">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="51796-123">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="get-the-tenants-root-site"></a><span data-ttu-id="51796-124">Obtener el sitio raíz del inquilino</span><span class="sxs-lookup"><span data-stu-id="51796-124">Get the tenant's root site</span></span>

<span data-ttu-id="51796-125">Para obtener acceso al sitio de SharePoint de raíz dentro de un inquilino:</span><span class="sxs-lookup"><span data-stu-id="51796-125">To access the root SharePoint site within a tenant:</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /sites/root
GET /sites/contoso.sharepoint.com
```

## <a name="access-a-site-by-server-relative-url"></a><span data-ttu-id="51796-126">Obtener acceso a un sitio mediante la dirección URL relativa al servidor</span><span class="sxs-lookup"><span data-stu-id="51796-126">Access a site by server-relative URL</span></span>

<span data-ttu-id="51796-127">Si tiene la dirección URL relativa al servidor de un recurso **site**, puede construir una solicitud de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="51796-127">If you have the server-relative URL for a **site** resource, you can construct a request as follows:</span></span>

```http
GET /sites/{hostname}:/{server-relative-path}
```

## <a name="access-a-group-team-site"></a><span data-ttu-id="51796-128">Obtener acceso a un sitio de grupo</span><span class="sxs-lookup"><span data-stu-id="51796-128">Access a group team site</span></span>

<span data-ttu-id="51796-129">Para obtener acceso al sitio de grupo de un grupo:</span><span class="sxs-lookup"><span data-stu-id="51796-129">To access the team site for a group:</span></span>

```http
GET /groups/{group-id}/sites/root
```

## <a name="example"></a><span data-ttu-id="51796-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51796-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="51796-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51796-131">Request</span></span>

<!-- { "blockType": "request", "name": "get-site", "scopes": "sites.read.all" } -->

```http
GET /sites/{site-id}
```

### <a name="response"></a><span data-ttu-id="51796-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51796-132">Response</span></span>

<!-- { "blockType": "response", "@type": "microsoft.graph.site", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

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
  "tocPath": "Sites/Get by ID"
} -->
