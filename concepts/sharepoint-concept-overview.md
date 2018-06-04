# <a name="sharepoint-sites-and-content-api-overview"></a><span data-ttu-id="635f4-101">Información general sobre la API de contenido y sitios de SharePoint</span><span class="sxs-lookup"><span data-stu-id="635f4-101">SharePoint sites and content API overview</span></span>

<span data-ttu-id="635f4-102">SharePoint es su intranet móvil inteligente.</span><span class="sxs-lookup"><span data-stu-id="635f4-102">SharePoint is your mobile, intelligent intranet.</span></span> <span data-ttu-id="635f4-103">Con SharePoint, los usuarios pueden compartir y administrar contenido, conocimientos y aplicaciones para mejorar el trabajo en equipo, buscar información y colaborar en la organización.</span><span class="sxs-lookup"><span data-stu-id="635f4-103">With SharePoint, users can share and manage content, knowledge, and applications to empower teamwork, find information, and collaborate across an organization.</span></span> <span data-ttu-id="635f4-104">Puede usar la API de REST de SharePoint en Microsoft Graph para integrar sus soluciones con contenidos y sitios de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="635f4-104">You can use the SharePoint REST API in Microsoft Graph to integrate your solutions with SharePoint sites and content.</span></span>

## <a name="why-integrate-with-sharepoint-sites-and-content"></a><span data-ttu-id="635f4-105">¿Por qué integrar con contenidos y sitios de SharePoint?</span><span class="sxs-lookup"><span data-stu-id="635f4-105">Why integrate with SharePoint sites and content?</span></span>

<span data-ttu-id="635f4-106">Los sitios de SharePoint mejoran la colaboración en grupo y la comunicación.</span><span class="sxs-lookup"><span data-stu-id="635f4-106">SharePoint sites power team collaboration and communication.</span></span> <span data-ttu-id="635f4-107">Grupos de Office 365, Microsoft Teams y los portales se basan en SharePoint, por lo que puede usar Microsoft Graph para obtener acceso a datos, sin importar dónde se encuentren.</span><span class="sxs-lookup"><span data-stu-id="635f4-107">Office 365 groups, Microsoft Teams, and portals are all based on SharePoint, so you can use Microsoft Graph to access data no matter where it's kept.</span></span> <span data-ttu-id="635f4-108">Use la API de SharePoint en Microsoft Graph para obtener acceso a:</span><span class="sxs-lookup"><span data-stu-id="635f4-108">Use the SharePoint API in Microsoft Graph to access:</span></span>

- <span data-ttu-id="635f4-109">Sitios de grupo que almacenen contenido donde colaboran los usuarios con sus compañeros.</span><span class="sxs-lookup"><span data-stu-id="635f4-109">Team sites that store the content that users collaborate on with their coworkers.</span></span>
- <span data-ttu-id="635f4-110">Portales y sitios de comunicación donde los usuarios publiquen páginas de contenido enriquecido que compartan con toda la organización.</span><span class="sxs-lookup"><span data-stu-id="635f4-110">Communication sites and portals where users publish rich content pages to share across the organization.</span></span>

### <a name="unleash-your-data-with-sharepoint-lists"></a><span data-ttu-id="635f4-111">Mejorar los datos con listas de SharePoint</span><span class="sxs-lookup"><span data-stu-id="635f4-111">Unleash your data with SharePoint lists</span></span>

<span data-ttu-id="635f4-112">Las [listas][lista] son la base del almacenamiento de datos en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="635f4-112">[Lists][list] are the foundation for data storage in SharePoint.</span></span>
<span data-ttu-id="635f4-113">[Cree listas][crear] para almacenar una amplia variedad de datos empresariales, desde una sencilla lista de contactos de clientes a una aplicación empresarial personalizada con PowerApps como front-end.</span><span class="sxs-lookup"><span data-stu-id="635f4-113">[Create lists][create] to store a variety of business data, from a simple customer contact list to a custom business application, fronted with PowerApps.</span></span>
<span data-ttu-id="635f4-114">Al usar [columnas][] para definir el esquema, SharePoint puede proteger la integridad de los datos, así como habilitar funciones enriquecidas de indexación, consultas y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="635f4-114">When you use [columns][] to define your schema, SharePoint can protect the integrity of your data as well as enable  rich indexing, querying, and search capabilities.</span></span>

### <a name="bring-the-power-of-lists-to-your-teams-files"></a><span data-ttu-id="635f4-115">Llevar las funciones avanzadas de las listas a los archivos de su equipo</span><span class="sxs-lookup"><span data-stu-id="635f4-115">Bring the power of lists to your team's files</span></span>

<span data-ttu-id="635f4-116">SharePoint almacena archivos en un [tipo de lista][] especial denominado biblioteca de documentos.</span><span class="sxs-lookup"><span data-stu-id="635f4-116">SharePoint stores files in a special [list type][] called a document library.</span></span>
<span data-ttu-id="635f4-117">Puede usar la [API de OneDrive para la Empresa][] y una biblioteca como una [unidad][], o bien puede usar la API de SharePoint para trabajar con una biblioteca como una [lista][].</span><span class="sxs-lookup"><span data-stu-id="635f4-117">You can use the [OneDrive API][] to work with a library as a [drive][], or the SharePoint API to work with it as a [list][].</span></span>
<span data-ttu-id="635f4-118">Al igual que con una lista normal, puede ampliar el esquema de una biblioteca de documentos para adaptarlo a sus necesidades empresariales con columnas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="635f4-118">Just like a regular list, you can extend the schema of a Document Library to support your business needs with custom columns.</span></span>

