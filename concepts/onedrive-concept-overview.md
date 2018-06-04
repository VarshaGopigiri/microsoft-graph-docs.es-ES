# <a name="onedrive-file-storage-api-overview"></a><span data-ttu-id="78028-101">Información general sobre la API de almacenamiento de archivos de OneDrive</span><span class="sxs-lookup"><span data-stu-id="78028-101">OneDrive file storage API overview</span></span>

<span data-ttu-id="78028-102">OneDrive es el centro de archivos en Office 365.</span><span class="sxs-lookup"><span data-stu-id="78028-102">OneDrive is the files hub in Office 365.</span></span>
<span data-ttu-id="78028-103">Los usuarios trabajan con los archivos en una amplia variedad de contextos, como Microsoft Teams, grupos, SharePoint y más.</span><span class="sxs-lookup"><span data-stu-id="78028-103">People work with files in a variety of contexts, like Microsoft Teams, groups, SharePoint, and more.</span></span>
<span data-ttu-id="78028-104">Con OneDrive, los usuarios pueden obtener acceso a estos archivos sin importar donde se encuentren y, con Microsoft Graph, puede usar una única API para trabajar con ellos.</span><span class="sxs-lookup"><span data-stu-id="78028-104">With OneDrive, users can access these files no matter where they are stored, and with Microsoft Graph, you can use a single API to work with them.</span></span>

<span data-ttu-id="78028-105">Los archivos en Office 365 se almacenan en [unidades][Drive API].</span><span class="sxs-lookup"><span data-stu-id="78028-105">Files in Office 365 are stored in [drives][Drive API].</span></span>
<span data-ttu-id="78028-106">Los usuarios pueden almacenar archivos en una unidad personal (su cuenta de OneDrive) o en una unidad compartida con tecnología de una biblioteca de documentos de [SharePoint][].</span><span class="sxs-lookup"><span data-stu-id="78028-106">Users can store files in a personal drive - their OneDrive - or in a shared drive powered by a [SharePoint][] document library.</span></span>
<span data-ttu-id="78028-107">La flexibilidad de OneDrive permite a los usuarios colaborar de la forma que más fácil le resulte.</span><span class="sxs-lookup"><span data-stu-id="78028-107">OneDrive's flexibility lets users collaborate however it works best for them.</span></span>
<span data-ttu-id="78028-108">Los usuarios pueden compartir vínculos a archivos, copiar o mover archivos a las unidades del equipo, o incluso adjuntar archivos de OneDrive a mensajes de correo en Outlook.</span><span class="sxs-lookup"><span data-stu-id="78028-108">Users can share links to files, copy or move files to team drives, or even attach OneDrive files to mail messages in Outlook.</span></span>

## <a name="why-integrate-with-onedrive-file-storage-in-the-cloud"></a><span data-ttu-id="78028-109">¿Por qué integrar con el almacenamiento de archivos de OneDrive en la nube?</span><span class="sxs-lookup"><span data-stu-id="78028-109">Why integrate with OneDrive file storage in the cloud?</span></span>

### <a name="tap-into-an-ecosystem-with-billions-of-files"></a><span data-ttu-id="78028-110">Obtener acceso a un ecosistema de miles de millones de archivos</span><span class="sxs-lookup"><span data-stu-id="78028-110">Tap into an ecosystem with billions of files</span></span>

<span data-ttu-id="78028-111">Los usuarios de OneDrive pueden obtener acceso a sus archivos desde cualquier dispositivo, tanto en línea como sin conexión, y compartir archivos con contactos, tanto dentro como fuera de su organización.</span><span class="sxs-lookup"><span data-stu-id="78028-111">OneDrive users can access their files from any device, online or offline, and share files with people inside or outside their organization.</span></span>
<span data-ttu-id="78028-112">OneDrive facilita la coautoría en tiempo real en aplicaciones conocidas como Word, Excel y PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="78028-112">OneDrive enables real-time coauthoring in familiar apps like Word, Excel, and PowerPoint.</span></span>
<span data-ttu-id="78028-113">Mejore los archivos con miniaturas enriquecidas para cientos de formatos, streaming de vídeo, análisis y más, con tecnología de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="78028-113">Files light up with rich thumbnails for hundreds of formats, video streaming, analytics, and more, powered by Microsoft Graph.</span></span>
<span data-ttu-id="78028-114">Los datos en OneDrive están protegidos con características de seguridad, cumplimiento y cifrado avanzado en las que confían los clientes.</span><span class="sxs-lookup"><span data-stu-id="78028-114">Data in OneDrive is protected with advanced encryption, compliance, and security features that customers trust.</span></span>

<span data-ttu-id="78028-115">Con más de 500 millones de dispositivos donde se ejecuta la aplicación de OneDrive y más del 85 % de las compañías de la lista Fortune 500 que usan OneDrive para la Empresa, al integrar su aplicación con OneDrive, puede conectarse con millones de consumidores, alumnos y usuarios empresariales, así como interactuar con los clientes donde ya trabajen a diario.</span><span class="sxs-lookup"><span data-stu-id="78028-115">With over 500 million devices running the OneDrive app and over 85% of the Fortune 500 using OneDrive for Business, by integrating your app with OneDrive, you can connect with millions of consumers, students, and business users and engage with customers where they already do their work every day.</span></span>

