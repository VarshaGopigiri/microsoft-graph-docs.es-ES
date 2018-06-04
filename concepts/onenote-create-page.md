# <a name="create-onenote-pages"></a><span data-ttu-id="045e4-101">Crear páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="045e4-101">Create OneNote pages</span></span>

<span data-ttu-id="045e4-102">*__Se aplica a:__ Blocs de notas para consumidores de OneDrive | Blocs de notas empresariales de Office 365*</span><span class="sxs-lookup"><span data-stu-id="045e4-102">*__Applies to:__ Consumer notebooks on OneDrive | Enterprise notebooks on Office 365*</span></span>

<span data-ttu-id="045e4-103">Para crear una página de OneNote, envíe una solicitud POST al punto de conexión *pages*.</span><span class="sxs-lookup"><span data-stu-id="045e4-103">When you create a OneNote page, you send a POST request to  the pages endpoint:</span></span> <span data-ttu-id="045e4-104">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="045e4-104">For example:</span></span>

`POST ../notes/sections/{id}/pages`</p>

<span data-ttu-id="045e4-105">Envíe el HTML que define la página en el cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="045e4-105">Send the HTML that defines the page in the message body.</span></span> <span data-ttu-id="045e4-106">Si la solicitud se completa correctamente, Microsoft Graph devuelve un código de estado HTTP 201.</span><span class="sxs-lookup"><span data-stu-id="045e4-106">If the create request is successful, the onnvshort API returns a 201 HTTP status code.</span></span>


