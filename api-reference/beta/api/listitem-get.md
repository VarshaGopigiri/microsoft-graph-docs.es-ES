---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Obtener una entrada de una lista de SharePoint
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: ad77cbc3ccaa393cbb9717a7c9cfabef64099d37
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27936273"
---
# <a name="get-an-item-in-a-list"></a><span data-ttu-id="061ac-102">Obtener un elemento en una lista</span><span class="sxs-lookup"><span data-stu-id="061ac-102">Get an item in a list</span></span>

> <span data-ttu-id="061ac-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="061ac-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="061ac-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="061ac-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="061ac-105">Devuelve los metadatos de un [elemento][] en un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="061ac-105">Returns the metadata for an [item][] in a [list][].</span></span>

[list]: ../resources/list.md
[elemento]: ../resources/listitem.md
[item]: ../resources/listitem.md

## <a name="permissions"></a><span data-ttu-id="061ac-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="061ac-108">Permissions</span></span>

<span data-ttu-id="061ac-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="061ac-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="061ac-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="061ac-111">Permission type</span></span>      | <span data-ttu-id="061ac-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="061ac-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="061ac-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="061ac-113">Delegated (work or school account)</span></span> | <span data-ttu-id="061ac-114">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="061ac-114">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="061ac-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="061ac-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="061ac-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="061ac-116">Not supported.</span></span>    |
|<span data-ttu-id="061ac-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="061ac-117">Application</span></span> | <span data-ttu-id="061ac-118">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="061ac-118">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="061ac-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="061ac-119">HTTP request</span></span>

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items/{item-id}
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items/{item-id}?expand=fields
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items/{item-id}?expand=fields(select=Column1,Column2)
```

## <a name="example"></a><span data-ttu-id="061ac-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="061ac-120">Example</span></span>

##### <a name="request"></a><span data-ttu-id="061ac-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="061ac-121">Request</span></span>

<!-- { "blockType": "request", "name": "get-list-item" } -->

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items/{item-id}?expand=fields
```

##### <a name="response"></a><span data-ttu-id="061ac-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="061ac-122">Response</span></span>

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
