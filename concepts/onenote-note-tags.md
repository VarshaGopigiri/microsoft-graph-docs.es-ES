# <a name="use-note-tags-in-onenote-pages"></a><span data-ttu-id="5151e-101">Usar etiquetas en páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="5151e-101">Use note tags in OneNote pages</span></span>

<span data-ttu-id="5151e-102">*__Se aplica a:__ blocs de notas para consumidores de OneDrive | blocs de notas para empresa de Office 365*</span><span class="sxs-lookup"><span data-stu-id="5151e-102">*__Applies to:__ Consumer notebooks on OneDrive | Enterprise notebooks on Office 365*</span></span>

<span data-ttu-id="5151e-103">Use el atributo `data-tag` para agregar y actualizar casillas, estrellas y otras etiquetas de nota integradas en una página de OneNote, como se muestra en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="5151e-103">Use the `data-tag` attribute to add and update check boxes, stars, and other built-in note tags on a OneNote page, as shown in the following image.</span></span>

![Tres etiquetas de nota que se muestran en una página de OneNote](images/note-tags-example.PNG)


<a name="attributes"></a>
## <a name="note-tag-attributes"></a><span data-ttu-id="5151e-105">Atributos de etiqueta de nota</span><span class="sxs-lookup"><span data-stu-id="5151e-105">Note tag attributes</span></span>

<span data-ttu-id="5151e-106">En el HTML de una página de OneNote, una etiqueta de nota se representa mediante el atributo `data-tag`.</span><span class="sxs-lookup"><span data-stu-id="5151e-106">In the HTML of a onnvshort page, a note tag is represented by the data-tag attribute. For example:</span></span> <span data-ttu-id="5151e-107">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5151e-107">For example:</span></span>

- <span data-ttu-id="5151e-108">Un cuadro de tareas pendientes sin marcar: `<p data-tag="to-do">`</span><span class="sxs-lookup"><span data-stu-id="5151e-108">An unchecked to-do box:  <p data-tag="to-do">`<p data-tag="to-do">`</span></span> 
- <span data-ttu-id="5151e-109">Un cuadro de tareas pendientes marcado: `<p data-tag="to-do:completed">`</span><span class="sxs-lookup"><span data-stu-id="5151e-109">A checked to-do box:  <p data-tag="to-do:completed">`<p data-tag="to-do:completed">`</span></span> 
- <span data-ttu-id="5151e-110">Una estrella: `<h2 data-tag="important">`</span><span class="sxs-lookup"><span data-stu-id="5151e-110">A star:  `<h2 data-tag="important">`</span></span> 

