---
title: Enumerar sitios
description: El [de] [sitios] disponibles en una organización que coinciden con los criterios de filtro proporcionado y las opciones de consulta de la lista.
ms.openlocfilehash: 4e7d9d12f7b18df84a8b23cc3272084b310edb3a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087829"
---
# <a name="enumerate-sites"></a><span data-ttu-id="fe02b-103">Enumerar sitios</span><span class="sxs-lookup"><span data-stu-id="fe02b-103">Enumerate sites</span></span>

> <span data-ttu-id="fe02b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fe02b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fe02b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fe02b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fe02b-106">Lista de los [sitios][] disponibles en una organización que coinciden con los criterios de filtro proporcionado y las opciones de consulta.</span><span class="sxs-lookup"><span data-stu-id="fe02b-106">List the available [sites][] in an organization that match provided filter criteria and query options.</span></span>

<span data-ttu-id="fe02b-107">Actualmente se admiten las siguientes opciones de consulta:</span><span class="sxs-lookup"><span data-stu-id="fe02b-107">Only the following query options are currently supported:</span></span>

| <span data-ttu-id="fe02b-108">Instrucción de filtro</span><span class="sxs-lookup"><span data-stu-id="fe02b-108">Filter statement</span></span>             | <span data-ttu-id="fe02b-109">Instrucción SELECT</span><span class="sxs-lookup"><span data-stu-id="fe02b-109">Select statement</span></span>        | <span data-ttu-id="fe02b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe02b-110">Description</span></span>
|:-----------------------------|:------------------------|:--------------------
|`siteCollection/root ne null` | `siteCollection,webUrl` | <span data-ttu-id="fe02b-111">Se enumeran todas las colecciones de sitios de nivel raíz de la organización.</span><span class="sxs-lookup"><span data-stu-id="fe02b-111">Lists all root-level site collections in the organization.</span></span> <span data-ttu-id="fe02b-112">Es útil para descubrir el sitio principal para cada zona geográfica.</span><span class="sxs-lookup"><span data-stu-id="fe02b-112">Useful for discovering the home site for each geography.</span></span>

<span data-ttu-id="fe02b-113">Además, puede usar una consulta de **[búsqueda][]** en la colección '/ sites' para encontrar los sitios que coincidan con las palabras clave al indicar.</span><span class="sxs-lookup"><span data-stu-id="fe02b-113">In addition, you may use a **[search][]** query against the '/sites' collection to find sites matching given keywords.</span></span>

[búsqueda]: site-search.md
[search]: site-search.md
[sites]: ../resources/site.md

## <a name="permissions"></a><span data-ttu-id="fe02b-116">Permisos</span><span class="sxs-lookup"><span data-stu-id="fe02b-116">Permissions</span></span>

<span data-ttu-id="fe02b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fe02b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fe02b-119">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fe02b-119">Permission type</span></span>                        | <span data-ttu-id="fe02b-120">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fe02b-120">Permissions (from least to most privileged)</span></span>
|:--------------------------------------|:-------------------------------------
|<span data-ttu-id="fe02b-121">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fe02b-121">Delegated (work or school account)</span></span>     | <span data-ttu-id="fe02b-122">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fe02b-122">Sites.Read.All, Sites.ReadWrite.All</span></span>
|<span data-ttu-id="fe02b-123">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fe02b-123">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fe02b-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fe02b-124">Not supported.</span></span>
|<span data-ttu-id="fe02b-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fe02b-125">Application</span></span>                            | <span data-ttu-id="fe02b-126">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fe02b-126">Sites.Read.All, Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="fe02b-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fe02b-127">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET https://graph.microsoft.com/beta/sites?filter=siteCollection/root ne null
```

## <a name="example"></a><span data-ttu-id="fe02b-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe02b-128">Example</span></span>

#### <a name="request"></a><span data-ttu-id="fe02b-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fe02b-129">Request</span></span>

<!-- { "blockType": "request", "name": "list-sites" } -->

```http
GET https://graph.microsoft.com/beta/sites?select=siteCollection,webUrl&filter=siteCollection/root%20ne%20null
```

#### <a name="response"></a><span data-ttu-id="fe02b-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe02b-130">Response</span></span>

<!-- { "blockType": "response", "@type": "microsoft.graph.site", "isCollection": true, "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "contoso.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,712a596e-90a1-49e3-9b48-bfa80bee8740",
      "name": "Contoso USA",
      "root": { },
      "siteCollection": {
        "hostname": "contoso.sharepoint.com",
        "dataLocationCode": "NAM",
        "root": { }
      },
      "webUrl": "https://contoso.sharepoint.com"
    },
    {
      "id": "contoso-jpn.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,0271110f-634f-4300-a841-3a8a2e851851",
      "name": "Contoso Japan",
      "root": { },
      "siteCollection": {
        "hostname": "contoso-jp.sharepoint.com",
        "dataLocationCode": "JPN",
        "root": { }
      },
      "webUrl": "https://contoso-jp.sharepoint.com"
    }
  ]
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Site/List sites"
} -->
