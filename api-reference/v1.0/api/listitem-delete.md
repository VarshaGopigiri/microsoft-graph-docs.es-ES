---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Eliminar una entrada de una lista de SharePoint
ms.openlocfilehash: 08cca45bc84ea3e9c66709951635efa46d48d237
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032612"
---
# <a name="delete-an-item-from-a-list"></a><span data-ttu-id="2da37-102">Eliminar un elemento de una lista</span><span class="sxs-lookup"><span data-stu-id="2da37-102">Delete an item from a list</span></span>

<span data-ttu-id="2da37-103">Elimina un elemento de un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="2da37-103">Removes an item from a [list][].</span></span>

[list]: ../resources/list.md

## <a name="permissions"></a><span data-ttu-id="2da37-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2da37-105">Permissions</span></span>

<span data-ttu-id="2da37-106">Para eliminar un elemento, al usuario se le debe haber concedido el acceso de escritura de la aplicación al elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="2da37-106">To delete an item, the user must have granted the application write access to the item to be deleted.</span></span>

<span data-ttu-id="2da37-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2da37-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2da37-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2da37-109">Permission type</span></span>      | <span data-ttu-id="2da37-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2da37-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2da37-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2da37-111">Delegated (work or school account)</span></span> | <span data-ttu-id="2da37-112">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2da37-112">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="2da37-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2da37-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2da37-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2da37-114">Not supported.</span></span>    |
|<span data-ttu-id="2da37-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2da37-115">Application</span></span> | <span data-ttu-id="2da37-116">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2da37-116">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2da37-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2da37-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="2da37-118">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="2da37-118">Optional request headers</span></span>

| <span data-ttu-id="2da37-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="2da37-119">Name</span></span>       | <span data-ttu-id="2da37-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2da37-120">Value</span></span> | <span data-ttu-id="2da37-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2da37-121">Description</span></span>
|:-----------|:------|:--------------------------------------------------------
| <span data-ttu-id="2da37-122">_if-match_</span><span class="sxs-lookup"><span data-stu-id="2da37-122">_if-match_</span></span> | <span data-ttu-id="2da37-123">etag</span><span class="sxs-lookup"><span data-stu-id="2da37-123">etag</span></span>  | <span data-ttu-id="2da37-124">Si se incluye este encabezado de la solicitud y la ETag proporcionada no coincide con la etiqueta actual del elemento, se devuelve una respuesta `412 Precondition Failed` y el elemento no se eliminará.</span><span class="sxs-lookup"><span data-stu-id="2da37-124">If this request header is included and the eTag provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span>

## <a name="request-body"></a><span data-ttu-id="2da37-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2da37-125">Request body</span></span>

<span data-ttu-id="2da37-126">No proporcione un cuerpo de solicitud con este método.</span><span class="sxs-lookup"><span data-stu-id="2da37-126">Do not supply a request body with this method.</span></span>

## <a name="example"></a><span data-ttu-id="2da37-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2da37-127">Example</span></span>

<!-- { "blockType": "request", "name": "delete-item-site", "scopes": "files.readwrite sites.readwrite.all" } -->

```http
DELETE https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}
```

## <a name="response"></a><span data-ttu-id="2da37-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2da37-128">Response</span></span>

<span data-ttu-id="2da37-129">Si se ejecuta correctamente, esta llamada devuelve una respuesta `204 No Content` para indicar que el recurso se ha eliminado y no había nada que devolver.</span><span class="sxs-lookup"><span data-stu-id="2da37-129">If successful, this call returns a `204 No Content` response to indicate that resource was deleted and there was nothing to return.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "ListItem/Delete"
} -->
