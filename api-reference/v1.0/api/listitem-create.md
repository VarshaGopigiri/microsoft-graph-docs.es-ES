---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Crear una entrada en una lista de SharePoint
localization_priority: Priority
ms.prod: sharepoint
ms.openlocfilehash: 9a7b81c17f7d0e56bb076fe3e351e8ba9c68e29f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27963370"
---
# <a name="create-a-new-item-in-a-list"></a><span data-ttu-id="2d0cb-102">Crear un elemento en una lista</span><span class="sxs-lookup"><span data-stu-id="2d0cb-102">Create a new item in a list</span></span>

<span data-ttu-id="2d0cb-103">Cree un [listItem][] en un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="2d0cb-103">Create a new [listItem][] in a [list][].</span></span>

## <a name="permissions"></a><span data-ttu-id="2d0cb-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="2d0cb-104">Permissions</span></span>

<span data-ttu-id="2d0cb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2d0cb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2d0cb-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2d0cb-107">Permission type</span></span>      | <span data-ttu-id="2d0cb-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2d0cb-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2d0cb-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2d0cb-109">Delegated (work or school account)</span></span> | <span data-ttu-id="2d0cb-110">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2d0cb-110">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="2d0cb-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2d0cb-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2d0cb-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d0cb-112">Not supported.</span></span>    |
|<span data-ttu-id="2d0cb-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2d0cb-113">Application</span></span> | <span data-ttu-id="2d0cb-114">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2d0cb-114">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2d0cb-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2d0cb-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items
```

## <a name="request-body"></a><span data-ttu-id="2d0cb-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2d0cb-116">Request body</span></span>

<span data-ttu-id="2d0cb-117">En el cuerpo de la solicitud, proporcione una representación JSON del recurso [listItem][] que quiere crear.</span><span class="sxs-lookup"><span data-stu-id="2d0cb-117">In the request body, supply a JSON representation of the [listItem][] resource to create.</span></span>

## <a name="example"></a><span data-ttu-id="2d0cb-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2d0cb-118">Example</span></span>

<span data-ttu-id="2d0cb-119">Aquí se muestra un ejemplo de cómo crear un elemento de lista genérica.</span><span class="sxs-lookup"><span data-stu-id="2d0cb-119">Here is an example of how to create a new generic list item.</span></span>

<!-- { "blockType": "request", "name": "create-listitem", "scopes": "sites.readwrite.all" } -->

```json
POST https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items
Content-Type: application/json

{
  "fields": {
    "Title": "Widget",
    "Color": "Purple",
    "Weight": 32
  }
}
```

## <a name="response"></a><span data-ttu-id="2d0cb-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d0cb-120">Response</span></span>

<span data-ttu-id="2d0cb-121">Si se realiza correctamente, este método devuelve un valor [listItem][] en el cuerpo de la respuesta del elemento de lista creado.</span><span class="sxs-lookup"><span data-stu-id="2d0cb-121">If successful, this method returns a [listItem][] in the response body for the created list item.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.listItem", "truncated": true } -->

```json
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "20",
  "createdDateTime": "2016-08-30T08:26:00Z",
  "createdBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "8606e4d5-d582-4f5f-aeba-7d7c18b20cfd"
    }
  },
  "lastModifiedDateTime": "2016-08-30T08:26:00Z",
  "lastModifiedBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "8606e4d5-d582-4f5f-aeba-7d7c18b20cfd"
    }
  }
}
```

<span data-ttu-id="2d0cb-122">**Nota:** El objeto Response se trunca para obtener una mayor claridad.</span><span class="sxs-lookup"><span data-stu-id="2d0cb-122">**Note:** The response object is truncated for clarity.</span></span> <span data-ttu-id="2d0cb-123">Se devolverán las propiedades predeterminadas de la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="2d0cb-123">Default properties will be returned from the actual call.</span></span>

[list]: ../resources/list.md
[listItem]: ../resources/listitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Add a new item to a SharePoint list.",
  "keywords": "",
  "section": "documentation",
  "tocPath": "ListItem/Create"
} -->
