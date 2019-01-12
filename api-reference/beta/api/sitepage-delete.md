---
author: rahmit
ms.author: rahmit
ms.date: 05/07/2018
title: Eliminar una página de un sitio de SharePoint
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: b4ac336999484f6af97e41d08caa926fae4c055f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950028"
---
# <a name="delete-page-from-the-site-pages-list-of-a-site"></a><span data-ttu-id="42fac-102">Eliminar la página de la lista de las páginas del sitio de un sitio</span><span class="sxs-lookup"><span data-stu-id="42fac-102">Delete page from the site pages list of a site</span></span>

> <span data-ttu-id="42fac-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="42fac-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="42fac-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="42fac-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="42fac-105">Quita un [sitePage][] de las páginas de sitio [lista][] en un [sitio][].</span><span class="sxs-lookup"><span data-stu-id="42fac-105">Removes a [sitePage][] from the site pages [list][] in a [site][].</span></span>

[sitePage]: ../resources/sitepage.md
[list]: ../resources/list.md
[site]: ../resources/site.md

## <a name="permissions"></a><span data-ttu-id="42fac-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="42fac-109">Permissions</span></span>

<span data-ttu-id="42fac-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="42fac-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

><span data-ttu-id="42fac-112">**Nota:** Para eliminar un elemento, el usuario debe disponer de acceso de escritura de aplicación en el elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="42fac-112">**Note:** To delete an item, the user must have granted the application write access to the item to be deleted.</span></span>

|<span data-ttu-id="42fac-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="42fac-113">Permission type</span></span>      | <span data-ttu-id="42fac-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="42fac-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="42fac-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="42fac-115">Delegated (work or school account)</span></span> | <span data-ttu-id="42fac-116">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="42fac-116">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="42fac-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="42fac-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="42fac-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="42fac-118">Not supported.</span></span>    |
|<span data-ttu-id="42fac-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="42fac-119">Application</span></span> | <span data-ttu-id="42fac-120">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="42fac-120">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="42fac-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="42fac-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /sites/{site-id}/pages/{page-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="42fac-122">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="42fac-122">Optional request headers</span></span>

| <span data-ttu-id="42fac-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="42fac-123">Name</span></span>       | <span data-ttu-id="42fac-124">Valor</span><span class="sxs-lookup"><span data-stu-id="42fac-124">Value</span></span> | <span data-ttu-id="42fac-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="42fac-125">Description</span></span>
|:-----------|:------|:--------------------------------------------------------
| <span data-ttu-id="42fac-126">_if-match_</span><span class="sxs-lookup"><span data-stu-id="42fac-126">_if-match_</span></span> | <span data-ttu-id="42fac-127">etag</span><span class="sxs-lookup"><span data-stu-id="42fac-127">etag</span></span>  | <span data-ttu-id="42fac-128">Si se incluye este encabezado de la solicitud y la ETag proporcionada no coincide con la etiqueta actual del elemento, se devuelve una respuesta `412 Precondition Failed` y el elemento no se eliminará.</span><span class="sxs-lookup"><span data-stu-id="42fac-128">If this request header is included and the eTag provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span>

## <a name="request-body"></a><span data-ttu-id="42fac-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="42fac-129">Request body</span></span>

<span data-ttu-id="42fac-130">No proporcione un cuerpo de solicitud con este método.</span><span class="sxs-lookup"><span data-stu-id="42fac-130">Do not supply a request body with this method.</span></span>
<!-- TODO: should we provide a URL to recover/undelete the file, if one exists? -->

## <a name="response"></a><span data-ttu-id="42fac-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42fac-131">Response</span></span>

<span data-ttu-id="42fac-132">Si tiene éxito, esta llamada devuelve una `204 No Content` respuesta para indicar que el recurso se eliminó y no había nada para devolver.</span><span class="sxs-lookup"><span data-stu-id="42fac-132">If successful, this call returns a `204 No Content` response to indicate that the resource was deleted and there was nothing to return.</span></span>

## <a name="example"></a><span data-ttu-id="42fac-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="42fac-133">Example</span></span>

<!-- { "blockType": "request", "name": "delete-page", "scopes": "files.readwrite sites.readwrite.all" } -->

##### <a name="request"></a><span data-ttu-id="42fac-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="42fac-134">Request</span></span>

```http
DELETE /sites/{site-id}/pages/{page-id}
```
##### <a name="response"></a><span data-ttu-id="42fac-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42fac-135">Response</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```

<!-- {
  "type": "#page.annotation",
  "description": "Delete a page in the SitePages list in a site.",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Pages/Delete"
} -->
