---
title: Enumerar páginas
description: Recupera una lista de objetos page.
ms.openlocfilehash: 9144d443b7fe73cc2720c85adb4199ae6ab9a589
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091198"
---
# <a name="list-pages"></a><span data-ttu-id="e9f04-103">Enumerar páginas</span><span class="sxs-lookup"><span data-stu-id="e9f04-103">List pages</span></span>

> <span data-ttu-id="e9f04-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e9f04-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e9f04-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e9f04-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e9f04-106">Recupera una lista de objetos [page](../resources/page.md).</span><span class="sxs-lookup"><span data-stu-id="e9f04-106">Retrieve a list of [page](../resources/page.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="e9f04-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e9f04-107">Permissions</span></span>
<span data-ttu-id="e9f04-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e9f04-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e9f04-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e9f04-110">Permission type</span></span>      | <span data-ttu-id="e9f04-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e9f04-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e9f04-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e9f04-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e9f04-113">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e9f04-113">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="e9f04-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e9f04-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e9f04-115">Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e9f04-115">Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="e9f04-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e9f04-116">Application</span></span> | <span data-ttu-id="e9f04-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e9f04-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e9f04-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9f04-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/pages
GET /users/{id | userPrincipalName}/onenote/pages
GET /groups/{id}/onenote/pages
GET /sites/{id}/onenote/pages
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e9f04-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e9f04-119">Optional query parameters</span></span>
<span data-ttu-id="e9f04-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9f04-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="e9f04-p103">La consulta predeterminada para páginas devuelve las primeras 20 páginas ordenadas por `lastModifiedTime desc`. Si la consulta predeterminada devuelve más de 20 páginas, la respuesta contendrá un `@odata.nextLink` que podrá usar para revisar el conjunto de resultados. El número máximo de páginas devueltas para una solicitud `top` es de 100.</span><span class="sxs-lookup"><span data-stu-id="e9f04-p103">The default query for pages returns the top 20 pages ordered by `lastModifiedTime desc`. If the default query returns more than 20 pages, the response contains an `@odata.nextLink` that you can use to page through the result set. The maximum number of pages returned for a `top` request is 100.</span></span>

<span data-ttu-id="e9f04-p104">La respuesta predeterminada expande `parentSection` y selecciona las propiedades `id`, `displayName` y `self` de la sección. Los valores válidos de `expand` de las páginas son `parentNotebook` y `parentSection`.</span><span class="sxs-lookup"><span data-stu-id="e9f04-p104">The default response expands `parentSection` and selects the section's `id`, `displayName`, and `self` properties. Valid `expand` values for pages are `parentNotebook` and `parentSection`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e9f04-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9f04-126">Request headers</span></span>
| <span data-ttu-id="e9f04-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="e9f04-127">Name</span></span>       | <span data-ttu-id="e9f04-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9f04-128">Type</span></span> | <span data-ttu-id="e9f04-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9f04-129">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e9f04-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="e9f04-130">Authorization</span></span>  | <span data-ttu-id="e9f04-131">string</span><span class="sxs-lookup"><span data-stu-id="e9f04-131">string</span></span>  | <span data-ttu-id="e9f04-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9f04-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e9f04-134">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e9f04-134">Accept</span></span> | <span data-ttu-id="e9f04-135">string</span><span class="sxs-lookup"><span data-stu-id="e9f04-135">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="e9f04-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e9f04-136">Request body</span></span>
<span data-ttu-id="e9f04-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e9f04-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e9f04-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9f04-138">Response</span></span>

<span data-ttu-id="e9f04-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [page](../resources/page.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9f04-139">If successful, this method returns a `200 OK` response code and a collection of [page](../resources/page.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e9f04-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9f04-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e9f04-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9f04-141">Request</span></span>
<span data-ttu-id="e9f04-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9f04-142">Here is an example of the request.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/me/onenote/pages
```
##### <a name="response"></a><span data-ttu-id="e9f04-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9f04-143">Response</span></span>
<span data-ttu-id="e9f04-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9f04-144">Here is an example of the response.</span></span> <span data-ttu-id="e9f04-145">Nota: El objeto de respuesta que se muestra aquí se trunca por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="e9f04-145">Note: The response object shown here is truncated for brevity.</span></span> <span data-ttu-id="e9f04-146">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e9f04-146">All of the properties will be returned from an actual call.</span></span>
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
      "id": "8fcb5dbc-d5aa-4681-8e31-b001d5168d79",
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