> <span data-ttu-id="045e4-107">**Nota:** Para obtener información sobre las solicitudes POST que puede enviar para crear secciones, grupos de secciones y blocs de notas, vea la [referencia de REST interactiva](http://dev.onenote.com/docs).</span><span class="sxs-lookup"><span data-stu-id="045e4-107">**Note:** To learn about the POST requests you can send to create sections, section groups, and notebooks, see our [interactive REST reference](http://dev.onenote.com/docs).</span></span>


<a name="request-uri"></a>
## <a name="construct-the-request-uri"></a><span data-ttu-id="045e4-108">Crear el URI de la solicitud</span><span class="sxs-lookup"><span data-stu-id="045e4-108">Construct the request</span></span>

<span data-ttu-id="045e4-109">Para crear el URI de la solicitud POST, empiece con la dirección URL raíz del servicio:</span><span class="sxs-lookup"><span data-stu-id="045e4-109">To construct the POST request URI, start with the service root URL:</span></span>

`https://graph.microsoft.com/v1.0/me/onenote`

<span data-ttu-id="045e4-110">Después, anexe el punto de conexión *pages*:</span><span class="sxs-lookup"><span data-stu-id="045e4-110">Then append the *pages* endpoint:</span></span>

<span data-ttu-id="045e4-111">**Crear una página en cualquier sección (especificado por el nombre de sección)**</span><span class="sxs-lookup"><span data-stu-id="045e4-111">**Create a page in any section (specified by section name)**</span></span>

`.../pages?sectionName=DefaultSection`

<span data-ttu-id="045e4-112">**Crear una página en cualquier sección (especificado por el id.)**</span><span class="sxs-lookup"><span data-stu-id="045e4-112">**Create a page in any section (specified by ID)**</span></span> 

`.../sections/{section-id}/pages` 

<span data-ttu-id="045e4-113">Si va a crear páginas en el bloc de notas personal del usuario, Microsoft Graph también proporciona puntos de conexión que puede usar para crear páginas en el bloc de notas predeterminado:</span><span class="sxs-lookup"><span data-stu-id="045e4-113">If you're creating pages in the user's personal notebook, Microsoft Graph also provides endpoints you can use to create pages in the default notebook:</span></span>

<span data-ttu-id="045e4-114">**Crear una página de OneNote en la sección predeterminada del bloc de notas predeterminado**</span><span class="sxs-lookup"><span data-stu-id="045e4-114">**Create a new OneNote page in the default section of the default notebook.**</span></span> 

`../pages` 



<span data-ttu-id="045e4-115">La URI de la solicitud completa tendrá un aspecto similar a uno de estos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="045e4-115">Your full request URI will look like one of these examples:</span></span>
* `https://graph.microsoft.com/v1.0/me/onenote/sections/{id}/pages`
* `https://graph.microsoft.com/v1.0/me/onenote/pages?sectionName=Homework`

<span data-ttu-id="045e4-116">Obtenga más información sobre la [URL de raíz del servicio](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).</span><span class="sxs-lookup"><span data-stu-id="045e4-116">Learn more about the [service root URL](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).</span></span>

<a name="post-pages-section-name"></a>
### <a name="using-the-sectionname-url-parameter"></a><span data-ttu-id="045e4-117">Usar el parámetro de URL *sectionName*</span><span class="sxs-lookup"><span data-stu-id="045e4-117">Using the *sectionName* URL parameter</span></span>

<span data-ttu-id="045e4-118">Las reglas siguientes se aplican al usar el parámetro *sectionName* para crear una página en una sección con nombre del bloc de notas predeterminado:</span><span class="sxs-lookup"><span data-stu-id="045e4-118">The following rules apply when using the *sectionName* parameter to create a page in a named section in the default notebook:</span></span>

- <span data-ttu-id="045e4-119">Solo se puede hacer referencia a las secciones de nivel superior (no a las secciones dentro de grupos de secciones).</span><span class="sxs-lookup"><span data-stu-id="045e4-119">Only top-level sections can be referenced (not sections within section groups).</span></span>

- <span data-ttu-id="045e4-120">Si en el bloc de notas predeterminado no existe una sección con el nombre especificado, la API la creará.</span><span class="sxs-lookup"><span data-stu-id="045e4-120">If a section with the specified name doesn't exist in the default notebook, the API creates it.</span></span> <span data-ttu-id="045e4-121">Los caracteres siguientes no pueden usarse en los nombres de sección: ?</span><span class="sxs-lookup"><span data-stu-id="045e4-121">These characters are not allowed for section names: ?</span></span> <span data-ttu-id="045e4-122">\* \ / : &lt; &gt; | &amp; # " % ~</span><span class="sxs-lookup"><span data-stu-id="045e4-122">\* \ / : &lt; &gt; | &amp; # " % ~</span></span>

- <span data-ttu-id="045e4-123">Los nombres de sección no distinguen mayúsculas de minúsculas, pero el uso de mayúsculas se conserva al crear las secciones.</span><span class="sxs-lookup"><span data-stu-id="045e4-123">Section names are case-insensitive for matching, but case is preserved when sections are created.</span></span> <span data-ttu-id="045e4-124">Por lo tanto, “Mi nueva sección” se mostrará de esa forma, pero “mi nueva sección” también coincidirá en las publicaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="045e4-124">Section names are case-insensitive for matching, but the case is preserved when they are created. So "My New Section" will be displayed like that, but "my new section" would also match on subsequent posts.</span></span>

- <span data-ttu-id="045e4-125">Los nombres de sección necesitan tener el formato de codificación URL.</span><span class="sxs-lookup"><span data-stu-id="045e4-125">Section names must be URL-encoded.</span></span> <span data-ttu-id="045e4-126">Por ejemplo, los espacios tienen que codificarse como *%20*.</span><span class="sxs-lookup"><span data-stu-id="045e4-126">The new section name must be URL-encoded.  For example, spaces must be encoded as *%20*.</span></span>

- <span data-ttu-id="045e4-127">El parámetro *sectionName* solo es válido con la ruta `../notes/pages` (pero no con `../notes/sections/{id}/pages`).</span><span class="sxs-lookup"><span data-stu-id="045e4-127">The *sectionName* parameter is valid only with the `../notes/pages` route (not `../notes/sections/{id}/pages`).</span></span>

<span data-ttu-id="045e4-128">Como se crearán secciones si no existen, es seguro usar esta llamada con todas las páginas que cree la aplicación.</span><span class="sxs-lookup"><span data-stu-id="045e4-128">Because sections are created if they don't exist, it's safe to use this call with every page your app creates.</span></span> <span data-ttu-id="045e4-129">Aunque los usuarios pueden cambiar el nombre de las secciones, la API creará una sección con el nombre de sección que especifique.</span><span class="sxs-lookup"><span data-stu-id="045e4-129">Users might rename sections, in which case the API will create a new section with the sectionName you supply.</span></span> 

> <span data-ttu-id="045e4-130">**Nota:** Los vínculos devueltos por la API para las páginas en una sección con un nombre cambiado también llegarán a las páginas anteriores.</span><span class="sxs-lookup"><span data-stu-id="045e4-130">**Note:** The links returned by the API for pages in a renamed section will still reach those older pages.</span></span> 


<a name="message-body"></a>
## <a name="construct-the-message-body"></a><span data-ttu-id="045e4-131">Crear el cuerpo del mensaje</span><span class="sxs-lookup"><span data-stu-id="045e4-131">Construct the message body</span></span>

<span data-ttu-id="045e4-132">El código HTML que define el contenido de la página se denomina *HTML de entrada*.</span><span class="sxs-lookup"><span data-stu-id="045e4-132">The HTML that defines the page content and structure when you create or update a OneNote page is called *input HTML*.</span></span> <span data-ttu-id="045e4-133">El código HTML de entrada admite un [subconjunto de HTML y CSS estándar](#supported-html-and-css-for-onenote-pages), además de atributos personalizados.</span><span class="sxs-lookup"><span data-stu-id="045e4-133">Input HTML supports a [subset of standard HTML and CSS](#supported-html-and-css-for-onenote-pages), with the addition of custom attributes.</span></span> <span data-ttu-id="045e4-134">(Los atributos personalizados, como **data-id** y **data-render-src**, se describen en [HTML de entrada y salida](onenote_input_output_html.md)).</span><span class="sxs-lookup"><span data-stu-id="045e4-134">(Custom attributes, like **data-id** and **data-render-src**, are described in [Input and output HTML](onenote_input_output_html.md).)</span></span> 

<span data-ttu-id="045e4-135">Envíe el código HTML de entrada en el cuerpo del mensaje de la solicitud POST.</span><span class="sxs-lookup"><span data-stu-id="045e4-135">Send the input HTML in the message body of the POST request.</span></span> <span data-ttu-id="045e4-136">Puede enviar el código HTML de entrada directamente en el cuerpo del mensaje con el tipo de contenido `application/xhtml+xml` o `text/html`, o bien puede enviarlo en el elemento “Presentación” de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="045e4-136">You can send the input HTML directly in the message body using the  `application/xhtml+xml` or `text/html` content type, or you can send it in the "Presentation" part of a multipart request.</span></span> 

<span data-ttu-id="045e4-137">En el ejemplo siguiente, se envía el código HTML de entrada directamente en el cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="045e4-137">The following example sends the input HTML directly in the message body.</span></span>

```
POST https://graph.microsoft.com/v1.0/me/onenote/pages
Authorization: Bearer {token}
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
    <img src="http://..." alt="an image on the page" width="500" />
  </body>
</html>
```

<span data-ttu-id="045e4-138">Si envía datos binarios, tendrá que usar una [solicitud de varias partes](#example-request).</span><span class="sxs-lookup"><span data-stu-id="045e4-138">If you're sending binary data, you must use a [multipart request](#example-request).</span></span> 

><span data-ttu-id="045e4-139">Para simplificar la programación y la coherencia en la aplicación, puede usar solicitudes de varias partes para crear todas las páginas.</span><span class="sxs-lookup"><span data-stu-id="045e4-139">To simplify programming and consistency in your app, you can use multipart requests to create all pages.</span></span> <span data-ttu-id="045e4-140">Le recomendamos que use una biblioteca para crear mensajes de varias partes.</span><span class="sxs-lookup"><span data-stu-id="045e4-140">It's a good idea to use a library to construct multipart messages.</span></span> <span data-ttu-id="045e4-141">Esto reduce el riesgo de crear cargas de trabajo con formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="045e4-141">This reduces the risk of creating malformed payloads.</span></span>


<a name="input-html-rules"></a>
### <a name="requirements-and-limitations-for-input-html-in-post-pages-requests"></a><span data-ttu-id="045e4-142">Requisitos y limitaciones para HTML de entrada en solicitudes de páginas POST</span><span class="sxs-lookup"><span data-stu-id="045e4-142">Requirements and limitations for input HTML in POST pages requests</span></span>

<span data-ttu-id="045e4-143">Al enviar HTML de entrada, tenga en cuenta estos requisitos y limitaciones generales:</span><span class="sxs-lookup"><span data-stu-id="045e4-143">When sending input HTML, be aware of these general requirements and limitations:</span></span>  

- <span data-ttu-id="045e4-144">El código HTML de entrada necesita tener codificación UTF-8 y XHTML con un formato correcto.</span><span class="sxs-lookup"><span data-stu-id="045e4-144">Input HTML should be UTF-8 encoded and well-formed XHTML.</span></span> <span data-ttu-id="045e4-145">Todas las etiquetas de inicio del contenedor necesitan las etiquetas de cierre correspondientes.</span><span class="sxs-lookup"><span data-stu-id="045e4-145">All container start tags require matching closing tags.</span></span> <span data-ttu-id="045e4-146">Todos los valores de atributo tienen que delimitarse con comillas dobles o simples.</span><span class="sxs-lookup"><span data-stu-id="045e4-146">All attribute values must be surrounded by double- or single-quote marks like in the preceding img tag.</span></span>  <!--docs say MUST be encoded-->

- <span data-ttu-id="045e4-147">El código JavaScript se quita, incluidos los archivos y CSS.</span><span class="sxs-lookup"><span data-stu-id="045e4-147">Javascript code, included files and CSS are removed.</span></span> 

- <span data-ttu-id="045e4-148">Los formularios HTML se quitan por completo.</span><span class="sxs-lookup"><span data-stu-id="045e4-148">HTML forms are removed in their entirety.</span></span>  

- <span data-ttu-id="045e4-149">Microsoft Graph admite un [subconjunto de elementos HTML](#supported-html-and-css-for-onenote-pages).</span><span class="sxs-lookup"><span data-stu-id="045e4-149">Microsoft Graph supports a [subset of HTML elements](#supported-html-and-css-for-onenote-pages).</span></span> 

- <span data-ttu-id="045e4-150">Microsoft Graph admite un subconjunto de atributos HTML comunes y un conjunto de atributos personalizados, como el atributo **data-id** usado para actualizar páginas.</span><span class="sxs-lookup"><span data-stu-id="045e4-150">Microsoft Graph supports a subset of common HTML attributes and a set of custom attributes, such as the **data-id** attribute used for updating pages.</span></span> <span data-ttu-id="045e4-151">Para obtener información sobre los atributos admitidos, vea [HTML de entrada y salida](onenote_input_output_html.md).</span><span class="sxs-lookup"><span data-stu-id="045e4-151">See [Input and output HTML](onenote_input_output_html.md) for supported attributes.</span></span>


<a name="supported-html"></a>
### <a name="supported-html-and-css-for-onenote-pages"></a><span data-ttu-id="045e4-152">HTML y CSS admitido para páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="045e4-152">Supported HTML and CSS for OneNote pages</span></span>

<span data-ttu-id="045e4-153">No se admiten todos los elementos, atributos y propiedades (en HTML4, XHTML, CSS, HTML5, etc.).</span><span class="sxs-lookup"><span data-stu-id="045e4-153">Not all elements, attributes, and properties are supported (in HTML4, XHTML, CSS, HTML5, etc.).</span></span> <span data-ttu-id="045e4-154">En su lugar, Microsoft Graph admite un conjunto limitado de HTML que se adapta mejor a la forma en que los usuarios usan OneNote.</span><span class="sxs-lookup"><span data-stu-id="045e4-154">Instead, Microsoft Graph accepts a limited set of HTML that better fits how people use OneNote.</span></span> <span data-ttu-id="045e4-155">Para obtener más información, vea [Etiquetas HTML admitidas para páginas](http://dev.onenote.com/docs#/introduction/html-tag-support-for-pages).</span><span class="sxs-lookup"><span data-stu-id="045e4-155">For more information, see [HTML tag support for pages](http://dev.onenote.com/docs#/introduction/html-tag-support-for-pages).</span></span> <span data-ttu-id="045e4-156">Si una etiqueta no se muestra aquí, lo más probable es que se omita.</span><span class="sxs-lookup"><span data-stu-id="045e4-156">If a tag's not listed there, it'll probably be ignored.</span></span>

<!--Microsoft Graph only accepts UTF-8 data. Be sure that all requests are encoded that way, and your content-type headers indicate that as well. xx our examples don't show this-->

<span data-ttu-id="045e4-157">En la lista siguiente, se muestran los tipos de elementos básicos admitidos por Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="045e4-157">The following list shows the basic element types that Microsoft Graph supports:</span></span>

- <span data-ttu-id="045e4-158">`<head>` y `<body>`</span><span class="sxs-lookup"><span data-stu-id="045e4-158">`<head>` and `<body>`</span></span></p>
- <span data-ttu-id="045e4-159">`<title>` y `<meta>` que establece el título de página y la fecha de creación</span><span class="sxs-lookup"><span data-stu-id="045e4-159"><title>`<title>` and <meta>`<meta>` that set the page title and creation date</span></span></p>
- <span data-ttu-id="045e4-160">`<h1>` a `<h6>` para los encabezados de sección</span><span class="sxs-lookup"><span data-stu-id="045e4-160"><h1>`<h1>` through <h6>`<h6>` for section headings</span></span></p>
- <span data-ttu-id="045e4-161">`<p>` para párrafos</span><span class="sxs-lookup"><span data-stu-id="045e4-161">`<p>` for paragraphs</span></span></p>
- <span data-ttu-id="045e4-162">`<ul>`, `<ol>` y `<li>` para listas y elementos de lista</span><span class="sxs-lookup"><span data-stu-id="045e4-162">`<ul>`, `<ol>`, and `<li>` for lists and list items</span></span></p>
- <span data-ttu-id="045e4-163">`<table>`, `<tr>`y `<td>`, incluidas las tablas anidadas</span><span class="sxs-lookup"><span data-stu-id="045e4-163">`<table>`, `<tr>` and `<td>`, including nested tables</span></span></p>
- <span data-ttu-id="045e4-164">`<pre>` para texto con formato previo (conserva el espacio en blanco y los saltos de línea)</span><span class="sxs-lookup"><span data-stu-id="045e4-164">`<pre>` for preformatted text (preserves white space and line breaks)</span></span></p>
- <span data-ttu-id="045e4-165">`<b>` y `<i>` para estilos de carácter negrita y cursiva</span><span class="sxs-lookup"><span data-stu-id="045e4-165"><b>`<b>` and <i>`<i>` for bold and italic character styles</span></span></p>

<span data-ttu-id="045e4-166">Microsoft Graph conserva el contenido semántico y la estructura básica del HTML de entrada al crear páginas, pero convierte el HTML de entrada para usar el conjunto admitido de HTML y CSS.</span><span class="sxs-lookup"><span data-stu-id="045e4-166">Microsoft Graph preserves the semantic content and basic structure of the input HTML when it creates pages, but it converts the input HTML to use the supported set of HTML and CSS.</span></span> <span data-ttu-id="045e4-167">Las características que no existen en OneNote no pueden traducirse a nada, por lo que es posible que no se reconozcan en el HTML de origen.</span><span class="sxs-lookup"><span data-stu-id="045e4-167">Features that don't exist in OneNote have nothing to be translated to, so they might not be recognized in the source HTML.</span></span> 


<a name="example"></a>
## <a name="example-request"></a><span data-ttu-id="045e4-168">Ejemplo de solicitud</span><span class="sxs-lookup"><span data-stu-id="045e4-168">Example request</span></span>

<span data-ttu-id="045e4-169">En esta solicitud de varias partes de ejemplo, se crea una página que contiene imágenes y un archivo incrustado.</span><span class="sxs-lookup"><span data-stu-id="045e4-169">This example multipart request creates a page that contains images and an embedded file.</span></span> <span data-ttu-id="045e4-170">El elemento **Presentation** necesario contiene el HTML de entrada que define la página.</span><span class="sxs-lookup"><span data-stu-id="045e4-170">The required **Presentation** part contains the input HTML that defines the page.</span></span> <span data-ttu-id="045e4-171">El elemento **imageBlock1** contiene los datos de imágenes binarias, y **fileBlock1** contiene los datos de archivos binarios.</span><span class="sxs-lookup"><span data-stu-id="045e4-171">The **imageBlock1** part contains the binary image data and **fileBlock1** contains the binary file data.</span></span> <span data-ttu-id="045e4-172">Los elementos de datos también pueden contener HTML; en ese caso, Microsoft Graph [representa el código HTML como una imagen](onenote_images_files.md#add-an-image-using-binary-data) en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="045e4-172">Data parts can also contain HTML, in which case Microsoft Graph [renders the HTML as an image](onenote_images_files.md#add-an-image-using-binary-data) on the OneNote page.</span></span> 

```
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
    <img src="http://..." alt="an image on the page" width="500" />
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

<span data-ttu-id="045e4-173">Para obtener más ejemplos donde se muestra cómo crear páginas que contienen imágenes y otros archivos, vea [Agregar imágenes y archivos](onenote_images_files.md), [tutoriales](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-tutorial) y [ejemplos](https://github.com/onenotedev).</span><span class="sxs-lookup"><span data-stu-id="045e4-173">For more examples that show how to create pages that contain images and other files, see [Add images and files](onenote_images_files.md), our [tutorials](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-tutorial), and our [samples](https://github.com/onenotedev).</span></span> <span data-ttu-id="045e4-174">Además, obtenga información sobre cómo [crear elementos con posición absoluta](onenote-abs-pos.md), [usar etiquetas de notas](onenote-note-tags.md) y [extraer datos de capturas](onenote-extract-data.md) de tarjetas de presentación y listas de productos y recetas en línea.</span><span class="sxs-lookup"><span data-stu-id="045e4-174">Also, learn how to [create absolute positioned elements](onenote-abs-pos.md), [use note tags](onenote-note-tags.md), and [extract data](onenote-extract-data.md) for business card captures and online recipe and product listings.</span></span>

<span data-ttu-id="045e4-175">Microsoft Graph es estricto en relación con algunos formatos, como nuevas líneas CRLF en el cuerpo de un mensaje de varias partes.</span><span class="sxs-lookup"><span data-stu-id="045e4-175">Microsoft Graph is strict about some formats, such as CRLF newlines in a multipart message body.</span></span> <span data-ttu-id="045e4-176">Para reducir el riesgo de crear cargas de trabajo con formato incorrecto, necesita usar una biblioteca para crear mensajes de varias partes.</span><span class="sxs-lookup"><span data-stu-id="045e4-176">To reduce the risk of creating malformed payloads, you should use a library to construct multipart messages.</span></span> <span data-ttu-id="045e4-177">Si recibe un código de estado 400 para una carga con formato incorrecto, compruebe el formato de las nuevas líneas y los espacios en blanco, y asegúrese de que no haya problemas de codificación.</span><span class="sxs-lookup"><span data-stu-id="045e4-177">If you do receive a 400 status for a malformed payload, check the formatting of newlines and whitespaces, and check for encoding issues.</span></span> <span data-ttu-id="045e4-178">Por ejemplo, pruebe a usar `charset=utf-8` (ejemplo: `Content-Type: text/html; charset=utf-8`).</span><span class="sxs-lookup"><span data-stu-id="045e4-178">For example, try using `charset=utf-8` (example: `Content-Type: text/html; charset=utf-8`).</span></span>

<span data-ttu-id="045e4-179">Vea [Requisitos y limitaciones de HTML de entrada](#requirements-and-limitations-for-input-html-in-post-pages-requests) y [Límites de tamaño de solicitudes POST](onenote_images_files.md#size-limitations-for-post-pages-requests).</span><span class="sxs-lookup"><span data-stu-id="045e4-179">See [requirements and limitations for input HTML](#requirements-and-limitations-for-input-html-in-post-pages-requests) and [size limits for POST requests](onenote_images_files.md#size-limitations-for-post-pages-requests).</span></span>


<a name="request-response-info"></a>
## <a name="request-and-response-information-for-post-pages-requests"></a><span data-ttu-id="045e4-180">Información de solicitudes y respuestas para solicitudes de *páginas POST*</span><span class="sxs-lookup"><span data-stu-id="045e4-180">Request and response information for *POST pages* requests</span></span>

| <span data-ttu-id="045e4-181">Solicitar datos</span><span class="sxs-lookup"><span data-stu-id="045e4-181">Request data</span></span> | <span data-ttu-id="045e4-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="045e4-182">Description</span></span> |  
|------|------|  
| <span data-ttu-id="045e4-183">Protocolo</span><span class="sxs-lookup"><span data-stu-id="045e4-183">Protocol</span></span> | <span data-ttu-id="045e4-184">Todas las solicitudes usan el protocolo HTTPS SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="045e4-184">All requests use the SSL/TLS HTTPS protocol.</span></span> |  
| <span data-ttu-id="045e4-185">Encabezado Authorization</span><span class="sxs-lookup"><span data-stu-id="045e4-185">Authorization header</span></span> | <p><span data-ttu-id="045e4-186">`Bearer {token}`, donde *{token}* es un token de acceso de OAuth 2.0 válido para la aplicación registrada.</span><span class="sxs-lookup"><span data-stu-id="045e4-186">`Bearer {token}`, where *{token}* is a valid OAuth 2.0 access token for your registered app.</span></span></p><p><span data-ttu-id="045e4-187">Si falta o no es válido, la solicitud producirá errores con el código de estado 401.</span><span class="sxs-lookup"><span data-stu-id="045e4-187">If missing or invalid, the request fails with a 401 status code.</span></span> <span data-ttu-id="045e4-188">Vea [Autenticación y permisos](permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="045e4-188">See [Authentication and permissions](permissions_reference.md).</span></span></p> |  
| <span data-ttu-id="045e4-189">Encabezado Content-Type</span><span class="sxs-lookup"><span data-stu-id="045e4-189">content-type header</span></span> | <p><span data-ttu-id="045e4-190">`text/html` o `application/xhtml+xml` para el contenido HTML, sin importar si se envía directamente en el cuerpo del mensaje o en el elemento “Presentación” necesario de las solicitudes de varias partes.</span><span class="sxs-lookup"><span data-stu-id="045e4-190">`text/html` or `application/xhtml+xml` for the HTML content, whether it's sent directly in the message body or in the required "Presentation" part of multipart requests.</span></span></p><p><span data-ttu-id="045e4-191">Las solicitudes de varias partes son necesarias al enviar datos binarios y usar el tipo de contenido `multipart/form-data; boundary=part-boundary`, donde *{límite-de-elemento}* es una cadena que señala el principio y el final de cada elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="045e4-191">Multipart requests are required when sending binary data, and use the `multipart/form-data; boundary=part-boundary` content type, where *{part-boundary}* is a string that signals the start and end of each data part.</span></span></p> |  
| <span data-ttu-id="045e4-192">Encabezado Accept</span><span class="sxs-lookup"><span data-stu-id="045e4-192">accept header</span></span> | `application/json` | 

| <span data-ttu-id="045e4-193">Datos de respuesta</span><span class="sxs-lookup"><span data-stu-id="045e4-193">Response data</span></span> | <span data-ttu-id="045e4-194">Descripción</span><span class="sxs-lookup"><span data-stu-id="045e4-194">Description</span></span> |  
|------|------|  
| <span data-ttu-id="045e4-195">Código de correcto</span><span class="sxs-lookup"><span data-stu-id="045e4-195">Success code</span></span> | <span data-ttu-id="045e4-196">Código de estado HTTP 201.</span><span class="sxs-lookup"><span data-stu-id="045e4-196">A 201 HTTP status code.</span></span> |  
| <span data-ttu-id="045e4-197">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="045e4-197">Response body</span></span> | <span data-ttu-id="045e4-198">Una representación de OData de la nueva página en formato JSON.</span><span class="sxs-lookup"><span data-stu-id="045e4-198">A OData representation of the new page in JSON format.</span></span> |  
| <span data-ttu-id="045e4-199">Errores</span><span class="sxs-lookup"><span data-stu-id="045e4-199">Errors</span></span> | <span data-ttu-id="045e4-200">Si la solicitud no se completa correctamente, la API mostrará los errores del objeto **@api.diagnostics** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="045e4-200">If the update request fails, the API returns errors in the **api.diagnostics** object in the response body. The request will fail if:</span></span> |  
| <span data-ttu-id="045e4-201">Encabezado de ubicación</span><span class="sxs-lookup"><span data-stu-id="045e4-201">Location header</span></span> | <span data-ttu-id="045e4-202">La URL de recursos de la nueva página.</span><span class="sxs-lookup"><span data-stu-id="045e4-202">The resource URL for the new page.</span></span> |  
| <span data-ttu-id="045e4-203">Encabezado X-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="045e4-203">X-CorrelationId header</span></span> | <span data-ttu-id="045e4-204">GUID que identifica la solicitud de forma única.</span><span class="sxs-lookup"><span data-stu-id="045e4-204">A GUID that uniquely identifies the request.</span></span> <span data-ttu-id="045e4-205">Puede usar este valor, además del valor del encabezado de fecha, al trabajar con el soporte técnico de Microsoft para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="045e4-205">You can use this value along with the value of the Date header when working with Microsoft support to troubleshoot issues.</span></span> |  


<a name="root-url"></a>
### <a name="constructing-the-microsoft-graph-service-root-url"></a><span data-ttu-id="045e4-206">Crear la URL raíz del servicio de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="045e4-206">Constructing the Microsoft Graph service root URL</span></span>

<span data-ttu-id="045e4-207">La URL raíz del servicio de Microsoft Graph usa el formato siguiente para todas las llamadas que se realicen a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="045e4-207">The Microsoft Graph service root URL uses the following format for all calls to Microsoft Graph.</span></span> <span data-ttu-id="045e4-208">`https://graph.microsoft.com/{version}/me/onenote/` El segmento `version` de la URL representa la versión de Microsoft Graph que quiere usar.</span><span class="sxs-lookup"><span data-stu-id="045e4-208">`https://graph.microsoft.com/{version}/me/onenote/`  The `version` segment in the URL represents the version of Microsoft Graph that you want to use.</span></span> <span data-ttu-id="045e4-209">Use `v1.0` para código de producción estable.</span><span class="sxs-lookup"><span data-stu-id="045e4-209">Use `v1.0` for stable production code.</span></span> <span data-ttu-id="045e4-210">Use `beta` para probar una característica que esté en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="045e4-210">Use `beta` to try out a feature that's in development.</span></span> <span data-ttu-id="045e4-211">Las características y funciones en versión beta pueden cambiar, por lo que no le recomendamos que las use en el código de producción.</span><span class="sxs-lookup"><span data-stu-id="045e4-211">Features and functionality in beta may change, so you shouldn't use it in your production code.</span></span> <span data-ttu-id="045e4-212">Use `me` para contenido de OneNote al que puede obtener acceso el usuario actual (contenido compartido y del que sea propietario).</span><span class="sxs-lookup"><span data-stu-id="045e4-212">Use `me` for OneNote content that the current user can access (owned and shared).</span></span> <span data-ttu-id="045e4-213">Use `users/{id}` para contenido de OneNote que el usuario especificado (en la URL) compartió con el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="045e4-213">Use `users/{id}` for OneNote content that the specified user (in the URL) has shared with the current user.</span></span> <span data-ttu-id="045e4-214">Use [Microsoft Graph](https://graph.microsoft.com/v1.0/users) para obtener identificadores de usuario.</span><span class="sxs-lookup"><span data-stu-id="045e4-214">Use the [Microsoft Graph](https://graph.microsoft.com/v1.0/users) to get user IDs.</span></span> 


<a name="permissions"></a>
## <a name="permissions"></a><span data-ttu-id="045e4-215">Permisos</span><span class="sxs-lookup"><span data-stu-id="045e4-215">Permissions</span></span>

<span data-ttu-id="045e4-216">Para crear páginas de OneNote, necesitará solicitar los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="045e4-216">To create OneNote pages, you'll need to request appropriate permissions.</span></span> <span data-ttu-id="045e4-217">Seleccione el nivel inferior de permisos que necesita la aplicación para funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="045e4-217">Choose the lowest level of permissions that your app needs to do its work.</span></span>

<span data-ttu-id="045e4-218">Seleccione entre:</span><span class="sxs-lookup"><span data-stu-id="045e4-218">Choose from:</span></span> 
- <span data-ttu-id="045e4-219">Notes.Create</span><span class="sxs-lookup"><span data-stu-id="045e4-219">Notes.Create</span></span>
- <span data-ttu-id="045e4-220">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="045e4-220">Notes.ReadWrite</span></span>
- <span data-ttu-id="045e4-221">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="045e4-221">Notes.ReadWrite.All</span></span>

<span data-ttu-id="045e4-222">Para obtener más información sobre los ámbitos de permiso y cómo funcionan, vea [Referencias de permisos de Microsoft Graph](permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="045e4-222">For more information about permission scopes and how they work, see [Microsoft Graph permissions reference](permissions_reference.md).</span></span>




<a name="see-also"></a>
## <a name="additional-resources"></a><span data-ttu-id="045e4-223">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="045e4-223">Additional resources</span></span>

- [<span data-ttu-id="045e4-224">Agregar imágenes y archivos</span><span class="sxs-lookup"><span data-stu-id="045e4-224">Add images and files</span></span>](onenote_images_files.md)
- [<span data-ttu-id="045e4-225">Crear elementos con posición absoluta</span><span class="sxs-lookup"><span data-stu-id="045e4-225">Create absolute positioned elements</span></span>](onenote-abs-pos.md)  
- [<span data-ttu-id="045e4-226">Extraer datos</span><span class="sxs-lookup"><span data-stu-id="045e4-226">Extract data</span></span>](onenote-extract-data.md)
- [<span data-ttu-id="045e4-227">Usar etiquetas de notas</span><span class="sxs-lookup"><span data-stu-id="045e4-227">Use note tags</span></span>](onenote-note-tags.md)
- [<span data-ttu-id="045e4-228">Integración con OneNote</span><span class="sxs-lookup"><span data-stu-id="045e4-228">Integrate with OneNote</span></span>](integrate_with_onenote.md)
- [<span data-ttu-id="045e4-229">Blog para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="045e4-229">OneNote Developer Blog</span></span>](http://go.microsoft.com/fwlink/?LinkID=390183)
- [<span data-ttu-id="045e4-230">Preguntas de desarrollo de OneNote en Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="045e4-230">OneNote development questions on Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkID=390182)
- [<span data-ttu-id="045e4-231">Repositorios de OneNote en GitHub</span><span class="sxs-lookup"><span data-stu-id="045e4-231">OneNote GitHub repos</span></span>](http://go.microsoft.com/fwlink/?LinkID=390178)  

