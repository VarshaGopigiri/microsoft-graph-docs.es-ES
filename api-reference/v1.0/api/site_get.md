---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener un sitio de SharePoint
ms.openlocfilehash: f3153845a0ce117c5442b5e66d1e96a388ac6720
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23264066"
---
# <a name="get-a-site-resource"></a><span data-ttu-id="1e4d3-102">Obtener un recurso site</span><span class="sxs-lookup"><span data-stu-id="1e4d3-102">Get a site resource</span></span>

<span data-ttu-id="1e4d3-p101">Recupera las propiedades y relaciones de un recurso [site][]. Un recurso **site** representa un sitio de grupo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1e4d3-p101">Retrieve properties and relationships for a [site][] resource. A **site** resource represents a team site in SharePoint.</span></span>

[site]: ../resources/site.md

<span data-ttu-id="1e4d3-106">Un recurso **site** se resuelve con un identificador único compuesto de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="1e4d3-106">A **site** is addressed be a unique identifier which is a composite ID of the following values:</span></span>

* <span data-ttu-id="1e4d3-107">Nombre de host de la colección de sitios (contoso.sharepoint.com)</span><span class="sxs-lookup"><span data-stu-id="1e4d3-107">Site collection hostname (contoso.sharepoint.com)</span></span>
* <span data-ttu-id="1e4d3-108">Identificador único (GUID) de la colección de sitios</span><span class="sxs-lookup"><span data-stu-id="1e4d3-108">Site collection unique ID (GUID)</span></span>
* <span data-ttu-id="1e4d3-109">Identificador único (GUID) del sitio</span><span class="sxs-lookup"><span data-stu-id="1e4d3-109">Site unique ID (GUID)</span></span>

<span data-ttu-id="1e4d3-110">También hay un identificador de sitio reservado, `root`, que siempre hace referencia al sitio raíz de un destino especificado de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="1e4d3-110">There is also a reserved site identifier, `root`, which always references the root site for a given target, as follows:</span></span>

* <span data-ttu-id="1e4d3-111">`/sites/root`: El sitio raíz del inquilino.</span><span class="sxs-lookup"><span data-stu-id="1e4d3-111">`/sites/root`: The tenant root site.</span></span>
* <span data-ttu-id="1e4d3-112">`/groups/{group-id}/sites/root`: Sitio del grupo.</span><span class="sxs-lookup"><span data-stu-id="1e4d3-112">`/groups/{group-id}/sites/root`: The group's team site.</span></span>

## <a name="permissions"></a><span data-ttu-id="1e4d3-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="1e4d3-113">Permissions</span></span>

<span data-ttu-id="1e4d3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1e4d3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1e4d3-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1e4d3-116">Permission type</span></span>      | <span data-ttu-id="1e4d3-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1e4d3-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1e4d3-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1e4d3-118">Delegated (work or school account)</span></span> | <span data-ttu-id="1e4d3-119">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1e4d3-119">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="1e4d3-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1e4d3-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1e4d3-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1e4d3-121">Not supported.</span></span>    |
|<span data-ttu-id="1e4d3-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1e4d3-122">Application</span></span> | <span data-ttu-id="1e4d3-123">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1e4d3-123">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="get-the-tenants-root-site"></a><span data-ttu-id="1e4d3-124">Obtener el sitio raíz del inquilino</span><span class="sxs-lookup"><span data-stu-id="1e4d3-124">Get the tenant's root site</span></span>

<span data-ttu-id="1e4d3-125">Para obtener acceso al sitio de SharePoint de raíz dentro de un inquilino:</span><span class="sxs-lookup"><span data-stu-id="1e4d3-125">To access the root SharePoint site within a tenant:</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /sites/root
GET /sites/contoso.sharepoint.com
```

## <a name="access-a-site-by-server-relative-url"></a><span data-ttu-id="1e4d3-126">Obtener acceso a un sitio mediante la dirección URL relativa al servidor</span><span class="sxs-lookup"><span data-stu-id="1e4d3-126">Access a site by server-relative URL</span></span>

<span data-ttu-id="1e4d3-127">Si tiene la dirección URL relativa al servidor de un recurso **site**, puede construir una solicitud de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="1e4d3-127">If you have the server-relative URL for a **site** resource, you can construct a request as follows:</span></span>

```http
GET /sites/{hostname}:/{server-relative-path}
```

## <a name="access-a-group-team-site"></a><span data-ttu-id="1e4d3-128">Obtener acceso a un sitio de grupo</span><span class="sxs-lookup"><span data-stu-id="1e4d3-128">Access a group team site</span></span>

<span data-ttu-id="1e4d3-129">Para obtener acceso al sitio de grupo de un grupo:</span><span class="sxs-lookup"><span data-stu-id="1e4d3-129">To access the team site for a group:</span></span>

```http
GET /groups/{group-id}/sites/root
```

## <a name="example"></a><span data-ttu-id="1e4d3-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1e4d3-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="1e4d3-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1e4d3-131">Request</span></span>

<!-- { "blockType": "request", "name": "get-site", "scopes": "sites.read.all" } -->

```http
GET /sites/{site-id}
```

### <a name="response"></a><span data-ttu-id="1e4d3-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e4d3-132">Response</span></span>

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
