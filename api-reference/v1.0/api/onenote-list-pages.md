---
title: Enumerar páginas
description: Recupera una lista de objetos page.
author: jewan-microsoft
localization_priority: Normal
ms.prod: onenote
ms.openlocfilehash: 5a7796bad3afbb7f30b6200f20b667fe53cc0c89
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27955649"
---
# <a name="list-pages"></a><span data-ttu-id="e6adc-103">Enumerar páginas</span><span class="sxs-lookup"><span data-stu-id="e6adc-103">List pages</span></span>

<span data-ttu-id="e6adc-104">Recupera una lista de objetos [page](../resources/page.md).</span><span class="sxs-lookup"><span data-stu-id="e6adc-104">Retrieve a list of [page](../resources/page.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="e6adc-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e6adc-105">Permissions</span></span>
<span data-ttu-id="e6adc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e6adc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e6adc-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6adc-108">Permission type</span></span>      | <span data-ttu-id="e6adc-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6adc-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e6adc-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6adc-110">Delegated (work or school account)</span></span> | <span data-ttu-id="e6adc-111">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e6adc-111">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="e6adc-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6adc-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e6adc-113">Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e6adc-113">Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="e6adc-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6adc-114">Application</span></span> | <span data-ttu-id="e6adc-115">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e6adc-115">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e6adc-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6adc-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/pages
GET /users/{id | userPrincipalName}/onenote/pages
GET /groups/{id}/onenote/pages
GET /sites/{id}/onenote/pages
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e6adc-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e6adc-117">Optional query parameters</span></span>
<span data-ttu-id="e6adc-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6adc-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="e6adc-p102">La consulta predeterminada para páginas devuelve las primeras 20 páginas ordenadas por `lastModifiedTime desc`. Si la consulta predeterminada devuelve más de 20 páginas, la respuesta contendrá un `@odata.nextLink` que podrá usar para revisar el conjunto de resultados. El número máximo de páginas devueltas para una solicitud `top` es de 100.</span><span class="sxs-lookup"><span data-stu-id="e6adc-p102">The default query for pages returns the top 20 pages ordered by `lastModifiedTime desc`. If the default query returns more than 20 pages, the response contains an `@odata.nextLink` that you can use to page through the result set. The maximum number of pages returned for a `top` request is 100.</span></span>

<span data-ttu-id="e6adc-p103">La respuesta predeterminada expande `parentSection` y selecciona las propiedades `id`, `displayName` y `self` de la sección. Los valores válidos de `expand` de las páginas son `parentNotebook` y `parentSection`.</span><span class="sxs-lookup"><span data-stu-id="e6adc-p103">The default response expands `parentSection` and selects the section's `id`, `displayName`, and `self` properties. Valid `expand` values for pages are `parentNotebook` and `parentSection`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e6adc-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6adc-124">Request headers</span></span>
| <span data-ttu-id="e6adc-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="e6adc-125">Name</span></span>       | <span data-ttu-id="e6adc-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6adc-126">Type</span></span> | <span data-ttu-id="e6adc-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6adc-127">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e6adc-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="e6adc-128">Authorization</span></span>  | <span data-ttu-id="e6adc-129">string</span><span class="sxs-lookup"><span data-stu-id="e6adc-129">string</span></span>  | <span data-ttu-id="e6adc-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e6adc-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e6adc-132">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e6adc-132">Accept</span></span> | <span data-ttu-id="e6adc-133">string</span><span class="sxs-lookup"><span data-stu-id="e6adc-133">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="e6adc-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e6adc-134">Request body</span></span>
<span data-ttu-id="e6adc-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e6adc-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e6adc-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6adc-136">Response</span></span>

<span data-ttu-id="e6adc-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [page](../resources/page.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6adc-137">If successful, this method returns a `200 OK` response code and a collection of [page](../resources/page.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e6adc-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6adc-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e6adc-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6adc-139">Request</span></span>
<span data-ttu-id="e6adc-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6adc-140">Here is an example of the request.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/pages
```
##### <a name="response"></a><span data-ttu-id="e6adc-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6adc-141">Response</span></span>
<span data-ttu-id="e6adc-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6adc-142">Here is an example of the response.</span></span> <span data-ttu-id="e6adc-143">Nota: El objeto de respuesta que se muestra aquí se trunca por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="e6adc-143">Note: The response object shown here is truncated for brevity.</span></span> <span data-ttu-id="e6adc-144">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e6adc-144">All of the properties will be returned from an actual call.</span></span>
<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 393

{
  "value": [
    {
      "title": "title-value",
      "createdByAppId": "createdByAppId-value",
      "links": {
        "oneNoteClientUrl": {
          "href": "href-value"
        },
        "oneNoteWebUrl": {
          "href": "href-value"
        }
      },
      "contentUrl": "contentUrl-value",
      "content": "content-value",
      "lastModifiedDateTime": "2016-10-19T10:37:00Z"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List pages",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
