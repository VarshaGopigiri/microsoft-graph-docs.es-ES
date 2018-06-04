
# <a name="add-images-videos-and-files-to-onenote-pages"></a><span data-ttu-id="e68e7-101">Agregar imágenes, vídeos y archivos a páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="e68e7-101">Add images, videos, and files to OneNote pages</span></span>

<span data-ttu-id="e68e7-102">*__Se aplica a:__ blocs de notas para consumidores de OneDrive | blocs de notas para empresa de Office 365*</span><span class="sxs-lookup"><span data-stu-id="e68e7-102">*__Applies to:__ Consumer notebooks on OneDrive | Enterprise notebooks on Office 365*</span></span>

<span data-ttu-id="e68e7-103">Puede usar elementos **img**, **object** y **iframe** para agregar imágenes, vídeos y archivos a una página de OneNote cuando [cree](onenote-create-page.md) o [actualice](onenote_update_page.md) la página.</span><span class="sxs-lookup"><span data-stu-id="e68e7-103">You can use **img**, **object**, and **iframe** elements to add images, videos, and files to a OneNote page when you're [creating](onenote-create-page.md) or [updating](onenote_update_page.md) the page.</span></span> 

- <span data-ttu-id="e68e7-104">Use **img** para representar una imagen en la página.</span><span class="sxs-lookup"><span data-stu-id="e68e7-104">Use **img** to render an image on the page.</span></span>
- <span data-ttu-id="e68e7-105">Use **iframe** para insertar un vídeo en la página.</span><span class="sxs-lookup"><span data-stu-id="e68e7-105">Use **iframe** to embed a video on the page.</span></span>
- <span data-ttu-id="e68e7-106">Use **object** para agregar un archivo adjunto a la página.</span><span class="sxs-lookup"><span data-stu-id="e68e7-106">Use **object** to add a file attachment to the page.</span></span>


<a name="images"></a>
## <a name="adding-images"></a><span data-ttu-id="e68e7-107">Agregar imágenes</span><span class="sxs-lookup"><span data-stu-id="e68e7-107">Adding images</span></span>

<span data-ttu-id="e68e7-108">Las imágenes pueden agregarse mediante una dirección URL de referencia o enviando datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="e68e7-108">Images can be added by URL reference or by sending raw data.</span></span> <span data-ttu-id="e68e7-109">Microsoft Graph admite los siguientes métodos para agregar imágenes, logotipos y fotos a páginas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e68e7-109">Microsoft Graph supports the following methods of adding images, logos, and photos to OneNote pages.</span></span> 

