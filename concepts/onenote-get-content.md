# <a name="get-onenote-content-and-structure-with-microsoft-graph"></a>Obtener el contenido y la estructura de OneNote con Microsoft Graph

*__Se aplica a:__ blocs de notas para consumidores de OneDrive | blocs de notas para empresa de Office 365*

Para obtener la estructura y el contenido de OneNote, envíe una solicitud GET al extremo de destino. Por ejemplo:

`GET ../onenote/pages/{id}`</p>

Si la solicitud es correcta, Microsoft Graph devuelve un código de estado HTTP 200 y las entidades o el contenido que ha solicitado. Las entidades de OneNote se devuelven como objetos JSON que cumplen la especificación de la versión 4.0 de OData.

Puede filtrar las consultas y mejorar el rendimiento usando las opciones de la cadena de consulta.


<a name="request-uri"></a>
## <a name="construct-the-request-uri"></a>Crear el URI de la solicitud

Para crear el URI de la solicitud, comience con la dirección URL raíz del servicio:

`https://graph.microsoft.com/v1.0/me/onenote`

Después, anexe el extremo del recurso que desea recuperar. ([Las rutas de acceso de recursos](#resource-paths-for-get-requests) se muestran en la siguiente sección).


Su URI de solicitud completa tendrá un aspecto similar a uno de estos ejemplos:
- `https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}/sections`</p>
- `https://graph.microsoft.com/v1.0/me/onenote/notes/pages`</p>
- `https://graph.microsoft.com/v1.0/me/onenote/pages?select=title,self`</p>

> **Nota:** Obtenga más información sobre la [URL de raíz del servicio](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).

<a name="resource-paths"></a>
## <a name="resource-paths-for-get-requests"></a>Rutas de acceso de recursos para las solicitudes GET

Use las siguientes rutas de acceso de recursos para obtener páginas, secciones, grupos de secciones, blocs de notas, imágenes u otros recursos de archivos.

[Colección de páginas](#page-collection)&nbsp;&nbsp;|&nbsp;&nbsp;[Entidad de página](#page-entity)&nbsp;&nbsp;|&nbsp;&nbsp;[Vista previa de página](#page-preview)&nbsp;&nbsp;|&nbsp;&nbsp;[Contenido HTML de página](#page-html-content)&nbsp;&nbsp;|&nbsp;&nbsp; [Colección de secciones](#section-collection)&nbsp;&nbsp;|&nbsp;&nbsp;[Entidad de sección](#section-entity)&nbsp;&nbsp;|&nbsp;&nbsp;[Colección de SectionGroup](#sectiongroup-collection)&nbsp;&nbsp;|&nbsp;&nbsp; [Entidad de SectionGroup](#sectiongroup-entity)&nbsp;&nbsp;|&nbsp;&nbsp;[Colección de blocs de notas](#notebook-collection)&nbsp;&nbsp;|&nbsp;&nbsp;[Entidad de bloc de notas](#notebook-entity)&nbsp;&nbsp;|&nbsp;&nbsp; [Imagen u otro recurso de archivo](#image-or-other-file-resource)

<a name="get-pages"></a>
### <a name="page-collection"></a>Colección de páginas

Obtener páginas (metadatos) en todos los blocs de notas

`../pages[?filter,orderby,select,expand,top,skip,search,count]`

Obtener páginas (metadatos) de una sección específica

`../sections/{section-id}/pages[?filter,orderby,select,expand,top,skip,search,count,pagelevel]`

 
La opción de cadena de consulta `search` solo está disponible para los blocs de notas de clientes.

El criterio de ordenación predeterminado para páginas es `lastModifiedTime desc`.

La consulta predeterminada expande la sección principal y selecciona y selecciona las propiedades `id`, `name` y `self` de la sección.

De forma predeterminada, solo se devuelven las 20 entradas principales para las solicitudes *GET pages*. Las solicitudes que no se especifican una opción de cadena de consulta **superior** devuelven un vínculo **@odata.nextLink** en la respuesta que puede usar para obtener las siguientes 20 entradas.

Para la colección de páginas de una sección, use **pagelevel** para obtener el nivel de sangría de las páginas y su orden en la sección. 

**Ejemplo:** `GET ../sections/{section-id}/pages?pagelevel=true`.  

- - -

<a name="get-page"></a> 
### <a name="page-entity"></a>Entidad de página

Obtenga los metadatos de una página específica. 

`../pages/{page-id}[?select,expand,pagelevel]` 


Las páginas pueden expandir las propiedades **parentNotebook** y **parentSection**.

La consulta predeterminada expande la sección principal y selecciona y selecciona las propiedades `id`, `name` y `self` de la sección.

Use **pagelevel** para obtener el nivel de sangría de la página y el su orden en la sección principal. Ejemplo: `GET ../pages/{page-id}?pagelevel=true`.

- - -

<a name="get-page-preview"></a> 
### <a name="page-preview"></a>Vista previa de la página

Obtener el contenido de vista previa de texto e imágenes de una página

`../pages/{page-id}/preview`


La respuesta JSON contiene el contenido de la vista previa, que puede usar para ayudar a los usuarios a identificar los elementos en la página.

```json
{
  "@odata.context":"https://www.onenote.com/api/v1.0/$metadata#Microsoft.OneNote.Api.PagePreview",
  "previewText":"text-snippet",
  "links":{
    "previewImageUrl":{
      "href":"https://www.onenote.com/api/v1.0/resources/{id}/content?publicAuth=true&mimeType=image/png"
    }
  }
}
```

La propiedad **previewText** contiene un fragmento de texto de la página. Microsoft Graph devuelve frases completas, hasta un máximo de 300 caracteres. 

Si la página tiene una imagen que puede usarse para crear una vista previa de la interfaz de usuario, la propiedad **href** en el objeto **previewImageUrl** contiene un vínculo a un [recurso de imagen](#image-or-other-file-resource) público que ya se ha autenticado. Puede usar este vínculo en HTML,

**Ejemplo:** `<img src="https://www.onenote.com/api/v1.0/resources/{id}/content?publicAuth=true&mimeType=image/png" />`. En caso contrario, **href** devuelve un valor nulo.

- - -

<a name="get-page-content"></a> 
### <a name="page-html-content"></a>Contenido HTML de página

Obtener el contenido HTML de una página `../pages/{page-id}/content[?includeIDs,preAuthenticated]`

(*obtenga más información sobre [ contenido HTML devuelto](onenote_input_output_html.md)*) 

 
Use la opción de cadena de consulta **includeIDs=true** para obtener ID generadas que se usan para [actualizar la página](onenote_update_page.md).

Use la opción de cadena de consulta **preAuthenticated=true** para obtener las direcciones URL públicas para los [recursos de imagen](#image-or-other-file-resource) que están en la página. Las direcciones URL públicas son válidas durante una hora. 

- - -

<a name="get-sections"></a>
### <a name="section-collection"></a>Colección de sitios

Obtener todas las secciones de todos los blocs de notas que posee el usuario, incluyendo las secciones en grupos de secciones anidados `../sections[?filter,orderby,select,top,skip,expand,count]` 

Obtener todas las secciones que están directamente en un grupo de secciones específico

`../sectionGroups/{sectiongroup-id}/sections[?filter,orderby,select,top,skip,expand,count]` 

Obtener todas las secciones que están directamente en un bloc de notas específico `../notebooks/{notebook-id}/sections[?filter,orderby,select,top,skip,expand,count]` 

 
Las secciones pueden expandir las propiedades **parentNotebook** y **parentSectionGroup**.

El criterio de ordenación predeterminado para secciones es `name asc`.

La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.

- - -

<a name="get-section"></a>
### <a name="section-entity"></a>Entidad de sección

Obtener una sección específica

`../sections/{section-id}[?select,expand]` 

 
Las secciones pueden expandir las propiedades **parentNotebook** y **parentSectionGroup**.

La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.

- - -

<a name="get-section-groups"></a>
### <a name="sectiongroup-collection"></a>Colección de SectionGroup

Obtener todos los grupos secciones de todos los blocs de notas que posee el usuario, incluyendo los grupos de secciones anidados

`../sectionGroups[?filter,orderby,select,top,skip,expand,count]` 

Obtener todos los grupos de secciones que están directamente en un bloc de notas específico 

`../notebooks/{notebook-id}/sectionGroups[?filter,orderby,select,top,skip,expand,count]` 

Los grupos de secciones pueden expandir las propiedades **sections**, **sectionGroups**, **parentNotebook** y **parentSectionGroup**.

El criterio de ordenación predeterminado para grupos de secciones es `name asc`.

La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.

- - -

<a name="get-section-group"></a>
### <a name="sectiongroup-entity"></a>Entidad de SectionGroup

Obtener un grupo de secciones específico

`../sectionGroups/{sectiongroup-id}[?select,expand]` 


Los grupos de secciones pueden expandir las propiedades **sections**, **sectionGroups**, **parentNotebook** y **parentSectionGroup**.

La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.

- - -

<a name="get-notebooks"></a>
### <a name="notebook-collection"></a>Colección de blocs de notas

Obtener todos los blocs de notas que posee el usuario 

`../notebooks[?filter,orderby,select,top,skip,expand,count]` 

 
Los blocs de notas pueden expandir las propiedades **sections** y **sectionGroups**.

El criterio de ordenación predeterminado para blocs de notas es `name asc`. 

- - -

<a name="get-notebook"></a>
### <a name="notebook-entity"></a>Entidad de bloc de notas

Obtener un bloc de notas específico `../notebooks/{notebook-id}[?select,expand]` 


Los blocs de notas pueden expandir las propiedades **sections** y **sectionGroups**.

- - -

<a name="get-resource"></a>
### <a name="image-or-other-file-resource"></a>Imágenes u otros recursos de archivo

Acceder a los datos binarios de un recurso específico 

`../resources/{resource-id}/$value` 


Puede encontrar el URI del recurso de archivo en el [resultado HTML](onenote_input_output_html.md) de la página.

Por ejemplo, una etiqueta **img** incluye extremos del recurso de imagen original en el atributo **data-fullres-src** y de la imagen optimizada en el atributo **src**. 

**Ejemplo:**

```
<img 
    src="https://www.onenote.com/api/v1.0/me/notes/resources/{image-id}/$value"  
    data-src-type="image/png"
    data-fullres-src="https://www.onenote.com/api/v1.0/resources/{image-id}/$value"  
    data-fullres-src-type="image/png" ... />
```

Una etiqueta **object** incluye el extremo del recurso de archivos en el atributo **data**. 

**Ejemplo:**

```
<object
    data="http://www.onenote.com/api/v1.0/me/notes/resources/{file-id}/$value"
    data-attachment="fileName.pdf" 
    type="application/pdf" ... />
```

Para obtener direcciones URL públicas que ya se han autenticado a los recursos de imagen en una página, incluya **preAuthenticated=true** en la cadena de consulta cuando [recupere el contenido de la página](#page-html-content) (**ejemplo:** `GET ../pages/{page-id}/content?preAuthenticated=true`). Las direcciones URL públicas que se devuelven en el [HTML de salida](onenote_input_output_html.md#output-html-examples-for-images) son válidas durante una hora. Sin esta etiqueta, las imágenes devueltas no se representarán directamente en un explorador porque son privadas y se necesita una autorización para recuperarlas, al igual que el contenido de la página. 

> **Nota:** no se admite la obtención de una colección de recursos. 

Cuando obtiene un recurso de archivos, no es necesario incluir un tipo de contenido **Accept** en la solicitud.

Para obtener más información sobre las solicitudes GET, consulte: 
- [GET Pages](../api-reference/v1.0/api/page_get.md)
- [GET Sections](../api-reference/v1.0/api/section_get.md)
- [GET SectionGroups](../api-reference/v1.0/api/sectiongroup_get.md)
- [GET Notebooks](../api-reference/v1.0/api/notebook_get.md) 

en la referencia de la API de REST de Microsoft Graph.


<a name="example"></a>
## <a name="example-get-requests"></a>Solicitudes GET de ejemplo
Puede consultar las entidades de OneNote y el contenido de la página de búsqueda para obtener solo la información que necesita. Los siguientes ejemplos muestran algunas formas en las que puede usar [opciones de cadena de consulta compatibles](#supported-odata-query-string-options) en las solicitudes GET a Microsoft Graph. 

**Recuerde:**

- Todas las solicitudes GET empiezan con la [dirección URL raíz de servicio](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).

  **Ejemplos:** 
  - `https://www.onenote.com/api/v1.0/me/notes`
  - `https://www.onenote.com/api/v1.0/myOrganization/siteCollections/{id}/sites/{id}/notes/`

- Los espacios en la cadena de consulta URL deben usar la codificación %20.

Ejemplo: `filter=title%20eq%20'biology'`

- Los nombres de propiedad y las comparaciones de cadenas de OData distinguen mayúsculas de minúsculas. Se recomienda usar la función **tolower** de OData para comparaciones de cadenas.

   Ejemplo: `filter=tolower(name) eq 'spring'`
 

**search & filter**  

Obtienen todas las páginas que contienen el término *receta* creadas por una aplicación específica.  (`search` solo está disponible para los blocs de notas de clientes)

```
[GET] ../pages?search=recipe&filter=createdByAppId eq 'WLID-000000004C12821A'
```
 
**search & select**  

Obtienen el título, los vínculos de cliente de OneNote y el vínculo de **contentUrl** para todas las páginas que contienen el término *golgi app*.  (`search` solo está disponible para los blocs de notas de clientes)

```
[GET] ../pages?search=golgi app&select=title,links,contentUrl
```
 
**expand**  

Obtienen todos los blocs de notas y expanden sus secciones y grupos de secciones.  

```
[GET] ../notebooks?expand=sections,sectionGroups
```
 
Obtienen un grupo de secciones específico y expanden sus secciones y grupos de secciones.  

```
[GET] ../sectionGroups/{sectiongroup-id}?expand=sections,sectionGroups
```

Obtienen una página y expanden su sección principal y bloc de notas principal.

```
[GET] ../pages/{page-id}?expand=parentSection,parentNotebook
```

**expand** (varios niveles)  

Obtienen todos los blocs de notas y expanden sus secciones y grupos de secciones, y expanden todas las secciones en cada grupo de secciones.  

```
[GET] ../notebooks?expand=sections,sectionGroups(expand=sections)
```
 
>No se admite expandir elementos primarios de entidades secundarias o expandir elementos secundarios de entidades primarias. Hacer eso crearía una referencia circular.

 
**expand & select** (varios niveles)  

Obtienen el nombre y el vínculo a **self** para un grupo de secciones específico, y obtienen el nombre y los vínculos a **self** para todas sus secciones.  

```
[GET] ../sectionGroups/{sectiongroup-id}?expand=sections(select=name,self)&select=name,self
```
 
Obtienen el nombre y el vínculo a **self** para todas las secciones, y obtienen el nombre y la hora de creación del bloc de notas primario de cada sección.  

```
[GET] ../sections?expand=parentNotebook(select=name,createdTime)&select=name,self
```
 
Obtienen el título y el identificador de todas las páginas, y obtienen el nombre de la sección principal y bloc de notas principal.

```
[GET] ../pages?select=id,title&expand=parentSection(select=name),parentNotebook(select=name)
```

**expand & levels** (varios niveles)  

Obtienen todos los blocs de notas, grupos de secciones y todas las secciones.  

```
[GET] ../notebooks?expand=sections,sectionGroups(expand=sections,sectionGroups(levels=max;expand=sections))
```
 
**filter**  

Obtienen todas las secciones creadas en octubre de 2014.

```
[GET] ../sections?filter=createdTime ge 2014-10-01 and createdTime le 2014-10-31
```

Obtienen todas las páginas creadas por una aplicación específica desde el 1 de enero de 2015.

```
[GET] ../pages?filter=createdByAppId eq 'WLID-0000000048118631' and createdTime ge 2015-01-01
```

**filter & expand**  

Obtienen todas las páginas de un bloc de notas específico. La API devuelve 20 entradas de forma predeterminada.

```
[GET] ../pages?filter=parentNotebook/id eq '{notebook-id}'&expand=parentNotebook
```

Obtienen el nombre y el vínculo a **pagesUrl** para todas las secciones del bloc de notas *Escuela*. Las comparaciones de cadenas OData distinguen mayúsculas de minúsculas, por lo que se recomienda usar la función **tolower**.

```
[GET] ../notebooks?filter=tolower(name) eq 'school'&expand=sections(select=name,pagesUrl)
```

**filter & select & orderby**   

Obtienen el nombre y el vínculo a **pagesUrl** para todas las secciones que contienen el término *spring* en el nombre de la sección. Ordenan las secciones por fecha de última modificación.

```
[GET] ../sections?filter=contains(tolower(name),'spring')&select=name,pagesUrl&orderby=lastModifiedTime desc
```
 
**orderby**  

Obtienen las primeras 20 páginas ordenadas por propiedad **createdByAppId** y luego por fecha de creación más reciente. La API devuelve 20 entradas de forma predeterminada.

```
[GET] ../pages?orderby=createdByAppId,createdTime desc
```

**search & filter & top**  

Obtienen las cinco páginas más recientes creadas desde el 1 de enero de 2015, que contienen la frase *división de celda*. La API devuelve 20 entradas de forma predeterminada con un máximo de 100. El criterio de ordenación predeterminado para páginas es `lastModifiedTime desc`. (`search` solo está disponible para los blocs de notas de clientes)

```
[GET] ../pages?search="cell division"&filter=createdTime ge 2015-01-01&top=5
```

**search & filter & top & skip**  

Obtienen las cinco páginas siguientes en el conjunto de resultados. (`search` solo está disponible para los blocs de notas de clientes)

```
[GET] ../pages?search=biology&filter=createdTime ge 2015-01-01&top=5&skip=5
```

Y las cinco siguientes. (`search` solo está disponible para los blocs de notas de clientes)

```
[GET] ../pages?search=biology&filter=createdTime ge 2015-01-01&top=5&skip=10
```

> **Nota:** Si se aplican **search** y **filter** a la misma solicitud, los resultados incluyen solamente las entidades que coinciden con ambos criterios.
 
**select**  

Obtienen el nombre, la hora de creación y el vínculo a **self** para todas las secciones en los blocs de notas del usuario.

```
[GET] ../sections?select=name,createdTime,self
```

Obtienen el título, la hora de creación y los vínculos a clientes de OneNote para una página específica.

```
[GET] ../pages/{page-id}?select=title,createdTime,links
```

**select & expand & filter** (varios niveles)  

Obtienen el nombre y el vínculo a **pagesUrl** para todas las secciones en el bloc de notas predeterminado del usuario.

```
[GET] ../notebooks?select=name&expand=sections(select=name,pagesUrl)&filter=isDefault eq true
```

**top & select & orderby**  

Obtienen el título y el vínculo **self** de las primeras 50 páginas, ordenadas alfabéticamente por título. La API devuelve 20 entradas de forma predeterminada con un máximo de 100. El criterio de ordenación predeterminado para páginas es `lastModifiedTime desc`.

```
[GET] ../pages?top=50&select=title,self&orderby=title
```

**skip & top & select & orderby**  

Obtienen las páginas 51 a 100. La API devuelve 20 entradas de forma predeterminada con un máximo de 100.

```
[GET] ../pages?skip=50&top=50&select=title,self&orderby=title
```

> **Note:** Las solicitudes GET para páginas que recuperan el número predeterminado de entradas (es decir, no especifican una expresión **top**) devuelven un vínculo a **@odata.nextLink** en la respuesta que puede usar para obtener las 20 entradas siguientes.
 

<a name="query-options"></a>
## <a name="supported-odata-query-string-options"></a>Opciones de cadena de consultas OData admitidas

Al enviar solicitudes GET a Microsoft Graph, puede usar las opciones de cadena de consultas OData para personalizar la consulta y obtener solo la información que necesita. También puede mejorar el rendimiento al reducir el número de llamadas al servicio y el tamaño de la carga de respuesta.

> **Note:** Para su legibilidad, los ejemplos de este artículo no usan la codificación porcentual de %20 que se requiere para espacios en la cadena de consulta URL: `filter=isDefault%20eq%20true`
 
| Opción de consulta | Ejemplo y descripción |  
|------|------|  
| count | <p>`count=true`</p><p>El recuento de entidades de la colección. El valor se devuelve en la propiedad **@odata.count** de la respuesta.</p> |  
| expand | <p>`expand=sections,sectionGroups`</p><p>Las propiedades de navegación para devolver la respuesta en línea. Las siguientes propiedades son compatibles con las expresiones **expand**:<br /> - Páginas: **parentNotebook**, **parentSection**<br /> - Secciones: **parentNotebook**, **parentSectionGroup**<br /> - Grupos de secciones: **sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**<br /> - Blocs de notas: **sections**, **sectionGroups**</p><p>De forma predeterminada, las solicitudes GET de páginas expanden **parentSection** y seleccionan las propiedades **id**, **name** y **self** de la sección. Las solicitudes GET predeterminadas para secciones y grupos de secciones expanden tanto **parentNotebook** como **parentSectionGroup**, y seleccionan las propiedades **id**, **name** y **self** del elemento primario. </p><p>Puede usarse para una única entidad o una colección. Separe las distintas propiedades mediante comas. Los nombres de las propiedades distinguen mayúsculas de minúsculas.</p> |   
| filter | <p>`filter=isDefault eq true`</p><p>Una expresión booleana por si desea incluir una entrada en el conjunto de resultados. Es compatible con las funciones y operadores de OData siguientes:<br /> - Operadores de comparación: **eq**, **ne**, **gt**, **ge**, **lt**, **le**<br /> - Operadores lógicos: **and**, **or**, **not**<br /> - Funciones de cadena: **contains**, **endswith**, **startswith**, **length**, **indexof**, **substring**, **tolower**, **toupper**, **trim**, **concat**</p><p>[Los nombres de propiedad](#onenote-entity-properties) y las comparaciones de cadenas de OData distinguen mayúsculas de minúsculas. Se recomienda usar la función **tolower** de OData para comparaciones de cadenas. Ejemplo: `filter=tolower(name) eq 'spring'`</p> |  
| orderby | <p>`orderby=title,createdTime desc`</p><p>Las [propiedades](#onenote-entity-properties) por las que se va a ordenar, con un criterio de ordenación **asc** (predeterminado) o **desc** opcional. Puede ordenar por cualquier propiedad de la entidad en la colección solicitada.</p><p>El orden predeterminado para blocs de notas, secciones y grupos de secciones es `name asc`, y para páginas es `lastModifiedTime desc` (última página modificada primero).</p><p>Si tiene varias propiedades, sepárelas con comas, y ordénelas con el orden en que desea que se apliquen. Los nombres de las propiedades distinguen mayúsculas de minúsculas.</p> |  
| buscar | <p>`search=cell div`</p><p>Solo está disponible para los blocs de notas de clientes.</p><p>El término o la frase para buscar en el título de la página, el cuerpo de la página, el texto alternativo de la imagen y el texto OCR de la imagen. De forma predeterminada, las consultas de búsqueda devuelven resultados ordenados por relevancia.</p><p>OneNote usa la búsqueda de texto completo de Bing para admitir búsqueda de frases, lematización, omisión ortográfica, relevancia y clasificación, separación de palabras, varios idiomas y otras características de búsqueda de texto completo. Las cadenas de búsqueda distinguen mayúsculas de minúsculas.</p><p>Solo se aplica a las páginas de los blocs de notas que posee el usuario (no a los que se comparten con el usuario). El contenido indexado es privado y solo puede acceder a él su propietario. Las páginas protegidas con contraseña no están indexadas. Solo se aplica al extremo `pages`.</p> |  
| select | <p>`select=id,title`</p><p>Las [propiedades](#onenote-entity-properties) que se devuelven. Puede usarse para una única entidad o para una colección. Separe las distintas propiedades mediante comas. Los nombres de las propiedades distinguen mayúsculas de minúsculas.</p> |  
| skip | <p>`skip=10`</p><p>El número de entradas que se omiten del conjunto de resultados. Se usa normalmente para los resultados de paginación.</p> |  
| top | <p>`top=50`</p><p>El número de entradas para devolver en el conjunto de resultados, hasta un máximo de 100. El valor predeterminado es 20.</p> |  

Microsoft Graph también proporciona la opción de cadena de consulta `pagelevel` que puede usar para obtener el nivel y el orden de las páginas en la sección principal. Solo se aplica a las consultas para las páginas de una sección específica o para una página específica. 

**Ejemplo:** 

- `GET ../sections/{section-id}/pages?pagelevel=true` 
- `GET ../pages/{page-id}?pagelevel=true` 

### <a name="supported-odata-operators-and-functions"></a>Operadores y funciones OData compatibles

Microsoft Graph admite los siguientes operadores y funciones OData en las expresiones **filter**. Al usar expresiones OData, recuerde:  
- Debe reemplazar los espacios en la cadena de consulta URL con la codificación `%20`.

   **Ejemplo:** `filter=isDefault%20eq%20true`
- Los nombres de propiedad y las comparaciones de cadenas de OData distinguen mayúsculas de minúsculas. Se recomienda usar la función **tolower** de OData para comparaciones de cadenas.
   
   **Ejemplo:** `filter=tolower(name) eq 'spring'`

| Operador de comparación | Ejemplo |  
|------|------|  
| eq<br />(igual a) | `createdByAppId eq '{app-id}'` |  
| ne<br />(no es igual a) | `userRole ne 'Owner'` |  
| gt<br />(mayor que) | `createdTime gt 2014-02-23` |  
| ge<br />(mayor o igual que) | `lastModifiedTime ge 2014-05-05T07:00:00Z` |  
| lt<br />(menor que) | `createdTime lt 2014-02-23` |  
| le<br />(menor que o igual que) | `lastModifiedTime le 2014-02-23` |  
 
| Operador lógico | Ejemplo |  
|------|------|  
| y | `createdTime le 2014-01-30 and createdTime gt 2014-01-23` |  
| o | `createdByAppId eq '{app-id}' or createdByAppId eq '{app-id}'` |  
| 
not | `not contains(tolower(title),'school')` |  
 
| Función String | Ejemplo |  
|------|------|   
| contains | `contains(tolower(title),'spring')` |  
| endswith | `endswith(tolower(title),'spring')` |  
| startswith | `startswith(tolower(title),'spring')` |  
| length | `length(title) eq 19` |  
| indexof | `indexof(tolower(title),'spring') eq 1` |  
| substring | `substring(tolower(title),1) eq 'spring'` |  
| tolower | `tolower(title) eq 'spring'` |  
| toupper | `toupper(title) eq 'SPRING'` |  
| trim | `trim(tolower(title)) eq 'spring'` |  
| concat | `concat(title,'- by MyRecipesApp') eq 'Carrot Cake Recipe - by MyRecipesApp'` |  
 

<a name="properties"></a>
## <a name="onenote-entity-properties"></a>Propiedades de entidad de OneNote

Las expresiones de consulta **filter**, **select**, **expand** y **orderby** pueden incluir propiedades de las entidades de OneNote. 

**Ejemplo:**

`../sections?filter=createdTime ge 2015-01-01&select=name,pagesUrl&orderby=lastModifiedTime desc` 

Los nombres de las propiedades distinguen mayúsculas de minúsculas en las expresiones de consulta.

Para la lista de propiedades y tipos de propiedades, consulte:

- [GET Pages](../api-reference/v1.0/api/page_get.md)
- [GET Sections](../api-reference/v1.0/api/section_get.md)
- [GET SectionGroups](../api-reference/v1.0/api/sectiongroup_get.md)
- [GET Notebooks](../api-reference/v1.0/api/notebook_get.md) 

en la referencia de la API de REST de Microsoft Graph.

La opción de cadena de consulta **expand** se puede usar con las siguientes propiedades de navegación:

- Páginas: **parentNotebook**, **parentSection**
- Secciones: **parentNotebook**, **parentSectionGroup**
- Grupos de secciones: **sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**
- Blocs de notas: **sections**, **sectionGroups**


<a name="request-response-info"></a>
## <a name="request-and-response-information-for-get-requests"></a>Información de la solicitud y respuesta para las solicitudes *GET*

| Datos de solicitud | Descripción |  
|------|------|  
| Protocolo | Todas las solicitudes usan el protocolo HTTPS SSL/TLS. |  
| Encabezado Authorization | <p>`Bearer {token}`, donde *{token}* es un token de acceso de OAuth 2.0 válido para la aplicación registrada.</p><p>Si falta o no es válido, se produce un error en la solicitud con un código de estado 401. Vea [Authentication and permissions](permissions_reference.md) (Autenticación y permisos).</p> |  
| Encabezado Accept | <p>- `application/json` para las entidades y los conjuntos de entidades de OneNote</p><p>- `text/html` para contenido de la página</p> | 

| Datos de respuesta | Descripción |  
|------|------|  
| Código de correcto | Un código de estado HTTP 200. |  
| Cuerpo de la respuesta | Una representación de OData de la entidad o entidad establecida en formato JSON, el HTML de la página, o datos binarios recursos de un recurso de archivo.  |  
| Errores | Si se produce un error en la solicitud, la API devuelve [errors](onenote_error_codes.md) en el objeto **@api.diagnostics** en el cuerpo de la respuesta. |  
| Encabezado X-CorrelationId | GUID que identifica la solicitud de manera única. Puede usar este valor junto con el valor del encabezado de fecha al trabajar con el soporte técnico de Microsoft para solucionar problemas. |  


<a name="root-url"></a>
### <a name="constructing-the-microsoft-graph-notes-service-root-url"></a>Crear la dirección URL raíz del servicio de notas de Microsoft Graph

La dirección URL raíz de notas de Microsoft Graph usa el siguiente formato para todas las llamadas a las notas de Microsoft Graph. `https://graph.microsoft.com/{version}/me/onenote/` El segmento `version` de la dirección URL representa la versión de Microsoft Graph que desea usar. Use `v1.0` para el código de producción estable. Use `beta` para probar una característica que se encuentra en desarrollo. Las características y la funcionalidad de la versión beta pueden cambiar, por lo que no se debe usar en el código de producción. Use `me` para contenido de OneNote al que pueda acceder el usuario actual (de su propiedad y compartido). Use `users/{id}` para contenido de OneNote que el usuario especificado (en la dirección URL) ha compartido con el usuario actual. Use [Microsoft Graph](https://graph.microsoft.com/v1.0/users) para obtener los identificadores de usuario. 


<a name="permissions"></a>
## <a name="permissions-for-get-requests"></a>Permisos de solicitudes GET

Para obtener el contenido o la estructura de OneNote, debe solicitar los permisos adecuados. 

Los siguientes ámbitos permiten obtener solicitudes a Microsoft Graph. Elija el nivel más bajo de permisos que necesita la aplicación para hacer su trabajo.

Elija entre: 
- Notes.read
- Notes.ReadWrite
- Notes.ReadWrite.All


Para obtener más información sobre los ámbitos de permiso y cómo funcionan, consulte [Referencia de permisos de Microsoft Graph](permissions_reference.md).

<a name="see-also"></a>
## <a name="additional-resources"></a>Recursos adicionales

- [HTML de entrada y salida para páginas de OneNote](onenote_input_output_html.md)
- [Integración con OneNote](integrate_with_onenote.md)
- [Blog para desarrolladores de OneNote](http://go.microsoft.com/fwlink/?LinkID=390183)
- [Preguntas de desarrollo de OneNote en Stack Overflow](http://go.microsoft.com/fwlink/?LinkID=390182)
- [Repositorios de OneNote en GitHub](http://go.microsoft.com/fwlink/?LinkID=390178)  
