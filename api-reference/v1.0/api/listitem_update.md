---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Actualizar un registro en una lista de SharePoint
ms.openlocfilehash: d59167e740d28d832cd9cf6b1175f6b5be1cd729
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23268532"
---
# <a name="update-an-item-in-a-list"></a><span data-ttu-id="a6075-102">Actualizar un elemento en una lista</span><span class="sxs-lookup"><span data-stu-id="a6075-102">Update an item in a list</span></span>

<span data-ttu-id="a6075-103">Actualice las propiedades de un recurso **[listItem][]**.</span><span class="sxs-lookup"><span data-stu-id="a6075-103">Update the properties on a **[listItem][]**.</span></span>

## <a name="permissions"></a><span data-ttu-id="a6075-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="a6075-104">Permissions</span></span>

<span data-ttu-id="a6075-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a6075-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a6075-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a6075-107">Permission type</span></span>      | <span data-ttu-id="a6075-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a6075-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a6075-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a6075-109">Delegated (work or school account)</span></span> | <span data-ttu-id="a6075-110">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a6075-110">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="a6075-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a6075-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a6075-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a6075-112">Not supported.</span></span>    |
|<span data-ttu-id="a6075-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a6075-113">Application</span></span> | <span data-ttu-id="a6075-114">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a6075-114">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a6075-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a6075-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}/fields
```

## <a name="optional-request-headers"></a><span data-ttu-id="a6075-116">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="a6075-116">Optional request headers</span></span>

| <span data-ttu-id="a6075-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="a6075-117">Name</span></span>       | <span data-ttu-id="a6075-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a6075-118">Value</span></span> | <span data-ttu-id="a6075-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6075-119">Description</span></span>
|:-----------|:------|:--------------------------------------------------------
| <span data-ttu-id="a6075-120">_if-match_</span><span class="sxs-lookup"><span data-stu-id="a6075-120">_if-match_</span></span> | <span data-ttu-id="a6075-121">etag</span><span class="sxs-lookup"><span data-stu-id="a6075-121">etag</span></span>  | <span data-ttu-id="a6075-122">Si se incluye el encabezado de la solicitud y la ETag proporcionada no coincide con la ETag actual del elemento, se devuelve una respuesta `412 Precondition Failed` y el elemento no se actualizará.</span><span class="sxs-lookup"><span data-stu-id="a6075-122">If this request header is included and the eTag provided does not match the current eTag on the item, a `412 Precondition Failed` response is returned and the item will not be updated.</span></span>


## <a name="request-body"></a><span data-ttu-id="a6075-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a6075-123">Request body</span></span>

<span data-ttu-id="a6075-124">En el cuerpo de la solicitud, proporcione una representación JSON de un recurso [fieldValueSet][] especificando los campos que quiere actualizar.</span><span class="sxs-lookup"><span data-stu-id="a6075-124">In the request body, supply a JSON representation of a [fieldValueSet][] specifying the fields to update.</span></span>

## <a name="example"></a><span data-ttu-id="a6075-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a6075-125">Example</span></span>

<span data-ttu-id="a6075-126">Aquí tiene un ejemplo que actualiza los campos Color y Quantity (Cantidad) del elemento de lista con los nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="a6075-126">Here is an example that updates the Color and Quantity fields of the list item with new values.</span></span>
<span data-ttu-id="a6075-127">Todos los demás valores de listItem quedan solos.</span><span class="sxs-lookup"><span data-stu-id="a6075-127">All other values on the listItem are left alone.</span></span> 

<!-- { "blockType": "request", "name": "update-listitem", "scopes": "sites.readwrite.all" } -->

```json
PATCH https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}/fields
Content-Type: application/json

{
    "Color": "Fuchsia",
    "Quantity": 934
}
```

## <a name="response"></a><span data-ttu-id="a6075-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6075-128">Response</span></span>

<span data-ttu-id="a6075-129">Si se realiza correctamente, este método devuelve un valor [fieldValueSet][] en el cuerpo de la respuesta del elemento de lista actualizado.</span><span class="sxs-lookup"><span data-stu-id="a6075-129">If successful, this method returns a [fieldValueSet][] in the response body for the updated list item.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.fieldValueSet", "truncated": true } -->

```json
HTTP/1.1 201 Created
Content-type: application/json

{
  "Name": "Widget",
  "Color": "Fuchsia",
  "Quantity": 934
}
```

[fieldValueSet]: ../resources/fieldValueSet.md
[listItem]: ../resources/listItem.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "ListItem/Update"
} -->
