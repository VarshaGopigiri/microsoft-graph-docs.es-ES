# <a name="update-onenote-page-content"></a>Actualizar el contenido de la página de OneNote

**Se aplica a:** Blocs de notas para consumidores de OneDrive | Blocs de notas empresariales de Office 365


Para actualizar el contenido de una página de OneNote, envíe una solicitud PATCH al punto de conexión *content* de la página.

`PATCH ../notes/pages/{id}/content`</p>

Envíe un objeto de cambio JSON en el cuerpo del mensaje. Si la solicitud se completa correctamente, Microsoft Graph devuelve un código de estado HTTP 204.


<a name="request-uri"></a>

## <a name="construct-the-request-uri"></a>Crear el URI de la solicitud

Para crear el URI de la solicitud, comience con la dirección URL raíz del servicio:

`https://graph.microsoft.com/v1.0/me/onenote`

<br/>

Luego anexe el punto de conexión *content* de la página:

- **Obtenga el HTML de página y todos los valores de *data-id* definidos**.<br/><br/>`../pages/{id}/content`   

- **Obtenga el HTML de página y todos los valores de *data-id* definidos y todos los valores de *id* generados**.<br/><br/>`../pages/{page-id}/content?includeIDs=true` 

Los valores de **data-id** y de **id** se usan como identificadores **target** de los elementos que se quieren actualizar.

 
El identificador URI de solicitud completo tendrá un aspecto similar al siguiente:<br/><br/>`https://graph.microsoft.com/v1.0/me/onenote/pages/{id}/content`


Obtenga más información sobre la [dirección URL raíz del servicio](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).


<a name="message-body"></a>

## <a name="construct-the-message-body"></a>Crear al cuerpo del mensaje

El código HTML de una página de OneNote contiene texto, imágenes y otro contenido organizado en estructuras tales como **div**, **img** y **ol** elementos. Para actualizar el contenido de la página de OneNote, puede agregar y reemplazar elementos HTML en la página.

Los cambios se envían en el cuerpo del mensaje como matriz de objetos de cambio JSON. Cada objeto especifica el nuevo contenido HTML del elemento de destino y qué hacer con el contenido.

La siguiente matriz define dos cambios. El primero inserta una imagen arriba del párrafo como un elemento relacionado, el segundo anexa un elemento a la lista como un último elemento secundario.

```json
[
   {
    'target':'#para-id',
    'action':'insert',
    'position':'before',
    'content':'<img src="image-url-or-part-name" alt="Image above the target paragraph" />'
  }, 
  {
    'target':'#list-id',
    'action':'append',
    'content':'<li>Item at the end of the list</li>'
  }
]
```

