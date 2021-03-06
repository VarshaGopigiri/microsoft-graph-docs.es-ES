---
title: Información general sobre la API de OneNote
description: OneNote es un bloc de notas digital que permite a los clientes realizar un seguimiento de ideas y notas para el hogar, trabajo o escuela por voz, esbozando o escribiendo en la web, teléfonos, tabletas o el escritorio. Pueden organizar notas libremente, cambiar de dispositivo y retomar el trabajo donde lo dejaron, así como colaborar en las notas con otras personas en tiempo real.
author: Jewan-microsoft
localization_priority: Priority
ms.openlocfilehash: a3ca57e9bac52613fbe884368f79b31b5b5165e0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825721"
---
# <a name="onenote-api-overview"></a>Información general sobre la API de OneNote

OneNote es un bloc de notas digital que permite a los clientes realizar un seguimiento de ideas y notas para el hogar, trabajo o escuela por voz, esbozando o escribiendo en la web, teléfonos, tabletas o el escritorio. Pueden organizar notas libremente, cambiar de dispositivo y retomar el trabajo donde lo dejaron, así como colaborar en las notas con otras personas en tiempo real.

![Un bloc de notas de OneNote con sus secciones y páginas](images/onenote-page.png)

## <a name="why-integrate-with-onenote"></a>¿Por qué debería realizar la integración con OneNote?

Al integrar sus aplicaciones con OneNote, puede crear experiencias enriquecedoras en varias plataformas que llegan a millones de usuarios en todo el mundo. Puede usar Microsoft Graph para tener acceso a los blocs de notas, secciones y páginas de OneNote para crear soluciones que ayuden a los usuarios a planear y organizar las ideas y la información.


### <a name="collect-and-organize-notes-and-ideas"></a>Recopilar y organizar notas e ideas  

Use OneNote como un lienzo donde los usuarios pueden agregar y organizar su contenido. Microsoft Graph facilita la escritura de aplicaciones que permiten a los alumnos tomar notas e investigar, a las familias compartir planes e ideas, y a los compradores compartir imágenes.
 Su aplicación puede obtener la información que la gente quiere, enviarla a OneNote y luego ayudarles a organizarla.

### <a name="capture-information-in-many-formats"></a>Capturar la información en varios formatos

Captura de HTML, imágenes insertadas (originadas localmente o en una dirección URL pública), vídeo, audio, mensajes de correo electrónico y otros tipos de archivo comunes. OneNote puede incluso presentar páginas web y archivos PDF como instantáneas. Microsoft Graph admite un conjunto HTML y CSS estándar para el diseño de página de OneNote, así que puede usar tablas, imágenes incorporadas y formato básico para conseguir el aspecto que quiera. 

### <a name="use-the-onenote-ecosystem-to-enhance-your-core-scenarios"></a>Usar el ecosistema de OneNote para mejorar los escenarios básicos

Aproveche otras poderosas características de OneNote.
 Las API de OneNote en Microsoft Graph ejecutan OCR en imágenes, son compatibles con la búsqueda de texto completo, sincronizan los clientes automáticamente, procesan imágenes y extraen capturas de tarjetas de presentación y descripciones de productos y recetas en línea. Use OneNote como almacén de memoria digital en la nube para notas y elementos multimedia ligeros, o como fuente de datos para datos específicos de dominio. 

### <a name="reach-millions-of-onenote-users-on-all-major-platforms"></a>Llegar a millones de usuarios de OneNote en todas las plataformas principales

Use OneNote para aumentar el uso de la aplicación. OneNote está preinstalado en los nuevos dispositivos de Windows y está disponible para la mayoría de las plataformas, en línea y como parte de Office 365. Al publicar aplicaciones que usan el entorno completo de OneNote, tendrá acceso al amplio potencial de mercado multiplataforma.

<!-- Might be good to show a few examples of Microsoft Graph API calls here, similar to what we have in the featured scenarios topic: featured_scenarios..md You could have an H2 section called "What can I do with OneNote APIs in Microsoft Graph?"-->

## <a name="what-can-i-do-with-onenote-apis-in-microsoft-graph"></a>¿Qué puedo hacer con las API de OneNote en Microsoft Graph?

A continuación se enumeran algunas de las solicitudes más populares para trabajar con los recursos de OneNote.

