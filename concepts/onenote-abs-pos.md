---
title: Crear elementos con posición absoluta en páginas de OneNote
description: El cuerpo de una página de OneNote puede contener varios elementos secundarios `div`, `img` y `object` directos que pueden colocarse en la página por separado.
author: jewan-microsoft
localization_priority: Normal
ms.prod: onenote
ms.openlocfilehash: 9630741091be52de8791f560a13b225ccce2e218
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981171"
---
# <a name="create-absolute-positioned-elements-in-onenote-pages"></a>Crear elementos con posición absoluta en páginas de OneNote

El cuerpo de una página de OneNote puede contener varios elementos secundarios `div`, `img` y `object` directos que pueden colocarse en la página por separado.

<a name="attributes"></a>

## <a name="attributes-and-positioning-behavior"></a>Comportamiento de posicionamiento y atributos

Use los atributos `data-absolute-enabled` y [`style`](#supported-css-style-attributes) para crear elementos con posición absoluta en una página, como se indica a continuación:

- El elemento de cuerpo debe especificar `data-absolute-enabled="true"`. Si se omite o establece en `false`, todo el contenido del cuerpo se representa dentro de una div con posición absoluta `_default` que la API ha creado, y se ignora la configuración de posición.

- Solo los elementos `div`, `img` y `object` pueden ser elementos con posición absoluta. 

- Los elementos con posición absoluta deben especificar `style="position:absolute"`.

- Los elementos con posición absolutos deben ser secundarios directos del elemento `body`. Cualquier secundario directo del cuerpo que no sea un elemento `div`, `img` o `object` con posición absoluta se representa como contenido estático dentro de la div `_default` con posición absoluta.

- Los elementos con posición absoluta tienen su posición en las coordenadas superior e izquierda especificadas, relativas a la posición inicial 0:0 en el extremo superior izquierdo de la página encima del área de título.

- Si un elemento con posición absoluta omite las coordenadas superior o izquierda, la coordenada que falta se establece en el valor predeterminado: `top:120px` o `left:48px`. Estas coordenadas predeterminadas especifican una posición justo debajo del área de título. Tenga en cuenta que omitir coordenadas puede traducirse en elementos que aparecen apilados uno encima de otro.

- Los elementos con posición absoluta no se pueden anidar ni contener elementos con posición. La API omite cualquier configuración de la posición especificada en los elementos anidados dentro de una div con posición absoluta, procesa el contenido anidado dentro de la div primaria con posición absoluta y devuelve una advertencia en la propiedad **api.diagnostics** en la respuesta.


### <a name="example"></a>Ejemplo

El ejemplo siguiente contiene un secundario `p` directo, una div con posición absoluta y una div sin posición absoluta.

#### <a name="input-html"></a>HTML de entrada  

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

La API representa la div sin posición absoluta en la div predeterminada. Tenga en cuenta que las etiquetas `<div>` anidadas se descartan porque no definen información semántica (como `data-id`).

#### <a name="output-html"></a>HTML de salida 

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

### <a name="example"></a>Ejemplo

El siguiente ejemplo crea una página que contiene una div con posición absoluta y una imagen con posición absoluta.


#### <a name="input-html"></a>HTML de entrada  

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
 
La API de OneNote evalúa el HTML de entrada y conserva todo el contenido semántico y cualquier información estructural que es compatible con OneNote. La página resultante se representa como se muestra en la siguiente imagen (pero sin los bordes de la imagen y div visibles). 

![Página resultante con imagen y div con posición absoluta](images/abs-pos.png)

Observe los cambios en la div anidada no colaborador del HTML de entrada. La API conserva el contenido de la div pero descarta las etiquetas `<div>` porque la div no define información semántica (como `data-id`).

Para obtener más información sobre cómo la API de OneNote controla el HTML de entrada y salida, consulte [HTML de entrada y salida para páginas de OneNote](onenote-input-output-html.md).

<a name="style-attributes"></a>

## <a name="supported-css-style-attributes"></a>Atributos de estilo CSS compatibles

Todos los elementos con posición absoluta pueden especificar las posiciones superior e izquierda. Las div e imágenes pueden especificar la anchura y las imágenes también pueden especificar la altura. Por ejemplo:

```html
<img style="position:absolute;top:140px;left:95px;width:480px;height:665px" src="..." />
```

| Atributo | Elemento admitido | Descripción |  
|:------|:------|:------|  
| top | div, img, object | Las coordenadas del eje y del borde superior del elemento, en píxeles únicamente. El valor predeterminado es 120 píxeles.<br/><br/>Ejemplo: `top:140px` |  
| left |  div, img, object  | La coordenada del eje x del borde izquierdo del elemento en píxeles únicamente. El valor predeterminado es 48 píxeles.<br/><br/>Ejemplo: `left:95px` |  
| width |  div, img  | La anchura del elemento, en píxeles únicamente.<br/><br/>Ejemplo: `width:480px` |  
| height | img | La altura del elemento, en píxeles únicamente. Para div, se calcula la altura en runtime y se omite cualquier valor de altura especificado.<br/><br/>Ejemplo: `height:665px` |  
 
Se ignoran otros atributos de posición, como `z-index`. Las imágenes con posición absolutas pueden usar el atributo `data-render-src` o `src`.


<a name="request-response-info"></a>

## <a name="response-information"></a>Información de respuesta

La API de OneNote proporciona la siguiente información en la respuesta.

| Datos de respuesta | Descripción |  
|:------|:------|  
| Código correcto | Un código de estado HTTP 201 para una solicitud POST correcta y un código de estado HTTP 204 para una solicitud PATCH correcta. |  
| Errores | Lea [Códigos de error para API de OneNote de Microsoft Graph](onenote-error-codes.md) para obtener información sobre los errores de OneNote que puede devolver Microsoft Graph. |  
  


<a name="permissions"></a>

## <a name="permissions"></a>Permisos

Para crear o actualizar páginas de OneNote, necesita solicitar los permisos adecuados. Seleccione el nivel inferior de permisos que necesita la aplicación para funcionar correctamente.

#### <a name="permissions-for-post-pages"></a>Permisos para páginas POST 

- Notes.Create
- Notes.ReadWrite
- Notes.ReadWrite.All  


#### <a name="permissions-for-patch-pages"></a>Permisos para páginas PATCH 

- Notes.ReadWrite
- Notes.ReadWrite.All

Para obtener más información sobre los ámbitos de permiso y cómo funcionan, consulte los [ámbitos de permisos de OneNote](permissions-reference.md#notes-permissions).


<a name="see-also"></a>

## <a name="see-also"></a>Vea también

- [Crear páginas de OneNote](onenote-create-page.md)
- [Actualizar el contenido de la página de OneNote](onenote-update-page.md)
- [Integración con OneNote](integrate-with-onenote.md)
- [Blog para desarrolladores de OneNote](https://go.microsoft.com/fwlink/?LinkID=390183)
- [Preguntas de desarrollo de OneNote en Stack Overflow](https://go.microsoft.com/fwlink/?LinkID=390182)
- [Repositorios de OneNote en GitHub](https://go.microsoft.com/fwlink/?LinkID=390178)  

