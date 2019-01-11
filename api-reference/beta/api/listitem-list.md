---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Recuperar elementos de una lista de SharePoint
localization_priority: Normal
ms.openlocfilehash: eaecf297e612f8eb832f13751571816dfe950942
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874483"
---
# <a name="enumerate-items-in-a-list"></a><span data-ttu-id="1dd18-102">Enumerar elementos de una lista</span><span class="sxs-lookup"><span data-stu-id="1dd18-102">Enumerate items in a list</span></span>

> <span data-ttu-id="1dd18-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1dd18-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1dd18-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1dd18-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1dd18-105">Obtenga la colección de [elementos][item] en un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="1dd18-105">Get the collection of [items][item] in a [list][].</span></span>

[list]: ../resources/list.md
[item]: ../resources/listitem.md

## <a name="permissions"></a><span data-ttu-id="1dd18-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1dd18-107">Permissions</span></span>

<span data-ttu-id="1dd18-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1dd18-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1dd18-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1dd18-110">Permission type</span></span>      | <span data-ttu-id="1dd18-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1dd18-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1dd18-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1dd18-112">Delegated (work or school account)</span></span> | <span data-ttu-id="1dd18-113">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1dd18-113">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="1dd18-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1dd18-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1dd18-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1dd18-115">Not supported.</span></span>    |
|<span data-ttu-id="1dd18-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1dd18-116">Application</span></span> | <span data-ttu-id="1dd18-117">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1dd18-117">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="1dd18-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1dd18-118">HTTP request</span></span>

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items?expand=fields
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items?expand=fields(select=Column1,Column2)
```

## <a name="example"></a><span data-ttu-id="1dd18-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1dd18-119">Example</span></span>

#### <a name="request"></a><span data-ttu-id="1dd18-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1dd18-120">Request</span></span>

<!-- { "blockType": "request", "name": "get-list-items" } -->

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items?expand=fields(select=Name,Color,Quantity)
```

#### <a name="response"></a><span data-ttu-id="1dd18-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1dd18-121">Response</span></span>

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