### <a name="store-your-apps-files-in-a-powerful-cloud"></a><span data-ttu-id="78028-116">Almacenar los archivos de la aplicación en una nube avanzada</span><span class="sxs-lookup"><span data-stu-id="78028-116">Store your app's files in a powerful cloud</span></span>

<span data-ttu-id="78028-117">Al almacenar los archivos en OneDrive, su aplicación podrá aprovechar las características de la nube de Microsoft y los usuarios podrán obtener acceso a sus archivos desde cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="78028-117">When you store your files in OneDrive, your app can take advantage of the features of the Microsoft cloud and your users can access their files anywhere.</span></span>
<span data-ttu-id="78028-118">Use el SDK del [selector de archivos][] para abrir, descargar, guardar o compartir rápidamente archivos almacenados en OneDrive desde su propia aplicación, con la misma experiencia que ya conocen los usuarios de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="78028-118">Use the [file picker][] SDK to quickly open, download, save, or share files stored in OneDrive from within your own app, using the same experience OneDrive users are familiar with.</span></span>
<span data-ttu-id="78028-119">Obtenga información sobre los archivos seleccionados directamente desde el SDK del selector, o bien use las API de Microsoft Graph directamente para interactuar de forma más avanzada con archivos.</span><span class="sxs-lookup"><span data-stu-id="78028-119">Get information about selected files directly from the picker SDK, or use Microsoft Graph APIs directly to interact more deeply with files.</span></span>
<span data-ttu-id="78028-120">Use [carpetas especiales][] para almacenar archivos en ubicaciones conocidas en OneDrive, como `Documents` y `Camera Roll`, o bien asigne su aplicación a su propia carpeta personal.</span><span class="sxs-lookup"><span data-stu-id="78028-120">Use [special folders][] to store files in well-known locations on OneDrive, like `Documents` and `Camera Roll`, or give your app its own personal folder.</span></span>

### <a name="bring-your-app-straight-to-users-within-onedrive"></a><span data-ttu-id="78028-121">Llevar la aplicación directamente a los usuarios en OneDrive</span><span class="sxs-lookup"><span data-stu-id="78028-121">Bring your app straight to users within OneDrive</span></span>

<span data-ttu-id="78028-122">Los clientes de OneDrive pueden usar o iniciar su aplicación directamente desde OneDrive para abrir, editar o previsualizar archivos.</span><span class="sxs-lookup"><span data-stu-id="78028-122">OneDrive customers can use or launch your app directly from within OneDrive to open, edit, or preview files.</span></span>
<span data-ttu-id="78028-123">Use las extensiones del [controlador de archivos][] de OneDrive para mostrar iconos y vistas previas de sus propias extensiones de archivo personalizadas, agregar su aplicación al botón **Nuevo** o incluso agregar sus propias acciones personalizadas a la barra de menús para iniciar su aplicación.</span><span class="sxs-lookup"><span data-stu-id="78028-123">Use OneDrive's [file handler][] extensions to provide icons and previews for your own custom file extensions, add your app to the **New** button or even add your own custom actions to the menu bar to launch your app.</span></span>

### <a name="work-with-content-in-formats-your-app-understands"></a><span data-ttu-id="78028-124">Trabajar con contenido en formatos que comprenda su aplicación</span><span class="sxs-lookup"><span data-stu-id="78028-124">Work with content in formats your app understands</span></span>

<span data-ttu-id="78028-125">Su aplicación puede obtener contenido de archivos en el formato que le resulte más cómodo.</span><span class="sxs-lookup"><span data-stu-id="78028-125">Your app can get file content in the format that is most convenient for you.</span></span>
<span data-ttu-id="78028-126">La aplicación puede mostrar [miniaturas][] de tamaño personalizado de cientos de formatos de archivo.</span><span class="sxs-lookup"><span data-stu-id="78028-126">Your app can display custom-sized [thumbnails][] for hundreds of different file formats.</span></span>
<span data-ttu-id="78028-127">Puede descargar archivos en una amplia variedad de [formatos alternativos][], como PDF.</span><span class="sxs-lookup"><span data-stu-id="78028-127">You can download files in a variety of alternative [formats][], like PDF.</span></span>
<span data-ttu-id="78028-128">Incluso puede integrar las características de vista previa de archivos de OneDrive en su aplicación con la API de [vista previa][] (beta).</span><span class="sxs-lookup"><span data-stu-id="78028-128">You can even embed the OneDrive file previewers within your app by using the [preview][] API (beta).</span></span>

### <a name="work-with-file-content-and-metadata-without-downloading-the-binary"></a><span data-ttu-id="78028-129">Trabajar con contenido de archivos y metadatos sin descargar datos binarios</span><span class="sxs-lookup"><span data-stu-id="78028-129">Work with file content and metadata without downloading the binary</span></span>