### <a name="light-up-your-app-with-your-users-sharepoint-intranet-data"></a><span data-ttu-id="635f4-119">Mejorar la aplicación con los datos de intranet de SharePoint de los usuarios</span><span class="sxs-lookup"><span data-stu-id="635f4-119">Light up your app with your users' SharePoint intranet data</span></span>

<span data-ttu-id="635f4-120">Con Microsoft Graph, puede mostrar los datos más importantes de los usuarios en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="635f4-120">With Microsoft Graph, you can surface your users' most important data within your app.</span></span>
<span data-ttu-id="635f4-121">Para mantener actualizados los datos, realice [consultas][] en la lista donde se almacenen los datos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="635f4-121">Keep things fresh by [querying][] the list that stores your users' data.</span></span>
<span data-ttu-id="635f4-122">[Cree][] sus propias listas para la aplicación y permita a los usuarios obtener acceso a los datos en otras experiencias de SharePoint, o bien mantenga todo oculto.</span><span class="sxs-lookup"><span data-stu-id="635f4-122">[Create][] your own lists for your app and let users access your data in other SharePoint experiences, or keep things hidden.</span></span>

### <a name="use-microsoft-graph-to-extend-sharepoint"></a><span data-ttu-id="635f4-123">Usar Microsoft Graph para ampliar SharePoint</span><span class="sxs-lookup"><span data-stu-id="635f4-123">Use Microsoft Graph to extend SharePoint</span></span>

<span data-ttu-id="635f4-124">Como plataforma, SharePoint ofrece distintos modelos para la extensión e integración:</span><span class="sxs-lookup"><span data-stu-id="635f4-124">As a platform, SharePoint provides several models for extension and integration:</span></span>

- <span data-ttu-id="635f4-125">[SharePoint Framework][] ofrece una forma de crear elementos web con tecnologías del lado cliente y herramientas de código abierto que se pueden hospedar en páginas de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="635f4-125">The [SharePoint Framework][] provides a way to build web parts using client-side technologies and open source tooling that can be hosted on SharePoint pages.</span></span>
- <span data-ttu-id="635f4-126">Los [complementos de SharePoint][] son extensiones independientes que se pueden agregar a un sitio de SharePoint sin que sea necesario ejecutar código personalizado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="635f4-126">[SharePoint Add-ins][] are self-contained extensions that can be added to a SharePoint site without the need for custom code to run on the server.</span></span>

<span data-ttu-id="635f4-127">Cuando las aplicaciones se ejecutan en la página de SharePoint, puede usar fácilmente Microsoft Graph para obtener acceso a datos en Office 365.</span><span class="sxs-lookup"><span data-stu-id="635f4-127">When your app runs within a SharePoint page, you can easily use Microsoft Graph to access data across Office 365.</span></span>

<span data-ttu-id="635f4-128">Para obtener más información sobre estos modelos, visite el [Centro de desarrollo de SharePoint][] o la [Documentación para desarrolladores de SharePoint][].</span><span class="sxs-lookup"><span data-stu-id="635f4-128">To learn about these models in more detail, visit the [SharePoint Dev Center][] or the [SharePoint Developer Docs][].</span></span>

## <a name="next-steps"></a><span data-ttu-id="635f4-129">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="635f4-129">Next steps</span></span>

<span data-ttu-id="635f4-130">Obtenga más información sobre cómo [trabajar con sitios][SharePoint] para empezar a usar SharePoint en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="635f4-130">Get started with SharePoint in Microsoft Graph by learning more about [working with sites][SharePoint].</span></span>

[lista]: ../api-reference/v1.0/resources/list.md
[list]: ../api-reference/v1.0/resources/list.md
[columnas]: ../api-reference/v1.0/resources/columndefinition.md
[columns]: ../api-reference/v1.0/resources/columndefinition.md
[tipo de lista]: ../api-reference/v1.0/resources/listinfo.md
[List Type]: ../api-reference/v1.0/resources/listinfo.md
[crear]: ../api-reference/v1.0/api/list_create.md
[Create]: ../api-reference/v1.0/api/list_create.md.
[consultas]: ../api-reference/v1.0/api/listitem_get.md
[querying]: ../api-reference/v1.0/api/listitem_get.md
[unidad]: ../api-reference/v1.0/resources/drive.md
[drive]: ../api-reference/v1.0/resources/drive.md
<span data-ttu-id="635f4-137">
  [API de OneDrive]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/onedrive</span><span class="sxs-lookup"><span data-stu-id="635f4-137">[onedrive api]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/onedrive</span></span>
[SharePoint Framework]: https://docs.microsoft.com/sharepoint/dev/spfx/sharepoint-framework-overview
[Complementos de SharePoint]: https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins
[SharePoint Add-ins]: https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins
[Centro de desarrollo de SharePoint]: https://developer.microsoft.com/sharepoint
[SharePoint Dev Center]: https://developer.microsoft.com/sharepoint
[Documentación para desarrolladores de SharePoint]: http://aka.ms/spdev-docs
[SharePoint Developer Docs]: http://aka.ms/spdev-docs
[SharePoint]: https://developer.microsoft.com/graph/docs/api-reference/v1.0/resources/sharepoint
