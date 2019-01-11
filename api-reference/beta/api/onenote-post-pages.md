---
title: Crear página
description: Cree una página de OneNote en la sección predeterminada del bloc de notas predeterminado.
author: Jewan-microsoft
localization_priority: Normal
ms.openlocfilehash: ca5656015a79e5ee684845d12b815cb1ec5f5159
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858992"
---
# <a name="create-page"></a><span data-ttu-id="1d364-103">Crear página</span><span class="sxs-lookup"><span data-stu-id="1d364-103">Create page</span></span>

> <span data-ttu-id="1d364-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d364-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d364-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d364-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1d364-106">Cree una página de OneNote en la sección predeterminada del bloc de notas predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1d364-106">Create a new OneNote page in the default section of the default notebook.</span></span>

<span data-ttu-id="1d364-p102">Para crear una página en una sección diferente del bloc de notas predeterminado, puede utilizar el parámetro de consulta `sectionName`.  Ejemplo: `../onenote/pages?sectionName=My%20section`</span><span class="sxs-lookup"><span data-stu-id="1d364-p102">To create a page in a different section in the default notebook, you can use the `sectionName` query parameter.  Example: `../onenote/pages?sectionName=My%20section`</span></span>

<span data-ttu-id="1d364-p103">La operación `POST /onenote/pages` solo se utiliza para crear páginas en el bloc de notas predeterminado del usuario actual. Si su objetivo son otros blocs de notas, puede [crear páginas en una sección especificada](../api/section-post-pages.md).</span><span class="sxs-lookup"><span data-stu-id="1d364-p103">The `POST /onenote/pages` operation is used only to create pages in the current user's default notebook. If you're targeting other notebooks, you can [create pages in a specified section](../api/section-post-pages.md).</span></span>           
## <a name="permissions"></a><span data-ttu-id="1d364-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="1d364-111">Permissions</span></span>
<span data-ttu-id="1d364-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d364-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d364-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d364-114">Permission type</span></span>      | <span data-ttu-id="1d364-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d364-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1d364-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d364-116">Delegated (work or school account)</span></span> | <span data-ttu-id="1d364-117">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1d364-117">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="1d364-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d364-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1d364-119">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1d364-119">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="1d364-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d364-120">Application</span></span> | <span data-ttu-id="1d364-121">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1d364-121">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="1d364-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d364-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

```http
POST /me/onenote/pages
POST /users/{id | userPrincipalName}/onenote/pages
POST /groups/{id}/onenote/pages
POST /sites/{id}/onenote/pages
```

## <a name="request-headers"></a><span data-ttu-id="1d364-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d364-123">Request headers</span></span>  
| <span data-ttu-id="1d364-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="1d364-124">Name</span></span>       | <span data-ttu-id="1d364-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d364-125">Type</span></span> | <span data-ttu-id="1d364-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d364-126">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="1d364-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="1d364-127">Authorization</span></span>  | <span data-ttu-id="1d364-128">string</span><span class="sxs-lookup"><span data-stu-id="1d364-128">string</span></span>  | <span data-ttu-id="1d364-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1d364-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1d364-131">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1d364-131">Content-Type</span></span> | <span data-ttu-id="1d364-132">string</span><span class="sxs-lookup"><span data-stu-id="1d364-132">string</span></span> | <span data-ttu-id="1d364-p106">`text/html` o `application/xhtml+xml` para el contenido HTML, también para la parte requerida "Presentación" de las solicitudes de varias partes. Las solicitudes de varias partes usan el tipo de contenido `multipart/form-data; boundary=your-boundary`.</span><span class="sxs-lookup"><span data-stu-id="1d364-p106">`text/html` or `application/xhtml+xml` for the HTML content, including for the required "Presentation" part of multipart requests. Multipart requests use the `multipart/form-data; boundary=your-boundary` content type.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1d364-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d364-135">Request body</span></span>
<span data-ttu-id="1d364-136">En el cuerpo de la solicitud, facilite el contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="1d364-136">In the request body, supply the HTML content for the page.</span></span>

<span data-ttu-id="1d364-p107">El cuerpo puede contener código HTML ubicado directamente en el cuerpo de la solicitud o un formato de mensaje de varias partes, como se muestra en el ejemplo. Si quiere enviar datos binarios, debe enviar una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="1d364-p107">The body can contain HTML placed directly in the request body, or it can contain a multipart message format as shown in the example. If you're sending binary data, then you must send a multipart request.</span></span>

## <a name="response"></a><span data-ttu-id="1d364-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d364-139">Response</span></span>

<span data-ttu-id="1d364-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el nuevo objeto [page](../resources/page.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d364-140">If successful, this method returns a `201 Created` response code and the new [page](../resources/page.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1d364-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d364-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1d364-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d364-142">Request</span></span>
<span data-ttu-id="1d364-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d364-143">Here is an example of the request.</span></span>

<span data-ttu-id="1d364-p108">En la ruta `../onenote/pages`, puede usar el parámetro de consulta `sectionName` para crear una página en una sección específica del bloc de notas predeterminado. Ejemplo: `../onenote/pages?sectionName=My%20section`. Si la sección no existe (o ha cambiado de nombre), la API creará una.</span><span class="sxs-lookup"><span data-stu-id="1d364-p108">In the `../onenote/pages` path, you can use the `sectionName` query parameter to create a page in a specific section in the default notebook. Example: `../onenote/pages?sectionName=My%20section`. If the section doesn't exist (or was renamed), the API will create a new section.</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/beta/me/onenote/pages
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
##### <a name="response"></a><span data-ttu-id="1d364-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d364-147">Response</span></span>
<span data-ttu-id="1d364-148">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d364-148">Here is an example of the response.</span></span> <span data-ttu-id="1d364-149">Nota: El objeto de respuesta que se muestra aquí se trunca por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="1d364-149">Note: The response object shown here is truncated for brevity.</span></span> <span data-ttu-id="1d364-150">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d364-150">All of the properties will be returned from an actual call.</span></span>
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
  "content": "content-value",
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
