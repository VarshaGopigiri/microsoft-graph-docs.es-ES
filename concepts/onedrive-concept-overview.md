---
title: Información general sobre la API de almacenamiento de archivos de OneDrive
description: OneDrive es el centro de archivos en Office 365.
ms.openlocfilehash: dcd16969a2f1b1f6898696fe0be9539d50800252
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092771"
---
# <a name="onedrive-file-storage-api-overview"></a>Información general sobre la API de almacenamiento de archivos de OneDrive

OneDrive es el centro de archivos en Office 365.
Los usuarios trabajan con los archivos en una amplia variedad de contextos, como Microsoft Teams, grupos, SharePoint y más.
Con OneDrive, los usuarios pueden obtener acceso a estos archivos sin importar donde se encuentren y, con Microsoft Graph, puede usar una única API para trabajar con ellos.

Los archivos en Office 365 se almacenan en [unidades][Drive API].
Los usuarios pueden almacenar archivos en una unidad personal (su cuenta de OneDrive) o en una unidad compartida con tecnología de una biblioteca de documentos de [SharePoint][].
La flexibilidad de OneDrive permite a los usuarios colaborar de la forma que más fácil le resulte.
Los usuarios pueden compartir vínculos a archivos, copiar o mover archivos a las unidades del equipo, o incluso adjuntar archivos de OneDrive a mensajes de correo en Outlook.

## <a name="why-integrate-with-onedrive-file-storage-in-the-cloud"></a>¿Por qué integrar con el almacenamiento de archivos de OneDrive en la nube?

### <a name="tap-into-an-ecosystem-with-billions-of-files"></a>Obtener acceso a un ecosistema de miles de millones de archivos

Los usuarios de OneDrive pueden obtener acceso a sus archivos desde cualquier dispositivo, tanto en línea como sin conexión, y compartir archivos con contactos, tanto dentro como fuera de su organización.
OneDrive facilita la coautoría en tiempo real en aplicaciones conocidas como Word, Excel y PowerPoint.
Mejore los archivos con miniaturas enriquecidas para cientos de formatos, streaming de vídeo, análisis y más, con tecnología de Microsoft Graph.
Los datos en OneDrive están protegidos con características de seguridad, cumplimiento y cifrado avanzado en las que confían los clientes.

Con más de 500 millones de dispositivos donde se ejecuta la aplicación de OneDrive y más del 85 % de las compañías de la lista Fortune 500 que usan OneDrive para la Empresa, al integrar su aplicación con OneDrive, puede conectarse con millones de consumidores, alumnos y usuarios empresariales, así como interactuar con los clientes donde ya trabajen a diario.

### <a name="store-your-apps-files-in-a-powerful-cloud"></a>Almacenar los archivos de la aplicación en una nube avanzada

Al almacenar los archivos en OneDrive, su aplicación podrá aprovechar las características de la nube de Microsoft y los usuarios podrán obtener acceso a sus archivos desde cualquier lugar.
Use el SDK del [selector de archivos][] para abrir, descargar, guardar o compartir rápidamente archivos almacenados en OneDrive desde su propia aplicación, con la misma experiencia que ya conocen los usuarios de OneDrive.
Obtenga información sobre los archivos seleccionados directamente desde el SDK del selector, o bien use las API de Microsoft Graph directamente para interactuar de forma más avanzada con archivos.
Use [carpetas especiales][] para almacenar archivos en ubicaciones conocidas en OneDrive, como `Documents` y `Camera Roll`, o bien asigne su aplicación a su propia carpeta personal.

### <a name="bring-your-app-straight-to-users-within-onedrive"></a>Llevar la aplicación directamente a los usuarios en OneDrive

Los clientes de OneDrive pueden usar o iniciar su aplicación directamente desde OneDrive para abrir, editar o previsualizar archivos.
Use las extensiones del [controlador de archivos][] de OneDrive para mostrar iconos y vistas previas de sus propias extensiones de archivo personalizadas, agregar su aplicación al botón **Nuevo** o incluso agregar sus propias acciones personalizadas a la barra de menús para iniciar su aplicación.

### <a name="work-with-content-in-formats-your-app-understands"></a>Trabajar con contenido en formatos que comprenda su aplicación

Su aplicación puede obtener contenido de archivos en el formato que le resulte más cómodo.
La aplicación puede mostrar [miniaturas][] de tamaño personalizado de cientos de formatos de archivo.
Puede descargar archivos en una amplia variedad de [formatos alternativos][], como PDF.
Incluso puede integrar las características de vista previa de archivos de OneDrive en su aplicación con la API de [vista previa][] (beta).

### <a name="work-with-file-content-and-metadata-without-downloading-the-binary"></a>Trabajar con contenido de archivos y metadatos sin descargar datos binarios

Con Microsoft Graph, puede obtener acceso a contenido enriquecido con API de REST sin tener que descargar los datos binarios.
Explore los metadatos extraídos de archivos de [foto][], [audio][] y [vídeo][].
Use la [API de Excel][] para trabajar directamente con los datos sin procesar almacenados en un libro de Excel.
Use la [API de notas][] para obtener acceso a los contenidos de blocs de notas de OneNote.

### <a name="react-to-file-changes"></a>Reaccionar a cambios en archivos

Con los [webhooks][], su aplicación puede recibir notificaciones cuando cambie un archivo para que pueda reaccionar rápidamente.
Use la [API delta][] para ver lo que cambió desde la última vez que la aplicación se sincronizó con la nube.

## <a name="api-reference"></a>Referencia de la API
¿Busca la referencia de la API para este servicio?

- [API de almacén de archivos de OneDrive en Microsoft Graph v1.0](/graph/api/resources/onedrive?view=graph-rest-1.0)
- [API de almacén de archivos de OneDrive en Microsoft Graph beta](/graph/api/resources/onedrive?view=graph-rest-beta)

## <a name="next-steps"></a>Pasos siguientes

Obtenga más información sobre cómo [usar la API de OneDrive][Drive API] en Microsoft Graph v1.0.

[SharePoint]: sharepoint-concept-overview.md
[selector de archivos]: https://dev.onedrive.com/sdk/js-v72/js-picker-overview.htm
[controlador de archivos]: https://docs.microsoft.com/onedrive/developer/file-handlers
[carpetas especiales]: /graph/api/drive-get-specialfolder?view=graph-rest-1.0
[API de notas]: integrate-with-onenote.md
[API de Excel]: /graph/api/resources/excel?view=graph-rest-1.0
[REST API]: /graph/api/resources/onedrive?view=graph-rest-1.0
[API delta]: /graph/api/driveitem-delta?view=graph-rest-1.0
[vídeo]: /graph/api/resources/video?view=graph-rest-1.0
[foto]: /graph/api/resources/photo?view=graph-rest-1.0
[audio]: /graph/api/resources/audio?view=graph-rest-1.0
[formatos]: /graph/api/driveitem-get-content-format?view=graph-rest-1.0
[miniaturas]: /graph/api/driveitem-list-thumbnails?view=graph-rest-1.0
[vista previa]: /graph/api/driveitem-preview?view=graph-rest-beta
[webhooks]: /graph/api/resources/webhooks?view=graph-rest-1.0
[Drive API]: /graph/api/resources/onedrive?view=graph-rest-1.0
