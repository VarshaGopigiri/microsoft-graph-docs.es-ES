---
title: Actualizar el contenido de la página de OneNote
description: " Blocs de notas de empresa en Office 365"
author: jewan-microsoft
localization_priority: Normal
ms.prod: onenote
ms.openlocfilehash: 97a9acb8244446191b09d99753e30d94c47c4f1e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981472"
---
# <a name="update-onenote-page-content"></a><span data-ttu-id="2a397-103">Actualizar el contenido de la página de OneNote</span><span class="sxs-lookup"><span data-stu-id="2a397-103">Update OneNote page content</span></span>

<span data-ttu-id="2a397-104">**Se aplica a:** Blocs de notas para consumidores de OneDrive | Blocs de notas empresariales de Office 365</span><span class="sxs-lookup"><span data-stu-id="2a397-104">**Applies to** Consumer notebooks on OneDrive | Enterprise notebooks on Office 365</span></span>


<span data-ttu-id="2a397-105">Para actualizar el contenido de una página de OneNote, envíe una solicitud PATCH al punto de conexión *content* de la página.</span><span class="sxs-lookup"><span data-stu-id="2a397-105">To update the content of a OneNote page, you send a PATCH request to the page's *content* endpoint:</span></span>

`PATCH ../notes/pages/{id}/content`</p>

<span data-ttu-id="2a397-p101">Envíe un objeto de cambio JSON en el cuerpo del mensaje. Si la solicitud es correcta, Microsoft Graph devuelve un código de estado 204 HTTP.</span><span class="sxs-lookup"><span data-stu-id="2a397-p101">Send a JSON change object in the message body. If the request is successful, Microsoft Graph returns a 204 HTTP status code.</span></span>


<a name="request-uri"></a>

## <a name="construct-the-request-uri"></a><span data-ttu-id="2a397-108">Crear el URI de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2a397-108">Construct the request URI</span></span>

<span data-ttu-id="2a397-109">Para crear el URI de la solicitud, comience con la dirección URL raíz del servicio:</span><span class="sxs-lookup"><span data-stu-id="2a397-109">To construct the request URI, start with the service root URL:</span></span>

`https://graph.microsoft.com/v1.0/me/onenote`

<br/>

<span data-ttu-id="2a397-110">Luego anexe el punto de conexión *content* de la página:</span><span class="sxs-lookup"><span data-stu-id="2a397-110">Then append the page's *content* endpoint:</span></span>

- <span data-ttu-id="2a397-111">**Obtenga el HTML de página y todos los valores de *data-id* definidos**.</span><span class="sxs-lookup"><span data-stu-id="2a397-111">**Get the page HTML and all defined *data-id* values**</span></span><br/><br/>`../pages/{id}/content`   

- <span data-ttu-id="2a397-112">**Obtenga el HTML de página y todos los valores de *data-id* definidos y todos los valores de *id* generados**.</span><span class="sxs-lookup"><span data-stu-id="2a397-112">**Get the page HTML, all defined *data-id* values, and all generated *id* values**</span></span><br/><br/>`../pages/{page-id}/content?includeIDs=true` 

<span data-ttu-id="2a397-113">Los valores de **data-id** y de **id** se usan como identificadores **target** de los elementos que se quieren actualizar.</span><span class="sxs-lookup"><span data-stu-id="2a397-113">The **data-id** and **id** values are used as **target** identifiers for the elements you want to update.</span></span>

 
<span data-ttu-id="2a397-114">El identificador URI de solicitud completo tendrá un aspecto similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="2a397-114">Your full request URI will look like this:</span></span><br/><br/>`https://graph.microsoft.com/v1.0/me/onenote/pages/{id}/content`