|Operación|URL|
|:--------|:--|
|OBTENER mis blocs de notas|[https://graph.microsoft.com/v1.0/me/onenote/notebooks](https://developer.microsoft.com/graph/graph-explorer?request=me/onenote/notebooks&version=1.0)|
|OBTENER mis secciones|[https://graph.microsoft.com/v1.0/me/onenote/sections](https://developer.microsoft.com/graph/graph-explorer?request=me/onenote/sections&version=1.0)|
|OBTENER mis páginas|[https://graph.microsoft.com/v1.0/me/onenote/pages](https://developer.microsoft.com/graph/graph-explorer?request=me/onenote/pages&version=1.0)|

## <a name="learn-more-about-onenote-apis"></a>Más información sobre las API de OneNote

Realice un análisis exhaustivo de las API de Microsoft Graph para obtener información sobre las capacidades de actualización de contenido de OneNote. Los temas de la siguiente lista muestran cómo crear nuevas páginas de OneNote y actualizar páginas existentes con nuevo contenido. También obtendrá información sobre procedimientos recomendados para usar Microsoft Graph para actualizar los blocs de notas de OneNote. 


### <a name="work-with-onenote"></a>Trabajar con OneNote

* [Usar la API de REST de OneNote](/graph/api/resources/onenote-api-overview?view=graph-rest-1.0)
* [Procedimientos recomendados](onenote-best-practices.md)
* [Instrucciones de personalización de marcas](onenote-branding.md)
* [Abrir el cliente de OneNote](open-onenote-client.md)
* [Usar etiquetas en páginas de OneNote](onenote-note-tags.md)
* [Códigos de error de las API de OneNote en Microsoft Graph](onenote-error-codes.md)

### <a name="work-with-onenote-pages"></a>Trabajar con páginas de OneNote

* [HTML de entrada y salida en páginas de OneNote](onenote-input-output-html.md)
* [Obtener el contenido y la estructura de OneNote con Microsoft Graph](onenote-get-content.md)
* [Crear páginas de OneNote](onenote-create-page.md)
* [Actualizar el contenido de la página de OneNote](onenote-update-page.md)

### <a name="work-with-onenote-page-content"></a>Trabajar con el contenido de la página de OneNote

* [Crear elementos con posición absoluta en páginas de OneNote](onenote-abs-pos.md)
* [Agregar imágenes, vídeos y archivos a páginas de OneNote](onenote-images-files.md)
* [Usar las etiquetas div de la API de OneNote para extraer datos de capturas](onenote-extract-data.md)

## <a name="see-also"></a>Vea también
Conozca algunas otras características de OneNote que se exponen en el punto de conexión REST de OneNote específico del servicio.

- [Desarrollo de OneNote](https://docs.microsoft.com/es-ES/previous-versions/office/office-365-api/how-to/onenote-landing)
- [Trabajar con blocs de notas de clase](https://docs.microsoft.com/es-ES/previous-versions/office/office-365-api/how-to/onenote-classnotebook)
- [Trabajar con blocs de notas de clase asincrónicos](https://docs.microsoft.com/es-ES/previous-versions/office/office-365-api/how-to/onenote-classnotebook-asynchronous)
- [Trabajar con blocs de notas para docentes](https://docs.microsoft.com/es-ES/previous-versions/office/office-365-api/how-to/onenote-staffnotebook)
- [Copiar blocs de notas, secciones y páginas](https://docs.microsoft.com/es-ES/previous-versions/office/office-365-api/how-to/onenote-copy)
- [Administrar los permisos de las entidades de OneNote](https://docs.microsoft.com/es-ES/previous-versions/office/office-365-api/how-to/onenote-manage-perms)
- [Usar el cuadro de diálogo de guardar de OneNote en sus páginas web](https://docs.microsoft.com/es-ES/previous-versions/office/office-365-api/how-to/onenote-save-dialog)
- [Suscribirse a webhooks](https://docs.microsoft.com/es-ES/previous-versions/office/office-365-api/how-to/onenote-sync)

## <a name="api-reference"></a>Referencia de la API
¿Busca la referencia de la API para este servicio?

- [API de OneNote en Microsoft Graph v1.0](/graph/api/resources/onenote-api-overview?view=graph-rest-1.0)
- [API de OneNote en Microsoft Graph beta](/graph/api/resources/onenote-api-overview?view=graph-rest-beta)

## <a name="next-steps"></a>Pasos siguientes

Use el [Probador de Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer) para probar las API de OneNote con sus propios blocs de notas de OneNote.

Para realizar llamadas a la API de OneNote desde el Probador de Graph, seleccione **Mostrar más ejemplos** en la columna de la izquierda. Use el menú para **activar** OneNote. También tendrá que habilitar los permisos adecuados. Bajo el nombre de cuenta en el menú de la izquierda, elija **Modificar permisos**. Para obtener más información sobre los permisos de OneNote, consulte [Permisos de notas](permissions-reference.md#notes-permissions).

Para comenzar con las API de OneNote en Microsoft Graph, vea el [contenido de referencia de OneNote](/graph/api/resources/onenote-api-overview?view=graph-rest-1.0).

