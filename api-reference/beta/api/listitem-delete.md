---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Eliminar una entrada de una lista de SharePoint
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 1b61c9359ca349a7f7882a204e8e474aba00444b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968466"
---
# <a name="delete-an-item-from-a-list"></a><span data-ttu-id="26956-102">Eliminar un elemento de una lista</span><span class="sxs-lookup"><span data-stu-id="26956-102">Delete an item from a list</span></span>

> <span data-ttu-id="26956-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="26956-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="26956-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="26956-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="26956-105">Elimina un elemento de un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="26956-105">Removes an item from a [list][].</span></span>

[list]: ../resources/list.md

## <a name="permissions"></a><span data-ttu-id="26956-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="26956-107">Permissions</span></span>

<span data-ttu-id="26956-108">Para eliminar un elemento, al usuario se le debe haber concedido el acceso de escritura de la aplicación al elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="26956-108">To delete an item, the user must have granted the application write access to the item to be deleted.</span></span>

<span data-ttu-id="26956-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="26956-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="26956-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="26956-111">Permission type</span></span>      | <span data-ttu-id="26956-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="26956-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="26956-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="26956-113">Delegated (work or school account)</span></span> | <span data-ttu-id="26956-114">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="26956-114">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="26956-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="26956-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="26956-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="26956-116">Not supported.</span></span>    |
|<span data-ttu-id="26956-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="26956-117">Application</span></span> | <span data-ttu-id="26956-118">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="26956-118">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="26956-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="26956-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items/{item-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="26956-120">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="26956-120">Optional request headers</span></span>

| <span data-ttu-id="26956-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="26956-121">Name</span></span>       | <span data-ttu-id="26956-122">Valor</span><span class="sxs-lookup"><span data-stu-id="26956-122">Value</span></span> | <span data-ttu-id="26956-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="26956-123">Description</span></span>
|:-----------|:------|:--------------------------------------------------------
| <span data-ttu-id="26956-124">_if-match_</span><span class="sxs-lookup"><span data-stu-id="26956-124">_if-match_</span></span> | <span data-ttu-id="26956-125">etag</span><span class="sxs-lookup"><span data-stu-id="26956-125">etag</span></span>  | <span data-ttu-id="26956-126">Si se incluye este encabezado de la solicitud y la ETag proporcionada no coincide con la etiqueta actual del elemento, se devuelve una respuesta `412 Precondition Failed` y el elemento no se eliminará.</span><span class="sxs-lookup"><span data-stu-id="26956-126">If this request header is included and the eTag provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span>

## <a name="request-body"></a><span data-ttu-id="26956-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="26956-127">Request body</span></span>

<span data-ttu-id="26956-128">No proporcione un cuerpo de solicitud con este método.</span><span class="sxs-lookup"><span data-stu-id="26956-128">Do not supply a request body with this method.</span></span>

## <a name="example"></a><span data-ttu-id="26956-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="26956-129">Example</span></span>

<!-- { "blockType": "request", "name": "delete-item", "scopes": "files.readwrite" } -->

```http
DELETE https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items/{item-id}
```

## <a name="response"></a><span data-ttu-id="26956-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="26956-130">Response</span></span>

<span data-ttu-id="26956-131">Si se ejecuta correctamente, esta llamada devuelve una respuesta `204 No Content` para indicar que el recurso se ha eliminado y no había nada que devolver.</span><span class="sxs-lookup"><span data-stu-id="26956-131">If successful, this call returns a `204 No Content` response to indicate that resource was deleted and there was nothing to return.</span></span>

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
