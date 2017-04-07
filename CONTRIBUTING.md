# <a name="contribute-to-microsoft-graph-documentation"></a>Contribuir a la documentación de Microsoft Graph

Gracias por su interés en la documentación de Microsoft Graph.

* [Formas de contribuir](#ways-to-contribute)
* [Antes de que podamos aceptar su solicitud de extracción](#before-we-can-accept-your-pull-request)
* [Usar GitHub, Git y este repositorio](#use-github-git-and-this-repository)
* [Cómo usar Markdown para dar formato al tema](#how-to-use-markdown-to-format-your-topic)
* [Markdown estándar](#standard-markdown)
* [Más recursos](#more-resources)

## <a name="ways-to-contribute"></a>Formas de contribuir

Puede contribuir a la [documentación de Microsoft Graph](http://graph.microsoft.io) de estas formas:

* Contribuir a los artículos a través del [repositorio público de documentos de desarrollador de Microsoft Graph](https://github.com/microsoftgraph/microsoft-graph-docs)
    * Enviar solicitudes de incorporación de cambios independientes a las ramas /beta o /v1.0. Este paso es necesario para garantizar que las ramas de versión se actualizan con los últimos cambios. 
    * Además, envíe solicitudes de incorporación de cambios independientes a la rama /master. Este paso es para asegurarse de que la documentación del sitio web de Microsoft Graph se actualiza con los últimos cambios. 
* Informar sobre errores de documentación a través de [problemas de GitHub](https://github.com/microsoftgraph/microsoft-graph-docs/issues)
* Agregar solicitudes de documentación a [Office Developer Platform UserVoice](http://officespdev.uservoice.com) (UserVoice de la plataforma de desarrolladores de Office)

##<a name="before-we-can-accept-your-pull-request"></a>Antes de que podamos aceptar su solicitud de extracción

###<a name="minor-corrections"></a>Correcciones menores

Las correcciones menores o aclaraciones que nos envíe para la documentación y los ejemplos de código de este repositorio no requieren un contrato de licencia de contribución (CLA). Los envíos se aceptan como solicitudes de incorporación de cambios. Nos esforzaremos al máximo para revisar las solicitudes de inserción de cambios en 10 días laborables.


###<a name="larger-submissions"></a>Envíos más grandes

Si envía cambios nuevos o significativos a ejemplos de código y documentación, debe enviarnos una copia firmada del contrato de licencia de contribución (CLA) antes de que podamos aceptar la solicitud de incorporación de cambios si se encuentra en uno de estos grupos:

* Miembros del grupo Microsoft Open Technologies
* Colaboradores que no trabajan para Microsoft

Como miembro de la comunidad, **debe firmar el contrato de licencia de colaborador (CLA) antes de poder realizar grandes envíos a este proyecto**, pero debe cumplimentar y enviar la documentación solo una vez. Lea el documento detenidamente, es posible que su jefe deba firmarlo también.

Firmar el contrato de licencia de distribución (CLA) no le compromete con el repositorio principal, sino que los equipos de desarrollo de Office y de publicación de contenidos de desarrollo de Office podrán revisar y considerar sus contribuciones y se le acreditará debidamente si lo hacen.

Puede descargar el contrato de licencia de contribución (CLA) [aquí](https://github.com/microsoftgraph/microsoft-graph-docs/raw/master/Contribution%20License%20Agreement.pdf). Rellene el formulario y envíelo por correo electrónico a [officedev@microsoft.com](mailto:officedev@microsoft.com).

Tras recibir y procesar su CLA, nos esforzaremos al máximo para revisar las solicitudes de inserción en los próximos 10 días laborables.

## <a name="use-github-git-and-this-repository"></a>Usar GitHub, Git y este repositorio

**Nota:** La mayoría de la información de esta sección se puede encontrar en artículos de la [Ayuda de GitHub] [].  Si está familiarizado con Git y GitHub, vaya a la sección **Contribuir y editar contenido** para consultar los detalles del flujo de código y contenido de este repositorio.

### <a name="setting-up-your-fork-of-the-repository"></a>Configuración de la horquilla del repositorio

1.    Configure una cuenta de GitHub para que pueda contribuir a este proyecto. Si todavía no lo ha hecho, vaya a la [página principal de GitHub] [] y hágalo ahora.
2.    Configure el equipo con Git. Siga las instrucciones del [Tutorial de configuración de Git] [Set Up Git].
3.    Cree su propia horquilla en este repositorio. Para ello, en la parte superior de la página, haga clic en el botón **Horquilla**.
4.    Copie la horquilla en el equipo local. Para ello, abra GitBash. En el símbolo del sistema, escriba:

        git clone https://github.com/{your user name}/microsoft-graph-docs.git

    Después, cree una referencia al repositorio raíz mediante estos comandos:

        cd microsoft-graph-docs   git remote add upstream https://github.com/microsoftgraph/microsoft-graph-docs.git   git fetch upstream

Enhorabuena. Ya ha configurado el repositorio. No tendrá que repetir estos pasos de nuevo.

### <a name="contribute-and-edit-content"></a>Colaborar y editar contenido

Para que el proceso de contribución sea lo más sencillo posible, siga estos pasos.

1. Cree una nueva rama.
2. Agregue contenido nuevo o edite contenido existente.
3. Envíe una solicitud de incorporación de cambios al repositorio principal.
4. Elimine la rama.

Limite cada rama para un solo artículo o concepto para optimizar el flujo de trabajo y reducir la posibilidad de conflictos de combinación. Los siguientes tipos de contribución son adecuados para una nueva rama:

* Un nuevo artículo (y las imágenes asociadas)
* Modificaciones de revisión ortográfica y gramatical de un artículo
* Aplicar un único cambio de formato en un conjunto amplio de artículos (por ejemplo, aplicar un nuevo pie de página de derechos de autor).

#### <a name="create-a-new-branch"></a>Crear una nueva rama

1.    Abra GitBash.
2.    Escriba `git pull upstream master:<new branch name>` en el símbolo del sistema. Esto crea una nueva rama local que se copia desde la última rama principal de *microsoftgraph*. **Nota:** Si es colaborador interno, reemplace `master` en el comando con la rama de la fecha de publicación de destino.
3.    Escriba `git push origin <new branch name>` en el símbolo del sistema. Esto alertará a GitHub de la nueva rama. Ahora debería ver la nueva rama de la horquilla del repositorio en GitHub.
4.    Escriba `git checkout <new branch name>` para cambiar a la nueva rama.

#### <a name="add-new-content-or-edit-existing-content"></a>Agregar contenido nuevo o editar contenido existente

Desplácese hasta el repositorio en el equipo local por medio del Explorador de archivos. Los archivos del repositorio están en `C:\Users\<yourusername>\microsoft-graph-docs`.

Para editar archivos, ábralos en un editor de su elección y modifíquelos. Para crear un nuevo archivo, use el editor de su elección y guarde el nuevo archivo en la ubicación adecuada en la copia local del repositorio. Mientras trabaja, asegúrese de guardar el trabajo con frecuencia.

Los archivos en `C:\Users\<yourusername>\microsoft-graph-docs` son una copia de trabajo de la nueva rama que creó en el repositorio local. Los cambios en esta carpeta no afectan al repositorio local hasta que se confirme un cambio. Para confirmar un cambio en el repositorio local, escriba los siguientes comandos en GitBash:

    git add .
    git commit -v -a -m "<Describe the changes made in this commit>"

El comando `add` agrega los cambios a un área de ensayo como preparación para confirmarlos en el repositorio. El punto después del comando `add` especifica que quiere organizar todos los archivos que agregó o modificó, comprobando las subcarpetas de forma recursiva. (Si no quiere confirmar todos los cambios, puede agregar archivos específicos. También puede deshacer una confirmación. Para obtener ayuda, escriba `git add -help` o `git status`).

El comando `commit` aplica los cambios por fases al repositorio. `-m` significa que está proporcionando el comentario de confirmación en la línea de comandos. Si no están dirigidos a una fecha específica para la publicación, puede indicar "para publicar cuanto antes".  Los modificadores -v y -a se pueden omitir. El modificador -v es para obtener resultados detallados del comando, y -a hace lo que ya hizo con el comando add). 

Puede confirmar varias veces mientras trabaja, o puede esperar y confirmar solo una vez cuando termine.

#### <a name="submit-a-pull-request-to-the-main-repository"></a>Enviar una solicitud de incorporación de cambios al repositorio principal

Cuando termine con el trabajo y esté listo para combinarlo en el repositorio central, siga estos pasos.

1.    En GitBash, escriba `git push origin <new branch name>` en el símbolo del sistema. En el repositorio local, `origin` hace referencia a su repositorio de GitHub desde el que se clonó el repositorio local. Este comando inserta el estado actual de la nueva rama, incluyendo todas las confirmaciones realizadas en los pasos anteriores, en la bifurcación de GitHub.
2.    En el sitio de GitHub, vaya a la bifurcación de la rama nueva.
3.    Haga clic en el botón **Pull Request** (Solicitud de incorporación de cambios) en la parte superior de la página.
4.    Asegúrese de que la rama base es `microsoftgraph/microsoft-graph-docs@master` y que la rama principal es `<your username>/microsoft-graph-docs@<branch name>`.
5.    Haga clic en el botón **Update Commit Range** (Actualizar intervalo de confirmación).
6.    Asigne un título a la solicitud de incorporación de cambios y describa todos los cambios que está realizando. Si el error soluciona un elemento de UserVoice o un problema de GitHub, asegúrese de hacer referencia a ese problema en la descripción.
7.    Envíe la solicitud de incorporación de cambios.

Uno de los administradores del sitio procesará su solicitud de incorporación de cambios. La solicitud de incorporación de cambios aparecerá en el sitio microsoftgraph/microsoft-graph-docs bajo Issues (Problemas). Cuando se acepte la solicitud de incorporación de cambios, el problema se resolverá.

#### <a name="create-a-new-branch-after-merge"></a>Crear una rama después de una combinación

Después de que una rama se combine correctamente (es decir, se acepta la solicitud de incorporación de cambios), no siga trabajando en la rama local que se combinó correctamente antes. Esto puede provocar conflictos de combinación si envía otra solicitud de incorporación de cambios. En su lugar, si quiere realizar otra actualización, cree una rama local nueva desde la rama precedente que se combinó correctamente.

Por ejemplo, supongamos que la rama local X se combinó correctamente en la rama principal microsoftgraph/microsoft-graph-docs y quiere realizar actualizaciones adicionales en el contenido que se combinó. Cree una rama local nueva, X2, desde la rama principal microsoftgraph/microsoft-graph-docs. Para ello, abra GitBash y ejecute los siguientes comandos:

    cd microsoft-graph-docs
    git pull upstream master:X2
    git push origin X2

Ahora dispone de copias locales (en una rama local nueva) del trabajo que envió en la rama X. La rama X2 también contiene todo el trabajo que otros escritores combinaron, de modo que si su trabajo depende del de otros (por ejemplo, imágenes compartidas), está disponible en la nueva rama. Puede comprobar que el trabajo anterior (y el de otros) está en la rama si consulta la nueva rama...

    git checkout X2

... y comprueba el contenido. (El comando `checkout` actualiza los archivos de `C:\Users\<yourusername>\microsoft-graph-docs` al estado actual de la rama X2). Una vez que compruebe la rama nueva, puede realizar actualizaciones en el contenido y confirmarlos como de costumbre. Pero para evitar trabajar en la rama combinada (X) por error, es mejor eliminarla (vea la siguiente sección **Eliminar una rama**).

#### <a name="delete-a-branch"></a>Eliminar una rama

Una vez que los cambios se combinan correctamente en el repositorio central, puede eliminar la rama que usó porque ya no lo necesita.  Cualquier trabajo adicional requiere una rama nueva.  

Para eliminar la rama siga estos pasos:

1.    En GitBash, escriba `git checkout master` en el símbolo del sistema.  Esto garantiza que no está en la rama que se va a eliminar (lo que no está permitido).
2.    Después, escriba `git branch -d <branch name>` en el símbolo del sistema.  Esto elimina la rama en el equipo local solo si se combinó correctamente en el repositorio que precede en la cadena. (Puede reemplazar este comportamiento con el indicador `–D`, pero primero asegúrese de que quiere hacerlo).
3.    Por último, escriba `git push origin :<branch name>` en el símbolo del sistema (un espacio antes de los dos puntos y sin espacios después).  Esto eliminará la rama en la bifurcación de github.  

Enhorabuena, ha contribuido correctamente al proyecto.

## <a name="how-to-use-markdown-to-format-your-topic"></a>Cómo usar Markdown para dar formato al tema

### <a name="standard-markdown"></a>Markdown estándar

Todos los artículos de este repositorio usan Markdown.  Aunque se puede encontrar una introducción completa (y la lista de toda la sintaxis) en la [página principal de Markdown] [], trataremos los aspectos básicos que necesitará.

Si está buscando un buen editor, pruebe [Markdown Pad][].


### <a name="markdown-basics"></a>Conceptos básicos de Markdown

Esta es una lista de la sintaxis de Markdown más común:

*     **Saltos de línea frente a párrafos:** En Markdown no existe un elemento `<br />` HTML. En su lugar, un nuevo párrafo se designa con una línea vacía entre dos bloques de texto.
*    **Cursiva:** El HTML `<i>some text</i>` se escribe `*some text*`
*     **Negrita:** El elemento `<strong>some text</strong>` de HTML se escribe `**some text**`
*     **Títulos:** Los títulos HTML se designan mediante un número de caracteres `#` al principio de la línea.  El número de caracteres `#` se corresponde con el nivel jerárquico del título (por ejemplo,`#` = h1, `##` = h2 y `###` = h3).
*     **Listas numeradas:** Para crear una lista numerada (ordenada), comience la línea con `1. `. Si quiere varios elementos dentro de un elemento de lista único, puede dar formato a la lista como sigue:
        
        1.    Notice that this line is tabbed over after the '.'
        
            Now notice that there is a line break between the two paragraphs in the list element, and that the indentation here matches the indentation of the line above.

*    **Listas con viñetas:** Las listas con viñetas (sin ordenar) son casi idénticas a las listas ordenadas, salvo que el `1. ` se reemplaza por `* `, `- ` o `+ `.  Las listas de varios elementos funcionan del mismo modo que las listas ordenadas.
*    **Vínculos:** La sintaxis básica para un vínculo es `[visible link text](link url)`.

    Los vínculos también pueden tener referencias, como se describe en la sección **Referencias de vínculos e imágenes** más adelante.

*    **Imágenes:** La sintaxis básica para una imagen es `![alt text for the image](image url)`.

    Las imágenes también pueden tener referencias, como se describe en la sección **Referencias de vínculos e imágenes** más adelante.

*    **HTML en línea:** Markdown permite incluir en HTML en línea: `<i>italic</i>` se representa correctamente en Markdown como <i>cursiva</i>.

### <a name="link-and-image-references"></a>Referencias de vínculos e imágenes

Markdown tiene una característica muy agradable que permite al usuario insertar una referencia en lugar de una dirección URL para imágenes y vínculos. Esta es la sintaxis para usar esta característica:

    The image below is from [Google][googleweb]
    
    ![Google's logo][logo]
    
    [googleweb]: http://www.google.com
    [logo]: https://www.google.com/images/srpr/logo3w.png

Al usar referencias agrupadas en la parte inferior del archivo, puede encontrar fácilmente, modificar y reutilizar las direcciones URL de vínculos e imágenes. 


## <a name="more-resources"></a>Más recursos

* Para más información sobre imágenes, vaya a [su sitio][Página principal de Markdown].
* Para más información sobre cómo usar Git y GitHub, consulte primero la [sección de Ayuda de GitHub] [Ayuda de GitHub] y si es necesario póngase en contacto con los administradores del sitio.

[Página principal de GitHub]: http://github.com
[Ayuda de GitHub]: http://help.github.com/
[Set Up Git]: http://help.github.com/win-set-up-git/
[Página de inicio de Markdown]: http://daringfireball.net/projects/markdown/
[Markdown Pad]: http://markdownpad.com/
[microsoftgraph/microsoft-graph-docs issues]: https://github.com/microsoftgraph/microsoft-graph-docs/issues
