---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Eliminar una entrada de una lista de SharePoint
ms.openlocfilehash: d0b39a7c0ca69d3bfdd0edb256ac20711dfe5efc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088716"
---
# <a name="delete-an-item-from-a-list"></a><span data-ttu-id="516f4-102">Eliminar un elemento de una lista</span><span class="sxs-lookup"><span data-stu-id="516f4-102">Delete an item from a list</span></span>

> <span data-ttu-id="516f4-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="516f4-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="516f4-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="516f4-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="516f4-105">Elimina un elemento de un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="516f4-105">Removes an item from a [list][].</span></span>

[list]: ../resources/list.md

## <a name="permissions"></a><span data-ttu-id="516f4-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="516f4-107">Permissions</span></span>

<span data-ttu-id="516f4-108">Para eliminar un elemento, al usuario se le debe haber concedido el acceso de escritura de la aplicación al elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="516f4-108">To delete an item, the user must have granted the application write access to the item to be deleted.</span></span>

<span data-ttu-id="516f4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="516f4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="516f4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="516f4-111">Permission type</span></span>      | <span data-ttu-id="516f4-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="516f4-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="516f4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="516f4-113">Delegated (work or school account)</span></span> | <span data-ttu-id="516f4-114">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="516f4-114">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="516f4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="516f4-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="516f4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="516f4-116">Not supported.</span></span>    |
|<span data-ttu-id="516f4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="516f4-117">Application</span></span> | <span data-ttu-id="516f4-118">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="516f4-118">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="516f4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="516f4-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items/{item-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="516f4-120">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="516f4-120">Optional request headers</span></span>

| <span data-ttu-id="516f4-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="516f4-121">Name</span></span>       | <span data-ttu-id="516f4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="516f4-122">Value</span></span> | <span data-ttu-id="516f4-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="516f4-123">Description</span></span>
|:-----------|:------|:--------------------------------------------------------
| <span data-ttu-id="516f4-124">_if-match_</span><span class="sxs-lookup"><span data-stu-id="516f4-124">_if-match_</span></span> | <span data-ttu-id="516f4-125">etag</span><span class="sxs-lookup"><span data-stu-id="516f4-125">etag</span></span>  | <span data-ttu-id="516f4-126">Si se incluye este encabezado de la solicitud y la ETag proporcionada no coincide con la etiqueta actual del elemento, se devuelve una respuesta `412 Precondition Failed` y el elemento no se eliminará.</span><span class="sxs-lookup"><span data-stu-id="516f4-126">If this request header is included and the eTag provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span>

## <a name="request-body"></a><span data-ttu-id="516f4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="516f4-127">Request body</span></span>

<span data-ttu-id="516f4-128">No proporcione un cuerpo de solicitud con este método.</span><span class="sxs-lookup"><span data-stu-id="516f4-128">Do not supply a request body with this method.</span></span>

## <a name="example"></a><span data-ttu-id="516f4-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="516f4-129">Example</span></span>

<!-- { "blockType": "request", "name": "delete-item", "scopes": "files.readwrite" } -->

```http
DELETE https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items/{item-id}
```

## <a name="response"></a><span data-ttu-id="516f4-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="516f4-130">Response</span></span>

<span data-ttu-id="516f4-131">Si se ejecuta correctamente, esta llamada devuelve una respuesta `204 No Content` para indicar que el recurso se ha eliminado y no había nada que devolver.</span><span class="sxs-lookup"><span data-stu-id="516f4-131">If successful, this call returns a `204 No Content` response to indicate that resource was deleted and there was nothing to return.</span></span>

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