<span data-ttu-id="5151e-111">Un valor `data-tag` se compone de una forma y, a veces, un estado.</span><span class="sxs-lookup"><span data-stu-id="5151e-111">A `data-tag` value is composed of a shape, and sometimes a status.</span></span> <span data-ttu-id="5151e-112">(*vea todos los [valores admitidos](#built-in-note-tags-for-onenote)*)</span><span class="sxs-lookup"><span data-stu-id="5151e-112">(*see all [supported values](#built-in-note-tags-for-onenote)*)</span></span>

| <span data-ttu-id="5151e-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5151e-113">Property</span></span> | <span data-ttu-id="5151e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5151e-114">Description</span></span> |  
|:------|:------|  
| <span data-ttu-id="5151e-115">shape</span><span class="sxs-lookup"><span data-stu-id="5151e-115">shape</span></span> | <span data-ttu-id="5151e-116">El identificador de la etiqueta de nota (ejemplo: `to-do` o `important`).</span><span class="sxs-lookup"><span data-stu-id="5151e-116">The identifier of the note tag (example: to-do`to-do` or important`important`).</span></span> |  
| <span data-ttu-id="5151e-117">status</span><span class="sxs-lookup"><span data-stu-id="5151e-117">status</span></span> | <span data-ttu-id="5151e-118">El estado de las etiquetas de nota de casillas.</span><span class="sxs-lookup"><span data-stu-id="5151e-118">The status of check-box note tags.</span></span> <span data-ttu-id="5151e-119">Se usa solo para establecer casillas como completadas.</span><span class="sxs-lookup"><span data-stu-id="5151e-119">The status of check-box note tags. This is used only to set check boxes as  completed.</span></span> |  
 

<a name="note-tags"></a>
## <a name="add-or-update-note-tags"></a><span data-ttu-id="5151e-120">Agregar o actualizar etiquetas de notas</span><span class="sxs-lookup"><span data-stu-id="5151e-120">Add or update note tags on onnvshort pages</span></span>

<span data-ttu-id="5151e-121">Para agregar o actualizar una etiqueta de nota integrada, use el atributo `data-tag` en un elemento compatible.</span><span class="sxs-lookup"><span data-stu-id="5151e-121">To add or update a built-in note tag, just use the `data-tag` attribute on a supported element.</span></span> <span data-ttu-id="5151e-122">Por ejemplo, este es un párrafo marcado como importante:</span><span class="sxs-lookup"><span data-stu-id="5151e-122">For example, here's a paragraph marked as important:</span></span>

```html
<p data-tag="important">...</p>
```

<span data-ttu-id="5151e-123">Separe las distintas etiquetas de notas mediante comas.</span><span class="sxs-lookup"><span data-stu-id="5151e-123">Separate multiple note tags with commas:</span></span>

```html
<p data-tag="important, critical">...</p>
```

<span data-ttu-id="5151e-124">Puede definir un `data-tag` en los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="5151e-124">You can define the data-tag attribute on  the following elements:</span></span>

- <span data-ttu-id="5151e-125">p</span><span class="sxs-lookup"><span data-stu-id="5151e-125">p</span></span> 
- <span data-ttu-id="5151e-126">ul, ol, li (*vea más información sobre [etiquetas de nota en listas](#note-tags-on-lists)*)</span><span class="sxs-lookup"><span data-stu-id="5151e-126">ul, ol, li (see more about lists)</span></span>
- <span data-ttu-id="5151e-127">img</span><span class="sxs-lookup"><span data-stu-id="5151e-127">img</span></span> 
- <span data-ttu-id="5151e-128">h1 - h6</span><span class="sxs-lookup"><span data-stu-id="5151e-128">h1 - h6</span></span> 
- <span data-ttu-id="5151e-129">title</span><span class="sxs-lookup"><span data-stu-id="5151e-129">title</span></span> 

<span data-ttu-id="5151e-130">Vea [Etiquetas de nota integradas](#built-in-note-tags-for-onenote) para obtener una lista de las etiquetas de nota que puede usar con Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="5151e-130">See Built-in note tags for OneNote for a list of note tags that you can use with the onnvshort API.</span></span> <span data-ttu-id="5151e-131">No es posible agregar o actualizar etiquetas personalizadas por medio de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="5151e-131">Adding or updating custom tags using the onnvshort API is not supported.</span></span>
 
<span data-ttu-id="5151e-132">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="5151e-132">**Examples**</span></span>

<span data-ttu-id="5151e-133">Aquí se muestra una lista de tareas pendientes simple con el primer elemento completado.</span><span class="sxs-lookup"><span data-stu-id="5151e-133">Here's a simple to-do list with the first item completed.</span></span>

```html 
<p data-tag="to-do:completed" data-id="prep">Till garden bed</p> 
<p data-tag="to-do" data-id="spring">Plant peas and spinach</p>
<p data-tag="to-do" data-id="summer">Plant tomatoes and peppers</p>
```

<span data-ttu-id="5151e-134">Tenga en cuenta que las etiquetas `<p>` anteriores incluyen cada una un atributo `data-id`.</span><span class="sxs-lookup"><span data-stu-id="5151e-134">Note that the `<p>` tags above each include a `data-id` attribute.</span></span> <span data-ttu-id="5151e-135">Esto simplifica la actualización de las etiquetas de nota de casilla.</span><span class="sxs-lookup"><span data-stu-id="5151e-135">This makes it easier to update the check-box note tags.</span></span> <span data-ttu-id="5151e-136">Por ejemplo, la solicitud siguiente marca el elemento de tarea pendiente de plantación de primavera como completado.</span><span class="sxs-lookup"><span data-stu-id="5151e-136">For example, the following request marks the spring planting to-do item as completed.</span></span>

``` 
PATCH https://graph.microsoft.com/v1.0/me/onenote/notebooks/pages/{page-id}/content

Content-Type: application/json
Authorization: Bearer {token}

[
   {
    'target':'#spring',
    'action':'replace',
    'content':'<p data-tag="to-do:completed"  data-id="spring">Plant peas and spinach</p>'
  }
]
```

<span data-ttu-id="5151e-137">La siguiente solicitud crea una página que contiene todas las [etiquetas de nota integradas](#built-in-note-tags-for-onenote).</span><span class="sxs-lookup"><span data-stu-id="5151e-137">The following request creates a page that contains all built-in note tags.</span></span>

``` 
POST https://graph.microsoft.com/v1.0/me/onenote/notebooks/pages

Content-Type: text/html
Authorization: Bearer {token}


<!DOCTYPE html>
<html>
  <head>
    <title data-tag="to-do:completed">All built-in note tags</title>
  </head>
  <body>
    <h1 data-tag="important">Paragraphs with built-in note tags</h1>
    <p data-tag="to-do">to-do</p>
    <p data-tag="important">important</p>
    <p data-tag="question">question</p>
    <p data-tag="definition">definition</p>
    <p data-tag="highlight">highlight</p>
    <p data-tag="contact">contact</p>
    <p data-tag="address">address</p>
    <p data-tag="phone-number">phone-number</p>
    <p data-tag="web-site-to-visit">web-site-to-visit</p>
    <p data-tag="idea">idea</p>
    <p data-tag="password">password</p>
    <p data-tag="critical">critical</p>
    <p data-tag="project-a">project-a</p>
    <p data-tag="project-b">project-b</p>
    <p data-tag="remember-for-later">remember-for-later</p>
    <p data-tag="movie-to-see">movie-to-see</p>
    <p data-tag="book-to-read">book-to-read</p>
    <p data-tag="music-to-listen-to">music-to-listen-to</p>
    <p data-tag="source-for-article">source-for-article</p>
    <p data-tag="remember-for-blog">remember-for-blog</p>
    <p data-tag="discuss-with-person-a">discuss-with-person-a</p>
    <p data-tag="discuss-with-person-b">discuss-with-person-b</p>
    <p data-tag="discuss-with-manager">discuss-with-manager</p>
    <p data-tag="send-in-email">send-in-email</p>
    <p data-tag="schedule-meeting">schedule-meeting</p>
    <p data-tag="call-back">call-back</p>
    <p data-tag="to-do-priority-1">to-do-priority-1</p>
    <p data-tag="to-do-priority-2">to-do-priority-2</p>
    <p data-tag="client-request">client-request</p>
    <h1 data-tag="important">Paragraphs with check boxes marked with "completed" status</h1>
    <p data-tag="to-do:completed">to-do:completed</p>
    <p data-tag="discuss-with-person-a:completed">discuss-with-person-a:completed</p>
    <p data-tag="discuss-with-person-b:completed">discuss-with-person-b:completed</p>
    <p data-tag="discuss-with-manager:completed">discuss-with-manager:completed</p>
    <p data-tag="schedule-meeting:completed">schedule-meeting:completed</p>
    <p data-tag="call-back:completed">call-back:completed</p>
    <p data-tag="to-do-priority-1:completed">to-do-priority-1:completed</p>
    <p data-tag="to-do-priority-2:completed">to-do-priority-2:completed</p>
    <p data-tag="client-request:completed">client-request:completed</p>
    <h1 data-tag="important">Multiple note tags</h1>
    <p data-tag="project-a,  client-request:completed">Two note tags:  project-a, client-request:completed</p>
    <p data-tag="idea, send-in-email, question">Three note tags:  idea, send-in-email, question</p>
    <h1 data-tag="important">Using note tags with other elements</h1>
    <p><b>Note tag on a list item:</b></p>
    <ul>
      <li data-tag="to-do-priority-1:completed">Make a to-do list</li>
    </ul>
    <p><b>Note tag on an image:</b></p>
    <img data-tag="source-for-article" src="http://placecorgi.com/200" />
    <p><b>Note tag with embedded style:</b></p>
    <p data-tag="important">Next time, <b>don't</b> forget to invite <span style="background-color:yellow">Dan</span>.</p>
  </body>
</html>
``` 

<span data-ttu-id="5151e-138">Para obtener más información sobre la creación de páginas, consulte [Crear páginas de OneNote](onenote-create-page.md).</span><span class="sxs-lookup"><span data-stu-id="5151e-138">For more information about creating pages, see [Create OneNote pages](onenote-create-page.md).</span></span> <span data-ttu-id="5151e-139">Para obtener más información sobre actualizar páginas, consulte [Actualizar páginas de OneNote](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="5151e-139">For more about updating pages, see [Update OneNote pages](onenote_update_page.md).</span></span>


<a name="note-tags-lists"></a>
### <a name="note-tags-on-lists"></a><span data-ttu-id="5151e-140">Las etiquetas de nota en listas</span><span class="sxs-lookup"><span data-stu-id="5151e-140">Note tags on lists</span></span>

<span data-ttu-id="5151e-141">Aquí encontrará algunas directrices para trabajar con etiquetas de nota en listas:</span><span class="sxs-lookup"><span data-stu-id="5151e-141">Here are some guidelines for working with note tags on lists:</span></span>

- <span data-ttu-id="5151e-142">Use elementos `p` para las listas de tareas pendientes.</span><span class="sxs-lookup"><span data-stu-id="5151e-142">Use `p` elements for to-do lists.</span></span> <span data-ttu-id="5151e-143">No muestran viñetas ni números, y son más fáciles de actualizar.</span><span class="sxs-lookup"><span data-stu-id="5151e-143">Use p elements for to-do lists. They don't display a bullet or number, and they're easier to update.</span></span>

- <span data-ttu-id="5151e-144">Para crear o actualizar listas que muestren la **misma** etiqueta de nota para todos los elementos de la lista:</span><span class="sxs-lookup"><span data-stu-id="5151e-144">To create or update ul or ol elements that display the **same**  note tag for all list items:</span></span>
  
   <p id="indent"><span data-ttu-id="5151e-145">Defina la `data-tag` en el `ul` u `ol`.</span><span class="sxs-lookup"><span data-stu-id="5151e-145">Define `data-tag` on the `ul` or `ol`.</span></span> <span data-ttu-id="5151e-146">Para actualizar la lista completa, tendrá que volver a definir la `data-tag` en el `ul` u `ol`.</span><span class="sxs-lookup"><span data-stu-id="5151e-146">Define data-tag`data-tag` on the ul`ul` or ol`ol`. To update the entire list, you'll need to redefine  data-tag on the ul or ol.</span></span></p>

- <span data-ttu-id="5151e-147">Para crear o actualizar listas que muestren etiquetas de nota **únicas** para algunos o todos los elementos de la lista:</span><span class="sxs-lookup"><span data-stu-id="5151e-147">To create or update ul or ol elements that display the **same**  note tag for all list items:</span></span>
  
   <p id="indent"><span data-ttu-id="5151e-148">Defina `data-tag` en elementos `li` y no anide los elementos `li` en una `ul` o `ol`.</span><span class="sxs-lookup"><span data-stu-id="5151e-148">Define `data-tag` on `li` elements, and don't nest the `li` elements in a `ul` or `ol`.</span></span> <span data-ttu-id="5151e-149">Para actualizar la lista completa, tendrá que quitar el `ul` que se devuelve en el HTML de salida y proporcionar solo los elementos `li` anidados.</span><span class="sxs-lookup"><span data-stu-id="5151e-149">To update the entire list, you'll need to remove the `ul` that's returned in the output HTML and provide only the unnested `li` elements.</span></span></p>

- <span data-ttu-id="5151e-150">Para actualizar elementos `li` concretos:</span><span class="sxs-lookup"><span data-stu-id="5151e-150">To update specific li`li` elements:</span></span>

   <p id="indent"><span data-ttu-id="5151e-151">Ponga como objetivo los elementos `li` por separado y defina la `data-tag` en el elemento `li`.</span><span class="sxs-lookup"><span data-stu-id="5151e-151">Target the `li` elements individually and define the `data-tag` on the `li` element.</span></span> <span data-ttu-id="5151e-152">Cualquier elemento `li` individualmente dirigido puede actualizarse para mostrar una etiqueta de nota única, independientemente de cómo se haya definido la lista originalmente.</span><span class="sxs-lookup"><span data-stu-id="5151e-152">Any individually addressed `li` element can be updated to display a unique note tag, no matter how the list was originally defined.</span></span></p>

<span data-ttu-id="5151e-153">Las instrucciones se basan en las siguientes reglas aplicadas por Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="5151e-153">The guidelines are based on the following rules that are applied by Microsoft Graph:</span></span>

- <span data-ttu-id="5151e-154">La configuración `data-tag` para un `ul` u `ol` invalida todas las configuraciones de elementos `li` secundarios.</span><span class="sxs-lookup"><span data-stu-id="5151e-154">The `data-tag` setting for a `ul` or `ol` overrides all settings on child `li` elements.</span></span> <span data-ttu-id="5151e-155">Esto se aplica incluso cuando el `ul` u `ol` no especifica un `data-tag` pero sí lo hacen sus elementos `li` secundarios.</span><span class="sxs-lookup"><span data-stu-id="5151e-155">The data-tag`ul` setting for a ul`ol` or ol`data-tag` overrides all settings on child li`li` elements. This applies even when the ul or ol doesn't specify a data-tag but its child li elements do.</span></span>

   <span data-ttu-id="5151e-156">Por ejemplo, si crea un `ul` u `ol` que define `data-tag="project-a"`, todos los elementos de la lista mostrarán la etiqueta de nota *Proyecto A*.</span><span class="sxs-lookup"><span data-stu-id="5151e-156">For example, if you create a `ul` or `ol` that defines `data-tag="project-a"`, all its list items will display the *Project A* note tag.</span></span> <span data-ttu-id="5151e-157">O si la `ul` u `ol` no define una `data-tag`, ninguno de los elementos mostrará una etiqueta de nota.</span><span class="sxs-lookup"><span data-stu-id="5151e-157">Or if the `ul` or `ol` doesn't define a `data-tag`, none of its items will display a note tag.</span></span> <span data-ttu-id="5151e-158">Esta invalidación ocurre independientemente de la configuración explícita de elementos `li` secundarios.</span><span class="sxs-lookup"><span data-stu-id="5151e-158">This override happens regardless of any explicit settings on child `li` elements.</span></span>

- <span data-ttu-id="5151e-159">Los valores de `data-tag` únicos se tienen en cuenta en elementos de lista cuando se dan las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="5151e-159">Unique data-tag`data-tag` settings are honored for list items under the following conditions:</span></span>

   - <span data-ttu-id="5151e-160">En una solicitud de creación o actualización, los elementos `li` no están anidados en un `ul` u `ol`.</span><span class="sxs-lookup"><span data-stu-id="5151e-160">The li`li` elements are not nested in a ul`ul` or ol`ol` in a create or update request (see example below).</span></span>

   - <span data-ttu-id="5151e-161">Un elemento `li` se trata individualmente en una solicitud de actualización.</span><span class="sxs-lookup"><span data-stu-id="5151e-161">An li`li` element is individually addressed in an update request.</span></span>

- <span data-ttu-id="5151e-162">Los elementos `li` sin anidar enviados en el HTML de entrada se devuelven en un `ul` en el HTML de salida.</span><span class="sxs-lookup"><span data-stu-id="5151e-162">Unnested li`li` elements sent in input HTML are returned in a ul`ul` in the output HTML (see example below).</span></span>

- <span data-ttu-id="5151e-163">En el HTML de salida, todos las opciones de configuración de la lista `data-tag` se definen en elementos `span` de la lista de elementos.</span><span class="sxs-lookup"><span data-stu-id="5151e-163">In output HTML, all `data-tag` list settings are defined on `span` elements on the list items.</span></span>

<br />
<span data-ttu-id="5151e-164">El siguiente código muestra cómo se aplican algunas de estas reglas.</span><span class="sxs-lookup"><span data-stu-id="5151e-164">The following code shows how some of these rules are applied.</span></span> <span data-ttu-id="5151e-165">El HTML de entrada crea dos listas con etiquetas.</span><span class="sxs-lookup"><span data-stu-id="5151e-165">The input HTML creates two lists with note tags.</span></span> <span data-ttu-id="5151e-166">El HTML de salida es lo que se devuelve para las listas cuando se recupera el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="5151e-166">The output HTML is what's returned for the lists when you retrieve page content.</span></span>

<span data-ttu-id="5151e-167">**HTML de entrada**</span><span class="sxs-lookup"><span data-stu-id="5151e-167">**Input HTML**</span></span>

```html 
<!--To display the same note tag on all list items, define note tags on the ul or ol.--> 
<ul data-tag="project-a" data-id="agenda">
  <li>An item with a Project A note tag</li>
  <li>An item with a Project A note tag</li>
</ul>

<!--To display unique note tags on list items, don't nest li elements in a ul or ol.--> 
<li data-tag="idea" data-id="my-idea">An item with an Idea note tag</li>
<li data-tag="question" data-id="my-question">An item with a Question note tag</li>
```
 
<span data-ttu-id="5151e-168">**HTML de salida**</span><span class="sxs-lookup"><span data-stu-id="5151e-168">**Output HTML**</span></span>

```html 
<ul>
  <li><span data-tag="project-a">An item with a Project A note tag</span></li>
  <li><span data-tag="project-a">An item with a Project A note tag</span></li>
</ul>
<br />
<ul>
  <li style="..."><span data-tag="idea">An item with an Idea note tag</span></li>
  <li style="..."><span data-tag="question">An item with a Question note tag</span></li>
</ul>
```

<a name="output-html"></a>
## <a name="retrieve-note-tags"></a><span data-ttu-id="5151e-169">Recuperar etiquetas de nota</span><span class="sxs-lookup"><span data-stu-id="5151e-169">Retrieve note tags</span></span>

<span data-ttu-id="5151e-170">Las etiquetas de nota integradas se incluyen en el HTML de salida cuando obtiene el contenido de página:</span><span class="sxs-lookup"><span data-stu-id="5151e-170">Built-in note tags are included in the output HTML when you retrieve page content by sending a GET request to the content endpoint:</span></span>

`GET ../api/v1.0/pages/{page-id}/content` 

<span data-ttu-id="5151e-171">Un atributo `data-tag` en el HTML de salida incluye siempre un valor de forma y solo incluye el estado si representa una etiqueta de nota de casilla establecida en completada.</span><span class="sxs-lookup"><span data-stu-id="5151e-171">The data-tag attribute in the output HTML always includes the shape value, and it only includes  status if it represents a check-box note tag that's  set to completed. The following examples show the input HTML used to create some note tags and the output HTML that's returned.</span></span> <span data-ttu-id="5151e-172">Los siguientes ejemplos muestran el HTML de salida utilizado para crear algunas etiquetas de nota y el HTML de salida que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="5151e-172">The following examples show the input HTML used to create some note tags and the output HTML that's returned.</span></span>

<span data-ttu-id="5151e-173">**HTML de entrada**</span><span class="sxs-lookup"><span data-stu-id="5151e-173">**Input HTML**</span></span>

```html 
<h1>Status meeting</h1>
<p data-tag="important">Next week's meeting has been moved to <b>Wednesday</b>.</p>
<p data-tag="question">What are the exact dates for the conference?</p>
<p>Upcoming training opportunities. See Katie for more info.</p>
<p data-tag="project-a">Around the room updates.</p>
<ul data-tag="critical">
  <li>Design handouts</li>
  <li>Plan keynote</li>
</ul>
```

<span data-ttu-id="5151e-174">**HTML de salida**</span><span class="sxs-lookup"><span data-stu-id="5151e-174">**Output HTML**</span></span>

```html 
<h1 style="...">Status meeting</h1>
<p data-tag="important">Next week's meeting has been moved to <span style="font-weight:bold">Wednesday</span>.</p>
<p data-tag="question">What are the exact dates for the conference?</p>
<p>Upcoming training opportunities. See Katie for more info.</p>
<p data-tag="project-a">Around the room updates.</p>
<ul>
  <li><span data-tag="critical">Design handouts</span></li>
  <li><span data-tag="critical">Plan keynote</span></li>
</ul>
```

<span data-ttu-id="5151e-175">Tenga en cuenta que el atributo `data-tag` definido en el nivel de lista se inserta en los elementos de lista.</span><span class="sxs-lookup"><span data-stu-id="5151e-175">Note that the data-tag`data-tag` attribute defined at the list level is pushed to its list items. For more information about using note tags with lists, see Note tags on lists.</span></span> <span data-ttu-id="5151e-176">Para obtener más información sobre el uso de etiquetas con listas, consulte [Etiquetas de nota en listas](#note-tags-on-lists).</span><span class="sxs-lookup"><span data-stu-id="5151e-176">Note that the data-tag attribute defined at the list level is pushed to its list items. For more information about using note tags with lists, see [Note tags on lists](#note-tags-on-lists).</span></span>

> <span data-ttu-id="5151e-177">**Nota:** en el HTML de salida, las etiquetas definición y notas de recordatorio se devuelven como `data-tag="remember-for-later"`.</span><span class="sxs-lookup"><span data-stu-id="5151e-177">**Note:** In the output HTML, the definition and remember-for-later note tags are both returned as `data-tag="remember-for-later"`.</span></span> <span data-ttu-id="5151e-178">El elemento `title` no devuelve información de etiqueta de nota.</span><span class="sxs-lookup"><span data-stu-id="5151e-178">element doesn't return any note tag information.</span></span>

<a name="built-in-tags"></a>
## <a name="built-in-note-tags-for-onenote"></a><span data-ttu-id="5151e-179">Etiquetas de nota integradas para OneNote</span><span class="sxs-lookup"><span data-stu-id="5151e-179">Built-in note tags for onnvshort</span></span>

<span data-ttu-id="5151e-180">OneNote contiene las siguientes etiquetas de nota integradas:</span><span class="sxs-lookup"><span data-stu-id="5151e-180">onnvshort  includes the following built-in  note tags:</span></span>

![Todas las etiquetas de nota integradas.](images/note-tags-all.png)

<span data-ttu-id="5151e-182">Los valores que puede asignar al atributo `data-tag` se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="5151e-182">The values you can assign to the data-tag`data-tag` attribute are shown below.</span></span> <span data-ttu-id="5151e-183">No se admiten etiquetas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="5151e-183">Custom tags are not supported.</span></span>

||<span data-ttu-id="5151e-184">Etiquetas</span><span class="sxs-lookup"><span data-stu-id="5151e-184">Tags</span></span>||
|:---|:---|:-----|
| `shape[:status]` |`to-do`<br />`to-do:completed`|`important`|
|`question`|`definition`|`highlight`|
|`contact`|`address`|`phone-number`|
|`web-site-to-visit`|`idea`|`password`|
|`critical`|`project-a`|`project-b`|
|`remember-for-later`|`movie-to-see`|`book-to-read`|
|`music-to-listen-to`|`source-for-article`|`remember-for-blog`|
|`discuss-with-person-a`<br />`discuss-with-person-a:completed`|`discuss-with-person-b`<br />`discuss-with-person-b:completed`|`discuss-with-manager`<br />`discuss-with-manager:completed`|
|`send-in-email`|`schedule-meeting`<br />`schedule-meeting:completed`|`call-back`<br />`call-back:completed`|
|`to-do-priority-1`<br />`to-do-priority-1:completed`|`to-do-priority-2`<br />`to-do-priority-2:completed`|`client-request`<br />`client-request:completed`|


<a name="request-response-info"></a>
## <a name="response-information"></a><span data-ttu-id="5151e-185">Información de respuesta</span><span class="sxs-lookup"><span data-stu-id="5151e-185">Response information</span></span>
<span data-ttu-id="5151e-186">Microsoft Graph proporciona la siguiente información en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5151e-186">The onnvshort API returns the following information in the response.</span></span>

| <span data-ttu-id="5151e-187">Datos de respuesta</span><span class="sxs-lookup"><span data-stu-id="5151e-187">Response data</span></span> | <span data-ttu-id="5151e-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="5151e-188">Description</span></span> |  
|------|------|  
| <span data-ttu-id="5151e-189">Código correcto</span><span class="sxs-lookup"><span data-stu-id="5151e-189">Success code</span></span> | <span data-ttu-id="5151e-190">Un código de estado HTTP 201 para una solicitud POST correcta y un código de estado HTTP 204 para una solicitud PATCH correcta.</span><span class="sxs-lookup"><span data-stu-id="5151e-190">A 201 HTTP status code for a successful POST request, and a 204 HTTP status code for a successful PATCH request.</span></span> |  
| <span data-ttu-id="5151e-191">Errores</span><span class="sxs-lookup"><span data-stu-id="5151e-191">Errors</span></span> | <span data-ttu-id="5151e-192">Lea [Códigos de error para API de OneNote de Microsoft Graph](onenote_error_codes.md) para obtener información sobre los errores de OneNote que puede devolver Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="5151e-192">Read [Error codes for OneNote APIs in Microsoft Graph](onenote_error_codes.md) to learn about OneNote errors that Microsoft Graph can return.</span></span> |  


<a name="permissions"></a>
## <a name="permissions"></a><span data-ttu-id="5151e-193">Permisos</span><span class="sxs-lookup"><span data-stu-id="5151e-193">Permissions</span></span>

<span data-ttu-id="5151e-194">Para crear o actualizar páginas OneNote, debe solicitar los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="5151e-194">To create or update OneNote pages, you'll need to request appropriate permissions.</span></span> <span data-ttu-id="5151e-195">Elija el nivel más bajo de permisos que necesita la aplicación para hacer su trabajo.</span><span class="sxs-lookup"><span data-stu-id="5151e-195">Choose the lowest level of permissions that your app needs to do its work.</span></span>

<span data-ttu-id="5151e-196">**Permisos de _páginas POST_**</span><span class="sxs-lookup"><span data-stu-id="5151e-196">**Permissions for _POST pages_**</span></span>

- <span data-ttu-id="5151e-197">Notes.Create</span><span class="sxs-lookup"><span data-stu-id="5151e-197">Notes.Create</span></span>
- <span data-ttu-id="5151e-198">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5151e-198">Notes.ReadWrite</span></span>
- <span data-ttu-id="5151e-199">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5151e-199">Notes.ReadWrite.All</span></span>  

<span data-ttu-id="5151e-200">**Permisos de _páginas PATCH_**</span><span class="sxs-lookup"><span data-stu-id="5151e-200">**Permissions for _PATCH pages_**</span></span>

- <span data-ttu-id="5151e-201">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5151e-201">Notes.ReadWrite</span></span>
- <span data-ttu-id="5151e-202">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5151e-202">Notes.ReadWrite.All</span></span>  

<span data-ttu-id="5151e-203">Para obtener más información sobre los ámbitos de permiso y cómo funcionan, consulte los [ámbitos de permisos de OneNote](permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5151e-203">For more information about how permission scopes work, see [OneNote permission scopes](permissions_reference.md).</span></span>


<a name="see-also"></a>
## <a name="additional-resources"></a><span data-ttu-id="5151e-204">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5151e-204">Additional resources</span></span>

- [<span data-ttu-id="5151e-205">Crear páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="5151e-205">Create OneNote pages</span></span>](onenote-create-page.md)
- [<span data-ttu-id="5151e-206">Actualizar el contenido de la página de OneNote</span><span class="sxs-lookup"><span data-stu-id="5151e-206">Update OneNote page content</span></span>](onenote_update_page.md)
- [<span data-ttu-id="5151e-207">Integración con OneNote</span><span class="sxs-lookup"><span data-stu-id="5151e-207">Integrate with OneNote</span></span>](integrate_with_onenote.md)
- [<span data-ttu-id="5151e-208">Blog para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="5151e-208">OneNote Developer Blog</span></span>](http://go.microsoft.com/fwlink/?LinkID=390183)
- [<span data-ttu-id="5151e-209">Preguntas de desarrollo de OneNote en Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="5151e-209">OneNote development questions on Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkID=390182)
- [<span data-ttu-id="5151e-210">Repositorios de OneNote en GitHub</span><span class="sxs-lookup"><span data-stu-id="5151e-210">OneNote GitHub repos</span></span>](http://go.microsoft.com/fwlink/?LinkID=390178)  
 


