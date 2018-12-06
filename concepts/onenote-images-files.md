---
title: Agregar imágenes, vídeos y archivos a páginas de OneNote
description: " Blocs de notas de empresa en Office 365"
ms.openlocfilehash: bc298339d73b162da6b2e37c314ffedfb76bd193
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092830"
---
# <a name="add-images-videos-and-files-to-onenote-pages"></a>Agregar imágenes, vídeos y archivos a páginas de OneNote

**Se aplica a:** Blocs de notas para consumidores de OneDrive | Blocs de notas empresariales de Office 365

Puede usar elementos **img**, **object** y **iframe** para agregar imágenes, vídeos y archivos a una página de OneNote cuando [cree](onenote-create-page.md) o [actualice](onenote-update-page.md) la página. 

- Use **img** para representar una imagen en la página.
- Use **iframe** para insertar un vídeo en la página.
- Use **object** para agregar un archivo adjunto a la página.


<a name="images"></a>

## <a name="adding-images"></a>Agregar imágenes

Las imágenes pueden agregarse mediante una dirección URL de referencia o enviando datos sin procesar. Microsoft Graph admite los siguientes métodos para agregar imágenes, logotipos y fotos a páginas de OneNote. 

[Agregar una imagen pública desde la web](#add-a-public-image-from-the-web)

Use `img` con `src="https://image-url"` y especifique la dirección URL de una imagen de acceso público. Representa la imagen en la página de OneNote.

[Agregar una imagen con datos binarios](#add-an-image-using-binary-data)

Use `img` con `src="name:image-block-name"` y envíe el archivo de imagen en una parte de datos de una solicitud de varias partes. Representa la imagen en la página de OneNote.

[Agregar una instantánea de página web](#add-a-webpage-snapshot)

Use `img` con `data-render-src="https://webpage-url"` y especifique la dirección URL de una página web. Representa una instantánea de la página web completa en la página de OneNote.

[Agregar una imagen representada desde HTML](#add-an-image-rendered-from-html)

Use `img` con `data-render-src="name:html-block-name"` y envíe el HTML en la parte de datos de una solicitud de varias partes. Representa el HTML como una imagen en la página de OneNote.

[Agregar imágenes de contenidos de archivo PDF](#add-images-of-pdf-file-contents)

Use `<img data-render-src="name:part-name" />` y envíe el archivo PDF en la parte de datos de una solicitud de varias partes. Representa cada página PDF como una imagen independiente en la página de OneNote.

[Agregar un archivo de imagen como un archivo adjunto](#add-an-image-file-as-an-attachment)

Use `object` con `data="name:file-block-name" data-attachment="file-name.file-ext" type="media-type"` y envíe un archivo de imagen en la parte de datos de una solicitud de varias partes. Agrega un archivo adjunto a la página de OneNote y muestra un icono de archivo.


> **Nota:** Para obtener las imágenes en una página de OneNote, primero envíe una [solicitud GET para el contenido de la página](onenote-get-content.md#page-html-content). Esto devuelve las direcciones URL a los recursos de la imagen en la página. Después separe las [solicitudes GET a los recursos de imagen](onenote-get-content.md#image-or-other-file-resource).


#### <a name="image-attributes"></a>Atributos de imagen 

Un elemento **img** puede, opcionalmente, incluir los atributos **alt**, **height** y **width**, y los atributos de estilo **max-width** y **max-height**.

#### <a name="image-media-types"></a>Tipos de elementos multimedia de imagen

Microsoft Graph es compatible con los tipos de imagen BMP, PNG, GIF, JPEG y TIFF. Para capturar una imagen que usa un formato diferente que no quiere convertir, [envíe los datos binarios](#add-an-image-using-binary-data) en una solicitud de varias partes. No es necesario usar Base64 ni codificar los datos binarios con otros formatos.

> **Nota**: La API de OneNote detecta automáticamente el tipo de imagen de entrada original y lo devuelve como el atributo **data-fullres-src-type** en el [HTML de salida](onenote-input-output-html.md#output-html). La API también devuelve el tipo de imagen de la imagen optimizada en **data-src-type**.
 
Consulte las [limitaciones](#size-limitations-for-post-pages-requests) que se aplican al crear páginas que contienen archivos multimedia.


<a name="image-img-url-src"></a>

### <a name="add-a-public-image-from-the-web"></a>Agregar una imagen pública desde la web

En el HTML de entrada de su solicitud, incluya `<img src="https://..." />` y especifique la dirección URL de una imagen de acceso público para el atributo **src**.

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

### <a name="add-an-image-using-binary-data"></a>Agregar una imagen con datos binarios

En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<img src="name:part-name" />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene los datos de imagen binarios. Solo tiene que enviar los datos binarios, no use Base64 ni los codifique con otros formatos.

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

### <a name="add-a-webpage-snapshot"></a>Agregar una instantánea de página web

Puede usar Microsoft Graph para tomar instantáneas de páginas web completas e insertarlas en otras páginas. Este método es útil para archivar páginas web o capturar páginas web complejas con características que no son compatibles con OneNote (por ejemplo, algunas CSS).  

En el HTML de entrada de su solicitud, incluya `<img src="https://..." />` y especifique la dirección URL de la página que desea insertar para el atributo **src**.

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

### <a name="add-an-image-rendered-from-html"></a>Agregar una imagen representada desde HTML

Al pasar el código HTML como un bloque de datos, asegúrese de que no hay ningún contenido activo que requiera credenciales de usuario o un complemento del explorador cargado previamente. El motor que Microsoft Graph usa para representar la página HTML en una imagen no tiene la capacidad de hacer que un usuario inicie sesión y no incluye los complementos, como Adobe Flash, Apple QuickTime y así sucesivamente. Eso también implica que el contenido que se carga dinámicamente, como el que puede incluir un script de AJAX, no aparecerá si para obtener los datos se requieren credenciales de inicio de sesión de usuario o cookies.

En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<img data-render-src="name:part-name" />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene el HTML.


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

### <a name="add-an-image-file-as-an-attachment"></a>Agregar un archivo de imagen como datos adjuntos

En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<object data="name:part-name" data-attachment="file-name.file-ext" type="media-type/media-subtype" />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene los datos de imagen binarios. Solo tiene que enviar los datos binarios, no use Base64 ni los codifique con otros formatos.

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

Obtenga más información sobre [tipos de archivos multimedia](#file-media-types).



<a name="adding-videos"></a>

## <a name="adding-videos"></a>Agregar vídeos

Puede insertar vídeos en páginas de OneNote con `<iframe data-original-src="https://..." />` en el HTML de entrada. 

### <a name="supported-video-sites"></a>Sitios de vídeo admitidos

- Dailymotion
- Office Mix
- Sway
- Sketchfab
- TED
- YouTube
- Vimeo
- Vine

### <a name="iframe-attributes"></a>Atributos iframe

#### <a name="data-original-src"></a>data-original-src

Obligatorio. La dirección URL del vídeo.

Ejemplo: `data-original-src="https://www.youtube.com/watch?v=3Ztr44aKmQ8"`

#### <a name="width"></a>width

Opcional. La anchura del iframe que contiene el vídeo. El valor predeterminado es 480.

Ejemplo: `width="300"`

#### <a name="height"></a>height

Opcional. La altura del iframe que contiene el vídeo. El valor predeterminado es 360.

Ejemplo: `height="300"`

### <a name="example"></a>Ejemplo

En el HTML de entrada de su solicitud, incluya `<iframe data-original-src="https://..." />` y especifique la dirección URL del vídeo para el atributo **data-original-src**.

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

## <a name="adding-files"></a>Agregar archivos

Puede agregar archivos adjuntos a las páginas de OneNote con un elemento **object** en el HTML de entrada. Si va a agregar un archivo PDF, puede usar un elemento **img** para representar las páginas del PDF como imágenes. 

[Agregar un archivo adjunto](#add-a-file-attachment)

Use `<object .../>` y envíe el archivo en una parte de datos de una solicitud de varias partes. Agrega un archivo adjunto que muestra un icono de archivo en la página de OneNote.

[Agregar imágenes de contenidos de archivo PDF](#add-images-of-pdf-file-contents)

Use `<img data-render-src="name:part-name" />` y envíe un archivo PDF en la parte de datos de una solicitud de varias partes. Representa cada página PDF como una imagen independiente en la página de OneNote.

#### <a name="file-attributes"></a>Atributos de archivo

El elemento **object** requiere los siguientes atributos.

**data-attachment**

El nombre de archivo y la extensión para mostrar en la página de OneNote.

Ejemplo: `data-attachment="filename.docx"`

**data**

El nombre de la parte del cuerpo de la solicitud de varias partes que contiene los datos de archivo binario. Microsoft Graph non admite pasar una referencia de la dirección URL aquí.

Ejemplo: `data="name:part-name"`

**type**

El tipo de archivos multimedia, se usa para determinar el icono de archivo que se usará en la página y qué aplicación se inicia cuando el usuario activa el archivo en el dispositivo desde OneNote.

Ejemplo: `type="application/pdf"`


<a name="file-media-types"></a>

#### <a name="file-media-types"></a>Tipos de archivos multimedia  

Microsoft Graph usa iconos de tipos de archivos multimedia predefinidos para los archivos adjuntos, o un icono genérico cuando la API no reconoce el tipo de archivo. La siguiente tabla muestra algunos tipos de archivo comunes que reconocen la API.

- application/pdf  
- application/vnd.openxmlformats-officedocument.wordprocessingml.document  
- application/vnd.openxmlformats-officedocument.presentationml.presentation
- application/vnd.openxmlformats-officedocument.spreadsheetml.sheet
- image/png
- image/jpeg
- image/gif
- audio/wav
- video/mp4
- application/msword
- application/mspowerpoint
- application/excel

Consulte las [limitaciones](#size-limitations-for-post-pages-requests) que se aplican al crear páginas que contienen archivos multimedia.


<a name="file-object"></a>

### <a name="add-a-file-attachment"></a>Agregar un archivo adjunto

En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<object data="name:part-name" data-attachment="file-name.file-ext" type="media-type/media-subtype" />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene los datos de archivo binario. Solo tiene que enviar los datos binarios, no use Base64 ni los codifique con otros formatos.

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

### <a name="add-images-of-pdf-file-contents"></a>Agregar imágenes de contenidos de archivo PDF

En el HTML de entrada de la parte **Presentation** de su solicitud, incluya `<img data-render-src="name:part-name" ... />`, donde *part-name* es el identificador único para el elemento de datos en su [solicitud de varias partes](onenote-create-page.md#example-request) que contiene los datos de archivo binario. Solo tiene que enviar los datos binarios, no use Base64 ni los codifique con otros formatos.

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

## <a name="size-limitations-for-post-pages-requests"></a>Limitaciones de tamaño para las solicitudes de páginas POST

Al enviar datos de imagen y de archivo, tenga en cuenta estas limitaciones: <!--TODO: check these-->

- El límite de tamaño total de POST es ~ 70 MB, incluyendo imágenes, archivos y otros datos. El límite se ve afectado por la codificación de bajada, por lo que no hay ningún límite fijo del número de bytes. Las solicitudes que superan el límite pueden producir resultados no confiables.

- El límite de cada parte de datos es 25 MB, incluyendo los encabezados de la parte. Microsoft Graph rechaza las partes de datos que superan el límite. 

- El número máximo de imágenes por página es 150. Al usar el atributo `src="https://..."`, la API omite las etiquetas **img** pasado este límite.

- El número máximo de partes de datos es 6 por POST, incluida la parte **Presentation** necesaria.

- Cada solicitud puede contener un máximo de cinco elementos **img** que usan **data-render-src**, y un elemento **object** que usa **data-render-src**. Se ignoran las referencias de imagen y archivos adicionales.

- El número máximo de imágenes en un solo POST es 30, independientemente del método que utilice para enviarlas a la API. Las imágenes adicionales se ignoran. Si desea capturar una página web que contiene una gran cantidad de imágenes, considere la posibilidad de [capturar toda la página como una instantánea](#add-a-webpage-snapshot).


## <a name="when-to-use-html-versus-data-render-src"></a>Cuándo usar HTML o data-render-src 

A la hora de decidir entre colocar el código HTML directamente en la página de OneNote o usar el atributo **data-render-src**, tenga en cuenta lo siguiente:

- El código HTML complejo probablemente se envía mejor al motor de representación mediante **data-render-src**, en lugar de intentar modificar el HTML para que se ajuste a lo que Microsoft Graph puede aceptar.  Esto también es así cuando el código HTML incluye etiquetas que aún no se admiten.

- Para la representación precisa de la página, para conservar su diseño y aspecto, probablemente es mejor usar el motor de representación mediante **data-render-src**.

- Para el texto directamente editable suele ser mejor insertar el código HTML directamente en la página. Las imágenes representadas se escanean mediante un sistema de Reconocimiento óptico de caracteres (OCR), pero no es lo mismo.

- Para las instantáneas puntuales para el historial o el archivo suele ser mejor el método **data-render-src**.

- En el marcado del diseño de una página web para revisiones es donde **data-render-src** realmente destaca. Usando las funciones de entrada manuscrita de OneNote puede dibujar en la imagen para indicar los cambios o destacar áreas importantes. Tener la página web como una imagen facilita mucho esta tarea.

- Las imágenes muy grandes o las imágenes con formatos que OneNote no acepta directamente a veces pueden reducirse a miniaturas y convertirse con el atributo **data-render-src** más fácilmente que haciéndolo con su propio código. Incluso si la imagen está disponible en línea, incrustar los datos en su POST a veces puede hacer que la página capturada esté disponible antes para usuarios de OneNote, ya que reduce el número total de ciclos de ida y vuelta necesarios para crear la página de OneNote.

A veces, la mejor forma de determinar qué método funcionará mejor para los usuarios es probar ambas formas al elaborar la aplicación.


<a name="permissions"></a>

## <a name="permissions"></a>Permisos

Para crear o actualizar páginas OneNote, debe solicitar los permisos adecuados. Elija el nivel más bajo que necesita la aplicación para hacer su trabajo.

#### <a name="permissions-for-post-pages"></a>Permisos para páginas POST

- Notes.Create
- Notes.ReadWrite
- Notes.ReadWrite.All 

#### <a name="permissions-for-patch-pages"></a>Permisos para páginas PATCH

- Notes.ReadWrite
- Notes.ReadWrite.All

Para obtener más información sobre los ámbitos de permiso y cómo funcionan, consulte los [ámbitos de permisos de OneNote](permissions-reference.md#notes-permissions).


<a name="see-also"></a>

## <a name="see-also"></a>Vea también

- [Integración con OneNote](integrate-with-onenote.md)
- [Blog para desarrolladores de OneNote](https://go.microsoft.com/fwlink/?LinkID=390183)
- [Preguntas de desarrollo de OneNote en Stack Overflow](https://go.microsoft.com/fwlink/?LinkID=390182)
- [Repositorios de OneNote en GitHub](https://go.microsoft.com/fwlink/?LinkID=390178)  
