---
title: Crear página
description: Crea una página en la sección especificada.
ms.openlocfilehash: c3fead813e64ba6bc1b806601a2f02a0adade706
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090635"
---
# <a name="create-page"></a><span data-ttu-id="b670f-103">Crear página</span><span class="sxs-lookup"><span data-stu-id="b670f-103">Create page</span></span>

> <span data-ttu-id="b670f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b670f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b670f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b670f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b670f-106">Crea una [página](../resources/page.md) en la sección especificada.</span><span class="sxs-lookup"><span data-stu-id="b670f-106">Create a new [page](../resources/page.md) in the specified section.</span></span>
## <a name="permissions"></a><span data-ttu-id="b670f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b670f-107">Permissions</span></span>
<span data-ttu-id="b670f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b670f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b670f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b670f-110">Permission type</span></span>      | <span data-ttu-id="b670f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b670f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b670f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b670f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b670f-113">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b670f-113">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="b670f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b670f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b670f-115">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b670f-115">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="b670f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b670f-116">Application</span></span> | <span data-ttu-id="b670f-117">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b670f-117">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b670f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b670f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/sections/{id}/pages
POST /users/{id | userPrincipalName}/onenote/sections/{id}/pages
POST /groups/{id}/onenote/sections/{id}/pages
POST /sites/{id}/onenote/sections/{id}/pages
```
## <a name="request-headers"></a><span data-ttu-id="b670f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b670f-119">Request headers</span></span>
| <span data-ttu-id="b670f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b670f-120">Name</span></span>       | <span data-ttu-id="b670f-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="b670f-121">Type</span></span> | <span data-ttu-id="b670f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b670f-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="b670f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b670f-123">Authorization</span></span>  | <span data-ttu-id="b670f-124">string</span><span class="sxs-lookup"><span data-stu-id="b670f-124">string</span></span>  | <span data-ttu-id="b670f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b670f-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b670f-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b670f-127">Content-Type</span></span> | <span data-ttu-id="b670f-128">string</span><span class="sxs-lookup"><span data-stu-id="b670f-128">string</span></span> | <span data-ttu-id="b670f-p104">`text/html` o `application/xhtml+xml` para el contenido HTML, también para la parte requerida "Presentación" de las solicitudes de varias partes. Las solicitudes de varias partes usan el tipo de contenido `multipart/form-data; boundary=your-boundary`.</span><span class="sxs-lookup"><span data-stu-id="b670f-p104">`text/html` or `application/xhtml+xml` for the HTML content, including for the required "Presentation" part of multipart requests. Multipart requests use the `multipart/form-data; boundary=your-boundary` content type.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b670f-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b670f-131">Request body</span></span>
<span data-ttu-id="b670f-132">En el cuerpo de la solicitud, facilite el contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="b670f-132">In the request body, supply the page HTML content.</span></span>

<span data-ttu-id="b670f-p105">El cuerpo puede contener código HTML ubicado directamente en el cuerpo de la solicitud o un formato de mensaje de varias partes, como se muestra en el ejemplo. Si quiere enviar datos binarios, debe enviar una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="b670f-p105">The body can contain HTML placed directly in the request body, or it can contain a multipart message format as shown in the example. If you're sending binary data, then you must send a multipart request.</span></span>

## <a name="response"></a><span data-ttu-id="b670f-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b670f-135">Response</span></span>

<span data-ttu-id="b670f-136">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el nuevo objeto [page](../resources/page.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b670f-136">If successful, this method returns `201 Created` response code and the new [page](../resources/page.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b670f-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b670f-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b670f-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b670f-138">Request</span></span>
<span data-ttu-id="b670f-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b670f-139">Here is an example of the request.</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/beta/me/onenote/sections/{id}/pages
Content-length: 312
Content-type: multipart/form-data; boundary=MyPartBoundary198374

--MyPartBoundary198374
Content-Disposition:form-data; name="Presentation"
Content-Type:text/html

<!DOCTYPE html>
<html>
  <head>
    <title>A page with <i>rendered</i> images and an <b>attached</b> file</title>
    <meta name="created" content="2015-07-22T09:00:00-08:00" />
  </head>
  <body>
    <p>Here's an image from an online source:</p>
    <img src="https://..." alt="an image on the page" width="500" />
    <p>Here's an image uploaded as binary data:</p>
    <img src="name:imageBlock1" alt="an image on the page" width="300" />
    <p>Here's a file attachment:</p>
    <object data-attachment="FileName.pdf" data="name:fileBlock1" type="application/pdf" />
  </body>
</html>

--MyPartBoundary198374
Content-Disposition:form-data; name="imageBlock1"
Content-Type:image/jpeg

... binary image data ...

--MyPartBoundary198374
Content-Disposition:form-data; name="fileBlock1"
Content-Type:application/pdf

... binary file data ...

--MyPartBoundary198374--
```
##### <a name="response"></a><span data-ttu-id="b670f-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b670f-140">Response</span></span>
<span data-ttu-id="b670f-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b670f-141">Here is an example of the response.</span></span> <span data-ttu-id="b670f-142">Nota: El objeto de respuesta que se muestra aquí se trunca por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="b670f-142">Note: The response object shown here is truncated for brevity.</span></span> <span data-ttu-id="b670f-143">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b670f-143">All of the properties will be returned from an actual call.</span></span>
<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 312

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
  "lastModifiedDateTime": "2016-10-19T10:37:00Z"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Page",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