Vea [más ejemplos](#example-requests).


### <a name="attributes-for-json-change-objects"></a>Atributos para los objetos de cambio JSON

Use los atributos **target**, **action**, **position** y **content** para definir objetos JSON para solicitudes PATCH.

#### <a name="target"></a>target

Elemento que se va a actualizar. El valor debe ser uno de los siguientes identificadores:

| Identificador | Descripción |  
|------|------|  
| #{data-id} | <p>Este identificador se define opcionalmente en los elementos del HTML de entrada [al crear una página](onenote-create-page.md) o [actualizar una página](onenote_update_page.md). Use # como prefijo.</p><p> Ejemplo:<br/>`'target':'#intro'` tiene como destino el elemento `<div data-id="intro" ...>`</p> |  
| id | <p>Se trata del [identificador generado](#generated-ids) en Microsoft Graph, y es necesario para la mayoría de las operaciones de reemplazo. No use # como prefijo.</p><p> Ejemplo:<br/>`'target':'div:{33f8a2...}{37}'` tiene como destino el elemento `<div id="div:{33f8a2...}{37}" ...>`</p><p>No debe confundirse con los valores de **id** definidos en el [HTML de entrada](onenote_input_output_html.md). Todos los valores de **id** enviados en el HTML de entrada se descartan.</p> |  
| body | Palabra clave que tiene como destino el primer div en la página. No use # como prefijo. |  
| title | Palabra clave que tiene como destino el título de página. No use # como prefijo. |  
 
#### <a name="action"></a>action

La acción que se va a realizar en el elemento de destino. Vea [acciones admitidas para elementos](#supported-elements-and-actions).

| Acción | Descripción |  
|------|------|  
| append | <p>Agrega el contenido especificado al destino como primer o último elemento secundario, tal y como se determina en el atributo **position**.</p><p>Solo se aplica a los elementos **body**, **div**, **ol** y **ul**.</p> |  
| insert | Agrega el contenido especificado como elemento del mismo nivel antes o después del elemento de destino, tal y como se determina en el atributo **position**. |  
| prepend | <p>Agrega el contenido especificado al destino como primer elemento secundario. Acceso directo a **append** + **before**.</p><p>Solo se aplica a los elementos **body**, **div**, **ol** y **ul**.</p> |  
| replace | <p>Reemplaza el destino por el contenido especificado.</p><p>La mayoría de las acciones **replace** requieren el uso del [identificador generado](#generated-ids) para el elemento de destino (excepto **img** y **object** dentro de un div, que también admiten el uso de **data-id**).</p> |  
 
#### <a name="position"></a>position

La ubicación donde agregar el contenido provisto, relativa al elemento de destino. Queda predeterminado como **after** si se omite.

| Posición | Descripción |  
|------|------|  
| after (valor predeterminado) |<p>Con **append**: último elemento secundario del elemento de destino.</p><p>Con **insert**: siguiente elemento del mismo nivel del elemento de destino.</p> |
| before | <p>Con **append**: primer elemento secundario del elemento de destino.</p><p>Con **insert**: anterior elemento del mismo nivel del elemento de destino.</p> |

#### <a name="content"></a>content

Cadena de HTML sintácticamente correcta que se agrega a la página y datos binarios de cualquier imagen o archivo. Si el contenido contiene datos binarios, la solicitud debe enviarse utilizando el tipo de contenido `multipart/form-data` con una parte "Comandos" (véase un [ejemplo](#multipart-request-with-binary-content)). 
 

<a name="generated-ids"></a>

### <a name="generated-ids"></a>Identificadores generados
Microsoft Graph genera valores de **id** para los elementos de la página que pueden actualizarse. Para obtener el identificador generado, use la expresión de cadena de consulta `includeIDs=true` en la solicitud GET:

`GET ../notes/pages/{page-id}/content?includeIDs=true` 

> **Nota:** La API descarta todos los valores de **id** definidos en el [HTML de entrada](onenote_input_output_html.md) de las solicitudes create-page y update-page.

En el siguiente ejemplo se muestran los identificadores generados para un párrafo y una imagen en el [HTML de salida](onenote_input_output_html.md) de una página.

```html
<p id="p:{33f8a242-7c33-4bb2-90c5-8425a68cc5bf}{40}">Some text on the page</p>
<img id="img:{33f8a242-7c33-4bb2-90c5-8425a68cc5bf}{45}" ... />
```

Los valores de **id** generados pueden cambiar después de la actualización de una página, por lo tanto debe obtener los valores actuales antes de crear una solicitud de PATCH que los utilice.
 
Puede especificar los elementos de destino con el valor de **data-id** o de **id**, de la manera siguiente:

- Para las acciones **append** y **insert**, puede usar cualquier identificador como valor de destino.
- Para las acciones **replace**, debe usar el identificador generado para todos los elementos excepto el título de página y las imágenes y los objetos que se encuentran dentro de un div. 
    - Para reemplazar un título, utilice la palabra clave **title**. 
    - Para reemplazar imágenes y objetos que se encuentran en un div, utilice **data-id** o **id**.

En el siguiente ejemplo se usa el valor de **id** como destino. No use el prefijo # con un identificador generado.

```json
[
   {
    'target':'p:{33f8a242-7c33-4bb2-90c5-8425a68cc5bf}{40}',
    'action':'insert',
    'position':'before',
    'content':'<p>This paragraph goes above the target paragraph.</p>'
  }
]
```

<a name="support-matrix"></a>

## <a name="supported-elements-and-actions"></a>Acciones y elementos admitidos

Se pueden actualizar muchos elementos de la página, pero cada tipo de elemento admite acciones específicas. En la siguiente tabla se muestran los elementos de destino admitidos y las acciones de actualización que admiten.

| Elemento | Reemplazar | Anexar elemento secundario | Insertar elemento del mismo nivel |  
|------|:------:|:------:|:------:|  
| body<br /> (tiene como destino el primer div en la página) | no | **sí** | no |  
| div<br /> ([posición absoluta](onenote-abs-pos.md)) | no | **sí** | no |  
| div<br /> (en un elemento div) | **sí**<br/>(solo identificador) | **sí** | **sí** |   
| img, object<br /> (en un elemento div) | **sí** | no | **sí** |   
| ol, ul | **sí**<br/>(solo identificador) | **sí** | **sí** |   
| table | **sí**<br/>(solo identificador) | no | **sí** |   
| p, li, h1-h6 | **sí**<br/>(solo identificador) | no | **sí** |   
| title | **sí** | no | no |  
 
<br/>

Los siguientes elementos no admiten ninguna acción de actualización.

- img ([posición absoluta](onenote-abs-pos.md))
- object ([posición absoluta](onenote-abs-pos.md))
- tr, td
- meta
- head
- span
- a
- etiquetas de estilo


<a name="examples"></a>

## <a name="example-requests"></a>Solicitudes de ejemplo

Una solicitud de actualización contiene uno o más cambios que se representan como objetos de cambio JSON. Estos objetos pueden definir diferentes destinos en la página y diferentes acciones y contenido para los destinos.

En los siguientes ejemplos se incluyen objetos JSON usados en solicitudes PATCH y solicitudes PATCH completas:

- [Anexar elementos secundarios](#append-child-elements)
- [Insertar elementos del mismo nivel](#insert-sibling-elements)
- [Reemplazar elementos](#replace-elements)
- [Solicitud PATCH completa](#complete-patch-request-examples)


<a name="append-examples"></a>

### <a name="append-child-elements"></a>Anexar elementos secundarios

La acción **append** agrega un elemento secundario a un elemento **body**, **div** (dentro de un div), **ol** o **ul**. El atributo **position** determina si el elemento secundario se va a anexar antes o después del destino. La posición predeterminada es **after**.

#### <a name="append-to-a-div"></a>Anexar a un div

En el ejemplo siguiente se agregan dos nodos secundarios al elemento **div1**. Agrega una imagen como primer elemento secundario y un párrafo como último elemento secundario. 

```json
[
 {
    'target':'#div1',
    'action':'append',
    'position':'before',
    'content':'<img data-id="first-child" src="image-url-or-part-name" />'
  },
  {
    'target':'#div1',
    'action':'append',
    'content':'<p data-id="last-child">New paragraph appended to the div</p>'
  }
]
```
 

#### <a name="append-to-the-body-element"></a>Anexar al elemento *body*

Puede usar el acceso directo **body** para anexar un elemento secundario en el interior del primer div de cualquier página.

En el siguiente ejemplo se agregan dos párrafos como primer elemento secundario y último elemento secundario en el primer div de la página. No use # con el destino **body**. En este ejemplo se usa la acción **prepend** como acceso directo a **append** + **before**.

```json
[
  {
    'target':'body',
    'action':'prepend',
    'content':'<p data-id="first-child">New paragraph as first child in the first div</p>'
  },
  {
    'target':'body',
    'action':'append',
    'content':'<p data-id="last-child">New paragraph as last child in the first div</p>'
  }
]
```
 

#### <a name="append-to-a-list"></a>Anexar a una lista

La acción insert agrega un elemento relacionado al elemento de destino. El atributo position determina si el elemento relacionado se insertará antes o después del elemento de destino. La posición predeterminada es after. Consulte elementos que admiten insertar.

```json
[
  {
    'target':'#circle-ul',
    'action':'append',
    'content':'<li style="list-style-type:circle">Item at the end of the list</li>'
  }
]
```
 

<a name="insert-examples"></a>

### <a name="insert-sibling-elements"></a>Insertar elementos del mismo nivel

La acción **insert** agrega un elemento del mismo nivel al elemento de destino. El atributo **position** determina si el elemento del mismo nivel se va a insertar antes o después del destino. La posición predeterminada es **after**. Vea [elementos que admiten **insert**](#supported-elements-and-actions).

#### <a name="insert-siblings"></a>Insertar elementos del mismo nivel

Puede usar tanto el data-id o el id generado como valor de destino para reemplazar elementosimg y object que se encuentran dentro de un div. Para reemplazar el título de una página, use la palabra clave title. Para todos los demás elementos que admiten reemplazo, debe usar el Id. generado.

```json
[
  {
     'target':'#para1',
     'action':'insert',
     'position':'before',
     'content':'<img src="image-url-or-part-name" alt="Image inserted above the target" />'
  },
  {
    'target':'#para2',
     'action':'insert',
     'content':'<p data-id="next-sibling">Paragraph inserted below the target</p>'
  }
]
```
 

<a name="replace-examples"></a>

### <a name="replace-elements"></a>Reemplazar elementos

Puede utilizar el **data-id** o el **id** generado como valor de destino para reemplazar los elementos **img** y **object** que están dentro de un div. Para reemplazar el título de página, utilice la palabra clave **title**. Para todos los demás [elementos que admiten **replace**](#supported-elements-and-actions), debe usar el identificador generado.

#### <a name="replace-an-image"></a>Reemplazar una imagen

En este ejemplo se reemplaza una imagen por un div mediante el **data-id** de la imagen como destino 

```json
[
  {
    'target':'#img1',
    'action':'replace',
    'content':'<div data-id="new-div"><p>This div replaces the image</p></div>'
  }
]
```
 

#### <a name="update-a-table"></a>Actualizar una tabla 

Este ejemplo muestra cómo cambiar el título de una página. Para cambiar el título, use la palabra clave title como el valor del elemento de destino. No use # con el elemento de destino title.

```json
[
  {
    'target':'table:{de3e0977-94e4-4bb0-8fee-0379eaf47486}{11}',
    'action':'replace',
    'content':'<table data-id="football">
      <tr><td><p><b>Brazil</b></p></td><td><p>Germany</p></td></tr>
      <tr><td><p>France</p></td><td><p><b>Italy</b></p></td></tr>
      <tr><td><p>Netherlands</p></td><td><p><b>Spain</b></p></td></tr>
      <tr><td><p>Argentina</p></td><td><p><b>Germany</b></p></td></tr></table>'
  }
]
```
 

#### <a name="change-the-title"></a>Cambiar el título 

En este ejemplo se muestra cómo cambiar el título de la página. Para cambiar el título, use la palabra clave **title** como valor de destino. No use el prefijo # con el destino title.

```json
[
  {
    'target':'title',
    'action':'replace',
    'content':'New title'
  }
]
```
 

#### <a name="update-a-to-do-item"></a>Actualizar una tarea pendiente

En el siguiente ejemplo se usa la acción replace para cambiar un elemento de casilla de tarea pendiente a un estado completado.

```json
[
  {
    'target':'#task1',
    'action':'replace',
    'content':'<p data-tag="to-do:completed" data-id="task1">First task</p>'
  }
]
```

Vea [Uso de etiquetas de nota](onenote-note-tags.md) para más información sobre el uso del atributo **data-tag**.


<a name="complete-requests"></a>

### <a name="complete-patch-request-examples"></a>Ejemplos de solicitud PATCH completa

En los ejemplos siguientes se muestran solicitudes PATCH completas.

#### <a name="request-with-text-content-only"></a>Solicitud con solo contenido de texto

En el siguiente ejemplo se muestra una solicitud PATCH que utiliza el tipo de contenido **application/json**. Puede usar este formato cuando el contenido no contiene datos binarios.

```json
PATCH https://graph.microsoft.com/v1.0/me/onenote/notebooks/pages/{page-id}/content

Content-Type: application/json
Authorization: Bearer {token}

[
   {
    'target':'#para-id',
    'action':'insert',
    'position':'before',
    'content':'<img src="image-url" alt="New image from a URL" />'
  }, 
  {
    'target':'#list-id',
    'action':'append',
    'content':'<li>Item at the bottom of the list</li>'
  }
]
```
 
<a name="multipart"></a>

#### <a name="multipart-request-with-binary-content"></a>Solicitud de varias partes con contenido binario 

En el ejemplo siguiente se muestra una solicitud PATCH de varias partes que incluye datos binarios. Las solicitudes de varias partes requieren una parte "Comandos" que especifica el tipo de contenido **application/json** y contiene la matriz de objetos de cambio JSON. Otras partes de datos pueden contener datos binarios. Los nombres de parte suelen ser cadenas anexadas con la hora actual en milisegundos o un GUID aleatorio.

```json
PATCH https://graph.microsoft.com/v1.0/me/onenote/notebooks/pages/{page-id}/content

Content-Type: multipart/form-data; boundary=PartBoundary123
Authorization: Bearer {token}

--PartBoundary123
Content-Disposition: form-data; name="Commands"
Content-Type: application/json

[
  {
    'target':'img:{2998967e-69b3-413f-a221-c1a3b5cbe0fc}{42}',
    'action':'replace',
    'content':'<img src="name:image-part-name" alt="New binary image" />'
  }, 
  {
    'target':'#list-id',
    'action':'append',
    'content':'<li>Item at the bottom of the list</li>'
  }
]

--PartBoundary123
Content-Disposition: form-data; name="image-part-name"
Content-Type: image/png

... binary image data ...

--PartBoundary123--
```

<a name="request-response-info"></a>

## <a name="request-and-response-information-for-patch-requests"></a>Información de solicitud y respuesta de las solicitudes PATCH

| Datos de solicitud | Descripción |  
|------|------|  
| Protocolo | Todas las solicitudes usan el protocolo HTTPS SSL/TLS. |  
| Encabezado Authorization | <p>`Bearer {token}`, donde `{token}` es un token de acceso de OAuth 2.0 válido para la aplicación registrada.</p><p>Si falta o no es válido, la solicitud producirá errores con el código de estado 401. Vea [Authentication and permissions](permissions_reference.md) (Autenticación y permisos).</p> |  
| Encabezado Content-Type | <p>`application/json` para la matriz de objetos de cambio JSON, tanto si se envía directamente en el cuerpo del mensaje como si se envía en la parte "Comandos" necesaria de las [solicitudes de varias partes](#multipart-request-with-binary-content).</p><p>Se necesitan solicitudes de varias partes cuando se envían datos binarios y se utiliza el tipo de contenido `multipart/form-data; boundary=part-boundary`, donde `{part-boundary}` es una cadena que señala el inicio y el final de cada parte de datos.</p> |  

<br/> 

| Datos de respuesta | Descripción |  
|------|------|  
| Errores | Si la solicitud de actualización falla, la API devuelve errores en el objeto api.diagnostics en el cuerpo de la respuesta. La solicitud fallará si: |  
| Errores | Lea [Códigos de error para API de OneNote de Microsoft Graph](onenote_error_codes.md) para obtener información sobre los errores de OneNote que puede devolver Microsoft Graph. |  
 
 

<a name="root-url"></a>

### <a name="constructing-the-microsoft-graph-service-root-url"></a>Crear la URL raíz del servicio de Microsoft Graph

La dirección URL raíz del servicio OneNote utiliza el siguiente formato para todas las llamadas a la API de OneNote:

`https://graph.microsoft.com/{version}/me/onenote/`

El segmento `version` de la URL representa la versión de Microsoft Graph que se quiere utilizar. `v1.0` corresponde al código de producción estable. `beta` corresponde a la prueba de una característica que se encuentra en desarrollo. Las características y la funcionalidad de la versión beta pueden cambiar, por lo que no se debe usar en el código de producción.

`me` corresponde a contenido de OneNote al que el usuario actual tiene acceso (de su propiedad y compartido). `users/{id}` corresponde a contenido de OneNote que el usuario especificado (en la dirección URL) ha compartido con el usuario actual. Use la [API de Azure AD Graph](https://msdn.microsoft.com/library/azure/ad/graph/api/api-catalog).


> **Nota:** Puede obtener identificadores de usuario realizando una solicitud GET en `https://graph.microsoft.com/v1.0/users`.



<a name="permissions"></a>

## <a name="permissions"></a>Permisos

Para actualizar páginas OneNote, tiene que solicitar los permisos adecuados. Elija el nivel más bajo de permisos que necesita la aplicación para hacer su trabajo.

- Notes.ReadWrite
- Notes.ReadWrite.All

Para obtener más información sobre los ámbitos de permiso y cómo funcionan, consulte los [ámbitos de permisos de OneNote](permissions_reference.md).
   

<a name="see-also"></a>

## <a name="see-also"></a>Vea también

- [Agregar imágenes y archivos](onenote_images_files.md)
- [Integración con OneNote](integrate_with_onenote.md)
- [Blog para desarrolladores de OneNote](http://go.microsoft.com/fwlink/?LinkID=390183)
- [Preguntas de desarrollo de OneNote en Stack Overflow](http://go.microsoft.com/fwlink/?LinkID=390182)
- [Repositorios de OneNote en GitHub](http://go.microsoft.com/fwlink/?LinkID=390178)  
