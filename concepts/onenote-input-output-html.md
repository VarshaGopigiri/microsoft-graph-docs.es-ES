---
title: HTML de entrada y salida en páginas de OneNote
description: 'El código HTML que define el contenido y la estructura de la página cuando crea o actualiza una página de OneNote se llama *HTML de entrada*. '
ms.openlocfilehash: f75601771437e359626ef9ffbb474b9a29f07033
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092921"
---
# <a name="input-and-output-html-in-onenote-pages"></a><span data-ttu-id="768d3-103">HTML de entrada y salida en páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="768d3-103">Input and output HTML in OneNote pages</span></span>

<span data-ttu-id="768d3-104">El código HTML que define el contenido y la estructura de la página cuando [crea](onenote-create-page.md) o [actualiza](onenote-update-page.md) una página de OneNote se llama *HTML de entrada*.</span><span class="sxs-lookup"><span data-stu-id="768d3-104">The HTML that defines the page content and structure when you [create](onenote-create-page.md) or [update](onenote-update-page.md) a OneNote page is called *input HTML*.</span></span> 

<span data-ttu-id="768d3-105">El código HTML que se devuelve cuando [,obtiene el contenido de la página](onenote-get-content.md) se denomina *HTML de salida*.</span><span class="sxs-lookup"><span data-stu-id="768d3-105">The HTML that's returned when you [get page content](onenote-get-content.md) is called *output HTML*.</span></span> <span data-ttu-id="768d3-106">El HTML de salida no será el mismo que el de entrada.</span><span class="sxs-lookup"><span data-stu-id="768d3-106">Output HTML won't be the same as input HTML.</span></span>

