---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Recuperar elementos de una lista de SharePoint
ms.openlocfilehash: 0935359d2e335cffdee3c09ce7ac97b526d432fe
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031640"
---
# <a name="enumerate-items-in-a-list"></a><span data-ttu-id="bcdb9-102">Enumerar elementos de una lista</span><span class="sxs-lookup"><span data-stu-id="bcdb9-102">Enumerate items in a list</span></span>

<span data-ttu-id="bcdb9-103">Obtenga la colección de [elementos][item] en un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="bcdb9-103">Get the collection of [items][item] in a [list][].</span></span>

[list]: ../resources/list.md
[item]: ../resources/listitem.md

## <a name="permissions"></a><span data-ttu-id="bcdb9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="bcdb9-105">Permissions</span></span>

<span data-ttu-id="bcdb9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bcdb9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bcdb9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bcdb9-108">Permission type</span></span>      | <span data-ttu-id="bcdb9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bcdb9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bcdb9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bcdb9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="bcdb9-111">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bcdb9-111">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="bcdb9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bcdb9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bcdb9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bcdb9-113">Not supported.</span></span>    |
|<span data-ttu-id="bcdb9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bcdb9-114">Application</span></span> | <span data-ttu-id="bcdb9-115">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bcdb9-115">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="bcdb9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bcdb9-116">HTTP request</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items?expand=fields
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items?expand=fields(select=Column1,Column2)
```

## <a name="example"></a><span data-ttu-id="bcdb9-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bcdb9-117">Example</span></span>

#### <a name="request"></a><span data-ttu-id="bcdb9-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bcdb9-118">Request</span></span>

<!-- { "blockType": "request", "name": "get-list-items", "scopes": "sites.read.all" } -->

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items?expand=fields(select=Name,Color,Quantity)
```

#### <a name="response"></a><span data-ttu-id="bcdb9-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcdb9-119">Response</span></span>

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
