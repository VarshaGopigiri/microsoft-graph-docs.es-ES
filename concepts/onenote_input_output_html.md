# <a name="input-and-output-html-in-onenote-pages"></a><span data-ttu-id="2c2b0-101">HTML de entrada y salida en páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="2c2b0-101">Input and output HTML in OneNote pages</span></span>

<span data-ttu-id="2c2b0-102">El código HTML que define el contenido y la estructura de la página cuando [crea](onenote-create-page.md) o [actualiza](onenote_update_page.md) una página de OneNote se llama *HTML de entrada*.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-102">The HTML that defines the page content and structure when you [create](onenote-create-page.md) or [update](onenote_update_page.md) a OneNote page is called *input HTML*.</span></span> 

<span data-ttu-id="2c2b0-103">El código HTML que se devuelve cuando [,obtiene el contenido de la página](onenote-get-content.md) se denomina *HTML de salida*.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-103">The HTML that's returned when you [get page content](onenote-get-content.md) is called *output HTML*.</span></span> <span data-ttu-id="2c2b0-104">El HTML de salida no será el mismo que el de entrada.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-104">Output HTML won't be the same as input HTML.</span></span>

<span data-ttu-id="2c2b0-105">Las API de OneNote en Microsoft Graph conservan el contenido semántico y la estructura básica del HTML de entrada, pero la convierten en un conjunto de [elementos HTML y propiedades CSS compatibles](onenote-create-page.md#supported-html-and-css-for-onenote-pages).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-105">The OneNote APIs in Microsoft Graph preserve the semantic content and basic structure of the input HTML, but convert it to a set of [supported HTML elements and CSS properties](onenote-create-page.md#supported-html-and-css-for-onenote-pages).</span></span> <span data-ttu-id="2c2b0-106">Las API también agregan atributos personalizados que admiten las características de OneNote.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-106">The APIs also add custom attributes that support OneNote features.</span></span>
 
<span data-ttu-id="2c2b0-107">Este artículo describe los principales elementos y atributos del HTML de entrada y de salida.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-107">This article describes the principal elements and attributes of input and output HTML.</span></span> <span data-ttu-id="2c2b0-108">Puede ser útil comprender el HTML de entrada cuando crea o actualiza el contenido de la página, y el HTML de salida cuando analiza el contenido de la página devuelto.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-108">It can be helpful to understand input HTML when you're creating or updating page content, and output HTML when you're parsing returned page content.</span></span> 

## <a name="body-element"></a><span data-ttu-id="2c2b0-109">Elemento body</span><span class="sxs-lookup"><span data-stu-id="2c2b0-109">Body element</span></span>

<span data-ttu-id="2c2b0-110">El contenido HTML en el cuerpo de la página representa el contenido y la estructura de la página, incluidos los recursos de imagen y archivo.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-110">The HTML content in the page body represents the page content and structure, including image and file resources.</span></span> <span data-ttu-id="2c2b0-111">El elemento **body** puede contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-111">The **body** element can contain the following attributes in the input and output HTML.</span></span>

#### <a name="input-attributes"></a><span data-ttu-id="2c2b0-112">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-112">Input attributes</span></span>

|<span data-ttu-id="2c2b0-113">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-113">Input attribute</span></span>|<span data-ttu-id="2c2b0-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-114">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-115">data-absolute-enabled</span><span class="sxs-lookup"><span data-stu-id="2c2b0-115">data-absolute-enabled</span></span> | <span data-ttu-id="2c2b0-116">Indica si el cuerpo de entrada admite los elementos [con posición absoluta](onenote-abs-pos.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-116">Indicates whether the input body supports [absolute positioned](onenote-abs-pos.md) elements.</span></span> |
| <span data-ttu-id="2c2b0-117">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-117">style</span></span> | <p><span data-ttu-id="2c2b0-118">Las propiedades CSS [style](#styles) del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-118">The CSS [style](#styles) properties of the body.</span></span> <span data-ttu-id="2c2b0-119">En el HTML de salida, la configuración de entrada podría devolverse insertada en los elementos secundarios adecuados.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-119">In the output HTML, input settings might be returned inline on appropriate child elements.</span></span></p><p><span data-ttu-id="2c2b0-120">Actualmente, el color de fondo no es compatible con el elemento **body**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-120">Background color is not currently supported for the **body** element.</span></span></p> |
 

#### <a name="output-attributes"></a><span data-ttu-id="2c2b0-121">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-121">Output attributes</span></span>

|<span data-ttu-id="2c2b0-122">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-122">Output attribute</span></span>|<span data-ttu-id="2c2b0-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-123">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-124">data-absolute-enabled</span><span class="sxs-lookup"><span data-stu-id="2c2b0-124">data-absolute-enabled</span></span> | <span data-ttu-id="2c2b0-125">Indica si el cuerpo admite los elementos [con posición absoluta](onenote-abs-pos.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-125">Indicates whether the body supports [absolute positioned](onenote-abs-pos.md) elements.</span></span> <span data-ttu-id="2c2b0-126">Siempre **true** en el HTML de salida.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-126">Always **true** in output HTML.</span></span> |
| <span data-ttu-id="2c2b0-127">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-127">style</span></span> | <span data-ttu-id="2c2b0-128">Las propiedades **font-family** y **font-size** del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-128">The **font-family** and **font-size** properties of the body.</span></span> |


## <a name="div-elements"></a><span data-ttu-id="2c2b0-129">Elementos div</span><span class="sxs-lookup"><span data-stu-id="2c2b0-129">Div elements</span></span>

<span data-ttu-id="2c2b0-130">Los elementos **div** contienen texto, imágenes y otro contenido.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-130">**Div** elements contain text, images, and other content.</span></span> <span data-ttu-id="2c2b0-131">Los elementos **div** pueden contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-131">A **div** element can contain the following attributes in the input and output HTML.</span></span>

#### <a name="input-attributes"></a><span data-ttu-id="2c2b0-132">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-132">Input attributes</span></span>

|<span data-ttu-id="2c2b0-133">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-133">Input attribute</span></span>|<span data-ttu-id="2c2b0-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-134">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-135">data-id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-135">data-id</span></span> | <span data-ttu-id="2c2b0-136">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-136">A reference for the element.</span></span><br/><br/><span data-ttu-id="2c2b0-137">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-137">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-138">data-render-fallback</span><span class="sxs-lookup"><span data-stu-id="2c2b0-138">data-render-fallback</span></span> | <span data-ttu-id="2c2b0-139">La acción de reserva si la [extracción](onenote-extract-data.md) produce error: **render** (predeterminado) o **none**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-139">The fallback action if the [extraction](onenote-extract-data.md) fails: **render** (default) or **none**.</span></span> |
| <span data-ttu-id="2c2b0-140">data-render-method</span><span class="sxs-lookup"><span data-stu-id="2c2b0-140">data-render-method</span></span> | <span data-ttu-id="2c2b0-141">El método de [extracción](onenote-extract-data.md) para realizar, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2c2b0-141">The [extraction](onenote-extract-data.md) method to perform, for example:  or .</span></span><br/><span data-ttu-id="2c2b0-142">`extract.businesscard` o `extract.recipe`</span><span class="sxs-lookup"><span data-stu-id="2c2b0-142">`extract.businesscard` or `extract.recipe`</span></span> |
| <span data-ttu-id="2c2b0-143">data-render-src</span><span class="sxs-lookup"><span data-stu-id="2c2b0-143">data-render-src</span></span> | <span data-ttu-id="2c2b0-144">El origen del contenido para la [extracción](onenote-extract-data.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-144">The content source for the [extraction](onenote-extract-data.md).</span></span> |
| <span data-ttu-id="2c2b0-145">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-145">style</span></span> | <span data-ttu-id="2c2b0-146">Las propiedades de posición, tamaño, fuente y color del elemento div:</span><span class="sxs-lookup"><span data-stu-id="2c2b0-146">The position, size, font, and color properties for the div:</span></span> <ul><li><span data-ttu-id="2c2b0-147">**position** (solo **absolute**), **left**, **top** y **width** (la propiedad height se configura automáticamente para los elementos div)</span><span class="sxs-lookup"><span data-stu-id="2c2b0-147">**position** (**absolute** only), **left**, **top**, and **width** (height is auto-configured for divs)</span></span><br/><br/><span data-ttu-id="2c2b0-148">Se usa para crear un elemento div [con posición absoluta](onenote-abs-pos.md), solo si el elemento div es un elemento secundario directo del cuerpo cuando el cuerpo indica `data-absolute-enabled="true"`.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-148">Used to create an [absolute positioned](onenote-abs-pos.md) div, only if the div is a direct child of the body when the body sets `data-absolute-enabled="true"`.</span></span><br/><br/><span data-ttu-id="2c2b0-149">Ejemplo: `<div style="position:absolute;width:360px;top:350px;left:300px" ... />`</span><span class="sxs-lookup"><span data-stu-id="2c2b0-149">Example: `<div style="position:absolute;width:360px;top:350px;left:300px" ... />`</span></span></li><li><span data-ttu-id="2c2b0-p108">Las propiedades CSS [style](#styles) del elemento. En el HTML de salida, estos valores se devuelven integrados en los elementos secundarios correspondientes.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-p108">The CSS [style](#styles) properties of the element. In the output HTML, these values are returned inline on appropriate child elements.</span></span></li></ul> |
 

<span data-ttu-id="2c2b0-152">Las API de OneNote en Microsoft Graph encapsulan todo el contenido del cuerpo en al menos un elemento div.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-152">The OneNote APIs in Microsoft Graph wrap all body content in at least one div.</span></span> <span data-ttu-id="2c2b0-153">La API crea un div predeterminado (con atributos `data-id="_default"`) para contener el contenido del cuerpo si:</span><span class="sxs-lookup"><span data-stu-id="2c2b0-153">The API creates a default div (attributed with `data-id="_default"`) to contain the body content if:</span></span>

- <span data-ttu-id="2c2b0-154">El atributo **data-absolute-enabled** del elemento de entrada del cuerpo se omite o se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-154">The input body element's **data-absolute-enabled** attribute is omitted or set to **false**.</span></span> <span data-ttu-id="2c2b0-155">En este caso, se coloca todo el contenido del cuerpo en el div predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-155">In this case, all body content is put in the default div.</span></span>

- <span data-ttu-id="2c2b0-156">El atributo **data-absolute-enabled** del elemento de entrada del cuerpo es **true**, pero el HTML de entrada contiene elementos secundarios directos que no son elementos [con posición absoluta](onenote-abs-pos.md)&nbsp;**div**, **img** u **object**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-156">The input body element's **data-absolute-enabled** attribute is **true**, but the input HTML contains direct children that aren't [absolute positioned](onenote-abs-pos.md)&nbsp;**div**, **img**, or **object** elements.</span></span> <span data-ttu-id="2c2b0-157">En este caso, los elementos secundarios directos que no son elementos [con posición absoluta](onenote-abs-pos.md)&nbsp;**div**, **img** u **object** se colocan en el elemento div predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-157">In this case, direct children that aren't [absolute positioned](onenote-abs-pos.md)&nbsp;**div**, **img**, or **object** elements are put in the default div.</span></span>


#### <a name="output-attributes"></a><span data-ttu-id="2c2b0-158">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-158">Output attributes</span></span>

|<span data-ttu-id="2c2b0-159">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-159">Output attribute</span></span>|<span data-ttu-id="2c2b0-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-160">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-161">data-id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-161">data-id</span></span> | <span data-ttu-id="2c2b0-162">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-162">A reference for the element.</span></span><br/><br/><span data-ttu-id="2c2b0-163">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-163">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-164">id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-164">id</span></span> | <span data-ttu-id="2c2b0-165">Un identificador único, generado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-165">A unique, generated ID for the element.</span></span> <span data-ttu-id="2c2b0-166">Devuelto por [solicitudes GET al punto de conexión del *contenido* de una página](../api-reference/v1.0/api/page_get.md) cuando se usa la opción de consulta `includeIDs=true`.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-166">Returned by [GET requests to a page's *content* endpoint](../api-reference/v1.0/api/page_get.md) when the `includeIDs=true` query option is used.</span></span><br/><br/><span data-ttu-id="2c2b0-167">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-167">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-168">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-168">style</span></span> | <span data-ttu-id="2c2b0-169">Las propiedades de posición y tamaño del div.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-169">The position and size properties of the div.</span></span> |
 
### <a name="non-contributing-divs"></a><span data-ttu-id="2c2b0-170">Div que no contribuyen</span><span class="sxs-lookup"><span data-stu-id="2c2b0-170">Non-contributing divs</span></span>

<span data-ttu-id="2c2b0-171">Cuando un elemento **div** en el HTML de entrada no contribuye a la estructura de la página o lleva información que OneNote usa, la API mueve el contenido del div al div primario o predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-171">When a **div** element in the input HTML does not contribute to the page structure or carry information that OneNote uses, the API moves the div's content into the parent or default div.</span></span> <span data-ttu-id="2c2b0-172">Esto se ilustra en los siguientes ejemplos.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-172">This is illustrated in the following examples.</span></span>

#### <a name="input-html"></a><span data-ttu-id="2c2b0-173">HTML de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-173">Input HTML</span></span>

<span data-ttu-id="2c2b0-174">Contiene un elemento div anidado, que no contribuye.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-174">Contains a non-contributing, nested div.</span></span>

```html
<html>
    <head>
        <title>Page Title</title>
    </head>
    <body>
        <div>
            <p>Some text</p>
            <div>
                <p>More text inside a div that doesn't define page structure</p>
            </div>
        </div>
    </body>
</html>
```

#### <a name="output-html"></a><span data-ttu-id="2c2b0-175">HTML de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-175">Output HTML</span></span>

> <span data-ttu-id="2c2b0-176">**Nota**: El contenido del div se ha movido al elemento div principal, y se han eliminado las etiquetas `<div>` anidadas.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-176">**Note:** The div's content was moved to the parent div and the nested `<div>` tags have been removed.</span></span> <span data-ttu-id="2c2b0-177">El div se habría conservado si hubiera definido cualquier información semántica, como **data-id** (ejemplo: `<div data-id="keep-me">`).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-177">The div would have been preserved if it defined any semantic information, such as a **data-id** (example: `<div data-id="keep-me">`).</span></span>

```html
<html htmlns="http://www.w3.org/1999/xhtml" lang="en-US">
    <head>
        <title>Page Title</title>
    </head>
    <body data-absolute-enabled="true" style="font-family:Calibri;font-size:11px">
        <div data-id="_default" style="position:absolute;left:48px;top:120px;width:624px">
            <p>Some text</p>
            <p>More text inside a nested div</p>
        </div>
    </body>
</html>
```


## <a name="img-elements"></a><span data-ttu-id="2c2b0-178">Elementos img</span><span class="sxs-lookup"><span data-stu-id="2c2b0-178">Img elements</span></span>

<span data-ttu-id="2c2b0-179">Las imágenes en las páginas de OneNote están representadas por elementos **img**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-179">Images on OneNote pages are represented by **img** elements.</span></span> <span data-ttu-id="2c2b0-180">Un elemento **img** puede contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-180">An **img** element can contain the following attributes in the input and output HTML.</span></span>

#### <a name="input-attributes"></a><span data-ttu-id="2c2b0-181">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-181">Input attributes</span></span>

|<span data-ttu-id="2c2b0-182">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-182">Input attribute</span></span>|<span data-ttu-id="2c2b0-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-183">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-184">alt</span><span class="sxs-lookup"><span data-stu-id="2c2b0-184">alt</span></span> | <span data-ttu-id="2c2b0-185">El texto alternativo que se proporciona para la imagen.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-185">The supplied alt text for the image.</span></span> |
| <span data-ttu-id="2c2b0-186">data-id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-186">data-id</span></span> | <span data-ttu-id="2c2b0-187">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-187">A reference for the element.</span></span><br/><br/><span data-ttu-id="2c2b0-188">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-188">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-189">data-render-src</span><span class="sxs-lookup"><span data-stu-id="2c2b0-189">data-render-src</span></span> |<span data-ttu-id="2c2b0-190">Se necesita **data-render-src** o **src**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-190">Either **data-render-src** or **src** is required.</span></span><br/><br/><span data-ttu-id="2c2b0-191">La página web para representar como imagen como mapa de bits en la página de OneNote:</span><span class="sxs-lookup"><span data-stu-id="2c2b0-191">The webpage to render as a bit-mapped image on the OneNote page:</span></span><br/><br/> <span data-ttu-id="2c2b0-192">- `data-render-src="http://..."` para una dirección URL pública.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-192">- `data-render-src="http://..."` for a public URL.</span></span><br/><br/> <span data-ttu-id="2c2b0-193">- `data-render-src="name:BlockName"` para una parte de imagen en el bloque "Presentación" de una [solicitud de varias partes](../api-reference/v1.0/api/section_post_pages.md#example).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-193">- `data-render-src="name:BlockName"` for an image part in the "Presentation" block of a [multipart request](../api-reference/v1.0/api/section_post_pages.md#example).</span></span><br/><br/><span data-ttu-id="2c2b0-194">Este método es útil cuando la página web es más compleja que la página que OneNote puede representar fielmente, o cuando la página requiere credenciales de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-194">This method is useful when the webpage is more complex than the OneNote page can faithfully render, or when the page requires login credentials.</span></span>|
| <span data-ttu-id="2c2b0-195">etiqueta de datos</span><span class="sxs-lookup"><span data-stu-id="2c2b0-195">data-tag</span></span> | <span data-ttu-id="2c2b0-196">Una [etiqueta de nota](onenote-note-tags.md) en el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-196">A [note tag](onenote-note-tags.md) on the element.</span></span> |
| <span data-ttu-id="2c2b0-197">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-197">style</span></span> |<span data-ttu-id="2c2b0-198">Las propiedades de posición y tamaño de la imagen: **posición** (**absoluta** solo), **izquierda**, **arriba**, **ancho** y **alto**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-198">The position and size properties for the image: **position** (**absolute** only), **left**, **top**, **width**, and **height**.</span></span><br/><br/><span data-ttu-id="2c2b0-199">El tamaño se puede establecer en cualquier imagen.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-199">Size can be set on any image.</span></span><br/><br/><span data-ttu-id="2c2b0-200">Las propiedades de posición se usan para crear una imagen [con posición absoluta](onenote-abs-pos.md), solo si la imagen es un elemento secundario directo del cuerpo cuando el cuerpo indica `data-absolute-enabled="true"`.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-200">Position properties are used to create an [absolute positioned](onenote-abs-pos.md) image, only if the image is a direct child of the body when the body sets `data-absolute-enabled="true"`.</span></span><br/><br/><span data-ttu-id="2c2b0-201">Ejemplo: `<img style="position:absolute;width:360px;top:350px;left:300px" ... />`</span><span class="sxs-lookup"><span data-stu-id="2c2b0-201">Example: `<img style="position:absolute;width:360px;top:350px;left:300px" ... />`</span></span><br/><br/><span data-ttu-id="2c2b0-202">En el HTML de salida, el tamaño de la imagen se devuelve por separado en los atributos **width** y **height**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-202">In the output HTML, the image size is returned separately in **width** and **height** attributes.</span></span> |
| <span data-ttu-id="2c2b0-203">src</span><span class="sxs-lookup"><span data-stu-id="2c2b0-203">src</span></span> |<span data-ttu-id="2c2b0-204">Se necesita **src** o **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-204">Either **src** or **data-render-src** is required.</span></span><br/><br/><span data-ttu-id="2c2b0-205">La imagen para representar en la página de OneNote:</span><span class="sxs-lookup"><span data-stu-id="2c2b0-205">The image to render on the OneNote page:</span></span><br/><br/><span data-ttu-id="2c2b0-206">- `src="http://..."` para una dirección URL a una imagen disponible públicamente en Internet.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-206">- `src="http://..."` for a URL to a publicly available image on the internet.</span></span><br/><br/> <span data-ttu-id="2c2b0-207">- `src="name:BlockName"` para una parte con nombre en una solicitud con varias partes que representa a la imagen.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-207">- `src="name:BlockName"` for a named part in a multipart request that represents the image.</span></span>|
| <span data-ttu-id="2c2b0-208">ancho, alto</span><span class="sxs-lookup"><span data-stu-id="2c2b0-208">width, height</span></span> | <span data-ttu-id="2c2b0-209">El ancho o alto de la imagen, en píxeles pero sin px.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-209">The width or height of the image, in pixels but without the px.</span></span> <span data-ttu-id="2c2b0-210">Ejemplo: `width="400"`</span><span class="sxs-lookup"><span data-stu-id="2c2b0-210">Example: `width="400"`</span></span> |
 
> <span data-ttu-id="2c2b0-211">**Nota**: Las API de OneNote detectan automáticamente el tipo de imagen de entrada y lo devuelve como el **data-fullres-src-type** en el HTML de salida.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-211">**Note:** The OneNote APIs automatically detect the input image type, and returns it as the **data-fullres-src-type** in the output HTML.</span></span> <span data-ttu-id="2c2b0-212">La API también devuelve el tipo de imagen de la imagen optimizada en **data-src-type**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-212">The API also returns the image type of the optimized image in **data-src-type**.</span></span>
 

#### <a name="output-attributes"></a><span data-ttu-id="2c2b0-213">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-213">Output attributes</span></span>

|<span data-ttu-id="2c2b0-214">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-214">Output attribute</span></span>|<span data-ttu-id="2c2b0-215">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-215">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-216">alt</span><span class="sxs-lookup"><span data-stu-id="2c2b0-216">alt</span></span> | <span data-ttu-id="2c2b0-217">El texto alternativo que se proporciona para la imagen.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-217">The supplied alt text for the image.</span></span> |
| <span data-ttu-id="2c2b0-218">data-id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-218">data-id</span></span> | <span data-ttu-id="2c2b0-219">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-219">A reference for the element.</span></span><br/><br/><span data-ttu-id="2c2b0-220">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-220">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-221">data-index</span><span class="sxs-lookup"><span data-stu-id="2c2b0-221">data-index</span></span> | <span data-ttu-id="2c2b0-p118">La posición de la imagen. Para compatibilidad con [imagen dividida](#split-images).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-p118">The position of the image. For [split image](#split-images) support.</span></span> |
| <span data-ttu-id="2c2b0-224">data-fullres-src</span><span class="sxs-lookup"><span data-stu-id="2c2b0-224">data-fullres-src</span></span> | <span data-ttu-id="2c2b0-225">El extremo para la versión del recurso de la imagen que se incrustó originalmente en la página.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-225">The endpoint for the version of the image resource that was originally embedded in the page.</span></span> |
| <span data-ttu-id="2c2b0-226">data-fullres-src-type</span><span class="sxs-lookup"><span data-stu-id="2c2b0-226">data-fullres-src-type</span></span> | <span data-ttu-id="2c2b0-227">El tipo de medios del recurso **data-fullres-src**. Por ejemplo: `image/png` o `image/jpeg`.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-227">The media type of the **data-fullres-src** resource, for example: `image/png` or `image/jpeg`.</span></span> |
| <span data-ttu-id="2c2b0-228">data-options</span><span class="sxs-lookup"><span data-stu-id="2c2b0-228">data-options</span></span> | <span data-ttu-id="2c2b0-p119">El tipo de origen: **printout** para archivos PDF o **splitimage** para todos los demás. Se aplica únicamente a [imágenes divididas](#split-images) creadas con el atributo **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-p119">The source type: **printout** for PDF files or **splitimage** for all others. Applies only to [split images](#split-images) created with the **data-render-src** attribute.</span></span> |
| <span data-ttu-id="2c2b0-231">data-render-original-src</span><span class="sxs-lookup"><span data-stu-id="2c2b0-231">data-render-original-src</span></span> | <span data-ttu-id="2c2b0-232">La dirección URL de origen de la imagen, si la imagen de origen proviene de Internet pública y se creó con el atributo **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-232">The original source URL of the image, if the source image is from the public internet and was created with the **data-render-src** attribute.</span></span> |
| <span data-ttu-id="2c2b0-233">data-src-type</span><span class="sxs-lookup"><span data-stu-id="2c2b0-233">data-src-type</span></span> | <span data-ttu-id="2c2b0-234">El tipo de medios del recurso **src**. Por ejemplo: `image/png` o `image/jpeg`.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-234">The media type of the **src** resource, for example: `image/png` or `image/jpeg`.</span></span> |
| <span data-ttu-id="2c2b0-235">etiqueta de datos</span><span class="sxs-lookup"><span data-stu-id="2c2b0-235">data-tag</span></span> | <span data-ttu-id="2c2b0-236">Una [etiqueta de nota](onenote-note-tags.md) en el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-236">A [note tag](onenote-note-tags.md) on the element.</span></span> |
| <span data-ttu-id="2c2b0-237">id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-237">id</span></span> | <span data-ttu-id="2c2b0-238">Un identificador único, generado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-238">A unique, generated ID for the element.</span></span> <span data-ttu-id="2c2b0-239">Devuelto por [solicitudes GET al punto de conexión del *contenido* de una página](../api-reference/v1.0/api/page_get.md) cuando se usa la opción de consulta `includeIDs=true`.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-239">Returned by [GET requests to a page's *content* endpoint](../api-reference/v1.0/api/page_get.md) when the `includeIDs=true` query option is used.</span></span><br/><br/><span data-ttu-id="2c2b0-240">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-240">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-241">src</span><span class="sxs-lookup"><span data-stu-id="2c2b0-241">src</span></span> | <span data-ttu-id="2c2b0-242">El extremo para la versión del recurso de imagen que se ha optimizado para exploradores web y factores de forma móviles y de tabletas.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-242">The endpoint for the version of the image resource that has been optimized for web browsers and mobile and tablet form factors.</span></span> |
| <span data-ttu-id="2c2b0-243">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-243">style</span></span> | <span data-ttu-id="2c2b0-244">Las propiedades de posición de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-244">The position properties of the image.</span></span> |
| <span data-ttu-id="2c2b0-245">ancho, alto</span><span class="sxs-lookup"><span data-stu-id="2c2b0-245">width, height</span></span> | <span data-ttu-id="2c2b0-246">El ancho o alto de la imagen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-246">The width or height of the image, in pixels.</span></span> |
 

### <a name="output-html-examples-for-images"></a><span data-ttu-id="2c2b0-247">Ejemplos de HTML de salida para imágenes</span><span class="sxs-lookup"><span data-stu-id="2c2b0-247">Output HTML examples for images</span></span>

<span data-ttu-id="2c2b0-248">Los elementos **img** de salida contienen puntos de conexión para los recursos de archivo de imagen y el tipo de imagen, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-248">Output **img** elements contain endpoints for image file resources and the image type, as shown below.</span></span> <span data-ttu-id="2c2b0-249">Puede hacer [solicitudes GET independientes a puntos de conexión de recursos de imagen](../api-reference/v1.0/api/resource_get.md) para recuperar su contenido binario.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-249">You can make separate [GET requests to image resource endpoints](../api-reference/v1.0/api/resource_get.md) to retrieve their binary contents.</span></span>

```html
<img 
    src="https://graph.microsoft.com/v1.0/me/onenote/resources/{image-id}/$value"  
    data-src-type="image/png"
    data-fullres-src="https://graph.microsoft.com/v1.0/me/onenote/resources/{image-id}/$value"  
    data-fullres-src-type="image/png" ... />
```

<span data-ttu-id="2c2b0-250">De forma predeterminada, las imágenes no se representarán directamente en un explorador porque son privadas y se necesita una autorización para recuperarlas, al igual que el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-250">By default, images won't render directly in a browser because they are private and require authorization to retrieve them, like the rest of the page contents.</span></span> <span data-ttu-id="2c2b0-251">Para obtener direcciones URL públicas a los recursos de imagen en una página, incluya **preAuthenticated=true** en la cadena de consulta cuando recupere el contenido de la página (ejemplo: `GET ../pages/{page-id}/content?preAuthenticated=true`).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-251">To get public URLs to the image resources on a page, include **preAuthenticated=true** in the query string when you retrieve the page content (example: `GET ../pages/{page-id}/content?preAuthenticated=true`).</span></span> <span data-ttu-id="2c2b0-252">Las direcciones URL públicas que se devuelven son válidas durante una hora.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-252">The public URLs that are returned are valid for one hour.</span></span> 

#### <a name="image-with-public-url-when-preauthenticatedtrue-is-included-in-the-request"></a><span data-ttu-id="2c2b0-253">Imagen con dirección URL pública cuando se incluye _preAuthenticated=true_ en la solicitud</span><span class="sxs-lookup"><span data-stu-id="2c2b0-253">Image with public URL when _preAuthenticated=true_ is included in the request</span></span>

```html
<img 
    width="170" height="128" 
    src="https://graph.microsoft.com/v1.0/me/onenote/resources/{image-id}/content?publicAuth=true&mimeType=image/jpeg" 
    data-src-type="image/{type}" 
    data-fullres-src="https://graph.microsoft.com/v1.0/me/onenote/resources/{image-id}/content?publicAuth=true&mimeType=image/jpeg" 
    data-fullres-src-type="image/{type}"
/>
```

<span data-ttu-id="2c2b0-254">Los siguientes ejemplos muestran la información que un elemento **img** podría contener en el HTML de salida.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-254">The following examples show the information an **img** element might contain in the output HTML.</span></span>

#### <a name="image-with-web-ready-and-high-resolution-resources"></a><span data-ttu-id="2c2b0-255">Imagen con recursos de alta resolución y listos para la web</span><span class="sxs-lookup"><span data-stu-id="2c2b0-255">Image with web-ready and high resolution resources</span></span>

```html
<img
    src="{web-ready-image-resource-url}/$value"
    data-src-type="image/{type}"
    data-fullres-src="{high-resolution-image-resource-url}/$value"
    data-fullres-src-type="image/{type}"
    [data-render-original-src="{original-source-url-or-named-part}"]
    [data-id="{image-id}"]
    [alt="supplied alt text"]
    [width="345"] [height="180"]
    [style="..."] />
```

#### <a name="image-created-by-using-the-data-render-src-attribute"></a><span data-ttu-id="2c2b0-256">Imagen creada mediante el atributo *data-render-src*</span><span class="sxs-lookup"><span data-stu-id="2c2b0-256">Image created by using the *data-render-src* attribute</span></span>

```html
<img
    src="{web-ready-image-resource-url}/$value"
    data-src-type="image/{type}"
    data-fullres-src="{high-resolution-image-resource-url}/$value"
    data-fullres-src-type="image/{type}"
    data-render-original-src="{original-source-url-or-named-part}"
    [data-id="{image-id}"]
    [data-index="{index-of-split-image}"]
    [data-options="{printout-or-splitimage}"]
    [alt="supplied alt text"]
    [width="1024"] [height="1900"]
    [style="..."] />
```

### <a name="split-images"></a><span data-ttu-id="2c2b0-257">Imágenes divididas</span><span class="sxs-lookup"><span data-stu-id="2c2b0-257">Split images</span></span>

<span data-ttu-id="2c2b0-258">Las imágenes que se crean mediante el atributo **data-render-src** (de una dirección URL de una página web o una parte con nombre) podrían dividirse en varias componentes de imágenes por motivos de representación y de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-258">Images that are created using the **data-render-src** attribute (from a webpage URL or a named part) might be split into multiple component images for performance and rendering reasons.</span></span> <span data-ttu-id="2c2b0-259">A todos los componentes de imágenes se les asigna el mismo valor **data-id**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-259">Component images are all assigned the same **data-id** value.</span></span> <span data-ttu-id="2c2b0-260">Cada componente de imagen tiene un atributo de índice de datos de base cero que define el diseño vertical original.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-260">Each component image has a zero-based data-index attribute that defines the original vertical layout.</span></span>

#### <a name="split-image-with-three-component-images"></a><span data-ttu-id="2c2b0-261">Imagen dividida con tres imágenes con componente</span><span class="sxs-lookup"><span data-stu-id="2c2b0-261">Split image with three component images</span></span>

```html
<div data-id="multi-component-image" style="position:absolute;left:48px;top:120px;width:624px">
    <img
        src="{image-resource0-url}/$value"
        data-src-type="image/{type}"
        data-fullres-src="{image-resource0-url}/$value" 
        data-fullres-src-type="image/{type}" 
        data-index="0" 
        data-render-original-src="{original-source-url-or-named-part}"
        data-id="{same-image-id}" ... />
    <img 
        src="{image-resource1-url}/$value" 
        data-src-type="image/{type}" 
        data-fullres-src="{image-resource1-url}/$value" 
        data-fullres-src-type="image/{type}" 
        data-index="1" 
        data-render-original-src="{original-source-url-or-named-part}"
        data-id="{same-image-id}" ... />
    <img 
        src="{image-resource2-url}/$value" 
        data-src-type="image/{type}" 
        data-fullres-src="{image-resource2-url}/$value" 
        data-fullres-src-type="image/{type}" 
        data-index="2" 
        data-render-original-src=""{original-source-url-or-named-part}"
        data-id="{same-image-id}" ... />
</div>
```

<span data-ttu-id="2c2b0-262">Debido a que los usuarios pueden mover las imágenes en la página, los índices devueltos pueden estar desordenados.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-262">Because users can move the images on the page, the returned indexes might be out of order.</span></span> <span data-ttu-id="2c2b0-263">El orden debe estar en orden descendente en el eje y, y de izquierda a derecha en el eje x, si hay conflictos en el eje y.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-263">Ordering should be in top to bottom y-order, then left to right x-order if there are y-order conflicts.</span></span>

## <a name="iframe-elements"></a><span data-ttu-id="2c2b0-264">elementos iframe</span><span class="sxs-lookup"><span data-stu-id="2c2b0-264">iframe elements</span></span>

<span data-ttu-id="2c2b0-265">Las páginas de OneNote pueden contener vídeos insertados representados por elementos **iframe**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-265">OneNote pages can contain embedded videos represented by **iframe** elements.</span></span> 

> <span data-ttu-id="2c2b0-266">**Nota**: También puede [adjuntar un archivo de vídeo mediante un elemento **object**](onenote_images_files.md#adding-files).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-266">**Note:** You can also [attach a video file using an **object** element](onenote_images_files.md#adding-files).</span></span>

#### <a name="input-attributes"></a><span data-ttu-id="2c2b0-267">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-267">Input attributes</span></span>

|<span data-ttu-id="2c2b0-268">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-268">Input attribute</span></span>|<span data-ttu-id="2c2b0-269">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-269">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-270">Data-original-src</span><span class="sxs-lookup"><span data-stu-id="2c2b0-270">data-original-src</span></span> | <span data-ttu-id="2c2b0-271">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-271">Required.</span></span> <span data-ttu-id="2c2b0-272">La dirección URL del origen del vídeo.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-272">The URL of the video source.</span></span> <span data-ttu-id="2c2b0-273">Consulte la [lista de orígenes de vídeo compatibles](onenote_images_files.md#adding-videos).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-273">See the [list of supported video sources](onenote_images_files.md#adding-videos).</span></span> <br/><br/><span data-ttu-id="2c2b0-274">Ejemplo: `data-original-src="https://www.youtube.com/watch?v=3Ztr44aKmQ8"`</span><span class="sxs-lookup"><span data-stu-id="2c2b0-274">Example: `data-original-src="https://www.youtube.com/watch?v=3Ztr44aKmQ8"`</span></span> |
| <span data-ttu-id="2c2b0-275">ancho, alto</span><span class="sxs-lookup"><span data-stu-id="2c2b0-275">width, height</span></span> | <span data-ttu-id="2c2b0-276">El ancho o alto del iframe, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-276">The width or height of the iframe, in pixels.</span></span> <span data-ttu-id="2c2b0-277">Ejemplo: `width=300`</span><span class="sxs-lookup"><span data-stu-id="2c2b0-277">Example: `width=300`</span></span> |

#### <a name="output-attributes"></a><span data-ttu-id="2c2b0-278">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-278">Output attributes</span></span>

|<span data-ttu-id="2c2b0-279">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-279">Output attribute</span></span>|<span data-ttu-id="2c2b0-280">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-280">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-281">Data-original-src</span><span class="sxs-lookup"><span data-stu-id="2c2b0-281">data-original-src</span></span> | <span data-ttu-id="2c2b0-282">La dirección URL del origen del vídeo.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-282">The URL of the video source.</span></span> |
| <span data-ttu-id="2c2b0-283">src</span><span class="sxs-lookup"><span data-stu-id="2c2b0-283">src</span></span> | <span data-ttu-id="2c2b0-284">Un vínculo al vídeo que está insertado en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-284">A link to the video that is embedded in the OneNote page.</span></span> |
| <span data-ttu-id="2c2b0-285">ancho, alto</span><span class="sxs-lookup"><span data-stu-id="2c2b0-285">width, height</span></span> | <span data-ttu-id="2c2b0-286">El ancho o alto del iframe, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-286">The width or height of the iframe, in pixels.</span></span><br/><br/><span data-ttu-id="2c2b0-287">Ejemplo: `width=300`</span><span class="sxs-lookup"><span data-stu-id="2c2b0-287">Example: `width=300`</span></span> |
 
### <a name="output-html-example-for-videos"></a><span data-ttu-id="2c2b0-288">Ejemplo de HTML de salida para vídeos</span><span class="sxs-lookup"><span data-stu-id="2c2b0-288">Output HTML example for videos</span></span>

<span data-ttu-id="2c2b0-289">Los elementos **iframe** de salida contienen los puntos de conexión que vinculan a la página de origen y el vídeo, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-289">Output **iframe** elements contain endpoints that link to the source page and video, as shown.</span></span> 

```html
<iframe 
    width="340" height="280" 
    data-original-src="https://www.youtube.com/watch?v=3Ztr44aKmQ8" 
    src="https://www.youtube.com/embed/3Ztr44aKmQ8?feature=oembed&autoplay=true" />
``` 

## <a name="object-elements"></a><span data-ttu-id="2c2b0-290">Elementos object</span><span class="sxs-lookup"><span data-stu-id="2c2b0-290">Object elements</span></span>

<span data-ttu-id="2c2b0-291">Las páginas de OneNote pueden contener archivos adjuntos representados por elementos **object**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-291">OneNote pages can contain file attachments represented by **object** elements.</span></span> <span data-ttu-id="2c2b0-292">Un elemento **object** puede contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-292">An **object** element can contain the following attributes in the input and output HTML.</span></span>

> <span data-ttu-id="2c2b0-293">**Nota**: Las API de OneNote también pueden representar el contenido de archivos como imágenes en una página cuando el archivo se envía como imagen y usa el atributo **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-293">**Note:** The OneNote APIs can also render file content as images in a page when the file is sent as an image and uses the **data-render-src** attribute.</span></span>
> <span data-ttu-id="2c2b0-294">Ejemplo: `<img data-render-src="name:part-name" ... />`</span><span class="sxs-lookup"><span data-stu-id="2c2b0-294">Example: `<img data-render-src="name:part-name" ... />`</span></span>
 

#### <a name="input-attributes"></a><span data-ttu-id="2c2b0-295">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-295">Input attributes</span></span>

|<span data-ttu-id="2c2b0-296">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-296">Input attribute</span></span>|<span data-ttu-id="2c2b0-297">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-297">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-298">data</span><span class="sxs-lookup"><span data-stu-id="2c2b0-298">data</span></span> | <span data-ttu-id="2c2b0-299">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-299">Required.</span></span> <span data-ttu-id="2c2b0-300">El nombre de la parte que representa el archivo en una [solicitud de varias partes](../api-reference/v1.0/api/section_post_pages.md#example).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-300">The name of the part that represents the file in the [multipart request](../api-reference/v1.0/api/section_post_pages.md#example).</span></span> |
| <span data-ttu-id="2c2b0-301">data-attachment</span><span class="sxs-lookup"><span data-stu-id="2c2b0-301">data-attachment</span></span> | <span data-ttu-id="2c2b0-p130">Obligatorio. El nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-p130">Required. The file name.</span></span> |
| <span data-ttu-id="2c2b0-304">data-id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-304">data-id</span></span> | <span data-ttu-id="2c2b0-305">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-305">A reference for the element.</span></span><br/><br/><span data-ttu-id="2c2b0-306">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-306">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-307">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-307">style</span></span> | <span data-ttu-id="2c2b0-308">Las propiedades de posición y tamaño del objeto: **posición** (**absoluta** solo), **izquierda**, **arriba** y **ancho**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-308">The position and size properties for the object: **position** (**absolute** only), **left**, **top**, and **width**.</span></span><br/><br/><span data-ttu-id="2c2b0-309">Se usa para crear un objeto [con posición absoluta](onenote-abs-pos.md), solo si el objeto es un elemento secundario directo del cuerpo cuando el cuerpo indica `data-absolute-enabled="true"`.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-309">Used to create an [absolute positioned](onenote-abs-pos.md) object, only if the object is a direct child of the body when the body sets `data-absolute-enabled="true"`.</span></span><br/><br/><span data-ttu-id="2c2b0-310">Ejemplo: `<object style="position:absolute;top:350px;left:300px" ... />`</span><span class="sxs-lookup"><span data-stu-id="2c2b0-310">Example: `<object style="position:absolute;top:350px;left:300px" ... />`</span></span> |
| <span data-ttu-id="2c2b0-311">type</span><span class="sxs-lookup"><span data-stu-id="2c2b0-311">type</span></span> | <span data-ttu-id="2c2b0-312">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-312">Required.</span></span><br/><br/><span data-ttu-id="2c2b0-313">El tipo de archivo de medios estándar.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-313">The standard media file type.</span></span> <span data-ttu-id="2c2b0-314">Los tipos de archivo conocidos muestran el icono asociado con el tipo de archivo en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-314">Known file types display the icon associated with the file type on the OneNote page.</span></span> <span data-ttu-id="2c2b0-315">Los tipos de archivo desconocidos muestran un icono de archivo genérico.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-315">Unknown file types display a generic file icon.</span></span> |
<!--todo: add link to known file types--> 

#### <a name="output-attributes"></a><span data-ttu-id="2c2b0-316">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-316">Output attributes</span></span>

|<span data-ttu-id="2c2b0-317">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-317">Output attribute</span></span>|<span data-ttu-id="2c2b0-318">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-318">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-319">data</span><span class="sxs-lookup"><span data-stu-id="2c2b0-319">data</span></span> | <span data-ttu-id="2c2b0-320">El extremo para el recurso de archivo.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-320">The endpoint for the file resource.</span></span> |
| <span data-ttu-id="2c2b0-321">data-attachment</span><span class="sxs-lookup"><span data-stu-id="2c2b0-321">data-attachment</span></span> | <span data-ttu-id="2c2b0-322">El nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-322">The file name.</span></span> |
| <span data-ttu-id="2c2b0-323">data-id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-323">data-id</span></span> | <span data-ttu-id="2c2b0-324">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-324">A reference for the element.</span></span><br/><br/><span data-ttu-id="2c2b0-325">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-325">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-326">id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-326">id</span></span> | <span data-ttu-id="2c2b0-327">Un identificador único, generado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-327">A unique, generated ID for the element.</span></span> <span data-ttu-id="2c2b0-328">Devuelto por [solicitudes GET al punto de conexión del *contenido* de una página](../api-reference/v1.0/api/page_get.md) cuando se usa la opción de consulta `includeIDs=true`.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-328">Returned by [GET requests to a page's *content* endpoint](../api-reference/v1.0/api/page_get.md) when the `includeIDs=true` query option is used.</span></span><br/><br/><span data-ttu-id="2c2b0-329">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-329">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-330">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-330">style</span></span> | <span data-ttu-id="2c2b0-331">Las propiedades de posición del objeto.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-331">The position properties of the object.</span></span> |
| <span data-ttu-id="2c2b0-332">type</span><span class="sxs-lookup"><span data-stu-id="2c2b0-332">type</span></span> | <span data-ttu-id="2c2b0-333">El tipo de archivo de medios estándar.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-333">The standard media file type.</span></span> |
 

#### <a name="output-html-example-for-objects"></a><span data-ttu-id="2c2b0-334">Ejemplo HTML de salida para objetos</span><span class="sxs-lookup"><span data-stu-id="2c2b0-334">Output HTML example for objects</span></span>

<span data-ttu-id="2c2b0-335">Los elementos **object** de salida contienen puntos de conexión que vinculan a los recursos de archivo en la página, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-335">Output **object** elements contain endpoints that link to the file resources in the page, as shown.</span></span> <span data-ttu-id="2c2b0-336">Puede hacer [solicitudes GET independientes a puntos de conexión de recursos de archivo](../api-reference/v1.0/api/resource_get.md) para recuperar su contenido binario.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-336">You can make separate [GET requests to file resource endpoints](../api-reference/v1.0/api/resource_get.md) to retrieve their binary contents.</span></span>

```html
<object
    data="https://graph.microsoft.com/v1.0/me/onenote/resources/{file-id}/$value"
    data-attachment="fileName.pdf" 
    type="application/pdf" 
    [style="..."] />
``` 

## <a name="paragraphs-and-headings"></a><span data-ttu-id="2c2b0-337">Párrafos y encabezados</span><span class="sxs-lookup"><span data-stu-id="2c2b0-337">Paragraphs and headings</span></span>

<span data-ttu-id="2c2b0-338">Los párrafos, encabezados y otros contenedores de texto pueden contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-338">Paragraphs, headings, and other text containers can contain the following attributes in the input and output HTML.</span></span>

#### <a name="input-attributes"></a><span data-ttu-id="2c2b0-339">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-339">Input attributes</span></span>

|<span data-ttu-id="2c2b0-340">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-340">Input attribute</span></span>|<span data-ttu-id="2c2b0-341">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-341">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-342">data-id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-342">data-id</span></span> | <span data-ttu-id="2c2b0-343">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-343">A reference for the element.</span></span><br/><br/><span data-ttu-id="2c2b0-344">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-344">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-345">etiqueta de datos</span><span class="sxs-lookup"><span data-stu-id="2c2b0-345">data-tag</span></span> | <span data-ttu-id="2c2b0-346">Una [etiqueta de nota](onenote-note-tags.md) en un elemento de **p** o **h1** - **h6**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-346">A [note tag](onenote-note-tags.md) on a **p** or **h1** - **h6** element.</span></span> |
| <span data-ttu-id="2c2b0-347">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-347">style</span></span> | <span data-ttu-id="2c2b0-348">Las propiedades CSS [style](#styles) del elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-348">The CSS [style](#styles) properties of the element.</span></span> |
 

#### <a name="output-attributes"></a><span data-ttu-id="2c2b0-349">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-349">Output attributes</span></span>

|<span data-ttu-id="2c2b0-350">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-350">Output attribute</span></span>|<span data-ttu-id="2c2b0-351">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-351">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-352">data-id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-352">data-id</span></span> | <span data-ttu-id="2c2b0-353">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-353">A reference for the element.</span></span><br/><br/><span data-ttu-id="2c2b0-354">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-354">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-355">etiqueta de datos</span><span class="sxs-lookup"><span data-stu-id="2c2b0-355">data-tag</span></span> | <span data-ttu-id="2c2b0-356">Una [etiqueta de nota](onenote-note-tags.md) en un elemento de **p** o **h1** - **h6**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-356">A [note tag](onenote-note-tags.md) on a **p** or **h1** - **h6** element.</span></span> |
| <span data-ttu-id="2c2b0-357">id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-357">id</span></span> | <span data-ttu-id="2c2b0-358">Un identificador único, generado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-358">A unique, generated ID for the element.</span></span> <span data-ttu-id="2c2b0-359">Devuelto por [solicitudes GET al punto de conexión del *contenido* de una página](../api-reference/v1.0/api/page_get.md) cuando se usa la opción de consulta `includeIDs=true`.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-359">Returned by [GET requests to a page's *content* endpoint](../api-reference/v1.0/api/page_get.md) when the `includeIDs=true` query option is used.</span></span><br/><br/><span data-ttu-id="2c2b0-360">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-360">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-361">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-361">style</span></span> | <span data-ttu-id="2c2b0-362">Las propiedades CSS [style](#styles) del elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-362">The CSS [style](#styles) properties of the element.</span></span> <span data-ttu-id="2c2b0-363">En el HTML de salida, estos valores podrían devolverse insertados en los elementos secundarios adecuados o en elementos **span**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-363">In the output HTML, these values may be returned inline on appropriate child elements or on **span** elements.</span></span> |
 

<span data-ttu-id="2c2b0-364">Los siguientes ejemplos muestran HTML de entrada que usa diferentes maneras de definir estilos en contenedores de texto y el HTML de salida que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-364">The following examples show input HTML that uses different ways to define styles on text containers and the output HTML that's returned.</span></span>

#### <a name="input-html-with-styles-defined-using-inline-character-styles-in-the-start-tag-and-within-a-span-element"></a><span data-ttu-id="2c2b0-365">HTML de entrada con estilos definidos mediante estilos de caracteres en línea, en la etiqueta de inicio, y dentro de un elemento span.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-365">Input HTML with styles defined using inline character styles, in the start tag, and within a span element.</span></span>

```html
<h1>Heading <i>One</i> text</h1>
<p style="font-size:8pt;color:green;font-family:Courier;text-align:center">Some text</p>
<p>Some <span  style="font-size:16px;color:#ff0000;font-family:Segoe UI Black">more</span> text</p>
``` 

#### <a name="output-html-with-the-i-character-style-and-the-font-settings-in-the-p-start-tag-returned-as-inline-css-styles-on-span-elements"></a><span data-ttu-id="2c2b0-366">HTML de salida con el estilo de caracteres `<i>` y la configuración de fuentes en la etiqueta de inicio `<p>` devuelta como estilos CSS insertados en elementos span.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-366">Output HTML with the `<i>` character style and the font settings in the `<p>` start tag returned as inline CSS styles on span elements.</span></span>

```html
<h1 style="font-size:16pt;color:#1e4e79;margin-top:11pt;margin-bottom:11pt">Heading <span style="font-style:italic">One</span> text</h1>
<p style="text-align:center"><span style="font-family:Courier;font-size:8pt;color:green">Some text</span></p>
<p>Some <span style="font-family:Segoe UI Black;font-size:12pt;color:red">more</span> text</p>
``` 


## <a name="lists"></a><span data-ttu-id="2c2b0-367">Listas</span><span class="sxs-lookup"><span data-stu-id="2c2b0-367">Lists</span></span>

<span data-ttu-id="2c2b0-368">Las listas se representan como elementos **ol** o **ul** que contienen elementos list representados como **li**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-368">Lists are represented as **ol** or **ul** elements that contain list items represented as **li** elements.</span></span>

<span data-ttu-id="2c2b0-369">Los elementos lists y list pueden contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-369">Lists and list items can contain the following attributes in the input and output HTML.</span></span>

#### <a name="input-attributes"></a><span data-ttu-id="2c2b0-370">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-370">Input attributes</span></span>

|<span data-ttu-id="2c2b0-371">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-371">Input attribute</span></span>|<span data-ttu-id="2c2b0-372">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-372">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-373">data-id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-373">data-id</span></span> | <span data-ttu-id="2c2b0-374">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-374">A reference for the element.</span></span><br/><br/><span data-ttu-id="2c2b0-375">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-375">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-376">etiqueta de datos</span><span class="sxs-lookup"><span data-stu-id="2c2b0-376">data-tag</span></span> | <span data-ttu-id="2c2b0-377">Una [etiqueta de nota](onenote-note-tags.md) en un elemento de **ul**, **ol** o de **li**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-377">A [note tag](onenote-note-tags.md) on a **ul**, **ol**, or **li** element.</span></span> |
| <span data-ttu-id="2c2b0-378">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-378">style</span></span> | <span data-ttu-id="2c2b0-379">Las propiedades CSS **list-style-type** y [style](#styles) para la lista o el elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-379">The **list-style-type** and the CSS [style](#styles) properties for the list or list item.</span></span> |
 

#### <a name="output-attributes"></a><span data-ttu-id="2c2b0-380">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-380">Output attributes</span></span>

|<span data-ttu-id="2c2b0-381">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-381">Output attribute</span></span>|<span data-ttu-id="2c2b0-382">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-382">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-383">data-id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-383">data-id</span></span> | <span data-ttu-id="2c2b0-384">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-384">A reference for the element.</span></span><br/><br/><span data-ttu-id="2c2b0-385">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-385">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-386">etiqueta de datos</span><span class="sxs-lookup"><span data-stu-id="2c2b0-386">data-tag</span></span> |  <span data-ttu-id="2c2b0-387">Una [etiqueta de nota](onenote-note-tags.md) en un span en un elemento de **li**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-387">A [note tag](onenote-note-tags.md) on a span in a **li** element.</span></span> |
| <span data-ttu-id="2c2b0-388">id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-388">id</span></span> | <span data-ttu-id="2c2b0-389">Un identificador único, generado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-389">A unique, generated ID for the element.</span></span> <span data-ttu-id="2c2b0-390">Devuelto por [solicitudes GET al punto de conexión del *contenido* de una página](../api-reference/v1.0/api/page_get.md) cuando se usa la opción de consulta `includeIDs=true`.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-390">Returned by [GET requests to a page's *content* endpoint](../api-reference/v1.0/api/page_get.md) when the `includeIDs=true` query option is used.</span></span><br/><br/><span data-ttu-id="2c2b0-391">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-391">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-392">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-392">style</span></span> | <span data-ttu-id="2c2b0-393">Las propiedades **list-style-type** y CSS [style](#styles) del elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-393">The **list-style-type** and CSS [style](#styles) properties of the element.</span></span> <span data-ttu-id="2c2b0-394">En el HTML de salida, la configuración de nivel de lista se devuelve en elementos list.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-394">In the output HTML, list-level settings are returned on list items.</span></span> <span data-ttu-id="2c2b0-395">No se devuelven las propiedades predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-395">Default properties are not returned.</span></span> |
 
### <a name="list-styles"></a><span data-ttu-id="2c2b0-396">Estilos de lista</span><span class="sxs-lookup"><span data-stu-id="2c2b0-396">List styles</span></span>

<span data-ttu-id="2c2b0-397">Las API de OneNote en Microsoft Graph admiten los siguientes estilos de lista:</span><span class="sxs-lookup"><span data-stu-id="2c2b0-397">The OneNote APIs in Microsoft Graph support the following list styles:</span></span>

|<span data-ttu-id="2c2b0-398">Lista ordenada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-398">Ordered list</span></span>|<span data-ttu-id="2c2b0-399">Lista no ordenada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-399">Unordered list</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-400">ninguno</span><span class="sxs-lookup"><span data-stu-id="2c2b0-400">none</span></span> | <span data-ttu-id="2c2b0-401">ninguno</span><span class="sxs-lookup"><span data-stu-id="2c2b0-401">none</span></span> |
| <span data-ttu-id="2c2b0-402">decimal (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2c2b0-402">decimal (default)</span></span> | <span data-ttu-id="2c2b0-403">disc (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2c2b0-403">disc (default)</span></span> |
| <span data-ttu-id="2c2b0-404">lower-alpha</span><span class="sxs-lookup"><span data-stu-id="2c2b0-404">lower-alpha</span></span> | <span data-ttu-id="2c2b0-405">circle</span><span class="sxs-lookup"><span data-stu-id="2c2b0-405">circle</span></span> |
| <span data-ttu-id="2c2b0-406">lower-roman</span><span class="sxs-lookup"><span data-stu-id="2c2b0-406">lower-roman</span></span> | <span data-ttu-id="2c2b0-407">square</span><span class="sxs-lookup"><span data-stu-id="2c2b0-407">square</span></span> |
| <span data-ttu-id="2c2b0-408">upper-alpha</span><span class="sxs-lookup"><span data-stu-id="2c2b0-408">upper-alpha</span></span> | &nbsp; |
| <span data-ttu-id="2c2b0-409">upper-roman</span><span class="sxs-lookup"><span data-stu-id="2c2b0-409">upper-roman</span></span> | &nbsp; |
 
<span data-ttu-id="2c2b0-410">Puede aplicar estilos globales para una lista en el elemento **ol** o **ul** del HTML de entrada, pero los estilos se devuelven en los elementos **li**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-410">You can apply global styles for a list on the **ol** or **ul** element in the input HTML, but styles are returned on the **li** elements.</span></span>

#### <a name="homogenous-list-style"></a><span data-ttu-id="2c2b0-411">Estilo de lista homogénea</span><span class="sxs-lookup"><span data-stu-id="2c2b0-411">Homogenous list style</span></span>

<span data-ttu-id="2c2b0-412">Este ejemplo muestra el HTML de entrada que establece el tipo de estilo de lista en el elemento **ol** y estilos CSS en elementos de listas individuales.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-412">This example shows input HTML that sets the list style type on the **ol** element and CSS styles on individual list items.</span></span>

```html
<ol style="list-style-type:upper-roman;color:blue">
    <li style="font-weight:bold">Jacksonville</li>
    <li style="text-decoration:line-through">Orlando</li>
    <li style="font-family:Courier">Naples</li>
</ol>
``` 

<span data-ttu-id="2c2b0-p138">Este es el HTML de salida. Observe que los estilos se devuelven en línea en los elementos **li** o **span** individuales.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-p138">This is the output HTML. Notice that styles are returned inline on the individual **li** or **span** elements.</span></span>

```html
<ol>
    <li style="list-style-type:upper-roman"><span style="color:blue;font-weight:bold">Jacksonville</span></li>
    <li style="list-style-type:upper-roman"><span style="color:blue;text-decoration:line-through">Orlando</span></li>
    <li style="list-style-type:upper-roman"><span style="font-family:Courier;color:blue">Naples</span></li>
</ol>
``` 

#### <a name="variable-list-styles"></a><span data-ttu-id="2c2b0-415">Estilos de listas variables</span><span class="sxs-lookup"><span data-stu-id="2c2b0-415">Variable list styles</span></span>

<span data-ttu-id="2c2b0-416">Este ejemplo muestra HTML de entrada que establece diferentes tipos de estilos de listas en los elementos **li**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-416">This example shows input HTML that sets different list style types on the **li** elements.</span></span>

```html
<ul style="font-style:italic">
    <li style="list-style-type:square">square style</li>
    <li style="list-style-type:circle">circle style</li>
    <li style="list-style-type:disc">disc style (default)</li>
</ul>
``` 

<span data-ttu-id="2c2b0-p139">Este es el HTML de salida. Observe que los estilos se devuelven en línea en los elementos **li** o **span** individuales.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-p139">This is the output HTML. Notice that styles are returned inline on the individual **li** or **span** elements.</span></span>

```html
<ul>
    <li style="list-style-type:square"><span style="font-style:italic">square style</span></li>
    <li style="list-style-type:circle"><span style="font-style:italic">circle style</span></li>
    <li><span style="font-style:italic">disc style (default)</span></li>
</ul>
``` 


## <a name="tables"></a><span data-ttu-id="2c2b0-419">Tablas</span><span class="sxs-lookup"><span data-stu-id="2c2b0-419">Tables</span></span>

<span data-ttu-id="2c2b0-p140">Las tablas se representan como elementos **table** que pueden contener elementos **tr** y **td**. Se admiten tablas anidadas.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-p140">Tables are represented as **table** elements that can contain **tr** and **td** elements. Nested tables are supported.</span></span>

<span data-ttu-id="2c2b0-422">Las tablas pueden contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-422">Tables can contain the following attributes in the input and output HTML.</span></span> <span data-ttu-id="2c2b0-423">Las API de OneNote no admiten los atributos **rowspan** o **colspan**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-423">The OneNote APIs do not support **rowspan** or **colspan** attributes.</span></span> 

#### <a name="input-attributes"></a><span data-ttu-id="2c2b0-424">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-424">Input attributes</span></span>

|<span data-ttu-id="2c2b0-425">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="2c2b0-425">Input attribute</span></span>|<span data-ttu-id="2c2b0-426">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-426">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-427">data-id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-427">data-id</span></span> | <span data-ttu-id="2c2b0-428">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-428">A reference for the element.</span></span><br/><br/><span data-ttu-id="2c2b0-429">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-429">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-430">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-430">style</span></span> | <span data-ttu-id="2c2b0-431">Las propiedades CSS [style](#styles) del elemento y también:</span><span class="sxs-lookup"><span data-stu-id="2c2b0-431">The CSS [style](#styles) properties of the element, and also:</span></span><br/> <span data-ttu-id="2c2b0-432">- **border**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-432">- **border**.</span></span> <span data-ttu-id="2c2b0-433">Puede ser 0px o 1px.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-433">Can be either 0px or 1px.</span></span><br/> <span data-ttu-id="2c2b0-434">- **width**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-434">- **width**.</span></span> <span data-ttu-id="2c2b0-435">Compatible con **table** y **td** como píxeles o porcentaje de ancho de página.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-435">Supported by **table** and **td** as pixels or percentage of page width.</span></span><br/><br/><span data-ttu-id="2c2b0-436">Por ejemplo, `width="100px"` o `width="60%"`</span><span class="sxs-lookup"><span data-stu-id="2c2b0-436">Example: `width="100px"` or `width="60%"`</span></span> |
 

#### <a name="output-attributes"></a><span data-ttu-id="2c2b0-437">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-437">Output attributes</span></span>

|<span data-ttu-id="2c2b0-438">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="2c2b0-438">Output attribute</span></span>|<span data-ttu-id="2c2b0-439">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2b0-439">Description</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-440">data-id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-440">data-id</span></span> | <span data-ttu-id="2c2b0-441">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-441">A reference for the element.</span></span><br/><br/><span data-ttu-id="2c2b0-442">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-442">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-443">id</span><span class="sxs-lookup"><span data-stu-id="2c2b0-443">id</span></span> | <span data-ttu-id="2c2b0-444">Un identificador único, generado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-444">A unique, generated ID for the element.</span></span> <span data-ttu-id="2c2b0-445">Devuelto por [solicitudes GET al punto de conexión del *contenido* de una página](../api-reference/v1.0/api/page_get.md) cuando se usa la opción de consulta `includeIDs=true`.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-445">Returned by [GET requests to a page's *content* endpoint](../api-reference/v1.0/api/page_get.md) when the `includeIDs=true` query option is used.</span></span><br/><br/><span data-ttu-id="2c2b0-446">Se usa para [actualizar el contenido de la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-446">Used to [update page content](onenote_update_page.md).</span></span> |
| <span data-ttu-id="2c2b0-447">style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-447">style</span></span> | <span data-ttu-id="2c2b0-448">Las propiedades CSS [style](#styles) del elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-448">The CSS [style](#styles) properties of the element.</span></span> |
 

<span data-ttu-id="2c2b0-449">Los siguientes ejemplos muestran HTML de entrada que usa diferentes maneras de definir estilos en tablas y el HTML de salida que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-449">The following examples show input HTML that uses different ways to define styles on tables and the output HTML that's returned.</span></span>

#### <a name="input-html-with-optional-settings-at-different-levels"></a><span data-ttu-id="2c2b0-450">HTML de entrada con valores de configuración opcionales en diferentes niveles</span><span class="sxs-lookup"><span data-stu-id="2c2b0-450">Input HTML with optional settings at different levels.</span></span>

```html
<table style="border:0px;width:500px;background-color:green">
    <tr> 
        <td>Cell 1</td> 
        <td>Cell 2</td> 
        <td>Cell 3</td> 
    </tr> 
    <tr style="background-color:blue"> 
        <td style="text-align:right;background-color:red">Left</td> 
        <td style="text-align:center">Middle</td> 
        <td>Right</td> 
    </tr> 
</table>
```
 
#### <a name="output-html-with-css-styles-returned-inline-on-the-td-elements"></a><span data-ttu-id="2c2b0-451">El HTML de salida con estilos CSS se devolvió insertado en los elementos td.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-451">Output HTML with CSS styles returned inline on the td elements.</span></span>

```html
<table style="border:0px">
    <tr>
        <td style="background-color:green;width:166;border:0px">Cell 1</td>
        <td style="background-color:green;width:166;border:0px">Cell 2</td>
        <td style="background-color:green;width:166;border:0px">Cell 3</td>
    </tr>
    <tr>
        <td style="background-color:red;width:166;border:0px;text-align:right">Left</td>
        <td style="background-color:blue;width:166;border:0px;text-align:center">Middle</td>
        <td style="background-color:blue;width:166;border:0px">Right</td>
    </tr>
</table>
``` 


## <a name="styles"></a><span data-ttu-id="2c2b0-452">Estilos</span><span class="sxs-lookup"><span data-stu-id="2c2b0-452">Styles</span></span>

<span data-ttu-id="2c2b0-453">Las API de OneNote en Microsoft Graph admiten las siguientes propiedades CSS **style** insertadas para elementos en el cuerpo de la página, como **body**, **div**, **p**, **li** y **span**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-453">OneNote APIs in Microsoft Graph support the following inline CSS **style** properties for elements in the page body, such as **body**, **div**, **p**, **li**, and **span**.</span></span>

|<span data-ttu-id="2c2b0-454">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2c2b0-454">Property</span></span>|<span data-ttu-id="2c2b0-455">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2c2b0-455">Example</span></span>|
|:------|:------|
| <span data-ttu-id="2c2b0-456">background-color</span><span class="sxs-lookup"><span data-stu-id="2c2b0-456">background-color</span></span> | <span data-ttu-id="2c2b0-457">`style="background-color:#66cc66"` (el valor predeterminado es blanco)</span><span class="sxs-lookup"><span data-stu-id="2c2b0-457">`style="background-color:#66cc66"` (defaults to white)</span></span><br/><br/><span data-ttu-id="2c2b0-458">Se admiten tanto en formato hexadecimal y colores con nombre.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-458">Both hexadecimal format and named colors are supported.</span></span> |
| <span data-ttu-id="2c2b0-459">color</span><span class="sxs-lookup"><span data-stu-id="2c2b0-459">color</span></span> | <span data-ttu-id="2c2b0-460">`style="color:#ffffff"` (el valor predeterminado es negro)</span><span class="sxs-lookup"><span data-stu-id="2c2b0-460">`style="color:#ffffff"` (defaults to black)</span></span> |
| <span data-ttu-id="2c2b0-461">font-family</span><span class="sxs-lookup"><span data-stu-id="2c2b0-461">font-family</span></span> | <span data-ttu-id="2c2b0-462">`style="font-family:Courier"` (el valor predeterminado es Calibri)</span><span class="sxs-lookup"><span data-stu-id="2c2b0-462">`style="font-family:Courier"` (defaults to Calibri)</span></span> |
| <span data-ttu-id="2c2b0-463">font-size</span><span class="sxs-lookup"><span data-stu-id="2c2b0-463">font-size</span></span> | <span data-ttu-id="2c2b0-464">`style="font-size:10pt"` (el valor predeterminado es 11pt)</span><span class="sxs-lookup"><span data-stu-id="2c2b0-464">`style="font-size:10pt"` (defaults to 11pt)</span></span><br/><br/><span data-ttu-id="2c2b0-465">Las API aceptan el tamaño de fuente en *pt* o *px*, pero convierten *px* a *pt*.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-465">The APIs accept font size in *pt* or *px*, but converts *px* to *pt*.</span></span> <span data-ttu-id="2c2b0-466">Los valores decimales se redondean al más próximo n.0pt o n.5pt.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-466">Decimal values are rounded to the nearest n.0pt or n.5pt.</span></span> |
| <span data-ttu-id="2c2b0-467">font-style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-467">font-style</span></span> | <span data-ttu-id="2c2b0-468">`style="font-style:italic"` (solo normal o cursiva)</span><span class="sxs-lookup"><span data-stu-id="2c2b0-468">`style="font-style:italic"` (normal or italic only)</span></span> |
| <span data-ttu-id="2c2b0-469">font-style</span><span class="sxs-lookup"><span data-stu-id="2c2b0-469">font-weight</span></span> | <span data-ttu-id="2c2b0-470">`style="font-weight:bold"` (solo normal o negrita)</span><span class="sxs-lookup"><span data-stu-id="2c2b0-470">`style="font-weight:bold"` (normal or bold only)</span></span> |
| <span data-ttu-id="2c2b0-471">strike-through</span><span class="sxs-lookup"><span data-stu-id="2c2b0-471">strike-through</span></span> | `style="text-decoration:line-through"` |
| <span data-ttu-id="2c2b0-472">text-align</span><span class="sxs-lookup"><span data-stu-id="2c2b0-472">text-align</span></span> | <span data-ttu-id="2c2b0-473">`style="text-align:center"` (solo para elementos de bloque)</span><span class="sxs-lookup"><span data-stu-id="2c2b0-473">`style="text-align:center"` (for block elements only)</span></span> |
| <span data-ttu-id="2c2b0-474">text-decoration</span><span class="sxs-lookup"><span data-stu-id="2c2b0-474">text-decoration</span></span> | <span data-ttu-id="2c2b0-475">`style="text-decoration:underline"` (ninguno o solo subrayado)</span><span class="sxs-lookup"><span data-stu-id="2c2b0-475">`style="text-decoration:underline"` (none or underline only)</span></span> |
 

<span data-ttu-id="2c2b0-476">También se admiten los siguientes estilos de caracteres insertados:</span><span class="sxs-lookup"><span data-stu-id="2c2b0-476">The following inline character styles and are also supported:</span></span>

<table id="simpletable">
<tr>
<td id="simplecell"><span data-ttu-id="2c2b0-477">&lt;b&gt;</span><span class="sxs-lookup"><span data-stu-id="2c2b0-477">&lt;b&gt;</span></span></td>
<td id="simplecell"><span data-ttu-id="2c2b0-478">&lt;k&gt;</span><span class="sxs-lookup"><span data-stu-id="2c2b0-478">&lt;i&gt;</span></span></td>
<td id="simplecell"><span data-ttu-id="2c2b0-479">&lt;s&gt;</span><span class="sxs-lookup"><span data-stu-id="2c2b0-479">&lt;u&gt;</span></span></td>
</tr>
<tr>
<td id="simplecell"><span data-ttu-id="2c2b0-480">&lt;em&gt;</span><span class="sxs-lookup"><span data-stu-id="2c2b0-480">&lt;em&gt;</span></span></td>
<td id="simplecell"><span data-ttu-id="2c2b0-481">&lt;Texto en negrita.&gt;</span><span class="sxs-lookup"><span data-stu-id="2c2b0-481">&lt;strong&gt;</span></span></td>
<td id="simplecell"><span data-ttu-id="2c2b0-482">&lt;Tachado&gt;</span><span class="sxs-lookup"><span data-stu-id="2c2b0-482">&lt;strike&gt;</span></span></td>
</tr>
<tr>
<td id="simplecell"><span data-ttu-id="2c2b0-483">&lt;sup&gt;</span><span class="sxs-lookup"><span data-stu-id="2c2b0-483">&lt;sup&gt;</span></span></td>
<td id="simplecell"><span data-ttu-id="2c2b0-484">&lt;sub&gt;</span><span class="sxs-lookup"><span data-stu-id="2c2b0-484">&lt;sub&gt;</span></span></td>
<td id="simplecell"><span data-ttu-id="2c2b0-485">&lt;supr&gt;</span><span class="sxs-lookup"><span data-stu-id="2c2b0-485">&lt;del&gt;</span></span></td>
</tr>
<tr>
<td id="simplecell"><span data-ttu-id="2c2b0-486">&lt;cite&gt;</span><span class="sxs-lookup"><span data-stu-id="2c2b0-486">&lt;cite&gt;</span></span></td>
<td id="simplecell">&nbsp;</td>
<td id="simplecell">&nbsp;</td>
</tr>
</table>

 
## <a name="input-and-output-html-example"></a><span data-ttu-id="2c2b0-487">HTML de entrada y salida de ejemplo</span><span class="sxs-lookup"><span data-stu-id="2c2b0-487">Input and output HTML example</span></span>

<span data-ttu-id="2c2b0-488">La siguiente imagen muestra una página simple que se creó con Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-488">The following image shows a simple page that was created with Microsoft Graph.</span></span>

![Imagen de una página de OneNote con notas de estudio de contenido de Wikipedia](images/onenote-sample-image.png)

<span data-ttu-id="2c2b0-490">Este es el HTML de entrada que se envió en el cuerpo del mensaje para crear la página.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-490">This is the input HTML sent in the message body to create the page.</span></span>

```html
<html lang="en-US">
    <head>
        <title>Sample Study Notes</title>
        <meta name="created" content="2015-01-01T01:01"/>
    </head>
    <body>
        <h1>Aurora Borealis</h1>
        <p>Dancing lights in the sky. Also called <i>Northern Lights</i>. Caused by solar radiation.</p>
        <br />
        <p><b>Intersting facts</b></p>
        <table>
            <tr>
                <td>Neil Armstrong</td>
                <td>Commander</td>
            </tr>
            <tr>
                <td>Buzz Aldrin</td>
                <td>LM Pilot</td>
            </tr>
            <tr>
                <td>Michael Collins</td>
                <td>Command Module Pilot</td>
            </tr>
        </table>
        <img alt="Apollo 11 commemorative stamp." src="http://upload.wikimedia.org/wikipedia/commons/a/a4/First_Man_on_Moon_1969_Issue-10c.jpg"  width="400"/>
        <p>References:</p>
        <p><a href="http://en.wikipedia.org/wiki/Apollo_11">http://en.wikipedia.org/wiki/Apollo_11</a></p>
        <p><a href="http://www.nasa.gov/mission_pages/apollo/missions/apollo11.html">http://www.nasa.gov/mission_pages/apollo/missions/apollo11.html</a></p>
    </body>
</html>
``` 

<br/>

<span data-ttu-id="2c2b0-491">Este es el HTML de salida que Microsoft Graph devuelve cuando [obtiene el contenido de la página](onenote-get-content.md).</span><span class="sxs-lookup"><span data-stu-id="2c2b0-491">This is the output HTML that Microsoft Graph returns when you [get page content](onenote-get-content.md).</span></span>

> <span data-ttu-id="2c2b0-492">**Nota**: Cuando [crea una página](onenote-create-page.md) u [obtiene los metadatos de una página](../api-reference/v1.0/api/page_get.md), la API devuelve la dirección URL del punto de conexión del *contenido* de la página en la propiedad **contentUrl**.</span><span class="sxs-lookup"><span data-stu-id="2c2b0-492">**Note:** When you [create a page](onenote-create-page.md) or [get page metadata](../api-reference/v1.0/api/page_get.md), the API returns the *content* endpoint URL of the page in the **contentUrl** property.</span></span>

```html
<html htmlns="http://www.w3.org/1999/xhtml" lang="en-US">
    <head>
        <title>Sample Study Notes</title>
    </head>
    <body data-absolute-enabled="true" style="font-family:Calibri;font-size:11pt">
        <div data-id="_default" style="position:absolute;left:48px;top:120px;width:624px">
            <h1 style="font-size:16pt;color:#1e4e79;margin-top:11pt;margin-bottom:11pt">American History 101: Moon Landing</h1>
            <p>First moon landing - July 20, 1969 with Apollo 11 (Eagle)</p>
            <br />
            <p><span style="font-weight:bold">Apollo 11 Astronauts</span></p>
            <table style="border:0px">
                <tr>
                    <td style="border:0px">Neil Armstrong</td>
                    <td style="border:0px">Commander</td>
                </tr>
                <tr>
                    <td style="border:0px">Buzz Aldrin</td>
                    <td style="border:0px">LM Pilot</td>
                </tr>
                <tr>
                    <td style="border:0px">Michael Collins</td>
                    <td style="border:0px">Command Module Pilot</td>
                </tr>
            </table>
            <br />
            <img alt="Apollo 11 commemorative stamp." width="400" height="248" src="https://graph.microsoft.com/v1.0/me/onenote/resources/0-f717b5fa5eaa454da7ecdf72a8c137fe!1-73DBAF9B7E5C4B4C!10456/$value"
                 data-src-type="image/jpeg" data-fullres-src="https://graph.microsoft.com/v1.0/me/onenote/resources/0-f717b5fa5eaa454da7ecdf72a8c137fe!1-73DBAF9B7E5C4B4C!10456/$value" data-fullres-src-type="image/jpeg" />
            <p>References:</p>
            <p><a href="http://en.wikipedia.org/wiki/Apollo_11">http://en.wikipedia.org/wiki/Apollo_11</a></p>
            <p><a href="http://www.nasa.gov/mission_pages/apollo/missions/apollo11.html">http://www.nasa.gov/mission_pages/apollo/missions/apollo11.html</a></p>
        </div>
    </body>
</html>
``` 

## <a name="see-also"></a><span data-ttu-id="2c2b0-493">Ver también</span><span class="sxs-lookup"><span data-stu-id="2c2b0-493">See also</span></span>

- [<span data-ttu-id="2c2b0-494">Obtener el contenido y la estructura de OneNote</span><span class="sxs-lookup"><span data-stu-id="2c2b0-494">Get OneNote content and structure</span></span>](onenote-get-content.md)
- [<span data-ttu-id="2c2b0-495">Crear páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="2c2b0-495">Create OneNote pages</span></span>](onenote-create-page.md)
- [<span data-ttu-id="2c2b0-496">Actualizar el contenido de la página de OneNote</span><span class="sxs-lookup"><span data-stu-id="2c2b0-496">Update OneNote page content</span></span>](onenote_update_page.md)
- [<span data-ttu-id="2c2b0-497">Agregar imágenes, vídeos y archivos</span><span class="sxs-lookup"><span data-stu-id="2c2b0-497">Add images, videos, and files</span></span>](onenote_images_files.md)
