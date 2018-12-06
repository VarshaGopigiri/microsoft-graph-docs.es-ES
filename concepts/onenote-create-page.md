---
title: Crear páginas de OneNote
description: " Blocs de notas de empresa en Office 365"
ms.openlocfilehash: 73ff77b16aaf5927bf28d009ca8ee1274f954c06
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092957"
---
# <a name="create-onenote-pages"></a><span data-ttu-id="97c57-103">Crear páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="97c57-103">Create OneNote pages</span></span>

<span data-ttu-id="97c57-104">**Se aplica a**: Blocs de notas para consumidores de OneDrive | Blocs de notas empresariales de Office 365</span><span class="sxs-lookup"><span data-stu-id="97c57-104">**Applies to**: Consumer notebooks on OneDrive | Enterprise notebooks on Office 365</span></span>

<span data-ttu-id="97c57-105">Para crear una página de OneNote, envíe una solicitud POST al punto de conexión *pages*.</span><span class="sxs-lookup"><span data-stu-id="97c57-105">To create a OneNote page, you send a POST request to a *pages* endpoint.</span></span> <span data-ttu-id="97c57-106">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="97c57-106">For example:</span></span>

`POST ../notes/sections/{id}/pages`

<br/>

<span data-ttu-id="97c57-107">Envíe el código HTML que define la página en el cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="97c57-107">Send the HTML that defines the page in the message body.</span></span> <span data-ttu-id="97c57-108">Si la solicitud se completa correctamente, Microsoft Graph devuelve un código de estado HTTP 201.</span><span class="sxs-lookup"><span data-stu-id="97c57-108">If the request is successful, Microsoft Graph returns a 201 HTTP status code.</span></span>


