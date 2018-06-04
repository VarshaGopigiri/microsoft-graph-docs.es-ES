# <a name="use-onenote-api-div-tags-to-extract-data-from-captures"></a><span data-ttu-id="e17f2-101">Usar etiquetas div de la API de OneNote para extraer datos de capturas</span><span class="sxs-lookup"><span data-stu-id="e17f2-101">Use OneNote API div tags to extract data from captures</span></span> 

<span data-ttu-id="e17f2-102">*__Se aplica a:__ Blocs de notas para consumidores de OneDrive | Blocs de notas empresariales de Office 365*</span><span class="sxs-lookup"><span data-stu-id="e17f2-102">*__Applies to:__ Consumer notebooks on OneDrive | Enterprise notebooks on Office 365*</span></span>

<span data-ttu-id="e17f2-103">Use la API de OneNote para extraer datos de tarjetas de presentación de imágenes, o bien datos de recetas y productos de URL.</span><span class="sxs-lookup"><span data-stu-id="e17f2-103">Use the OneNote API to extract business card data from an image, or recipe and product data from a URL.</span></span>

<a name="attributes"></a>
## <a name="extraction-attributes"></a><span data-ttu-id="e17f2-104">Atributos de extracción</span><span class="sxs-lookup"><span data-stu-id="e17f2-104">Extraction attributes</span></span>

