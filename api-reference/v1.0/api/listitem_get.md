---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Obtener una entrada de una lista de SharePoint
ms.openlocfilehash: 418c64534fe20cd74ddba607fa9c765dc20bac42
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23270051"
---
# <a name="get-an-item-in-a-list"></a><span data-ttu-id="8e643-102">Obtener un elemento en una lista</span><span class="sxs-lookup"><span data-stu-id="8e643-102">Get an item in a list</span></span>

<span data-ttu-id="8e643-103">Devuelve los metadatos de un [elemento][] en un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="8e643-103">Returns the metadata for an [item][] in a [list][].</span></span>

[list]: ../resources/list.md
[elemento]: ../resources/listItem.md
[item]: ../resources/listItem.md

## <a name="permissions"></a><span data-ttu-id="8e643-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="8e643-106">Permissions</span></span>

<span data-ttu-id="8e643-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8e643-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8e643-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8e643-109">Permission type</span></span>      | <span data-ttu-id="8e643-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8e643-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8e643-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8e643-111">Delegated (work or school account)</span></span> | <span data-ttu-id="8e643-112">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8e643-112">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="8e643-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8e643-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8e643-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8e643-114">Not supported.</span></span>    |
|<span data-ttu-id="8e643-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8e643-115">Application</span></span> | <span data-ttu-id="8e643-116">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8e643-116">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8e643-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8e643-117">HTTP request</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}?expand=fields
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}?expand=fields(select=Column1,Column2)
```

## <a name="example"></a><span data-ttu-id="8e643-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8e643-118">Example</span></span>

##### <a name="request"></a><span data-ttu-id="8e643-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8e643-119">Request</span></span>

<!-- { "blockType": "request", "name": "get-list-item", "scopes": "sites.read.all" } -->

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}?expand=fields
```

##### <a name="response"></a><span data-ttu-id="8e643-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8e643-120">Response</span></span>

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
