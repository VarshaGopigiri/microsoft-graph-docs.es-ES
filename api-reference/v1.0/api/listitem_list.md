---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Recuperar de elementos de una lista de SharePoint
ms.openlocfilehash: a7f66db11ef201d0ae5afb2cc49887ee10dc89d7
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="enumerate-items-in-a-list"></a><span data-ttu-id="444b7-102">Enumerar elementos de una lista</span><span class="sxs-lookup"><span data-stu-id="444b7-102">Enumerate items in a list</span></span>

<span data-ttu-id="444b7-103">Obtenga la colección de [elementos][item] en un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="444b7-103">Get the collection of [items][item] in a [list][].</span></span>

[list]: ../resources/list.md
[item]: ../resources/listItem.md

## <a name="permissions"></a><span data-ttu-id="444b7-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="444b7-105">Permissions</span></span>

<span data-ttu-id="444b7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="444b7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="444b7-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="444b7-108">Permission type</span></span>      | <span data-ttu-id="444b7-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="444b7-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="444b7-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="444b7-110">Delegated (work or school account)</span></span> | <span data-ttu-id="444b7-111">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="444b7-111">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="444b7-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="444b7-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="444b7-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="444b7-113">Not supported.</span></span>    |
|<span data-ttu-id="444b7-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="444b7-114">Application</span></span> | <span data-ttu-id="444b7-115">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="444b7-115">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="444b7-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="444b7-116">HTTP request</span></span>

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items?expand=fields
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items?expand=fields(select=Column1,Column2)
```

## <a name="example"></a><span data-ttu-id="444b7-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="444b7-117">Example</span></span>

#### <a name="request"></a><span data-ttu-id="444b7-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="444b7-118">Request</span></span>

<!-- { "blockType": "request", "name": "get-list-items" } -->

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items?expand=fields(select=Name,Color,Quantity)
```

#### <a name="response"></a><span data-ttu-id="444b7-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="444b7-119">Response</span></span>

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