<span data-ttu-id="2a397-115">Obtenga más información sobre la [dirección URL raíz del servicio](/graph/api/resources/onenote-api-overview?view=graph-rest-1.0#root-url).</span><span class="sxs-lookup"><span data-stu-id="2a397-115">Learn more about the [service root URL](/graph/api/resources/onenote-api-overview?view=graph-rest-1.0#root-url).</span></span>


<a name="message-body"></a>

## <a name="construct-the-message-body"></a><span data-ttu-id="2a397-116">Crear al cuerpo del mensaje</span><span class="sxs-lookup"><span data-stu-id="2a397-116">Construct the message body</span></span>

<span data-ttu-id="2a397-117">El código HTML de una página de OneNote contiene texto, imágenes y otro contenido organizado en estructuras tales como **div**, **img** y **ol** elementos.</span><span class="sxs-lookup"><span data-stu-id="2a397-117">The HTML of a OneNote page contains text, images, and other content organized into structures such as **div**, **img**, and **ol** elements.</span></span> <span data-ttu-id="2a397-118">Para actualizar el contenido de la página de OneNote, puede agregar y reemplazar elementos HTML en la página.</span><span class="sxs-lookup"><span data-stu-id="2a397-118">To update OneNote page content, you add and replace HTML elements on the page.</span></span>

<span data-ttu-id="2a397-119">Los cambios se envían en el cuerpo del mensaje como matriz de objetos de cambio JSON.</span><span class="sxs-lookup"><span data-stu-id="2a397-119">Your changes are sent in the message body as an array of JSON change objects.</span></span> <span data-ttu-id="2a397-120">Cada objeto especifica el nuevo contenido HTML del elemento de destino y qué hacer con el contenido.</span><span class="sxs-lookup"><span data-stu-id="2a397-120">Each object specifies the target element, new HTML content, and what to do with the content.</span></span>

<span data-ttu-id="2a397-p104">La siguiente matriz define dos cambios. El primero inserta una imagen arriba del párrafo como un elemento relacionado, el segundo anexa un elemento a la lista como un último elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="2a397-p104">The following array defines two changes. The first inserts an image above a paragraph as a sibling, and the second appends an item to a list as a last child.</span></span>

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

<span data-ttu-id="2a397-123">Vea [más ejemplos](#example-requests).</span><span class="sxs-lookup"><span data-stu-id="2a397-123">See [more examples](#example-requests).</span></span>


### <a name="attributes-for-json-change-objects"></a><span data-ttu-id="2a397-124">Atributos para los objetos de cambio JSON</span><span class="sxs-lookup"><span data-stu-id="2a397-124">Attributes for JSON change objects</span></span>

<span data-ttu-id="2a397-125">Use los atributos **target**, **action**, **position** y **content** para definir objetos JSON para solicitudes PATCH.</span><span class="sxs-lookup"><span data-stu-id="2a397-125">Use the **target**, **action**, **position**, and **content** attributes to define JSON objects for PATCH requests.</span></span>

#### <a name="target"></a><span data-ttu-id="2a397-126">target</span><span class="sxs-lookup"><span data-stu-id="2a397-126">target</span></span>

<span data-ttu-id="2a397-p105">Elemento que se va a actualizar. El valor debe ser uno de los siguientes identificadores:</span><span class="sxs-lookup"><span data-stu-id="2a397-p105">The element to update. The value must be one of the following identifiers:</span></span>

| <span data-ttu-id="2a397-129">Identificador</span><span class="sxs-lookup"><span data-stu-id="2a397-129">Identifier</span></span> | <span data-ttu-id="2a397-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a397-130">Description</span></span> |  
|------|------|  
| <span data-ttu-id="2a397-131">#{data-id}</span><span class="sxs-lookup"><span data-stu-id="2a397-131">#{data-id}</span></span> | <p><span data-ttu-id="2a397-132">Este identificador se define opcionalmente en los elementos del HTML de entrada [al crear una página](onenote-create-page.md) o [actualizar una página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="2a397-132">This ID is optionally defined on elements in the input HTML when [creating a page](onenote-create-page.md) or [updating a page](onenote-update-page.md).</span></span> <span data-ttu-id="2a397-133">Use # como prefijo.</span><span class="sxs-lookup"><span data-stu-id="2a397-133">Prefix the value with a #.</span></span></p><p> <span data-ttu-id="2a397-134">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2a397-134">Example:</span></span><br/><span data-ttu-id="2a397-135">`'target':'#intro'` tiene como destino el elemento `<div data-id="intro" ...>`</span><span class="sxs-lookup"><span data-stu-id="2a397-135">`'target':'#intro'` targets the element `<div data-id="intro" ...>`</span></span></p> |  
| <span data-ttu-id="2a397-136">id</span><span class="sxs-lookup"><span data-stu-id="2a397-136">id</span></span> | <p><span data-ttu-id="2a397-137">Se trata del [identificador generado](#generated-ids) en Microsoft Graph, y es necesario para la mayoría de las operaciones de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="2a397-137">This is the [generated ID](#generated-ids) from Microsoft Graph, and is required for most replace operations.</span></span> <span data-ttu-id="2a397-138">No use # como prefijo.</span><span class="sxs-lookup"><span data-stu-id="2a397-138">Do not prefix with a #.</span></span></p><p> <span data-ttu-id="2a397-139">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2a397-139">Example:</span></span><br/><span data-ttu-id="2a397-140">`'target':'div:{33f8a2...}{37}'` tiene como destino el elemento `<div id="div:{33f8a2...}{37}" ...>`</span><span class="sxs-lookup"><span data-stu-id="2a397-140">`'target':'div:{33f8a2...}{37}'` targets the element `<div id="div:{33f8a2...}{37}" ...>`</span></span></p><p><span data-ttu-id="2a397-141">No debe confundirse con los valores de **id** definidos en el [HTML de entrada](onenote-input-output-html.md).</span><span class="sxs-lookup"><span data-stu-id="2a397-141">Don't confuse these with any **id** values defined in the [input HTML](onenote-input-output-html.md).</span></span> <span data-ttu-id="2a397-142">Todos los valores de **id** enviados en el HTML de entrada se descartan.</span><span class="sxs-lookup"><span data-stu-id="2a397-142">All **id** values sent in the input HTML are discarded.</span></span></p> |  
| <span data-ttu-id="2a397-143">body</span><span class="sxs-lookup"><span data-stu-id="2a397-143">body</span></span> | <span data-ttu-id="2a397-144">Palabra clave que tiene como destino el primer div en la página.</span><span class="sxs-lookup"><span data-stu-id="2a397-144">The keyword that targets the first div on the page.</span></span> <span data-ttu-id="2a397-145">No use # como prefijo.</span><span class="sxs-lookup"><span data-stu-id="2a397-145">Do not prefix with a #.</span></span> |  
| <span data-ttu-id="2a397-146">title</span><span class="sxs-lookup"><span data-stu-id="2a397-146">title</span></span> | <span data-ttu-id="2a397-147">Palabra clave que tiene como destino el título de página.</span><span class="sxs-lookup"><span data-stu-id="2a397-147">The keyword that targets the page title.</span></span> <span data-ttu-id="2a397-148">No use # como prefijo.</span><span class="sxs-lookup"><span data-stu-id="2a397-148">Do not prefix with a #.</span></span> |  
 
#### <a name="action"></a><span data-ttu-id="2a397-149">action</span><span class="sxs-lookup"><span data-stu-id="2a397-149">action</span></span>

<span data-ttu-id="2a397-p111">La acción que se va a realizar en el elemento de destino. Vea [acciones admitidas para elementos](#supported-elements-and-actions).</span><span class="sxs-lookup"><span data-stu-id="2a397-p111">The action to perform on the target element. See [supported actions for elements](#supported-elements-and-actions).</span></span>

| <span data-ttu-id="2a397-152">Acción</span><span class="sxs-lookup"><span data-stu-id="2a397-152">Action</span></span> | <span data-ttu-id="2a397-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a397-153">Description</span></span> |  
|------|------|  
| <span data-ttu-id="2a397-154">append</span><span class="sxs-lookup"><span data-stu-id="2a397-154">append</span></span> | <p><span data-ttu-id="2a397-155">Agrega el contenido especificado al destino como primer o último elemento secundario, tal y como se determina en el atributo **position**.</span><span class="sxs-lookup"><span data-stu-id="2a397-155">Adds the supplied content to the target as a first or last child, as determined by the **position** attribute.</span></span></p><p><span data-ttu-id="2a397-156">Solo se aplica a los elementos **body**, **div**, **ol** y **ul**.</span><span class="sxs-lookup"><span data-stu-id="2a397-156">Applies only to **body**, **div**, **ol**, and **ul** elements.</span></span></p> |  
| <span data-ttu-id="2a397-157">insert</span><span class="sxs-lookup"><span data-stu-id="2a397-157">insert</span></span> | <span data-ttu-id="2a397-158">Agrega el contenido especificado como elemento del mismo nivel antes o después del elemento de destino, tal y como se determina en el atributo **position**.</span><span class="sxs-lookup"><span data-stu-id="2a397-158">Adds the supplied content as a sibling before or after the target, as determined by the **position** attribute.</span></span> |  
| <span data-ttu-id="2a397-159">prepend</span><span class="sxs-lookup"><span data-stu-id="2a397-159">prepend</span></span> | <p><span data-ttu-id="2a397-160">Agrega el contenido especificado al destino como primer elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="2a397-160">Adds the supplied content to the target as a first child.</span></span> <span data-ttu-id="2a397-161">Acceso directo a **append** + **before**.</span><span class="sxs-lookup"><span data-stu-id="2a397-161">Shortcut for **append** + **before**.</span></span></p><p><span data-ttu-id="2a397-162">Solo se aplica a los elementos **body**, **div**, **ol** y **ul**.</span><span class="sxs-lookup"><span data-stu-id="2a397-162">Applies only to **body**, **div**, **ol**, and **ul** elements.</span></span></p> |  
| <span data-ttu-id="2a397-163">replace</span><span class="sxs-lookup"><span data-stu-id="2a397-163">replace</span></span> | <p><span data-ttu-id="2a397-164">Reemplaza el destino por el contenido especificado.</span><span class="sxs-lookup"><span data-stu-id="2a397-164">Replaces the target with the supplied content.</span></span></p><p><span data-ttu-id="2a397-165">La mayoría de las acciones **replace** requieren el uso del [identificador generado](#generated-ids) para el elemento de destino (excepto **img** y **object** dentro de un div, que también admiten el uso de **data-id**).</span><span class="sxs-lookup"><span data-stu-id="2a397-165">Most **replace** actions require using the [generated ID](#generated-ids) for the target (except **img** and **object** elements within a div, which also support using **data-id**).</span></span></p> |  
 
#### <a name="position"></a><span data-ttu-id="2a397-166">position</span><span class="sxs-lookup"><span data-stu-id="2a397-166">position</span></span>

<span data-ttu-id="2a397-p113">La ubicación donde agregar el contenido provisto, relativa al elemento de destino. Queda predeterminado como **after** si se omite.</span><span class="sxs-lookup"><span data-stu-id="2a397-p113">The location to add the supplied content, relative to the target element. Defaults to **after** if omitted.</span></span>

| <span data-ttu-id="2a397-169">Posición</span><span class="sxs-lookup"><span data-stu-id="2a397-169">Position</span></span> | <span data-ttu-id="2a397-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a397-170">Description</span></span> |  
|------|------|  
| <span data-ttu-id="2a397-171">after (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2a397-171">after (default)</span></span> |<p><span data-ttu-id="2a397-172">Con **append**: último elemento secundario del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="2a397-172">With **append**: The last child of the target element.</span></span></p><p><span data-ttu-id="2a397-173">Con **insert**: siguiente elemento del mismo nivel del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="2a397-173">With **insert**: The subsequent sibling of the target element.</span></span></p> |
| <span data-ttu-id="2a397-174">before</span><span class="sxs-lookup"><span data-stu-id="2a397-174">before</span></span> | <p><span data-ttu-id="2a397-175">Con **append**: primer elemento secundario del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="2a397-175">With **append**: The first child of the target element.</span></span></p><p><span data-ttu-id="2a397-176">Con **insert**: anterior elemento del mismo nivel del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="2a397-176">With **insert**: The preceding sibling of the target element.</span></span></p> |

#### <a name="content"></a><span data-ttu-id="2a397-177">content</span><span class="sxs-lookup"><span data-stu-id="2a397-177">content</span></span>

<span data-ttu-id="2a397-178">Cadena de HTML sintácticamente correcta que se agrega a la página y datos binarios de cualquier imagen o archivo.</span><span class="sxs-lookup"><span data-stu-id="2a397-178">A string of well-formed HTML to add to the page, and any image or file binary data.</span></span> <span data-ttu-id="2a397-179">Si el contenido contiene datos binarios, la solicitud debe enviarse utilizando el tipo de contenido `multipart/form-data` con una parte "Comandos" (véase un [ejemplo](#multipart-request-with-binary-content)).</span><span class="sxs-lookup"><span data-stu-id="2a397-179">If the content contains binary data, the request must be sent using the `multipart/form-data` content type with a "Commands" part (see an [example](#multipart-request-with-binary-content)).</span></span> 
 

<a name="generated-ids"></a>

### <a name="generated-ids"></a><span data-ttu-id="2a397-180">Identificadores generados</span><span class="sxs-lookup"><span data-stu-id="2a397-180">Generated IDs</span></span>
<span data-ttu-id="2a397-181">Microsoft Graph genera valores de **id** para los elementos de la página que pueden actualizarse.</span><span class="sxs-lookup"><span data-stu-id="2a397-181">Microsoft Graph generates **id** values for the elements on the page that can be updated.</span></span> <span data-ttu-id="2a397-182">Para obtener el identificador generado, use la expresión de cadena de consulta `includeIDs=true` en la solicitud GET:</span><span class="sxs-lookup"><span data-stu-id="2a397-182">To get generated IDs, use the `includeIDs=true` query string expression in your GET request:</span></span>

`GET ../notes/pages/{page-id}/content?includeIDs=true` 

> <span data-ttu-id="2a397-183">**Nota:** La API descarta todos los valores de **id** definidos en el [HTML de entrada](onenote-input-output-html.md) de las solicitudes create-page y update-page.</span><span class="sxs-lookup"><span data-stu-id="2a397-183">**Note:** The API discards all **id** values that are defined in the [input HTML](onenote-input-output-html.md) of create-page and update-page requests.</span></span>

<span data-ttu-id="2a397-184">En el siguiente ejemplo se muestran los identificadores generados para un párrafo y una imagen en el [HTML de salida](onenote-input-output-html.md) de una página.</span><span class="sxs-lookup"><span data-stu-id="2a397-184">The following example shows generated IDs for a paragraph and an image in the [output HTML](onenote-input-output-html.md) of a page.</span></span>

```html
<p id="p:{33f8a242-7c33-4bb2-90c5-8425a68cc5bf}{40}">Some text on the page</p>
<img id="img:{33f8a242-7c33-4bb2-90c5-8425a68cc5bf}{45}" ... />
```

<span data-ttu-id="2a397-185">Los valores de **id** generados pueden cambiar después de la actualización de una página, por lo tanto debe obtener los valores actuales antes de crear una solicitud de PATCH que los utilice.</span><span class="sxs-lookup"><span data-stu-id="2a397-185">Generated **id** values might change after a page update, so you should get the current values before building a PATCH request that uses them.</span></span>
 
<span data-ttu-id="2a397-186">Puede especificar los elementos de destino con el valor de **data-id** o de **id**, de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="2a397-186">You can specify target elements by using the **data-id** or **id** value, as follows:</span></span>

- <span data-ttu-id="2a397-187">Para las acciones **append** y **insert**, puede usar cualquier identificador como valor de destino.</span><span class="sxs-lookup"><span data-stu-id="2a397-187">For **append** and **insert** actions, you can use either ID as the target value.</span></span>
- <span data-ttu-id="2a397-188">Para las acciones **replace**, debe usar el identificador generado para todos los elementos excepto el título de página y las imágenes y los objetos que se encuentran dentro de un div.</span><span class="sxs-lookup"><span data-stu-id="2a397-188">For **replace** actions, you must use the generated ID for all elements except for the page title and images and objects that are within a div.</span></span> 
    - <span data-ttu-id="2a397-189">Para reemplazar un título, utilice la palabra clave **title**.</span><span class="sxs-lookup"><span data-stu-id="2a397-189">To replace a title, use the **title** keyword.</span></span> 
    - <span data-ttu-id="2a397-190">Para reemplazar imágenes y objetos que se encuentran en un div, utilice **data-id** o **id**.</span><span class="sxs-lookup"><span data-stu-id="2a397-190">To replace images and objects that are within a div, use either **data-id** or **id**.</span></span>

<span data-ttu-id="2a397-191">En el siguiente ejemplo se usa el valor de **id** como destino.</span><span class="sxs-lookup"><span data-stu-id="2a397-191">The following example uses the **id** value for the target.</span></span> <span data-ttu-id="2a397-192">No use el prefijo # con un identificador generado.</span><span class="sxs-lookup"><span data-stu-id="2a397-192">Don't use the # prefix with a generated ID.</span></span>

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

## <a name="supported-elements-and-actions"></a><span data-ttu-id="2a397-193">Acciones y elementos admitidos</span><span class="sxs-lookup"><span data-stu-id="2a397-193">Supported elements and actions</span></span>

<span data-ttu-id="2a397-194">Se pueden actualizar muchos elementos de la página, pero cada tipo de elemento admite acciones específicas.</span><span class="sxs-lookup"><span data-stu-id="2a397-194">Many elements on the page can be updated, but each element type supports specific actions.</span></span> <span data-ttu-id="2a397-195">En la siguiente tabla se muestran los elementos de destino admitidos y las acciones de actualización que admiten.</span><span class="sxs-lookup"><span data-stu-id="2a397-195">The following table shows supported target elements and the update actions that they support.</span></span>

| <span data-ttu-id="2a397-196">Elemento</span><span class="sxs-lookup"><span data-stu-id="2a397-196">Element</span></span> | <span data-ttu-id="2a397-197">Reemplazar</span><span class="sxs-lookup"><span data-stu-id="2a397-197">Replace</span></span> | <span data-ttu-id="2a397-198">Anexar elemento secundario</span><span class="sxs-lookup"><span data-stu-id="2a397-198">Append child</span></span> | <span data-ttu-id="2a397-199">Insertar elemento del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="2a397-199">Insert sibling</span></span> |  
|------|:------:|:------:|:------:|  
| <span data-ttu-id="2a397-200">body</span><span class="sxs-lookup"><span data-stu-id="2a397-200">body</span></span><br /> <span data-ttu-id="2a397-201">(tiene como destino el primer div en la página)</span><span class="sxs-lookup"><span data-stu-id="2a397-201">(targets first div on the page)</span></span> | <span data-ttu-id="2a397-202">no</span><span class="sxs-lookup"><span data-stu-id="2a397-202">no</span></span> | <span data-ttu-id="2a397-203">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-203">**yes**</span></span> | <span data-ttu-id="2a397-204">no</span><span class="sxs-lookup"><span data-stu-id="2a397-204">no</span></span> |  
| <span data-ttu-id="2a397-205">div</span><span class="sxs-lookup"><span data-stu-id="2a397-205">div</span></span><br /> <span data-ttu-id="2a397-206">([posición absoluta](onenote-abs-pos.md))</span><span class="sxs-lookup"><span data-stu-id="2a397-206">([absolute positioned](onenote-abs-pos.md))</span></span> | <span data-ttu-id="2a397-207">no</span><span class="sxs-lookup"><span data-stu-id="2a397-207">no</span></span> | <span data-ttu-id="2a397-208">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-208">**yes**</span></span> | <span data-ttu-id="2a397-209">no</span><span class="sxs-lookup"><span data-stu-id="2a397-209">no</span></span> |  
| <span data-ttu-id="2a397-210">div</span><span class="sxs-lookup"><span data-stu-id="2a397-210">div</span></span><br /> <span data-ttu-id="2a397-211">(en un elemento div)</span><span class="sxs-lookup"><span data-stu-id="2a397-211">(within a div)</span></span> | <span data-ttu-id="2a397-212">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-212">**yes**</span></span><br/><span data-ttu-id="2a397-213">(solo identificador)</span><span class="sxs-lookup"><span data-stu-id="2a397-213">(id only)</span></span> | <span data-ttu-id="2a397-214">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-214">**yes**</span></span> | <span data-ttu-id="2a397-215">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-215">**yes**</span></span> |   
| <span data-ttu-id="2a397-216">img, object</span><span class="sxs-lookup"><span data-stu-id="2a397-216">img, object</span></span><br /> <span data-ttu-id="2a397-217">(en un elemento div)</span><span class="sxs-lookup"><span data-stu-id="2a397-217">(within a div)</span></span> | <span data-ttu-id="2a397-218">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-218">**yes**</span></span> | <span data-ttu-id="2a397-219">no</span><span class="sxs-lookup"><span data-stu-id="2a397-219">no</span></span> | <span data-ttu-id="2a397-220">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-220">**yes**</span></span> |   
| <span data-ttu-id="2a397-221">ol, ul</span><span class="sxs-lookup"><span data-stu-id="2a397-221">ol, ul</span></span> | <span data-ttu-id="2a397-222">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-222">**yes**</span></span><br/><span data-ttu-id="2a397-223">(solo identificador)</span><span class="sxs-lookup"><span data-stu-id="2a397-223">(id only)</span></span> | <span data-ttu-id="2a397-224">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-224">**yes**</span></span> | <span data-ttu-id="2a397-225">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-225">**yes**</span></span> |   
| <span data-ttu-id="2a397-226">table</span><span class="sxs-lookup"><span data-stu-id="2a397-226">table</span></span> | <span data-ttu-id="2a397-227">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-227">**yes**</span></span><br/><span data-ttu-id="2a397-228">(solo identificador)</span><span class="sxs-lookup"><span data-stu-id="2a397-228">(id only)</span></span> | <span data-ttu-id="2a397-229">no</span><span class="sxs-lookup"><span data-stu-id="2a397-229">no</span></span> | <span data-ttu-id="2a397-230">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-230">**yes**</span></span> |   
| <span data-ttu-id="2a397-231">p, li, h1-h6</span><span class="sxs-lookup"><span data-stu-id="2a397-231">p, li, h1-h6</span></span> | <span data-ttu-id="2a397-232">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-232">**yes**</span></span><br/><span data-ttu-id="2a397-233">(solo identificador)</span><span class="sxs-lookup"><span data-stu-id="2a397-233">(id only)</span></span> | <span data-ttu-id="2a397-234">no</span><span class="sxs-lookup"><span data-stu-id="2a397-234">no</span></span> | <span data-ttu-id="2a397-235">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-235">**yes**</span></span> |   
| <span data-ttu-id="2a397-236">title</span><span class="sxs-lookup"><span data-stu-id="2a397-236">title</span></span> | <span data-ttu-id="2a397-237">**sí**</span><span class="sxs-lookup"><span data-stu-id="2a397-237">**yes**</span></span> | <span data-ttu-id="2a397-238">no</span><span class="sxs-lookup"><span data-stu-id="2a397-238">no</span></span> | <span data-ttu-id="2a397-239">no</span><span class="sxs-lookup"><span data-stu-id="2a397-239">no</span></span> |  
 
<br/>

<span data-ttu-id="2a397-240">Los siguientes elementos no admiten ninguna acción de actualización.</span><span class="sxs-lookup"><span data-stu-id="2a397-240">The following elements do not support any update actions.</span></span>

- <span data-ttu-id="2a397-241">img ([posición absoluta](onenote-abs-pos.md))</span><span class="sxs-lookup"><span data-stu-id="2a397-241">img ([absolute positioned](onenote-abs-pos.md))</span></span>
- <span data-ttu-id="2a397-242">object ([posición absoluta](onenote-abs-pos.md))</span><span class="sxs-lookup"><span data-stu-id="2a397-242">object ([absolute positioned](onenote-abs-pos.md))</span></span>
- <span data-ttu-id="2a397-243">tr, td</span><span class="sxs-lookup"><span data-stu-id="2a397-243">tr, td</span></span>
- <span data-ttu-id="2a397-244">meta</span><span class="sxs-lookup"><span data-stu-id="2a397-244">meta</span></span>
- <span data-ttu-id="2a397-245">head</span><span class="sxs-lookup"><span data-stu-id="2a397-245">head</span></span>
- <span data-ttu-id="2a397-246">span</span><span class="sxs-lookup"><span data-stu-id="2a397-246">span</span></span>
- <span data-ttu-id="2a397-247">a</span><span class="sxs-lookup"><span data-stu-id="2a397-247">a</span></span>
- <span data-ttu-id="2a397-248">etiquetas de estilo</span><span class="sxs-lookup"><span data-stu-id="2a397-248">style tags</span></span>


<a name="examples"></a>

## <a name="example-requests"></a><span data-ttu-id="2a397-249">Solicitudes de ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a397-249">Example requests</span></span>

<span data-ttu-id="2a397-250">Una solicitud de actualización contiene uno o más cambios que se representan como objetos de cambio JSON.</span><span class="sxs-lookup"><span data-stu-id="2a397-250">An update request contains one or more changes represented as JSON change objects.</span></span> <span data-ttu-id="2a397-251">Estos objetos pueden definir diferentes destinos en la página y diferentes acciones y contenido para los destinos.</span><span class="sxs-lookup"><span data-stu-id="2a397-251">These objects can define different targets on the page and different actions and content for the targets.</span></span>

<span data-ttu-id="2a397-252">En los siguientes ejemplos se incluyen objetos JSON usados en solicitudes PATCH y solicitudes PATCH completas:</span><span class="sxs-lookup"><span data-stu-id="2a397-252">The following examples include JSON objects used in PATCH requests and complete PATCH requests:</span></span>

- [<span data-ttu-id="2a397-253">Anexar elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2a397-253">Append child elements</span></span>](#append-child-elements)
- [<span data-ttu-id="2a397-254">Insertar elementos del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="2a397-254">Insert sibling elements</span></span>](#insert-sibling-elements)
- [<span data-ttu-id="2a397-255">Reemplazar elementos</span><span class="sxs-lookup"><span data-stu-id="2a397-255">Replace elements</span></span>](#replace-elements)
- [<span data-ttu-id="2a397-256">Solicitud PATCH completa</span><span class="sxs-lookup"><span data-stu-id="2a397-256">Complete PATCH requests</span></span>](#complete-patch-request-examples)


<a name="append-examples"></a>

### <a name="append-child-elements"></a><span data-ttu-id="2a397-257">Anexar elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2a397-257">Append child elements</span></span>

<span data-ttu-id="2a397-258">La acción **append** agrega un elemento secundario a un elemento **body**, **div** (dentro de un div), **ol** o **ul**.</span><span class="sxs-lookup"><span data-stu-id="2a397-258">The **append** action adds a child to a **body**, **div** (within a div), **ol**, or **ul** element.</span></span> <span data-ttu-id="2a397-259">El atributo **position** determina si el elemento secundario se va a anexar antes o después del destino.</span><span class="sxs-lookup"><span data-stu-id="2a397-259">The **position** attribute determines whether to append the child before or after the target.</span></span> <span data-ttu-id="2a397-260">La posición predeterminada es **after**.</span><span class="sxs-lookup"><span data-stu-id="2a397-260">The default position is **after**.</span></span>

#### <a name="append-to-a-div"></a><span data-ttu-id="2a397-261">Anexar a un div</span><span class="sxs-lookup"><span data-stu-id="2a397-261">Append to a div</span></span>

<span data-ttu-id="2a397-262">En el ejemplo siguiente se agregan dos nodos secundarios al elemento **div1**.</span><span class="sxs-lookup"><span data-stu-id="2a397-262">The following example adds two child nodes to the **div1** element.</span></span> <span data-ttu-id="2a397-263">Agrega una imagen como primer elemento secundario y un párrafo como último elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="2a397-263">It adds an image as the first child and a paragraph as the last child.</span></span> 

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
 

#### <a name="append-to-the-body-element"></a><span data-ttu-id="2a397-264">Anexar al elemento *body*</span><span class="sxs-lookup"><span data-stu-id="2a397-264">Append to the *body* element</span></span>

<span data-ttu-id="2a397-265">Puede usar el acceso directo **body** para anexar un elemento secundario en el interior del primer div de cualquier página.</span><span class="sxs-lookup"><span data-stu-id="2a397-265">You can use the **body** shortcut to append a child element inside the first div on any page.</span></span>

<span data-ttu-id="2a397-266">En el siguiente ejemplo se agregan dos párrafos como primer elemento secundario y último elemento secundario en el primer div de la página.</span><span class="sxs-lookup"><span data-stu-id="2a397-266">The following example adds two paragraphs as the first child and the last child to the first div on the page.</span></span> <span data-ttu-id="2a397-267">No use # con el destino **body**.</span><span class="sxs-lookup"><span data-stu-id="2a397-267">Don't use a # with the **body** target.</span></span> <span data-ttu-id="2a397-268">En este ejemplo se usa la acción **prepend** como acceso directo a **append** + **before**.</span><span class="sxs-lookup"><span data-stu-id="2a397-268">This example uses the **prepend** action as a shortcut for **append** + **before**.</span></span>

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
 

#### <a name="append-to-a-list"></a><span data-ttu-id="2a397-269">Anexar a una lista</span><span class="sxs-lookup"><span data-stu-id="2a397-269">Append to a list</span></span>

<span data-ttu-id="2a397-p122">La acción insert agrega un elemento relacionado al elemento de destino. El atributo position determina si el elemento relacionado se insertará antes o después del elemento de destino. La posición predeterminada es after. Consulte elementos que admiten insertar.</span><span class="sxs-lookup"><span data-stu-id="2a397-p122">The following example adds a list item as a last child to the target list. The **list-style-type** property is defined because the item uses a non-default list style.</span></span>

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

### <a name="insert-sibling-elements"></a><span data-ttu-id="2a397-272">Insertar elementos del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="2a397-272">Insert sibling elements</span></span>

<span data-ttu-id="2a397-273">La acción **insert** agrega un elemento del mismo nivel al elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="2a397-273">The **insert** action adds a sibling to the target element.</span></span> <span data-ttu-id="2a397-274">El atributo **position** determina si el elemento del mismo nivel se va a insertar antes o después del destino.</span><span class="sxs-lookup"><span data-stu-id="2a397-274">The **position** attribute determines whether to insert the sibling before or after the target.</span></span> <span data-ttu-id="2a397-275">La posición predeterminada es **after**.</span><span class="sxs-lookup"><span data-stu-id="2a397-275">The default position is **after**.</span></span> <span data-ttu-id="2a397-276">Vea [elementos que admiten **insert**](#supported-elements-and-actions).</span><span class="sxs-lookup"><span data-stu-id="2a397-276">See [elements that support **insert**](#supported-elements-and-actions).</span></span>

#### <a name="insert-siblings"></a><span data-ttu-id="2a397-277">Insertar elementos del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="2a397-277">Insert siblings</span></span>

<span data-ttu-id="2a397-p124">Puede usar tanto el data-id o el id generado como valor de destino para reemplazar elementosimg y object que se encuentran dentro de un div. Para reemplazar el título de una página, use la palabra clave title. Para todos los demás elementos que admiten reemplazo, debe usar el Id. generado.</span><span class="sxs-lookup"><span data-stu-id="2a397-p124">The following example adds two sibling nodes to the page. It adds an image above the **para1** element and a paragraph below the **para2** element.</span></span>

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

### <a name="replace-elements"></a><span data-ttu-id="2a397-280">Reemplazar elementos</span><span class="sxs-lookup"><span data-stu-id="2a397-280">Replace elements</span></span>

<span data-ttu-id="2a397-281">Puede utilizar el **data-id** o el **id** generado como valor de destino para reemplazar los elementos **img** y **object** que están dentro de un div.</span><span class="sxs-lookup"><span data-stu-id="2a397-281">You can use either the **data-id** or generated **id** as the target value to replace **img** and **object** elements that are within a div.</span></span> <span data-ttu-id="2a397-282">Para reemplazar el título de página, utilice la palabra clave **title**.</span><span class="sxs-lookup"><span data-stu-id="2a397-282">To replace the page title, use the **title** keyword.</span></span> <span data-ttu-id="2a397-283">Para todos los demás [elementos que admiten **replace**](#supported-elements-and-actions), debe usar el identificador generado.</span><span class="sxs-lookup"><span data-stu-id="2a397-283">For all other [elements that support **replace**](#supported-elements-and-actions), you must use the generated ID.</span></span>

#### <a name="replace-an-image"></a><span data-ttu-id="2a397-284">Reemplazar una imagen</span><span class="sxs-lookup"><span data-stu-id="2a397-284">Replace an image</span></span>

<span data-ttu-id="2a397-285">En este ejemplo se reemplaza una imagen por un div mediante el **data-id** de la imagen como destino</span><span class="sxs-lookup"><span data-stu-id="2a397-285">The following example replaces an image with a div by using the image's **data-id** as the target.</span></span> 

```json
[
  {
    'target':'#img1',
    'action':'replace',
    'content':'<div data-id="new-div"><p>This div replaces the image</p></div>'
  }
]
```
 

#### <a name="update-a-table"></a><span data-ttu-id="2a397-286">Actualizar una tabla</span><span class="sxs-lookup"><span data-stu-id="2a397-286">Update a table</span></span> 

<span data-ttu-id="2a397-p126">Este ejemplo muestra cómo cambiar el título de una página. Para cambiar el título, use la palabra clave title como el valor del elemento de destino. No use # con el elemento de destino title.</span><span class="sxs-lookup"><span data-stu-id="2a397-p126">This example shows how to update a table by using its generated ID. Replacing **tr** and **td** elements is not supported, but you can replace the entire table.</span></span>

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
 

#### <a name="change-the-title"></a><span data-ttu-id="2a397-289">Cambiar el título</span><span class="sxs-lookup"><span data-stu-id="2a397-289">Change the title</span></span> 

<span data-ttu-id="2a397-290">En este ejemplo se muestra cómo cambiar el título de la página.</span><span class="sxs-lookup"><span data-stu-id="2a397-290">This example shows how to change the title of a page.</span></span> <span data-ttu-id="2a397-291">Para cambiar el título, use la palabra clave **title** como valor de destino.</span><span class="sxs-lookup"><span data-stu-id="2a397-291">To change the title, use the **title** keyword as the target value.</span></span> <span data-ttu-id="2a397-292">No use el prefijo # con el destino title.</span><span class="sxs-lookup"><span data-stu-id="2a397-292">Don't use a # with the title target.</span></span>

```json
[
  {
    'target':'title',
    'action':'replace',
    'content':'New title'
  }
]
```
 

#### <a name="update-a-to-do-item"></a><span data-ttu-id="2a397-293">Actualizar una tarea pendiente</span><span class="sxs-lookup"><span data-stu-id="2a397-293">Update a to-do item</span></span>

<span data-ttu-id="2a397-294">En el siguiente ejemplo se usa la acción replace para cambiar un elemento de casilla de tarea pendiente a un estado completado.</span><span class="sxs-lookup"><span data-stu-id="2a397-294">The following example uses the replace action to change a to-do check box item to a completed state.</span></span>

```json
[
  {
    'target':'#task1',
    'action':'replace',
    'content':'<p data-tag="to-do:completed" data-id="task1">First task</p>'
  }
]
```

<span data-ttu-id="2a397-295">Vea [Uso de etiquetas de nota](onenote-note-tags.md) para más información sobre el uso del atributo **data-tag**.</span><span class="sxs-lookup"><span data-stu-id="2a397-295">See [Use note tags](onenote-note-tags.md) for more about using the **data-tag** attribute.</span></span>


<a name="complete-requests"></a>

### <a name="complete-patch-request-examples"></a><span data-ttu-id="2a397-296">Ejemplos de solicitud PATCH completa</span><span class="sxs-lookup"><span data-stu-id="2a397-296">Complete PATCH request examples</span></span>

<span data-ttu-id="2a397-297">En los ejemplos siguientes se muestran solicitudes PATCH completas.</span><span class="sxs-lookup"><span data-stu-id="2a397-297">The following examples show complete PATCH requests.</span></span>

#### <a name="request-with-text-content-only"></a><span data-ttu-id="2a397-298">Solicitud con solo contenido de texto</span><span class="sxs-lookup"><span data-stu-id="2a397-298">Request with text content only</span></span>

<span data-ttu-id="2a397-299">En el siguiente ejemplo se muestra una solicitud PATCH que utiliza el tipo de contenido **application/json**.</span><span class="sxs-lookup"><span data-stu-id="2a397-299">The following example shows a PATCH request that uses the **application/json** content type.</span></span> <span data-ttu-id="2a397-300">Puede usar este formato cuando el contenido no contiene datos binarios.</span><span class="sxs-lookup"><span data-stu-id="2a397-300">You can use this format when your content doesn't contain binary data.</span></span>

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

#### <a name="multipart-request-with-binary-content"></a><span data-ttu-id="2a397-301">Solicitud de varias partes con contenido binario</span><span class="sxs-lookup"><span data-stu-id="2a397-301">Multipart request with binary content</span></span> 

<span data-ttu-id="2a397-302">En el ejemplo siguiente se muestra una solicitud PATCH de varias partes que incluye datos binarios.</span><span class="sxs-lookup"><span data-stu-id="2a397-302">The following example shows a multipart PATCH request that includes binary data.</span></span> <span data-ttu-id="2a397-303">Las solicitudes de varias partes requieren una parte "Comandos" que especifica el tipo de contenido **application/json** y contiene la matriz de objetos de cambio JSON.</span><span class="sxs-lookup"><span data-stu-id="2a397-303">Multipart requests require a "Commands" part that specifies the **application/json** content type and contains the array of JSON change objects.</span></span> <span data-ttu-id="2a397-304">Otras partes de datos pueden contener datos binarios.</span><span class="sxs-lookup"><span data-stu-id="2a397-304">Other data parts can contain binary data.</span></span> <span data-ttu-id="2a397-305">Los nombres de parte suelen ser cadenas anexadas con la hora actual en milisegundos o un GUID aleatorio.</span><span class="sxs-lookup"><span data-stu-id="2a397-305">Part names typically are strings appended with the current time in milliseconds or a random GUID.</span></span>

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

## <a name="request-and-response-information-for-patch-requests"></a><span data-ttu-id="2a397-306">Información de solicitud y respuesta de las solicitudes PATCH</span><span class="sxs-lookup"><span data-stu-id="2a397-306">Request and response information for PATCH requests</span></span>

| <span data-ttu-id="2a397-307">Datos de solicitud</span><span class="sxs-lookup"><span data-stu-id="2a397-307">Request data</span></span> | <span data-ttu-id="2a397-308">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a397-308">Description</span></span> |  
|------|------|  
| <span data-ttu-id="2a397-309">Protocolo</span><span class="sxs-lookup"><span data-stu-id="2a397-309">Protocol</span></span> | <span data-ttu-id="2a397-310">Todas las solicitudes usan el protocolo HTTPS SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="2a397-310">All requests use the SSL/TLS HTTPS protocol.</span></span> |  
| <span data-ttu-id="2a397-311">Encabezado Authorization</span><span class="sxs-lookup"><span data-stu-id="2a397-311">Authorization header</span></span> | <p><span data-ttu-id="2a397-312">`Bearer {token}`, donde `{token}` es un token de acceso de OAuth 2.0 válido para la aplicación registrada.</span><span class="sxs-lookup"><span data-stu-id="2a397-312">`Bearer {token}`, where `{token}` is a valid OAuth 2.0 access token for your registered app.</span></span></p><p><span data-ttu-id="2a397-313">Si falta o no es válido, la solicitud producirá errores con el código de estado 401.</span><span class="sxs-lookup"><span data-stu-id="2a397-313">If missing or invalid, the request fails with a 401 status code.</span></span> <span data-ttu-id="2a397-314">Vea [Authentication and permissions](permissions-reference.md) (Autenticación y permisos).</span><span class="sxs-lookup"><span data-stu-id="2a397-314">See [Authentication and permissions](permissions-reference.md).</span></span></p> |  
| <span data-ttu-id="2a397-315">Encabezado Content-Type</span><span class="sxs-lookup"><span data-stu-id="2a397-315">Content-Type header</span></span> | <p><span data-ttu-id="2a397-316">`application/json` para la matriz de objetos de cambio JSON, tanto si se envía directamente en el cuerpo del mensaje como si se envía en la parte "Comandos" necesaria de las [solicitudes de varias partes](#multipart-request-with-binary-content).</span><span class="sxs-lookup"><span data-stu-id="2a397-316">`application/json` for the array of JSON change objects, whether sent directly in the message body or in the required "Commands" part of [multipart requests](#multipart-request-with-binary-content).</span></span></p><p><span data-ttu-id="2a397-317">Se necesitan solicitudes de varias partes cuando se envían datos binarios y se utiliza el tipo de contenido `multipart/form-data; boundary=part-boundary`, donde `{part-boundary}` es una cadena que señala el inicio y el final de cada parte de datos.</span><span class="sxs-lookup"><span data-stu-id="2a397-317">Multipart requests are required when sending binary data, and use the `multipart/form-data; boundary=part-boundary` content type, where `{part-boundary}` is a string that signals the start and end of each data part.</span></span></p> |  

<br/> 

| <span data-ttu-id="2a397-318">Datos de respuesta</span><span class="sxs-lookup"><span data-stu-id="2a397-318">Response data</span></span> | <span data-ttu-id="2a397-319">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a397-319">Description</span></span> |  
|------|------|  
| <span data-ttu-id="2a397-320">Errores</span><span class="sxs-lookup"><span data-stu-id="2a397-320">Success code</span></span> | <span data-ttu-id="2a397-p131">Si la solicitud de actualización falla, la API devuelve errores en el objeto api.diagnostics en el cuerpo de la respuesta. La solicitud fallará si:</span><span class="sxs-lookup"><span data-stu-id="2a397-p131">A 204 HTTP status code. No JSON data is returned for a PATCH request.</span></span> |  
| <span data-ttu-id="2a397-323">Errores</span><span class="sxs-lookup"><span data-stu-id="2a397-323">Errors</span></span> | <span data-ttu-id="2a397-324">Lea [Códigos de error para API de OneNote de Microsoft Graph](onenote-error-codes.md) para obtener información sobre los errores de OneNote que puede devolver Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="2a397-324">Read [Error codes for OneNote APIs in Microsoft Graph](onenote-error-codes.md) to learn about OneNote errors that Microsoft Graph can return.</span></span> |  
 
 

<a name="root-url"></a>

### <a name="constructing-the-microsoft-graph-service-root-url"></a><span data-ttu-id="2a397-325">Crear la URL raíz del servicio de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="2a397-325">Constructing the Microsoft Graph service root URL</span></span>

<span data-ttu-id="2a397-326">La dirección URL raíz del servicio OneNote utiliza el siguiente formato para todas las llamadas a la API de OneNote:</span><span class="sxs-lookup"><span data-stu-id="2a397-326">The OneNote service root URL uses the following format for all calls to the OneNote API:</span></span>

`https://graph.microsoft.com/{version}/me/onenote/`

<span data-ttu-id="2a397-327">El segmento `version` de la URL representa la versión de Microsoft Graph que se quiere utilizar.</span><span class="sxs-lookup"><span data-stu-id="2a397-327">The `version` segment in the URL represents the version of Microsoft Graph that you want to use.</span></span> <span data-ttu-id="2a397-328">`v1.0` corresponde al código de producción estable.</span><span class="sxs-lookup"><span data-stu-id="2a397-328">`v1.0` is for stable production code.</span></span> <span data-ttu-id="2a397-329">`beta` corresponde a la prueba de una característica que se encuentra en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="2a397-329">`beta` is to try out a feature that's in development.</span></span> <span data-ttu-id="2a397-330">Las características y la funcionalidad de la versión beta pueden cambiar, por lo que no se debe usar en el código de producción.</span><span class="sxs-lookup"><span data-stu-id="2a397-330">Features and functionality in beta may change, so you shouldn't use it in your production code.</span></span>

<span data-ttu-id="2a397-331">`me` corresponde a contenido de OneNote al que el usuario actual tiene acceso (de su propiedad y compartido).</span><span class="sxs-lookup"><span data-stu-id="2a397-331">`me` is for OneNote content that the current user can access (owned and shared).</span></span> <span data-ttu-id="2a397-332">`users/{id}` corresponde a contenido de OneNote que el usuario especificado (en la dirección URL) ha compartido con el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="2a397-332">`users/{id}` is for OneNote content that the specified user (in the URL) has shared with the current user.</span></span> <span data-ttu-id="2a397-333">Use la [API de Azure AD Graph](https://msdn.microsoft.com/library/azure/ad/graph/api/api-catalog).</span><span class="sxs-lookup"><span data-stu-id="2a397-333">Use the [Azure AD Graph API](https://msdn.microsoft.com/library/azure/ad/graph/api/api-catalog).</span></span>


> <span data-ttu-id="2a397-334">**Nota:** Puede obtener identificadores de usuario realizando una solicitud GET en `https://graph.microsoft.com/v1.0/users`.</span><span class="sxs-lookup"><span data-stu-id="2a397-334">**Note:** You can get user ids by making a GET request on `https://graph.microsoft.com/v1.0/users`.</span></span>



<a name="permissions"></a>

## <a name="permissions"></a><span data-ttu-id="2a397-335">Permisos</span><span class="sxs-lookup"><span data-stu-id="2a397-335">Permissions</span></span>

<span data-ttu-id="2a397-336">Para actualizar páginas OneNote, tiene que solicitar los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="2a397-336">To update OneNote pages, you'll need to request appropriate permissions.</span></span> <span data-ttu-id="2a397-337">Elija el nivel más bajo de permisos que necesita la aplicación para hacer su trabajo.</span><span class="sxs-lookup"><span data-stu-id="2a397-337">Choose the lowest level of permissions that your app needs to do its work.</span></span>

- <span data-ttu-id="2a397-338">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2a397-338">Notes.ReadWrite</span></span>
- <span data-ttu-id="2a397-339">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2a397-339">Notes.ReadWrite.All</span></span>

<span data-ttu-id="2a397-340">Para obtener más información sobre los ámbitos de permiso y cómo funcionan, consulte los [ámbitos de permisos de OneNote](permissions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2a397-340">For more information about permission scopes and how they work, see [OneNote permission scopes](permissions-reference.md).</span></span>
   

<a name="see-also"></a>

## <a name="see-also"></a><span data-ttu-id="2a397-341">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a397-341">See also</span></span>

- [<span data-ttu-id="2a397-342">Agregar imágenes y archivos</span><span class="sxs-lookup"><span data-stu-id="2a397-342">Add images and files</span></span>](onenote-images-files.md)
- [<span data-ttu-id="2a397-343">Integración con OneNote</span><span class="sxs-lookup"><span data-stu-id="2a397-343">Integrate with OneNote</span></span>](integrate-with-onenote.md)
- [<span data-ttu-id="2a397-344">Blog para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="2a397-344">OneNote Developer Blog</span></span>](https://go.microsoft.com/fwlink/?LinkID=390183)
- [<span data-ttu-id="2a397-345">Preguntas de desarrollo de OneNote en Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="2a397-345">OneNote development questions on Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkID=390182)
- [<span data-ttu-id="2a397-346">Repositorios de OneNote en GitHub</span><span class="sxs-lookup"><span data-stu-id="2a397-346">OneNote GitHub repos</span></span>](https://go.microsoft.com/fwlink/?LinkID=390178)  
