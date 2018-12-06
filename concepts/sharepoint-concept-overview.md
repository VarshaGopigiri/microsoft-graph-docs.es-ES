---
title: Información general sobre la API de contenido y sitios de SharePoint
description: SharePoint es su intranet móvil inteligente. Con SharePoint, los usuarios pueden compartir y administrar contenido, conocimientos y aplicaciones para mejorar el trabajo en equipo, buscar información y colaborar en la organización. Puede usar la API de REST de SharePoint en Microsoft Graph para integrar sus soluciones con contenidos y sitios de SharePoint.
ms.openlocfilehash: e71ef735cadf13ddb05799431fcf74ae9b3fa463
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092912"
---
# <a name="sharepoint-sites-and-content-api-overview"></a><span data-ttu-id="32375-105">Información general sobre la API de contenido y sitios de SharePoint</span><span class="sxs-lookup"><span data-stu-id="32375-105">SharePoint sites and content API overview</span></span>

<span data-ttu-id="32375-106">SharePoint es su intranet móvil inteligente.</span><span class="sxs-lookup"><span data-stu-id="32375-106">SharePoint is your mobile, intelligent intranet.</span></span> <span data-ttu-id="32375-107">Con SharePoint, los usuarios pueden compartir y administrar contenido, conocimientos y aplicaciones para mejorar el trabajo en equipo, buscar información y colaborar en la organización.</span><span class="sxs-lookup"><span data-stu-id="32375-107">With SharePoint, users can share and manage content, knowledge, and applications to empower teamwork, find information, and collaborate across an organization.</span></span> <span data-ttu-id="32375-108">Puede usar la API de REST de SharePoint en Microsoft Graph para integrar sus soluciones con contenidos y sitios de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="32375-108">You can use the SharePoint REST API in Microsoft Graph to integrate your solutions with SharePoint sites and content.</span></span>

## <a name="why-integrate-with-sharepoint-sites-and-content"></a><span data-ttu-id="32375-109">¿Por qué integrar con contenidos y sitios de SharePoint?</span><span class="sxs-lookup"><span data-stu-id="32375-109">Why integrate with SharePoint sites and content?</span></span>

<span data-ttu-id="32375-110">Los sitios de SharePoint mejoran la colaboración en grupo y la comunicación.</span><span class="sxs-lookup"><span data-stu-id="32375-110">SharePoint sites power team collaboration and communication.</span></span> <span data-ttu-id="32375-111">Grupos de Office 365, Microsoft Teams y los portales se basan en SharePoint, por lo que puede usar Microsoft Graph para obtener acceso a datos, sin importar dónde se encuentren.</span><span class="sxs-lookup"><span data-stu-id="32375-111">Office 365 groups, Microsoft Teams, and portals are all based on SharePoint, so you can use Microsoft Graph to access data no matter where it's kept.</span></span> <span data-ttu-id="32375-112">Use la API de SharePoint en Microsoft Graph para obtener acceso a:</span><span class="sxs-lookup"><span data-stu-id="32375-112">Use the SharePoint API in Microsoft Graph to access:</span></span>

- <span data-ttu-id="32375-113">Sitios de grupo que almacenen contenido donde colaboran los usuarios con sus compañeros.</span><span class="sxs-lookup"><span data-stu-id="32375-113">Team sites that store the content that users collaborate on with their coworkers.</span></span>
- <span data-ttu-id="32375-114">Portales y sitios de comunicación donde los usuarios publiquen páginas de contenido enriquecido que compartan con toda la organización.</span><span class="sxs-lookup"><span data-stu-id="32375-114">Communication sites and portals where users publish rich content pages to share across the organization.</span></span>

### <a name="unleash-your-data-with-sharepoint-lists"></a><span data-ttu-id="32375-115">Mejorar los datos con listas de SharePoint</span><span class="sxs-lookup"><span data-stu-id="32375-115">Unleash your data with SharePoint lists</span></span>

