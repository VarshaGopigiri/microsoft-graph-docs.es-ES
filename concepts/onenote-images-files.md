---
title: Agregar imágenes, vídeos y archivos a páginas de OneNote
description: " Blocs de notas de empresa en Office 365"
ms.openlocfilehash: bc298339d73b162da6b2e37c314ffedfb76bd193
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092830"
---
# <a name="add-images-videos-and-files-to-onenote-pages"></a><span data-ttu-id="467e8-103">Agregar imágenes, vídeos y archivos a páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="467e8-103">Add images, videos, and files to OneNote pages</span></span>

<span data-ttu-id="467e8-104">**Se aplica a:** Blocs de notas para consumidores de OneDrive | Blocs de notas empresariales de Office 365</span><span class="sxs-lookup"><span data-stu-id="467e8-104">**Applies to** Consumer notebooks on OneDrive | Enterprise notebooks on Office 365</span></span>

<span data-ttu-id="467e8-105">Puede usar elementos **img**, **object** y **iframe** para agregar imágenes, vídeos y archivos a una página de OneNote cuando [cree](onenote-create-page.md) o [actualice](onenote-update-page.md) la página.</span><span class="sxs-lookup"><span data-stu-id="467e8-105">You can use **img**, **object**, and **iframe** elements to add images, videos, and files to a OneNote page when you're [creating](onenote-create-page.md) or [updating](onenote-update-page.md) the page.</span></span> 

- <span data-ttu-id="467e8-106">Use **img** para representar una imagen en la página.</span><span class="sxs-lookup"><span data-stu-id="467e8-106">Use **img** to render an image on the page.</span></span>
- <span data-ttu-id="467e8-107">Use **iframe** para insertar un vídeo en la página.</span><span class="sxs-lookup"><span data-stu-id="467e8-107">Use **iframe** to embed a video on the page.</span></span>
- <span data-ttu-id="467e8-108">Use **object** para agregar un archivo adjunto a la página.</span><span class="sxs-lookup"><span data-stu-id="467e8-108">Use **object** to add a file attachment to the page.</span></span>


<a name="images"></a>

## <a name="adding-images"></a><span data-ttu-id="467e8-109">Agregar imágenes</span><span class="sxs-lookup"><span data-stu-id="467e8-109">Adding images</span></span>

<span data-ttu-id="467e8-110">Las imágenes pueden agregarse mediante una dirección URL de referencia o enviando datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="467e8-110">Images can be added by URL reference or by sending raw data.</span></span> <span data-ttu-id="467e8-111">Microsoft Graph admite los siguientes métodos para agregar imágenes, logotipos y fotos a páginas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="467e8-111">Microsoft Graph supports the following methods of adding images, logos, and photos to OneNote pages.</span></span> 

