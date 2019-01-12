---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener un sitio de SharePoint
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 7ef1a6a3a0bdbcf84cb0e0696e280842a63f4812
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27942370"
---
# <a name="get-a-site-resource"></a><span data-ttu-id="e1832-102">Obtener un recurso site</span><span class="sxs-lookup"><span data-stu-id="e1832-102">Get a site resource</span></span>

> <span data-ttu-id="e1832-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e1832-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e1832-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e1832-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e1832-p102">Recupera las propiedades y relaciones de un recurso [site][]. Un recurso **site** representa un sitio de grupo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e1832-p102">Retrieve properties and relationships for a [site][] resource. A **site** resource represents a team site in SharePoint.</span></span>

[site]: ../resources/site.md

<span data-ttu-id="e1832-108">Un recurso **site** se resuelve con un identificador único compuesto de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e1832-108">A **site** is addressed be a unique identifier which is a composite ID of the following values:</span></span>

* <span data-ttu-id="e1832-109">Nombre de host de la colección de sitios (contoso.sharepoint.com)</span><span class="sxs-lookup"><span data-stu-id="e1832-109">Site collection hostname (contoso.sharepoint.com)</span></span>
* <span data-ttu-id="e1832-110">Identificador único (GUID) de la colección de sitios</span><span class="sxs-lookup"><span data-stu-id="e1832-110">Site collection unique ID (GUID)</span></span>
* <span data-ttu-id="e1832-111">Identificador único (GUID) del sitio</span><span class="sxs-lookup"><span data-stu-id="e1832-111">Site unique ID (GUID)</span></span>

<span data-ttu-id="e1832-112">También hay un identificador de sitio reservado, `root`, que siempre hace referencia al sitio raíz de un destino especificado de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="e1832-112">There is also a reserved site identifier, `root`, which always references the root site for a given target, as follows:</span></span>

* <span data-ttu-id="e1832-113">`/sites/root`: El sitio raíz del inquilino.</span><span class="sxs-lookup"><span data-stu-id="e1832-113">`/sites/root`: The tenant root site.</span></span>
* <span data-ttu-id="e1832-114">`/groups/{group-id}/sites/root`: Sitio del grupo.</span><span class="sxs-lookup"><span data-stu-id="e1832-114">`/groups/{group-id}/sites/root`: The group's team site.</span></span>

## <a name="permissions"></a><span data-ttu-id="e1832-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="e1832-115">Permissions</span></span>

<span data-ttu-id="e1832-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e1832-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e1832-118">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e1832-118">Permission type</span></span>      | <span data-ttu-id="e1832-119">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e1832-119">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e1832-120">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e1832-120">Delegated (work or school account)</span></span> | <span data-ttu-id="e1832-121">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e1832-121">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="e1832-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e1832-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e1832-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e1832-123">Not supported.</span></span>    |
|<span data-ttu-id="e1832-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e1832-124">Application</span></span> | <span data-ttu-id="e1832-125">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e1832-125">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="get-the-tenants-root-site"></a><span data-ttu-id="e1832-126">Obtener el sitio raíz del inquilino</span><span class="sxs-lookup"><span data-stu-id="e1832-126">Get the tenant's root site</span></span>

<span data-ttu-id="e1832-127">Para obtener acceso al sitio de SharePoint de raíz dentro de un inquilino:</span><span class="sxs-lookup"><span data-stu-id="e1832-127">To access the root SharePoint site within a tenant:</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /sites/root
GET /sites/contoso.sharepoint.com
```

## <a name="access-a-site-by-server-relative-url"></a><span data-ttu-id="e1832-128">Obtener acceso a un sitio mediante la dirección URL relativa al servidor</span><span class="sxs-lookup"><span data-stu-id="e1832-128">Access a site by server-relative URL</span></span>

<span data-ttu-id="e1832-129">Si tiene la dirección URL relativa al servidor de un recurso **site**, puede construir una solicitud de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="e1832-129">If you have the server-relative URL for a **site** resource, you can construct a request as follows:</span></span>

```http
GET /sites/{hostname}:/{server-relative-path}
```

## <a name="access-a-group-team-site"></a><span data-ttu-id="e1832-130">Obtener acceso a un sitio de grupo</span><span class="sxs-lookup"><span data-stu-id="e1832-130">Access a group team site</span></span>

<span data-ttu-id="e1832-131">Para obtener acceso al sitio de grupo de un grupo:</span><span class="sxs-lookup"><span data-stu-id="e1832-131">To access the team site for a group:</span></span>

```http
GET /groups/{group-id}/sites/root
```

## <a name="example"></a><span data-ttu-id="e1832-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1832-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="e1832-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e1832-133">Request</span></span>

<!-- { "blockType": "request", "name": "get-site" } -->

```http
GET /sites/{site-id}
```

### <a name="response"></a><span data-ttu-id="e1832-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1832-134">Response</span></span>

<!-- { "blockType": "response", "@type": "microsoft.graph.site", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

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
  "tocPath": "Sites/Get by ID"
} -->