<span data-ttu-id="32375-116">Las [listas][lista] son la base del almacenamiento de datos en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="32375-116">[Lists][list] are the foundation for data storage in SharePoint.</span></span>
<span data-ttu-id="32375-117">[Cree listas][crear] para almacenar una amplia variedad de datos empresariales, desde una sencilla lista de contactos de clientes a una aplicación empresarial personalizada con PowerApps como front-end.</span><span class="sxs-lookup"><span data-stu-id="32375-117">[Create lists][create] to store a variety of business data, from a simple customer contact list to a custom business application, fronted with PowerApps.</span></span>
<span data-ttu-id="32375-118">Al usar [columnas][] para definir el esquema, SharePoint puede proteger la integridad de los datos, así como habilitar funciones enriquecidas de indexación, consultas y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="32375-118">When you use [columns][] to define your schema, SharePoint can protect the integrity of your data as well as enable  rich indexing, querying, and search capabilities.</span></span>

### <a name="bring-the-power-of-lists-to-your-teams-files"></a><span data-ttu-id="32375-119">Llevar las funciones avanzadas de las listas a los archivos de su equipo</span><span class="sxs-lookup"><span data-stu-id="32375-119">Bring the power of lists to your team's files</span></span>

<span data-ttu-id="32375-120">SharePoint almacena archivos en un [tipo de lista][] especial denominado biblioteca de documentos.</span><span class="sxs-lookup"><span data-stu-id="32375-120">SharePoint stores files in a special [list type][] called a document library.</span></span>
<span data-ttu-id="32375-121">Puede usar la [API de OneDrive para la Empresa][] y una biblioteca como una [unidad][], o bien puede usar la API de SharePoint para trabajar con una biblioteca como una [lista][].</span><span class="sxs-lookup"><span data-stu-id="32375-121">You can use the [OneDrive API][] to work with a library as a [drive][], or the SharePoint API to work with it as a [list][].</span></span>
<span data-ttu-id="32375-122">Al igual que con una lista normal, puede ampliar el esquema de una biblioteca de documentos para adaptarlo a sus necesidades empresariales con columnas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="32375-122">Just like a regular list, you can extend the schema of a Document Library to support your business needs with custom columns.</span></span>

### <a name="light-up-your-app-with-your-users-sharepoint-intranet-data"></a><span data-ttu-id="32375-123">Mejorar la aplicación con los datos de intranet de SharePoint de los usuarios</span><span class="sxs-lookup"><span data-stu-id="32375-123">Light up your app with your users' SharePoint intranet data</span></span>

<span data-ttu-id="32375-124">Con Microsoft Graph, puede mostrar los datos más importantes de los usuarios en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32375-124">With Microsoft Graph, you can surface your users' most important data within your app.</span></span>
<span data-ttu-id="32375-125">Para mantener actualizados los datos, realice [consultas][] en la lista donde se almacenen los datos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="32375-125">Keep things fresh by [querying][] the list that stores your users' data.</span></span>
<span data-ttu-id="32375-126">[Cree][] sus propias listas para la aplicación y permita a los usuarios obtener acceso a los datos en otras experiencias de SharePoint, o bien mantenga todo oculto.</span><span class="sxs-lookup"><span data-stu-id="32375-126">[Create][] your own lists for your app and let users access your data in other SharePoint experiences, or keep things hidden.</span></span>

### <a name="use-microsoft-graph-to-extend-sharepoint"></a><span data-ttu-id="32375-127">Usar Microsoft Graph para ampliar SharePoint</span><span class="sxs-lookup"><span data-stu-id="32375-127">Use Microsoft Graph to extend SharePoint</span></span>

<span data-ttu-id="32375-128">Como plataforma, SharePoint ofrece distintos modelos para la extensión e integración:</span><span class="sxs-lookup"><span data-stu-id="32375-128">As a platform, SharePoint provides several models for extension and integration:</span></span>

- <span data-ttu-id="32375-129">[SharePoint Framework][] ofrece una forma de crear elementos web con tecnologías del lado cliente y herramientas de código abierto que se pueden hospedar en páginas de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="32375-129">The [SharePoint Framework][] provides a way to build web parts using client-side technologies and open source tooling that can be hosted on SharePoint pages.</span></span>
- <span data-ttu-id="32375-130">Los [complementos de SharePoint][] son extensiones independientes que se pueden agregar a un sitio de SharePoint sin que sea necesario ejecutar código personalizado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="32375-130">[SharePoint Add-ins][] are self-contained extensions that can be added to a SharePoint site without the need for custom code to run on the server.</span></span>

