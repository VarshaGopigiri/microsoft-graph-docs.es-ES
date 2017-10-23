---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Recuperar de elementos de una lista de SharePoint
ms.openlocfilehash: ff414159015b4731b76626e309418c32cb6640d4
ms.sourcegitcommit: 339070a20730bc4d363da7eb346d5f3c1e1d6c3e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="enumerate-items-in-a-list"></a><span data-ttu-id="ab778-102">Enumerar elementos de una lista</span><span class="sxs-lookup"><span data-stu-id="ab778-102">Enumerate items in a list</span></span>

<span data-ttu-id="ab778-103">Obtenga la colección de [elementos][item] en un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="ab778-103">Get the collection of [items][item] in a [list][].</span></span>

[list]: ../resources/list.md
[item]: ../resources/listItem.md

## <a name="permissions"></a><span data-ttu-id="ab778-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ab778-105">Permissions</span></span>

<span data-ttu-id="ab778-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ab778-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ab778-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ab778-108">Permission type</span></span>      | <span data-ttu-id="ab778-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ab778-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ab778-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ab778-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ab778-111">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ab778-111">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="ab778-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ab778-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ab778-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ab778-113">Not supported.</span></span>    |
|<span data-ttu-id="ab778-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ab778-114">Application</span></span> | <span data-ttu-id="ab778-115">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ab778-115">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ab778-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ab778-116">HTTP request</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items?expand=fields
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items?expand=fields(select=Column1,Column2)
```

## <a name="example"></a><span data-ttu-id="ab778-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab778-117">Example</span></span>

#### <a name="request"></a><span data-ttu-id="ab778-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ab778-118">Request</span></span>

<!-- { "blockType": "request", "name": "get-list-items" } -->

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items?expand=fields(select=Name,Color,Quantity)
```

#### <a name="response"></a><span data-ttu-id="ab778-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab778-119">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.listItem)", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
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
  "tocPath": "ListItem/Enumerate"
} -->
