---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Eliminar una entrada de una lista de SharePoint
ms.openlocfilehash: f091ba2806d0206ca840cb25d9f38a20f42dd2c7
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23269820"
---
# <a name="delete-an-item-from-a-list"></a><span data-ttu-id="79389-102">Eliminar un elemento de una lista</span><span class="sxs-lookup"><span data-stu-id="79389-102">Delete an item from a list</span></span>

<span data-ttu-id="79389-103">Elimina un elemento de un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="79389-103">Removes an item from a [list][].</span></span>

[list]: ../resources/list.md

## <a name="permissions"></a><span data-ttu-id="79389-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="79389-105">Permissions</span></span>

<span data-ttu-id="79389-106">Para eliminar un elemento, al usuario se le debe haber concedido el acceso de escritura de la aplicación al elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="79389-106">To delete an item, the user must have granted the application write access to the item to be deleted.</span></span>

<span data-ttu-id="79389-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="79389-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="79389-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="79389-109">Permission type</span></span>      | <span data-ttu-id="79389-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="79389-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="79389-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="79389-111">Delegated (work or school account)</span></span> | <span data-ttu-id="79389-112">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="79389-112">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="79389-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="79389-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="79389-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79389-114">Not supported.</span></span>    |
|<span data-ttu-id="79389-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="79389-115">Application</span></span> | <span data-ttu-id="79389-116">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="79389-116">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="79389-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79389-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="79389-118">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="79389-118">Optional request headers</span></span>

| <span data-ttu-id="79389-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="79389-119">Name</span></span>       | <span data-ttu-id="79389-120">Valor</span><span class="sxs-lookup"><span data-stu-id="79389-120">Value</span></span> | <span data-ttu-id="79389-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="79389-121">Description</span></span>
|:-----------|:------|:--------------------------------------------------------
| <span data-ttu-id="79389-122">_if-match_</span><span class="sxs-lookup"><span data-stu-id="79389-122">_if-match_</span></span> | <span data-ttu-id="79389-123">etag</span><span class="sxs-lookup"><span data-stu-id="79389-123">etag</span></span>  | <span data-ttu-id="79389-124">Si se incluye este encabezado de la solicitud y la ETag proporcionada no coincide con la etiqueta actual del elemento, se devuelve una respuesta `412 Precondition Failed` y el elemento no se eliminará.</span><span class="sxs-lookup"><span data-stu-id="79389-124">If this request header is included and the eTag provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span>

## <a name="request-body"></a><span data-ttu-id="79389-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="79389-125">Request body</span></span>

<span data-ttu-id="79389-126">No proporcione un cuerpo de solicitud con este método.</span><span class="sxs-lookup"><span data-stu-id="79389-126">Do not supply a request body with this method.</span></span>

## <a name="example"></a><span data-ttu-id="79389-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79389-127">Example</span></span>

<!-- { "blockType": "request", "name": "delete-item-site", "scopes": "files.readwrite sites.readwrite.all" } -->

```http
DELETE https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}
```

## <a name="response"></a><span data-ttu-id="79389-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79389-128">Response</span></span>

<span data-ttu-id="79389-129">Si se ejecuta correctamente, esta llamada devuelve una respuesta `204 No Content` para indicar que el recurso se ha eliminado y no había nada que devolver.</span><span class="sxs-lookup"><span data-stu-id="79389-129">If successful, this call returns a `204 No Content` response to indicate that resource was deleted and there was nothing to return.</span></span>

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