<span data-ttu-id="32375-131">Cuando las aplicaciones se ejecutan en la página de SharePoint, puede usar fácilmente Microsoft Graph para obtener acceso a datos en Office 365.</span><span class="sxs-lookup"><span data-stu-id="32375-131">When your app runs within a SharePoint page, you can easily use Microsoft Graph to access data across Office 365.</span></span>

<span data-ttu-id="32375-132">Para obtener más información sobre estos modelos, visite el [Centro de desarrollo de SharePoint][] o la [Documentación para desarrolladores de SharePoint][].</span><span class="sxs-lookup"><span data-stu-id="32375-132">To learn about these models in more detail, visit the [SharePoint Dev Center][] or the [SharePoint Developer Docs][].</span></span>

## <a name="api-reference"></a><span data-ttu-id="32375-133">Referencia de la API</span><span class="sxs-lookup"><span data-stu-id="32375-133">API reference</span></span>
<span data-ttu-id="32375-134">¿Busca la referencia de la API para este servicio?</span><span class="sxs-lookup"><span data-stu-id="32375-134">Looking for the API reference for this service?</span></span>

- [<span data-ttu-id="32375-135">API de SharePoint en Microsoft Graph v1.0</span><span class="sxs-lookup"><span data-stu-id="32375-135">SharePoint API in Microsoft Graph v1.0</span></span>](/graph/api/resources/sharepoint?view=graph-rest-1.0)
- [<span data-ttu-id="32375-136">API de SharePoint en Microsoft Graph beta</span><span class="sxs-lookup"><span data-stu-id="32375-136">SharePoint API in Microsoft Graph beta</span></span>](/graph/api/resources/sharepoint?view=graph-rest-beta)

## <a name="next-steps"></a><span data-ttu-id="32375-137">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="32375-137">Next steps</span></span>

<span data-ttu-id="32375-138">Obtenga más información sobre cómo [trabajar con sitios][SharePoint] para empezar a usar SharePoint en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="32375-138">Get started with SharePoint in Microsoft Graph by learning more about [working with sites][SharePoint].</span></span>

[lista]: /graph/api/resources/list?view=graph-rest-1.0
[list]: /graph/api/resources/list?view=graph-rest-1.0
[columnas]: /graph/api/resources/columndefinition?view=graph-rest-1.0
[columns]: /graph/api/resources/columndefinition?view=graph-rest-1.0
[tipo de lista]: /graph/api/resources/listinfo?view=graph-rest-1.0
[list type]: /graph/api/resources/listinfo?view=graph-rest-1.0
[crear]: /graph/api/list-create?view=graph-rest-1.0
[create]: /graph/api/list-create?view=graph-rest-1.0
[consultas]: /graph/api/listitem-get?view=graph-rest-1.0
[querying]: /graph/api/listitem-get?view=graph-rest-1.0
[unidad]: /graph/api/resources/drive?view=graph-rest-1.0
[drive]: /graph/api/resources/drive?view=graph-rest-1.0
[API de OneDrive]: /graph/api/resources/onedrive?view=graph-rest-1.0
[OneDrive API]: /graph/api/resources/onedrive?view=graph-rest-1.0
[SharePoint Framework]: https://docs.microsoft.com/sharepoint/dev/spfx/sharepoint-framework-overview
[Complementos de SharePoint]: https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins
[SharePoint Add-ins]: https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins
[Centro de desarrollo de SharePoint]: https://developer.microsoft.com/sharepoint
[SharePoint Dev Center]: https://developer.microsoft.com/sharepoint
[Documentación para desarrolladores de SharePoint]: https://aka.ms/spdev-docs
[SharePoint Developer Docs]: https://aka.ms/spdev-docs
[SharePoint]: /graph/api/resources/sharepoint?view=graph-rest-1.0
