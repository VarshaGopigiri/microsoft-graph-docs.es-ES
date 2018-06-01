# <a name="update-onenote-page-content"></a><span data-ttu-id="a9e98-101">Actualizar el contenido de la página de OneNote</span><span class="sxs-lookup"><span data-stu-id="a9e98-101">Update OneNote page content</span></span>

<span data-ttu-id="a9e98-102">*__Se aplica a:__ blocs de notas para consumidores de OneDrive | blocs de notas para empresa de Office 365*</span><span class="sxs-lookup"><span data-stu-id="a9e98-102">*__Applies to:__ Consumer notebooks on OneDrive | Enterprise notebooks on Office 365*</span></span>


<span data-ttu-id="a9e98-103">Para actualizar el contenido de una página de OneNote, envíe una solicitud PATCH al punto de conexión *content* de la página.</span><span class="sxs-lookup"><span data-stu-id="a9e98-103">To retrieve the HTML content of a onnvshort page, you send a GET request to  the page's content endpoint:</span></span>

`PATCH ../notes/pages/{id}/content`</p>

<span data-ttu-id="a9e98-104">Envíe un objeto de cambio JSON en el cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a9e98-104">Send a JSON change object in the message body.</span></span> <span data-ttu-id="a9e98-105">Si la solicitud es correcta, Microsoft Graph devuelve un código de estado HTTP 204.</span><span class="sxs-lookup"><span data-stu-id="a9e98-105">If the create request is successful, the onnvshort API returns a 201 HTTP status code.</span></span>


<a name="request-uri"></a>
## <a name="construct-the-request-uri"></a><span data-ttu-id="a9e98-106">Crear el URI de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a9e98-106">Construct the request</span></span>

<span data-ttu-id="a9e98-107">Para crear el URI de la solicitud, comience con la dirección URL raíz del servicio:</span><span class="sxs-lookup"><span data-stu-id="a9e98-107">To construct the request URI, start with the service root URL:</span></span>

`https://graph.microsoft.com/v1.0/me/onenote`

<span data-ttu-id="a9e98-108">Luego anexe el punto de conexión *content* de la página:</span><span class="sxs-lookup"><span data-stu-id="a9e98-108">Then append the page's *content* endpoint:</span></span>

<span data-ttu-id="a9e98-109">**Obtenga el HTML de página y todos los valores de *data-id* definidos**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-109">**Get the page HTML and all defined *data-id* values**</span></span></p>
`../pages/{id}/content`   

<span data-ttu-id="a9e98-110">**Obtenga el HTML de página y todos los valores de *data-id* definidos y todos los valores de *id* generados**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-110">**Get the page HTML, all defined *data-id* values, and all generated *id* values**</span></span>  
`../pages/{page-id}/content?includeIDs=true` 

<span data-ttu-id="a9e98-111">Los valores de **data-id** y de **id** se usan como identificadores **target** de los elementos que se quieren actualizar.</span><span class="sxs-lookup"><span data-stu-id="a9e98-111">The **data-id** and **id** values are used as **target** identifiers for the elements you want to update.</span></span>

 
<span data-ttu-id="a9e98-112">El identificador URI de solicitud completo tendrá un aspecto similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="a9e98-112">Your full request URI will look like this:</span></span>

`https://graph.microsoft.com/v1.0/me/onenote/pages/{id}/content`


<span data-ttu-id="a9e98-113">Obtenga más información sobre la [dirección URL raíz del servicio](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).</span><span class="sxs-lookup"><span data-stu-id="a9e98-113">Learn more about the [service root URL](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).</span></span>


<a name="message-body"></a>
## <a name="construct-the-message-body"></a><span data-ttu-id="a9e98-114">Crear al cuerpo del mensaje</span><span class="sxs-lookup"><span data-stu-id="a9e98-114">Construct the message body</span></span>

<span data-ttu-id="a9e98-115">El código HTML de una página de OneNote contiene texto, imágenes y otro contenido organizado en estructuras tales como **div**, **img** y **ol** elementos.</span><span class="sxs-lookup"><span data-stu-id="a9e98-115">The HTML of a onnvshort page contains text, images, and other content organized into structures such as div, img, and ol elements. To update page HTML, you send a PATCH request to the page's content endpoint:</span></span> <span data-ttu-id="a9e98-116">Para actualizar el contenido de la página de OneNote, puede agregar y reemplazar elementos HTML en la página.</span><span class="sxs-lookup"><span data-stu-id="a9e98-116">To update OneNote page content, you add and replace HTML elements on the page.</span></span>

<span data-ttu-id="a9e98-117">Los cambios se envían en el cuerpo del mensaje como matriz de objetos de cambio JSON.</span><span class="sxs-lookup"><span data-stu-id="a9e98-117">Your changes are sent in the message body as an array of JSON change objects.</span></span> <span data-ttu-id="a9e98-118">Cada objeto especifica el nuevo contenido HTML del elemento de destino y qué hacer con el contenido.</span><span class="sxs-lookup"><span data-stu-id="a9e98-118">Your changes are sent in the request body as an array of JSON objects. Each object specifies the target element,  new HTML content, and what to do with the content.</span></span>

<span data-ttu-id="a9e98-p104">La siguiente matriz define dos cambios. El primero inserta una imagen arriba del párrafo como un elemento relacionado, el segundo anexa un elemento a la lista como un último elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="a9e98-p104">The following array defines two changes. The first inserts an image above a paragraph as a sibling, and the second appends an item to a list as a last child.</span></span>

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