<span data-ttu-id="768d3-107">Las API de OneNote en Microsoft Graph conservan el contenido semántico y la estructura básica del HTML de entrada, pero la convierten en un conjunto de [elementos HTML y propiedades CSS compatibles](onenote-create-page.md#supported-html-and-css-for-onenote-pages).</span><span class="sxs-lookup"><span data-stu-id="768d3-107">The OneNote APIs in Microsoft Graph preserve the semantic content and basic structure of the input HTML, but convert it to a set of [supported HTML elements and CSS properties](onenote-create-page.md#supported-html-and-css-for-onenote-pages).</span></span> <span data-ttu-id="768d3-108">Las API también agregan atributos personalizados que admiten las características de OneNote.</span><span class="sxs-lookup"><span data-stu-id="768d3-108">The APIs also add custom attributes that support OneNote features.</span></span>
 
<span data-ttu-id="768d3-109">Este artículo describe los principales elementos y atributos del HTML de entrada y de salida.</span><span class="sxs-lookup"><span data-stu-id="768d3-109">This article describes the principal elements and attributes of input and output HTML.</span></span> <span data-ttu-id="768d3-110">Puede ser útil comprender el HTML de entrada cuando crea o actualiza el contenido de la página, y el HTML de salida cuando analiza el contenido de la página devuelto.</span><span class="sxs-lookup"><span data-stu-id="768d3-110">It can be helpful to understand input HTML when you're creating or updating page content, and output HTML when you're parsing returned page content.</span></span> 

## <a name="body-element"></a><span data-ttu-id="768d3-111">body element</span><span class="sxs-lookup"><span data-stu-id="768d3-111">Body element</span></span>

<span data-ttu-id="768d3-112">El contenido HTML en el cuerpo de la página representa el contenido y la estructura de la página, incluidos los recursos de imagen y archivo.</span><span class="sxs-lookup"><span data-stu-id="768d3-112">The HTML content in the page body represents the page content and structure, including image and file resources.</span></span> <span data-ttu-id="768d3-113">El elemento **body** puede contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="768d3-113">The **body** element can contain the following attributes in the input and output HTML.</span></span>

#### <a name="input-attributes"></a><span data-ttu-id="768d3-114">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-114">Input attributes</span></span>

|<span data-ttu-id="768d3-115">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-115">Input attribute</span></span>|<span data-ttu-id="768d3-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-116">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-117">data-absolute-enabled</span><span class="sxs-lookup"><span data-stu-id="768d3-117">data-absolute-enabled</span></span> | <span data-ttu-id="768d3-118">Indica si el cuerpo de entrada admite los elementos [con posición absoluta](onenote-abs-pos.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-118">Indicates whether the input body supports [absolute positioned](onenote-abs-pos.md) elements.</span></span> |
| <span data-ttu-id="768d3-119">style</span><span class="sxs-lookup"><span data-stu-id="768d3-119">style</span></span> | <p><span data-ttu-id="768d3-120">Las propiedades CSS [style](#styles) del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="768d3-120">The CSS [style](#styles) properties of the body.</span></span> <span data-ttu-id="768d3-121">En el HTML de salida, la configuración de entrada podría devolverse insertada en los elementos secundarios adecuados.</span><span class="sxs-lookup"><span data-stu-id="768d3-121">In the output HTML, input settings might be returned inline on appropriate child elements.</span></span></p><p><span data-ttu-id="768d3-122">Actualmente, el color de fondo no es compatible con el elemento **body**.</span><span class="sxs-lookup"><span data-stu-id="768d3-122">Background color is not currently supported for the **body** element.</span></span></p> |
 

#### <a name="output-attributes"></a><span data-ttu-id="768d3-123">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-123">Output attributes</span></span>

|<span data-ttu-id="768d3-124">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-124">Output attribute</span></span>|<span data-ttu-id="768d3-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-125">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-126">data-absolute-enabled</span><span class="sxs-lookup"><span data-stu-id="768d3-126">data-absolute-enabled</span></span> | <span data-ttu-id="768d3-127">Indica si el cuerpo admite los elementos [con posición absoluta](onenote-abs-pos.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-127">Indicates whether the body supports [absolute positioned](onenote-abs-pos.md) elements.</span></span> <span data-ttu-id="768d3-128">Siempre **true** en el HTML de salida.</span><span class="sxs-lookup"><span data-stu-id="768d3-128">Always **true** in output HTML.</span></span> |
| <span data-ttu-id="768d3-129">style</span><span class="sxs-lookup"><span data-stu-id="768d3-129">style</span></span> | <span data-ttu-id="768d3-130">Las propiedades **font-family** y **font-size** del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="768d3-130">The **font-family** and **font-size** properties of the body.</span></span> |


## <a name="div-elements"></a><span data-ttu-id="768d3-131">Elementos div</span><span class="sxs-lookup"><span data-stu-id="768d3-131">Div elements</span></span>

<span data-ttu-id="768d3-132">Los elementos **div** contienen texto, imágenes y otro contenido.</span><span class="sxs-lookup"><span data-stu-id="768d3-132">**Div** elements contain text, images, and other content.</span></span> <span data-ttu-id="768d3-133">Un elemento **div** puede contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="768d3-133">A **div** element can contain the following attributes in the input and output HTML.</span></span>

#### <a name="input-attributes"></a><span data-ttu-id="768d3-134">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-134">Input attributes</span></span>

|<span data-ttu-id="768d3-135">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-135">Input attribute</span></span>|<span data-ttu-id="768d3-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-136">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-137">data-id</span><span class="sxs-lookup"><span data-stu-id="768d3-137">data-id</span></span> | <span data-ttu-id="768d3-138">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-138">A reference for the element.</span></span><br/><br/><span data-ttu-id="768d3-139">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-139">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-140">data-render-fallback</span><span class="sxs-lookup"><span data-stu-id="768d3-140">data-render-fallback</span></span> | <span data-ttu-id="768d3-141">La acción de reserva si falla la [extracción](onenote-extract-data.md): **render** (predeterminado) o **none**</span><span class="sxs-lookup"><span data-stu-id="768d3-141">The fallback action if the [extraction](onenote-extract-data.md) fails: **render** (default) or **none**.</span></span> |
| <span data-ttu-id="768d3-142">data-render-method</span><span class="sxs-lookup"><span data-stu-id="768d3-142">data-render-method</span></span> | <span data-ttu-id="768d3-143">El método [extraction](onenote-extract-data.md) para llevar a cabo, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="768d3-143">The [extraction](onenote-extract-data.md) method to perform, for example:  or .</span></span><br/><span data-ttu-id="768d3-144">`extract.businesscard` o `extract.recipe`</span><span class="sxs-lookup"><span data-stu-id="768d3-144">`extract.businesscard` or `extract.recipe`</span></span> |
| <span data-ttu-id="768d3-145">data-render-src</span><span class="sxs-lookup"><span data-stu-id="768d3-145">data-render-src</span></span> | <span data-ttu-id="768d3-146">El origen del contenido para la [extracción](onenote-extract-data.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-146">The content source for the [extraction](onenote-extract-data.md).</span></span> |
| <span data-ttu-id="768d3-147">style</span><span class="sxs-lookup"><span data-stu-id="768d3-147">style</span></span> | <span data-ttu-id="768d3-148">La posición, tamaño, fuente y propiedades de color del elemento div:</span><span class="sxs-lookup"><span data-stu-id="768d3-148">The position, size, font, and color properties for the div:</span></span> <ul><li><span data-ttu-id="768d3-149">**position** (solo **absolute**), **left**, **top** y **width** (height se configura automáticamente para div)</span><span class="sxs-lookup"><span data-stu-id="768d3-149">**position** (**absolute** only), **left**, **top**, and **width** (height is auto-configured for divs)</span></span><br/><br/><span data-ttu-id="768d3-150">Se usa para crear un elemento div [con posición absoluta](onenote-abs-pos.md), solo si el div es un elemento secundario directo del cuerpo cuando el cuerpo indica `data-absolute-enabled="true"`.</span><span class="sxs-lookup"><span data-stu-id="768d3-150">Used to create an [absolute positioned](onenote-abs-pos.md) div, only if the div is a direct child of the body when the body sets `data-absolute-enabled="true"`.</span></span><br/><br/><span data-ttu-id="768d3-151">Ejemplo: `<div style="position:absolute;width:360px;top:350px;left:300px" ... />`</span><span class="sxs-lookup"><span data-stu-id="768d3-151">Example: `<div style="position:absolute;width:360px;top:350px;left:300px" ... />`</span></span></li><li><span data-ttu-id="768d3-p108">Las propiedades CSS [style](#styles) del elemento. En el HTML de salida, estos valores se devuelven en línea en elementos secundarios correspondientes.</span><span class="sxs-lookup"><span data-stu-id="768d3-p108">The CSS [style](#styles) properties of the element. In the output HTML, these values are returned inline on appropriate child elements.</span></span></li></ul> |
 

<span data-ttu-id="768d3-154">Las API de OneNote en Microsoft Graph ajustan todo el contenido del cuerpo en al menos un div.</span><span class="sxs-lookup"><span data-stu-id="768d3-154">The OneNote APIs in Microsoft Graph wrap all body content in at least one div.</span></span> <span data-ttu-id="768d3-155">La API crea un div predeterminado (con atributos `data-id="_default"`) para contener el contenido del cuerpo si:</span><span class="sxs-lookup"><span data-stu-id="768d3-155">The API creates a default div (attributed with `data-id="_default"`) to contain the body content if:</span></span>

- <span data-ttu-id="768d3-156">El atributo **data-absolute-enabled** del elemento de entrada del cuerpo se omite o se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="768d3-156">The input body element's **data-absolute-enabled** attribute is omitted or set to **false**.</span></span> <span data-ttu-id="768d3-157">En este caso, se coloca todo el contenido del cuerpo en el div predeterminado.</span><span class="sxs-lookup"><span data-stu-id="768d3-157">In this case, all body content is put in the default div.</span></span>

- <span data-ttu-id="768d3-158">El atributo **data-absolute-enabled** del elemento de entrada del cuerpo es **true**, pero el HTML de entrada contiene elementos secundarios directos que no son elementos [con posición absoluta](onenote-abs-pos.md)&nbsp;**div**, **img** u **object**.</span><span class="sxs-lookup"><span data-stu-id="768d3-158">The input body element's **data-absolute-enabled** attribute is **true**, but the input HTML contains direct children that aren't [absolute positioned](onenote-abs-pos.md)&nbsp;**div**, **img**, or **object** elements.</span></span> <span data-ttu-id="768d3-159">En este caso, los elementos secundarios directos que no son elementos [con posición absoluta](onenote-abs-pos.md)&nbsp;**div**, **img** u **object** se colocan en el div predeterminado.</span><span class="sxs-lookup"><span data-stu-id="768d3-159">In this case, direct children that aren't [absolute positioned](onenote-abs-pos.md)&nbsp;**div**, **img**, or **object** elements are put in the default div.</span></span>


#### <a name="output-attributes"></a><span data-ttu-id="768d3-160">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-160">Output attributes</span></span>

|<span data-ttu-id="768d3-161">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-161">Output attribute</span></span>|<span data-ttu-id="768d3-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-162">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-163">data-id</span><span class="sxs-lookup"><span data-stu-id="768d3-163">data-id</span></span> | <span data-ttu-id="768d3-164">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-164">A reference for the element.</span></span><br/><br/><span data-ttu-id="768d3-165">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-165">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-166">id</span><span class="sxs-lookup"><span data-stu-id="768d3-166">id</span></span> | <span data-ttu-id="768d3-167">Un identificador único, generado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-167">A unique, generated ID for the element.</span></span> <span data-ttu-id="768d3-168">Devuelto por [solicitudes GET al punto de conexión del *contenido* de una página](/graph/api/page-get?view=graph-rest-1.0) cuando se usa la opción de consulta `includeIDs=true`.</span><span class="sxs-lookup"><span data-stu-id="768d3-168">Returned by [GET requests to a page's *content* endpoint](/graph/api/page-get?view=graph-rest-1.0) when the `includeIDs=true` query option is used.</span></span><br/><br/><span data-ttu-id="768d3-169">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-169">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-170">style</span><span class="sxs-lookup"><span data-stu-id="768d3-170">style</span></span> | <span data-ttu-id="768d3-171">Las propiedades de posición y tamaño del div.</span><span class="sxs-lookup"><span data-stu-id="768d3-171">The position and size properties of the div.</span></span> |
 
### <a name="non-contributing-divs"></a><span data-ttu-id="768d3-172">Div que no contribuyen</span><span class="sxs-lookup"><span data-stu-id="768d3-172">Non-contributing divs</span></span>

<span data-ttu-id="768d3-173">Cuando un elemento **div** en el HTML de entrada no contribuye a la estructura de la página o lleva información que OneNote usa, la API mueve el contenido del div al div primario o predeterminado.</span><span class="sxs-lookup"><span data-stu-id="768d3-173">When a **div** element in the input HTML does not contribute to the page structure or carry information that OneNote uses, the API moves the div's content into the parent or default div.</span></span> <span data-ttu-id="768d3-174">Se muestra en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="768d3-174">This is illustrated in the following examples.</span></span>

#### <a name="input-html"></a><span data-ttu-id="768d3-175">HTML de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-175">Input HTML</span></span>

<span data-ttu-id="768d3-176">Contiene un div anidado de no contribución.</span><span class="sxs-lookup"><span data-stu-id="768d3-176">Contains a non-contributing, nested div.</span></span>

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

#### <a name="output-html"></a><span data-ttu-id="768d3-177">HTML de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-177">Output HTML</span></span>

> <span data-ttu-id="768d3-178">**Nota:** El contenido del div se movió al div principal y se eliminaron las etiquetas `<div>` anidadas.</span><span class="sxs-lookup"><span data-stu-id="768d3-178">**Note:** The div's content was moved to the parent div and the nested `<div>` tags have been removed.</span></span> <span data-ttu-id="768d3-179">El div se habría conservado si hubiera definido cualquier información semántica, como un **data-id** (ejemplo: `<div data-id="keep-me">`).</span><span class="sxs-lookup"><span data-stu-id="768d3-179">The div would have been preserved if it defined any semantic information, such as a **data-id** (example: `<div data-id="keep-me">`).</span></span>

```html
<html htmlns="https://www.w3.org/1999/xhtml" lang="en-US">
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


## <a name="img-elements"></a><span data-ttu-id="768d3-180">Elementos img</span><span class="sxs-lookup"><span data-stu-id="768d3-180">Img elements</span></span>

<span data-ttu-id="768d3-181">Las imágenes en las páginas de OneNote están representadas por elementos **img**.</span><span class="sxs-lookup"><span data-stu-id="768d3-181">Images on OneNote pages are represented by **img** elements.</span></span> <span data-ttu-id="768d3-182">Un elemento **img** puede contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="768d3-182">An **img** element can contain the following attributes in the input and output HTML.</span></span>

#### <a name="input-attributes"></a><span data-ttu-id="768d3-183">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-183">Input attributes</span></span>

|<span data-ttu-id="768d3-184">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-184">Input attribute</span></span>|<span data-ttu-id="768d3-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-185">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-186">alt</span><span class="sxs-lookup"><span data-stu-id="768d3-186">alt</span></span> | <span data-ttu-id="768d3-187">El texto alternativo que se proporciona para la imagen.</span><span class="sxs-lookup"><span data-stu-id="768d3-187">The supplied alt text for the image.</span></span> |
| <span data-ttu-id="768d3-188">data-id</span><span class="sxs-lookup"><span data-stu-id="768d3-188">data-id</span></span> | <span data-ttu-id="768d3-189">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-189">A reference for the element.</span></span><br/><br/><span data-ttu-id="768d3-190">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-190">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-191">data-render-src</span><span class="sxs-lookup"><span data-stu-id="768d3-191">data-render-src</span></span> |<span data-ttu-id="768d3-192">Se necesita **data-render-src** o **src**.</span><span class="sxs-lookup"><span data-stu-id="768d3-192">Either **data-render-src** or **src** is required.</span></span><br/><br/><span data-ttu-id="768d3-193">La página web para representar como imagen como mapa de bits en la página de OneNote:</span><span class="sxs-lookup"><span data-stu-id="768d3-193">The webpage to render as a bit-mapped image on the OneNote page:</span></span><br/><br/> <span data-ttu-id="768d3-194">- `data-render-src="https://..."` para una dirección URL pública.</span><span class="sxs-lookup"><span data-stu-id="768d3-194">- `data-render-src="https://..."` for a public URL.</span></span><br/><br/> <span data-ttu-id="768d3-195">- `data-render-src="name:BlockName"` para una parte de imagen en el bloque "Presentación" de una [solicitud de varias partes](/graph/api/section-post-pages?view=graph-rest-1.0#example).</span><span class="sxs-lookup"><span data-stu-id="768d3-195">- `data-render-src="name:BlockName"` for an image part in the "Presentation" block of a [multipart request](/graph/api/section-post-pages?view=graph-rest-1.0#example).</span></span><br/><br/><span data-ttu-id="768d3-196">Este método es útil cuando la página web es más compleja que la página que OneNote puede representar fielmente, o cuando la página requiere credenciales de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="768d3-196">This method is useful when the webpage is more complex than the OneNote page can faithfully render, or when the page requires login credentials.</span></span>|
| <span data-ttu-id="768d3-197">etiqueta de datos</span><span class="sxs-lookup"><span data-stu-id="768d3-197">data-tag</span></span> | <span data-ttu-id="768d3-198">Una [etiqueta de nota](onenote-note-tags.md) en el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-198">A [note tag](onenote-note-tags.md) on the element.</span></span> |
| <span data-ttu-id="768d3-199">style</span><span class="sxs-lookup"><span data-stu-id="768d3-199">style</span></span> |<span data-ttu-id="768d3-200">Las propiedades de posición y tamaño de la imagen: **posición** (**absoluta** solo), **izquierda**, **arriba**, **ancho** y **alto**.</span><span class="sxs-lookup"><span data-stu-id="768d3-200">The position and size properties for the image: **position** (**absolute** only), **left**, **top**, **width**, and **height**.</span></span><br/><br/><span data-ttu-id="768d3-201">El tamaño se puede establecer en cualquier imagen.</span><span class="sxs-lookup"><span data-stu-id="768d3-201">Size can be set on any image.</span></span><br/><br/><span data-ttu-id="768d3-202">Las propiedades de posición se usan para crear una imagen [con posición absoluta](onenote-abs-pos.md), solo si la imagen es un elemento secundario directo del cuerpo cuando el cuerpo indica `data-absolute-enabled="true"`.</span><span class="sxs-lookup"><span data-stu-id="768d3-202">Position properties are used to create an [absolute positioned](onenote-abs-pos.md) image, only if the image is a direct child of the body when the body sets `data-absolute-enabled="true"`.</span></span><br/><br/><span data-ttu-id="768d3-203">Ejemplo: `<img style="position:absolute;width:360px;top:350px;left:300px" ... />`</span><span class="sxs-lookup"><span data-stu-id="768d3-203">Example: `<img style="position:absolute;width:360px;top:350px;left:300px" ... />`</span></span><br/><br/><span data-ttu-id="768d3-204">En el HTML de salida, el tamaño de la imagen se devuelve por separado en los atributos **width** y **height**.</span><span class="sxs-lookup"><span data-stu-id="768d3-204">In the output HTML, the image size is returned separately in **width** and **height** attributes.</span></span> |
| <span data-ttu-id="768d3-205">src</span><span class="sxs-lookup"><span data-stu-id="768d3-205">src</span></span> |<span data-ttu-id="768d3-206">Se necesita **src** o **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="768d3-206">Either **src** or **data-render-src** is required.</span></span><br/><br/><span data-ttu-id="768d3-207">La imagen para representar en la página de OneNote:</span><span class="sxs-lookup"><span data-stu-id="768d3-207">The image to render on the OneNote page:</span></span><br/><br/><span data-ttu-id="768d3-208">- `src="https://..."` para una dirección URL a una imagen disponible públicamente en Internet.</span><span class="sxs-lookup"><span data-stu-id="768d3-208">- `src="https://..."` for a URL to a publicly available image on the internet.</span></span><br/><br/> <span data-ttu-id="768d3-209">- `src="name:BlockName"` para una parte con nombre en una solicitud con varias partes que representa a la imagen.</span><span class="sxs-lookup"><span data-stu-id="768d3-209">- `src="name:BlockName"` for a named part in a multipart request that represents the image.</span></span>|
| <span data-ttu-id="768d3-210">width, height</span><span class="sxs-lookup"><span data-stu-id="768d3-210">width, height</span></span> | <span data-ttu-id="768d3-211">El ancho o alto de la imagen, en píxeles pero sin px.</span><span class="sxs-lookup"><span data-stu-id="768d3-211">The width or height of the image, in pixels but without the px.</span></span> <span data-ttu-id="768d3-212">Ejemplo: `width="400"`</span><span class="sxs-lookup"><span data-stu-id="768d3-212">Example: `width="400"`</span></span> |
 
> <span data-ttu-id="768d3-213">**Nota**: Las API de OneNote detectan automáticamente el tipo de imagen de entrada y lo devuelven como el **data-fullres-src-type** en el HTML de salida.</span><span class="sxs-lookup"><span data-stu-id="768d3-213">**Note:** The OneNote APIs automatically detect the input image type, and returns it as the **data-fullres-src-type** in the output HTML.</span></span> <span data-ttu-id="768d3-214">La API también devuelve el tipo de imagen de la imagen optimizada en **data-src-type**.</span><span class="sxs-lookup"><span data-stu-id="768d3-214">The API also returns the image type of the optimized image in **data-src-type**.</span></span>
 

#### <a name="output-attributes"></a><span data-ttu-id="768d3-215">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-215">Output attributes</span></span>

|<span data-ttu-id="768d3-216">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-216">Output attribute</span></span>|<span data-ttu-id="768d3-217">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-217">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-218">alt</span><span class="sxs-lookup"><span data-stu-id="768d3-218">alt</span></span> | <span data-ttu-id="768d3-219">El texto alternativo que se proporciona para la imagen.</span><span class="sxs-lookup"><span data-stu-id="768d3-219">The supplied alt text for the image.</span></span> |
| <span data-ttu-id="768d3-220">data-id</span><span class="sxs-lookup"><span data-stu-id="768d3-220">data-id</span></span> | <span data-ttu-id="768d3-221">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-221">A reference for the element.</span></span><br/><br/><span data-ttu-id="768d3-222">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-222">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-223">data-index</span><span class="sxs-lookup"><span data-stu-id="768d3-223">data-index</span></span> | <span data-ttu-id="768d3-p118">La posición de la imagen. Para compatibilidad con [imagen dividida](#split-images).</span><span class="sxs-lookup"><span data-stu-id="768d3-p118">The position of the image. For [split image](#split-images) support.</span></span> |
| <span data-ttu-id="768d3-226">data-fullres-src</span><span class="sxs-lookup"><span data-stu-id="768d3-226">data-fullres-src</span></span> | <span data-ttu-id="768d3-227">El extremo para la versión del recurso de la imagen que se incrustó originalmente en la página.</span><span class="sxs-lookup"><span data-stu-id="768d3-227">The endpoint for the version of the image resource that was originally embedded in the page.</span></span> |
| <span data-ttu-id="768d3-228">data-fullres-src-type</span><span class="sxs-lookup"><span data-stu-id="768d3-228">data-fullres-src-type</span></span> | <span data-ttu-id="768d3-229">El tipo de medios del recurso **data-fullres-src**. Por ejemplo: `image/png` o `image/jpeg`.</span><span class="sxs-lookup"><span data-stu-id="768d3-229">The media type of the **data-fullres-src** resource, for example: `image/png` or `image/jpeg`.</span></span> |
| <span data-ttu-id="768d3-230">data-options</span><span class="sxs-lookup"><span data-stu-id="768d3-230">data-options</span></span> | <span data-ttu-id="768d3-p119">El tipo de origen: **printout** para archivos PDF o **splitimage** para todos los demás. Se aplica únicamente a [imágenes divididas](#split-images) creadas con el atributo **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="768d3-p119">The source type: **printout** for PDF files or **splitimage** for all others. Applies only to [split images](#split-images) created with the **data-render-src** attribute.</span></span> |
| <span data-ttu-id="768d3-233">data-render-original-src</span><span class="sxs-lookup"><span data-stu-id="768d3-233">data-render-original-src</span></span> | <span data-ttu-id="768d3-234">La dirección URL de origen de la imagen, si la imagen de origen proviene de Internet pública y se creó con el atributo **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="768d3-234">The original source URL of the image, if the source image is from the public internet and was created with the **data-render-src** attribute.</span></span> |
| <span data-ttu-id="768d3-235">data-src-type</span><span class="sxs-lookup"><span data-stu-id="768d3-235">data-src-type</span></span> | <span data-ttu-id="768d3-236">El tipo de medios del recurso **src**. Por ejemplo: `image/png` o `image/jpeg`.</span><span class="sxs-lookup"><span data-stu-id="768d3-236">The media type of the **src** resource, for example: `image/png` or `image/jpeg`.</span></span> |
| <span data-ttu-id="768d3-237">etiqueta de datos</span><span class="sxs-lookup"><span data-stu-id="768d3-237">data-tag</span></span> | <span data-ttu-id="768d3-238">Una [etiqueta de nota](onenote-note-tags.md) en el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-238">A [note tag](onenote-note-tags.md) on the element.</span></span> |
| <span data-ttu-id="768d3-239">id</span><span class="sxs-lookup"><span data-stu-id="768d3-239">id</span></span> | <span data-ttu-id="768d3-240">Un identificador único, generado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-240">A unique, generated ID for the element.</span></span> <span data-ttu-id="768d3-241">Devuelto por [solicitudes GET al punto de conexión del *contenido* de una página](/graph/api/page-get?view=graph-rest-1.0) cuando se usa la opción de consulta `includeIDs=true`.</span><span class="sxs-lookup"><span data-stu-id="768d3-241">Returned by [GET requests to a page's *content* endpoint](/graph/api/page-get?view=graph-rest-1.0) when the `includeIDs=true` query option is used.</span></span><br/><br/><span data-ttu-id="768d3-242">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-242">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-243">src</span><span class="sxs-lookup"><span data-stu-id="768d3-243">src</span></span> | <span data-ttu-id="768d3-244">El extremo para la versión del recurso de imagen que se ha optimizado para exploradores web y factores de forma móviles y de tabletas.</span><span class="sxs-lookup"><span data-stu-id="768d3-244">The endpoint for the version of the image resource that has been optimized for web browsers and mobile and tablet form factors.</span></span> |
| <span data-ttu-id="768d3-245">style</span><span class="sxs-lookup"><span data-stu-id="768d3-245">style</span></span> | <span data-ttu-id="768d3-246">Las propiedades de posición de la imagen.</span><span class="sxs-lookup"><span data-stu-id="768d3-246">The position properties of the image.</span></span> |
| <span data-ttu-id="768d3-247">width, height</span><span class="sxs-lookup"><span data-stu-id="768d3-247">width, height</span></span> | <span data-ttu-id="768d3-248">El ancho o alto de la imagen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="768d3-248">The width or height of the image, in pixels.</span></span> |
 

### <a name="output-html-examples-for-images"></a><span data-ttu-id="768d3-249">Ejemplos de HTML de salida para imágenes</span><span class="sxs-lookup"><span data-stu-id="768d3-249">Output HTML examples for images</span></span>

<span data-ttu-id="768d3-250">Los elementos **img** de salida contienen puntos de conexión para los recursos de archivo de imagen y el tipo de imagen, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="768d3-250">Output **img** elements contain endpoints for image file resources and the image type, as shown below.</span></span> <span data-ttu-id="768d3-251">Puede hacer [solicitudes GET independientes a puntos de conexión de recursos de imagen](/graph/api/resource-get?view=graph-rest-1.0) para recuperar su contenido binario.</span><span class="sxs-lookup"><span data-stu-id="768d3-251">You can make separate [GET requests to image resource endpoints](/graph/api/resource-get?view=graph-rest-1.0) to retrieve their binary contents.</span></span>

```html
<img 
    src="https://graph.microsoft.com/v1.0/me/onenote/resources/{image-id}/$value"  
    data-src-type="image/png"
    data-fullres-src="https://graph.microsoft.com/v1.0/me/onenote/resources/{image-id}/$value"  
    data-fullres-src-type="image/png" ... />
```

<span data-ttu-id="768d3-252">De forma predeterminada, las imágenes no se representarán directamente en un explorador porque son privadas y se necesita una autorización para recuperarlas, al igual que el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="768d3-252">By default, images won't render directly in a browser because they are private and require authorization to retrieve them, like the rest of the page contents.</span></span> <span data-ttu-id="768d3-253">Para obtener direcciones URL públicas a los recursos de imagen en una página, incluya **preAuthenticated=true** en la cadena de consulta cuando recupere el contenido de la página (ejemplo: `GET ../pages/{page-id}/content?preAuthenticated=true`).</span><span class="sxs-lookup"><span data-stu-id="768d3-253">To get public URLs to the image resources on a page, include **preAuthenticated=true** in the query string when you retrieve the page content (example: `GET ../pages/{page-id}/content?preAuthenticated=true`).</span></span> <span data-ttu-id="768d3-254">Las direcciones URL públicas que se devuelven son válidas durante una hora.</span><span class="sxs-lookup"><span data-stu-id="768d3-254">The public URLs that are returned are valid for one hour.</span></span> 

#### <a name="image-with-public-url-when-preauthenticatedtrue-is-included-in-the-request"></a><span data-ttu-id="768d3-255">Imagen con dirección URL pública cuando se incluye _preAuthenticated=true_ en la solicitud</span><span class="sxs-lookup"><span data-stu-id="768d3-255">Image with public URL when _preAuthenticated=true_ is included in the request</span></span>

```html
<img 
    width="170" height="128" 
    src="https://graph.microsoft.com/v1.0/me/onenote/resources/{image-id}/content?publicAuth=true&mimeType=image/jpeg" 
    data-src-type="image/{type}" 
    data-fullres-src="https://graph.microsoft.com/v1.0/me/onenote/resources/{image-id}/content?publicAuth=true&mimeType=image/jpeg" 
    data-fullres-src-type="image/{type}"
/>
```

<span data-ttu-id="768d3-256">Los siguientes ejemplos muestran la información que un elemento **img** podría contener en el HTML de salida.</span><span class="sxs-lookup"><span data-stu-id="768d3-256">The following examples show the information an **img** element might contain in the output HTML.</span></span>

#### <a name="image-with-web-ready-and-high-resolution-resources"></a><span data-ttu-id="768d3-257">Imagen con recursos de alta resolución y listos para la web</span><span class="sxs-lookup"><span data-stu-id="768d3-257">Image with web-ready and high resolution resources</span></span>

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

#### <a name="image-created-by-using-the-data-render-src-attribute"></a><span data-ttu-id="768d3-258">Imagen creada mediante el atributo *data-render-src*</span><span class="sxs-lookup"><span data-stu-id="768d3-258">Image created by using the *data-render-src* attribute</span></span>

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

### <a name="split-images"></a><span data-ttu-id="768d3-259">Imágenes divididas</span><span class="sxs-lookup"><span data-stu-id="768d3-259">Split images</span></span>

<span data-ttu-id="768d3-260">Las imágenes que se crean mediante el atributo **data-render-src** (de una dirección URL de una página web o una parte con nombre) podrían dividirse en varias componentes de imágenes por motivos de representación y de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="768d3-260">Images that are created using the **data-render-src** attribute (from a webpage URL or a named part) might be split into multiple component images for performance and rendering reasons.</span></span> <span data-ttu-id="768d3-261">A todos los componentes de imágenes se les asigna el mismo valor **data-id**.</span><span class="sxs-lookup"><span data-stu-id="768d3-261">Component images are all assigned the same **data-id** value.</span></span> <span data-ttu-id="768d3-262">Cada componente de imagen tiene un atributo de índice de datos de base cero que define el diseño vertical original.</span><span class="sxs-lookup"><span data-stu-id="768d3-262">Each component image has a zero-based data-index attribute that defines the original vertical layout.</span></span>

#### <a name="split-image-with-three-component-images"></a><span data-ttu-id="768d3-263">Imagen dividida con tres imágenes con componente</span><span class="sxs-lookup"><span data-stu-id="768d3-263">Split image with three component images</span></span>

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

<span data-ttu-id="768d3-264">Debido a que los usuarios pueden mover las imágenes en la página, los índices devueltos pueden estar desordenados.</span><span class="sxs-lookup"><span data-stu-id="768d3-264">Because users can move the images on the page, the returned indexes might be out of order.</span></span> <span data-ttu-id="768d3-265">El orden debe estar en orden descendente en el eje y, y de izquierda a derecha en el eje x, si hay conflictos en el eje y.</span><span class="sxs-lookup"><span data-stu-id="768d3-265">Ordering should be in top to bottom y-order, then left to right x-order if there are y-order conflicts.</span></span>

## <a name="iframe-elements"></a><span data-ttu-id="768d3-266">Elementos iframe</span><span class="sxs-lookup"><span data-stu-id="768d3-266">iframe elements</span></span>

<span data-ttu-id="768d3-267">Las páginas de OneNote pueden contener vídeos insertados representados por elementos **iframe**.</span><span class="sxs-lookup"><span data-stu-id="768d3-267">OneNote pages can contain embedded videos represented by **iframe** elements.</span></span> 

> <span data-ttu-id="768d3-268">**Nota**: También puede [adjuntar un archivo de vídeo mediante un elemento **object**](onenote-images-files.md#adding-files).</span><span class="sxs-lookup"><span data-stu-id="768d3-268">**Note:** You can also [attach a video file using an **object** element](onenote-images-files.md#adding-files).</span></span>

#### <a name="input-attributes"></a><span data-ttu-id="768d3-269">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-269">Input attributes</span></span>

|<span data-ttu-id="768d3-270">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-270">Input attribute</span></span>|<span data-ttu-id="768d3-271">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-271">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-272">data-original-src</span><span class="sxs-lookup"><span data-stu-id="768d3-272">data-original-src</span></span> | <span data-ttu-id="768d3-273">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="768d3-273">Required.</span></span> <span data-ttu-id="768d3-274">La dirección URL del origen del vídeo.</span><span class="sxs-lookup"><span data-stu-id="768d3-274">The URL of the video source.</span></span> <span data-ttu-id="768d3-275">Consulte la [lista de orígenes de vídeo compatibles](onenote-images-files.md#adding-videos).</span><span class="sxs-lookup"><span data-stu-id="768d3-275">See the [list of supported video sources](onenote-images-files.md#adding-videos).</span></span> <br/><br/><span data-ttu-id="768d3-276">Ejemplo: `data-original-src="https://www.youtube.com/watch?v=3Ztr44aKmQ8"`</span><span class="sxs-lookup"><span data-stu-id="768d3-276">Example: `data-original-src="https://www.youtube.com/watch?v=3Ztr44aKmQ8"`</span></span> |
| <span data-ttu-id="768d3-277">width, height</span><span class="sxs-lookup"><span data-stu-id="768d3-277">width, height</span></span> | <span data-ttu-id="768d3-278">El ancho o alto del iframe, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="768d3-278">The width or height of the iframe, in pixels.</span></span> <span data-ttu-id="768d3-279">Ejemplo: `width=300`</span><span class="sxs-lookup"><span data-stu-id="768d3-279">Example: `width=300`</span></span> |

#### <a name="output-attributes"></a><span data-ttu-id="768d3-280">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-280">Output attributes</span></span>

|<span data-ttu-id="768d3-281">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-281">Output attribute</span></span>|<span data-ttu-id="768d3-282">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-282">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-283">data-original-src</span><span class="sxs-lookup"><span data-stu-id="768d3-283">data-original-src</span></span> | <span data-ttu-id="768d3-284">La dirección URL del origen del vídeo.</span><span class="sxs-lookup"><span data-stu-id="768d3-284">The URL of the video source.</span></span> |
| <span data-ttu-id="768d3-285">src</span><span class="sxs-lookup"><span data-stu-id="768d3-285">src</span></span> | <span data-ttu-id="768d3-286">Un vínculo al vídeo que está insertado en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="768d3-286">A link to the video that is embedded in the OneNote page.</span></span> |
| <span data-ttu-id="768d3-287">width, height</span><span class="sxs-lookup"><span data-stu-id="768d3-287">width, height</span></span> | <span data-ttu-id="768d3-288">El ancho o alto del iframe, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="768d3-288">The width or height of the iframe, in pixels.</span></span><br/><br/><span data-ttu-id="768d3-289">Ejemplo: `width=300`</span><span class="sxs-lookup"><span data-stu-id="768d3-289">Example: `width=300`</span></span> |
 
### <a name="output-html-example-for-videos"></a><span data-ttu-id="768d3-290">Ejemplo de HTML de salida para vídeos</span><span class="sxs-lookup"><span data-stu-id="768d3-290">Output HTML example for videos</span></span>

<span data-ttu-id="768d3-291">Los elementos **iframe** de salida contienen los puntos de conexión que vinculan a la página de origen y el vídeo, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="768d3-291">Output **iframe** elements contain endpoints that link to the source page and video, as shown.</span></span> 

```html
<iframe 
    width="340" height="280" 
    data-original-src="https://www.youtube.com/watch?v=3Ztr44aKmQ8" 
    src="https://www.youtube.com/embed/3Ztr44aKmQ8?feature=oembed&autoplay=true" />
``` 

## <a name="object-elements"></a><span data-ttu-id="768d3-292">Elementos object</span><span class="sxs-lookup"><span data-stu-id="768d3-292">Object elements</span></span>

<span data-ttu-id="768d3-293">Las páginas de OneNote pueden contener archivos adjuntos representados por elementos **object**.</span><span class="sxs-lookup"><span data-stu-id="768d3-293">OneNote pages can contain file attachments represented by **object** elements.</span></span> <span data-ttu-id="768d3-294">Un elemento **object** puede contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="768d3-294">An **object** element can contain the following attributes in the input and output HTML.</span></span>

> <span data-ttu-id="768d3-295">**Nota**: Las API de OneNote también pueden representar el contenido de archivos como imágenes en una página cuando el archivo se envía como imagen y usa el atributo **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="768d3-295">**Note:** The OneNote APIs can also render file content as images in a page when the file is sent as an image and uses the **data-render-src** attribute.</span></span>
> <span data-ttu-id="768d3-296">Ejemplo: `<img data-render-src="name:part-name" ... />`</span><span class="sxs-lookup"><span data-stu-id="768d3-296">Example: `<img data-render-src="name:part-name" ... />`</span></span>
 

#### <a name="input-attributes"></a><span data-ttu-id="768d3-297">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-297">Input attributes</span></span>

|<span data-ttu-id="768d3-298">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-298">Input attribute</span></span>|<span data-ttu-id="768d3-299">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-299">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-300">data</span><span class="sxs-lookup"><span data-stu-id="768d3-300">data</span></span> | <span data-ttu-id="768d3-301">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="768d3-301">Required.</span></span> <span data-ttu-id="768d3-302">El nombre de la parte que representa el archivo en una [solicitud de varias partes](/graph/api/section-post-pages?view=graph-rest-1.0#example).</span><span class="sxs-lookup"><span data-stu-id="768d3-302">The name of the part that represents the file in the [multipart request](/graph/api/section-post-pages?view=graph-rest-1.0#example).</span></span> |
| <span data-ttu-id="768d3-303">data-attachment</span><span class="sxs-lookup"><span data-stu-id="768d3-303">data-attachment</span></span> | <span data-ttu-id="768d3-p130">Obligatorio. El nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="768d3-p130">Required. The file name.</span></span> |
| <span data-ttu-id="768d3-306">data-id</span><span class="sxs-lookup"><span data-stu-id="768d3-306">data-id</span></span> | <span data-ttu-id="768d3-307">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-307">A reference for the element.</span></span><br/><br/><span data-ttu-id="768d3-308">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-308">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-309">style</span><span class="sxs-lookup"><span data-stu-id="768d3-309">style</span></span> | <span data-ttu-id="768d3-310">Las propiedades de posición y tamaño del objeto: **posición** (**absoluta** solo), **izquierda**, **arriba** y **ancho**.</span><span class="sxs-lookup"><span data-stu-id="768d3-310">The position and size properties for the object: **position** (**absolute** only), **left**, **top**, and **width**.</span></span><br/><br/><span data-ttu-id="768d3-311">Se usa para crear un objeto [con posición absoluta](onenote-abs-pos.md), solo si el objeto es un elemento secundario directo del cuerpo cuando el cuerpo indica `data-absolute-enabled="true"`.</span><span class="sxs-lookup"><span data-stu-id="768d3-311">Used to create an [absolute positioned](onenote-abs-pos.md) object, only if the object is a direct child of the body when the body sets `data-absolute-enabled="true"`.</span></span><br/><br/><span data-ttu-id="768d3-312">Ejemplo: `<object style="position:absolute;top:350px;left:300px" ... />`</span><span class="sxs-lookup"><span data-stu-id="768d3-312">Example: `<object style="position:absolute;top:350px;left:300px" ... />`</span></span> |
| <span data-ttu-id="768d3-313">type</span><span class="sxs-lookup"><span data-stu-id="768d3-313">type</span></span> | <span data-ttu-id="768d3-314">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="768d3-314">Required.</span></span><br/><br/><span data-ttu-id="768d3-315">El tipo de archivo de medios estándar.</span><span class="sxs-lookup"><span data-stu-id="768d3-315">The standard media file type.</span></span> <span data-ttu-id="768d3-316">Los tipos de archivo conocidos muestran el icono asociado con el tipo de archivo en la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="768d3-316">Known file types display the icon associated with the file type on the OneNote page.</span></span> <span data-ttu-id="768d3-317">Los tipos de archivo desconocidos muestran un icono de archivo genérico.</span><span class="sxs-lookup"><span data-stu-id="768d3-317">Unknown file types display a generic file icon.</span></span> |
<!--todo: add link to known file types--> 

#### <a name="output-attributes"></a><span data-ttu-id="768d3-318">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-318">Output attributes</span></span>

|<span data-ttu-id="768d3-319">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-319">Output attribute</span></span>|<span data-ttu-id="768d3-320">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-320">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-321">data</span><span class="sxs-lookup"><span data-stu-id="768d3-321">data</span></span> | <span data-ttu-id="768d3-322">El extremo para el recurso de archivo.</span><span class="sxs-lookup"><span data-stu-id="768d3-322">The endpoint for the file resource.</span></span> |
| <span data-ttu-id="768d3-323">data-attachment</span><span class="sxs-lookup"><span data-stu-id="768d3-323">data-attachment</span></span> | <span data-ttu-id="768d3-324">El nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="768d3-324">The file name.</span></span> |
| <span data-ttu-id="768d3-325">data-id</span><span class="sxs-lookup"><span data-stu-id="768d3-325">data-id</span></span> | <span data-ttu-id="768d3-326">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-326">A reference for the element.</span></span><br/><br/><span data-ttu-id="768d3-327">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-327">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-328">id</span><span class="sxs-lookup"><span data-stu-id="768d3-328">id</span></span> | <span data-ttu-id="768d3-329">Un identificador único, generado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-329">A unique, generated ID for the element.</span></span> <span data-ttu-id="768d3-330">Devuelto por [solicitudes GET al punto de conexión del *contenido* de una página](/graph/api/page-get?view=graph-rest-1.0) cuando se usa la opción de consulta `includeIDs=true`.</span><span class="sxs-lookup"><span data-stu-id="768d3-330">Returned by [GET requests to a page's *content* endpoint](/graph/api/page-get?view=graph-rest-1.0) when the `includeIDs=true` query option is used.</span></span><br/><br/><span data-ttu-id="768d3-331">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-331">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-332">style</span><span class="sxs-lookup"><span data-stu-id="768d3-332">style</span></span> | <span data-ttu-id="768d3-333">Las propiedades de posición del objeto.</span><span class="sxs-lookup"><span data-stu-id="768d3-333">The position properties of the object.</span></span> |
| <span data-ttu-id="768d3-334">type</span><span class="sxs-lookup"><span data-stu-id="768d3-334">type</span></span> | <span data-ttu-id="768d3-335">El tipo de archivo de medios estándar.</span><span class="sxs-lookup"><span data-stu-id="768d3-335">The standard media file type.</span></span> |
 

#### <a name="output-html-example-for-objects"></a><span data-ttu-id="768d3-336">Ejemplo HTML de salida para objetos</span><span class="sxs-lookup"><span data-stu-id="768d3-336">Output HTML example for objects</span></span>

<span data-ttu-id="768d3-337">Los elementos **object** de salida contienen puntos de conexión que vinculan a los recursos de archivo en la página, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="768d3-337">Output **object** elements contain endpoints that link to the file resources in the page, as shown.</span></span> <span data-ttu-id="768d3-338">Puede hacer [solicitudes GET independientes a puntos de conexión de recursos de archivo](/graph/api/resource-get?view=graph-rest-1.0) para recuperar su contenido binario.</span><span class="sxs-lookup"><span data-stu-id="768d3-338">You can make separate [GET requests to file resource endpoints](/graph/api/resource-get?view=graph-rest-1.0) to retrieve their binary contents.</span></span>

```html
<object
    data="https://graph.microsoft.com/v1.0/me/onenote/resources/{file-id}/$value"
    data-attachment="fileName.pdf" 
    type="application/pdf" 
    [style="..."] />
``` 

## <a name="paragraphs-and-headings"></a><span data-ttu-id="768d3-339">Párrafos y encabezados</span><span class="sxs-lookup"><span data-stu-id="768d3-339">Paragraphs and headings</span></span>

<span data-ttu-id="768d3-340">Los párrafos, encabezados y otros contenedores de texto pueden contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="768d3-340">Paragraphs, headings, and other text containers can contain the following attributes in the input and output HTML.</span></span>

#### <a name="input-attributes"></a><span data-ttu-id="768d3-341">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-341">Input attributes</span></span>

|<span data-ttu-id="768d3-342">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-342">Input attribute</span></span>|<span data-ttu-id="768d3-343">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-343">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-344">data-id</span><span class="sxs-lookup"><span data-stu-id="768d3-344">data-id</span></span> | <span data-ttu-id="768d3-345">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-345">A reference for the element.</span></span><br/><br/><span data-ttu-id="768d3-346">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-346">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-347">etiqueta de datos</span><span class="sxs-lookup"><span data-stu-id="768d3-347">data-tag</span></span> | <span data-ttu-id="768d3-348">Una [etiqueta de nota](onenote-note-tags.md) en un elemento de **p** o **h1** - **h6**.</span><span class="sxs-lookup"><span data-stu-id="768d3-348">A [note tag](onenote-note-tags.md) on a **p** or **h1** - **h6** element.</span></span> |
| <span data-ttu-id="768d3-349">style</span><span class="sxs-lookup"><span data-stu-id="768d3-349">style</span></span> | <span data-ttu-id="768d3-350">Las propiedades CSS [style](#styles) del elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-350">The CSS [style](#styles) properties of the element.</span></span> |
 

#### <a name="output-attributes"></a><span data-ttu-id="768d3-351">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-351">Output attributes</span></span>

|<span data-ttu-id="768d3-352">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-352">Output attribute</span></span>|<span data-ttu-id="768d3-353">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-353">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-354">data-id</span><span class="sxs-lookup"><span data-stu-id="768d3-354">data-id</span></span> | <span data-ttu-id="768d3-355">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-355">A reference for the element.</span></span><br/><br/><span data-ttu-id="768d3-356">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-356">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-357">etiqueta de datos</span><span class="sxs-lookup"><span data-stu-id="768d3-357">data-tag</span></span> | <span data-ttu-id="768d3-358">Una [etiqueta de nota](onenote-note-tags.md) en un elemento de **p** o **h1** - **h6**.</span><span class="sxs-lookup"><span data-stu-id="768d3-358">A [note tag](onenote-note-tags.md) on a **p** or **h1** - **h6** element.</span></span> |
| <span data-ttu-id="768d3-359">id</span><span class="sxs-lookup"><span data-stu-id="768d3-359">id</span></span> | <span data-ttu-id="768d3-360">Un identificador único, generado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-360">A unique, generated ID for the element.</span></span> <span data-ttu-id="768d3-361">Devuelto por [solicitudes GET al punto de conexión del *contenido* de una página](/graph/api/page-get?view=graph-rest-1.0) cuando se usa la opción de consulta `includeIDs=true`.</span><span class="sxs-lookup"><span data-stu-id="768d3-361">Returned by [GET requests to a page's *content* endpoint](/graph/api/page-get?view=graph-rest-1.0) when the `includeIDs=true` query option is used.</span></span><br/><br/><span data-ttu-id="768d3-362">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-362">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-363">style</span><span class="sxs-lookup"><span data-stu-id="768d3-363">style</span></span> | <span data-ttu-id="768d3-364">Las propiedades CSS [style](#styles) del elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-364">The CSS [style](#styles) properties of the element.</span></span> <span data-ttu-id="768d3-365">En el HTML de salida, estos valores podrían devolverse insertados en los elementos secundarios adecuados o en elementos **span**.</span><span class="sxs-lookup"><span data-stu-id="768d3-365">In the output HTML, these values may be returned inline on appropriate child elements or on **span** elements.</span></span> |
 

<span data-ttu-id="768d3-366">Los siguientes ejemplos muestran HTML de entrada que usa diferentes maneras de definir estilos en contenedores de texto y el HTML de salida que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="768d3-366">The following examples show input HTML that uses different ways to define styles on text containers and the output HTML that's returned.</span></span>

#### <a name="input-html-with-styles-defined-using-inline-character-styles-in-the-start-tag-and-within-a-span-element"></a><span data-ttu-id="768d3-367">HTML de entrada con estilos definidos mediante estilos de caracteres en línea, en la etiqueta de inicio, y dentro de un elemento span.</span><span class="sxs-lookup"><span data-stu-id="768d3-367">Input HTML with styles defined using inline character styles, in the start tag, and within a span element.</span></span>

```html
<h1>Heading <i>One</i> text</h1>
<p style="font-size:8pt;color:green;font-family:Courier;text-align:center">Some text</p>
<p>Some <span  style="font-size:16px;color:#ff0000;font-family:Segoe UI Black">more</span> text</p>
``` 

#### <a name="output-html-with-the-i-character-style-and-the-font-settings-in-the-p-start-tag-returned-as-inline-css-styles-on-span-elements"></a><span data-ttu-id="768d3-368">HTML de salida con el estilo de caracteres `<i>` y la configuración de fuentes en la etiqueta de inicio `<p>` devuelta como estilos CSS insertados en elementos span.</span><span class="sxs-lookup"><span data-stu-id="768d3-368">Output HTML with the `<i>` character style and the font settings in the `<p>` start tag returned as inline CSS styles on span elements.</span></span>

```html
<h1 style="font-size:16pt;color:#1e4e79;margin-top:11pt;margin-bottom:11pt">Heading <span style="font-style:italic">One</span> text</h1>
<p style="text-align:center"><span style="font-family:Courier;font-size:8pt;color:green">Some text</span></p>
<p>Some <span style="font-family:Segoe UI Black;font-size:12pt;color:red">more</span> text</p>
``` 


## <a name="lists"></a><span data-ttu-id="768d3-369">Listas</span><span class="sxs-lookup"><span data-stu-id="768d3-369">Lists</span></span>

<span data-ttu-id="768d3-370">Las listas se representan como elementos **ol** o **ul** que contienen elementos list representados como **li**.</span><span class="sxs-lookup"><span data-stu-id="768d3-370">Lists are represented as **ol** or **ul** elements that contain list items represented as **li** elements.</span></span>

<span data-ttu-id="768d3-371">Los elementos lists y list pueden contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="768d3-371">Lists and list items can contain the following attributes in the input and output HTML.</span></span>

#### <a name="input-attributes"></a><span data-ttu-id="768d3-372">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-372">Input attributes</span></span>

|<span data-ttu-id="768d3-373">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-373">Input attribute</span></span>|<span data-ttu-id="768d3-374">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-374">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-375">data-id</span><span class="sxs-lookup"><span data-stu-id="768d3-375">data-id</span></span> | <span data-ttu-id="768d3-376">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-376">A reference for the element.</span></span><br/><br/><span data-ttu-id="768d3-377">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-377">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-378">etiqueta de datos</span><span class="sxs-lookup"><span data-stu-id="768d3-378">data-tag</span></span> | <span data-ttu-id="768d3-379">Una [etiqueta de nota](onenote-note-tags.md) en un elemento de **ul**, **ol** o de **li**.</span><span class="sxs-lookup"><span data-stu-id="768d3-379">A [note tag](onenote-note-tags.md) on a **ul**, **ol**, or **li** element.</span></span> |
| <span data-ttu-id="768d3-380">style</span><span class="sxs-lookup"><span data-stu-id="768d3-380">style</span></span> | <span data-ttu-id="768d3-381">Las propiedades CSS **list-style-type** y [style](#styles) para la lista o el elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="768d3-381">The **list-style-type** and the CSS [style](#styles) properties for the list or list item.</span></span> |
 

#### <a name="output-attributes"></a><span data-ttu-id="768d3-382">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-382">Output attributes</span></span>

|<span data-ttu-id="768d3-383">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-383">Output attribute</span></span>|<span data-ttu-id="768d3-384">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-384">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-385">data-id</span><span class="sxs-lookup"><span data-stu-id="768d3-385">data-id</span></span> | <span data-ttu-id="768d3-386">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-386">A reference for the element.</span></span><br/><br/><span data-ttu-id="768d3-387">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-387">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-388">etiqueta de datos</span><span class="sxs-lookup"><span data-stu-id="768d3-388">data-tag</span></span> |  <span data-ttu-id="768d3-389">Una [etiqueta de nota](onenote-note-tags.md) en un span en un elemento de **li**.</span><span class="sxs-lookup"><span data-stu-id="768d3-389">A [note tag](onenote-note-tags.md) on a span in a **li** element.</span></span> |
| <span data-ttu-id="768d3-390">id</span><span class="sxs-lookup"><span data-stu-id="768d3-390">id</span></span> | <span data-ttu-id="768d3-391">Un identificador único, generado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-391">A unique, generated ID for the element.</span></span> <span data-ttu-id="768d3-392">Devuelto por [solicitudes GET al punto de conexión del *contenido* de una página](/graph/api/page-get?view=graph-rest-1.0) cuando se usa la opción de consulta `includeIDs=true`.</span><span class="sxs-lookup"><span data-stu-id="768d3-392">Returned by [GET requests to a page's *content* endpoint](/graph/api/page-get?view=graph-rest-1.0) when the `includeIDs=true` query option is used.</span></span><br/><br/><span data-ttu-id="768d3-393">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-393">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-394">style</span><span class="sxs-lookup"><span data-stu-id="768d3-394">style</span></span> | <span data-ttu-id="768d3-395">Las propiedades **list-style-type** y CSS [style](#styles) del elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-395">The **list-style-type** and CSS [style](#styles) properties of the element.</span></span> <span data-ttu-id="768d3-396">En el HTML de salida, la configuración de nivel de lista se devuelve en elementos list.</span><span class="sxs-lookup"><span data-stu-id="768d3-396">In the output HTML, list-level settings are returned on list items.</span></span> <span data-ttu-id="768d3-397">No se devuelven las propiedades predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="768d3-397">Default properties are not returned.</span></span> |
 
### <a name="list-styles"></a><span data-ttu-id="768d3-398">Estilos de lista</span><span class="sxs-lookup"><span data-stu-id="768d3-398">List styles</span></span>

<span data-ttu-id="768d3-399">Las API de OneNote en Microsoft Graph admiten los siguientes estilos de lista:</span><span class="sxs-lookup"><span data-stu-id="768d3-399">The OneNote APIs in Microsoft Graph support the following list styles:</span></span>

|<span data-ttu-id="768d3-400">Lista ordenada</span><span class="sxs-lookup"><span data-stu-id="768d3-400">Ordered list</span></span>|<span data-ttu-id="768d3-401">Lista no ordenada</span><span class="sxs-lookup"><span data-stu-id="768d3-401">Unordered list</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-402">ninguno</span><span class="sxs-lookup"><span data-stu-id="768d3-402">none</span></span> | <span data-ttu-id="768d3-403">ninguno</span><span class="sxs-lookup"><span data-stu-id="768d3-403">none</span></span> |
| <span data-ttu-id="768d3-404">
decimal (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="768d3-404">decimal (default)</span></span> | <span data-ttu-id="768d3-405">
disc (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="768d3-405">disc (default)</span></span> |
| <span data-ttu-id="768d3-406">
lower-alpha</span><span class="sxs-lookup"><span data-stu-id="768d3-406">lower-alpha</span></span> | <span data-ttu-id="768d3-407">
circle</span><span class="sxs-lookup"><span data-stu-id="768d3-407">circle</span></span> |
| <span data-ttu-id="768d3-408">
lower-roman</span><span class="sxs-lookup"><span data-stu-id="768d3-408">lower-roman</span></span> | <span data-ttu-id="768d3-409">

square</span><span class="sxs-lookup"><span data-stu-id="768d3-409">square</span></span> |
| <span data-ttu-id="768d3-410">
upper-alpha</span><span class="sxs-lookup"><span data-stu-id="768d3-410">upper-alpha</span></span> | &nbsp; |
| <span data-ttu-id="768d3-411">
upper-roman</span><span class="sxs-lookup"><span data-stu-id="768d3-411">upper-roman</span></span> | &nbsp; |
 
<span data-ttu-id="768d3-412">Puede aplicar estilos globales para una lista en el elemento **ol** o **ul** del HTML de entrada, pero los estilos se devuelven en los elementos **li**.</span><span class="sxs-lookup"><span data-stu-id="768d3-412">You can apply global styles for a list on the **ol** or **ul** element in the input HTML, but styles are returned on the **li** elements.</span></span>

#### <a name="homogenous-list-style"></a><span data-ttu-id="768d3-413">Estilo de lista homogénea</span><span class="sxs-lookup"><span data-stu-id="768d3-413">Homogenous list style</span></span>

<span data-ttu-id="768d3-414">Este ejemplo muestra el HTML de entrada que establece el tipo de estilo de lista en el elemento **ol** y estilos CSS en elementos de listas individuales.</span><span class="sxs-lookup"><span data-stu-id="768d3-414">This example shows input HTML that sets the list style type on the **ol** element and CSS styles on individual list items.</span></span>

```html
<ol style="list-style-type:upper-roman;color:blue">
    <li style="font-weight:bold">Jacksonville</li>
    <li style="text-decoration:line-through">Orlando</li>
    <li style="font-family:Courier">Naples</li>
</ol>
``` 

<span data-ttu-id="768d3-p138">Este es el HTML de salida. Observe que los estilos se devuelven en línea en los elementos **li** o **span** individuales.</span><span class="sxs-lookup"><span data-stu-id="768d3-p138">This is the output HTML. Notice that styles are returned inline on the individual **li** or **span** elements.</span></span>

```html
<ol>
    <li style="list-style-type:upper-roman"><span style="color:blue;font-weight:bold">Jacksonville</span></li>
    <li style="list-style-type:upper-roman"><span style="color:blue;text-decoration:line-through">Orlando</span></li>
    <li style="list-style-type:upper-roman"><span style="font-family:Courier;color:blue">Naples</span></li>
</ol>
``` 

#### <a name="variable-list-styles"></a><span data-ttu-id="768d3-417">Estilos de listas variables</span><span class="sxs-lookup"><span data-stu-id="768d3-417">Variable list styles</span></span>

<span data-ttu-id="768d3-418">Este ejemplo muestra HTML de entrada que establece diferentes tipos de estilos de listas en los elementos **li**.</span><span class="sxs-lookup"><span data-stu-id="768d3-418">This example shows input HTML that sets different list style types on the **li** elements.</span></span>

```html
<ul style="font-style:italic">
    <li style="list-style-type:square">square style</li>
    <li style="list-style-type:circle">circle style</li>
    <li style="list-style-type:disc">disc style (default)</li>
</ul>
``` 

<span data-ttu-id="768d3-p139">Este es el HTML de salida. Observe que los estilos se devuelven en línea en los elementos **li** o **span** individuales.</span><span class="sxs-lookup"><span data-stu-id="768d3-p139">This is the output HTML. Notice that styles are returned inline on the individual **li** or **span** elements.</span></span>

```html
<ul>
    <li style="list-style-type:square"><span style="font-style:italic">square style</span></li>
    <li style="list-style-type:circle"><span style="font-style:italic">circle style</span></li>
    <li><span style="font-style:italic">disc style (default)</span></li>
</ul>
``` 


## <a name="tables"></a><span data-ttu-id="768d3-421">Tablas</span><span class="sxs-lookup"><span data-stu-id="768d3-421">Tables</span></span>

<span data-ttu-id="768d3-p140">Las tablas se representan como elementos **table** que pueden contener elementos **tr** y **td**. Se admiten tablas anidadas.</span><span class="sxs-lookup"><span data-stu-id="768d3-p140">Tables are represented as **table** elements that can contain **tr** and **td** elements. Nested tables are supported.</span></span>

<span data-ttu-id="768d3-424">Las tablas pueden contener los siguientes atributos en el HTML de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="768d3-424">Tables can contain the following attributes in the input and output HTML.</span></span> <span data-ttu-id="768d3-425">Las API de OneNote no admiten los atributos **rowspan** o **colspan**.</span><span class="sxs-lookup"><span data-stu-id="768d3-425">The OneNote APIs do not support **rowspan** or **colspan** attributes.</span></span> 

#### <a name="input-attributes"></a><span data-ttu-id="768d3-426">Atributos de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-426">Input attributes</span></span>

|<span data-ttu-id="768d3-427">Atributo de entrada</span><span class="sxs-lookup"><span data-stu-id="768d3-427">Input attribute</span></span>|<span data-ttu-id="768d3-428">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-428">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-429">data-id</span><span class="sxs-lookup"><span data-stu-id="768d3-429">data-id</span></span> | <span data-ttu-id="768d3-430">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-430">A reference for the element.</span></span><br/><br/><span data-ttu-id="768d3-431">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-431">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-432">style</span><span class="sxs-lookup"><span data-stu-id="768d3-432">style</span></span> | <span data-ttu-id="768d3-433">Las propiedades CSS [style](#styles) del elemento y también:</span><span class="sxs-lookup"><span data-stu-id="768d3-433">The CSS [style](#styles) properties of the element, and also:</span></span><br/> <span data-ttu-id="768d3-434">- **border**.</span><span class="sxs-lookup"><span data-stu-id="768d3-434">- **border**.</span></span> <span data-ttu-id="768d3-435">Puede ser 0px o 1px.</span><span class="sxs-lookup"><span data-stu-id="768d3-435">Can be either 0px or 1px.</span></span><br/> <span data-ttu-id="768d3-436">- **width**.</span><span class="sxs-lookup"><span data-stu-id="768d3-436">- **width**.</span></span> <span data-ttu-id="768d3-437">Compatible con **table** y **td** como píxeles o porcentaje de ancho de página.</span><span class="sxs-lookup"><span data-stu-id="768d3-437">Supported by **table** and **td** as pixels or percentage of page width.</span></span><br/><br/><span data-ttu-id="768d3-438">Por ejemplo, `width="100px"` o `width="60%"`</span><span class="sxs-lookup"><span data-stu-id="768d3-438">Example: `width="100px"` or `width="60%"`</span></span> |
 

#### <a name="output-attributes"></a><span data-ttu-id="768d3-439">Atributos de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-439">Output attributes</span></span>

|<span data-ttu-id="768d3-440">Atributo de salida</span><span class="sxs-lookup"><span data-stu-id="768d3-440">Output attribute</span></span>|<span data-ttu-id="768d3-441">Descripción</span><span class="sxs-lookup"><span data-stu-id="768d3-441">Description</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-442">data-id</span><span class="sxs-lookup"><span data-stu-id="768d3-442">data-id</span></span> | <span data-ttu-id="768d3-443">Una referencia para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-443">A reference for the element.</span></span><br/><br/><span data-ttu-id="768d3-444">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-444">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-445">id</span><span class="sxs-lookup"><span data-stu-id="768d3-445">id</span></span> | <span data-ttu-id="768d3-446">Un identificador único, generado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-446">A unique, generated ID for the element.</span></span> <span data-ttu-id="768d3-447">Devuelto por [solicitudes GET al punto de conexión del *contenido* de una página](/graph/api/page-get?view=graph-rest-1.0) cuando se usa la opción de consulta `includeIDs=true`.</span><span class="sxs-lookup"><span data-stu-id="768d3-447">Returned by [GET requests to a page's *content* endpoint](/graph/api/page-get?view=graph-rest-1.0) when the `includeIDs=true` query option is used.</span></span><br/><br/><span data-ttu-id="768d3-448">Se usa para [actualizar el contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-448">Used to [update page content](onenote-update-page.md).</span></span> |
| <span data-ttu-id="768d3-449">style</span><span class="sxs-lookup"><span data-stu-id="768d3-449">style</span></span> | <span data-ttu-id="768d3-450">Las propiedades CSS [style](#styles) del elemento.</span><span class="sxs-lookup"><span data-stu-id="768d3-450">The CSS [style](#styles) properties of the element.</span></span> |
 

<span data-ttu-id="768d3-451">Los siguientes ejemplos muestran HTML de entrada que usa diferentes maneras de definir estilos en tablas y el HTML de salida que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="768d3-451">The following examples show input HTML that uses different ways to define styles on tables and the output HTML that's returned.</span></span>

#### <a name="input-html-with-optional-settings-at-different-levels"></a><span data-ttu-id="768d3-452">HTML de entrada con configuración opcional en diferentes niveles.</span><span class="sxs-lookup"><span data-stu-id="768d3-452">Input HTML with optional settings at different levels.</span></span>

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
 
#### <a name="output-html-with-css-styles-returned-inline-on-the-td-elements"></a><span data-ttu-id="768d3-453">HTML de salida con estilos CSS devueltos en línea en los elementos td.</span><span class="sxs-lookup"><span data-stu-id="768d3-453">Output HTML with CSS styles returned inline on the td elements.</span></span>

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


## <a name="styles"></a><span data-ttu-id="768d3-454">Estilos</span><span class="sxs-lookup"><span data-stu-id="768d3-454">Styles</span></span>

<span data-ttu-id="768d3-455">Las API de OneNote en Microsoft Graph admiten las siguientes propiedades CSS **style** insertadas para elementos en el cuerpo de la página, como **body**, **div**, **p**, **li** y **span**.</span><span class="sxs-lookup"><span data-stu-id="768d3-455">OneNote APIs in Microsoft Graph support the following inline CSS **style** properties for elements in the page body, such as **body**, **div**, **p**, **li**, and **span**.</span></span>

|<span data-ttu-id="768d3-456">Propiedad</span><span class="sxs-lookup"><span data-stu-id="768d3-456">Property</span></span>|<span data-ttu-id="768d3-457">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="768d3-457">Example</span></span>|
|:------|:------|
| <span data-ttu-id="768d3-458">background-color</span><span class="sxs-lookup"><span data-stu-id="768d3-458">background-color</span></span> | <span data-ttu-id="768d3-459">`style="background-color:#66cc66"` (el valor predeterminado es blanco)</span><span class="sxs-lookup"><span data-stu-id="768d3-459">`style="background-color:#66cc66"` (defaults to white)</span></span><br/><br/><span data-ttu-id="768d3-460">Se admiten tanto en formato hexadecimal y colores con nombre.</span><span class="sxs-lookup"><span data-stu-id="768d3-460">Both hexadecimal format and named colors are supported.</span></span> |
| <span data-ttu-id="768d3-461">color</span><span class="sxs-lookup"><span data-stu-id="768d3-461">color</span></span> | <span data-ttu-id="768d3-462">`style="color:#ffffff"` (el valor predeterminado es negro)</span><span class="sxs-lookup"><span data-stu-id="768d3-462">`style="color:#ffffff"` (defaults to black)</span></span> |
| <span data-ttu-id="768d3-463">font-family</span><span class="sxs-lookup"><span data-stu-id="768d3-463">font-family</span></span> | <span data-ttu-id="768d3-464">`style="font-family:Courier"` (el valor predeterminado es Calibri)</span><span class="sxs-lookup"><span data-stu-id="768d3-464">`style="font-family:Courier"` (defaults to Calibri)</span></span> |
| <span data-ttu-id="768d3-465">font-size</span><span class="sxs-lookup"><span data-stu-id="768d3-465">font-size</span></span> | <span data-ttu-id="768d3-466">`style="font-size:10pt"`(el valor predeterminado es 11pt)</span><span class="sxs-lookup"><span data-stu-id="768d3-466">`style="font-size:10pt"` (defaults to 11pt)</span></span><br/><br/><span data-ttu-id="768d3-467">Las API aceptan el tamaño de fuente en *pt* o *px*, pero convierten *px* a *pt*.</span><span class="sxs-lookup"><span data-stu-id="768d3-467">The APIs accept font size in *pt* or *px*, but converts *px* to *pt*.</span></span> <span data-ttu-id="768d3-468">Los valores decimales se redondean al más próximo n.0pt o n.5pt.</span><span class="sxs-lookup"><span data-stu-id="768d3-468">Decimal values are rounded to the nearest n.0pt or n.5pt.</span></span> |
| <span data-ttu-id="768d3-469">font-style</span><span class="sxs-lookup"><span data-stu-id="768d3-469">font-style</span></span> | <span data-ttu-id="768d3-470">`style="font-style:italic"`(solo normal o cursiva)</span><span class="sxs-lookup"><span data-stu-id="768d3-470">`style="font-style:italic"` (normal or italic only)</span></span> |
| <span data-ttu-id="768d3-471">font-weight</span><span class="sxs-lookup"><span data-stu-id="768d3-471">font-weight</span></span> | <span data-ttu-id="768d3-472">`style="font-weight:bold"`(solo normal o negrita)</span><span class="sxs-lookup"><span data-stu-id="768d3-472">`style="font-weight:bold"` (normal or bold only)</span></span> |
| <span data-ttu-id="768d3-473">strike-through</span><span class="sxs-lookup"><span data-stu-id="768d3-473">strike-through</span></span> | `style="text-decoration:line-through"` |
| <span data-ttu-id="768d3-474">text-align</span><span class="sxs-lookup"><span data-stu-id="768d3-474">text-align</span></span> | <span data-ttu-id="768d3-475">`style="text-align:center"`(solo para elementos de bloque)</span><span class="sxs-lookup"><span data-stu-id="768d3-475">`style="text-align:center"` (for block elements only)</span></span> |
| <span data-ttu-id="768d3-476">text-decoration</span><span class="sxs-lookup"><span data-stu-id="768d3-476">text-decoration</span></span> | <span data-ttu-id="768d3-477">`style="text-decoration:underline"` (ninguno o solo subrayado)</span><span class="sxs-lookup"><span data-stu-id="768d3-477">`style="text-decoration:underline"` (none or underline only)</span></span> |
 

<span data-ttu-id="768d3-478">También se admiten los siguientes estilos de caracteres insertados:</span><span class="sxs-lookup"><span data-stu-id="768d3-478">The following inline character styles and are also supported:</span></span>

<table id="simpletable">
<tr>
<td id="simplecell"><span data-ttu-id="768d3-479"><n></span><span class="sxs-lookup"><span data-stu-id="768d3-479"><b></span></span></td>
<td id="simplecell"><span data-ttu-id="768d3-480"><k></span><span class="sxs-lookup"><span data-stu-id="768d3-480"><i></span></span></td>
<td id="simplecell"><span data-ttu-id="768d3-481"><s></span><span class="sxs-lookup"><span data-stu-id="768d3-481"><u></span></span></td>
</tr>
<tr>
<td id="simplecell"><span data-ttu-id="768d3-482"><em></span><span class="sxs-lookup"><span data-stu-id="768d3-482"><em></span></span></td>
<td id="simplecell"><span data-ttu-id="768d3-483"><Texto en negrita.></span><span class="sxs-lookup"><span data-stu-id="768d3-483"><strong></span></span></td>
<td id="simplecell"><span data-ttu-id="768d3-484"><Tachado></span><span class="sxs-lookup"><span data-stu-id="768d3-484"><strike></span></span></td>
</tr>
<tr>
<td id="simplecell"><span data-ttu-id="768d3-485"><sup></span><span class="sxs-lookup"><span data-stu-id="768d3-485"><sup></span></span></td>
<td id="simplecell"><span data-ttu-id="768d3-486"><sub></span><span class="sxs-lookup"><span data-stu-id="768d3-486"><sub></span></span></td>
<td id="simplecell"><span data-ttu-id="768d3-487"><supr></span><span class="sxs-lookup"><span data-stu-id="768d3-487"><del></span></span></td>
</tr>
<tr>
<td id="simplecell"><span data-ttu-id="768d3-488"><cite></span><span class="sxs-lookup"><span data-stu-id="768d3-488"><cite></span></span></td>
<td id="simplecell">&nbsp;</td>
<td id="simplecell">&nbsp;</td>
</tr>
</table>

 
## <a name="input-and-output-html-example"></a><span data-ttu-id="768d3-489">HTML de entrada y salida de ejemplo</span><span class="sxs-lookup"><span data-stu-id="768d3-489">Input and output HTML example</span></span>

<span data-ttu-id="768d3-490">La siguiente imagen muestra una página simple que se creó con Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="768d3-490">The following image shows a simple page that was created with Microsoft Graph.</span></span>

![Imagen de una página de OneNote con notas de estudio de contenido de Wikipedia](images/onenote-sample-image.png)

<span data-ttu-id="768d3-492">Este es el HTML de entrada que se envió en el cuerpo del mensaje para crear la página.</span><span class="sxs-lookup"><span data-stu-id="768d3-492">This is the input HTML sent in the message body to create the page.</span></span>

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
        <img alt="Apollo 11 commemorative stamp." src="https://upload.wikimedia.org/wikipedia/commons/a/a4/First_Man_on_Moon_1969_Issue-10c.jpg"  width="400"/>
        <p>References:</p>
        <p><a href="https://en.wikipedia.org/wiki/Apollo_11">https://en.wikipedia.org/wiki/Apollo_11</a></p>
        <p><a href="https://www.nasa.gov/mission_pages/apollo/missions/apollo11.html">https://www.nasa.gov/mission_pages/apollo/missions/apollo11.html</a></p>
    </body>
</html>
``` 

<br/>

<span data-ttu-id="768d3-493">Este es el HTML de salida que Microsoft Graph devuelve cuando [obtiene el contenido de la página](onenote-get-content.md).</span><span class="sxs-lookup"><span data-stu-id="768d3-493">This is the output HTML that Microsoft Graph returns when you [get page content](onenote-get-content.md).</span></span>

> <span data-ttu-id="768d3-494">**Nota**: Cuando [crea una página](onenote-create-page.md) u [obtiene los metadatos de una página](/graph/api/page-get?view=graph-rest-1.0), la API devuelve la dirección URL del punto de conexión del *contenido* de la página en la propiedad **contentUrl**.</span><span class="sxs-lookup"><span data-stu-id="768d3-494">**Note:** When you [create a page](onenote-create-page.md) or [get page metadata](/graph/api/page-get?view=graph-rest-1.0), the API returns the *content* endpoint URL of the page in the **contentUrl** property.</span></span>

```html
<html htmlns="https://www.w3.org/1999/xhtml" lang="en-US">
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
            <p><a href="https://en.wikipedia.org/wiki/Apollo_11">https://en.wikipedia.org/wiki/Apollo_11</a></p>
            <p><a href="https://www.nasa.gov/mission_pages/apollo/missions/apollo11.html">https://www.nasa.gov/mission_pages/apollo/missions/apollo11.html</a></p>
        </div>
    </body>
</html>
``` 

## <a name="see-also"></a><span data-ttu-id="768d3-495">Consulte también</span><span class="sxs-lookup"><span data-stu-id="768d3-495">See also</span></span>

- [<span data-ttu-id="768d3-496">Obtener el contenido y la estructura de OneNote</span><span class="sxs-lookup"><span data-stu-id="768d3-496">Get OneNote content and structure</span></span>](onenote-get-content.md)
- [<span data-ttu-id="768d3-497">Crear páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="768d3-497">Create OneNote pages</span></span>](onenote-create-page.md)
- [<span data-ttu-id="768d3-498">Actualizar el contenido de la página de OneNote</span><span class="sxs-lookup"><span data-stu-id="768d3-498">Update OneNote page content</span></span>](onenote-update-page.md)
- [<span data-ttu-id="768d3-499">Agregar imágenes, vídeos y archivos</span><span class="sxs-lookup"><span data-stu-id="768d3-499">Add images, videos, and files</span></span>](onenote-images-files.md)
