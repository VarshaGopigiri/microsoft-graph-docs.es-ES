---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Actualizar un registro en una lista de SharePoint
localization_priority: Normal
ms.openlocfilehash: 0b6053f997422f396825aafe058dfd5252986ca1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27872482"
---
# <a name="update-an-item-in-a-list"></a><span data-ttu-id="adf29-102">Actualizar un elemento en una lista</span><span class="sxs-lookup"><span data-stu-id="adf29-102">Update an item in a list</span></span>

> <span data-ttu-id="adf29-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="adf29-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="adf29-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="adf29-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="adf29-105">Actualice las propiedades de un recurso **[listItem][]**.</span><span class="sxs-lookup"><span data-stu-id="adf29-105">Update the properties on a **[listItem][]**.</span></span>

## <a name="permissions"></a><span data-ttu-id="adf29-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="adf29-106">Permissions</span></span>

<span data-ttu-id="adf29-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="adf29-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="adf29-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="adf29-109">Permission type</span></span>      | <span data-ttu-id="adf29-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="adf29-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="adf29-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="adf29-111">Delegated (work or school account)</span></span> | <span data-ttu-id="adf29-112">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="adf29-112">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="adf29-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="adf29-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="adf29-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="adf29-114">Not supported.</span></span>    |
|<span data-ttu-id="adf29-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="adf29-115">Application</span></span> | <span data-ttu-id="adf29-116">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="adf29-116">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="adf29-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="adf29-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items/{item-id}/fields
```

## <a name="optional-request-headers"></a><span data-ttu-id="adf29-118">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="adf29-118">Optional request headers</span></span>

| <span data-ttu-id="adf29-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="adf29-119">Name</span></span>       | <span data-ttu-id="adf29-120">Valor</span><span class="sxs-lookup"><span data-stu-id="adf29-120">Value</span></span> | <span data-ttu-id="adf29-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="adf29-121">Description</span></span>
|:-----------|:------|:--------------------------------------------------------
| <span data-ttu-id="adf29-122">_if-match_</span><span class="sxs-lookup"><span data-stu-id="adf29-122">_if-match_</span></span> | <span data-ttu-id="adf29-123">etag</span><span class="sxs-lookup"><span data-stu-id="adf29-123">etag</span></span>  | <span data-ttu-id="adf29-124">Si se incluye el encabezado de la solicitud y la ETag proporcionada no coincide con la ETag actual del elemento, se devuelve una respuesta `412 Precondition Failed` y el elemento no se actualizará.</span><span class="sxs-lookup"><span data-stu-id="adf29-124">If this request header is included and the eTag provided does not match the current eTag on the item, a `412 Precondition Failed` response is returned and the item will not be updated.</span></span>


## <a name="request-body"></a><span data-ttu-id="adf29-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="adf29-125">Request body</span></span>

<span data-ttu-id="adf29-126">En el cuerpo de la solicitud, proporcione una representación JSON de un recurso [fieldValueSet][] especificando los campos que quiere actualizar.</span><span class="sxs-lookup"><span data-stu-id="adf29-126">In the request body, supply a JSON representation of a [fieldValueSet][] specifying the fields to update.</span></span>

## <a name="example"></a><span data-ttu-id="adf29-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="adf29-127">Example</span></span>

<span data-ttu-id="adf29-128">Aquí tiene un ejemplo que actualiza los campos Color y Quantity (Cantidad) del elemento de lista con los nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="adf29-128">Here is an example that updates the Color and Quantity fields of the list item with new values.</span></span>
<span data-ttu-id="adf29-129">Todos los demás valores de listItem quedan solos.</span><span class="sxs-lookup"><span data-stu-id="adf29-129">All other values on the listItem are left alone.</span></span> 

<!-- { "blockType": "request", "name": "create-listitem", "scopes": "sites.readwrite.all" } -->

```json
PATCH https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items/{item-id}/fields
Content-Type: application/json

{
    "Color": "Fuchsia",
    "Quantity": 934
}
```

## <a name="response"></a><span data-ttu-id="adf29-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="adf29-130">Response</span></span>

<span data-ttu-id="adf29-131">Si se realiza correctamente, este método devuelve un valor [fieldValueSet][] en el cuerpo de la respuesta del elemento de lista actualizado.</span><span class="sxs-lookup"><span data-stu-id="adf29-131">If successful, this method returns a [fieldValueSet][] in the response body for the updated list item.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.listItem", "truncated": true } -->

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
