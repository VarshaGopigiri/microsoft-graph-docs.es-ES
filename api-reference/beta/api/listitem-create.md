---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Crear una entrada en una lista de SharePoint
ms.openlocfilehash: 6f0df86210e164f78e9efa59ba2d43952117681a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089834"
---
# <a name="create-a-new-item-in-a-list"></a><span data-ttu-id="0194c-102">Crear un elemento en una lista</span><span class="sxs-lookup"><span data-stu-id="0194c-102">Create a new item in a list</span></span>

> <span data-ttu-id="0194c-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0194c-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0194c-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0194c-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0194c-105">Cree un [listItem][] en un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="0194c-105">Create a new [listItem][] in a [list][].</span></span>

## <a name="permissions"></a><span data-ttu-id="0194c-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="0194c-106">Permissions</span></span>

<span data-ttu-id="0194c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0194c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0194c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0194c-109">Permission type</span></span>      | <span data-ttu-id="0194c-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0194c-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0194c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0194c-111">Delegated (work or school account)</span></span> | <span data-ttu-id="0194c-112">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0194c-112">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="0194c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0194c-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0194c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0194c-114">Not supported.</span></span>    |
|<span data-ttu-id="0194c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0194c-115">Application</span></span> | <span data-ttu-id="0194c-116">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0194c-116">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0194c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0194c-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items
```

## <a name="request-body"></a><span data-ttu-id="0194c-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0194c-118">Request body</span></span>

<span data-ttu-id="0194c-119">En el cuerpo de la solicitud, proporcione una representación JSON del recurso [listItem][] que quiere crear.</span><span class="sxs-lookup"><span data-stu-id="0194c-119">In the request body, supply a JSON representation of the [listItem][] resource to create.</span></span>

## <a name="example"></a><span data-ttu-id="0194c-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0194c-120">Example</span></span>

<span data-ttu-id="0194c-121">Aquí se muestra un ejemplo de cómo crear un elemento de lista genérica.</span><span class="sxs-lookup"><span data-stu-id="0194c-121">Here is an example of how to create a new generic list item.</span></span>

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

## <a name="response"></a><span data-ttu-id="0194c-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0194c-122">Response</span></span>

<span data-ttu-id="0194c-123">Si se realiza correctamente, este método devuelve un valor [listItem][] en el cuerpo de la respuesta del elemento de lista creado.</span><span class="sxs-lookup"><span data-stu-id="0194c-123">If successful, this method returns a [listItem][] in the response body for the created list item.</span></span>

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

<span data-ttu-id="0194c-124">**Nota:** El objeto Response se trunca para obtener una mayor claridad.</span><span class="sxs-lookup"><span data-stu-id="0194c-124">**Note:** The response object is truncated for clarity.</span></span> <span data-ttu-id="0194c-125">Se devolverán las propiedades predeterminadas de la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="0194c-125">Default properties will be returned from the actual call.</span></span>

[list]: ../resources/list.md
[listItem]: ../resources/listitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Add a new item to a SharePoint list.",
  "keywords": "",
  "section": "documentation",
  "tocPath": "ListItem/Create"
} -->