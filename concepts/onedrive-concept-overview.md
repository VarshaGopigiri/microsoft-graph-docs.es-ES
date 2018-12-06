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
# <a name="onedrive-file-storage-api-overview"></a><span data-ttu-id="6747a-103">Información general sobre la API de almacenamiento de archivos de OneDrive</span><span class="sxs-lookup"><span data-stu-id="6747a-103">OneDrive file storage API overview</span></span>

<span data-ttu-id="6747a-104">OneDrive es el centro de archivos en Office 365.</span><span class="sxs-lookup"><span data-stu-id="6747a-104">OneDrive is the files hub in Office 365.</span></span>
<span data-ttu-id="6747a-105">Los usuarios trabajan con los archivos en una amplia variedad de contextos, como Microsoft Teams, grupos, SharePoint y más.</span><span class="sxs-lookup"><span data-stu-id="6747a-105">People work with files in a variety of contexts, like Microsoft Teams, groups, SharePoint, and more.</span></span>
<span data-ttu-id="6747a-106">Con OneDrive, los usuarios pueden obtener acceso a estos archivos sin importar donde se encuentren y, con Microsoft Graph, puede usar una única API para trabajar con ellos.</span><span class="sxs-lookup"><span data-stu-id="6747a-106">With OneDrive, users can access these files no matter where they are stored, and with Microsoft Graph, you can use a single API to work with them.</span></span>

<span data-ttu-id="6747a-107">Los archivos en Office 365 se almacenan en [unidades][Drive API].</span><span class="sxs-lookup"><span data-stu-id="6747a-107">Files in Office 365 are stored in [drives][Drive API].</span></span>
<span data-ttu-id="6747a-108">Los usuarios pueden almacenar archivos en una unidad personal (su cuenta de OneDrive) o en una unidad compartida con tecnología de una biblioteca de documentos de [SharePoint][].</span><span class="sxs-lookup"><span data-stu-id="6747a-108">Users can store files in a personal drive - their OneDrive - or in a shared drive powered by a [SharePoint][] document library.</span></span>
<span data-ttu-id="6747a-109">La flexibilidad de OneDrive permite a los usuarios colaborar de la forma que más fácil le resulte.</span><span class="sxs-lookup"><span data-stu-id="6747a-109">OneDrive's flexibility lets users collaborate however it works best for them.</span></span>
<span data-ttu-id="6747a-110">Los usuarios pueden compartir vínculos a archivos, copiar o mover archivos a las unidades del equipo, o incluso adjuntar archivos de OneDrive a mensajes de correo en Outlook.</span><span class="sxs-lookup"><span data-stu-id="6747a-110">Users can share links to files, copy or move files to team drives, or even attach OneDrive files to mail messages in Outlook.</span></span>

## <a name="why-integrate-with-onedrive-file-storage-in-the-cloud"></a><span data-ttu-id="6747a-111">¿Por qué integrar con el almacenamiento de archivos de OneDrive en la nube?</span><span class="sxs-lookup"><span data-stu-id="6747a-111">Why integrate with OneDrive file storage in the cloud?</span></span>

### <a name="tap-into-an-ecosystem-with-billions-of-files"></a><span data-ttu-id="6747a-112">Obtener acceso a un ecosistema de miles de millones de archivos</span><span class="sxs-lookup"><span data-stu-id="6747a-112">Tap into an ecosystem with billions of files</span></span>

