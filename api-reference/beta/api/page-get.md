---
title: Obtener página
description: Recupere las propiedades y las relaciones de un objeto page.
ms.openlocfilehash: 2a7d33caf9f3562d6a59b5a96b38714a7f994b67
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083752"
---
# <a name="get-page"></a><span data-ttu-id="a55bb-103">Obtener página</span><span class="sxs-lookup"><span data-stu-id="a55bb-103">Get page</span></span>

> <span data-ttu-id="a55bb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a55bb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a55bb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a55bb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a55bb-106">Recupere las propiedades y las relaciones de un objeto [page](../resources/page.md).</span><span class="sxs-lookup"><span data-stu-id="a55bb-106">Retrieve the properties and relationships of a [page](../resources/page.md) object.</span></span>

<span data-ttu-id="a55bb-107">**Obtener información de la página**</span><span class="sxs-lookup"><span data-stu-id="a55bb-107">**Getting page information**</span></span>

<span data-ttu-id="a55bb-108">Acceder a los metadatos de una página por el identificador de página:</span><span class="sxs-lookup"><span data-stu-id="a55bb-108">Access a page's metadata by page identifier:</span></span>

```
GET /me/onenote/pages/{id}
```

<span data-ttu-id="a55bb-109">**Obtener contenido de la página**</span><span class="sxs-lookup"><span data-stu-id="a55bb-109">**Getting page content**</span></span>

<span data-ttu-id="a55bb-110">Puede usar el punto de conexión `content` de la página para obtener el contenido HTML de una página:</span><span class="sxs-lookup"><span data-stu-id="a55bb-110">You can use the page's `content` endpoint to get the HTML content of a page:</span></span>

```
GET /me/onenote/pages/{id}/content[?includeIDs=true]
GET /me/onenote/pages/{id}/$value[?includeIDs=true]
```

<span data-ttu-id="a55bb-111">La opción de consulta `includeIDs=true` se usa para [actualizar páginas](../api/page-update.md).</span><span class="sxs-lookup"><span data-stu-id="a55bb-111">The `includeIDs=true` query option is used to [update pages](../api/page-update.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="a55bb-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="a55bb-112">Permissions</span></span>
<span data-ttu-id="a55bb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a55bb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a55bb-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a55bb-115">Permission type</span></span>      | <span data-ttu-id="a55bb-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a55bb-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a55bb-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a55bb-117">Delegated (work or school account)</span></span> | <span data-ttu-id="a55bb-118">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a55bb-118">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="a55bb-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a55bb-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a55bb-120">Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a55bb-120">Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="a55bb-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a55bb-121">Application</span></span> | <span data-ttu-id="a55bb-122">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a55bb-122">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a55bb-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a55bb-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/pages/{id}
GET /users/{id | userPrincipalName}/onenote/pages/{id}
GET /groups/{id}/onenote/pages/{id}
GET /sites/{id}/onenote/pages/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a55bb-124">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a55bb-124">Optional query parameters</span></span>
<span data-ttu-id="a55bb-125">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a55bb-125">This method supports the `select` and `expand` [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="a55bb-p103">La respuesta predeterminada expande `parentSection` y selecciona las propiedades `id`, `name` y `self` de la sección. Los valores válidos de `expand` de las páginas son `parentNotebook` y `parentSection`.</span><span class="sxs-lookup"><span data-stu-id="a55bb-p103">The default response expands `parentSection` and selects the section's `id`, `name`, and `self` properties. Valid `expand` values for pages are `parentNotebook` and `parentSection`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a55bb-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a55bb-128">Request headers</span></span>
| <span data-ttu-id="a55bb-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="a55bb-129">Name</span></span>       | <span data-ttu-id="a55bb-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="a55bb-130">Type</span></span> | <span data-ttu-id="a55bb-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="a55bb-131">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="a55bb-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="a55bb-132">Authorization</span></span>  | <span data-ttu-id="a55bb-133">string</span><span class="sxs-lookup"><span data-stu-id="a55bb-133">string</span></span>  | <span data-ttu-id="a55bb-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a55bb-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a55bb-136">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a55bb-136">Accept</span></span> | <span data-ttu-id="a55bb-137">string</span><span class="sxs-lookup"><span data-stu-id="a55bb-137">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="a55bb-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a55bb-138">Request body</span></span>
<span data-ttu-id="a55bb-139">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a55bb-139">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a55bb-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a55bb-140">Response</span></span>

<span data-ttu-id="a55bb-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [page](../resources/page.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a55bb-141">If successful, this method returns a `200 OK` response code and the [page](../resources/page.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a55bb-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a55bb-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a55bb-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a55bb-143">Request</span></span>
<span data-ttu-id="a55bb-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a55bb-144">Here is an example of the request.</span></span>
 <!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/me/onenote/pages/{id}
```
##### <a name="response"></a><span data-ttu-id="a55bb-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a55bb-145">Response</span></span>
<span data-ttu-id="a55bb-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a55bb-146">Here is an example of the response.</span></span> <span data-ttu-id="a55bb-147">Nota: El objeto de respuesta que se muestra aquí se trunca por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="a55bb-147">Note: The response object shown here is truncated for brevity.</span></span> <span data-ttu-id="a55bb-148">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a55bb-148">All of the properties will be returned from an actual call.</span></span>
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
