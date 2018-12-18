---
title: Crear elementos con posición absoluta en páginas de OneNote
description: El cuerpo de una página de OneNote puede contener varios elementos secundarios `div`, `img` y `object` directos que pueden colocarse en la página por separado.
author: Jewan-microsoft
ms.openlocfilehash: 37e6fb88ff7738c273cd0a3ef9debfe5c6ef8975
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321073"
---
# <a name="create-absolute-positioned-elements-in-onenote-pages"></a><span data-ttu-id="784a4-103">Crear elementos con posición absoluta en páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="784a4-103">Create absolute positioned elements in OneNote pages</span></span>

<span data-ttu-id="784a4-104">El cuerpo de una página de OneNote puede contener varios elementos secundarios `div`, `img` y `object` directos que pueden colocarse en la página por separado.</span><span class="sxs-lookup"><span data-stu-id="784a4-104">The body of a OneNote page can contain multiple direct `div`, `img`, and `object` child elements that can be positioned independently on the page.</span></span>

<a name="attributes"></a>

## <a name="attributes-and-positioning-behavior"></a><span data-ttu-id="784a4-105">Comportamiento de posicionamiento y atributos</span><span class="sxs-lookup"><span data-stu-id="784a4-105">Attributes and positioning behavior</span></span>

<span data-ttu-id="784a4-106">Use los atributos `data-absolute-enabled` y [`style`](#supported-css-style-attributes) para crear elementos con posición absoluta en una página, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="784a4-106">Use the `data-absolute-enabled` and [`style`](#supported-css-style-attributes) attributes to create absolute positioned elements on a page, as follows:</span></span>

- <span data-ttu-id="784a4-107">El elemento de cuerpo debe especificar `data-absolute-enabled="true"`.</span><span class="sxs-lookup"><span data-stu-id="784a4-107">The body element must specify `data-absolute-enabled="true"`.</span></span> <span data-ttu-id="784a4-108">Si se omite o establece en `false`, todo el contenido del cuerpo se representa dentro de una div con posición absoluta `_default` que la API ha creado, y se ignora la configuración de posición.</span><span class="sxs-lookup"><span data-stu-id="784a4-108">If omitted or set to `false`, all body content is rendered inside a `_default` absolute positioned div that the API creates, and all position settings are ignored.</span></span>

- <span data-ttu-id="784a4-109">Solo los elementos `div`, `img` y `object` pueden ser elementos con posición absoluta.</span><span class="sxs-lookup"><span data-stu-id="784a4-109">Only `div`, `img`, and `object` elements can be absolute positioned elements.</span></span> 

- <span data-ttu-id="784a4-110">Los elementos con posición absoluta deben especificar `style="position:absolute"`.</span><span class="sxs-lookup"><span data-stu-id="784a4-110">Absolute positioned elements must specify `style="position:absolute"`.</span></span>

- <span data-ttu-id="784a4-111">Los elementos con posición absolutos deben ser secundarios directos del elemento `body`.</span><span class="sxs-lookup"><span data-stu-id="784a4-111">Absolute positioned elements must be direct children of the `body` element.</span></span> <span data-ttu-id="784a4-112">Cualquier secundario directo del cuerpo que no sea un elemento `div`, `img` o `object` con posición absoluta se representa como contenido estático dentro de la div `_default` con posición absoluta.</span><span class="sxs-lookup"><span data-stu-id="784a4-112">Any direct children of the body that aren't absolute positioned `div`, `img`, or `object` elements are rendered as static content inside the absolute positioned `_default` div.</span></span>

- <span data-ttu-id="784a4-113">Los elementos con posición absoluta tienen su posición en las coordenadas superior e izquierda especificadas, relativas a la posición inicial 0:0 en el extremo superior izquierdo de la página encima del área de título.</span><span class="sxs-lookup"><span data-stu-id="784a4-113">Absolute positioned elements are positioned at their specified top and left coordinates, relative to the 0:0 starting position at the top, left corner of the page above the title area.</span></span>

- <span data-ttu-id="784a4-114">Si un elemento con posición absoluta omite las coordenadas superior o izquierda, la coordenada que falta se establece en el valor predeterminado: `top:120px` o `left:48px`.</span><span class="sxs-lookup"><span data-stu-id="784a4-114">If an absolute positioned element omits the top or left coordinate, the missing coordinate is set to its default value: `top:120px` or `left:48px`.</span></span> <span data-ttu-id="784a4-115">Estas coordenadas predeterminadas especifican una posición justo debajo del área de título.</span><span class="sxs-lookup"><span data-stu-id="784a4-115">These default coordinates specify a position just below the title area.</span></span> <span data-ttu-id="784a4-116">Tenga en cuenta que omitir coordenadas puede traducirse en elementos que aparecen apilados uno encima de otro.</span><span class="sxs-lookup"><span data-stu-id="784a4-116">Be aware that omitting coordinates can result in elements that are stacked on top of each other.</span></span>

- <span data-ttu-id="784a4-117">Los elementos con posición absoluta no se pueden anidar ni contener elementos con posición.</span><span class="sxs-lookup"><span data-stu-id="784a4-117">Absolute positioned elements cannot be nested or contain positioned elements.</span></span> <span data-ttu-id="784a4-118">La API omite cualquier configuración de la posición especificada en los elementos anidados dentro de una div con posición absoluta, procesa el contenido anidado dentro de la div primaria con posición absoluta y devuelve una advertencia en la propiedad **api.diagnostics** en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="784a4-118">The API ignores any position settings specified on nested elements inside an absolute positioned div, renders the nested content inside the absolute positioned parent div, and returns a warning in the **api.diagnostics** property in the response.</span></span>


### <a name="example"></a><span data-ttu-id="784a4-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="784a4-119">Example</span></span>

<span data-ttu-id="784a4-120">El ejemplo siguiente contiene un secundario `p` directo, una div con posición absoluta y una div sin posición absoluta.</span><span class="sxs-lookup"><span data-stu-id="784a4-120">The following example contains a direct `p` child, an absolute positioned div, and a non-absolute positioned div.</span></span>

#### <a name="input-html"></a><span data-ttu-id="784a4-121">HTML de entrada</span><span class="sxs-lookup"><span data-stu-id="784a4-121">Input HTML</span></span>  

   ```html 
   <body data-absolute-enabled="true">
       <p>This content will appear in the _default div.</p>
       <div style="position:absolute;top:175px;left:100px" data-id="div1">
         <p>This content will appear in an absolute positioned div.</p>
       </div>
       <div>
           <p>This content will also appear in the _default div.</p>
       </div>
   </body>
   ```

<span data-ttu-id="784a4-122">La API representa la div sin posición absoluta en la div predeterminada.</span><span class="sxs-lookup"><span data-stu-id="784a4-122">The API renders the non-absolute positioned div in the default div.</span></span> <span data-ttu-id="784a4-123">Tenga en cuenta que las etiquetas `<div>` anidadas se descartan porque no definen información semántica (como `data-id`).</span><span class="sxs-lookup"><span data-stu-id="784a4-123">Note that the nested `<div>` tags are discarded because they do not define any semantic information (such as `data-id`).</span></span>

#### <a name="output-html"></a><span data-ttu-id="784a4-124">HTML de salida</span><span class="sxs-lookup"><span data-stu-id="784a4-124">Output HTML</span></span> 

   ```html 
   <body data-absolute-enabled="true" style="font-family:Calibri;font-size:11pt">
       <div data-id="_default" style="position:absolute;left:48px;top:120px;width:624px">
           <p>This content will appear in the _default div.</p>
           <p>This content will also appear in the _default div.</p>
       </div>
       <div data-id="div1" style="position:absolute;left:99px;top:174px;width:624px">
           <p>This content will appear in an absolute positioned div.</p>
       </div>
   </body>
   ```

### <a name="example"></a><span data-ttu-id="784a4-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="784a4-125">Example</span></span>

<span data-ttu-id="784a4-126">El siguiente ejemplo crea una página que contiene una div con posición absoluta y una imagen con posición absoluta.</span><span class="sxs-lookup"><span data-stu-id="784a4-126">The following example creates a page that contains one absolute positioned div and one absolute positioned image.</span></span>


#### <a name="input-html"></a><span data-ttu-id="784a4-127">HTML de entrada</span><span class="sxs-lookup"><span data-stu-id="784a4-127">Input HTML</span></span>  

```html 
<html>
    <head>
        <title>Page Title</title>
    </head>
    <body data-absolute-enabled="true">
        <div style="position:absolute;width:280px;top:120px;left:68px">
            <p>Some text</p>
            <img style="width:120px" src="https://officeimg.vo.msecnd.net/en-us/files/018/949/ZA103278226.png" />
            <div>
                <p>More text inside a regular, nested div</p>
            </div>
        </div>
        <img style="position:absolute;width:360px;top:350px;left:300px" src="https://officeimg.vo.msecnd.net/en-us/files/018/949/ZA103278226.png" />
    </body>
</html>
```
 
<span data-ttu-id="784a4-128">La API de OneNote evalúa el HTML de entrada y conserva todo el contenido semántico y cualquier información estructural que es compatible con OneNote.</span><span class="sxs-lookup"><span data-stu-id="784a4-128">The OneNote API evaluates the input HTML and preserves all semantic content and any structural information that is supported by OneNote.</span></span> <span data-ttu-id="784a4-129">La página resultante se representa como se muestra en la siguiente imagen (pero sin los bordes de la imagen y div visibles).</span><span class="sxs-lookup"><span data-stu-id="784a4-129">The resulting page renders as shown in the following image (but without the visible borders for the div and image).</span></span> 

![Página resultante con imagen y div con posición absoluta](images/abs-pos.png)

<span data-ttu-id="784a4-131">Observe los cambios en la div anidada no colaborador del HTML de entrada.</span><span class="sxs-lookup"><span data-stu-id="784a4-131">Notice the changes to the non-contributing, nested div from the input HTML.</span></span> <span data-ttu-id="784a4-132">La API conserva el contenido de la div pero descarta las etiquetas `<div>` porque la div no define información semántica (como `data-id`).</span><span class="sxs-lookup"><span data-stu-id="784a4-132">The API preserves the div's content but discards the `<div>` tags because the div doesn't define semantic information (such as `data-id`).</span></span>

<span data-ttu-id="784a4-133">Para obtener más información sobre cómo la API de OneNote controla el HTML de entrada y salida, consulte [HTML de entrada y salida para páginas de OneNote](onenote-input-output-html.md).</span><span class="sxs-lookup"><span data-stu-id="784a4-133">For more information about how the OneNote API handles input and output HTML, see [Input and output HTML for OneNote pages](onenote-input-output-html.md).</span></span>

<a name="style-attributes"></a>

## <a name="supported-css-style-attributes"></a><span data-ttu-id="784a4-134">Atributos de estilo CSS compatibles</span><span class="sxs-lookup"><span data-stu-id="784a4-134">Supported CSS style attributes</span></span>

<span data-ttu-id="784a4-135">Todos los elementos con posición absoluta pueden especificar las posiciones superior e izquierda.</span><span class="sxs-lookup"><span data-stu-id="784a4-135">All absolute positioned elements can specify top and left positions.</span></span> <span data-ttu-id="784a4-136">Las div e imágenes pueden especificar la anchura y las imágenes también pueden especificar la altura.</span><span class="sxs-lookup"><span data-stu-id="784a4-136">Divs and images can specify width, and images can also specify height.</span></span> <span data-ttu-id="784a4-137">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="784a4-137">For example:</span></span>

```html
<img style="position:absolute;top:140px;left:95px;width:480px;height:665px" src="..." />
```

| <span data-ttu-id="784a4-138">Atributo</span><span class="sxs-lookup"><span data-stu-id="784a4-138">Attribute</span></span> | <span data-ttu-id="784a4-139">Elemento admitido</span><span class="sxs-lookup"><span data-stu-id="784a4-139">Supported element</span></span> | <span data-ttu-id="784a4-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="784a4-140">Description</span></span> |  
|:------|:------|:------|  
| <span data-ttu-id="784a4-141">top</span><span class="sxs-lookup"><span data-stu-id="784a4-141">top</span></span> | <span data-ttu-id="784a4-142">div, img, object</span><span class="sxs-lookup"><span data-stu-id="784a4-142">div, img, object</span></span> | <span data-ttu-id="784a4-143">Las coordenadas del eje y del borde superior del elemento, en píxeles únicamente.</span><span class="sxs-lookup"><span data-stu-id="784a4-143">The y-axis coordinate of the element's top border, in pixels only.</span></span> <span data-ttu-id="784a4-144">El valor predeterminado es 120 píxeles.</span><span class="sxs-lookup"><span data-stu-id="784a4-144">Default is 120 pixels.</span></span><br/><br/><span data-ttu-id="784a4-145">Ejemplo: `top:140px`</span><span class="sxs-lookup"><span data-stu-id="784a4-145">Example: `top:140px`</span></span> |  
| <span data-ttu-id="784a4-146">left</span><span class="sxs-lookup"><span data-stu-id="784a4-146">left</span></span> |  <span data-ttu-id="784a4-147">div, img, object</span><span class="sxs-lookup"><span data-stu-id="784a4-147">div, img, object</span></span>  | <span data-ttu-id="784a4-148">La coordenada del eje x del borde izquierdo del elemento en píxeles únicamente.</span><span class="sxs-lookup"><span data-stu-id="784a4-148">The x-axis coordinate of the element's left border, in pixels only.</span></span> <span data-ttu-id="784a4-149">El valor predeterminado es 48 píxeles.</span><span class="sxs-lookup"><span data-stu-id="784a4-149">Default is 48 pixels.</span></span><br/><br/><span data-ttu-id="784a4-150">Ejemplo: `left:95px`</span><span class="sxs-lookup"><span data-stu-id="784a4-150">Example: `left:95px`</span></span> |  
| <span data-ttu-id="784a4-151">width</span><span class="sxs-lookup"><span data-stu-id="784a4-151">width</span></span> |  <span data-ttu-id="784a4-152">div, img</span><span class="sxs-lookup"><span data-stu-id="784a4-152">div, img</span></span>  | <span data-ttu-id="784a4-153">La anchura del elemento, en píxeles únicamente.</span><span class="sxs-lookup"><span data-stu-id="784a4-153">The width of the element, in pixels only.</span></span><br/><br/><span data-ttu-id="784a4-154">Ejemplo: `width:480px`</span><span class="sxs-lookup"><span data-stu-id="784a4-154">Example: `width:480px`</span></span> |  
| <span data-ttu-id="784a4-155">height</span><span class="sxs-lookup"><span data-stu-id="784a4-155">height</span></span> | <span data-ttu-id="784a4-156">img</span><span class="sxs-lookup"><span data-stu-id="784a4-156">img</span></span> | <span data-ttu-id="784a4-157">La altura del elemento, en píxeles únicamente.</span><span class="sxs-lookup"><span data-stu-id="784a4-157">The height of the element, in pixels only.</span></span> <span data-ttu-id="784a4-158">Para div, se calcula la altura en runtime y se omite cualquier valor de altura especificado.</span><span class="sxs-lookup"><span data-stu-id="784a4-158">For divs, height is calculated at runtime and any specified height value is ignored.</span></span><br/><br/><span data-ttu-id="784a4-159">Ejemplo: `height:665px`</span><span class="sxs-lookup"><span data-stu-id="784a4-159">Example: `height:665px`</span></span> |  
 
<span data-ttu-id="784a4-160">Se ignoran otros atributos de posición, como `z-index`.</span><span class="sxs-lookup"><span data-stu-id="784a4-160">Other position attributes, such as `z-index`, are ignored.</span></span> <span data-ttu-id="784a4-161">Las imágenes con posición absolutas pueden usar el atributo `data-render-src` o `src`.</span><span class="sxs-lookup"><span data-stu-id="784a4-161">Absolute positioned images can use either the `data-render-src` or `src` attribute.</span></span>


<a name="request-response-info"></a>

## <a name="response-information"></a><span data-ttu-id="784a4-162">Información de respuesta</span><span class="sxs-lookup"><span data-stu-id="784a4-162">Response information</span></span>

<span data-ttu-id="784a4-163">La API de OneNote proporciona la siguiente información en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="784a4-163">The OneNote API returns the following information in the response.</span></span>

| <span data-ttu-id="784a4-164">Datos de respuesta</span><span class="sxs-lookup"><span data-stu-id="784a4-164">Response data</span></span> | <span data-ttu-id="784a4-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="784a4-165">Description</span></span> |  
|:------|:------|  
| <span data-ttu-id="784a4-166">Código correcto</span><span class="sxs-lookup"><span data-stu-id="784a4-166">Success code</span></span> | <span data-ttu-id="784a4-167">Un código de estado HTTP 201 para una solicitud POST correcta y un código de estado HTTP 204 para una solicitud PATCH correcta.</span><span class="sxs-lookup"><span data-stu-id="784a4-167">A 201 HTTP status code for a successful POST request, and a 204 HTTP status code for a successful PATCH request.</span></span> |  
| <span data-ttu-id="784a4-168">Errores</span><span class="sxs-lookup"><span data-stu-id="784a4-168">Errors</span></span> | <span data-ttu-id="784a4-169">Lea [Códigos de error para API de OneNote de Microsoft Graph](onenote-error-codes.md) para obtener información sobre los errores de OneNote que puede devolver Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="784a4-169">Read [Error codes for OneNote APIs in Microsoft Graph](onenote-error-codes.md) to learn about OneNote errors that Microsoft Graph can return.</span></span> |  
  


<a name="permissions"></a>

## <a name="permissions"></a><span data-ttu-id="784a4-170">Permisos</span><span class="sxs-lookup"><span data-stu-id="784a4-170">Permissions</span></span>

<span data-ttu-id="784a4-171">Para crear o actualizar páginas de OneNote, necesita solicitar los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="784a4-171">To create or update OneNote pages, you'll need to request appropriate permissions.</span></span> <span data-ttu-id="784a4-172">Seleccione el nivel inferior de permisos que necesita la aplicación para funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="784a4-172">Choose the lowest level of permissions that your app needs to do its work.</span></span>

#### <a name="permissions-for-post-pages"></a><span data-ttu-id="784a4-173">Permisos para páginas POST</span><span class="sxs-lookup"><span data-stu-id="784a4-173">Permissions for POST pages</span></span> 

- <span data-ttu-id="784a4-174">Notes.Create</span><span class="sxs-lookup"><span data-stu-id="784a4-174">Notes.Create</span></span>
- <span data-ttu-id="784a4-175">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="784a4-175">Notes.ReadWrite</span></span>
- <span data-ttu-id="784a4-176">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="784a4-176">Notes.ReadWrite.All</span></span>  


#### <a name="permissions-for-patch-pages"></a><span data-ttu-id="784a4-177">Permisos para páginas PATCH</span><span class="sxs-lookup"><span data-stu-id="784a4-177">Permissions for PATCH pages</span></span> 

- <span data-ttu-id="784a4-178">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="784a4-178">Notes.ReadWrite</span></span>
- <span data-ttu-id="784a4-179">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="784a4-179">Notes.ReadWrite.All</span></span>

<span data-ttu-id="784a4-180">Para obtener más información sobre los ámbitos de permiso y cómo funcionan, consulte los [ámbitos de permisos de OneNote](permissions-reference.md#notes-permissions).</span><span class="sxs-lookup"><span data-stu-id="784a4-180">For more information about permission scopes and how they work, see [OneNote permission scopes](permissions-reference.md#notes-permissions).</span></span>


<a name="see-also"></a>

## <a name="see-also"></a><span data-ttu-id="784a4-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="784a4-181">See also</span></span>

- [<span data-ttu-id="784a4-182">Crear páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="784a4-182">Create OneNote pages</span></span>](onenote-create-page.md)
- [<span data-ttu-id="784a4-183">Actualizar el contenido de la página de OneNote</span><span class="sxs-lookup"><span data-stu-id="784a4-183">Update OneNote page content</span></span>](onenote-update-page.md)
- [<span data-ttu-id="784a4-184">Integración con OneNote</span><span class="sxs-lookup"><span data-stu-id="784a4-184">Integrate with OneNote</span></span>](integrate-with-onenote.md)
- [<span data-ttu-id="784a4-185">Blog para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="784a4-185">OneNote Developer Blog</span></span>](https://go.microsoft.com/fwlink/?LinkID=390183)
- [<span data-ttu-id="784a4-186">Preguntas de desarrollo de OneNote en Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="784a4-186">OneNote development questions on Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkID=390182)
- [<span data-ttu-id="784a4-187">Repositorios de OneNote en GitHub</span><span class="sxs-lookup"><span data-stu-id="784a4-187">OneNote GitHub repos</span></span>](https://go.microsoft.com/fwlink/?LinkID=390178)  

