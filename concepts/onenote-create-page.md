# <a name="create-onenote-pages"></a>Crear páginas de OneNote

**Se aplica a**: Blocs de notas para consumidores de OneDrive | Blocs de notas empresariales de Office 365

Para crear una página de OneNote, envíe una solicitud POST al punto de conexión *pages*. Por ejemplo:

`POST ../notes/sections/{id}/pages`

<br/>

Envíe el HTML que define la página en el cuerpo del mensaje. Si la solicitud se completa correctamente, Microsoft Graph devuelve un código de estado HTTP 201.


> **Nota:** Para obtener información sobre las solicitudes POST que puede enviar para crear secciones, grupos de secciones y blocs de notas, vea la [referencia de REST interactiva](http://dev.onenote.com/docs).


<a name="request-uri"></a>

## <a name="construct-the-request-uri"></a>Crear el URI de la solicitud

Para crear el URI de la solicitud POST, empiece con la dirección URL raíz del servicio:

`https://graph.microsoft.com/v1.0/me/onenote`

<br/>

Después, anexe el punto de conexión *pages*:

- **Crear una página en cualquier sección (especificado por el nombre de sección)**<br/><br/>`.../pages?sectionName=DefaultSection`

- **Crear una página en cualquier sección (especificado por el id.)**<br/><br/>`.../sections/{section-id}/pages` 

Si va a crear páginas en el bloc de notas personal del usuario, Microsoft Graph también proporciona puntos de conexión que puede usar para crear páginas en el bloc de notas predeterminado:

- **Crear una página de OneNote en la sección predeterminada del bloc de notas predeterminado**<br/><br/>`../pages` 



La URI de la solicitud completa tendrá un aspecto similar a uno de estos ejemplos:

- `https://graph.microsoft.com/v1.0/me/onenote/sections/{id}/pages`
- `https://graph.microsoft.com/v1.0/me/onenote/pages?sectionName=Homework`

Obtenga más información sobre la [URL de raíz del servicio](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).

<a name="post-pages-section-name"></a>

### <a name="using-the-sectionname-url-parameter"></a>Usar el parámetro de URL *sectionName*

Las reglas siguientes se aplican al usar el parámetro *sectionName* para crear una página en una sección con nombre del bloc de notas predeterminado:

- Solo se puede hacer referencia a las secciones de nivel superior (no a las secciones dentro de grupos de secciones).

- Si en el bloc de notas predeterminado no existe una sección con el nombre especificado, la API la creará. Los caracteres siguientes no pueden usarse en los nombres de sección: `? * \ / : < > | & # " % ~`

- Los nombres de sección no distinguen mayúsculas de minúsculas, pero el uso de mayúsculas se conserva al crear las secciones. Por lo tanto, “Mi nueva sección” se mostrará de esa forma, pero “mi nueva sección” también coincidirá en las publicaciones posteriores.

- Los nombres de sección necesitan tener el formato de codificación URL. Por ejemplo, los espacios tienen que codificarse como *%20*.

- El parámetro *sectionName* solo es válido con la ruta `../notes/pages` (pero no con `../notes/sections/{id}/pages`).

Como se crearán secciones si no existen, es seguro usar esta llamada con todas las páginas que cree la aplicación. Aunque los usuarios pueden cambiar el nombre de las secciones, la API creará una sección con el nombre de sección que especifique. 

> **Nota:** Los vínculos devueltos por la API para las páginas en una sección con un nombre cambiado también llegarán a las páginas anteriores. 


<a name="message-body"></a>

## <a name="construct-the-message-body"></a>Crear el cuerpo del mensaje

El código HTML que define el contenido de la página se denomina *HTML de entrada*. El código HTML de entrada admite un [subconjunto de HTML y CSS estándar](#supported-html-and-css-for-onenote-pages), además de atributos personalizados. (Los atributos personalizados, como **data-id** y **data-render-src**, se describen en [HTML de entrada y salida](onenote_input_output_html.md)). 

Envíe el código HTML de entrada en el cuerpo del mensaje de la solicitud POST. Puede enviar el código HTML de entrada directamente en el cuerpo del mensaje con el tipo de contenido `application/xhtml+xml` o `text/html`, o bien puede enviarlo en el elemento “Presentación” de una solicitud de varias partes. 

En el ejemplo siguiente, se envía el código HTML de entrada directamente en el cuerpo del mensaje.

```html
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

<br/>

Si envía datos binarios, tendrá que usar una [solicitud de varias partes](#example-request). 

> **Nota:** Para simplificar la programación y la coherencia en la aplicación, puede usar solicitudes de varias partes para crear todas las páginas. Le recomendamos que use una biblioteca para crear mensajes de varias partes. Esto reduce el riesgo de crear cargas de trabajo con formato incorrecto.


<a name="input-html-rules"></a>

### <a name="requirements-and-limitations-for-input-html-in-post-pages-requests"></a>Requisitos y limitaciones para HTML de entrada en solicitudes de páginas POST

Al enviar HTML de entrada, tenga en cuenta estos requisitos y limitaciones generales:  

- El código HTML de entrada necesita tener codificación UTF-8 y XHTML con un formato correcto. Todas las etiquetas de inicio del contenedor necesitan las etiquetas de cierre correspondientes. Todos los valores de atributo tienen que delimitarse con comillas dobles o simples.  <!--docs say MUST be encoded-->

- El código JavaScript se quita, incluidos los archivos y CSS. 

- Los formularios HTML se quitan por completo.  

- Microsoft Graph admite un [subconjunto de elementos HTML](#supported-html-and-css-for-onenote-pages). 

- Microsoft Graph admite un subconjunto de atributos HTML comunes y un conjunto de atributos personalizados, como el atributo **data-id** usado para actualizar páginas. Para obtener información sobre los atributos admitidos, vea [HTML de entrada y salida](onenote_input_output_html.md).


<a name="supported-html"></a>

### <a name="supported-html-and-css-for-onenote-pages"></a>HTML y CSS admitido para páginas de OneNote

No se admiten todos los elementos, atributos y propiedades (en HTML4, XHTML, CSS, HTML5, etc.). En su lugar, Microsoft Graph admite un conjunto limitado de HTML que se adapta mejor a la forma en que los usuarios usan OneNote. Para obtener más información, vea [Etiquetas HTML admitidas para páginas](http://dev.onenote.com/docs#/introduction/html-tag-support-for-pages). Si una etiqueta no se muestra aquí, lo más probable es que se omita.

<!--Microsoft Graph only accepts UTF-8 data. Be sure that all requests are encoded that way, and your content-type headers indicate that as well. xx our examples don't show this-->

En la lista siguiente, se muestran los tipos de elementos básicos admitidos por Microsoft Graph:

- `<head>` y `<body>`</p>
- `<title>` y `<meta>` que establece el título de página y la fecha de creación</p>
- `<h1>` a `<h6>` para los encabezados de sección</p>
- `<p>` para párrafos</p>
- `<ul>`, `<ol>` y `<li>` para listas y elementos de lista</p>
- `<table>`, `<tr>`y `<td>`, incluidas las tablas anidadas</p>
- `<pre>` para texto con formato previo (conserva el espacio en blanco y los saltos de línea)</p>
- `<b>` y `<i>` para estilos de carácter negrita y cursiva</p>

Microsoft Graph conserva el contenido semántico y la estructura básica del HTML de entrada al crear páginas, pero convierte el HTML de entrada para usar el conjunto admitido de HTML y CSS. Las características que no existen en OneNote no pueden traducirse a nada, por lo que es posible que no se reconozcan en el HTML de origen. 


<a name="example"></a>

## <a name="example-request"></a>Ejemplo de solicitud

En esta solicitud de varias partes de ejemplo, se crea una página que contiene imágenes y un archivo incrustado. El elemento **Presentation** necesario contiene el HTML de entrada que define la página. El elemento **imageBlock1** contiene los datos de imágenes binarias y **fileBlock1** contiene los datos de archivos binarios. Los elementos de datos también pueden contener HTML; en ese caso, Microsoft Graph [representa el código HTML como una imagen](onenote_images_files.md#add-an-image-using-binary-data) en la página de OneNote. 

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

Para obtener más ejemplos donde se muestra cómo crear páginas que contienen imágenes y otros archivos, vea [Agregar imágenes y archivos](onenote_images_files.md), [tutoriales](https://docs.microsoft.com/es-ES/previous-versions/office/office-365-api/how-to/onenote-tutorial) y [ejemplos](https://github.com/onenotedev). Además, obtenga información sobre cómo [crear elementos con posición absoluta](onenote-abs-pos.md), [usar etiquetas de notas](onenote-note-tags.md) y [extraer datos de capturas](onenote-extract-data.md) de tarjetas de presentación y listas de productos y recetas en línea.

Microsoft Graph es estricto en relación con algunos formatos, como nuevas líneas CRLF en el cuerpo de un mensaje de varias partes. Para reducir el riesgo de crear cargas de trabajo con formato incorrecto, necesita usar una biblioteca para crear mensajes de varias partes. 

Si recibe un código de estado 400 para una carga con formato incorrecto, compruebe el formato de las nuevas líneas y los espacios en blanco, y asegúrese de que no haya problemas de codificación. Por ejemplo, pruebe a usar `charset=utf-8` (ejemplo: `Content-Type: text/html; charset=utf-8`).

Vea [Requisitos y limitaciones de HTML de entrada](#requirements-and-limitations-for-input-html-in-post-pages-requests) y [Límites de tamaño de solicitudes POST](onenote_images_files.md#size-limitations-for-post-pages-requests).


<a name="request-response-info"></a>

## <a name="request-and-response-information-for-post-pages-requests"></a>Información de solicitudes y respuestas para solicitudes de *páginas POST*

| Solicitar datos | Descripción |  
|------|------|  
| Protocolo | Todas las solicitudes usan el protocolo HTTPS SSL/TLS. |  
| Encabezado Authorization | <p>`Bearer {token}`, donde `{token}` es un token de acceso de OAuth 2.0 válido para la aplicación registrada.</p><p>Si falta o no es válido, la solicitud producirá errores con el código de estado 401. Vea [Authentication and permissions](permissions_reference.md) (Autenticación y permisos).</p> |  
| Encabezado Content-Type | <p>`text/html` o `application/xhtml+xml` para el contenido HTML, sin importar si se envía directamente en el cuerpo del mensaje o en el elemento “Presentación” necesario de las solicitudes de varias partes.</p><p>Las solicitudes de varias partes son necesarias al enviar datos binarios y usar el tipo de contenido `multipart/form-data; boundary=part-boundary`, donde `{part-boundary}` es una cadena que señala el principio y el final de cada elemento de datos.</p> |  
| Encabezado Accept | `application/json` | 

<br/>

| Datos de respuesta | Descripción |  
|------|------|  
| Código de correcto | Código de estado HTTP 201. |  
| Cuerpo de la respuesta | Una representación de OData de la nueva página en formato JSON. |  
| Errores | Si la solicitud no se completa correctamente, la API mostrará los errores del objeto **@api.diagnostics** en el cuerpo de la respuesta. |  
| Encabezado de ubicación | La URL de recursos de la nueva página. |  
| Encabezado X-CorrelationId | GUID que identifica la solicitud de forma única. Puede usar este valor, además del valor del encabezado de fecha, al trabajar con el soporte técnico de Microsoft para solucionar problemas. |  


<a name="root-url"></a>

### <a name="constructing-the-microsoft-graph-service-root-url"></a>Crear la URL raíz del servicio de Microsoft Graph

La URL raíz del servicio de Microsoft Graph usa el formato siguiente para todas las llamadas que se realicen a Microsoft Graph:

`https://graph.microsoft.com/{version}/me/onenote/`  

El segmento `version` de la URL representa la versión de Microsoft Graph que se quiere utilizar. Use `v1.0` para código de producción estable. Use `beta` para probar una característica que esté en desarrollo. Las características y la funcionalidad de la versión beta pueden cambiar, por lo que no se debe usar en el código de producción. 

Use `me` para contenido de OneNote al que puede obtener acceso el usuario actual (contenido compartido y del que sea propietario). Use `users/{id}` para contenido de OneNote que el usuario especificado (en la URL) compartió con el usuario actual. Use [Microsoft Graph](https://graph.microsoft.com/v1.0/users) para obtener identificadores de usuario. 


<a name="permissions"></a>

## <a name="permissions"></a>Permisos

Para crear páginas de OneNote, necesitará solicitar los permisos adecuados. Seleccione el nivel inferior de permisos que necesita la aplicación para funcionar correctamente.

Seleccione entre:

- Notes.Create
- Notes.ReadWrite
- Notes.ReadWrite.All

Para obtener más información sobre los ámbitos de permiso y cómo funcionan, vea [Referencias de permisos de Microsoft Graph](permissions_reference.md).




<a name="see-also"></a>

## <a name="see-also"></a>Vea también

- [Agregar imágenes y archivos](onenote_images_files.md)
- [Crear elementos con posición absoluta](onenote-abs-pos.md)  
- [Extraer datos](onenote-extract-data.md)
- [Usar etiquetas de notas](onenote-note-tags.md)
- [Integración con OneNote](integrate_with_onenote.md)
- [Blog para desarrolladores de OneNote](http://go.microsoft.com/fwlink/?LinkID=390183)
- [Preguntas de desarrollo de OneNote en Stack Overflow](http://go.microsoft.com/fwlink/?LinkID=390182)
- [Repositorios de OneNote en GitHub](http://go.microsoft.com/fwlink/?LinkID=390178)  


