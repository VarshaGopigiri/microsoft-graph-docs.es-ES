---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Actualizar un registro en una lista de SharePoint
localization_priority: Priority
ms.prod: sharepoint
ms.openlocfilehash: a48ad30e2610ea13a5859ce8f4f224dab8af5011
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987149"
---
# <a name="update-an-item-in-a-list"></a><span data-ttu-id="c2db5-102">Actualizar un elemento en una lista</span><span class="sxs-lookup"><span data-stu-id="c2db5-102">Update an item in a list</span></span>

<span data-ttu-id="c2db5-103">Actualice las propiedades de un recurso **[listItem][]**.</span><span class="sxs-lookup"><span data-stu-id="c2db5-103">Update the properties on a **[listItem][]**.</span></span>

## <a name="permissions"></a><span data-ttu-id="c2db5-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="c2db5-104">Permissions</span></span>

<span data-ttu-id="c2db5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c2db5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c2db5-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c2db5-107">Permission type</span></span>      | <span data-ttu-id="c2db5-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c2db5-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c2db5-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c2db5-109">Delegated (work or school account)</span></span> | <span data-ttu-id="c2db5-110">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c2db5-110">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="c2db5-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c2db5-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c2db5-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c2db5-112">Not supported.</span></span>    |
|<span data-ttu-id="c2db5-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c2db5-113">Application</span></span> | <span data-ttu-id="c2db5-114">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c2db5-114">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c2db5-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c2db5-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}/fields
```

## <a name="optional-request-headers"></a><span data-ttu-id="c2db5-116">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="c2db5-116">Optional request headers</span></span>

| <span data-ttu-id="c2db5-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="c2db5-117">Name</span></span>       | <span data-ttu-id="c2db5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c2db5-118">Value</span></span> | <span data-ttu-id="c2db5-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2db5-119">Description</span></span>
|:-----------|:------|:--------------------------------------------------------
| <span data-ttu-id="c2db5-120">_if-match_</span><span class="sxs-lookup"><span data-stu-id="c2db5-120">_if-match_</span></span> | <span data-ttu-id="c2db5-121">etag</span><span class="sxs-lookup"><span data-stu-id="c2db5-121">etag</span></span>  | <span data-ttu-id="c2db5-122">Si se incluye el encabezado de la solicitud y la ETag proporcionada no coincide con la ETag actual del elemento, se devuelve una respuesta `412 Precondition Failed` y el elemento no se actualizará.</span><span class="sxs-lookup"><span data-stu-id="c2db5-122">If this request header is included and the eTag provided does not match the current eTag on the item, a `412 Precondition Failed` response is returned and the item will not be updated.</span></span>


## <a name="request-body"></a><span data-ttu-id="c2db5-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c2db5-123">Request body</span></span>

<span data-ttu-id="c2db5-124">En el cuerpo de la solicitud, proporcione una representación JSON de un recurso [fieldValueSet][] especificando los campos que quiere actualizar.</span><span class="sxs-lookup"><span data-stu-id="c2db5-124">In the request body, supply a JSON representation of a [fieldValueSet][] specifying the fields to update.</span></span>

## <a name="example"></a><span data-ttu-id="c2db5-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2db5-125">Example</span></span>

<span data-ttu-id="c2db5-126">Aquí tiene un ejemplo que actualiza los campos Color y Quantity (Cantidad) del elemento de lista con los nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="c2db5-126">Here is an example that updates the Color and Quantity fields of the list item with new values.</span></span>
<span data-ttu-id="c2db5-127">Todos los demás valores de listItem quedan solos.</span><span class="sxs-lookup"><span data-stu-id="c2db5-127">All other values on the listItem are left alone.</span></span> 

<!-- { "blockType": "request", "name": "update-listitem", "scopes": "sites.readwrite.all" } -->

```json
PATCH https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}/fields
Content-Type: application/json

{
    "Color": "Fuchsia",
    "Quantity": 934
}
```

## <a name="response"></a><span data-ttu-id="c2db5-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2db5-128">Response</span></span>

<span data-ttu-id="c2db5-129">Si se realiza correctamente, este método devuelve un valor [fieldValueSet][] en el cuerpo de la respuesta del elemento de lista actualizado.</span><span class="sxs-lookup"><span data-stu-id="c2db5-129">If successful, this method returns a [fieldValueSet][] in the response body for the updated list item.</span></span>

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

[fieldValueSet]: ../resources/fieldvalueset.md
[listItem]: ../resources/listitem.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "ListItem/Update"
} -->
