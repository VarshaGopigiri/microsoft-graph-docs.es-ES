---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Crear una entrada en una lista de SharePoint
ms.openlocfilehash: 55a3c52d7afb2a276055cdddfb826ebbcb574ae7
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="create-a-new-item-in-a-list"></a><span data-ttu-id="415a5-102">Crear un elemento en una lista</span><span class="sxs-lookup"><span data-stu-id="415a5-102">Create a new item in a list</span></span>

<span data-ttu-id="415a5-103">Cree un [listItem][] en un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="415a5-103">Create a new [listItem][] in a [list][].</span></span>

## <a name="permissions"></a><span data-ttu-id="415a5-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="415a5-104">Permissions</span></span>

<span data-ttu-id="415a5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="415a5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="415a5-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="415a5-107">Permission type</span></span>      | <span data-ttu-id="415a5-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="415a5-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="415a5-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="415a5-109">Delegated (work or school account)</span></span> | <span data-ttu-id="415a5-110">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="415a5-110">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="415a5-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="415a5-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="415a5-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="415a5-112">Not supported.</span></span>    |
|<span data-ttu-id="415a5-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="415a5-113">Application</span></span> | <span data-ttu-id="415a5-114">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="415a5-114">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="415a5-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="415a5-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items
```

## <a name="request-body"></a><span data-ttu-id="415a5-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="415a5-116">Request body</span></span>

<span data-ttu-id="415a5-117">En el cuerpo de la solicitud, proporcione una representación JSON del recurso [listItem][] que quiere crear.</span><span class="sxs-lookup"><span data-stu-id="415a5-117">In the request body, supply a JSON representation of the [DriveItem][] resource to create.</span></span>

## <a name="example"></a><span data-ttu-id="415a5-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="415a5-118">Example</span></span>

<span data-ttu-id="415a5-119">Aquí se muestra un ejemplo de cómo crear un elemento de lista genérica.</span><span class="sxs-lookup"><span data-stu-id="415a5-119">Here is an example of how to create a new folder.</span></span>

<!-- { "blockType": "request", "name": "create-listitem", "scopes": "sites.readwrite.all" } -->

```json
POST https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items
Content-Type: application/json

{
  "fields": {
    "Title": "Widget",
    "Color": "Purple",
    "Weight": 32
  }
}
```

## <a name="response"></a><span data-ttu-id="415a5-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="415a5-120">Response</span></span>

<span data-ttu-id="415a5-121">Si se realiza correctamente, este método devuelve un valor [listItem][] en el cuerpo de la respuesta del elemento de lista creado.</span><span class="sxs-lookup"><span data-stu-id="415a5-121">If successful, this method returns a [driveItem][] object in the response body for the newly created file.</span></span>

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

<span data-ttu-id="415a5-122">**Nota**: El objeto Response se trunca para obtener una mayor claridad.</span><span class="sxs-lookup"><span data-stu-id="415a5-122">**Note:** The response object is truncated for clarity.</span></span> <span data-ttu-id="415a5-123">Se devolverán las propiedades predeterminadas de la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="415a5-123">All default properties will be returned from the actual call.</span></span>

[list]: ../resources/list.md
[listItem]: ../resources/listItem.md

<!-- {
  "type": "#page.annotation",
  "description": "Add a new item to a SharePoint list.",
  "keywords": "",
  "section": "documentation",
  "tocPath": "ListItem/Create"
} -->
