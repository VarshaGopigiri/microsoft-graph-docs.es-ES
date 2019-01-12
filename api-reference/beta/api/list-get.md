---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Obtener una lista de SharePoint
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: f9744ec25d852359246e84c83ba3bd1dec92ff17
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27927957"
---
# <a name="get-metadata-for-a-list"></a><span data-ttu-id="5908c-102">Obtener los metadatos de una lista</span><span class="sxs-lookup"><span data-stu-id="5908c-102">Get metadata for a list</span></span>

> <span data-ttu-id="5908c-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5908c-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5908c-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5908c-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5908c-105">Devuelve los metadatos de un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="5908c-105">Returns the metadata for a [list][].</span></span>

[list]: ../resources/list.md

## <a name="permissions"></a><span data-ttu-id="5908c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5908c-107">Permissions</span></span>

<span data-ttu-id="5908c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5908c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5908c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5908c-110">Permission type</span></span>      | <span data-ttu-id="5908c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5908c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5908c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5908c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5908c-113">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5908c-113">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="5908c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5908c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5908c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5908c-115">Not supported.</span></span>    |
|<span data-ttu-id="5908c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5908c-116">Application</span></span> | <span data-ttu-id="5908c-117">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5908c-117">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5908c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5908c-118">HTTP request</span></span>

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}?expand=columns,items(expand=fields)
```

## <a name="request-body"></a><span data-ttu-id="5908c-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5908c-119">Request body</span></span>

<span data-ttu-id="5908c-120">No proporcione un cuerpo de solicitud con este método.</span><span class="sxs-lookup"><span data-stu-id="5908c-120">Do not supply a request body with this method.</span></span>

## <a name="example"></a><span data-ttu-id="5908c-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5908c-121">Example</span></span>

#### <a name="request"></a><span data-ttu-id="5908c-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5908c-122">Request</span></span>

<!-- { "blockType": "request", "name": "get-list" } -->

```http
GET /sites/{site-id}/lists/{list-id}
```

#### <a name="response"></a><span data-ttu-id="5908c-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5908c-123">Response</span></span>

<!-- { "blockType": "response", "@type": "microsoft.graph.list", "truncated": true, "scopes": "sites.read.all service.sharepoint" } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "1234-112-112-4",
  "name": "MicroFeed",
  "createdDateTime": "2016-08-30T08:32:00Z",
  "lastModifiedDateTime": "2016-08-30T08:32:00Z",
  "list": {
    "hidden": false,
    "template": "genericList"
    }
}
```

<span data-ttu-id="5908c-124">Con las instrucciones `select` y `expand`, puede recuperar metadatos de listas, definiciones de columnas y elementos de lista en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="5908c-124">With `select` and `expand` statements, you can retrieve list metadata, column definitions, and list items in a single request.</span></span>

#### <a name="request"></a><span data-ttu-id="5908c-125">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5908c-125">Request</span></span>

<!-- { "blockType": "request", "name": "get-list-multi-expand" } -->

```http
GET /sites/{site-id}/lists/{list-id}?select=name,lastModifiedDateTime&expand=columns(select=name,description),items(expand=fields(select=Name,Color,Quantity))
```

#### <a name="response"></a><span data-ttu-id="5908c-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5908c-126">Response</span></span>

<!-- { "blockType": "response", "@type": "microsoft.graph.list", "truncated": true, "scopes": "sites.read.all service.sharepoint" } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "name": "Inventory",
  "lastModifiedDateTime": "2016-08-30T08:32:00Z",
  "columns": [
    {
      "name": "Name",
      "description": "Customer-facing name of the SKU"
    },
    {
      "name": "Color",
      "description": "Color of the item in stock"
    },
    {
      "name": "Quantity",
      "description": "Number of items in stock"
    }
  ],
  "items": [
    {
      "id": "2",
      "fields": {
        "Name": "Gadget",
        "Color": "Red",
        "Quantity": 503
       }
    },
    {
      "id": "4",
      "fields": {
        "Name": "Widget",
        "Color": "Blue",
        "Quantity": 2357
       }
    },
    {
      "id": "7",
      "fields": {
        "Name": "Gizmo",
        "Color": "Green",
        "Quantity": 92
       }
    }
  ]
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Lists/Get metadata"
} -->