<span data-ttu-id="78028-130">Con Microsoft Graph, puede obtener acceso a contenido enriquecido con API de REST sin tener que descargar los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="78028-130">With Microsoft Graph, you can access rich content through REST APIs without having to download the binary.</span></span>
<span data-ttu-id="78028-131">Explore los metadatos extraídos de archivos de [foto][], [audio][] y [vídeo][].</span><span class="sxs-lookup"><span data-stu-id="78028-131">Explore extracted metadata from [photo][], [audio][], and [video][] files.</span></span>
<span data-ttu-id="78028-132">Use la [API de Excel][] para trabajar directamente con los datos sin procesar almacenados en un libro de Excel.</span><span class="sxs-lookup"><span data-stu-id="78028-132">Use the [Excel API][] to work directly with the raw data stored in an Excel workbook.</span></span>
<span data-ttu-id="78028-133">Use la [API de notas][] para obtener acceso a los contenidos de blocs de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="78028-133">Use the [Notes API][] to access the contents of OneNote notebooks.</span></span>

### <a name="react-to-file-changes"></a><span data-ttu-id="78028-134">Reaccionar a cambios en archivos</span><span class="sxs-lookup"><span data-stu-id="78028-134">React to file changes</span></span>

<span data-ttu-id="78028-135">Con los [webhooks][], su aplicación puede recibir notificaciones cuando cambie un archivo para que pueda reaccionar rápidamente.</span><span class="sxs-lookup"><span data-stu-id="78028-135">With [webhooks][], your app can get notified when files change so you can quickly react.</span></span>
<span data-ttu-id="78028-136">Use la [API delta][] para ver lo que cambió desde la última vez que la aplicación se sincronizó con la nube.</span><span class="sxs-lookup"><span data-stu-id="78028-136">Use the [delta API][] to see what changed since the last time your app synchronized with the cloud.</span></span>

## <a name="next-steps"></a><span data-ttu-id="78028-137">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="78028-137">Next steps</span></span>

<span data-ttu-id="78028-138">Obtenga más información sobre cómo [usar la API de OneDrive][Drive API] en Microsoft Graph v1.0.</span><span class="sxs-lookup"><span data-stu-id="78028-138">Find out more about [using the OneDrive API][Drive API] in Microsoft Graph v1.0.</span></span>

[SharePoint]: sharepoint-concept-overview.md
[selector de archivos]: https://dev.onedrive.com/sdk/js-v72/js-picker-overview.htm
[File picker]: https://dev.onedrive.com/sdk/js-v72/js-picker-overview.htm
[controlador de archivos]: https://docs.microsoft.com/onedrive/developer/file-handlers
[file handler]: https://docs.microsoft.com/onedrive/developer/file-handlers
<span data-ttu-id="78028-142">
  [carpetas especiales]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/drive_get_specialfolder</span><span class="sxs-lookup"><span data-stu-id="78028-142">[Special folders]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/drive_get_specialfolder</span></span>
<span data-ttu-id="78028-143">
  [API de notas]: https://developer.microsoft.com/en-us/graph/docs/concepts/integrate_with_onenote</span><span class="sxs-lookup"><span data-stu-id="78028-143">[Notes API]: https://developer.microsoft.com/en-us/graph/docs/concepts/integrate_with_onenote</span></span>
<span data-ttu-id="78028-144">
  [API de Excel]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/excel</span><span class="sxs-lookup"><span data-stu-id="78028-144">[Excel API]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/excel</span></span>
[REST API]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/onedrive
<span data-ttu-id="78028-145">
  [API delta]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_delta</span><span class="sxs-lookup"><span data-stu-id="78028-145">[delta API]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_delta</span></span>
<span data-ttu-id="78028-146">
  [vídeo]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/video</span><span class="sxs-lookup"><span data-stu-id="78028-146">[video]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/video</span></span>
<span data-ttu-id="78028-147">
  [foto]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/photo</span><span class="sxs-lookup"><span data-stu-id="78028-147">[photo]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/photo</span></span>
<span data-ttu-id="78028-148">
  [audio]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/audio</span><span class="sxs-lookup"><span data-stu-id="78028-148">[audio]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/audio</span></span>
<span data-ttu-id="78028-149">
  [formatos]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_get_content_format</span><span class="sxs-lookup"><span data-stu-id="78028-149">[Formats]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_get_content_format</span></span>
<span data-ttu-id="78028-150">
  [miniaturas]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_list_thumbnails</span><span class="sxs-lookup"><span data-stu-id="78028-150">[thumbnails]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_list_thumbnails</span></span>
<span data-ttu-id="78028-151">
  [vista previa]: https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/driveitem_preview</span><span class="sxs-lookup"><span data-stu-id="78028-151">[preview]: https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/driveitem_preview</span></span>
<span data-ttu-id="78028-152">
  [webhooks]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/webhooks</span><span class="sxs-lookup"><span data-stu-id="78028-152">[Webhooks]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/webhooks</span></span>
[Drive API]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/onedrive