<span data-ttu-id="e17f2-105">Para extraer y transformar datos, solo tiene que incluir un div que especifique el contenido de origen, el método de extracción y el comportamiento de reserva en la solicitud [create-page](onenote-create-page.md) o [update-page](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="e17f2-105">To extract and transform data, simply include a div that specifies the source content, extraction method, and fallback behavior in your [create-page](onenote-create-page.md) or [update-page](onenote_update_page.md) request.</span></span> <span data-ttu-id="e17f2-106">La API representa los datos extraídos de la página en un formato de fácil lectura.</span><span class="sxs-lookup"><span data-stu-id="e17f2-106">The API renders extracted data on the page in an easy-to-read format.</span></span> 

```
<div
  data-render-src="image-or-url"
  data-render-method="extraction-method"
  data-render-fallback="fallback-action">
</div>
```

<span data-ttu-id="e17f2-107">**data-render-src**</span><span class="sxs-lookup"><span data-stu-id="e17f2-107">**data-render-src**</span></span>

<span data-ttu-id="e17f2-108">El origen de contenido.</span><span class="sxs-lookup"><span data-stu-id="e17f2-108">The content source.</span></span> <span data-ttu-id="e17f2-109">Puede ser una imagen de una tarjeta de presentación, o bien una URL absoluta de sitios web populares de productos o recetas.</span><span class="sxs-lookup"><span data-stu-id="e17f2-109">This can be an image of a business card or an absolute URL from many popular recipe or product websites.</span></span> <span data-ttu-id="e17f2-110">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e17f2-110">Required.</span></span>

<span data-ttu-id="e17f2-111">Para obtener los mejores resultados al especificar una dirección URL, use la URL canónica definida en el HTML de la página web de origen, si se define una.</span><span class="sxs-lookup"><span data-stu-id="e17f2-111">For best results when sending a URL, use the canonical URL defined in the  HTML of the source webpage, if one is defined. Example: <link rel="canonical" href="www.domainname.com/page/123/size12/type987" />.</span></span> <span data-ttu-id="e17f2-112">Por ejemplo, se puede definir una URL canónica en la página web de origen de esta forma:</span><span class="sxs-lookup"><span data-stu-id="e17f2-112">For example, a canonical URL might be defined in the source webpage like this:</span></span>

`<link rel="canonical" href="www.domainname.com/page/123/size12/type987" />` 


<span data-ttu-id="e17f2-113">**data-render-method**</span><span class="sxs-lookup"><span data-stu-id="e17f2-113">**data-render-method**</span></span>

<span data-ttu-id="e17f2-114">El método de extracción que se ejecutará.</span><span class="sxs-lookup"><span data-stu-id="e17f2-114">The extraction method to run:</span></span> <span data-ttu-id="e17f2-115">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e17f2-115">Required.</span></span>

| <span data-ttu-id="e17f2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e17f2-116">Value</span></span> | <span data-ttu-id="e17f2-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e17f2-117">Description</span></span> |
|:------|:------|
| <span data-ttu-id="e17f2-118">extract.businesscard</span><span class="sxs-lookup"><span data-stu-id="e17f2-118">extract.businesscard</span></span> | <span data-ttu-id="e17f2-119">Una extracción de tarjetas de presentación.</span><span class="sxs-lookup"><span data-stu-id="e17f2-119">A business card extraction.</span></span> |
| <span data-ttu-id="e17f2-120">extract.recipe</span><span class="sxs-lookup"><span data-stu-id="e17f2-120">extract.recipe</span></span> | <span data-ttu-id="e17f2-121">Una extracción de recetas.</span><span class="sxs-lookup"><span data-stu-id="e17f2-121">A recipe extraction.</span></span> |
| <span data-ttu-id="e17f2-122">extract.product</span><span class="sxs-lookup"><span data-stu-id="e17f2-122">extract.product</span></span> | <span data-ttu-id="e17f2-123">Una extracción de listas de productos.</span><span class="sxs-lookup"><span data-stu-id="e17f2-123">A product listing extraction.</span></span> |
| <span data-ttu-id="e17f2-124">extract</span><span class="sxs-lookup"><span data-stu-id="e17f2-124">Extract</span></span> | <span data-ttu-id="e17f2-125">Un tipo de extracción desconocido.</span><span class="sxs-lookup"><span data-stu-id="e17f2-125">An unknown extraction type.</span></span> |

<span data-ttu-id="e17f2-126">Para obtener los mejores resultados, especifique el tipo de contenido (`extract.businesscard`, `extract.recipe` o `extract.product`) si lo conoce.</span><span class="sxs-lookup"><span data-stu-id="e17f2-126">For best results, specify the content type (`extract.businesscard`, `extract.recipe`, or `extract.product`) if you know it.</span></span> <span data-ttu-id="e17f2-127">Si el tipo es desconocido, use el método `extract` y la API de OneNote para intentar detectar automáticamente el tipo.</span><span class="sxs-lookup"><span data-stu-id="e17f2-127">For best results, specify the content type (business card, recipe, or product) if you know it. If  the type is unknown, you can use the extract method and the onnvshort API will try to auto-detect the type.</span></span>

<span data-ttu-id="e17f2-128">**data-render-fallback**</span><span class="sxs-lookup"><span data-stu-id="e17f2-128">**data-render-fallback**</span></span>

<span data-ttu-id="e17f2-129">El comportamiento de reserva si hay un error de extracción.</span><span class="sxs-lookup"><span data-stu-id="e17f2-129">The fallback behavior if the extraction fails:</span></span> <span data-ttu-id="e17f2-130">Si se omite, se establece de forma predeterminada como **render**.</span><span class="sxs-lookup"><span data-stu-id="e17f2-130">Defaults to **render** if omitted.</span></span> 

| <span data-ttu-id="e17f2-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e17f2-131">Value</span></span> | <span data-ttu-id="e17f2-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e17f2-132">Description</span></span> |
|:------|:------|
| <span data-ttu-id="e17f2-133">render</span><span class="sxs-lookup"><span data-stu-id="e17f2-133">render()</span></span> | <span data-ttu-id="e17f2-134">Representa la imagen de origen o una instantánea de la página web del producto o la receta.</span><span class="sxs-lookup"><span data-stu-id="e17f2-134">Renders the source image or a snapshot of the recipe or product webpage.</span></span> |
| <span data-ttu-id="e17f2-135">none</span><span class="sxs-lookup"><span data-stu-id="e17f2-135">none</span></span> | <span data-ttu-id="e17f2-136">No realiza ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="e17f2-136">Does nothing.</span></span><br /><span data-ttu-id="e17f2-137">Esta opción es útil si siempre quiere incluir una instantánea de la tarjeta de presentación o la página web en la página, además del contenido extraído.</span><span class="sxs-lookup"><span data-stu-id="e17f2-137">Does nothing. This option is useful if you want to always include a snapshot of the business card or webpage on  the page in addition to any extracted content. Be sure to send a separate img element in the request.</span></span> <span data-ttu-id="e17f2-138">Asegúrese de enviar un elemento `img` separado en la solicitud, como se muestra en los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="e17f2-138">Be sure to send a separate `img` element in the request, as shown in the examples.</span></span> |

<a name="biz-card"></a>
## <a name="business-card-extractions"></a><span data-ttu-id="e17f2-139">Extracciones de tarjetas de presentación</span><span class="sxs-lookup"><span data-stu-id="e17f2-139">Business card extractions</span></span>

<span data-ttu-id="e17f2-140">La API de OneNote intenta encontrar y presentar la siguiente información de contacto según la imagen de la tarjeta de presentación de una persona o una empresa.</span><span class="sxs-lookup"><span data-stu-id="e17f2-140">The onnvshort API tries to find and  render the following contact information  based on an image of a person's or company's business card.</span></span>


- <span data-ttu-id="e17f2-141">Nombre</span><span class="sxs-lookup"><span data-stu-id="e17f2-141">Name</span></span>
- <span data-ttu-id="e17f2-142">El título</span><span class="sxs-lookup"><span data-stu-id="e17f2-142">Title</span></span>
- <span data-ttu-id="e17f2-143">Organización</span><span class="sxs-lookup"><span data-stu-id="e17f2-143">Organization</span></span>
- <span data-ttu-id="e17f2-144">Números de teléfono y fax</span><span class="sxs-lookup"><span data-stu-id="e17f2-144">Phone and fax numbers</span></span>
- <span data-ttu-id="e17f2-145">Direcciones de correo y físicas</span><span class="sxs-lookup"><span data-stu-id="e17f2-145">Mailing and physical addresses</span></span>
- <span data-ttu-id="e17f2-146">Direcciones de correo</span><span class="sxs-lookup"><span data-stu-id="e17f2-146">Email addresses</span></span>
- <span data-ttu-id="e17f2-147">Sitios web</span><span class="sxs-lookup"><span data-stu-id="e17f2-147">Websites</span></span>
   
  ![Un ejemplo de extracción de tarjetas de presentación.](images/biz-card-extraction.png)

<span data-ttu-id="e17f2-149">En la página, también se inserta una vCard (archivo .VCF) con la información del contacto extraída.</span><span class="sxs-lookup"><span data-stu-id="e17f2-149">A vCard (.VCF file) with the extracted contact information is also embedded in the page. The vCard is a convenient way to get the contact information when retrieving page HTML content.</span></span> <span data-ttu-id="e17f2-150">Una vCard es una forma útil de obtener la información de contacto al recuperar el contenido HTML de una página.</span><span class="sxs-lookup"><span data-stu-id="e17f2-150">A vCard (.VCF file) with the extracted contact information is also embedded in the page. The vCard is a convenient way to get the contact information when retrieving page HTML content.</span></span>

### <a name="common-scenarios-for-business-card-extractions"></a><span data-ttu-id="e17f2-151">Escenarios comunes de extracciones de tarjetas de presentación</span><span class="sxs-lookup"><span data-stu-id="e17f2-151">Common scenarios for business card extractions</span></span>

<span data-ttu-id="e17f2-152">**Extraer información de tarjetas de presentación y, además, representar la imagen de la tarjeta de presentación**</span><span class="sxs-lookup"><span data-stu-id="e17f2-152">**Extract business card information, and also render the business card image**</span></span>

<span data-ttu-id="e17f2-153">Especifique el método `extract.businesscard` y la reserva `none`.</span><span class="sxs-lookup"><span data-stu-id="e17f2-153">Specify the `extract.businesscard` method and the `none` fallback.</span></span> <span data-ttu-id="e17f2-154">Además, envíe un elemento `img` con el atributo `src` que también haga referencia la imagen.</span><span class="sxs-lookup"><span data-stu-id="e17f2-154">Also send an `img` element with the `src` attribute that also references the image.</span></span> <span data-ttu-id="e17f2-155">Si la API no puede extraer ningún contenido, solo representará la imagen de la tarjeta de presentación.</span><span class="sxs-lookup"><span data-stu-id="e17f2-155">If the API is unable to extract any content, it renders the business card image only.</span></span>

```html 
<div
    data-render-src="name:scanned-card-image"
    data-render-method="extract.businesscard"
    data-render-fallback="none">
</div>
<img src="name:scanned-card-image" />
```


<span data-ttu-id="e17f2-156">**Extraer información de tarjetas de presentación y solo representar la imagen de la tarjeta de presentación si la extracción produce errores**</span><span class="sxs-lookup"><span data-stu-id="e17f2-156">**Extract business card information, and render the business card image only if the extraction fails**</span></span>

<span data-ttu-id="e17f2-157">Especifique el método `extract.businesscard` y use la reserva `render` predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e17f2-157">Specify the `extract.businesscard` method and use the default `render` fallback.</span></span> <span data-ttu-id="e17f2-158">Si la API no puede extraer ningún contenido, solo representará la imagen de la tarjeta de presentación en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e17f2-158">If the API is unable to extract any content, it renders the business card image instead.</span></span>

```html
<div
    data-render-src="name:scanned-card-image"
    data-render-method="extract.businesscard">
</div>
```
 
<span data-ttu-id="e17f2-159">Para extracciones de tarjetas de presentación, la imagen se envía como un elemento con nombre en una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="e17f2-159">For business card extractions, the image is sent as a named part in a multipart request.</span></span> <span data-ttu-id="e17f2-160">Vea [Agregar imágenes y archivos](onenote_images_files.md) para obtener ejemplos de cómo enviar una imagen en una solicitud.</span><span class="sxs-lookup"><span data-stu-id="e17f2-160">See Capture photos and images  for examples that show how to send an image in a create-page request.</span></span>


<a name="recipe"></a>
## <a name="recipe-extractions"></a><span data-ttu-id="e17f2-161">Extracciones de recetas</span><span class="sxs-lookup"><span data-stu-id="e17f2-161">Recipe extractions</span></span>

<span data-ttu-id="e17f2-162">La API de OneNote intenta buscar y procesar la siguiente información según la dirección URL de una receta.</span><span class="sxs-lookup"><span data-stu-id="e17f2-162">The onnvshort API tries to find and  render the following information based on a recipe's URL.</span></span>

- <span data-ttu-id="e17f2-163">Imagen principal</span><span class="sxs-lookup"><span data-stu-id="e17f2-163">Hero image</span></span>
- <span data-ttu-id="e17f2-164">Clasificación</span><span class="sxs-lookup"><span data-stu-id="e17f2-164">Rating</span></span>
- <span data-ttu-id="e17f2-165">Ingredientes</span><span class="sxs-lookup"><span data-stu-id="e17f2-165">Ingredients</span></span>
- <span data-ttu-id="e17f2-166">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="e17f2-166">Instructions</span></span>
- <span data-ttu-id="e17f2-167">Preparación, cocción, tiempo total</span><span class="sxs-lookup"><span data-stu-id="e17f2-167">Prep, cook, and total times</span></span>
- <span data-ttu-id="e17f2-168">Raciones</span><span class="sxs-lookup"><span data-stu-id="e17f2-168">Servings</span></span>

   ![Un ejemplo de extracción de recetas](images/recipe-extraction.png)

<span data-ttu-id="e17f2-170">La API está optimizada para recetas de sitios populares, como *Allrecipes.com*, *FoodNetwork.com* y *SeriousEats.com*.</span><span class="sxs-lookup"><span data-stu-id="e17f2-170">The API is optimized for recipes from many popular sites such as Allrecipes.com, FoodNetwork.com, and SeriousEats.com.</span></span>

### <a name="common-scenarios-for-recipe-extractions"></a><span data-ttu-id="e17f2-171">Escenarios comunes de extracciones de recetas</span><span class="sxs-lookup"><span data-stu-id="e17f2-171">Common scenarios for recipe extractions</span></span>

<span data-ttu-id="e17f2-172">**Extraer información de la receta y, además, mostrar una instantánea de la página web de la receta**</span><span class="sxs-lookup"><span data-stu-id="e17f2-172">**Extract recipe information, and also render a snapshot of the recipe webpage**</span></span>

<span data-ttu-id="e17f2-173">Especifique el método `extract.recipe` y la reserva `none`.</span><span class="sxs-lookup"><span data-stu-id="e17f2-173">Specify the `extract.recipe` method and the `none` fallback.</span></span> <span data-ttu-id="e17f2-174">Además, envía un elemento `img` con el atributo `data-render-src` establecido en la URL de la receta.</span><span class="sxs-lookup"><span data-stu-id="e17f2-174">Also send an `img` element with the `data-render-src` attribute set to the recipe URL.</span></span> <span data-ttu-id="e17f2-175">Si la API no puede extraer ningún contenido, solo mostrará una instantánea de la página web de la receta.</span><span class="sxs-lookup"><span data-stu-id="e17f2-175">If the API is unable to extract any content, it renders a snapshot of the recipe webpage only.</span></span>

<span data-ttu-id="e17f2-176">Este escenario proporciona potencialmente la mayor cantidad de información posible, ya que la página web puede contener información adicional, como sugerencias y opiniones de clientes.</span><span class="sxs-lookup"><span data-stu-id="e17f2-176">This scenario potentially provides the most information because the webpage may include additional information, such as customer reviews and suggestions.</span></span>

```html 
<div
    data-render-src="http://allrecipes.com/recipe/guacamole/"
    data-render-method="extract.recipe"
    data-render-fallback="none">
</div>
<img data-render-src="http://allrecipes.com/recipe/guacamole/" />
```
 

<span data-ttu-id="e17f2-177">**Extraer información de la receta y solo mostrar una instantánea de la página web de la receta si la extracción produce errores**</span><span class="sxs-lookup"><span data-stu-id="e17f2-177">**Extract recipe information, and render a snapshot of the recipe webpage only if the extraction fails**</span></span>

<span data-ttu-id="e17f2-178">Especifique el método `extract.recipe` y use la reserva de representación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e17f2-178">Specify the `extract.recipe` method and use the default render fallback.</span></span> <span data-ttu-id="e17f2-179">Si la API no puede extraer ningún contenido, solo mostrará una instantánea de la página web de la receta en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e17f2-179">If the API is unable to extract any content, it renders a snapshot of the recipe webpage instead.</span></span>

```html  
<div
    data-render-src="http://www.foodnetwork.com/recipes/alton-brown/creme-brulee-recipe.html"
    data-render-method="extract.recipe">
</div>
```


<span data-ttu-id="e17f2-180">**Extraer la información de la receta y, además, mostrar un vínculo la receta**</span><span class="sxs-lookup"><span data-stu-id="e17f2-180">**Extract recipe information, and also render a link to the recipe**</span></span>

<span data-ttu-id="e17f2-181">Especifique el método `extract.recipe` y la reserva `none`.</span><span class="sxs-lookup"><span data-stu-id="e17f2-181">Specify the `extract.recipe` method and the `none` fallback.</span></span> <span data-ttu-id="e17f2-182">Además, envía un elemento `a` con el atributo `src` establecido en la URL de la receta (o bien, puede enviar cualquier otra información que quiera agregar a la página).</span><span class="sxs-lookup"><span data-stu-id="e17f2-182">Extract recipe information, and also render  a link to the recipeSpecify the extract.recipe`a` method and the none`src` fallback. Also send an a element with the src  attribute set to the recipe URL (or you can send any other information you want to add to the page). If the API is unable to extract any content, only the recipe link is rendered.</span></span> <span data-ttu-id="e17f2-183">Si la API no puede extraer ningún contenido, solo se mostrará el vínculo de la receta.</span><span class="sxs-lookup"><span data-stu-id="e17f2-183">If the API is unable to extract any content, only the recipe link is rendered.</span></span>

```html  
<div
    data-render-src="http://www.seriouseats.com/recipes/2014/09/diy-spicy-kimchi-beef-instant-noodles-recipe.html"
    data-render-method="extract.recipe"
    data-render-fallback="none">
</div>
<a href="http://www.seriouseats.com/recipes/2014/09/diy-spicy-kimchi-beef-instant-noodles-recipe.html">Recipe URL</a>
``` 


<a name="product"></a>
## <a name="product-listing-extractions"></a><span data-ttu-id="e17f2-184">Extracciones de listas de productos</span><span class="sxs-lookup"><span data-stu-id="e17f2-184">Product listing extractions</span></span>

- <span data-ttu-id="e17f2-185">El título</span><span class="sxs-lookup"><span data-stu-id="e17f2-185">Title</span></span>
- <span data-ttu-id="e17f2-186">Clasificación</span><span class="sxs-lookup"><span data-stu-id="e17f2-186">Rating</span></span>
- <span data-ttu-id="e17f2-187">Imagen principal</span><span class="sxs-lookup"><span data-stu-id="e17f2-187">Primary image</span></span>
- <span data-ttu-id="e17f2-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="e17f2-188">Description</span></span>
- <span data-ttu-id="e17f2-189">Características</span><span class="sxs-lookup"><span data-stu-id="e17f2-189">Features</span></span>
- <span data-ttu-id="e17f2-190">Especificaciones</span><span class="sxs-lookup"><span data-stu-id="e17f2-190">Specifications</span></span></td>

  ![Un ejemplo de extracción de listas de productos.](images/product-extraction.png)

<span data-ttu-id="e17f2-192">La API está optimizada para productos de muchos sitios populares como *Amazon.com* y *HomeDepot.com*.</span><span class="sxs-lookup"><span data-stu-id="e17f2-192">The API is optimized for products from many popular sites such as Amazon.com, HomeDepot.com, and Sears.com.</span></span>

### <a name="common-scenarios-for-recipe-extractions"></a><span data-ttu-id="e17f2-193">Escenarios comunes de extracciones de recetas</span><span class="sxs-lookup"><span data-stu-id="e17f2-193">Common scenarios for recipe extractions</span></span>

<span data-ttu-id="e17f2-194">**Extraer información de productos y, además, mostrar una instantánea de la página web del producto**</span><span class="sxs-lookup"><span data-stu-id="e17f2-194">**Extract product information, and also render a snapshot of the product webpage**</span></span>

<span data-ttu-id="e17f2-195">Especifique el método `extract.product` y la reserva `none`.</span><span class="sxs-lookup"><span data-stu-id="e17f2-195">Specify the `extract.product` method and the `none` fallback.</span></span> <span data-ttu-id="e17f2-196">Además, envía un elemento `img` con el atributo `data-render-src` establecido en la URL del producto.</span><span class="sxs-lookup"><span data-stu-id="e17f2-196">Also send an `img` element with the `data-render-src` attribute set to the product URL.</span></span> <span data-ttu-id="e17f2-197">Si la API no puede extraer ningún contenido, solo mostrará una instantánea de la página web del producto.</span><span class="sxs-lookup"><span data-stu-id="e17f2-197">If the API is unable to extract any content, it renders a snapshot of the product webpage only.</span></span>

<span data-ttu-id="e17f2-198">Este escenario proporciona potencialmente la mayor cantidad de información posible, ya que la página web puede contener información adicional, como sugerencias y opiniones de clientes.</span><span class="sxs-lookup"><span data-stu-id="e17f2-198">This scenario potentially provides the most information because the webpage may include additional information, such as customer reviews and suggestions.</span></span>

```html 
<div
    data-render-src="http://www.amazon.com/Microsoft-Band-Small/dp/B00P2T2WVO"
    data-render-method="extract.product"
    data-render-fallback="none">
</div>
<img data-render-src="http://www.amazon.com/Microsoft-Band-Small/dp/B00P2T2WVO" />
```


<span data-ttu-id="e17f2-199">**Extraer información del producto y solo mostrar una instantánea de la página web del producto si la extracción produce errores**</span><span class="sxs-lookup"><span data-stu-id="e17f2-199">**Extract product information, and render a snapshot of the product webpage only if the extraction fails**</span></span>

<span data-ttu-id="e17f2-200">Especifique el método `extract.product` y use la reserva de representación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e17f2-200">Specify the `extract.product` method and use the default render fallback.</span></span> <span data-ttu-id="e17f2-201">Si la API no puede extraer ningún contenido, solo mostrará una instantánea de la página web del producto en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e17f2-201">If the API is unable to extract any content, it renders a snapshot of the product webpage instead.</span></span>

```html 
<div
    data-render-src="http://www.sears.com/craftsman-19hp-42-8221-turn-tight-174-hydrostatic-yard-tractor/p-07120381000P"
    data-render-method="extract.product">
</div>
```
 

<span data-ttu-id="e17f2-202">**Extraer la información del producto y, además, mostrar un vínculo al producto**</span><span class="sxs-lookup"><span data-stu-id="e17f2-202">**Extract product information, and also render a link to the product**</span></span>

<span data-ttu-id="e17f2-203">Especifique el método `extract.product` y la reserva `none`.</span><span class="sxs-lookup"><span data-stu-id="e17f2-203">Specify the `extract.product` method and the `none` fallback.</span></span> <span data-ttu-id="e17f2-204">Además, envía un elemento `a` con el atributo `src` establecido en la URL del producto (o bien, puede enviar cualquier otra información que quiera agregar a la página).</span><span class="sxs-lookup"><span data-stu-id="e17f2-204">Extract product information, and also render  a link to the productSpecify the extract.product`a` method and the none`src` fallback. Also send an a element with the src  attribute set to the product URL (or you can send any other information you want to add to the page). If the API is unable to extract any content, only the page link is rendered.</span></span> <span data-ttu-id="e17f2-205">Si la API no puede extraer ningún contenido, solo se mostrará el vínculo de la página.</span><span class="sxs-lookup"><span data-stu-id="e17f2-205">If the API is unable to extract any content, only the page link is rendered.</span></span>

```html 
<div
    data-render-src="http://www.homedepot.com/p/Active-Ventilation-5-Watt-Solar-Powered-Exhaust-Attic-Fan-RBSF-8-WT/204203001"
    data-render-method="extract.product"
    data-render-fallback="none">
</div>
<a href="http://www.homedepot.com/p/Active-Ventilation-5-Watt-Solar-Powered-Exhaust-Attic-Fan-RBSF-8-WT/204203001">Product URL</a>
```


<a name="unknown"></a> 
## <a name="unknown-content-type-extractions"></a><span data-ttu-id="e17f2-206">Extracciones de tipo de contenido desconocido</span><span class="sxs-lookup"><span data-stu-id="e17f2-206">Unknown content type extractions</span></span>

<span data-ttu-id="e17f2-207">Si no conoce el tipo de contenido (tarjeta de presentación, receta o producto) que quiere enviar, puede usar el método `extract` incompleto y dejar que la API de OneNote detecte el tipo automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e17f2-207">If you don't know the content type (business card, recipe, or product) that you're sending,   you can use the unqualified extract method and let the onnvshort API automatically detect the type. You might want to do this if your app sends different capture types.</span></span> <span data-ttu-id="e17f2-208">Puede hacer esto si la aplicación envía distintos tipos de captura.</span><span class="sxs-lookup"><span data-stu-id="e17f2-208">You might want to do this if your app sends different capture types.</span></span>

> <span data-ttu-id="e17f2-209">**Nota:** Si conoce el tipo de contenido que quiere enviar, necesita usar el método `extract.businesscard`, `extract.recipe` o `extract.product`.</span><span class="sxs-lookup"><span data-stu-id="e17f2-209">**Note:** If you do know the content type that you're sending, you should use the `extract.businesscard`, `extract.recipe`, or `extract.product` method.</span></span> <span data-ttu-id="e17f2-210">En algunos casos, esto puede permitirle optimizar los resultados de la extracción.</span><span class="sxs-lookup"><span data-stu-id="e17f2-210">In some cases, this can help to optimize the extraction results.</span></span>
 
### <a name="common-scenarios-for-unknown-extractions"></a><span data-ttu-id="e17f2-211">Escenarios comunes para extracciones desconocidas</span><span class="sxs-lookup"><span data-stu-id="e17f2-211">Common  scenarios for article extractions</span></span>

<span data-ttu-id="e17f2-212">**Enviar una imagen de una URL y, si la extracción produce errores, representar la imagen proporcionada o una instantánea de la página web**</span><span class="sxs-lookup"><span data-stu-id="e17f2-212">**Send an image or a URL, and render the supplied image or a snapshot of the webpage if the extraction fails**</span></span>

<span data-ttu-id="e17f2-213">Especifique el método `extract` para que la API detecte automáticamente el tipo de contenido y use la reserva de representación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e17f2-213">Specify the `extract` method so the API automatically detects the content type, and use the default render fallback.</span></span> <span data-ttu-id="e17f2-214">Si la API no puede extraer ningún contenido, en su lugar se mostrará la imagen proporcionada o una instantánea de la página web.</span><span class="sxs-lookup"><span data-stu-id="e17f2-214">If the API is unable to extract any content, it renders the supplied image or snapshot of the webpage instead.</span></span>

```html 
<div
    data-render-src="some image or url"
    data-render-method="extract">
</div>
```


<a name="request-response-info"></a>
## <a name="response-information"></a><span data-ttu-id="e17f2-215">Información de respuesta</span><span class="sxs-lookup"><span data-stu-id="e17f2-215">Response information</span></span>

| <span data-ttu-id="e17f2-216">Datos de respuesta</span><span class="sxs-lookup"><span data-stu-id="e17f2-216">Response data</span></span> | <span data-ttu-id="e17f2-217">Descripción</span><span class="sxs-lookup"><span data-stu-id="e17f2-217">Description</span></span> |  
|------|------|  
| <span data-ttu-id="e17f2-218">Código correcto</span><span class="sxs-lookup"><span data-stu-id="e17f2-218">Success code</span></span> | <span data-ttu-id="e17f2-219">Un código de estado HTTP 201 para una solicitud POST correcta y un código de estado HTTP 204 para una solicitud PATCH correcta.</span><span class="sxs-lookup"><span data-stu-id="e17f2-219">A 201 HTTP status code for a successful POST request, and a 204 HTTP status code for a successful PATCH request.</span></span> |  
| <span data-ttu-id="e17f2-220">Errores</span><span class="sxs-lookup"><span data-stu-id="e17f2-220">Errors</span></span>| <span data-ttu-id="e17f2-221">Para obtener información sobre los errores de OneNote que puede mostrar Microsoft Graph, vea [Códigos de error para las API de OneNote en Microsoft Graph](onenote_error_codes.md).</span><span class="sxs-lookup"><span data-stu-id="e17f2-221">Read [Error codes for OneNote APIs in Microsoft Graph](onenote_error_codes.md) to learn about OneNote errors that Microsoft Graph can return.</span></span> |  


<a name="permissions"></a>
## <a name="permissions"></a><span data-ttu-id="e17f2-222">Permisos</span><span class="sxs-lookup"><span data-stu-id="e17f2-222">Permissions</span></span>

<span data-ttu-id="e17f2-223">Para crear o actualizar páginas de OneNote, necesita solicitar los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="e17f2-223">To create or update OneNote pages, you'll need to request appropriate permissions.</span></span> <span data-ttu-id="e17f2-224">Seleccione el nivel inferior de permisos que necesita la aplicación para funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="e17f2-224">Choose the lowest level of permissions that your app needs to do its work.</span></span>

<span data-ttu-id="e17f2-225">**Permisos para _PUBLICAR páginas_**</span><span class="sxs-lookup"><span data-stu-id="e17f2-225">**Permissions for _POST pages_**</span></span>

- <span data-ttu-id="e17f2-226">Notes.Create</span><span class="sxs-lookup"><span data-stu-id="e17f2-226">Notes.Create</span></span>
- <span data-ttu-id="e17f2-227">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e17f2-227">Notes.ReadWrite</span></span>
- <span data-ttu-id="e17f2-228">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e17f2-228">Notes.ReadWrite.All</span></span>  

<span data-ttu-id="e17f2-229">**Permisos para _APLICAR REVISIONES de páginas_**</span><span class="sxs-lookup"><span data-stu-id="e17f2-229">**Permissions for _PATCH pages_**</span></span>

- <span data-ttu-id="e17f2-230">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e17f2-230">Notes.ReadWrite</span></span>
- <span data-ttu-id="e17f2-231">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e17f2-231">Notes.ReadWrite.All</span></span>

<span data-ttu-id="e17f2-232">Para obtener más información sobre los ámbitos de permiso y cómo funcionan, vea [Referencias de permisos de Microsoft Graph](permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e17f2-232">For more information about permission scopes and how they work, see [Microsoft Graph permissions reference](permissions_reference.md).</span></span>


<a name="see-also"></a>
## <a name="additional-resources"></a><span data-ttu-id="e17f2-233">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e17f2-233">Additional resources</span></span>

- [<span data-ttu-id="e17f2-234">Crear páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="e17f2-234">Create OneNote pages</span></span>](onenote-create-page.md)
- [<span data-ttu-id="e17f2-235">Actualizar el contenido de la página de OneNote</span><span class="sxs-lookup"><span data-stu-id="e17f2-235">Update OneNote page content</span></span>](onenote_update_page.md)
- [<span data-ttu-id="e17f2-236">Agregar imágenes y archivos</span><span class="sxs-lookup"><span data-stu-id="e17f2-236">Add images and files</span></span>](onenote_images_files.md)
- [<span data-ttu-id="e17f2-237">Integración con OneNote</span><span class="sxs-lookup"><span data-stu-id="e17f2-237">Integrate with OneNote</span></span>](integrate_with_onenote.md)
- [<span data-ttu-id="e17f2-238">Blog para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="e17f2-238">OneNote Developer Blog</span></span>](http://go.microsoft.com/fwlink/?LinkID=390183)
- [<span data-ttu-id="e17f2-239">Preguntas de desarrollo de OneNote en Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="e17f2-239">OneNote development questions on Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkID=390182)
- [<span data-ttu-id="e17f2-240">Repositorios de OneNote en GitHub</span><span class="sxs-lookup"><span data-stu-id="e17f2-240">OneNote GitHub repos</span></span>](http://go.microsoft.com/fwlink/?LinkID=390178)  