<span data-ttu-id="6747a-113">Los usuarios de OneDrive pueden obtener acceso a sus archivos desde cualquier dispositivo, tanto en línea como sin conexión, y compartir archivos con contactos, tanto dentro como fuera de su organización.</span><span class="sxs-lookup"><span data-stu-id="6747a-113">OneDrive users can access their files from any device, online or offline, and share files with people inside or outside their organization.</span></span>
<span data-ttu-id="6747a-114">OneDrive facilita la coautoría en tiempo real en aplicaciones conocidas como Word, Excel y PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="6747a-114">OneDrive enables real-time coauthoring in familiar apps like Word, Excel, and PowerPoint.</span></span>
<span data-ttu-id="6747a-115">Mejore los archivos con miniaturas enriquecidas para cientos de formatos, streaming de vídeo, análisis y más, con tecnología de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="6747a-115">Files light up with rich thumbnails for hundreds of formats, video streaming, analytics, and more, powered by Microsoft Graph.</span></span>
<span data-ttu-id="6747a-116">Los datos en OneDrive están protegidos con características de seguridad, cumplimiento y cifrado avanzado en las que confían los clientes.</span><span class="sxs-lookup"><span data-stu-id="6747a-116">Data in OneDrive is protected with advanced encryption, compliance, and security features that customers trust.</span></span>

<span data-ttu-id="6747a-117">Con más de 500 millones de dispositivos donde se ejecuta la aplicación de OneDrive y más del 85 % de las compañías de la lista Fortune 500 que usan OneDrive para la Empresa, al integrar su aplicación con OneDrive, puede conectarse con millones de consumidores, alumnos y usuarios empresariales, así como interactuar con los clientes donde ya trabajen a diario.</span><span class="sxs-lookup"><span data-stu-id="6747a-117">With over 500 million devices running the OneDrive app and over 85% of the Fortune 500 using OneDrive for Business, by integrating your app with OneDrive, you can connect with millions of consumers, students, and business users and engage with customers where they already do their work every day.</span></span>

### <a name="store-your-apps-files-in-a-powerful-cloud"></a><span data-ttu-id="6747a-118">Almacenar los archivos de la aplicación en una nube avanzada</span><span class="sxs-lookup"><span data-stu-id="6747a-118">Store your app's files in a powerful cloud</span></span>

<span data-ttu-id="6747a-119">Al almacenar los archivos en OneDrive, su aplicación podrá aprovechar las características de la nube de Microsoft y los usuarios podrán obtener acceso a sus archivos desde cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="6747a-119">When you store your files in OneDrive, your app can take advantage of the features of the Microsoft cloud and your users can access their files anywhere.</span></span>
<span data-ttu-id="6747a-120">Use el SDK del [selector de archivos][] para abrir, descargar, guardar o compartir rápidamente archivos almacenados en OneDrive desde su propia aplicación, con la misma experiencia que ya conocen los usuarios de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="6747a-120">Use the [file picker][] SDK to quickly open, download, save, or share files stored in OneDrive from within your own app, using the same experience OneDrive users are familiar with.</span></span>
<span data-ttu-id="6747a-121">Obtenga información sobre los archivos seleccionados directamente desde el SDK del selector, o bien use las API de Microsoft Graph directamente para interactuar de forma más avanzada con archivos.</span><span class="sxs-lookup"><span data-stu-id="6747a-121">Get information about selected files directly from the picker SDK, or use Microsoft Graph APIs directly to interact more deeply with files.</span></span>
<span data-ttu-id="6747a-122">Use [carpetas especiales][] para almacenar archivos en ubicaciones conocidas en OneDrive, como `Documents` y `Camera Roll`, o bien asigne su aplicación a su propia carpeta personal.</span><span class="sxs-lookup"><span data-stu-id="6747a-122">Use [special folders][] to store files in well-known locations on OneDrive, like `Documents` and `Camera Roll`, or give your app its own personal folder.</span></span>

### <a name="bring-your-app-straight-to-users-within-onedrive"></a><span data-ttu-id="6747a-123">Llevar la aplicación directamente a los usuarios en OneDrive</span><span class="sxs-lookup"><span data-stu-id="6747a-123">Bring your app straight to users within OneDrive</span></span>

