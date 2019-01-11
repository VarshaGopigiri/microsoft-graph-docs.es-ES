---
title: Obtener página
description: Recupere las propiedades y las relaciones de un objeto page.
localization_priority: Normal
ms.openlocfilehash: 117f4d15d676f0be26e75a610d87b2de2581b17a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890828"
---
# <a name="get-page"></a><span data-ttu-id="0cfd5-103">Obtener página</span><span class="sxs-lookup"><span data-stu-id="0cfd5-103">Get page</span></span>

> <span data-ttu-id="0cfd5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0cfd5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0cfd5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0cfd5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0cfd5-106">Recupere las propiedades y las relaciones de un objeto [page](../resources/page.md).</span><span class="sxs-lookup"><span data-stu-id="0cfd5-106">Retrieve the properties and relationships of a [page](../resources/page.md) object.</span></span>

<span data-ttu-id="0cfd5-107">**Obtener información de la página**</span><span class="sxs-lookup"><span data-stu-id="0cfd5-107">**Getting page information**</span></span>

<span data-ttu-id="0cfd5-108">Acceder a los metadatos de una página por el identificador de página:</span><span class="sxs-lookup"><span data-stu-id="0cfd5-108">Access a page's metadata by page identifier:</span></span>

```
GET /me/onenote/pages/{id}
```

<span data-ttu-id="0cfd5-109">**Obtener contenido de la página**</span><span class="sxs-lookup"><span data-stu-id="0cfd5-109">**Getting page content**</span></span>

<span data-ttu-id="0cfd5-110">Puede usar el punto de conexión `content` de la página para obtener el contenido HTML de una página:</span><span class="sxs-lookup"><span data-stu-id="0cfd5-110">You can use the page's `content` endpoint to get the HTML content of a page:</span></span>

```
GET /me/onenote/pages/{id}/content[?includeIDs=true]
GET /me/onenote/pages/{id}/$value[?includeIDs=true]
```

<span data-ttu-id="0cfd5-111">La opción de consulta `includeIDs=true` se usa para [actualizar páginas](../api/page-update.md).</span><span class="sxs-lookup"><span data-stu-id="0cfd5-111">The `includeIDs=true` query option is used to [update pages](../api/page-update.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="0cfd5-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="0cfd5-112">Permissions</span></span>
<span data-ttu-id="0cfd5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0cfd5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0cfd5-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0cfd5-115">Permission type</span></span>      | <span data-ttu-id="0cfd5-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0cfd5-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0cfd5-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0cfd5-117">Delegated (work or school account)</span></span> | <span data-ttu-id="0cfd5-118">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0cfd5-118">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="0cfd5-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0cfd5-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0cfd5-120">Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0cfd5-120">Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="0cfd5-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0cfd5-121">Application</span></span> | <span data-ttu-id="0cfd5-122">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0cfd5-122">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0cfd5-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0cfd5-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/pages/{id}
GET /users/{id | userPrincipalName}/onenote/pages/{id}
GET /groups/{id}/onenote/pages/{id}
GET /sites/{id}/onenote/pages/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="0cfd5-124">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0cfd5-124">Optional query parameters</span></span>
<span data-ttu-id="0cfd5-125">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0cfd5-125">This method supports the `select` and `expand` [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="0cfd5-p103">La respuesta predeterminada expande `parentSection` y selecciona las propiedades `id`, `name` y `self` de la sección. Los valores válidos de `expand` de las páginas son `parentNotebook` y `parentSection`.</span><span class="sxs-lookup"><span data-stu-id="0cfd5-p103">The default response expands `parentSection` and selects the section's `id`, `name`, and `self` properties. Valid `expand` values for pages are `parentNotebook` and `parentSection`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0cfd5-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0cfd5-128">Request headers</span></span>
| <span data-ttu-id="0cfd5-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="0cfd5-129">Name</span></span>       | <span data-ttu-id="0cfd5-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="0cfd5-130">Type</span></span> | <span data-ttu-id="0cfd5-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cfd5-131">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="0cfd5-132">Autorización</span><span class="sxs-lookup"><span data-stu-id="0cfd5-132">Authorization</span></span>  | <span data-ttu-id="0cfd5-133">string</span><span class="sxs-lookup"><span data-stu-id="0cfd5-133">string</span></span>  | <span data-ttu-id="0cfd5-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0cfd5-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0cfd5-136">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0cfd5-136">Accept</span></span> | <span data-ttu-id="0cfd5-137">string</span><span class="sxs-lookup"><span data-stu-id="0cfd5-137">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="0cfd5-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0cfd5-138">Request body</span></span>
<span data-ttu-id="0cfd5-139">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0cfd5-139">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0cfd5-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0cfd5-140">Response</span></span>

<span data-ttu-id="0cfd5-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [page](../resources/page.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0cfd5-141">If successful, this method returns a `200 OK` response code and the [page](../resources/page.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0cfd5-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0cfd5-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0cfd5-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0cfd5-143">Request</span></span>
<span data-ttu-id="0cfd5-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0cfd5-144">Here is an example of the request.</span></span>
 <!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/me/onenote/pages/{id}
```
##### <a name="response"></a><span data-ttu-id="0cfd5-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0cfd5-145">Response</span></span>
<span data-ttu-id="0cfd5-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0cfd5-146">Here is an example of the response.</span></span> <span data-ttu-id="0cfd5-147">Nota: El objeto de respuesta que se muestra aquí se trunca por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="0cfd5-147">Note: The response object shown here is truncated for brevity.</span></span> <span data-ttu-id="0cfd5-148">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0cfd5-148">All of the properties will be returned from an actual call.</span></span>
 <!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 312

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get page",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