[<span data-ttu-id="467e8-112">Agregar una imagen pública desde la web</span><span class="sxs-lookup"><span data-stu-id="467e8-112">Add a public image from the web</span></span>](#add-a-public-image-from-the-web)

<span data-ttu-id="467e8-113">Use `img` con `src="https://image-url"` y especifique la dirección URL de una imagen de acceso público.</span><span class="sxs-lookup"><span data-stu-id="467e8-113">Use `img` with `src="https://image-url"` and specify the URL of a publicly accessible image.</span></span> <span data-ttu-id="467e8-114">Representa la imagen en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="467e8-114">Renders the image on the OneNote page.</span></span>

[<span data-ttu-id="467e8-115">Agregar una imagen con datos binarios</span><span class="sxs-lookup"><span data-stu-id="467e8-115">Add an image using binary data</span></span>](#add-an-image-using-binary-data)

<span data-ttu-id="467e8-116">Use `img` con `src="name:image-block-name"` y envíe el archivo de imagen en una parte de datos de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="467e8-116">Use `img` with `src="name:image-block-name"` and send the image file in a data part of a multipart request.</span></span> <span data-ttu-id="467e8-117">Representa la imagen en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="467e8-117">Renders the image on the OneNote page.</span></span>

[<span data-ttu-id="467e8-118">Agregar una instantánea de página web</span><span class="sxs-lookup"><span data-stu-id="467e8-118">Add a webpage snapshot</span></span>](#add-a-webpage-snapshot)

<span data-ttu-id="467e8-119">Use `img` con `data-render-src="https://webpage-url"` y especifique la dirección URL de una página web.</span><span class="sxs-lookup"><span data-stu-id="467e8-119">Use `img` with `data-render-src="https://webpage-url"` and specify the URL of a webpage.</span></span> <span data-ttu-id="467e8-120">Representa una instantánea de la página web completa en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="467e8-120">Renders a snapshot of the whole webpage on the OneNote page.</span></span>

[<span data-ttu-id="467e8-121">Agregar una imagen representada desde HTML</span><span class="sxs-lookup"><span data-stu-id="467e8-121">Add an image rendered from HTML</span></span>](#add-an-image-rendered-from-html)

<span data-ttu-id="467e8-122">Use `img` con `data-render-src="name:html-block-name"` y envíe el HTML en la parte de datos de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="467e8-122">Use `img` with `data-render-src="name:html-block-name"` and send HTML in the data part of a multipart request.</span></span> <span data-ttu-id="467e8-123">Representa el HTML como una imagen en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="467e8-123">Renders the HTML as an image on the OneNote page.</span></span>

[<span data-ttu-id="467e8-124">Agregar imágenes de contenidos de archivo PDF</span><span class="sxs-lookup"><span data-stu-id="467e8-124">Add images of PDF file contents</span></span>](#add-images-of-pdf-file-contents)

<span data-ttu-id="467e8-125">Use `<img data-render-src="name:part-name" />` y envíe el archivo PDF en la parte de datos de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="467e8-125">Use `<img data-render-src="name:part-name" />` and send the PDF file in the data part of a multipart request.</span></span> <span data-ttu-id="467e8-126">Representa cada página PDF como una imagen independiente en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="467e8-126">Renders each PDF page as a separate image on the OneNote page.</span></span>

[<span data-ttu-id="467e8-127">Agregar un archivo de imagen como un archivo adjunto</span><span class="sxs-lookup"><span data-stu-id="467e8-127">Add an image file as a file attachment</span></span>](#add-an-image-file-as-an-attachment)

<span data-ttu-id="467e8-128">Use `object` con `data="name:file-block-name" data-attachment="file-name.file-ext" type="media-type"` y envíe un archivo de imagen en la parte de datos de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="467e8-128">Use `object` with `data="name:file-block-name" data-attachment="file-name.file-ext" type="media-type"` and send an image file in the data part of a multipart request.</span></span> <span data-ttu-id="467e8-129">Agrega un archivo adjunto a la página de OneNote y muestra un icono de archivo.</span><span class="sxs-lookup"><span data-stu-id="467e8-129">Adds a file attachment to the OneNote page and displays a file icon.</span></span>


> <span data-ttu-id="467e8-130">**Nota:** Para obtener las imágenes en una página de OneNote, primero envíe una [solicitud GET para el contenido de la página](onenote-get-content.md#page-html-content).</span><span class="sxs-lookup"><span data-stu-id="467e8-130">**Note:** To get images on a OneNote page, first send a [GET request for the page content](onenote-get-content.md#page-html-content).</span></span> <span data-ttu-id="467e8-131">Esto devuelve las direcciones URL a los recursos de la imagen en la página.</span><span class="sxs-lookup"><span data-stu-id="467e8-131">This returns the URLs to the image resources on the page.</span></span> <span data-ttu-id="467e8-132">Después separe las [solicitudes GET a los recursos de imagen](onenote-get-content.md#image-or-other-file-resource).</span><span class="sxs-lookup"><span data-stu-id="467e8-132">You then separate [GET requests to the image resources](onenote-get-content.md#image-or-other-file-resource).</span></span>


#### <a name="image-attributes"></a><span data-ttu-id="467e8-133">Atributos de imagen</span><span class="sxs-lookup"><span data-stu-id="467e8-133">Image attributes</span></span> 

<span data-ttu-id="467e8-134">Un elemento **img** puede, opcionalmente, incluir los atributos **alt**, **height** y **width**, y los atributos de estilo **max-width** y **max-height**.</span><span class="sxs-lookup"><span data-stu-id="467e8-134">An **img** element can optionally include **alt**, **height**, and **width** attributes, and the style attributes **max-width** and **max-height**.</span></span>

#### <a name="image-media-types"></a><span data-ttu-id="467e8-135">Tipos de elementos multimedia de imagen</span><span class="sxs-lookup"><span data-stu-id="467e8-135">Image media types</span></span>

<span data-ttu-id="467e8-136">Microsoft Graph es compatible con los tipos de imagen BMP, PNG, GIF, JPEG y TIFF.</span><span class="sxs-lookup"><span data-stu-id="467e8-136">Microsoft Graph supports TIFF, PNG, GIF, JPEG, and BMP image types.</span></span> <span data-ttu-id="467e8-137">Para capturar una imagen que usa un formato diferente que no quiere convertir, [envíe los datos binarios](#add-an-image-using-binary-data) en una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="467e8-137">To capture an image that uses a different format that you don't want to convert, [send the binary data](#add-an-image-using-binary-data) in a multipart request.</span></span> <span data-ttu-id="467e8-138">No es necesario usar Base64 ni codificar los datos binarios con otros formatos.</span><span class="sxs-lookup"><span data-stu-id="467e8-138">You don't need to use Base64 or otherwise encode the binary data that you send.</span></span>

> <span data-ttu-id="467e8-139">**Nota**: La API de OneNote detecta automáticamente el tipo de imagen de entrada original y lo devuelve como el atributo **data-fullres-src-type** en el [HTML de salida](onenote-input-output-html.md#output-html).</span><span class="sxs-lookup"><span data-stu-id="467e8-139">**Note:** The API detects the original input image type, and returns it as the **data-fullres-src-type** attribute in the [output HTML](onenote-input-output-html.md#output-html).</span></span> <span data-ttu-id="467e8-140">La API también devuelve el tipo de imagen de la imagen optimizada en **data-src-type**.</span><span class="sxs-lookup"><span data-stu-id="467e8-140">The API also returns the image type of the optimized image in **data-src-type**.</span></span>
 
<span data-ttu-id="467e8-141">Consulte las [limitaciones](#size-limitations-for-post-pages-requests) que se aplican al crear páginas que contienen archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="467e8-141">See [limitations](#size-limitations-for-post-pages-requests) that apply when creating pages that contain media.</span></span>


<a name="image-img-url-src"></a>

### <a name="add-a-public-image-from-the-web"></a><span data-ttu-id="467e8-142">Agregar una imagen pública desde la web</span><span class="sxs-lookup"><span data-stu-id="467e8-142">Add a public image from the web</span></span>

<span data-ttu-id="467e8-143">En el HTML de entrada de su solicitud, incluya `<img src="https://..." />` y especifique la dirección URL de una imagen de acceso público para el atributo **src**.</span><span class="sxs-lookup"><span data-stu-id="467e8-143">In the input HTML of your request, include `<img src="https://..." />` and specify the URL of a publicly accessible image for the **src** attribute.</span></span>

```html
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
    <img src="https://..." width="300"/>
  </body>
</html>

--MyAppPartBoundary--  
```

<a name="image-img-binary-src"></a>

### <a name="add-an-image-using-binary-data"></a><span data-ttu-id="467e8-144">Agregar una imagen con datos binarios</span><span class="sxs-lookup"><span data-stu-id="467e8-144">Add an image using binary data</span></span>

<span data-ttu-id="467e8-145">En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<img src="name:part-name" />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene los datos de imagen binarios.</span><span class="sxs-lookup"><span data-stu-id="467e8-145">In the input HTML of your request's **Presentation** part, include `<img src="name:part-name" />`, where *part-name* is the unique identifier for the data part in your [multipart request](onenote-create-page.md#example-request) that contains the binary image data.</span></span> <span data-ttu-id="467e8-146">Solo tiene que enviar los datos binarios, no use Base64 ni los codifique con otros formatos.</span><span class="sxs-lookup"><span data-stu-id="467e8-146">Just send the binary data, don't use Base64 or otherwise encode it.</span></span>

```html
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

### <a name="add-a-webpage-snapshot"></a><span data-ttu-id="467e8-147">Agregar una instantánea de página web</span><span class="sxs-lookup"><span data-stu-id="467e8-147">Add a webpage snapshot</span></span>

<span data-ttu-id="467e8-148">Puede usar Microsoft Graph para tomar instantáneas de páginas web completas e insertarlas en otras páginas.</span><span class="sxs-lookup"><span data-stu-id="467e8-148">You can use Microsoft Graph to snapshot entire webpages and insert them into new pages.</span></span> <span data-ttu-id="467e8-149">Este método es útil para archivar páginas web o capturar páginas web complejas con características que no son compatibles con OneNote (por ejemplo, algunas CSS).</span><span class="sxs-lookup"><span data-stu-id="467e8-149">This method is useful to archive webpages or capture complex webpages that have features that OneNote doesn't support (like some CSS).</span></span>  

<span data-ttu-id="467e8-150">En el HTML de entrada de su solicitud, incluya `<img src="https://..." />` y especifique la dirección URL de la página que desea insertar para el atributo **src**.</span><span class="sxs-lookup"><span data-stu-id="467e8-150">In the input HTML of your request, include `<img src="https://..." />` and specify the URL of the webpage you want to insert for the **src** attribute.</span></span>

```html
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
    <img data-render-src="https://www.onenote.com" width="200"/>
  </body>
</html>

--MyAppPartBoundary--  
```


<a name="image-img-binary-data-render-src"></a>

### <a name="add-an-image-rendered-from-html"></a><span data-ttu-id="467e8-151">Agregar una imagen representada desde HTML</span><span class="sxs-lookup"><span data-stu-id="467e8-151">Add an image rendered from HTML</span></span>

<span data-ttu-id="467e8-152">Al pasar el código HTML como un bloque de datos, asegúrese de que no hay ningún contenido activo que requiera credenciales de usuario o un complemento del explorador cargado previamente.</span><span class="sxs-lookup"><span data-stu-id="467e8-152">When you pass the HTML as a data-block, be sure there is no active content that would require user credentials, or a pre-loaded browser plug-in.</span></span> <span data-ttu-id="467e8-153">El motor que Microsoft Graph usa para representar la página HTML en una imagen no tiene la capacidad de hacer que un usuario inicie sesión y no incluye los complementos, como Adobe Flash, Apple QuickTime y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="467e8-153">The engine that Microsoft Graph uses to render the HTML page into an image has no ability to log in a user, and doesn't include plug-ins like Adobe Flash, Apple QuickTime, and so on.</span></span> <span data-ttu-id="467e8-154">Eso también implica que el contenido que se carga dinámicamente, como el que puede incluir un script de AJAX, no aparecerá si para obtener los datos se requieren credenciales de inicio de sesión de usuario o cookies.</span><span class="sxs-lookup"><span data-stu-id="467e8-154">That also means that dynamically-loaded content, such as might come with an AJAX script, won't appear if getting the data requires user login credentials or cookies.</span></span>

<span data-ttu-id="467e8-155">En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<img data-render-src="name:part-name" />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene el HTML.</span><span class="sxs-lookup"><span data-stu-id="467e8-155">In the input HTML of your request's **Presentation** part, include `<img data-render-src="name:part-name" />`, where *part-name* is the unique identifier for the data part in your [multipart request](onenote-create-page.md#example-request) that contains the HTML.</span></span>


```html
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
<img src="https://cdn.onenote.net/1664161560_Images/OneNote.ico" />
</body>
</html>

--MyAppPartBoundary--  
```


<a name="image-object"></a>

### <a name="add-an-image-file-as-an-attachment"></a><span data-ttu-id="467e8-156">Agregar un archivo de imagen como datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="467e8-156">Add an image file as an attachment</span></span>

<span data-ttu-id="467e8-157">En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<object data="name:part-name" data-attachment="file-name.file-ext" type="media-type/media-subtype" />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene los datos de imagen binarios.</span><span class="sxs-lookup"><span data-stu-id="467e8-157">In the input HTML of your request's **Presentation** part, include `<object data="name:part-name" data-attachment="file-name.file-ext" type="media-type/media-subtype" />`, where *part-name* is the unique identifier for the data part in your [multipart request](onenote-create-page.md#example-request) that contains the binary image data.</span></span> <span data-ttu-id="467e8-158">Solo tiene que enviar los datos binarios, no use Base64 ni los codifique con otros formatos.</span><span class="sxs-lookup"><span data-stu-id="467e8-158">Just send the binary data, don't use Base64 or otherwise encode it.</span></span>

```html
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

<span data-ttu-id="467e8-159">Obtenga más información sobre [tipos de archivos multimedia](#file-media-types).</span><span class="sxs-lookup"><span data-stu-id="467e8-159">Learn more about [file media types](#file-media-types).</span></span>



<a name="adding-videos"></a>

## <a name="adding-videos"></a><span data-ttu-id="467e8-160">Agregar vídeos</span><span class="sxs-lookup"><span data-stu-id="467e8-160">Adding videos</span></span>

<span data-ttu-id="467e8-161">Puede insertar vídeos en páginas de OneNote con `<iframe data-original-src="https://..." />` en el HTML de entrada.</span><span class="sxs-lookup"><span data-stu-id="467e8-161">You can embed videos in OneNote pages using `<iframe data-original-src="https://..." />` in the input HTML.</span></span> 

### <a name="supported-video-sites"></a><span data-ttu-id="467e8-162">Sitios de vídeo admitidos</span><span class="sxs-lookup"><span data-stu-id="467e8-162">Supported video sites</span></span>

- <span data-ttu-id="467e8-163">Dailymotion</span><span class="sxs-lookup"><span data-stu-id="467e8-163">Dailymotion</span></span>
- <span data-ttu-id="467e8-164">Office Mix</span><span class="sxs-lookup"><span data-stu-id="467e8-164">Office Mix</span></span>
- <span data-ttu-id="467e8-165">Sway</span><span class="sxs-lookup"><span data-stu-id="467e8-165">Sway</span></span>
- <span data-ttu-id="467e8-166">Sketchfab</span><span class="sxs-lookup"><span data-stu-id="467e8-166">Sketchfab</span></span>
- <span data-ttu-id="467e8-167">TED</span><span class="sxs-lookup"><span data-stu-id="467e8-167">TED</span></span>
- <span data-ttu-id="467e8-168">YouTube</span><span class="sxs-lookup"><span data-stu-id="467e8-168">YouTube</span></span>
- <span data-ttu-id="467e8-169">Vimeo</span><span class="sxs-lookup"><span data-stu-id="467e8-169">Vimeo</span></span>
- <span data-ttu-id="467e8-170">Vine</span><span class="sxs-lookup"><span data-stu-id="467e8-170">Vine</span></span>

### <a name="iframe-attributes"></a><span data-ttu-id="467e8-171">Atributos iframe</span><span class="sxs-lookup"><span data-stu-id="467e8-171">iframe attributes</span></span>

#### <a name="data-original-src"></a><span data-ttu-id="467e8-172">data-original-src</span><span class="sxs-lookup"><span data-stu-id="467e8-172">data-original-src</span></span>

<span data-ttu-id="467e8-173">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="467e8-173">Required.</span></span> <span data-ttu-id="467e8-174">La dirección URL del vídeo.</span><span class="sxs-lookup"><span data-stu-id="467e8-174">The URL of the video.</span></span>

<span data-ttu-id="467e8-175">Ejemplo: `data-original-src="https://www.youtube.com/watch?v=3Ztr44aKmQ8"`</span><span class="sxs-lookup"><span data-stu-id="467e8-175">Example: `data-original-src="https://www.youtube.com/watch?v=3Ztr44aKmQ8"`</span></span>

#### <a name="width"></a><span data-ttu-id="467e8-176">width</span><span class="sxs-lookup"><span data-stu-id="467e8-176">width</span></span>

<span data-ttu-id="467e8-177">Opcional.</span><span class="sxs-lookup"><span data-stu-id="467e8-177">Optional.</span></span> <span data-ttu-id="467e8-178">La anchura del iframe que contiene el vídeo.</span><span class="sxs-lookup"><span data-stu-id="467e8-178">The width of the iframe that contains the video.</span></span> <span data-ttu-id="467e8-179">El valor predeterminado es 480.</span><span class="sxs-lookup"><span data-stu-id="467e8-179">Default is 480.</span></span>

<span data-ttu-id="467e8-180">Ejemplo: `width="300"`</span><span class="sxs-lookup"><span data-stu-id="467e8-180">Example: `width="300"`</span></span>

#### <a name="height"></a><span data-ttu-id="467e8-181">height</span><span class="sxs-lookup"><span data-stu-id="467e8-181">height</span></span>

<span data-ttu-id="467e8-182">Opcional.</span><span class="sxs-lookup"><span data-stu-id="467e8-182">Optional.</span></span> <span data-ttu-id="467e8-183">La altura del iframe que contiene el vídeo.</span><span class="sxs-lookup"><span data-stu-id="467e8-183">The height of the iframe that contains the video.</span></span> <span data-ttu-id="467e8-184">El valor predeterminado es 360.</span><span class="sxs-lookup"><span data-stu-id="467e8-184">Default is 360.</span></span>

<span data-ttu-id="467e8-185">Ejemplo: `height="300"`</span><span class="sxs-lookup"><span data-stu-id="467e8-185">Example: `height="300"`</span></span>

### <a name="example"></a><span data-ttu-id="467e8-186">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="467e8-186">Example</span></span>

<span data-ttu-id="467e8-187">En el HTML de entrada de su solicitud, incluya `<iframe data-original-src="https://..." />` y especifique la dirección URL del vídeo para el atributo **data-original-src**.</span><span class="sxs-lookup"><span data-stu-id="467e8-187">In the input HTML of your request, include `<iframe data-original-src="https://..." />` and specify the URL of the video for the **data-original-src** attribute.</span></span>

```html
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


<a name="adding-files"></a>

## <a name="adding-files"></a><span data-ttu-id="467e8-188">Agregar archivos</span><span class="sxs-lookup"><span data-stu-id="467e8-188">Adding files</span></span>

<span data-ttu-id="467e8-189">Puede agregar archivos adjuntos a las páginas de OneNote con un elemento **object** en el HTML de entrada.</span><span class="sxs-lookup"><span data-stu-id="467e8-189">You can add file attachments to OneNote pages using an **object** element in the input HTML.</span></span> <span data-ttu-id="467e8-190">Si va a agregar un archivo PDF, puede usar un elemento **img** para representar las páginas del PDF como imágenes.</span><span class="sxs-lookup"><span data-stu-id="467e8-190">If you're adding a PDF file, you can use an **img** element to render the PDF pages as images.</span></span> 

[<span data-ttu-id="467e8-191">Agregar un archivo adjunto</span><span class="sxs-lookup"><span data-stu-id="467e8-191">Add a file attachment</span></span>](#add-a-file-attachment)

<span data-ttu-id="467e8-192">Use `<object .../>` y envíe el archivo en una parte de datos de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="467e8-192">Use `<object .../>` and send the file in a data part of a multipart request.</span></span> <span data-ttu-id="467e8-193">Agrega un archivo adjunto que muestra un icono de archivo en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="467e8-193">Adds a file attachment that displays a file icon on the OneNote page.</span></span>

[<span data-ttu-id="467e8-194">Agregar imágenes de contenidos de archivo PDF</span><span class="sxs-lookup"><span data-stu-id="467e8-194">Add images of PDF file contents</span></span>](#add-images-of-pdf-file-contents)

<span data-ttu-id="467e8-195">Use `<img data-render-src="name:part-name" />` y envíe un archivo PDF en la parte de datos de una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="467e8-195">Use `<img data-render-src="name:part-name" />` and send a PDF file in the data part of a multipart request.</span></span> <span data-ttu-id="467e8-196">Representa cada página PDF como una imagen independiente en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="467e8-196">Renders each PDF page as a separate image on the OneNote page.</span></span>

#### <a name="file-attributes"></a><span data-ttu-id="467e8-197">Atributos de archivo</span><span class="sxs-lookup"><span data-stu-id="467e8-197">File attributes</span></span>

<span data-ttu-id="467e8-198">El elemento **object** requiere los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="467e8-198">The **object** element requires the following attributes.</span></span>

<span data-ttu-id="467e8-199">**data-attachment**</span><span class="sxs-lookup"><span data-stu-id="467e8-199">**data-attachment**</span></span>

<span data-ttu-id="467e8-200">El nombre de archivo y la extensión para mostrar en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="467e8-200">The file name and extension to display on the OneNote page.</span></span>

<span data-ttu-id="467e8-201">Ejemplo: `data-attachment="filename.docx"`</span><span class="sxs-lookup"><span data-stu-id="467e8-201">Example: `data-attachment="filename.docx"`</span></span>

<span data-ttu-id="467e8-202">**data**</span><span class="sxs-lookup"><span data-stu-id="467e8-202">**data**</span></span>

<span data-ttu-id="467e8-203">El nombre de la parte del cuerpo de la solicitud de varias partes que contiene los datos de archivo binario.</span><span class="sxs-lookup"><span data-stu-id="467e8-203">The name of the body part in the multipart request that contains the binary file data.</span></span> <span data-ttu-id="467e8-204">Microsoft Graph non admite pasar una referencia de la dirección URL aquí.</span><span class="sxs-lookup"><span data-stu-id="467e8-204">Microsoft Graph does not support passing a URL reference here.</span></span>

<span data-ttu-id="467e8-205">Ejemplo: `data="name:part-name"`</span><span class="sxs-lookup"><span data-stu-id="467e8-205">Example: `data="name:part-name"`</span></span>

<span data-ttu-id="467e8-206">**type**</span><span class="sxs-lookup"><span data-stu-id="467e8-206">**type**</span></span>

<span data-ttu-id="467e8-207">El tipo de archivos multimedia, se usa para determinar el icono de archivo que se usará en la página y qué aplicación se inicia cuando el usuario activa el archivo en el dispositivo desde OneNote.</span><span class="sxs-lookup"><span data-stu-id="467e8-207">The file media type, used to determine the file icon to use on the page, and which application starts when the user activates the file on the device from OneNote.</span></span>

<span data-ttu-id="467e8-208">Ejemplo: `type="application/pdf"`</span><span class="sxs-lookup"><span data-stu-id="467e8-208">Example: `type="application/pdf"`</span></span>


<a name="file-media-types"></a>

#### <a name="file-media-types"></a><span data-ttu-id="467e8-209">Tipos de archivos multimedia</span><span class="sxs-lookup"><span data-stu-id="467e8-209">File media types</span></span>  

<span data-ttu-id="467e8-210">Microsoft Graph usa iconos de tipos de archivos multimedia predefinidos para los archivos adjuntos, o un icono genérico cuando la API no reconoce el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="467e8-210">Microsoft Graph uses predefined file-types icon for attached files, or a generic icon when the API doesn't recognize the file type.</span></span> <span data-ttu-id="467e8-211">La siguiente tabla muestra algunos tipos de archivo comunes que reconocen la API.</span><span class="sxs-lookup"><span data-stu-id="467e8-211">The following table shows some common file types that are recognized by the API.</span></span>

- <span data-ttu-id="467e8-212">application/pdf</span><span class="sxs-lookup"><span data-stu-id="467e8-212">application/pdf</span></span>  
- <span data-ttu-id="467e8-213">application/vnd.openxmlformats-officedocument.wordprocessingml.document</span><span class="sxs-lookup"><span data-stu-id="467e8-213">application/vnd.openxmlformats-officedocument.wordprocessingml.document</span></span>  
- <span data-ttu-id="467e8-214">application/vnd.openxmlformats-officedocument.presentationml.presentation</span><span class="sxs-lookup"><span data-stu-id="467e8-214">application/vnd.openxmlformats-officedocument.presentationml.presentation</span></span>
- <span data-ttu-id="467e8-215">application/vnd.openxmlformats-officedocument.spreadsheetml.sheet</span><span class="sxs-lookup"><span data-stu-id="467e8-215">application/vnd.openxmlformats-officedocument.spreadsheetml.sheet</span></span>
- <span data-ttu-id="467e8-216">image/png</span><span class="sxs-lookup"><span data-stu-id="467e8-216">image/png</span></span>
- <span data-ttu-id="467e8-217">image/jpeg</span><span class="sxs-lookup"><span data-stu-id="467e8-217">image/jpeg</span></span>
- <span data-ttu-id="467e8-218">image/gif</span><span class="sxs-lookup"><span data-stu-id="467e8-218">image/gif</span></span>
- <span data-ttu-id="467e8-219">audio/wav</span><span class="sxs-lookup"><span data-stu-id="467e8-219">audio/wav</span></span>
- <span data-ttu-id="467e8-220">video/mp4</span><span class="sxs-lookup"><span data-stu-id="467e8-220">video/mp4</span></span>
- <span data-ttu-id="467e8-221">application/msword</span><span class="sxs-lookup"><span data-stu-id="467e8-221">application/msword</span></span>
- <span data-ttu-id="467e8-222">application/mspowerpoint</span><span class="sxs-lookup"><span data-stu-id="467e8-222">application/mspowerpoint</span></span>
- <span data-ttu-id="467e8-223">application/excel</span><span class="sxs-lookup"><span data-stu-id="467e8-223">application/excel</span></span>

<span data-ttu-id="467e8-224">Consulte las [limitaciones](#size-limitations-for-post-pages-requests) que se aplican al crear páginas que contienen archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="467e8-224">See [limitations](#size-limitations-for-post-pages-requests) that apply when creating pages that contain media.</span></span>


<a name="file-object"></a>

### <a name="add-a-file-attachment"></a><span data-ttu-id="467e8-225">Agregar un archivo adjunto</span><span class="sxs-lookup"><span data-stu-id="467e8-225">Add a file attachment</span></span>

<span data-ttu-id="467e8-226">En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<object data="name:part-name" data-attachment="file-name.file-ext" type="media-type/media-subtype" />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene los datos de archivo binario.</span><span class="sxs-lookup"><span data-stu-id="467e8-226">In the input HTML of your request's **Presentation** part, include `<object data="name:part-name" data-attachment="file-name.file-ext" type="media-type/media-subtype" />`, where *part-name* is the unique identifier for the data part in your [multipart request](onenote-create-page.md#example-request) that contains the binary file data.</span></span> <span data-ttu-id="467e8-227">Solo tiene que enviar los datos binarios, no use Base64 ni los codifique con otros formatos.</span><span class="sxs-lookup"><span data-stu-id="467e8-227">Just send the binary data, don't use Base64 or otherwise encode it.</span></span>

```html
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

### <a name="add-images-of-pdf-file-contents"></a><span data-ttu-id="467e8-228">Agregar imágenes de contenidos de archivo PDF</span><span class="sxs-lookup"><span data-stu-id="467e8-228">Add images of PDF file contents</span></span>

<span data-ttu-id="467e8-229">En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<img data-render-src="name:part-name" ... />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene los datos de archivo binario.</span><span class="sxs-lookup"><span data-stu-id="467e8-229">In the input HTML of your request's **Presentation** part, include `<img data-render-src="name:part-name" ... />`, where *part-name* is the unique identifier for the data part in your [multipart request](onenote-create-page.md#example-request) that contains the binary file data.</span></span> <span data-ttu-id="467e8-230">Solo tiene que enviar los datos binarios, no use Base64 ni los codifique con otros formatos.</span><span class="sxs-lookup"><span data-stu-id="467e8-230">Just send the binary data, don't use Base64 or otherwise encode it.</span></span>

```html
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

## <a name="size-limitations-for-post-pages-requests"></a><span data-ttu-id="467e8-231">Limitaciones de tamaño para las solicitudes de páginas POST</span><span class="sxs-lookup"><span data-stu-id="467e8-231">Size limitations for POST pages requests</span></span>

<span data-ttu-id="467e8-232">Al enviar datos de imagen y de archivo, tenga en cuenta estas limitaciones: <!--TODO: check these--></span><span class="sxs-lookup"><span data-stu-id="467e8-232">When sending image and file data, be aware of these limitations: <!--TODO: check these--></span></span>

- <span data-ttu-id="467e8-233">El límite de tamaño total de POST es ~ 70 MB, incluyendo imágenes, archivos y otros datos.</span><span class="sxs-lookup"><span data-stu-id="467e8-233">The total POST size limit is ~70 MB, including images, files, and other data.</span></span> <span data-ttu-id="467e8-234">El límite se ve afectado por la codificación de bajada, por lo que no hay ningún límite fijo del número de bytes.</span><span class="sxs-lookup"><span data-stu-id="467e8-234">The actual limit is affected by downstream encoding, so there's no fixed byte-count limit.</span></span> <span data-ttu-id="467e8-235">Las solicitudes que superan el límite pueden producir resultados no confiables.</span><span class="sxs-lookup"><span data-stu-id="467e8-235">Requests that exceed the limit may produce unreliable results.</span></span>

- <span data-ttu-id="467e8-236">El límite de cada parte de datos es 25 MB, incluyendo los encabezados de la parte.</span><span class="sxs-lookup"><span data-stu-id="467e8-236">The limit for each data part is 25 MB, including the part headers.</span></span> <span data-ttu-id="467e8-237">Microsoft Graph rechaza las partes de datos que superan el límite.</span><span class="sxs-lookup"><span data-stu-id="467e8-237">Data parts that exceed the limit are rejected by Microsoft Graph.</span></span> 

- <span data-ttu-id="467e8-238">El número máximo de imágenes por página es 150.</span><span class="sxs-lookup"><span data-stu-id="467e8-238">The maximum number of images per page is 150.</span></span> <span data-ttu-id="467e8-239">Al usar el atributo `src="https://..."`, la API omite las etiquetas **img** pasado este límite.</span><span class="sxs-lookup"><span data-stu-id="467e8-239">When using the `src="https://..."` attribute, the API ignores **img** tags beyond the limit.</span></span>

- <span data-ttu-id="467e8-240">El número máximo de partes de datos es 6 por POST, incluida la parte **Presentation** necesaria.</span><span class="sxs-lookup"><span data-stu-id="467e8-240">The maximum number of data parts is 6 per POST, including the required **Presentation** part.</span></span>

- <span data-ttu-id="467e8-241">Cada solicitud puede contener un máximo de cinco elementos **img** que usan **data-render-src**, y un elemento **object** que usa **data-render-src**. Se ignoran las referencias de imagen y archivos adicionales.</span><span class="sxs-lookup"><span data-stu-id="467e8-241">Each request can contain up to five **img** elements that use **data-render-src** and one **object** elements that uses **data-render-src**. Additional image and file references are ignored.</span></span>

- <span data-ttu-id="467e8-242">El número máximo de imágenes en un solo POST es 30, independientemente del método que utilice para enviarlas a la API.</span><span class="sxs-lookup"><span data-stu-id="467e8-242">The maximum number of images in a single POST is 30, no matter which method you use to send them to the API.</span></span> <span data-ttu-id="467e8-243">Las imágenes adicionales se ignoran.</span><span class="sxs-lookup"><span data-stu-id="467e8-243">Additional images are ignored.</span></span> <span data-ttu-id="467e8-244">Si desea capturar una página web que contiene una gran cantidad de imágenes, considere la posibilidad de [capturar toda la página como una instantánea](#add-a-webpage-snapshot).</span><span class="sxs-lookup"><span data-stu-id="467e8-244">If you want to capture a webpage that contains a lot of images, consider [capturing the whole page as a snapshot](#add-a-webpage-snapshot).</span></span>


## <a name="when-to-use-html-versus-data-render-src"></a><span data-ttu-id="467e8-245">Cuándo usar HTML o data-render-src</span><span class="sxs-lookup"><span data-stu-id="467e8-245">When to use HTML versus data-render-src</span></span> 

<span data-ttu-id="467e8-246">A la hora de decidir entre colocar el código HTML directamente en la página de OneNote o usar el atributo **data-render-src**, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="467e8-246">When trying to decide between putting HTML directly onto the OneNote page instead of using the **data-render-src** attribute, consider the following:</span></span>

- <span data-ttu-id="467e8-247">El código HTML complejo probablemente se envía mejor al motor de representación mediante **data-render-src**, en lugar de intentar modificar el HTML para que se ajuste a lo que Microsoft Graph puede aceptar. </span><span class="sxs-lookup"><span data-stu-id="467e8-247">Complex HTML is probably best sent to the rendering engine via **data-render-src**, rather than attempting to modify the HTML to fit into what Microsoft Graph can accept.</span></span> <span data-ttu-id="467e8-248">Esto también es así cuando el código HTML incluye etiquetas que aún no se admiten.</span><span class="sxs-lookup"><span data-stu-id="467e8-248">This is also true when your HTML includes tags that aren't supported supported.</span></span>

- <span data-ttu-id="467e8-249">Para la representación precisa de la página, para conservar su diseño y aspecto, probablemente es mejor usar el motor de representación mediante **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="467e8-249">Accurate page rendering to preserve the layout and look of the page is probably best done with the rendering engine via **data-render-src**.</span></span>

- <span data-ttu-id="467e8-p130">Para el texto directamente editable suele ser mejor insertar el código HTML directamente en la página. Las imágenes representadas se escanean mediante un sistema de Reconocimiento óptico de caracteres (OCR), pero no es lo mismo.</span><span class="sxs-lookup"><span data-stu-id="467e8-p130">Directly-editable text is often best done with inserting the HTML directly onto the page. The rendered images are scanned by an optical character recognition (OCR) system, but it's just not the same.</span></span>

- <span data-ttu-id="467e8-252">Para las instantáneas puntuales para el historial o el archivo suele ser mejor el método **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="467e8-252">Snapshot-in-time for historical or archival purposes is usually best done with the **data-render-src** method.</span></span>

- <span data-ttu-id="467e8-p131">En el marcado del diseño de una página web para revisiones es donde **data-render-src** realmente destaca. Usando las funciones de entrada manuscrita de OneNote puede dibujar en la imagen para indicar los cambios o destacar áreas importantes. Tener la página web como una imagen facilita mucho esta tarea.</span><span class="sxs-lookup"><span data-stu-id="467e8-p131">Marking-up a web page design for revisions is one place the **data-render-src** truly shines. Using OneNote's inking capabilities, you can draw on the image to indicate changes or call out important areas. Having the web page as an image makes that a lot easier.</span></span>

- <span data-ttu-id="467e8-256">Las imágenes muy grandes o las imágenes con formatos que OneNote no acepta directamente a veces pueden reducirse a miniaturas y convertirse con el atributo **data-render-src** más fácilmente que haciéndolo con su propio código.</span><span class="sxs-lookup"><span data-stu-id="467e8-256">Very large images, or images in formats that OneNote doesn't directly accept, can sometimes be thumbnailed and converted with the **data-render-src** attribute more easily than by doing it in your own code.</span></span> <span data-ttu-id="467e8-257">Incluso si la imagen está disponible en línea, incrustar los datos en su POST a veces puede hacer que la página capturada esté disponible antes para usuarios de OneNote, ya que reduce el número total de ciclos de ida y vuelta necesarios para crear la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="467e8-257">Even if the image is also available online, embedding the data in your POST can sometimes make the captured page available to OneNote users sooner, by reducing the total number of round-trips needed to build the OneNote page.</span></span>

<span data-ttu-id="467e8-258">A veces, la mejor forma de determinar qué método funcionará mejor para los usuarios es probar ambas formas al elaborar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="467e8-258">Sometimes, the best way to determine which method will work best for your users is to try it both ways as you develop your app.</span></span>


<a name="permissions"></a>

## <a name="permissions"></a><span data-ttu-id="467e8-259">Permisos</span><span class="sxs-lookup"><span data-stu-id="467e8-259">Permissions</span></span>

<span data-ttu-id="467e8-260">Para crear o actualizar páginas OneNote, debe solicitar los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="467e8-260">To create or update OneNote pages, you'll need to request appropriate permissions.</span></span> <span data-ttu-id="467e8-261">Elija el nivel más bajo que necesita la aplicación para hacer su trabajo.</span><span class="sxs-lookup"><span data-stu-id="467e8-261">Choose the lowest level that your app needs to do its work.</span></span>

#### <a name="permissions-for-post-pages"></a><span data-ttu-id="467e8-262">Permisos para páginas POST</span><span class="sxs-lookup"><span data-stu-id="467e8-262">Permissions for POST pages</span></span>

- <span data-ttu-id="467e8-263">Notes.Create</span><span class="sxs-lookup"><span data-stu-id="467e8-263">Notes.Create</span></span>
- <span data-ttu-id="467e8-264">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="467e8-264">Notes.ReadWrite</span></span>
- <span data-ttu-id="467e8-265">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="467e8-265">Notes.ReadWrite.All</span></span> 

#### <a name="permissions-for-patch-pages"></a><span data-ttu-id="467e8-266">Permisos para páginas PATCH</span><span class="sxs-lookup"><span data-stu-id="467e8-266">Permissions for PATCH pages</span></span>

- <span data-ttu-id="467e8-267">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="467e8-267">Notes.ReadWrite</span></span>
- <span data-ttu-id="467e8-268">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="467e8-268">Notes.ReadWrite.All</span></span>

<span data-ttu-id="467e8-269">Para obtener más información sobre los ámbitos de permiso y cómo funcionan, consulte los [ámbitos de permisos de OneNote](permissions-reference.md#notes-permissions).</span><span class="sxs-lookup"><span data-stu-id="467e8-269">For more information about permission scopes and how they work, see [OneNote permission scopes](permissions-reference.md#notes-permissions).</span></span>


<a name="see-also"></a>

## <a name="see-also"></a><span data-ttu-id="467e8-270">Vea también</span><span class="sxs-lookup"><span data-stu-id="467e8-270">See also</span></span>

- [<span data-ttu-id="467e8-271">Integración con OneNote</span><span class="sxs-lookup"><span data-stu-id="467e8-271">Integrate with OneNote</span></span>](integrate-with-onenote.md)
- [<span data-ttu-id="467e8-272">Blog para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="467e8-272">OneNote Developer Blog</span></span>](https://go.microsoft.com/fwlink/?LinkID=390183)
- [<span data-ttu-id="467e8-273">Preguntas de desarrollo de OneNote en Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="467e8-273">OneNote development questions on Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkID=390182)
- [<span data-ttu-id="467e8-274">Repositorios de OneNote en GitHub</span><span class="sxs-lookup"><span data-stu-id="467e8-274">OneNote GitHub repos</span></span>](https://go.microsoft.com/fwlink/?LinkID=390178)  
