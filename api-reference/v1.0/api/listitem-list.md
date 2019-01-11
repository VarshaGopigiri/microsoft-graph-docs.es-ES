---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Recuperar elementos de una lista de SharePoint
localization_priority: Priority
ms.openlocfilehash: 865d6040aa2a7daaef1ed62c61c45f1e525ded54
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812995"
---
# <a name="enumerate-items-in-a-list"></a><span data-ttu-id="d35c6-102">Enumerar elementos de una lista</span><span class="sxs-lookup"><span data-stu-id="d35c6-102">Enumerate items in a list</span></span>

<span data-ttu-id="d35c6-103">Obtenga la colección de [elementos][item] en un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="d35c6-103">Get the collection of [items][item] in a [list][].</span></span>

[list]: ../resources/list.md
[item]: ../resources/listitem.md

## <a name="permissions"></a><span data-ttu-id="d35c6-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d35c6-105">Permissions</span></span>

<span data-ttu-id="d35c6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d35c6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d35c6-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d35c6-108">Permission type</span></span>      | <span data-ttu-id="d35c6-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d35c6-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d35c6-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d35c6-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d35c6-111">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d35c6-111">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="d35c6-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d35c6-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d35c6-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d35c6-113">Not supported.</span></span>    |
|<span data-ttu-id="d35c6-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d35c6-114">Application</span></span> | <span data-ttu-id="d35c6-115">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d35c6-115">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d35c6-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d35c6-116">HTTP request</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items?expand=fields
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items?expand=fields(select=Column1,Column2)
```

## <a name="example"></a><span data-ttu-id="d35c6-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d35c6-117">Example</span></span>

#### <a name="request"></a><span data-ttu-id="d35c6-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d35c6-118">Request</span></span>

<!-- { "blockType": "request", "name": "get-list-items", "scopes": "sites.read.all" } -->

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items?expand=fields(select=Name,Color,Quantity)
```

#### <a name="response"></a><span data-ttu-id="d35c6-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d35c6-119">Response</span></span>

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