<span data-ttu-id="a9e98-121">Vea [más ejemplos](#example-requests).</span><span class="sxs-lookup"><span data-stu-id="a9e98-121">See [more examples](#example-requests).</span></span>


### <a name="attributes-for-json-change-objects"></a><span data-ttu-id="a9e98-122">Atributos para los objetos de cambio JSON</span><span class="sxs-lookup"><span data-stu-id="a9e98-122">Attributes for JSON objects</span></span>

<span data-ttu-id="a9e98-123">Use los atributos **target**, **action**, **position** y **content** para definir objetos JSON para solicitudes PATCH.</span><span class="sxs-lookup"><span data-stu-id="a9e98-123">Use the **target**, **action**, **position**, and **content** attributes to define JSON objects for PATCH requests.</span></span>

<span data-ttu-id="a9e98-124">**target**</span><span class="sxs-lookup"><span data-stu-id="a9e98-124">**target**</span></span>  
<span data-ttu-id="a9e98-p105">Elemento que se va a actualizar. El valor debe ser uno de los siguientes identificadores:</span><span class="sxs-lookup"><span data-stu-id="a9e98-p105">The element to update. The value must be one of the following identifiers:</span></span>

| <span data-ttu-id="a9e98-127">Identificador</span><span class="sxs-lookup"><span data-stu-id="a9e98-127">Identifier</span></span> | <span data-ttu-id="a9e98-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9e98-128">Description</span></span> |  
|------|------|  
| <span data-ttu-id="a9e98-129">#{data-id}</span><span class="sxs-lookup"><span data-stu-id="a9e98-129">data-id</span></span> | <p><span data-ttu-id="a9e98-130">Este identificador se define opcionalmente en los elementos del HTML de entrada [al crear una página](onenote-create-page.md) o [actualizar una página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="a9e98-130">This ID is optionally defined on elements in the input HTML when [creating a page](onenote-create-page.md) or [updating a page](onenote_update_page.md).</span></span> <span data-ttu-id="a9e98-131">Use # como prefijo.</span><span class="sxs-lookup"><span data-stu-id="a9e98-131">Prefix the value with a #.</span></span></p><p> <span data-ttu-id="a9e98-132">Ejemplo: `'target':'#intro'` tiene como destino el elemento `<div data-id="intro" ...>`</span><span class="sxs-lookup"><span data-stu-id="a9e98-132">Example: `'target':'#intro'` targets the element `<div data-id="intro" ...>`</span></span></p> |  
| <span data-ttu-id="a9e98-133">id</span><span class="sxs-lookup"><span data-stu-id="a9e98-133">id</span></span> | <p><span data-ttu-id="a9e98-134">Se trata del [identificador generado](#generated-ids) en Microsoft Graph, y es necesario para la mayoría de las operaciones de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="a9e98-134">This is the [generated ID](#generated-ids) from Microsoft Graph, and is required for most replace operations.</span></span> <span data-ttu-id="a9e98-135">No use # como prefijo.</span><span class="sxs-lookup"><span data-stu-id="a9e98-135">Do not prefix with a #.</span></span></p><p> <span data-ttu-id="a9e98-136">Ejemplo: `'target':'div:{33f8a2...}{37}'` tiene como destino el elemento `<div id="div:{33f8a2...}{37}" ...>`</span><span class="sxs-lookup"><span data-stu-id="a9e98-136">Example: `'target':'div:{33f8a2...}{37}'` targets the element `<div id="div:{33f8a2...}{37}" ...>`</span></span></p><p><span data-ttu-id="a9e98-137">No debe confundirse con los valores de **id** definidos en el [HTML de entrada](onenote_input_output_html.md).</span><span class="sxs-lookup"><span data-stu-id="a9e98-137">Don't confuse these with any **id** values defined in the [input HTML](onenote_input_output_html.md).</span></span> <span data-ttu-id="a9e98-138">Todos los valores de **id** enviados en el HTML de entrada se descartan.</span><span class="sxs-lookup"><span data-stu-id="a9e98-138">All **id** values sent in the input HTML are discarded.</span></span></p> |  
| <span data-ttu-id="a9e98-139">body</span><span class="sxs-lookup"><span data-stu-id="a9e98-139">body</span></span> | <span data-ttu-id="a9e98-140">Palabra clave que tiene como destino el primer div en la página.</span><span class="sxs-lookup"><span data-stu-id="a9e98-140">The keyword that targets the first div on the page.</span></span> <span data-ttu-id="a9e98-141">No use # como prefijo.</span><span class="sxs-lookup"><span data-stu-id="a9e98-141">Do not prefix with a #.</span></span> |  
| <span data-ttu-id="a9e98-142">title</span><span class="sxs-lookup"><span data-stu-id="a9e98-142">title</span></span> | <span data-ttu-id="a9e98-143">Palabra clave que tiene como destino el título de página.</span><span class="sxs-lookup"><span data-stu-id="a9e98-143">The keyword that targets the page title.</span></span> <span data-ttu-id="a9e98-144">No use # como prefijo.</span><span class="sxs-lookup"><span data-stu-id="a9e98-144">Do not prefix with a #.</span></span> |  
 
<span data-ttu-id="a9e98-145">**action**</span><span class="sxs-lookup"><span data-stu-id="a9e98-145">**action**</span></span>  
<span data-ttu-id="a9e98-146">Acción que se debe efectuar en el elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="a9e98-146">The action to perform on the target element. Possible values are: , , , , or .</span></span> <span data-ttu-id="a9e98-147">Vea [acciones admitidas para elementos](#supported-elements-and-actions).</span><span class="sxs-lookup"><span data-stu-id="a9e98-147">See [supported actions for elements](#supported-elements-and-actions).</span></span>

| <span data-ttu-id="a9e98-148">Acción</span><span class="sxs-lookup"><span data-stu-id="a9e98-148">Action</span></span> | <span data-ttu-id="a9e98-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9e98-149">Description</span></span> |  
|------|------|  
| <span data-ttu-id="a9e98-150">append</span><span class="sxs-lookup"><span data-stu-id="a9e98-150">Append</span></span> | <p><span data-ttu-id="a9e98-151">Agrega el contenido especificado al destino como primer o último elemento secundario, tal y como se determina en el atributo **position**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-151">**append**Adds the supplied content to the target as a first or last child, as determined by the position attribute.Applies only to body, div, ol, and ul elements.</span></span></p><p><span data-ttu-id="a9e98-152">Solo se aplica a los elementos **body**, **div**, **ol** y **ul**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-152">Applies only to **body**, **div**, **ol**, and **ul** elements.</span></span></p> |  
| <span data-ttu-id="a9e98-153">insert</span><span class="sxs-lookup"><span data-stu-id="a9e98-153">insert</span></span> | <span data-ttu-id="a9e98-154">Agrega el contenido especificado como elemento del mismo nivel antes o después del elemento de destino, tal y como se determina en el atributo **position**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-154">**insert**Adds the supplied content as a sibling before or after the target, as determined by the position attribute.</span></span> |  
| <span data-ttu-id="a9e98-155">prepend</span><span class="sxs-lookup"><span data-stu-id="a9e98-155">prepend</span></span> | <p><span data-ttu-id="a9e98-156">Agrega el contenido especificado al destino como primer elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="a9e98-156">Adds the supplied content to the target as a first child.</span></span> <span data-ttu-id="a9e98-157">Acceso directo a **append** + **before**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-157">Shortcut for **append** + **before**.</span></span></p><p><span data-ttu-id="a9e98-158">Solo se aplica a los elementos **body**, **div**, **ol** y **ul**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-158">Applies only to **body**, **div**, **ol**, and **ul** elements.</span></span></p> |  
| <span data-ttu-id="a9e98-159">replace</span><span class="sxs-lookup"><span data-stu-id="a9e98-159">replace</span></span> | <p><span data-ttu-id="a9e98-160">Reemplaza el destino por el contenido especificado.</span><span class="sxs-lookup"><span data-stu-id="a9e98-160">Replaces the target with the supplied content.</span></span></p><p><span data-ttu-id="a9e98-161">La mayoría de las acciones **replace** requieren el uso del [identificador generado](#generated-ids) para el elemento de destino (excepto **img** y **object** dentro de un div, que también admiten el uso de **data-id**).</span><span class="sxs-lookup"><span data-stu-id="a9e98-161">Most **replace** actions require using the [generated ID](#generated-ids) for the target (except **img** and **object** elements within a div, which also support using **data-id**).</span></span></p> |  
 
<span data-ttu-id="a9e98-162">**position**</span><span class="sxs-lookup"><span data-stu-id="a9e98-162">**position**</span></span>  
<span data-ttu-id="a9e98-163">Ubicación donde se debe agregar el contenido provisto, en relación con el elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="a9e98-163">The location to add the supplied content, relative to the target element. Possible values are:  (default) or .</span></span> <span data-ttu-id="a9e98-164">Si se omite, se establece de manera predeterminada en **after**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-164">Defaults to **render** if omitted.</span></span>

| <span data-ttu-id="a9e98-165">Posición</span><span class="sxs-lookup"><span data-stu-id="a9e98-165">Position</span></span> | <span data-ttu-id="a9e98-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9e98-166">Description</span></span> |  
|------|------|  
| <span data-ttu-id="a9e98-167">after (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="a9e98-167">after (default)</span></span> | <p><span data-ttu-id="a9e98-168">-Con **append**: último elemento secundario del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="a9e98-168">- With **append**: The last child of the target element.</span></span></p><p><span data-ttu-id="a9e98-169">- Con **insert**: siguiente elemento del mismo nivel del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="a9e98-169">**after** (default)- With append: The last child of the target element.- With insert: The subsequent sibling of the target element.</span></span></p> |
| <span data-ttu-id="a9e98-170">before</span><span class="sxs-lookup"><span data-stu-id="a9e98-170">Before</span></span> | <p><span data-ttu-id="a9e98-171">-Con **append**: primer elemento secundario del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="a9e98-171">- With **append**: The first child of the target element.</span></span></p><p><span data-ttu-id="a9e98-172">- Con **insert**: anterior elemento del mismo nivel del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="a9e98-172">**before**- With append: The first child of the target element.- With insert: The preceding sibling of the target element.</span></span></p> |

<span data-ttu-id="a9e98-173">**content**</span><span class="sxs-lookup"><span data-stu-id="a9e98-173">**content**</span></span>  
<span data-ttu-id="a9e98-174">Cadena de HTML sintácticamente correcta que se agrega a la página y datos binarios de cualquier imagen o archivo.</span><span class="sxs-lookup"><span data-stu-id="a9e98-174">A string of well-formed HTML to add to the page, and any image or file binary data. If the content contains binary data, the request must be sent using the  content type with a "Commands" part.</span></span> <span data-ttu-id="a9e98-175">Si el contenido contiene datos binarios, la solicitud debe enviarse utilizando el tipo de contenido `multipart/form-data` con una parte "Comandos" (véase un [ejemplo](#multipart-request-with-binary-content)).</span><span class="sxs-lookup"><span data-stu-id="a9e98-175">A string of well-formed HTML to add to the page and any image or file binary data. If the content contains binary data, the request must be sent using the multipart/form-data`multipart/form-data` content type with a "Commands" part (see an  [example](#multipart-request-with-binary-content)).</span></span> 
 

<a name="generated-ids"></a>

### <a name="generated-ids"></a><span data-ttu-id="a9e98-176">Identificadores generados</span><span class="sxs-lookup"><span data-stu-id="a9e98-176">Generated IDs</span></span>
<span data-ttu-id="a9e98-177">Microsoft Graph genera valores de **id** para los elementos de la página que pueden actualizarse.</span><span class="sxs-lookup"><span data-stu-id="a9e98-177">Microsoft Graph generates **id** values for the elements on the page that can be updated.</span></span> <span data-ttu-id="a9e98-178">Para obtener el identificador generado, use la expresión de cadena de consulta `includeIDs=true` en la solicitud GET:</span><span class="sxs-lookup"><span data-stu-id="a9e98-178">The onnvshort API generates id`includeIDs=true` values for page elements that can be updated. To get generated IDs, use the includeIDs=true query string expression in your GET request:</span></span>

`GET ../notes/pages/{page-id}/content?includeIDs=true` 

> <span data-ttu-id="a9e98-179">**Nota:** La API descarta todos los valores de **id** definidos en el [HTML de entrada](onenote_input_output_html.md) de las solicitudes create-page y update-page.</span><span class="sxs-lookup"><span data-stu-id="a9e98-179">**Note:** The API discards all **id** values that are defined in the [input HTML](onenote_input_output_html.md) of create-page and update-page requests.</span></span>

<span data-ttu-id="a9e98-180">En el siguiente ejemplo se muestran los identificadores generados para un párrafo y una imagen en el [HTML de salida](onenote_input_output_html.md) de una página.</span><span class="sxs-lookup"><span data-stu-id="a9e98-180">The following example shows generated IDs for a paragraph and an image in the [output HTML](onenote_input_output_html.md) of a page.</span></span>

```html
<p id="p:{33f8a242-7c33-4bb2-90c5-8425a68cc5bf}{40}">Some text on the page</p>
<img id="img:{33f8a242-7c33-4bb2-90c5-8425a68cc5bf}{45}" ... />
```

<span data-ttu-id="a9e98-181">Los valores de **id** generados pueden cambiar después de la actualización de una página, por lo tanto debe obtener los valores actuales antes de crear una solicitud de PATCH que los utilice.</span><span class="sxs-lookup"><span data-stu-id="a9e98-181">Generated **id** values might change after a page update, so you should get the current values before building a PATCH request that uses them.</span></span>
 
<span data-ttu-id="a9e98-182">Puede especificar los elementos de destino con el valor de **data-id** o de **id**, de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="a9e98-182">You can specify target elements by using the **data-id** or **id** value, as follows:</span></span>

- <span data-ttu-id="a9e98-183">Para las acciones **append** y **insert**, puede usar cualquier identificador como valor de destino.</span><span class="sxs-lookup"><span data-stu-id="a9e98-183">For **append** and **insert** actions, you can use either ID as the target value.</span></span>
- <span data-ttu-id="a9e98-184">Para las acciones **replace**, debe usar el identificador generado para todos los elementos excepto el título de página y las imágenes y los objetos que se encuentran dentro de un div.</span><span class="sxs-lookup"><span data-stu-id="a9e98-184">For **replace** actions, you must use the generated ID for all elements except for the page title and images and objects that are within a div. To replace a title, use the title keyword. To replace images and objects that are within a div, use either data-id or id.</span></span> 
    - <span data-ttu-id="a9e98-185">Para reemplazar un título, utilice la palabra clave **title**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-185">To replace a title, use the **title** keyword.</span></span> 
    - <span data-ttu-id="a9e98-186">Para reemplazar imágenes y objetos que se encuentran en un div, utilice **data-id** o **id**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-186">To replace images and objects that are within a div, use either **data-id** or **id**.</span></span>

<span data-ttu-id="a9e98-187">En el siguiente ejemplo se usa el valor de **id** como destino.</span><span class="sxs-lookup"><span data-stu-id="a9e98-187">The following example uses the **id** value for the target . Don't use the # prefix with a generated ID.</span></span> <span data-ttu-id="a9e98-188">No use el prefijo # con un identificador generado.</span><span class="sxs-lookup"><span data-stu-id="a9e98-188">The following example uses the id value for the target . Don't use the # prefix with a generated ID.</span></span>

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

## <a name="supported-elements-and-actions"></a><span data-ttu-id="a9e98-189">Acciones y elementos admitidos</span><span class="sxs-lookup"><span data-stu-id="a9e98-189">Supported elements and actions</span></span>
<span data-ttu-id="a9e98-190">Se pueden actualizar muchos elementos de la página, pero cada tipo de elemento admite acciones específicas.</span><span class="sxs-lookup"><span data-stu-id="a9e98-190">Many elements on  the page can be updated, but each element type supports specific actions. The following table shows supported target elements and the update actions that they support.</span></span> <span data-ttu-id="a9e98-191">En la siguiente tabla se muestran los elementos de destino admitidos y las acciones de actualización que admiten.</span><span class="sxs-lookup"><span data-stu-id="a9e98-191">Many elements on  the page can be updated, but each element type supports specific actions. The following table shows supported target elements and the update actions that they support.</span></span>

| <span data-ttu-id="a9e98-192">Elemento</span><span class="sxs-lookup"><span data-stu-id="a9e98-192">Element</span></span> | <span data-ttu-id="a9e98-193">Reemplazar</span><span class="sxs-lookup"><span data-stu-id="a9e98-193">Replace</span></span> | <span data-ttu-id="a9e98-194">Anexar elemento secundario</span><span class="sxs-lookup"><span data-stu-id="a9e98-194">Append child</span></span> | <span data-ttu-id="a9e98-195">Insertar elemento del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="a9e98-195">Insert sibling</span></span> |  
|------|------|------|------|  
| <span data-ttu-id="a9e98-196">body</span><span class="sxs-lookup"><span data-stu-id="a9e98-196">body</span></span><br /> <span data-ttu-id="a9e98-197">(tiene como destino el primer div en la página)</span><span class="sxs-lookup"><span data-stu-id="a9e98-197">body(targets first div on the page)</span></span> | <span data-ttu-id="a9e98-198">no</span><span class="sxs-lookup"><span data-stu-id="a9e98-198">no</span></span> | <span data-ttu-id="a9e98-199">**sí**</span><span class="sxs-lookup"><span data-stu-id="a9e98-199">**yes**</span></span> | <span data-ttu-id="a9e98-200">no</span><span class="sxs-lookup"><span data-stu-id="a9e98-200">no</span></span> |  
| <span data-ttu-id="a9e98-201">div</span><span class="sxs-lookup"><span data-stu-id="a9e98-201">div</span></span><br /> <span data-ttu-id="a9e98-202">([posición absoluta](onenote-abs-pos.md))</span><span class="sxs-lookup"><span data-stu-id="a9e98-202">([absolute positioned](onenote-abs-pos.md))</span></span> | <span data-ttu-id="a9e98-203">no</span><span class="sxs-lookup"><span data-stu-id="a9e98-203">no</span></span> | <span data-ttu-id="a9e98-204">**sí**</span><span class="sxs-lookup"><span data-stu-id="a9e98-204">**yes**</span></span> | <span data-ttu-id="a9e98-205">no</span><span class="sxs-lookup"><span data-stu-id="a9e98-205">no</span></span> |  
| <span data-ttu-id="a9e98-206">div</span><span class="sxs-lookup"><span data-stu-id="a9e98-206">div</span></span><br /> <span data-ttu-id="a9e98-207">(en un elemento div)</span><span class="sxs-lookup"><span data-stu-id="a9e98-207">(within a div)</span></span> | <span data-ttu-id="a9e98-208">**sí** (solo identificador)</span><span class="sxs-lookup"><span data-stu-id="a9e98-208">**yes** (id only)</span></span> | <span data-ttu-id="a9e98-209">**sí**</span><span class="sxs-lookup"><span data-stu-id="a9e98-209">**Yes**</span></span> | <span data-ttu-id="a9e98-210">**sí**</span><span class="sxs-lookup"><span data-stu-id="a9e98-210">**Yes**</span></span> |   
| <span data-ttu-id="a9e98-211">img, object</span><span class="sxs-lookup"><span data-stu-id="a9e98-211">img, object</span></span><br /> <span data-ttu-id="a9e98-212">(en un elemento div)</span><span class="sxs-lookup"><span data-stu-id="a9e98-212">(within a div)</span></span> | <span data-ttu-id="a9e98-213">**sí**</span><span class="sxs-lookup"><span data-stu-id="a9e98-213">**yes**</span></span> | <span data-ttu-id="a9e98-214">no</span><span class="sxs-lookup"><span data-stu-id="a9e98-214">no</span></span> | <span data-ttu-id="a9e98-215">**sí**</span><span class="sxs-lookup"><span data-stu-id="a9e98-215">**yes**</span></span> |   
| <span data-ttu-id="a9e98-216">ol, ul</span><span class="sxs-lookup"><span data-stu-id="a9e98-216">ol, ul</span></span> | <span data-ttu-id="a9e98-217">**sí** (solo identificador)</span><span class="sxs-lookup"><span data-stu-id="a9e98-217">**yes** (id only)</span></span> | <span data-ttu-id="a9e98-218">**sí**</span><span class="sxs-lookup"><span data-stu-id="a9e98-218">**Yes**</span></span> | <span data-ttu-id="a9e98-219">**sí**</span><span class="sxs-lookup"><span data-stu-id="a9e98-219">**yes**</span></span> |   
| <span data-ttu-id="a9e98-220">table</span><span class="sxs-lookup"><span data-stu-id="a9e98-220">table</span></span> | <span data-ttu-id="a9e98-221">**sí** (solo identificador)</span><span class="sxs-lookup"><span data-stu-id="a9e98-221">**yes** (id only)</span></span> | <span data-ttu-id="a9e98-222">no</span><span class="sxs-lookup"><span data-stu-id="a9e98-222">no</span></span> | <span data-ttu-id="a9e98-223">**sí**</span><span class="sxs-lookup"><span data-stu-id="a9e98-223">**yes**</span></span> |   
| <span data-ttu-id="a9e98-224">p, li, h1-h6</span><span class="sxs-lookup"><span data-stu-id="a9e98-224">p, li, h1-h6</span></span> | <span data-ttu-id="a9e98-225">**sí** (solo identificador)</span><span class="sxs-lookup"><span data-stu-id="a9e98-225">**yes** (id only)</span></span> | <span data-ttu-id="a9e98-226">no</span><span class="sxs-lookup"><span data-stu-id="a9e98-226">no</span></span> | <span data-ttu-id="a9e98-227">**sí**</span><span class="sxs-lookup"><span data-stu-id="a9e98-227">**yes**</span></span> |   
| <span data-ttu-id="a9e98-228">title</span><span class="sxs-lookup"><span data-stu-id="a9e98-228">title</span></span> | <span data-ttu-id="a9e98-229">**sí**</span><span class="sxs-lookup"><span data-stu-id="a9e98-229">**yes**</span></span> | <span data-ttu-id="a9e98-230">no</span><span class="sxs-lookup"><span data-stu-id="a9e98-230">no</span></span> | <span data-ttu-id="a9e98-231">no</span><span class="sxs-lookup"><span data-stu-id="a9e98-231">no</span></span> |  
 

<span data-ttu-id="a9e98-232">Los siguientes elementos no admiten ninguna acción de actualización.</span><span class="sxs-lookup"><span data-stu-id="a9e98-232">The following elements do not support any update actions.</span></span>

- <span data-ttu-id="a9e98-233">img ([posición absoluta](onenote-abs-pos.md))</span><span class="sxs-lookup"><span data-stu-id="a9e98-233">img ([absolute positioned](onenote-abs-pos.md))</span></span>
- <span data-ttu-id="a9e98-234">object ([posición absoluta](onenote-abs-pos.md))</span><span class="sxs-lookup"><span data-stu-id="a9e98-234">object ([absolute positioned](onenote-abs-pos.md))</span></span>
- <span data-ttu-id="a9e98-235">tr, td</span><span class="sxs-lookup"><span data-stu-id="a9e98-235">tr, td</span></span>
- <span data-ttu-id="a9e98-236">meta</span><span class="sxs-lookup"><span data-stu-id="a9e98-236">meta</span></span>
- <span data-ttu-id="a9e98-237">head</span><span class="sxs-lookup"><span data-stu-id="a9e98-237">head</span></span>
- <span data-ttu-id="a9e98-238">span</span><span class="sxs-lookup"><span data-stu-id="a9e98-238">span</span></span>
- <span data-ttu-id="a9e98-239">a</span><span class="sxs-lookup"><span data-stu-id="a9e98-239">a</span></span>
- <span data-ttu-id="a9e98-240">etiquetas de estilo</span><span class="sxs-lookup"><span data-stu-id="a9e98-240">style tags</span></span>


<a name="examples"></a>
## <a name="example-requests"></a><span data-ttu-id="a9e98-241">Solicitudes de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a9e98-241">Example requests</span></span>
<span data-ttu-id="a9e98-242">Una solicitud de actualización contiene uno o más cambios que se representan como objetos de cambio JSON.</span><span class="sxs-lookup"><span data-stu-id="a9e98-242">An update request contains one or more changes represented as JSON change objects.</span></span> <span data-ttu-id="a9e98-243">Estos objetos pueden definir diferentes destinos en la página y diferentes acciones y contenido para los destinos.</span><span class="sxs-lookup"><span data-stu-id="a9e98-243">An update request contains one or more changes represented as JSON objects. These objects can define different targets on the page and different actions and content for the targets.</span></span>

<span data-ttu-id="a9e98-244">En los siguientes ejemplos se incluyen objetos JSON usados en solicitudes PATCH y solicitudes PATCH completas:</span><span class="sxs-lookup"><span data-stu-id="a9e98-244">The following examples include JSON objects used in PATCH requests and complete PATCH requests:</span></span>

<span data-ttu-id="a9e98-245">[Anexar elementos secundarios](#append-child-elements)&nbsp;&nbsp;|&nbsp;&nbsp;[Insertar elementos del mismo nivel](#insert-sibling-elements)&nbsp;&nbsp;|&nbsp;&nbsp;[Reemplazar elementos](#replace-elements)&nbsp;&nbsp;|&nbsp;&nbsp;[Completar solicitudes PATCH](#complete-patch-request-examples)</span><span class="sxs-lookup"><span data-stu-id="a9e98-245">[Append child elements](#append-child-elements)&nbsp;&nbsp;|&nbsp;&nbsp;[Insert sibling elements](#insert-sibling-elements)&nbsp;&nbsp;|&nbsp;&nbsp;[Replace elements](#replace-elements)&nbsp;&nbsp;|&nbsp;&nbsp;[Complete PATCH requests](#complete-patch-request-examples)</span></span>


<a name="append-examples"></a>

### <a name="append-child-elements"></a><span data-ttu-id="a9e98-246">Anexar elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a9e98-246">Append child elements</span></span>
<span data-ttu-id="a9e98-247">La acción **append** agrega un elemento secundario a un elemento **body**, **div** (dentro de un div), **ol** o **ul**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-247">The **append** action adds a child to a **body**, **div** (within a div), **ol**, or **ul** element. The position attribute determines whether to append the child before or after the target. The default position is after.</span></span> <span data-ttu-id="a9e98-248">El atributo **position** determina si el elemento secundario se va a anexar antes o después del destino.</span><span class="sxs-lookup"><span data-stu-id="a9e98-248">The **position** attribute determines whether to append the child before or after the target.</span></span> <span data-ttu-id="a9e98-249">La posición predeterminada es **after**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-249">The default position is **after**.</span></span>

#### <a name="append-to-a-div"></a><span data-ttu-id="a9e98-250">Anexar a un div</span><span class="sxs-lookup"><span data-stu-id="a9e98-250">Append to a  div</span></span>

<span data-ttu-id="a9e98-251">En el ejemplo siguiente se agregan dos nodos secundarios al elemento **div1**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-251">The following example adds two child nodes  to the **div1** element. It adds an image as the first child and a paragraph as the last child.</span></span> <span data-ttu-id="a9e98-252">Agrega una imagen como primer elemento secundario y un párrafo como último elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="a9e98-252">The following example adds two child nodes  to the div1 element. It adds an image as the first child and a paragraph as the last child.</span></span> 

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
 

#### <a name="append-to-the-body-element"></a><span data-ttu-id="a9e98-253">Anexar al elemento *body*</span><span class="sxs-lookup"><span data-stu-id="a9e98-253">Append to the body element</span></span>

<span data-ttu-id="a9e98-254">Puede usar el acceso directo **body** para anexar un elemento secundario en el interior del primer div de cualquier página.</span><span class="sxs-lookup"><span data-stu-id="a9e98-254">You can use the body target as a shortcut to append a child element inside the first div on any page.</span></span>

<span data-ttu-id="a9e98-255">En el siguiente ejemplo se agregan dos párrafos como primer elemento secundario y último elemento secundario en el primer div de la página.</span><span class="sxs-lookup"><span data-stu-id="a9e98-255">The following example adds two paragraphs as the first child and the last child to the first div on the page. Don't use a # with the body target. This example uses the prepend shortcut for append + before.</span></span> <span data-ttu-id="a9e98-256">No use # con el destino **body**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-256">Don't use a # with the **body** target.</span></span> <span data-ttu-id="a9e98-257">En este ejemplo se usa la acción **prepend** como acceso directo a **append** + **before**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-257">This example uses the **prepend** action as a shortcut for **append** + **before**.</span></span>

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
 

#### <a name="append-to-a-list"></a><span data-ttu-id="a9e98-258">Anexar a una lista</span><span class="sxs-lookup"><span data-stu-id="a9e98-258">Append to a  div</span></span>

<span data-ttu-id="a9e98-259">En el ejemplo siguiente se agrega un elemento de lista como último elemento secundario a la lista de destino.</span><span class="sxs-lookup"><span data-stu-id="a9e98-259">The following example adds a list item as a last child to the target list. The list-style-type property is defined because the item uses a non-default list style.</span></span> <span data-ttu-id="a9e98-260">Se define la propiedad **list-style-type** porque el elemento usa un estilo de lista no predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a9e98-260">The following example adds a list item as a last child to the target list. The **list-style-type** property is defined because the item uses a non-default list style.</span></span>

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

### <a name="insert-sibling-elements"></a><span data-ttu-id="a9e98-261">Insertar elementos del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="a9e98-261">Insert sibling elements</span></span>
<span data-ttu-id="a9e98-262">La acción **insert** agrega un elemento del mismo nivel al elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="a9e98-262">The **insert** action adds a sibling to the target element.</span></span> <span data-ttu-id="a9e98-263">El atributo **position** determina si el elemento del mismo nivel se va a insertar antes o después del destino.</span><span class="sxs-lookup"><span data-stu-id="a9e98-263">The **position** attribute determines whether to insert the sibling before or after the target.</span></span> <span data-ttu-id="a9e98-264">La posición predeterminada es **after**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-264">The default position is **after**.</span></span> <span data-ttu-id="a9e98-265">Vea [elementos que admiten **insert**](#supported-elements-and-actions).</span><span class="sxs-lookup"><span data-stu-id="a9e98-265">See [elements that support **insert**](#supported-elements-and-actions).</span></span>

<span data-ttu-id="a9e98-266">**Insertar elementos del mismo nivel**</span><span class="sxs-lookup"><span data-stu-id="a9e98-266">**Insert siblings**</span></span>

<span data-ttu-id="a9e98-267">En el ejemplo siguiente se agregan dos nodos del mismo nivel a la página.</span><span class="sxs-lookup"><span data-stu-id="a9e98-267">The following example adds two sibling nodes to the page.</span></span> <span data-ttu-id="a9e98-268">Agrega una imagen por encima del elemento **para1** y un párrafo por debajo del elemento **para2**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-268">The following example adds two sibling nodes to the page. It adds an image above the **para1** element and a paragraph below the **para2** element.</span></span>

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

### <a name="replace-elements"></a><span data-ttu-id="a9e98-269">Reemplazar elementos</span><span class="sxs-lookup"><span data-stu-id="a9e98-269">Replace elements</span></span>

<span data-ttu-id="a9e98-270">Puede utilizar el **data-id** o el **id** generado como valor de destino para reemplazar los elementos **img** y **object** que están dentro de un div.</span><span class="sxs-lookup"><span data-stu-id="a9e98-270">You can use either the **data-id** or generated **id** as the target value to replace **img** and **object** elements that are within a div. To replace the page title, use the title keyword. For all other elements that support replace, you must use the generated ID.</span></span> <span data-ttu-id="a9e98-271">Para reemplazar el título de página, utilice la palabra clave **title**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-271">To replace the page title, use the **title** keyword.</span></span> <span data-ttu-id="a9e98-272">Para todos los demás [elementos que admiten **replace**](#supported-elements-and-actions), debe usar el identificador generado.</span><span class="sxs-lookup"><span data-stu-id="a9e98-272">For all other [elements that support **replace**](#supported-elements-and-actions), you must use the generated ID.</span></span>

#### <a name="replace-an-image"></a><span data-ttu-id="a9e98-273">Reemplazar una imagen</span><span class="sxs-lookup"><span data-stu-id="a9e98-273">Replace an image</span></span>

<span data-ttu-id="a9e98-274">En este ejemplo se reemplaza una imagen por un div mediante el **data-id** de la imagen como destino</span><span class="sxs-lookup"><span data-stu-id="a9e98-274">The following example replaces an image with a div by using the image's **data-id** as the target.</span></span> 

```json
[
  {
    'target':'#img1',
    'action':'replace',
    'content':'<div data-id="new-div"><p>This div replaces the image</p></div>'
  }
]
```
 

#### <a name="update-a-table"></a><span data-ttu-id="a9e98-275">Actualizar una tabla</span><span class="sxs-lookup"><span data-stu-id="a9e98-275">Update a table</span></span> 

<span data-ttu-id="a9e98-276">En este ejemplo se muestra cómo actualizar una tabla mediante su identificador generado.</span><span class="sxs-lookup"><span data-stu-id="a9e98-276">This example shows how to update a table by using its generated ID. Replacing tr and td elements is not supported, but you can replace the entire table.</span></span> <span data-ttu-id="a9e98-277">No se admite el reemplazo de los elementos **tr** y **td**, pero puede reemplazarse toda la tabla.</span><span class="sxs-lookup"><span data-stu-id="a9e98-277">This example shows how to update a table by using its generated ID. Replacing **tr** and **td** elements is not supported, but you can replace the entire table.</span></span>

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
 

#### <a name="change-the-title"></a><span data-ttu-id="a9e98-278">Cambiar el título</span><span class="sxs-lookup"><span data-stu-id="a9e98-278">Change the title</span></span> 

<span data-ttu-id="a9e98-279">En este ejemplo se muestra cómo cambiar el título de la página.</span><span class="sxs-lookup"><span data-stu-id="a9e98-279">This example shows how to change the title of a page.</span></span> <span data-ttu-id="a9e98-280">Para cambiar el título, use la palabra clave **title** como valor de destino.</span><span class="sxs-lookup"><span data-stu-id="a9e98-280">To change the title, use the **title** keyword as the target value.</span></span> <span data-ttu-id="a9e98-281">No use el prefijo # con el destino title.</span><span class="sxs-lookup"><span data-stu-id="a9e98-281">Don't use a # with the title target.</span></span>

```json
[
  {
    'target':'title',
    'action':'replace',
    'content':'New title'
  }
]
```
 

#### <a name="update-a-to-do-item"></a><span data-ttu-id="a9e98-282">Actualizar una tarea pendiente</span><span class="sxs-lookup"><span data-stu-id="a9e98-282">Assign a to-do item</span></span>

<span data-ttu-id="a9e98-283">En el siguiente ejemplo se usa la acción replace para cambiar un elemento de casilla de tarea pendiente a un estado completado.</span><span class="sxs-lookup"><span data-stu-id="a9e98-283">The following example uses the replace action to change a to-do check box item to a completed state.</span></span>

```json
[
  {
    'target':'#task1',
    'action':'replace',
    'content':'<p data-tag="to-do:completed" data-id="task1">First task</p>'
  }
]
```

<span data-ttu-id="a9e98-284">Vea [Uso de etiquetas de nota](onenote-note-tags.md) para más información sobre el uso del atributo **data-tag**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-284">See [Use note tags](onenote-note-tags.md) for more about using the **data-tag** attribute.</span></span>


<a name="complete-requests"></a>

### <a name="complete-patch-request-examples"></a><span data-ttu-id="a9e98-285">Ejemplos de solicitud PATCH completa</span><span class="sxs-lookup"><span data-stu-id="a9e98-285">Complete PATCH request examples</span></span>

<span data-ttu-id="a9e98-286">En los ejemplos siguientes se muestran solicitudes PATCH completas.</span><span class="sxs-lookup"><span data-stu-id="a9e98-286">The following examples show complete PATCH requests.</span></span>

#### <a name="request-with-text-content-only"></a><span data-ttu-id="a9e98-287">Solicitud con solo contenido de texto</span><span class="sxs-lookup"><span data-stu-id="a9e98-287">Request with text content only</span></span>  
<span data-ttu-id="a9e98-288">En el siguiente ejemplo se muestra una solicitud PATCH que utiliza el tipo de contenido **application/json**.</span><span class="sxs-lookup"><span data-stu-id="a9e98-288">The following example shows a PATCH request that uses the   **application/json** content type. You can use this format when your content doesn't contain binary data.</span></span> <span data-ttu-id="a9e98-289">Puede usar este formato cuando el contenido no contiene datos binarios.</span><span class="sxs-lookup"><span data-stu-id="a9e98-289">The following example shows a PATCH request that uses the   application/json content type. You can use this format when your content doesn't contain binary data.</span></span>

```
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

#### <a name="multipart-request-with-binary-content"></a><span data-ttu-id="a9e98-290">Solicitud de varias partes con contenido binario</span><span class="sxs-lookup"><span data-stu-id="a9e98-290">Multipart request with binary content</span></span> 

<span data-ttu-id="a9e98-291">En el ejemplo siguiente se muestra una solicitud PATCH de varias partes que incluye datos binarios.</span><span class="sxs-lookup"><span data-stu-id="a9e98-291">The following example shows a multipart PATCH request that includes binary data.</span></span> <span data-ttu-id="a9e98-292">Las solicitudes de varias partes requieren una parte "Comandos" que especifica el tipo de contenido **application/json** y contiene la matriz de objetos de cambio JSON.</span><span class="sxs-lookup"><span data-stu-id="a9e98-292">Multipart requests require a "Commands" part that specifies the **application/json** content type and contains the array of JSON change objects.</span></span> <span data-ttu-id="a9e98-293">Otras partes de datos pueden contener datos binarios.</span><span class="sxs-lookup"><span data-stu-id="a9e98-293">Other data parts can contain binary data.</span></span> <span data-ttu-id="a9e98-294">Los nombres de parte suelen ser cadenas anexadas con la hora actual en milisegundos o un GUID aleatorio.</span><span class="sxs-lookup"><span data-stu-id="a9e98-294">Part names typically are strings appended with the current time in milliseconds or a random GUID.</span></span>

```
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

## <a name="request-and-response-information-for-patch-requests"></a><span data-ttu-id="a9e98-295">Información de solicitud y respuesta de las solicitudes PATCH</span><span class="sxs-lookup"><span data-stu-id="a9e98-295">Request and response information for PATCH requests</span></span>

| <span data-ttu-id="a9e98-296">Datos de solicitud</span><span class="sxs-lookup"><span data-stu-id="a9e98-296">Request data</span></span> | <span data-ttu-id="a9e98-297">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9e98-297">Description</span></span> |  
|------|------|  
| <span data-ttu-id="a9e98-298">Protocolo</span><span class="sxs-lookup"><span data-stu-id="a9e98-298">Protocol</span></span> | <span data-ttu-id="a9e98-299">Todas las solicitudes usan el protocolo HTTPS SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="a9e98-299">All requests use the SSL/TLS HTTPS protocol.</span></span> |  
| <span data-ttu-id="a9e98-300">Encabezado Authorization</span><span class="sxs-lookup"><span data-stu-id="a9e98-300">Authorization header</span></span> | <p><span data-ttu-id="a9e98-301">`Bearer {token}`, donde *{token}* es un token de acceso de OAuth 2.0 válido para la aplicación registrada.</span><span class="sxs-lookup"><span data-stu-id="a9e98-301">`Bearer {token}`, where *{token}* is a valid OAuth 2.0 access token for your registered app.</span></span></p><p><span data-ttu-id="a9e98-302">Si falta o no es válido, se produce un error en la solicitud con un código de estado 401.</span><span class="sxs-lookup"><span data-stu-id="a9e98-302">If missing or invalid, the request fails with a 401 status code.</span></span> <span data-ttu-id="a9e98-303">Vea [Authentication and permissions](permissions_reference.md) (Autenticación y permisos).</span><span class="sxs-lookup"><span data-stu-id="a9e98-303">See [Authentication and permissions](permissions_reference.md).</span></span></p> |  
| <span data-ttu-id="a9e98-304">Encabezado Content-Type</span><span class="sxs-lookup"><span data-stu-id="a9e98-304">content-type header</span></span> | <p><span data-ttu-id="a9e98-305">`application/json` para la matriz de objetos de cambio JSON, tanto si se envía directamente en el cuerpo del mensaje como si se envía en la parte "Comandos" necesaria de las [solicitudes de varias partes](#multipart-request-with-binary-content).</span><span class="sxs-lookup"><span data-stu-id="a9e98-305">`application/json` for the array of JSON change objects, whether sent directly in the message body or in the required "Commands" part of [multipart requests](#multipart-request-with-binary-content).</span></span></p><p><span data-ttu-id="a9e98-306">Se necesitan solicitudes de varias partes cuando se envían datos binarios y se utiliza el tipo de contenido `multipart/form-data; boundary=part-boundary`, donde *{part-boundary}* es una cadena que señala el inicio y el final de cada parte de datos.</span><span class="sxs-lookup"><span data-stu-id="a9e98-306">Multipart requests are required when sending binary data, and use the `multipart/form-data; boundary=part-boundary` content type, where *{part-boundary}* is a string that signals the start and end of each data part.</span></span></p> |  
 

| <span data-ttu-id="a9e98-307">Datos de respuesta</span><span class="sxs-lookup"><span data-stu-id="a9e98-307">Response data</span></span> | <span data-ttu-id="a9e98-308">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9e98-308">Description</span></span> |  
|------|------|  
| <span data-ttu-id="a9e98-309">Errores</span><span class="sxs-lookup"><span data-stu-id="a9e98-309">Success code</span></span> | <span data-ttu-id="a9e98-p131">Si la solicitud de actualización falla, la API devuelve errores en el objeto api.diagnostics en el cuerpo de la respuesta. La solicitud fallará si:</span><span class="sxs-lookup"><span data-stu-id="a9e98-p131">A 204 HTTP status code. No JSON data is returned for a PATCH request.</span></span> |  
| <span data-ttu-id="a9e98-312">Errores</span><span class="sxs-lookup"><span data-stu-id="a9e98-312">Errors</span></span> | <span data-ttu-id="a9e98-313">Lea [Códigos de error para API de OneNote de Microsoft Graph](onenote_error_codes.md) para obtener información sobre los errores de OneNote que puede devolver Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="a9e98-313">Read [Error codes for OneNote APIs in Microsoft Graph](onenote_error_codes.md) to learn about OneNote errors that Microsoft Graph can return.</span></span> |  
 
 

<a name="root-url"></a>

### <a name="constructing-the-microsoft-graph-service-root-url"></a><span data-ttu-id="a9e98-314">Crear la dirección URL raíz del servicio de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="a9e98-314">Constructing the Microsoft Graph service root URL</span></span>

<a name="root-url"></a>

## <a name="root-url"></a><span data-ttu-id="a9e98-315">Dirección URL raíz</span><span class="sxs-lookup"><span data-stu-id="a9e98-315">URL Root</span></span>
<span data-ttu-id="a9e98-316">La dirección URL raíz del servicio OneNote utiliza el siguiente formato para todas las llamadas a la API de OneNote.</span><span class="sxs-lookup"><span data-stu-id="a9e98-316">The OneNote service root URL uses the following format for all calls to the OneNote API.</span></span>
`https://graph.microsoft.com/{version}/me/onenote/`

<span data-ttu-id="a9e98-317">El segmento `version` de la URL representa la versión de Microsoft Graph que se quiere utilizar.</span><span class="sxs-lookup"><span data-stu-id="a9e98-317">The `version` segment in the URL represents the version of Microsoft Graph that you want to use.</span></span>
- <span data-ttu-id="a9e98-318">`v1.0` corresponde al código de producción estable.</span><span class="sxs-lookup"><span data-stu-id="a9e98-318">`v1.0` is for stable production code.</span></span>
- <span data-ttu-id="a9e98-319">`beta` corresponde a la prueba de una característica que se encuentra en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="a9e98-319">`beta` is to try out a feature that's in development.</span></span> <span data-ttu-id="a9e98-320">Las características y la funcionalidad de la versión beta pueden cambiar, por lo que no se debe usar en el código de producción.</span><span class="sxs-lookup"><span data-stu-id="a9e98-320">Features and functionality in beta may change, so you shouldn't use it in your production code.</span></span>
- <span data-ttu-id="a9e98-321">`me` corresponde a contenido de OneNote al que el usuario actual tiene acceso (de su propiedad y compartido).</span><span class="sxs-lookup"><span data-stu-id="a9e98-321">`me` is for OneNote content that the current user can access (owned and shared).</span></span>
- <span data-ttu-id="a9e98-322">`users/{id}` corresponde a contenido de OneNote que el usuario especificado (en la dirección URL) ha compartido con el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="a9e98-322">`users/{id}` is for OneNote content that the specified user (in the URL) has shared with the current user.</span></span> <span data-ttu-id="a9e98-323">Use la [API de Azure AD Graph](https://msdn.microsoft.com/library/azure/ad/graph/api/api-catalog).</span><span class="sxs-lookup"><span data-stu-id="a9e98-323">Use the [Azure AD Graph API](https://msdn.microsoft.com/library/azure/ad/graph/api/api-catalog)</span></span>


> <span data-ttu-id="a9e98-324">**Nota:** Puede obtener identificadores de usuario realizando una solicitud GET en `https://graph.microsoft.com/v1.0/users`.</span><span class="sxs-lookup"><span data-stu-id="a9e98-324">**Note:** You can get user ids by making a GET request on `https://graph.microsoft.com/v1.0/users`.</span></span>



<a name="permissions"></a>

## <a name="permissions"></a><span data-ttu-id="a9e98-325">Permisos</span><span class="sxs-lookup"><span data-stu-id="a9e98-325">Permissions</span></span>

<span data-ttu-id="a9e98-326">Para actualizar páginas OneNote, tiene que solicitar los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="a9e98-326">To update OneNote pages, you'll need to request appropriate permissions.</span></span> <span data-ttu-id="a9e98-327">Elija el nivel más bajo de permisos que necesita la aplicación para hacer su trabajo.</span><span class="sxs-lookup"><span data-stu-id="a9e98-327">Choose the lowest level of permissions that your app needs to do its work.</span></span>

- <span data-ttu-id="a9e98-328">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a9e98-328">Notes.ReadWrite</span></span>
- <span data-ttu-id="a9e98-329">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a9e98-329">Notes.ReadWrite.All</span></span>

<span data-ttu-id="a9e98-330">Para obtener más información sobre los ámbitos de permiso y cómo funcionan, consulte los [ámbitos de permisos de OneNote](permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a9e98-330">For more information about how permission scopes work, see [OneNote permission scopes](permissions_reference.md).</span></span>
   

<a name="see-also"></a>

## <a name="additional-resources"></a><span data-ttu-id="a9e98-331">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a9e98-331">Additional resources</span></span>

- [<span data-ttu-id="a9e98-332">Agregar imágenes y archivos</span><span class="sxs-lookup"><span data-stu-id="a9e98-332">Add images and files</span></span>](onenote_images_files.md)
- [<span data-ttu-id="a9e98-333">Integración con OneNote</span><span class="sxs-lookup"><span data-stu-id="a9e98-333">Integrate with OneNote</span></span>](integrate_with_onenote.md)
- [<span data-ttu-id="a9e98-334">Blog para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="a9e98-334">OneNote Developer Blog</span></span>](http://go.microsoft.com/fwlink/?LinkID=390183)
- [<span data-ttu-id="a9e98-335">Preguntas de desarrollo de OneNote en Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="a9e98-335">OneNote development questions on Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkID=390182)
- [<span data-ttu-id="a9e98-336">Repositorios de OneNote en GitHub</span><span class="sxs-lookup"><span data-stu-id="a9e98-336">OneNote GitHub repos</span></span>](http://go.microsoft.com/fwlink/?LinkID=390178)  