<span data-ttu-id="6747a-124">Los clientes de OneDrive pueden usar o iniciar su aplicación directamente desde OneDrive para abrir, editar o previsualizar archivos.</span><span class="sxs-lookup"><span data-stu-id="6747a-124">OneDrive customers can use or launch your app directly from within OneDrive to open, edit, or preview files.</span></span>
<span data-ttu-id="6747a-125">Use las extensiones del [controlador de archivos][] de OneDrive para mostrar iconos y vistas previas de sus propias extensiones de archivo personalizadas, agregar su aplicación al botón **Nuevo** o incluso agregar sus propias acciones personalizadas a la barra de menús para iniciar su aplicación.</span><span class="sxs-lookup"><span data-stu-id="6747a-125">Use OneDrive's [file handler][] extensions to provide icons and previews for your own custom file extensions, add your app to the **New** button or even add your own custom actions to the menu bar to launch your app.</span></span>

### <a name="work-with-content-in-formats-your-app-understands"></a><span data-ttu-id="6747a-126">Trabajar con contenido en formatos que comprenda su aplicación</span><span class="sxs-lookup"><span data-stu-id="6747a-126">Work with content in formats your app understands</span></span>

<span data-ttu-id="6747a-127">Su aplicación puede obtener contenido de archivos en el formato que le resulte más cómodo.</span><span class="sxs-lookup"><span data-stu-id="6747a-127">Your app can get file content in the format that is most convenient for you.</span></span>
<span data-ttu-id="6747a-128">La aplicación puede mostrar [miniaturas][] de tamaño personalizado de cientos de formatos de archivo.</span><span class="sxs-lookup"><span data-stu-id="6747a-128">Your app can display custom-sized [thumbnails][] for hundreds of different file formats.</span></span>
<span data-ttu-id="6747a-129">Puede descargar archivos en una amplia variedad de [formatos alternativos][], como PDF.</span><span class="sxs-lookup"><span data-stu-id="6747a-129">You can download files in a variety of alternative [formats][], like PDF.</span></span>
<span data-ttu-id="6747a-130">Incluso puede integrar las características de vista previa de archivos de OneDrive en su aplicación con la API de [vista previa][] (beta).</span><span class="sxs-lookup"><span data-stu-id="6747a-130">You can even embed the OneDrive file previewers within your app by using the [preview][] API (beta).</span></span>

### <a name="work-with-file-content-and-metadata-without-downloading-the-binary"></a><span data-ttu-id="6747a-131">Trabajar con contenido de archivos y metadatos sin descargar datos binarios</span><span class="sxs-lookup"><span data-stu-id="6747a-131">Work with file content and metadata without downloading the binary</span></span>

<span data-ttu-id="6747a-132">Con Microsoft Graph, puede obtener acceso a contenido enriquecido con API de REST sin tener que descargar los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="6747a-132">With Microsoft Graph, you can access rich content through REST APIs without having to download the binary.</span></span>
<span data-ttu-id="6747a-133">Explore los metadatos extraídos de archivos de [foto][], [audio][] y [vídeo][].</span><span class="sxs-lookup"><span data-stu-id="6747a-133">Explore extracted metadata from [photo][], [audio][], and [video][] files.</span></span>
<span data-ttu-id="6747a-134">Use la [API de Excel][] para trabajar directamente con los datos sin procesar almacenados en un libro de Excel.</span><span class="sxs-lookup"><span data-stu-id="6747a-134">Use the [Excel API][] to work directly with the raw data stored in an Excel workbook.</span></span>
<span data-ttu-id="6747a-135">Use la [API de notas][] para obtener acceso a los contenidos de blocs de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="6747a-135">Use the [Notes API][] to access the contents of OneNote notebooks.</span></span>

### <a name="react-to-file-changes"></a><span data-ttu-id="6747a-136">Reaccionar a cambios en archivos</span><span class="sxs-lookup"><span data-stu-id="6747a-136">React to file changes</span></span>