> <span data-ttu-id="97c57-109">**Nota:** Para obtener información sobre las solicitudes POST que puede enviar para crear secciones, grupos de secciones y blocs de notas, vea la [referencia de REST interactiva](https://dev.onenote.com/docs).</span><span class="sxs-lookup"><span data-stu-id="97c57-109">**Note:** To learn about the POST requests you can send to create sections, section groups, and notebooks, see our [interactive REST reference](https://dev.onenote.com/docs).</span></span>


<a name="request-uri"></a>

## <a name="construct-the-request-uri"></a><span data-ttu-id="97c57-110">Crear el URI de la solicitud</span><span class="sxs-lookup"><span data-stu-id="97c57-110">Construct the request URI</span></span>

<span data-ttu-id="97c57-111">Para crear el URI de la solicitud POST, empiece con la dirección URL raíz del servicio:</span><span class="sxs-lookup"><span data-stu-id="97c57-111">To construct the POST request URI, start with the service root URL:</span></span>

`https://graph.microsoft.com/v1.0/me/onenote`

<br/>

<span data-ttu-id="97c57-112">Después, anexe el punto de conexión *pages*:</span><span class="sxs-lookup"><span data-stu-id="97c57-112">Then append the *pages* endpoint:</span></span>

- <span data-ttu-id="97c57-113">**Crear una página en cualquier sección (especificado por el nombre de sección)**</span><span class="sxs-lookup"><span data-stu-id="97c57-113">**Create a page in any section (specified by section name)**</span></span><br/><br/>`.../pages?sectionName=DefaultSection`

- <span data-ttu-id="97c57-114">**Crear una página en cualquier sección (especificado por el id.)**</span><span class="sxs-lookup"><span data-stu-id="97c57-114">**Create a page in any section (specified by ID)**</span></span><br/><br/>`.../sections/{section-id}/pages` 

<span data-ttu-id="97c57-115">Si va a crear páginas en el bloc de notas personal del usuario, Microsoft Graph también proporciona puntos de conexión que puede usar para crear páginas en el bloc de notas predeterminado:</span><span class="sxs-lookup"><span data-stu-id="97c57-115">If you're creating pages in the user's personal notebook, Microsoft Graph also provides endpoints you can use to create pages in the default notebook:</span></span>

- <span data-ttu-id="97c57-116">**Crear una página de OneNote en la sección predeterminada del bloc de notas predeterminado**</span><span class="sxs-lookup"><span data-stu-id="97c57-116">**Create a page in the default section of the default notebook**</span></span><br/><br/>`../pages` 



<span data-ttu-id="97c57-117">La URI de la solicitud completa tendrá un aspecto similar a uno de estos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="97c57-117">Your full request URI will look like one of these examples:</span></span>

- `https://graph.microsoft.com/v1.0/me/onenote/sections/{id}/pages`
- `https://graph.microsoft.com/v1.0/me/onenote/pages?sectionName=Homework`

<span data-ttu-id="97c57-118">Obtenga más información sobre la [URL de raíz del servicio](/graph/api/resources/onenote-api-overview?view=graph-rest-1.0#root-url).</span><span class="sxs-lookup"><span data-stu-id="97c57-118">Learn more about the [service root URL](/graph/api/resources/onenote-api-overview?view=graph-rest-1.0#root-url).</span></span>

<a name="post-pages-section-name"></a>

### <a name="using-the-sectionname-url-parameter"></a><span data-ttu-id="97c57-119">Usar el parámetro de URL *sectionName*</span><span class="sxs-lookup"><span data-stu-id="97c57-119">Using the *sectionName* URL parameter</span></span>

<span data-ttu-id="97c57-120">Las reglas siguientes se aplican al usar el parámetro *sectionName* para crear una página en una sección con nombre del bloc de notas predeterminado:</span><span class="sxs-lookup"><span data-stu-id="97c57-120">The following rules apply when using the *sectionName* parameter to create a page in a named section in the default notebook:</span></span>

- <span data-ttu-id="97c57-121">Solo se puede hacer referencia a las secciones de nivel superior (no a las secciones dentro de grupos de secciones).</span><span class="sxs-lookup"><span data-stu-id="97c57-121">Only top-level sections can be referenced (not sections within section groups).</span></span>

- <span data-ttu-id="97c57-122">Si en el bloc de notas predeterminado no existe una sección con el nombre especificado, la API la creará.</span><span class="sxs-lookup"><span data-stu-id="97c57-122">If a section with the specified name doesn't exist in the default notebook, the API creates it.</span></span> <span data-ttu-id="97c57-123">Los caracteres siguientes no pueden usarse en los nombres de sección: `? * \ / : < > | & # " % ~`</span><span class="sxs-lookup"><span data-stu-id="97c57-123">These characters are not allowed for section names: `? * \ / : < > | & # " % ~`</span></span>

- <span data-ttu-id="97c57-124">Los nombres de sección no distinguen mayúsculas de minúsculas, pero el uso de mayúsculas se conserva al crear las secciones.</span><span class="sxs-lookup"><span data-stu-id="97c57-124">Section names are case-insensitive for matching, but case is preserved when sections are created.</span></span> <span data-ttu-id="97c57-125">Por lo tanto, “Mi nueva sección” se mostrará de esa forma, pero “mi nueva sección” también coincidirá en las publicaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="97c57-125">So "My New Section" will display like that, but "my new section" would also match on subsequent posts.</span></span>

- <span data-ttu-id="97c57-126">Los nombres de sección necesitan tener el formato de codificación URL.</span><span class="sxs-lookup"><span data-stu-id="97c57-126">Section names must be URL-encoded.</span></span> <span data-ttu-id="97c57-127">Por ejemplo, los espacios tienen que codificarse como *%20*.</span><span class="sxs-lookup"><span data-stu-id="97c57-127">For example, spaces must be encoded as *%20*.</span></span>

- <span data-ttu-id="97c57-128">El parámetro *sectionName* solo es válido con la ruta `../notes/pages` (pero no con `../notes/sections/{id}/pages`).</span><span class="sxs-lookup"><span data-stu-id="97c57-128">The *sectionName* parameter is valid only with the `../notes/pages` route (not `../notes/sections/{id}/pages`).</span></span>

<span data-ttu-id="97c57-129">Como se crearán secciones si no existen, es seguro usar esta llamada con todas las páginas que cree la aplicación.</span><span class="sxs-lookup"><span data-stu-id="97c57-129">Because sections are created if they don't exist, it's safe to use this call with every page your app creates.</span></span> <span data-ttu-id="97c57-130">Aunque los usuarios pueden cambiar el nombre de las secciones, la API creará una sección con el nombre de sección que especifique.</span><span class="sxs-lookup"><span data-stu-id="97c57-130">Users might rename sections, but the API will create a new section with the section name that you supply.</span></span> 

> <span data-ttu-id="97c57-131">**Nota:** Los vínculos devueltos por la API para las páginas en una sección con un nombre cambiado también llegarán a las páginas anteriores.</span><span class="sxs-lookup"><span data-stu-id="97c57-131">**Note:** The links returned by the API for pages in a renamed section will still reach those older pages.</span></span> 


<a name="message-body"></a>

## <a name="construct-the-message-body"></a><span data-ttu-id="97c57-132">Crear el cuerpo del mensaje</span><span class="sxs-lookup"><span data-stu-id="97c57-132">Construct the message body</span></span>

<span data-ttu-id="97c57-133">El código HTML que define el contenido de la página se denomina *HTML de entrada*.</span><span class="sxs-lookup"><span data-stu-id="97c57-133">The HTML that defines page content is called *input HTML*.</span></span> <span data-ttu-id="97c57-134">El código HTML de entrada admite un [subconjunto de HTML y CSS estándar](#supported-html-and-css-for-onenote-pages), además de atributos personalizados.</span><span class="sxs-lookup"><span data-stu-id="97c57-134">Input HTML supports a [subset of standard HTML and CSS](#supported-html-and-css-for-onenote-pages), with the addition of custom attributes.</span></span> <span data-ttu-id="97c57-135">(Los atributos personalizados, como **data-id** y **data-render-src**, se describen en [HTML de entrada y salida](onenote-input-output-html.md)).</span><span class="sxs-lookup"><span data-stu-id="97c57-135">(Custom attributes, like **data-id** and **data-render-src**, are described in [Input and output HTML](onenote-input-output-html.md).)</span></span> 

<span data-ttu-id="97c57-136">Envíe el código HTML de entrada en el cuerpo del mensaje de la solicitud POST.</span><span class="sxs-lookup"><span data-stu-id="97c57-136">Send the input HTML in the message body of the POST request.</span></span> <span data-ttu-id="97c57-137">Puede enviar el código HTML de entrada directamente en el cuerpo del mensaje con el tipo de contenido `application/xhtml+xml` o `text/html`, o bien puede enviarlo en el elemento “Presentación” de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="97c57-137">You can send the input HTML directly in the message body using the  `application/xhtml+xml` or `text/html` content type, or you can send it in the "Presentation" part of a multipart request.</span></span> 

<span data-ttu-id="97c57-138">En el ejemplo siguiente, se envía el código HTML de entrada directamente en el cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="97c57-138">The following example sends the input HTML directly in the message body.</span></span>

```html
POST https://graph.microsoft.com/v1.0/me/onenote/pages
Authorization: Bearer {token}
Content-Type: application/xhtml+xml

<!DOCTYPE html>
<html>
  <head>
    <title>A page with a block of HTML</title>
    <meta name="created" content="2015-07-22T09:00:00-08:00" />
  </head>
  <body>
    <p>This page contains some <i>formatted</i> <b>text</b> and an image.</p>
    <img src="https://..." alt="an image on the page" width="500" />
  </body>
</html>
```

<br/>

<span data-ttu-id="97c57-139">Si envía datos binarios, tendrá que usar una [solicitud de varias partes](#example-request).</span><span class="sxs-lookup"><span data-stu-id="97c57-139">If you're sending binary data, you must use a [multipart request](#example-request).</span></span> 

> <span data-ttu-id="97c57-140">**Nota:** Para simplificar la programación y la coherencia en la aplicación, puede usar solicitudes de varias partes para crear todas las páginas.</span><span class="sxs-lookup"><span data-stu-id="97c57-140">**Note:** To simplify programming and consistency in your app, you can use multipart requests to create all pages.</span></span> <span data-ttu-id="97c57-141">Le recomendamos que use una biblioteca para crear mensajes de varias partes.</span><span class="sxs-lookup"><span data-stu-id="97c57-141">It's a good idea to use a library to construct multipart messages.</span></span> <span data-ttu-id="97c57-142">Esto reduce el riesgo de crear cargas de trabajo con formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="97c57-142">This reduces the risk of creating malformed payloads.</span></span>


<a name="input-html-rules"></a>

### <a name="requirements-and-limitations-for-input-html-in-post-pages-requests"></a><span data-ttu-id="97c57-143">Requisitos y limitaciones para código HTML de entrada en solicitudes de páginas POST</span><span class="sxs-lookup"><span data-stu-id="97c57-143">Requirements and limitations for input HTML in POST pages requests</span></span>

<span data-ttu-id="97c57-144">Al enviar código HTML de entrada, tenga en cuenta estos requisitos y limitaciones generales:</span><span class="sxs-lookup"><span data-stu-id="97c57-144">When sending input HTML, be aware of these general requirements and limitations:</span></span>  

- <span data-ttu-id="97c57-145">El código HTML de entrada necesita tener codificación UTF-8 y XHTML con un formato correcto.</span><span class="sxs-lookup"><span data-stu-id="97c57-145">Input HTML should be UTF-8 encoded and well-formed XHTML.</span></span> <span data-ttu-id="97c57-146">Todas las etiquetas de inicio del contenedor necesitan las etiquetas de cierre correspondientes.</span><span class="sxs-lookup"><span data-stu-id="97c57-146">All container start tags require matching closing tags.</span></span> <span data-ttu-id="97c57-147">Todos los valores de atributo tienen que delimitarse con comillas dobles o simples.</span><span class="sxs-lookup"><span data-stu-id="97c57-147">All attribute values must be surrounded by double- or single-quote marks.</span></span>  <!--docs say MUST be encoded-->

- <span data-ttu-id="97c57-148">El código JavaScript se quita, incluidos los archivos y CSS.</span><span class="sxs-lookup"><span data-stu-id="97c57-148">JavaScript code, included files, and CSS are removed.</span></span> 

- <span data-ttu-id="97c57-149">Los formularios HTML se quitan por completo.</span><span class="sxs-lookup"><span data-stu-id="97c57-149">HTML forms are removed in their entirety.</span></span>  

- <span data-ttu-id="97c57-150">Microsoft Graph admite un [subconjunto de elementos HTML](#supported-html-and-css-for-onenote-pages).</span><span class="sxs-lookup"><span data-stu-id="97c57-150">Microsoft Graph supports a [subset of HTML elements](#supported-html-and-css-for-onenote-pages).</span></span> 

- <span data-ttu-id="97c57-151">Microsoft Graph admite un subconjunto de atributos HTML comunes y un conjunto de atributos personalizados, como el atributo **data-id** usado para actualizar páginas.</span><span class="sxs-lookup"><span data-stu-id="97c57-151">Microsoft Graph supports a subset of common HTML attributes and a set of custom attributes, such as the **data-id** attribute used for updating pages.</span></span> <span data-ttu-id="97c57-152">Para obtener información sobre los atributos admitidos, vea [HTML de entrada y salida](onenote-input-output-html.md).</span><span class="sxs-lookup"><span data-stu-id="97c57-152">For supported attributes, see [Input and output HTML](onenote-input-output-html.md).</span></span>


<a name="supported-html"></a>

### <a name="supported-html-and-css-for-onenote-pages"></a><span data-ttu-id="97c57-153">HTML y CSS admitido para páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="97c57-153">Supported HTML and CSS for OneNote pages</span></span>

<span data-ttu-id="97c57-154">No se admiten todos los elementos, atributos y propiedades (en HTML4, XHTML, CSS, HTML5, etc.).</span><span class="sxs-lookup"><span data-stu-id="97c57-154">Not all elements, attributes, and properties are supported (in HTML4, XHTML, CSS, HTML5, etc.).</span></span> <span data-ttu-id="97c57-155">En su lugar, Microsoft Graph admite un conjunto limitado de HTML que se adapta mejor a la forma en que los usuarios usan OneNote.</span><span class="sxs-lookup"><span data-stu-id="97c57-155">Instead, Microsoft Graph accepts a limited set of HTML that better fits how people use OneNote.</span></span> <span data-ttu-id="97c57-156">Para obtener más información, vea [Etiquetas HTML admitidas para páginas](https://dev.onenote.com/docs#/introduction/html-tag-support-for-pages).</span><span class="sxs-lookup"><span data-stu-id="97c57-156">For more information, see [HTML tag support for pages](https://dev.onenote.com/docs#/introduction/html-tag-support-for-pages).</span></span> <span data-ttu-id="97c57-157">Si una etiqueta no se muestra aquí, lo más probable es que se omita.</span><span class="sxs-lookup"><span data-stu-id="97c57-157">If a tag's not listed there, it'll probably be ignored.</span></span>

<!--Microsoft Graph only accepts UTF-8 data. Be sure that all requests are encoded that way, and your content-type headers indicate that as well. xx our examples don't show this-->

<span data-ttu-id="97c57-158">En la lista siguiente, se muestran los tipos de elementos básicos admitidos por Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="97c57-158">The following list shows the basic element types that Microsoft Graph supports:</span></span>

- <span data-ttu-id="97c57-159">`<head>` y `<body>`</span><span class="sxs-lookup"><span data-stu-id="97c57-159">`<head>` and `<body>`</span></span></p>
- <span data-ttu-id="97c57-160">`<title>` y `<meta>` que establece el título de página y la fecha de creación</span><span class="sxs-lookup"><span data-stu-id="97c57-160">`<title>` and `<meta>` that set the page title and creation date</span></span></p>
- <span data-ttu-id="97c57-161">`<h1>` a `<h6>` para los encabezados de sección</span><span class="sxs-lookup"><span data-stu-id="97c57-161">`<h1>` through `<h6>` for section headings</span></span></p>
- <span data-ttu-id="97c57-162">`<p>` para párrafos</span><span class="sxs-lookup"><span data-stu-id="97c57-162">`<p>` for paragraphs</span></span></p>
- <span data-ttu-id="97c57-163">`<ul>`, `<ol>` y `<li>` para listas y elementos de lista</span><span class="sxs-lookup"><span data-stu-id="97c57-163">`<ul>`, `<ol>`, and `<li>` for lists and list items</span></span></p>
- <span data-ttu-id="97c57-164">`<table>`, `<tr>`y `<td>`, incluidas las tablas anidadas</span><span class="sxs-lookup"><span data-stu-id="97c57-164">`<table>`, `<tr>` and `<td>`, including nested tables</span></span></p>
- <span data-ttu-id="97c57-165">`<pre>` para texto con formato previo (conserva el espacio en blanco y los saltos de línea)</span><span class="sxs-lookup"><span data-stu-id="97c57-165">`<pre>` for preformatted text (preserves white space and line breaks)</span></span></p>
- <span data-ttu-id="97c57-166">`<b>` y `<i>` para estilos de carácter negrita y cursiva</span><span class="sxs-lookup"><span data-stu-id="97c57-166">`<b>` and `<i>` for bold and italic character styles</span></span></p>

<span data-ttu-id="97c57-167">Microsoft Graph conserva el contenido semántico y la estructura básica del código HTML de entrada al crear páginas, pero convierte el código HTML de entrada para usar el conjunto admitido de HTML y CSS.</span><span class="sxs-lookup"><span data-stu-id="97c57-167">Microsoft Graph preserves the semantic content and basic structure of the input HTML when it creates pages, but it converts the input HTML to use the supported set of HTML and CSS.</span></span> <span data-ttu-id="97c57-168">Las características que no existen en OneNote no pueden traducirse a nada, por lo que es posible que no se reconozcan en el código HTML de origen.</span><span class="sxs-lookup"><span data-stu-id="97c57-168">Features that don't exist in OneNote have nothing to be translated to, so they might not be recognized in the source HTML.</span></span> 


<a name="example"></a>

## <a name="example-request"></a><span data-ttu-id="97c57-169">Ejemplo de solicitud</span><span class="sxs-lookup"><span data-stu-id="97c57-169">Example request</span></span>

<span data-ttu-id="97c57-170">En esta solicitud de varias partes de ejemplo, se crea una página que contiene imágenes y un archivo incrustado.</span><span class="sxs-lookup"><span data-stu-id="97c57-170">This example multipart request creates a page that contains images and an embedded file.</span></span> <span data-ttu-id="97c57-171">El elemento **Presentation** necesario contiene el código HTML de entrada que define la página.</span><span class="sxs-lookup"><span data-stu-id="97c57-171">The required **Presentation** part contains the input HTML that defines the page.</span></span> <span data-ttu-id="97c57-172">El elemento **imageBlock1** contiene los datos de imágenes binarias y **fileBlock1** contiene los datos de archivos binarios.</span><span class="sxs-lookup"><span data-stu-id="97c57-172">The **imageBlock1** part contains the binary image data, and **fileBlock1** contains the binary file data.</span></span> <span data-ttu-id="97c57-173">Los elementos de datos también pueden contener HTML; en ese caso, Microsoft Graph [representa el código HTML como una imagen](onenote-images-files.md#add-an-image-using-binary-data) en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="97c57-173">Data parts can also contain HTML, in which case Microsoft Graph [renders the HTML as an image](onenote-images-files.md#add-an-image-using-binary-data) on the OneNote page.</span></span> 

```html
POST https://graph.microsoft.com/v1.0/me/onenote/pages
Authorization: Bearer {token}
Content-Type: multipart/form-data; boundary=MyPartBoundary198374

--MyPartBoundary198374
Content-Disposition:form-data; name="Presentation"
Content-Type:text/html

<!DOCTYPE html>
<html>
  <head>
    <title>A page with rendered images and an attached file</title>
    <meta name="created" content="2015-07-22T09:00:00-08:00" />
  </head>
  <body>
    <p>Here's an image from an <i>online source</i>:</p>
    <img src="https://..." alt="an image on the page" width="500" />
    <p>Here's an image uploaded as <b>binary data</b>:</p>
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

<span data-ttu-id="97c57-174">Para obtener más ejemplos donde se muestra cómo crear páginas que contienen imágenes y otros archivos, vea [Agregar imágenes y archivos](onenote-images-files.md), [tutoriales](https://docs.microsoft.com/es-ES/previous-versions/office/office-365-api/how-to/onenote-tutorial) y [ejemplos](https://github.com/onenotedev).</span><span class="sxs-lookup"><span data-stu-id="97c57-174">For more examples that show how to create pages that contain images and other files, see [Add images and files](onenote-images-files.md), our [tutorials](https://docs.microsoft.com/es-ES/previous-versions/office/office-365-api/how-to/onenote-tutorial), and our [samples](https://github.com/onenotedev).</span></span> <span data-ttu-id="97c57-175">Además, obtenga información sobre cómo [crear elementos con posición absoluta](onenote-abs-pos.md), [usar etiquetas de nota](onenote-note-tags.md) y [extraer datos de capturas](onenote-extract-data.md) de tarjetas de presentación y listas de productos y recetas en línea.</span><span class="sxs-lookup"><span data-stu-id="97c57-175">Also, learn how to [create absolute positioned elements](onenote-abs-pos.md), [use note tags](onenote-note-tags.md), and [extract data](onenote-extract-data.md) for business card captures and online recipe and product listings.</span></span>

<span data-ttu-id="97c57-176">Microsoft Graph es estricto en relación con algunos formatos, como nuevas líneas CRLF en el cuerpo de un mensaje de varias partes.</span><span class="sxs-lookup"><span data-stu-id="97c57-176">Microsoft Graph is strict about some formats, such as CRLF newlines in a multipart message body.</span></span> <span data-ttu-id="97c57-177">Para reducir el riesgo de crear cargas de trabajo con formato incorrecto, necesita usar una biblioteca para crear mensajes de varias partes.</span><span class="sxs-lookup"><span data-stu-id="97c57-177">To reduce the risk of creating malformed payloads, you should use a library to construct multipart messages.</span></span> 

<span data-ttu-id="97c57-178">Si recibe un código de estado 400 para una carga con formato incorrecto, compruebe el formato de las nuevas líneas y los espacios en blanco, y asegúrese de que no haya problemas de codificación.</span><span class="sxs-lookup"><span data-stu-id="97c57-178">If you do receive a 400 status for a malformed payload, check the formatting of newlines and whitespaces, and check for encoding issues.</span></span> <span data-ttu-id="97c57-179">Por ejemplo, pruebe a usar `charset=utf-8` (ejemplo: `Content-Type: text/html; charset=utf-8`).</span><span class="sxs-lookup"><span data-stu-id="97c57-179">For example, try using `charset=utf-8` (example: `Content-Type: text/html; charset=utf-8`).</span></span>

<span data-ttu-id="97c57-180">Vea [Requisitos y limitaciones de HTML de entrada](#requirements-and-limitations-for-input-html-in-post-pages-requests) y [Límites de tamaño de solicitudes POST](onenote-images-files.md#size-limitations-for-post-pages-requests).</span><span class="sxs-lookup"><span data-stu-id="97c57-180">See [requirements and limitations for input HTML](#requirements-and-limitations-for-input-html-in-post-pages-requests) and [size limits for POST requests](onenote-images-files.md#size-limitations-for-post-pages-requests).</span></span>


<a name="request-response-info"></a>

## <a name="request-and-response-information-for-post-pages-requests"></a><span data-ttu-id="97c57-181">Información de solicitudes y respuestas para solicitudes de *páginas POST*</span><span class="sxs-lookup"><span data-stu-id="97c57-181">Request and response information for *POST pages* requests</span></span>

| <span data-ttu-id="97c57-182">Solicitar datos</span><span class="sxs-lookup"><span data-stu-id="97c57-182">Request data</span></span> | <span data-ttu-id="97c57-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="97c57-183">Description</span></span> |  
|------|------|  
| <span data-ttu-id="97c57-184">Protocolo</span><span class="sxs-lookup"><span data-stu-id="97c57-184">Protocol</span></span> | <span data-ttu-id="97c57-185">Todas las solicitudes usan el protocolo HTTPS SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="97c57-185">All requests use the SSL/TLS HTTPS protocol.</span></span> |  
| <span data-ttu-id="97c57-186">Encabezado Authorization</span><span class="sxs-lookup"><span data-stu-id="97c57-186">Authorization header</span></span> | <p><span data-ttu-id="97c57-187">`Bearer {token}`, donde `{token}` es un token de acceso de OAuth 2.0 válido para la aplicación registrada.</span><span class="sxs-lookup"><span data-stu-id="97c57-187">`Bearer {token}`, where `{token}` is a valid OAuth 2.0 access token for your registered app.</span></span></p><p><span data-ttu-id="97c57-188">Si falta o no es válido, la solicitud producirá errores con el código de estado 401.</span><span class="sxs-lookup"><span data-stu-id="97c57-188">If missing or invalid, the request fails with a 401 status code.</span></span> <span data-ttu-id="97c57-189">Vea [Authentication and permissions](permissions-reference.md) (Autenticación y permisos).</span><span class="sxs-lookup"><span data-stu-id="97c57-189">See [Authentication and permissions](permissions-reference.md).</span></span></p> |  
| <span data-ttu-id="97c57-190">Encabezado Content-Type</span><span class="sxs-lookup"><span data-stu-id="97c57-190">Content-Type header</span></span> | <p><span data-ttu-id="97c57-191">`text/html` o `application/xhtml+xml` para el contenido HTML, sin importar si se envía directamente en el cuerpo del mensaje o en el elemento “Presentación” necesario de las solicitudes de varias partes.</span><span class="sxs-lookup"><span data-stu-id="97c57-191">`text/html` or `application/xhtml+xml` for the HTML content, whether it's sent directly in the message body or in the required "Presentation" part of multipart requests.</span></span></p><p><span data-ttu-id="97c57-192">Las solicitudes de varias partes son necesarias al enviar datos binarios y usar el tipo de contenido `multipart/form-data; boundary=part-boundary`, donde `{part-boundary}` es una cadena que señala el principio y el final de cada elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="97c57-192">Multipart requests are required when sending binary data, and use the `multipart/form-data; boundary=part-boundary` content type, where `{part-boundary}` is a string that signals the start and end of each data part.</span></span></p> |  
| <span data-ttu-id="97c57-193">Encabezado Accept</span><span class="sxs-lookup"><span data-stu-id="97c57-193">Accept header</span></span> | `application/json` | 

<br/>

| <span data-ttu-id="97c57-194">Datos de respuesta</span><span class="sxs-lookup"><span data-stu-id="97c57-194">Response data</span></span> | <span data-ttu-id="97c57-195">Descripción</span><span class="sxs-lookup"><span data-stu-id="97c57-195">Description</span></span> |  
|------|------|  
| <span data-ttu-id="97c57-196">Código de correcto</span><span class="sxs-lookup"><span data-stu-id="97c57-196">Success code</span></span> | <span data-ttu-id="97c57-197">Código de estado HTTP 201.</span><span class="sxs-lookup"><span data-stu-id="97c57-197">A 201 HTTP status code.</span></span> |  
| <span data-ttu-id="97c57-198">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="97c57-198">Response body</span></span> | <span data-ttu-id="97c57-199">Una representación de OData de la nueva página en formato JSON.</span><span class="sxs-lookup"><span data-stu-id="97c57-199">A OData representation of the new page in JSON format.</span></span> |  
| <span data-ttu-id="97c57-200">Errores</span><span class="sxs-lookup"><span data-stu-id="97c57-200">Errors</span></span> | <span data-ttu-id="97c57-201">Si la solicitud no se completa correctamente, la API mostrará los errores del objeto **@api.diagnostics** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="97c57-201">If the request fails, the API returns errors in the **@api.diagnostics** object in the response body.</span></span> |  
| <span data-ttu-id="97c57-202">Encabezado de ubicación</span><span class="sxs-lookup"><span data-stu-id="97c57-202">Location header</span></span> | <span data-ttu-id="97c57-203">La URL de recursos de la nueva página.</span><span class="sxs-lookup"><span data-stu-id="97c57-203">The resource URL for the new page.</span></span> |  
| <span data-ttu-id="97c57-204">Encabezado X-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="97c57-204">X-CorrelationId header</span></span> | <span data-ttu-id="97c57-205">GUID que identifica la solicitud de forma única.</span><span class="sxs-lookup"><span data-stu-id="97c57-205">A GUID that uniquely identifies the request.</span></span> <span data-ttu-id="97c57-206">Puede usar este valor, además del valor del encabezado de fecha, al trabajar con el soporte técnico de Microsoft para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="97c57-206">You can use this value along with the value of the Date header when working with Microsoft support to troubleshoot issues.</span></span> |  


<a name="root-url"></a>

### <a name="constructing-the-microsoft-graph-service-root-url"></a><span data-ttu-id="97c57-207">Crear la URL raíz del servicio de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="97c57-207">Constructing the Microsoft Graph service root URL</span></span>

<span data-ttu-id="97c57-208">La URL raíz del servicio de Microsoft Graph usa el formato siguiente para todas las llamadas que se realicen a Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="97c57-208">The Microsoft Graph service root URL uses the following format for all calls to Microsoft Graph:</span></span>

`https://graph.microsoft.com/{version}/me/onenote/`  

<span data-ttu-id="97c57-209">El segmento `version` de la URL representa la versión de Microsoft Graph que se quiere utilizar.</span><span class="sxs-lookup"><span data-stu-id="97c57-209">The `version` segment in the URL represents the version of Microsoft Graph that you want to use.</span></span> <span data-ttu-id="97c57-210">Use `v1.0` para código de producción estable.</span><span class="sxs-lookup"><span data-stu-id="97c57-210">Use `v1.0` for stable production code.</span></span> <span data-ttu-id="97c57-211">Use `beta` para probar una característica que esté en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="97c57-211">Use `beta` to try out a feature that's in development.</span></span> <span data-ttu-id="97c57-212">Las características y la funcionalidad de la versión beta pueden cambiar, por lo que no se debe usar en el código de producción.</span><span class="sxs-lookup"><span data-stu-id="97c57-212">Features and functionality in beta may change, so you shouldn't use it in your production code.</span></span> 

<span data-ttu-id="97c57-213">Use `me` para contenido de OneNote al que puede obtener acceso el usuario actual (contenido compartido y del que sea propietario).</span><span class="sxs-lookup"><span data-stu-id="97c57-213">Use `me` for OneNote content that the current user can access (owned and shared).</span></span> <span data-ttu-id="97c57-214">Use `users/{id}` para contenido de OneNote que el usuario especificado (en la URL) compartió con el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="97c57-214">Use `users/{id}` for OneNote content that the specified user (in the URL) has shared with the current user.</span></span> <span data-ttu-id="97c57-215">Use [Microsoft Graph](https://graph.microsoft.com/v1.0/users) para obtener identificadores de usuario.</span><span class="sxs-lookup"><span data-stu-id="97c57-215">Use [Microsoft Graph](https://graph.microsoft.com/v1.0/users) to get user IDs.</span></span> 


<a name="permissions"></a>

## <a name="permissions"></a><span data-ttu-id="97c57-216">Permisos</span><span class="sxs-lookup"><span data-stu-id="97c57-216">Permissions</span></span>

<span data-ttu-id="97c57-217">Para crear páginas de OneNote, necesitará solicitar los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="97c57-217">To create OneNote pages, you'll need to request appropriate permissions.</span></span> <span data-ttu-id="97c57-218">Seleccione el nivel inferior de permisos que necesita la aplicación para funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="97c57-218">Choose the lowest level of permissions that your app needs to do its work.</span></span>

<span data-ttu-id="97c57-219">Seleccione entre:</span><span class="sxs-lookup"><span data-stu-id="97c57-219">Choose from:</span></span>

- <span data-ttu-id="97c57-220">Notes.Create</span><span class="sxs-lookup"><span data-stu-id="97c57-220">Notes.Create</span></span>
- <span data-ttu-id="97c57-221">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="97c57-221">Notes.ReadWrite</span></span>
- <span data-ttu-id="97c57-222">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="97c57-222">Notes.ReadWrite.All</span></span>

<span data-ttu-id="97c57-223">Para obtener más información sobre los ámbitos de permiso y cómo funcionan, vea [Referencias de permisos de Microsoft Graph](permissions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="97c57-223">For more information about permission scopes and how they work, see [Microsoft Graph permissions reference](permissions-reference.md).</span></span>




<a name="see-also"></a>

## <a name="see-also"></a><span data-ttu-id="97c57-224">Vea también</span><span class="sxs-lookup"><span data-stu-id="97c57-224">See also</span></span>

- [<span data-ttu-id="97c57-225">Agregar imágenes y archivos</span><span class="sxs-lookup"><span data-stu-id="97c57-225">Add images and files</span></span>](onenote-images-files.md)
- [<span data-ttu-id="97c57-226">Crear elementos con posición absoluta</span><span class="sxs-lookup"><span data-stu-id="97c57-226">Create absolute positioned elements</span></span>](onenote-abs-pos.md)  
- [<span data-ttu-id="97c57-227">Extraer datos</span><span class="sxs-lookup"><span data-stu-id="97c57-227">Extract data</span></span>](onenote-extract-data.md)
- [<span data-ttu-id="97c57-228">Usar etiquetas de nota</span><span class="sxs-lookup"><span data-stu-id="97c57-228">Use note tags</span></span>](onenote-note-tags.md)
- [<span data-ttu-id="97c57-229">Integración con OneNote</span><span class="sxs-lookup"><span data-stu-id="97c57-229">Integrate with OneNote</span></span>](integrate-with-onenote.md)
- [<span data-ttu-id="97c57-230">Blog para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="97c57-230">OneNote Developer Blog</span></span>](https://go.microsoft.com/fwlink/?LinkID=390183)
- [<span data-ttu-id="97c57-231">Preguntas de desarrollo de OneNote en Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="97c57-231">OneNote development questions on Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkID=390182)
- [<span data-ttu-id="97c57-232">Repositorios de OneNote en GitHub</span><span class="sxs-lookup"><span data-stu-id="97c57-232">OneNote GitHub repos</span></span>](https://go.microsoft.com/fwlink/?LinkID=390178)  