[<span data-ttu-id="e68e7-110">Agregar una imagen pública desde la web</span><span class="sxs-lookup"><span data-stu-id="e68e7-110">Add a public image from the web</span></span>](#add-a-public-image-from-the-web)  
<span data-ttu-id="e68e7-111">Use `img` con `src="http://image-url"` y especifique la dirección URL de una imagen de acceso público.</span><span class="sxs-lookup"><span data-stu-id="e68e7-111">Use `img` with `src="http://image-url"` and specify the URL of a publicly accessible image.</span></span> <span data-ttu-id="e68e7-112">Representa la imagen en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e68e7-112">Renders the image on the OneNote page.</span></span></p>
[<span data-ttu-id="e68e7-113">Agregar una imagen con datos binarios</span><span class="sxs-lookup"><span data-stu-id="e68e7-113">Add an image using binary data</span></span>](#add-an-image-using-binary-data)</p>
<span data-ttu-id="e68e7-114">Use `img` con `src="name:image-block-name"` y envíe el archivo de imagen en una parte de datos de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="e68e7-114">Use `img` with `src="name:image-block-name"` and send the image file in a data part of a multipart request.</span></span> <span data-ttu-id="e68e7-115">Representa la imagen en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e68e7-115">Renders the image on the OneNote page.</span></span></p>
[<span data-ttu-id="e68e7-116">Agregar una instantánea de página web</span><span class="sxs-lookup"><span data-stu-id="e68e7-116">Add a webpage snapshot</span></span>](#add-a-webpage-snapshot)</p>
<span data-ttu-id="e68e7-117">Use `img` con `data-render-src="http://webpage-url"` y especifique la dirección URL de una página web.</span><span class="sxs-lookup"><span data-stu-id="e68e7-117">Use `img` with `data-render-src="http://webpage-url"` and specify the URL of a webpage.</span></span> <span data-ttu-id="e68e7-118">Representa una instantánea de la página web completa en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e68e7-118">Renders a snapshot of the whole webpage on the OneNote page.</span></span></p>
[<span data-ttu-id="e68e7-119">Agregar una imagen representada desde HTML</span><span class="sxs-lookup"><span data-stu-id="e68e7-119">Add an image rendered from HTML</span></span>](#add-an-image-rendered-from-html)</p>
<span data-ttu-id="e68e7-120">Use `img` con `data-render-src="name:html-block-name"` y envíe el HTML en la parte de datos de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="e68e7-120">Use `img` with `data-render-src="name:html-block-name"` and send HTML in the data part of a multipart request.</span></span> <span data-ttu-id="e68e7-121">Representa el HTML como una imagen en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e68e7-121">Renders the HTML as an image on the OneNote page.</span></span></p>
[<span data-ttu-id="e68e7-122">Agregar imágenes de contenidos de archivo PDF</span><span class="sxs-lookup"><span data-stu-id="e68e7-122">Add images of PDF file contents</span></span>](#add-images-of-pdf-file-contents)</p>
<span data-ttu-id="e68e7-123">Use `<img data-render-src="name:part-name" />` y envíe el archivo PDF en la parte de datos de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="e68e7-123">Use `<img data-render-src="name:part-name" />` and send the PDF file in the data part of a multipart request.</span></span> <span data-ttu-id="e68e7-124">Representa cada página PDF como una imagen independiente en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e68e7-124">Renders each PDF page as a separate image on the OneNote page.</span></span></p>
[<span data-ttu-id="e68e7-125">Agregar un archivo de imagen como un archivo adjunto</span><span class="sxs-lookup"><span data-stu-id="e68e7-125">Add an image file as a file attachment</span></span>](#add-an-image-file-as-an-attachment)</p>
<span data-ttu-id="e68e7-126">Use `object` con `data="name:file-block-name" data-attachment="file-name.file-ext" type="media-type"` y envíe un archivo de imagen en la parte de datos de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="e68e7-126">Use `object` with `data="name:file-block-name" data-attachment="file-name.file-ext" type="media-type"` and send an image file in the data part of a multipart request.</span></span> <span data-ttu-id="e68e7-127">Agrega un archivo adjunto a la página de OneNote y muestra un icono de archivo.</span><span class="sxs-lookup"><span data-stu-id="e68e7-127">Adds a file attachment to the OneNote page and displays a file icon.</span></span></p>

> <span data-ttu-id="e68e7-128">**Nota:** Para obtener las imágenes en una página de OneNote, primero envíe una [solicitud GET para el contenido de la página](onenote-get-content.md#page-html-content).</span><span class="sxs-lookup"><span data-stu-id="e68e7-128">**Note:** To get images on a OneNote page, first send a [GET request for the page content](onenote-get-content.md#page-html-content).</span></span> <span data-ttu-id="e68e7-129">Esto devuelve las direcciones URL a los recursos de la imagen en la página.</span><span class="sxs-lookup"><span data-stu-id="e68e7-129">This returns the URLs to the image resources on the page.</span></span> <span data-ttu-id="e68e7-130">Después separe las [solicitudes GET a los recursos de imagen](onenote-get-content.md#image-or-other-file-resource).</span><span class="sxs-lookup"><span data-stu-id="e68e7-130">Then you separate [GET requests to the image resources](onenote-get-content.md#image-or-other-file-resource).</span></span>


<span data-ttu-id="e68e7-131">**Atributos de imagen**</span><span class="sxs-lookup"><span data-stu-id="e68e7-131">**Image attributes**</span></span> 

<span data-ttu-id="e68e7-132">Un elemento **img** puede, opcionalmente, incluir los atributos **alt**, **height** y **width**, y los atributos de estilo **max-width** y **max-height**.</span><span class="sxs-lookup"><span data-stu-id="e68e7-132">An **img** element can optionally include **alt**, **height**, and **width** attributes, and the style attributes **max-width** and **max-height**.</span></span>

<span data-ttu-id="e68e7-133">**Tipos de elementos multimedia de imagen**</span><span class="sxs-lookup"><span data-stu-id="e68e7-133">**Image media types**</span></span>

<span data-ttu-id="e68e7-134">Microsoft Graph es compatible con los tipos de imagen BMP, PNG, GIF, JPEG y TIFF.</span><span class="sxs-lookup"><span data-stu-id="e68e7-134">Microsoft Graph supports TIFF, PNG, GIF, JPEG, and BMP image types.</span></span> <span data-ttu-id="e68e7-135">Para capturar una imagen que usa un formato diferente que no quiere convertir, [envíe los datos binarios](#add-an-image-using-binary-data) en una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="e68e7-135">To capture an image that uses a different format that you don't want to convert, [send the binary data](#add-an-image-using-binary-data) in a multipart request.</span></span> <span data-ttu-id="e68e7-136">No es necesario usar Base64 ni codificar los datos binarios con otros formatos.</span><span class="sxs-lookup"><span data-stu-id="e68e7-136">You don't need to use Base64 or otherwise encode the binary data that you send.</span></span>

> <span data-ttu-id="e68e7-137">**Nota**: La API de OneNote detecta automáticamente el tipo de imagen de entrada original y lo devuelve como el atributo **data-fullres-src-type** en el [HTML de salida](onenote_input_output_html.md#output-html).</span><span class="sxs-lookup"><span data-stu-id="e68e7-137">**Note:** The OneNote APIs automatically detect the input image type, and returns it as the **data-fullres-src-type** in the output HTML.</span></span> <span data-ttu-id="e68e7-138">La API también devuelve el tipo de imagen de la imagen optimizada en **data-src-type**.</span><span class="sxs-lookup"><span data-stu-id="e68e7-138">The API also returns the image type of the optimized image in **data-src-type**.</span></span>
 
<span data-ttu-id="e68e7-139">Consulte las [limitaciones](#size-limitations-for-post-pages-requests) que se aplican al crear páginas que contienen archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="e68e7-139">See [limitations](#size-limitations-for-post-pages-requests) that apply when creating pages that contain media.</span></span>


<a name="image-img-url-src"></a>
### <a name="add-a-public-image-from-the-web"></a><span data-ttu-id="e68e7-140">Agregar una imagen pública desde la web</span><span class="sxs-lookup"><span data-stu-id="e68e7-140">Add a public image from the web</span></span>

<span data-ttu-id="e68e7-141">En el HTML de entrada de su solicitud, incluya `<img src="http://..." />` y especifique la dirección URL de una imagen de acceso público para el atributo **src**.</span><span class="sxs-lookup"><span data-stu-id="e68e7-141">In the input HTML of your request, include  `<img src="http://..." />` and specify the URL of a publicly accessible image for the **src** attribute.</span></span>

```
Content-Type: multipart/form-data; boundary=MyAppPartBoundary
Authorization: Bearer {access-token}

--MyAppPartBoundary
Content-Disposition: form-data; name="Presentation"
Content-Type: text/html

<!DOCTYPE html>
<html>
  <head>
    <title>A page with an image: Public URL</title>
    <meta name="created" value="2015-11-11T12:45:00.000-8:00"/>
  </head>
  <body>
    <p>This page displays an image from the web.</p>
    <img src="http://..." width="300"/>
  </body>
</html>

--MyAppPartBoundary--  
```

<a name="image-img-binary-src"></a>
### <a name="add-an-image-using-binary-data"></a><span data-ttu-id="e68e7-142">Agregar una imagen con datos binarios</span><span class="sxs-lookup"><span data-stu-id="e68e7-142">Add an image using binary data</span></span>

<span data-ttu-id="e68e7-143">En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<img src="name:part-name" />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene los datos de imagen binarios.</span><span class="sxs-lookup"><span data-stu-id="e68e7-143">In the input HTML of your request's **Presentation** part, include  `<img src="name:part-name" />`, where *part-name* is the unique identifier for the data part in your [multipart request](onenote-create-page.md#example-request) that contains the binary image data.</span></span> <span data-ttu-id="e68e7-144">Solo tiene que enviar los datos binarios, no use Base64 ni los codifique con otros formatos.</span><span class="sxs-lookup"><span data-stu-id="e68e7-144">The image data is the binary file data; don't use Base64 or otherwise encode it.</span></span>

```
Content-Type: multipart/form-data; boundary=MyAppPartBoundary
Authorization: Bearer {access-token}

--MyAppPartBoundary
Content-Disposition: form-data; name="Presentation"
Content-Type: text/html

<!DOCTYPE html>
<html>
  <head>
    <title>A page with an image: Image binary data</title>
    <meta name="created" value="2015-11-11T12:45:00.000-8:00"/>
  </head>
  <body>
    <p>This page displays the uploaded image.</p>
    <img src="name:image-block-name" alt="a cool image" width="500"/>
  </body>
</html>

--MyAppPartBoundary
Content-Disposition: form-data; name="MyAppPictureId"
Content-Type: image/jpeg

... image binary data ...

--MyAppPartBoundary--  
```


<a name="image-img-url-data-render-src"></a>
### <a name="add-a-webpage-snapshot"></a><span data-ttu-id="e68e7-145">Agregar una instantánea de página web</span><span class="sxs-lookup"><span data-stu-id="e68e7-145">Add a webpage snapshot</span></span>

<span data-ttu-id="e68e7-146">Puede usar Microsoft Graph para tomar instantáneas de páginas web completas e insertarlas en otras páginas.</span><span class="sxs-lookup"><span data-stu-id="e68e7-146">You can use Microsoft Graph to snapshot entire webpages and insert them into new pages.</span></span> <span data-ttu-id="e68e7-147">Este método es útil para archivar páginas web o capturar páginas web complejas con características que no son compatibles con OneNote (por ejemplo, algunas CSS).</span><span class="sxs-lookup"><span data-stu-id="e68e7-147">This method is useful to archive webpages or capture complex webpages that have features that OneNote doesn't support (like some CSS).</span></span>  

<span data-ttu-id="e68e7-148">En el HTML de entrada de su solicitud, incluya `<img src="http://..." />` y especifique la dirección URL de la página que desea insertar para el atributo **src**.</span><span class="sxs-lookup"><span data-stu-id="e68e7-148">In the input HTML of your request, include  `<img src="http://..." />` and specify the URL of the webpage you want to insert for the **src** attribute.</span></span>

```
Content-Type: multipart/form-data; boundary=MyAppPartBoundary
Authorization: Bearer {access-token}

--MyAppPartBoundary
Content-Disposition: form-data; name="Presentation"
Content-Type: text/html

<!DOCTYPE html>
<html>
  <head>
    <title>A page with an image: Webpage capture</title>
    <meta name="created" value="2015-11-11T12:45:00.000-8:00"/>
  </head>
  <body>
    <p>This page displays an image of the webpage.</p>
    <img data-render-src="http://www.onenote.com" width="200"/>
  </body>
</html>

--MyAppPartBoundary--  
```


<a name="image-img-binary-data-render-src"></a>
### <a name="add-an-image-rendered-from-html"></a><span data-ttu-id="e68e7-149">Agregar una imagen representada desde HTML</span><span class="sxs-lookup"><span data-stu-id="e68e7-149">Add an image rendered from HTML</span></span>
<span data-ttu-id="e68e7-150">Al pasar el código HTML como un bloque de datos, asegúrese de que no hay ningún contenido activo que requiera credenciales de usuario o un complemento del explorador cargado previamente.</span><span class="sxs-lookup"><span data-stu-id="e68e7-150">When you pass the HTML as a data-block, be sure there is no active content that would require user credentials, or a pre-loaded browser plug-in.</span></span> <span data-ttu-id="e68e7-151">El motor que Microsoft Graph usa para representar la página HTML en una imagen no tiene la capacidad de hacer que un usuario inicie sesión y no incluye los complementos, como Adobe Flash, Apple QuickTime y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="e68e7-151">The engine that Microsoft Graph uses to render the HTML page into an image has no ability to log in a user, and doesn't include plug-ins like Adobe Flash, Apple QuickTime, and so-on.</span></span> <span data-ttu-id="e68e7-152">Eso también implica que el contenido que se carga dinámicamente, como el que puede incluir un script de AJAX, no aparecerá si para obtener los datos se requieren credenciales de inicio de sesión de usuario o cookies.</span><span class="sxs-lookup"><span data-stu-id="e68e7-152">That also means that dynamically-loaded content, like might come with an AJAX script, won't appear if getting the data requires user login credentials or cookies.</span></span>

<span data-ttu-id="e68e7-153">En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<img data-render-src="name:part-name" />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene el HTML.</span><span class="sxs-lookup"><span data-stu-id="e68e7-153">In the input HTML of your request's **Presentation** part, include  `<img data-render-src="name:part-name" />`, where *part-name* is the unique identifier for the data part in your [multipart request](onenote-create-page.md#example-request) that contains the HTML.</span></span>

```
Content-Type: multipart/form-data; boundary=MyAppPartBoundary
Authorization: Bearer {access-token}

--MyAppPartBoundary
Content-Disposition: form-data; name="Presentation"
Content-Type: text/html

<!DOCTYPE html>
<html>
  <head>
    <title>A page with an image: HTML block</title>
    <meta name="created" value="2015-11-11T12:45:00.000-8:00"/>
  </head>
  <body>
    <p>This page displays the block of HTML as an image.</p>
    <img data-render-src="name:html-block-name" alt="a cool image" width="500"/>
  </body>
</html>

--MyAppPartBoundary
Content-Disposition: form-data; name="html-block-name"
Content-Type: text/html

<html>
<body>
<h1>This HTML will render as an image</h1>
<p><b>Don't</b> try to embed another <i>data-render-src</i> type-image inside the HTML part--
it won't work. Instead, use URL-based real images like this:</p>
<img src="http://cdn.onenote.net/1664161560_Images/OneNote.ico" />
</body>
</html>

--MyAppPartBoundary--  
```


<a name="image-object"></a>
### <a name="add-an-image-file-as-an-attachment"></a><span data-ttu-id="e68e7-154">Agregar un archivo de imagen como datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="e68e7-154">Add an image file as an attachment</span></span>

<span data-ttu-id="e68e7-155">En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<object data="name:part-name" data-attachment="file-name.file-ext" type="media-type/media-subtype" />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene los datos de imagen binarios.</span><span class="sxs-lookup"><span data-stu-id="e68e7-155">In the input HTML of your request's **Presentation** part, include  `<object data="name:part-name" data-attachment="file-name.file-ext" type="media-type/media-subtype" />`, where *part-name* is the unique identifier for the data part in your [multipart request](onenote-create-page.md#example-request) that contains the binary image data.</span></span> <span data-ttu-id="e68e7-156">Solo tiene que enviar los datos binarios, no use Base64 ni los codifique con otros formatos.</span><span class="sxs-lookup"><span data-stu-id="e68e7-156">The image data is the binary file data; don't use Base64 or otherwise encode it.</span></span>

```
Content-Type: multipart/form-data; boundary=MyAppPartBoundary
Authorization: Bearer {access-token}

--MyAppPartBoundary
Content-Disposition: form-data; name="Presentation"
Content-Type: text/html

<!DOCTYPE html>
<html>
  <head>
    <title>A page with an image: Binary image data as file attachment</title>
    <meta name="created" value="2015-11-11T12:45:00.000-8:00"/>
  </head>
  <body>
    <p>This page contains the image as a file attachment.</p>
    <object data-attachment="image-file.jpg" data="name:image-block-name" type="image/jpeg" />
  </body>
</html>

--MyAppPartBoundary
Content-Disposition: form-data; name="logo1-file"
Content-Type: image/jpeg

... binary file data ...

--MyAppPartBoundary--
```

<span data-ttu-id="e68e7-157">Obtenga más información sobre [tipos de archivos multimedia](#file-media-types).</span><span class="sxs-lookup"><span data-stu-id="e68e7-157">Learn more about [file media types](#file-media-types).</span></span>



<a name="videos"></a>
## <a name="adding-videos"></a><span data-ttu-id="e68e7-158">Agregar vídeos</span><span class="sxs-lookup"><span data-stu-id="e68e7-158">Adding videos</span></span>

<span data-ttu-id="e68e7-159">Puede insertar vídeos en páginas de OneNote con `<iframe data-original-src="http://..." />` en el HTML de entrada.</span><span class="sxs-lookup"><span data-stu-id="e68e7-159">You can embed videos in OneNote pages using `<iframe data-original-src="http://..." />` in the input HTML.</span></span> 

<span data-ttu-id="e68e7-160">**Sitios de vídeo admitidos**</span><span class="sxs-lookup"><span data-stu-id="e68e7-160">**Supported video sites**</span></span>

- <span data-ttu-id="e68e7-161">Dailymotion</span><span class="sxs-lookup"><span data-stu-id="e68e7-161">Dailymotion</span></span>
- <span data-ttu-id="e68e7-162">Office Mix</span><span class="sxs-lookup"><span data-stu-id="e68e7-162">Office Mix</span></span>
- <span data-ttu-id="e68e7-163">Sway</span><span class="sxs-lookup"><span data-stu-id="e68e7-163">Sway</span></span>
- <span data-ttu-id="e68e7-164">Sketchfab</span><span class="sxs-lookup"><span data-stu-id="e68e7-164">Sketchfab</span></span>
- <span data-ttu-id="e68e7-165">TED</span><span class="sxs-lookup"><span data-stu-id="e68e7-165">TED</span></span>
- <span data-ttu-id="e68e7-166">YouTube</span><span class="sxs-lookup"><span data-stu-id="e68e7-166">YouTube</span></span>
- <span data-ttu-id="e68e7-167">Vimeo</span><span class="sxs-lookup"><span data-stu-id="e68e7-167">Vimeo</span></span>
- <span data-ttu-id="e68e7-168">Vine</span><span class="sxs-lookup"><span data-stu-id="e68e7-168">Vine</span></span>

<span data-ttu-id="e68e7-169">**Atributos iframe**</span><span class="sxs-lookup"><span data-stu-id="e68e7-169">**iframe attributes**</span></span>

<span data-ttu-id="e68e7-170">**data-original-src**</span><span class="sxs-lookup"><span data-stu-id="e68e7-170">**data-original-src**</span></span></p>
<span data-ttu-id="e68e7-171">Necesario.</span><span class="sxs-lookup"><span data-stu-id="e68e7-171">Required.</span></span> <span data-ttu-id="e68e7-172">La dirección URL del vídeo.</span><span class="sxs-lookup"><span data-stu-id="e68e7-172">The URL of the video source.</span></span><br /><span data-ttu-id="e68e7-173">Ejemplo: `data-original-src="https://www.youtube.com/watch?v=3Ztr44aKmQ8"`</span><span class="sxs-lookup"><span data-stu-id="e68e7-173">Example: `data-original-src="https://www.youtube.com/watch?v=3Ztr44aKmQ8"`</span></span></p>
<span data-ttu-id="e68e7-174">**width**</span><span class="sxs-lookup"><span data-stu-id="e68e7-174">**width**</span></span></p>
<span data-ttu-id="e68e7-175">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e68e7-175">Optional.</span></span> <span data-ttu-id="e68e7-176">La anchura del iframe que contiene el vídeo.</span><span class="sxs-lookup"><span data-stu-id="e68e7-176">The width of the iframe that contains the video.</span></span> <span data-ttu-id="e68e7-177">El valor predeterminado es 480.</span><span class="sxs-lookup"><span data-stu-id="e68e7-177">Default is 480.</span></span><br /><span data-ttu-id="e68e7-178">Ejemplo: `width="300"`</span><span class="sxs-lookup"><span data-stu-id="e68e7-178">Example: `width="300"`</span></span></p>
<span data-ttu-id="e68e7-179">**height**</span><span class="sxs-lookup"><span data-stu-id="e68e7-179">**height**</span></span></p>
<span data-ttu-id="e68e7-180">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e68e7-180">Optional.</span></span> <span data-ttu-id="e68e7-181">La altura del iframe que contiene el vídeo.</span><span class="sxs-lookup"><span data-stu-id="e68e7-181">The height of the iframe that contains the video.</span></span> <span data-ttu-id="e68e7-182">El valor predeterminado es 360.</span><span class="sxs-lookup"><span data-stu-id="e68e7-182">Default is 360.</span></span><br /><span data-ttu-id="e68e7-183">Ejemplo: `height="300"`</span><span class="sxs-lookup"><span data-stu-id="e68e7-183">Example: `height="300"`</span></span></p>

<span data-ttu-id="e68e7-184">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="e68e7-184">**Example**</span></span>

<span data-ttu-id="e68e7-185">En el HTML de entrada de su solicitud, incluya `<iframe data-original-src="http://..." />` y especifique la dirección URL del vídeo para el atributo **data-original-src**.</span><span class="sxs-lookup"><span data-stu-id="e68e7-185">In the input HTML of your request, include `<iframe data-original-src="http://..." />` and specify the URL of the video for the **data-original-src** attribute.</span></span>

```
Content-Type: multipart/form-data; boundary=MyAppPartBoundary
Authorization: Bearer {access-token}

--MyAppPartBoundary
Content-Disposition: form-data; name="Presentation"
Content-Type: text/html

<!DOCTYPE html>
<html>
    <head>
        <title>A page with an embedded video</title>
    </head>
    <body>
        <iframe data-original-src="https://www.youtube.com/watch?v=3Ztr44aKmQ8" width="340" height="280"/>
    </body>
</html>

--MyAppPartBoundary--
```


<a name="files"></a>
## <a name="adding-files"></a><span data-ttu-id="e68e7-186">Agregar archivos</span><span class="sxs-lookup"><span data-stu-id="e68e7-186">Adding installation files</span></span>

<span data-ttu-id="e68e7-187">Puede agregar archivos adjuntos a las páginas de OneNote con un elemento **object** en el HTML de entrada.</span><span class="sxs-lookup"><span data-stu-id="e68e7-187">You can add file attachments to OneNote pages using an **object** element in the input HTML.</span></span> <span data-ttu-id="e68e7-188">Si va a agregar un archivo PDF, puede usar un elemento **img** para representar las páginas del PDF como imágenes.</span><span class="sxs-lookup"><span data-stu-id="e68e7-188">If you're adding a PDF file, you can use an **img** element to render the PDF pages as images.</span></span> 

[<span data-ttu-id="e68e7-189">Agregar un archivo adjunto</span><span class="sxs-lookup"><span data-stu-id="e68e7-189">Add a file attachment</span></span>](#add-a-file-attachment)</p>
<span data-ttu-id="e68e7-190">Use `<object .../>` y envíe el archivo en una parte de datos de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="e68e7-190">Use `<object .../>` and send the file in a data part of a multipart request.</span></span> <span data-ttu-id="e68e7-191">Agrega un archivo adjunto que muestra un icono de archivo en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e68e7-191">Adds a file attachment that displays a file icon on the OneNote page.</span></span></p>
[<span data-ttu-id="e68e7-192">Agregar imágenes de contenidos de archivo PDF</span><span class="sxs-lookup"><span data-stu-id="e68e7-192">Add images of PDF file contents</span></span>](#add-images-of-pdf-file-contents)</p>
<span data-ttu-id="e68e7-193">Use `<img data-render-src="name:part-name" />` y envíe un archivo PDF en la parte de datos de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="e68e7-193">Use `<img data-render-src="name:part-name" />` and send a PDF file in the data part of a multipart request.</span></span> <span data-ttu-id="e68e7-194">Representa cada página PDF como una imagen independiente en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e68e7-194">Renders each PDF page as a separate image on the OneNote page.</span></span></p>

<span data-ttu-id="e68e7-195">**Atributos de archivo**</span><span class="sxs-lookup"><span data-stu-id="e68e7-195">**File attributes**</span></span>

<span data-ttu-id="e68e7-196">El elemento **object** requiere los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="e68e7-196">The **object** element requires the following attributes.</span></span>

<span data-ttu-id="e68e7-197">**data-attachment**</span><span class="sxs-lookup"><span data-stu-id="e68e7-197">**data-attachment**</span></span></p>
<span data-ttu-id="e68e7-198">El nombre de archivo y la extensión para mostrar en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e68e7-198">The file name and extension to display on the OneNote page.</span></span><br /><span data-ttu-id="e68e7-199">Ejemplo: `data-attachment="filename.docx"`</span><span class="sxs-lookup"><span data-stu-id="e68e7-199">Example: `data-attachment="filename.docx"`</span></span></p>
<span data-ttu-id="e68e7-200">**data**</span><span class="sxs-lookup"><span data-stu-id="e68e7-200">**Data**</span></span></p>
<span data-ttu-id="e68e7-201">El nombre de la parte del cuerpo de la solicitud de varias partes que contiene los datos de archivo binario.</span><span class="sxs-lookup"><span data-stu-id="e68e7-201">The name of the body part in the multipart request that contains the binary file data.</span></span> <span data-ttu-id="e68e7-202">Microsoft Graph non admite pasar una referencia de la dirección URL aquí.</span><span class="sxs-lookup"><span data-stu-id="e68e7-202">Microsoft Graph does not support passing a URL reference here.</span></span><br /><span data-ttu-id="e68e7-203">Ejemplo: `data="name:part-name"`</span><span class="sxs-lookup"><span data-stu-id="e68e7-203">Example: `data="name:part-name"`</span></span></p>
<span data-ttu-id="e68e7-204">**type**</span><span class="sxs-lookup"><span data-stu-id="e68e7-204">**type**</span></span></p>
<span data-ttu-id="e68e7-205">El tipo de archivos multimedia, se usa para determinar el icono de archivo que se usará en la página y qué aplicación se inicia cuando el usuario activa el archivo en el dispositivo desde OneNote.</span><span class="sxs-lookup"><span data-stu-id="e68e7-205">type="standardMimeType" indicates the file MIME type. This is used to select the file icon on the page, and also determines which application starts when the user activates the file on the device from OneNote.</span></span><br /><span data-ttu-id="e68e7-206">Ejemplo: `type="application/pdf"`</span><span class="sxs-lookup"><span data-stu-id="e68e7-206">Example: `type="application/pdf"`</span></span></p>


<a name="file-media-types"></a>

### <a name="file-media-types"></a><span data-ttu-id="e68e7-207">Tipos de archivos multimedia</span><span class="sxs-lookup"><span data-stu-id="e68e7-207">File media types</span></span>  
<span data-ttu-id="e68e7-208">Microsoft Graph usa iconos de tipos de archivos multimedia predefinidos para los archivos adjuntos, o un icono genérico cuando la API no reconoce el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="e68e7-208">Microsoft Graph uses predefined file-types icon for attached files, or a generic icon when the API doesn't recognize the file type.</span></span> <span data-ttu-id="e68e7-209">La siguiente tabla muestra algunos tipos de archivo comunes que reconocen la API.</span><span class="sxs-lookup"><span data-stu-id="e68e7-209">The following table shows some common file types that are recognized by the API.</span></span>

- <span data-ttu-id="e68e7-210">application/pdf</span><span class="sxs-lookup"><span data-stu-id="e68e7-210">application/pdf</span></span>  
- <span data-ttu-id="e68e7-211">application/vnd.openxmlformats-officedocument.wordprocessingml.document</span><span class="sxs-lookup"><span data-stu-id="e68e7-211">application/vnd.openxmlformats-officedocument.wordprocessingml.document</span></span>  
- <span data-ttu-id="e68e7-212">application/vnd.openxmlformats-officedocument.presentationml.presentation</span><span class="sxs-lookup"><span data-stu-id="e68e7-212">application/vnd.openxmlformats-officedocument.presentationml.presentation</span></span>
- <span data-ttu-id="e68e7-213">application/vnd.openxmlformats-officedocument.spreadsheetml.sheet</span><span class="sxs-lookup"><span data-stu-id="e68e7-213">application/vnd.openxmlformats-officedocument.spreadsheetml.sheet</span></span>
- <span data-ttu-id="e68e7-214">image/png</span><span class="sxs-lookup"><span data-stu-id="e68e7-214">image/png</span></span>
- <span data-ttu-id="e68e7-215">image/jpeg</span><span class="sxs-lookup"><span data-stu-id="e68e7-215">image/jpeg</span></span>
- <span data-ttu-id="e68e7-216">image/gif</span><span class="sxs-lookup"><span data-stu-id="e68e7-216">image/gif</span></span>
- <span data-ttu-id="e68e7-217">audio/wav</span><span class="sxs-lookup"><span data-stu-id="e68e7-217">audio/wav</span></span>
- <span data-ttu-id="e68e7-218">video/mp4</span><span class="sxs-lookup"><span data-stu-id="e68e7-218">video/mp4</span></span>
- <span data-ttu-id="e68e7-219">application/msword</span><span class="sxs-lookup"><span data-stu-id="e68e7-219">application/msword</span></span>
- <span data-ttu-id="e68e7-220">application/mspowerpoint</span><span class="sxs-lookup"><span data-stu-id="e68e7-220">application/mspowerpoint</span></span>
- <span data-ttu-id="e68e7-221">application/excel</span><span class="sxs-lookup"><span data-stu-id="e68e7-221">application/excel</span></span>

<span data-ttu-id="e68e7-222">Consulte las [limitaciones](#size-limitations-for-post-pages-requests) que se aplican al crear páginas que contienen archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="e68e7-222">See [limitations](#size-limitations-for-post-pages-requests) that apply when creating pages that contain media.</span></span>


<a name="file-object"></a>
### <a name="add-a-file-attachment"></a><span data-ttu-id="e68e7-223">Agregar un archivo adjunto</span><span class="sxs-lookup"><span data-stu-id="e68e7-223">Add a file attachment</span></span>

<span data-ttu-id="e68e7-224">En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<object data="name:part-name" data-attachment="file-name.file-ext" type="media-type/media-subtype" />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene los datos de archivo binario.</span><span class="sxs-lookup"><span data-stu-id="e68e7-224">In the input HTML of your request's **Presentation** part, include  `<object data="name:part-name" data-attachment="file-name.file-ext" type="media-type/media-subtype" />`, where *part-name* is the unique identifier for the data part in your [multipart request](onenote-create-page.md#example-request) that contains the binary file data.</span></span> <span data-ttu-id="e68e7-225">Solo tiene que enviar los datos binarios, no use Base64 ni los codifique con otros formatos.</span><span class="sxs-lookup"><span data-stu-id="e68e7-225">The image data is the binary file data; don't use Base64 or otherwise encode it.</span></span>

```
Content-Type: multipart/form-data; boundary=MyAppPartBoundary
Authorization: Bearer {access-token}

--MyAppPartBoundary
Content-Disposition: form-data; name="Presentation"
Content-Type: text/html

<!DOCTYPE html>
<html>
  <head>
    <title>A page with an image file attachment</title>
  </head>
  <body>
    <p>This is an image file attachment.</p>
    <object data-attachment="Logo.jpg" data="name:logo1-file" type="image/jpeg" />
  </body>
</html>

--MyAppPartBoundary
Content-Disposition: form-data; name="logo1-file"
Content-Type: image/jpeg

... binary file data ...

--MyAppPartBoundary--
```


<a name="file-binary-data-render-src"></a>
### <a name="add-images-of-pdf-file-contents"></a><span data-ttu-id="e68e7-226">Agregar imágenes de contenidos de archivo PDF</span><span class="sxs-lookup"><span data-stu-id="e68e7-226">Add images of PDF file contents</span></span>

<span data-ttu-id="e68e7-227">En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<img data-render-src="name:part-name" ... />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene los datos de archivo binario.</span><span class="sxs-lookup"><span data-stu-id="e68e7-227">In the input HTML of your request's **Presentation** part, include  `<img data-render-src="name:part-name" ... />`, where *part-name* is the unique identifier for the data part in your [multipart request](onenote-create-page.md#example-request) that contains the binary file data.</span></span> <span data-ttu-id="e68e7-228">Solo tiene que enviar los datos binarios, no use Base64 ni los codifique con otros formatos.</span><span class="sxs-lookup"><span data-stu-id="e68e7-228">The image data is the binary file data; don't use Base64 or otherwise encode it.</span></span>

```
Content-Type: multipart/form-data; boundary=MyAppPartBoundary
Authorization: Bearer {access-token}

--MyAppPartBoundary
Content-Disposition: form-data; name="Presentation"
Content-Type: text/html

<!DOCTYPE html>
<html>
  <head>
    <title>A page with images of the pages of a PDF file</title>
  </head>
  <body>
    <p>The pages of this PDF file render as images.</p>
    <img data-render-src="name:file-part" alt="PDF file as images" width="500"/>
  </body>
</html>

--MyAppPartBoundary
Content-Disposition: form-data; name="file-part"
Content-Type: application/pdf

... binary file data ...

--MyAppPartBoundary--  
```


<a name="size-limits"></a>
## <a name="size-limitations-for-post-pages-requests"></a><span data-ttu-id="e68e7-229">Limitaciones de tamaño para las solicitudes de páginas POST</span><span class="sxs-lookup"><span data-stu-id="e68e7-229">Size limitations for POST pages requests</span></span>

<span data-ttu-id="e68e7-230">Al enviar datos de imagen y de archivo, tenga en cuenta estas limitaciones: <!--TODO: check these--></span><span class="sxs-lookup"><span data-stu-id="e68e7-230">When sending image and file data, be aware of these limitations: <!--TODO: check these--></span></span>

- <span data-ttu-id="e68e7-231">El límite de tamaño total de POST es ~ 70 MB, incluyendo imágenes, archivos y otros datos.</span><span class="sxs-lookup"><span data-stu-id="e68e7-231">The total POST size limit is ~70 MB, including images, files, and other data.</span></span> <span data-ttu-id="e68e7-232">El límite se ve afectado por la codificación de bajada, por lo que no hay ningún límite fijo del número de bytes.</span><span class="sxs-lookup"><span data-stu-id="e68e7-232">The actual limit is affected by downstream encoding, so there's no fixed byte-count limit.</span></span> <span data-ttu-id="e68e7-233">Las solicitudes que superan el límite pueden producir resultados no confiables.</span><span class="sxs-lookup"><span data-stu-id="e68e7-233">Requests that exceed the limit may produce unreliable results.</span></span>

- <span data-ttu-id="e68e7-234">El límite de cada parte de datos es 25 MB, incluyendo los encabezados de la parte.</span><span class="sxs-lookup"><span data-stu-id="e68e7-234">The limit for each data part is 25 MB, including the part headers.</span></span> <span data-ttu-id="e68e7-235">Microsoft Graph rechaza las partes de datos que superan el límite.</span><span class="sxs-lookup"><span data-stu-id="e68e7-235">Data parts that exceed the limit are rejected by Microsoft Graph.</span></span> 

- <span data-ttu-id="e68e7-236">El número máximo de imágenes por página es 150.</span><span class="sxs-lookup"><span data-stu-id="e68e7-236">The maximum number of images per page is 150.</span></span> <span data-ttu-id="e68e7-237">Al usar el atributo `src="http://..."`, la API omite las etiquetas **img** pasado este límite.</span><span class="sxs-lookup"><span data-stu-id="e68e7-237">Image limit is 150 per page. When using the **src="internetURL"`src="http://..."` attribute, the API ignores <img>** tags beyond the limit.</span></span>

- <span data-ttu-id="e68e7-238">El número máximo de partes de datos es 6 por POST, incluida la parte **Presentation** necesaria.</span><span class="sxs-lookup"><span data-stu-id="e68e7-238">The maximum number of data parts is 6 per POST, including the required **Presentation** part.</span></span>

- <span data-ttu-id="e68e7-239">Cada solicitud puede contener un máximo de cinco elementos **img** que usan **data-render-src**, y un elemento **object** que usa **data-render-src**. Se ignoran las referencias de imagen y archivos adicionales.</span><span class="sxs-lookup"><span data-stu-id="e68e7-239">Each request can contain up to five **img** elements that use **data-render-src** and one **object** elements that uses **data-render-src**. Additional image and file references are ignored.</span></span>

- <span data-ttu-id="e68e7-240">El número máximo de imágenes en un solo POST es 30, independientemente del método que utilice para enviarlas a la API.</span><span class="sxs-lookup"><span data-stu-id="e68e7-240">The maximum number of images in a single POST is 30, no matter which method you use to send them to the API.</span></span> <span data-ttu-id="e68e7-241">Las imágenes adicionales se ignoran.</span><span class="sxs-lookup"><span data-stu-id="e68e7-241">Additional images are ignored.</span></span> <span data-ttu-id="e68e7-242">Si desea capturar una página web que contiene una gran cantidad de imágenes, considere la posibilidad de [capturar toda la página como una instantánea](#add-a-webpage-snapshot).</span><span class="sxs-lookup"><span data-stu-id="e68e7-242">If you want to capture a webpage that contains a lot of images, consider [capturing the whole page as a snapshot](#add-a-webpage-snapshot).</span></span>


## <a name="when-to-use-html-versus-data-render-src"></a><span data-ttu-id="e68e7-243">Cuándo usar HTML o *data-render-src*</span><span class="sxs-lookup"><span data-stu-id="e68e7-243">When to use HTML versus *data-render-src*</span></span> 
<span data-ttu-id="e68e7-244">A la hora de decidir entre colocar el código HTML directamente en la página de OneNote o usar el atributo **data-render-src**, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e68e7-244">When trying to decide between directly putting HTML onto the OneNote page, versus using the data-render-src rendering, consider the following:</span></span>

- <span data-ttu-id="e68e7-245">El código HTML complejo probablemente se envía mejor al motor de representación mediante **data-render-src**, en lugar de intentar modificar el HTML para que se ajuste a lo que Microsoft Graph puede aceptar. </span><span class="sxs-lookup"><span data-stu-id="e68e7-245">Complex HTML is probably best sent to the rendering engine via data-render-src, rather than attempting to modify the HTML to fit into what the oncshort API can accept. This is also true when your HTML includes tags not yet supported (see ).</span></span> <span data-ttu-id="e68e7-246">Esto también es así cuando el código HTML incluye etiquetas que aún no se admiten.</span><span class="sxs-lookup"><span data-stu-id="e68e7-246">This is also true when your HTML includes tags that aren't supported supported.</span></span>

- <span data-ttu-id="e68e7-247">Para la representación precisa de la página, para conservar su diseño y aspecto, probablemente es mejor usar el motor de representación mediante **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="e68e7-247">Accurate page rendering to preserve the layout and look of the page is probably best done with the rendering engine via **data-render-src**.</span></span>

- <span data-ttu-id="e68e7-248">El texto directamente editable a menudo se realiza mejor insertando el código HTML directamente en la página.</span><span class="sxs-lookup"><span data-stu-id="e68e7-248">Directly-editable text is often best done with inserting the HTML directly onto the page. The rendered images are scanned by an optical character recognition (OCR) system, but it's just not the same.</span></span> <span data-ttu-id="e68e7-249">Un sistema de reconocimiento óptico de caracteres (OCR) analiza las imágenes representadas, pero no es lo mismo.</span><span class="sxs-lookup"><span data-stu-id="e68e7-249">Directly-editable text is often best done with inserting the HTML directly onto the page. The rendered images are scanned by an optical character recognition (OCR) system, but it's just not the same.</span></span>

- <span data-ttu-id="e68e7-250">Para las instantáneas puntuales para el historial o el archivo suele ser mejor el método data-render-src.</span><span class="sxs-lookup"><span data-stu-id="e68e7-250">Snapshot-in-time for historical or archival purposes is usually best done with the data-render-src method.</span></span>

- <span data-ttu-id="e68e7-251">Marcar un diseño de página web para las revisiones es algo en lo que realmente destaca el **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="e68e7-251">Marking-up a web page design for revisions is one place the **data-render-src** truly shines.</span></span> <span data-ttu-id="e68e7-252">Con las capacidades de entrada de lápiz de OneNote, puede dibujar en la imagen para indicar los cambios o destacar áreas importantes.</span><span class="sxs-lookup"><span data-stu-id="e68e7-252">Using OneNote's inking capabilities, you can draw on the image to indicate changes or call out important areas.</span></span> <span data-ttu-id="e68e7-253">Tener la página web como una imagen facilita mucho ese proceso.</span><span class="sxs-lookup"><span data-stu-id="e68e7-253">Having the web page as an image makes that a lot easier.</span></span>

- <span data-ttu-id="e68e7-254">Las imágenes muy grandes o las imágenes con formatos que OneNote no acepta directamente a veces pueden reducirse a miniaturas y convertirse con el atributo **data-render-src** más fácilmente que haciéndolo con su propio código.</span><span class="sxs-lookup"><span data-stu-id="e68e7-254">Very large images, or images in formats that OneNote doesn't directly accept can sometimes be thumbnailed and converted with the data-render-src method more easily than by doing it in your own code.</span></span> <span data-ttu-id="e68e7-255">Incluso si la imagen está disponible en línea, incrustar los datos en su POST a veces puede hacer que la página capturada esté disponible antes para usuarios de OneNote, ya que reduce el número total de ciclos de ida y vuelta necesarios para crear la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e68e7-255">You can also send the image data for up to 150 images directly inside the oncshort API POST. This is common when the images are from a mobile device camera, or if your app is running on a hardware device like a scanner or camera. Even if the image is also available on the Internet, embedding the data in your POST can sometimes make the captured page available to OneNote user sooner, by reducing the total number of round-trips needed to build the OneNote page.</span></span>

<span data-ttu-id="e68e7-256">A veces, la mejor forma de determinar qué método funcionará mejor para los usuarios es probar ambas formas al elaborar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e68e7-256">Sometimes, the best way to determine which method will work best for your users is to try it both ways as you develop your app.</span></span>


<a name="permissions"></a>
## <a name="permissions"></a><span data-ttu-id="e68e7-257">Permisos</span><span class="sxs-lookup"><span data-stu-id="e68e7-257">Permissions</span></span>

<span data-ttu-id="e68e7-258">Para crear o actualizar páginas OneNote, debe solicitar los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="e68e7-258">To create or update OneNote pages, you'll need to request appropriate permissions.</span></span> <span data-ttu-id="e68e7-259">Elija el nivel más bajo que necesita la aplicación para hacer su trabajo.</span><span class="sxs-lookup"><span data-stu-id="e68e7-259">Choose the lowest level that your app needs to do its work.</span></span>

<span data-ttu-id="e68e7-260">**Permisos de _páginas POST_**</span><span class="sxs-lookup"><span data-stu-id="e68e7-260">**Permissions for _POST pages_**</span></span>

- <span data-ttu-id="e68e7-261">Notes.Create</span><span class="sxs-lookup"><span data-stu-id="e68e7-261">Notes.Create</span></span>
- <span data-ttu-id="e68e7-262">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e68e7-262">Notes.ReadWrite</span></span>
- <span data-ttu-id="e68e7-263">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e68e7-263">Notes.ReadWrite.All</span></span> 

<span data-ttu-id="e68e7-264">**Permisos de _páginas PATCH_**</span><span class="sxs-lookup"><span data-stu-id="e68e7-264">**Permissions for _PATCH pages_**</span></span>

- <span data-ttu-id="e68e7-265">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e68e7-265">Notes.ReadWrite</span></span>
- <span data-ttu-id="e68e7-266">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e68e7-266">Notes.ReadWrite.All</span></span>

<span data-ttu-id="e68e7-267">Para obtener más información sobre los ámbitos de permiso y cómo funcionan, consulte los [ámbitos de permisos de OneNote](permissions_reference.md#notes-permissions).</span><span class="sxs-lookup"><span data-stu-id="e68e7-267">For more information about how permission scopes work, see [OneNote permission scopes](permissions_reference.md#notes-permissions).</span></span>


<a name="see-also"></a>
## <a name="additional-resources"></a><span data-ttu-id="e68e7-268">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e68e7-268">Additional resources</span></span>

- [<span data-ttu-id="e68e7-269">Integración con OneNote</span><span class="sxs-lookup"><span data-stu-id="e68e7-269">Integrate with OneNote</span></span>](integrate_with_onenote.md)
- [<span data-ttu-id="e68e7-270">Blog para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="e68e7-270">OneNote Developer Blog</span></span>](http://go.microsoft.com/fwlink/?LinkID=390183)
- [<span data-ttu-id="e68e7-271">Preguntas de desarrollo de OneNote en Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="e68e7-271">OneNote development questions on Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkID=390182)
- [<span data-ttu-id="e68e7-272">Repositorios de OneNote en GitHub</span><span class="sxs-lookup"><span data-stu-id="e68e7-272">OneNote GitHub repos</span></span>](http://go.microsoft.com/fwlink/?LinkID=390178)  