<span data-ttu-id="6747a-137">Con los [webhooks][], su aplicación puede recibir notificaciones cuando cambie un archivo para que pueda reaccionar rápidamente.</span><span class="sxs-lookup"><span data-stu-id="6747a-137">With [webhooks][], your app can get notified when files change so you can quickly react.</span></span>
<span data-ttu-id="6747a-138">Use la [API delta][] para ver lo que cambió desde la última vez que la aplicación se sincronizó con la nube.</span><span class="sxs-lookup"><span data-stu-id="6747a-138">Use the [delta API][] to see what changed since the last time your app synchronized with the cloud.</span></span>

## <a name="api-reference"></a><span data-ttu-id="6747a-139">Referencia de la API</span><span class="sxs-lookup"><span data-stu-id="6747a-139">API reference</span></span>
<span data-ttu-id="6747a-140">¿Busca la referencia de la API para este servicio?</span><span class="sxs-lookup"><span data-stu-id="6747a-140">Looking for the API reference for this service?</span></span>

- [<span data-ttu-id="6747a-141">API de almacén de archivos de OneDrive en Microsoft Graph v1.0</span><span class="sxs-lookup"><span data-stu-id="6747a-141">OneDrive file storage API in Microsoft Graph v1.0</span></span>](/graph/api/resources/onedrive?view=graph-rest-1.0)
- [<span data-ttu-id="6747a-142">API de almacén de archivos de OneDrive en Microsoft Graph beta</span><span class="sxs-lookup"><span data-stu-id="6747a-142">OneDrive file storage API in Microsoft Graph beta</span></span>](/graph/api/resources/onedrive?view=graph-rest-beta)

## <a name="next-steps"></a><span data-ttu-id="6747a-143">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="6747a-143">Next steps</span></span>

<span data-ttu-id="6747a-144">Obtenga más información sobre cómo [usar la API de OneDrive][Drive API] en Microsoft Graph v1.0.</span><span class="sxs-lookup"><span data-stu-id="6747a-144">Find out more about [using the OneDrive API][Drive API] in Microsoft Graph v1.0.</span></span>

[SharePoint]: sharepoint-concept-overview.md
[selector de archivos]: https://dev.onedrive.com/sdk/js-v72/js-picker-overview.htm
[file picker]: https://dev.onedrive.com/sdk/js-v72/js-picker-overview.htm
[controlador de archivos]: https://docs.microsoft.com/onedrive/developer/file-handlers
[file handler]: https://docs.microsoft.com/onedrive/developer/file-handlers
[carpetas especiales]: /graph/api/drive-get-specialfolder?view=graph-rest-1.0
[special folders]: /graph/api/drive-get-specialfolder?view=graph-rest-1.0
[API de notas]: integrate-with-onenote.md
[Notes API]: integrate-with-onenote.md
[API de Excel]: /graph/api/resources/excel?view=graph-rest-1.0
[Excel API]: /graph/api/resources/excel?view=graph-rest-1.0
[REST API]: /graph/api/resources/onedrive?view=graph-rest-1.0
[API delta]: /graph/api/driveitem-delta?view=graph-rest-1.0
[delta API]: /graph/api/driveitem-delta?view=graph-rest-1.0
[vídeo]: /graph/api/resources/video?view=graph-rest-1.0
[video]: /graph/api/resources/video?view=graph-rest-1.0
[foto]: /graph/api/resources/photo?view=graph-rest-1.0
[photo]: /graph/api/resources/photo?view=graph-rest-1.0
[audio]: /graph/api/resources/audio?view=graph-rest-1.0
[formatos]: /graph/api/driveitem-get-content-format?view=graph-rest-1.0
[formats]: /graph/api/driveitem-get-content-format?view=graph-rest-1.0
[miniaturas]: /graph/api/driveitem-list-thumbnails?view=graph-rest-1.0
[thumbnails]: /graph/api/driveitem-list-thumbnails?view=graph-rest-1.0
[vista previa]: /graph/api/driveitem-preview?view=graph-rest-beta
[preview]: /graph/api/driveitem-preview?view=graph-rest-beta
[webhooks]: /graph/api/resources/webhooks?view=graph-rest-1.0
[Drive API]: /graph/api/resources/onedrive?view=graph-rest-1.0
