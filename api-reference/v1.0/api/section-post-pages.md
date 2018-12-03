---
title: Crear página
description: Crea una página en la sección especificada.
ms.openlocfilehash: ec4373af59ef8a324e8da8f685fc2ff01bde4a2f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031930"
---
# <a name="create-page"></a><span data-ttu-id="3a06d-103">Crear página</span><span class="sxs-lookup"><span data-stu-id="3a06d-103">Create page</span></span>

<span data-ttu-id="3a06d-104">Crea una [página](../resources/page.md) en la sección especificada.</span><span class="sxs-lookup"><span data-stu-id="3a06d-104">Create a new [page](../resources/page.md) in the specified section.</span></span>

## <a name="permissions"></a><span data-ttu-id="3a06d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="3a06d-105">Permissions</span></span>
<span data-ttu-id="3a06d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3a06d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3a06d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3a06d-108">Permission type</span></span>      | <span data-ttu-id="3a06d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3a06d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3a06d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3a06d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="3a06d-111">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3a06d-111">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="3a06d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3a06d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3a06d-113">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3a06d-113">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="3a06d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3a06d-114">Application</span></span> | <span data-ttu-id="3a06d-115">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3a06d-115">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3a06d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3a06d-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/sections/{id}/pages
POST /users/{id | userPrincipalName}/onenote/sections/{id}/pages
POST /groups/{id}/onenote/sections/{id}/pages
POST /sites/{id}/onenote/sections/{id}/pages
```
## <a name="request-headers"></a><span data-ttu-id="3a06d-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3a06d-117">Request headers</span></span>
| <span data-ttu-id="3a06d-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="3a06d-118">Name</span></span>       | <span data-ttu-id="3a06d-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a06d-119">Type</span></span> | <span data-ttu-id="3a06d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a06d-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="3a06d-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="3a06d-121">Authorization</span></span>  | <span data-ttu-id="3a06d-122">string</span><span class="sxs-lookup"><span data-stu-id="3a06d-122">string</span></span>  | <span data-ttu-id="3a06d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3a06d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="3a06d-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="3a06d-125">Content-Type</span></span> | <span data-ttu-id="3a06d-126">string</span><span class="sxs-lookup"><span data-stu-id="3a06d-126">string</span></span> | <span data-ttu-id="3a06d-p103">`text/html` o `application/xhtml+xml` para el contenido HTML, también para la parte requerida "Presentación" de las solicitudes de varias partes. Las solicitudes de varias partes usan el tipo de contenido `multipart/form-data; boundary=your-boundary`.</span><span class="sxs-lookup"><span data-stu-id="3a06d-p103">`text/html` or `application/xhtml+xml` for the HTML content, including for the required "Presentation" part of multipart requests. Multipart requests use the `multipart/form-data; boundary=your-boundary` content type.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3a06d-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3a06d-129">Request body</span></span>
<span data-ttu-id="3a06d-130">En el cuerpo de la solicitud, facilite el contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="3a06d-130">In the request body, supply the page HTML content.</span></span>

<span data-ttu-id="3a06d-p104">El cuerpo puede contener código HTML ubicado directamente en el cuerpo de la solicitud o un formato de mensaje de varias partes, como se muestra en el ejemplo. Si quiere enviar datos binarios, debe enviar una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="3a06d-p104">The body can contain HTML placed directly in the request body, or it can contain a multipart message format as shown in the example. If you're sending binary data, then you must send a multipart request.</span></span>

## <a name="response"></a><span data-ttu-id="3a06d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a06d-133">Response</span></span>

<span data-ttu-id="3a06d-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el nuevo objeto [page](../resources/page.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a06d-134">If successful, this method returns `201 Created` response code and the new [page](../resources/page.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3a06d-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a06d-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3a06d-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3a06d-136">Request</span></span>
<span data-ttu-id="3a06d-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a06d-137">Here is an example of the request.</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/sections/{id}/pages
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
##### <a name="response"></a><span data-ttu-id="3a06d-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a06d-138">Response</span></span>
<span data-ttu-id="3a06d-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a06d-139">Here is an example of the response.</span></span> <span data-ttu-id="3a06d-140">Nota: El objeto de respuesta que se muestra aquí se trunca por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="3a06d-140">Note: The response object shown here is truncated for brevity.</span></span> <span data-ttu-id="3a06d-141">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3a06d-141">All of the properties will be returned from an actual call.</span></span>
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