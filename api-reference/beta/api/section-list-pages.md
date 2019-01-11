---
title: Enumerar páginas
description: Recupera una página de objetos page desde la sección especificada.
localization_priority: Normal
ms.openlocfilehash: 9e0dea1f9a786734222dbc4c93b059e22d4322bc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27813023"
---
# <a name="list-pages"></a><span data-ttu-id="0074e-103">Enumerar páginas</span><span class="sxs-lookup"><span data-stu-id="0074e-103">List pages</span></span>

> <span data-ttu-id="0074e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0074e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0074e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0074e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0074e-106">Recupera una página de objetos [page](../resources/page.md) desde la sección especificada.</span><span class="sxs-lookup"><span data-stu-id="0074e-106">Retrieve a list of [page](../resources/page.md) objects from the specified section.</span></span>
## <a name="permissions"></a><span data-ttu-id="0074e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0074e-107">Permissions</span></span>
<span data-ttu-id="0074e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0074e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0074e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0074e-110">Permission type</span></span>      | <span data-ttu-id="0074e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0074e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0074e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0074e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0074e-113">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0074e-113">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="0074e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0074e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0074e-115">Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0074e-115">Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="0074e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0074e-116">Application</span></span> | <span data-ttu-id="0074e-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0074e-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0074e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0074e-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sections/{id}/pages
GET /users/{id | userPrincipalName}/onenote/sections/{id}/pages
GET /groups/{id}/onenote/sections/{id}/pages
GET /sites/{id}/onenote/sections/{id}/pages
```
## <a name="optional-query-parameters"></a><span data-ttu-id="0074e-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0074e-119">Optional query parameters</span></span>
<span data-ttu-id="0074e-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0074e-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="0074e-p103">La consulta predeterminada para páginas devuelve las primeras 20 páginas ordenadas por `lastModifiedTime desc`. Si la consulta predeterminada devuelve más de 20 páginas, la respuesta contendrá un `@odata.nextLink` que podrá usar para revisar el conjunto de resultados. El número máximo de páginas devueltas para una solicitud `top` es de 100.</span><span class="sxs-lookup"><span data-stu-id="0074e-p103">The default query for pages returns the top 20 pages ordered by `lastModifiedTime desc`. If the default query returns more than 20 pages, the response contains an `@odata.nextLink` that you can use to page through the result set. The maximum number of pages returned for a `top` request is 100.</span></span>

<span data-ttu-id="0074e-p104">La respuesta predeterminada expande `parentSection` y selecciona las propiedades `id`, `name` y `self` de la sección. Los valores válidos de `expand` de las páginas son `parentNotebook` y `parentSection`.</span><span class="sxs-lookup"><span data-stu-id="0074e-p104">The default response expands `parentSection` and selects the section's `id`, `name`, and `self` properties. Valid `expand` values for pages are `parentNotebook` and `parentSection`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0074e-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0074e-126">Request headers</span></span>
| <span data-ttu-id="0074e-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="0074e-127">Name</span></span>       | <span data-ttu-id="0074e-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="0074e-128">Type</span></span> | <span data-ttu-id="0074e-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="0074e-129">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="0074e-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="0074e-130">Authorization</span></span>  | <span data-ttu-id="0074e-131">string</span><span class="sxs-lookup"><span data-stu-id="0074e-131">string</span></span>  | <span data-ttu-id="0074e-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0074e-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0074e-134">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0074e-134">Accept</span></span> | <span data-ttu-id="0074e-135">string</span><span class="sxs-lookup"><span data-stu-id="0074e-135">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="0074e-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0074e-136">Request body</span></span>
<span data-ttu-id="0074e-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0074e-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0074e-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0074e-138">Response</span></span>

<span data-ttu-id="0074e-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [page](../resources/page.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0074e-139">If successful, this method returns a `200 OK` response code and a collection of [page](../resources/page.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0074e-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0074e-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0074e-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0074e-141">Request</span></span>
<span data-ttu-id="0074e-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0074e-142">Here is an example of the request.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/me/onenote/sections/{id}/pages
```
##### <a name="response"></a><span data-ttu-id="0074e-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0074e-143">Response</span></span>
<span data-ttu-id="0074e-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0074e-144">Here is an example of the response.</span></span> <span data-ttu-id="0074e-145">Nota: El objeto de respuesta que se muestra aquí se trunca por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="0074e-145">Note: The response object shown here is truncated for brevity.</span></span> <span data-ttu-id="0074e-146">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0074e-146">All of the properties will be returned from an actual call.</span></span>
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
