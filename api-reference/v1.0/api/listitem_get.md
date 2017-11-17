---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Obtener una entrada de una lista de SharePoint
ms.openlocfilehash: eaa97e169a8fcfdcb676679bb6dedd3a192925d8
ms.sourcegitcommit: 339070a20730bc4d363da7eb346d5f3c1e1d6c3e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="get-an-item-in-a-list"></a><span data-ttu-id="d0a35-102">Obtener un elemento en una lista</span><span class="sxs-lookup"><span data-stu-id="d0a35-102">Get an item in a list</span></span>

<span data-ttu-id="d0a35-103">Devuelve los metadatos de un [elemento][] en un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="d0a35-103">Returns the metadata for an [item][] in a [list][].</span></span>

[list]: ../resources/list.md
[elemento]: ../resources/listItem.md

## <a name="permissions"></a><span data-ttu-id="d0a35-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="d0a35-106">Permissions</span></span>

<span data-ttu-id="d0a35-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d0a35-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d0a35-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d0a35-109">Permission type</span></span>      | <span data-ttu-id="d0a35-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d0a35-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d0a35-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d0a35-111">Delegated (work or school account)</span></span> | <span data-ttu-id="d0a35-112">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0a35-112">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="d0a35-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0a35-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d0a35-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0a35-114">Not supported.</span></span>    |
|<span data-ttu-id="d0a35-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d0a35-115">Application</span></span> | <span data-ttu-id="d0a35-116">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0a35-116">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d0a35-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0a35-117">HTTP request</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}?expand=fields
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}?expand=fields(select=Column1,Column2)
```

## <a name="example"></a><span data-ttu-id="d0a35-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0a35-118">Example</span></span>

##### <a name="request"></a><span data-ttu-id="d0a35-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0a35-119">Request</span></span>

<!-- { "blockType": "request", "name": "get-list-item" } -->

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}?expand=fields
```

##### <a name="response"></a><span data-ttu-id="d0a35-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0a35-120">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.listItem", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "d14922d8-43e6-4c8a-b029-e35c5b4e0d63",
  "listItemId": 2,
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
