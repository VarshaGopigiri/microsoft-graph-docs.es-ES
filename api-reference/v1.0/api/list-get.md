---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Obtener una lista de SharePoint
localization_priority: Priority
ms.openlocfilehash: 0485a8bf3c37af3c659e7a630b65a5fd8f1849f7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809887"
---
# <a name="get-metadata-for-a-list"></a><span data-ttu-id="574dd-102">Obtener los metadatos de una lista</span><span class="sxs-lookup"><span data-stu-id="574dd-102">Get metadata for a list</span></span>

<span data-ttu-id="574dd-103">Devuelve los metadatos de un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="574dd-103">Returns the metadata for a [list][].</span></span>

[list]: ../resources/list.md

## <a name="permissions"></a><span data-ttu-id="574dd-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="574dd-105">Permissions</span></span>

<span data-ttu-id="574dd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="574dd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="574dd-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="574dd-108">Permission type</span></span>      | <span data-ttu-id="574dd-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="574dd-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="574dd-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="574dd-110">Delegated (work or school account)</span></span> | <span data-ttu-id="574dd-111">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="574dd-111">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="574dd-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="574dd-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="574dd-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="574dd-113">Not supported.</span></span>    |
|<span data-ttu-id="574dd-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="574dd-114">Application</span></span> | <span data-ttu-id="574dd-115">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="574dd-115">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="574dd-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="574dd-116">HTTP request</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}?expand=columns,items(expand=fields)
```

## <a name="request-body"></a><span data-ttu-id="574dd-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="574dd-117">Request body</span></span>

<span data-ttu-id="574dd-118">No proporcione un cuerpo de solicitud con este método.</span><span class="sxs-lookup"><span data-stu-id="574dd-118">Do not supply a request body with this method.</span></span>

## <a name="example"></a><span data-ttu-id="574dd-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="574dd-119">Example</span></span>

#### <a name="request"></a><span data-ttu-id="574dd-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="574dd-120">Request</span></span>

<!-- { "blockType": "request", "name": "get-list", "scopes": "sites.read.all" } -->

```http
GET /sites/{site-id}/lists/{list-id}
```

#### <a name="response"></a><span data-ttu-id="574dd-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="574dd-121">Response</span></span>

<!-- { "blockType": "response", "@type": "microsoft.graph.list", "truncated": true, "scopes": "sites.read.all", "tags": "service.sharepoint" } -->

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

<span data-ttu-id="574dd-122">Con las instrucciones `select` y `expand`, puede recuperar metadatos de listas, definiciones de columnas y elementos de lista en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="574dd-122">With `select` and `expand` statements, you can retrieve list metadata, column definitions, and list items in a single request.</span></span>

#### <a name="request"></a><span data-ttu-id="574dd-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="574dd-123">Request</span></span>

<!-- { "blockType": "request", "name": "get-list-multi-expand", "scopes": "sites.read.all" } -->

```http
GET /sites/{site-id}/lists/{list-id}?select=id,name,lastModifiedDateTime&expand=columns(select=name,description),items(expand=fields(select=Name,Color,Quantity))
```

#### <a name="response"></a><span data-ttu-id="574dd-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="574dd-124">Response</span></span>

<!-- { "blockType": "response", "@type": "microsoft.graph.list", "truncated": true, "scopes": "sites.read.all", "tags": "service.sharepoint" } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "1234-112-112-4",
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
