---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Obtener una entrada de una lista de SharePoint
ms.openlocfilehash: b650507e8a8bc74b8156117f765220712a2a46d2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030373"
---
# <a name="get-an-item-in-a-list"></a><span data-ttu-id="a9fe8-102">Obtener un elemento en una lista</span><span class="sxs-lookup"><span data-stu-id="a9fe8-102">Get an item in a list</span></span>

<span data-ttu-id="a9fe8-103">Devuelve los metadatos de un [elemento][] en un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="a9fe8-103">Returns the metadata for an [item][] in a [list][].</span></span>

[list]: ../resources/list.md
[elemento]: ../resources/listitem.md
[item]: ../resources/listitem.md

## <a name="permissions"></a><span data-ttu-id="a9fe8-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="a9fe8-106">Permissions</span></span>

<span data-ttu-id="a9fe8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a9fe8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a9fe8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a9fe8-109">Permission type</span></span>      | <span data-ttu-id="a9fe8-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a9fe8-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a9fe8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a9fe8-111">Delegated (work or school account)</span></span> | <span data-ttu-id="a9fe8-112">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a9fe8-112">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="a9fe8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a9fe8-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a9fe8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-114">Not supported.</span></span>    |
|<span data-ttu-id="a9fe8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a9fe8-115">Application</span></span> | <span data-ttu-id="a9fe8-116">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a9fe8-116">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a9fe8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a9fe8-117">HTTP request</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}?expand=fields
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}?expand=fields(select=Column1,Column2)
```

## <a name="example"></a><span data-ttu-id="a9fe8-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a9fe8-118">Example</span></span>

##### <a name="request"></a><span data-ttu-id="a9fe8-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a9fe8-119">Request</span></span>

<!-- { "blockType": "request", "name": "get-list-item", "scopes": "sites.read.all" } -->

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}?expand=fields
```

##### <a name="response"></a><span data-ttu-id="a9fe8-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a9fe8-120">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.listItem", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "5",
  "fields": {
    "Name": "Widget",
    "Color": "Blue",
    "Quantity": 2357
    }
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "ListItem/Get metadata"
} -->