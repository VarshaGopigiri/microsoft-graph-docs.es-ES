# <a name="use-the-onenote-rest-api"></a><span data-ttu-id="c2a1d-101">Usar la API de REST de OneNote</span><span class="sxs-lookup"><span data-stu-id="c2a1d-101">Use the OneNote REST API</span></span>

<span data-ttu-id="c2a1d-102">Microsoft Graph permite a su aplicación obtener autorización de acceso a blocs de notas OneNote de un usuario, a secciones y páginas en una cuenta personal u organizativa.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-102">Microsoft Graph lets your app get authorized access to a user's OneNote notebooks, sections, and pages in a personal or organization account.</span></span> <span data-ttu-id="c2a1d-103">Con los [permisos adecuados delegados o de la aplicación](../../../concepts/permissions_reference.md#notes-permissions), la aplicación puede tener acceso a los datos de OneNote del usuario que haya iniciado sesión o cualquier usuario en una cuenta empresarial.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-103">With the [appropriate delegated or application permissions](../../../concepts/permissions_reference.md#notes-permissions), your app can access the OneNote data of the signed-in user or any user in a tenant.</span></span>

## <a name="root-url"></a><span data-ttu-id="c2a1d-104">Dirección URL raíz</span><span class="sxs-lookup"><span data-stu-id="c2a1d-104">Root URL</span></span>
<span data-ttu-id="c2a1d-105">La dirección URL raíz del servicio OneNote utiliza el siguiente formato para todas las llamadas a la API de OneNote.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-105">The OneNote service root URL uses the following format for all calls to the OneNote API.</span></span>
```
https://graph.microsoft.com/{version}/{location}/onenote/ 
```
<span data-ttu-id="c2a1d-106">El segmento `version` de la URL representa la versión de Microsoft Graph que quiere utilizar:</span><span class="sxs-lookup"><span data-stu-id="c2a1d-106">The `version` segment in the URL represents the version of Microsoft Graph that you want to use.</span></span>

- <span data-ttu-id="c2a1d-107">`v1.0` corresponde al código de producción estable.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-107">`v1.0` is for stable production code.</span></span>
- <span data-ttu-id="c2a1d-108">`beta` corresponde a la prueba de una característica que se encuentra en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-108">`beta` is to try out a feature that's in development.</span></span> <span data-ttu-id="c2a1d-109">Pueden cambiar las características y la funcionalidad en el extremo de la versión beta; no se recomienda usarlos en el código de producción.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-109">Features and functionality in the beta endpoint might change; we don't recommend that you use it in your production code.</span></span>

<span data-ttu-id="c2a1d-110">La ubicación puede ser el bloc de notas del usuario en Office 365 o OneDrive para consumidores, los blocs de notas de grupo o blocs de notas de grupo hospedados en un sitio de SharePoint en Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-110">The location can be user notebooks on Office 365 or consumer OneDrive, group notebooks or SharePoint site-hosted team notebooks on Office 365.</span></span> 

![Pila de desarrollo de la API de OneNote](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/onenote-dev-diagram.png)

### <a name="user-notebooks"></a><span data-ttu-id="c2a1d-112">Blocs de notas de usuario</span><span class="sxs-lookup"><span data-stu-id="c2a1d-112">User notebooks</span></span>
<span data-ttu-id="c2a1d-113">Para obtener acceso a los blocs de notas personales en OneDrive para consumidores o para la empresa, utilice una de las siguientes direcciones URL:</span><span class="sxs-lookup"><span data-stu-id="c2a1d-113">User notebooks To access personal notebooks on consumer OneDrive or OneDrive for Business, use one of the following URLs:</span></span>

```
https://graph.microsoft.com/{version}/me/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{userPrincipalName}/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

- <span data-ttu-id="c2a1d-114">`me` corresponde a contenido de OneNote al que el usuario actual tiene acceso (de su propiedad y compartido).</span><span class="sxs-lookup"><span data-stu-id="c2a1d-114">`me` is for OneNote content that the current user can access (owned and shared).</span></span>
- <span data-ttu-id="c2a1d-115">`users/{id}` corresponde a contenido de OneNote que el usuario especificado (en la dirección URL) ha compartido con el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-115">`users/{id}` is for OneNote content that the specified user (in the URL) has shared with the current user.</span></span> <span data-ttu-id="c2a1d-116">Use la API de los [usuarios](users.md).</span><span class="sxs-lookup"><span data-stu-id="c2a1d-116">[Use the Planner API](users.md)</span></span>
> <span data-ttu-id="c2a1d-117">**Nota:** Puede obtener identificadores de usuario realizando una solicitud GET en `https://graph.microsoft.com/v1.0/users`.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-117">**Note:** You can get user ids by making a GET request on `https://graph.microsoft.com/v1.0/users`.</span></span>

### <a name="group-notebooks"></a><span data-ttu-id="c2a1d-118">Blocs de notas de grupo</span><span class="sxs-lookup"><span data-stu-id="c2a1d-118">Group notebooks</span></span>
<span data-ttu-id="c2a1d-119">Para obtener acceso a los blocs de notas que pertenecen a un grupo, utilice la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="c2a1d-119">Group notebooks To access notebooks that are owned by a group, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/groups/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
### <a name="sharepoint-site-notebooks"></a><span data-ttu-id="c2a1d-120">Blocs de notas del sitio de SharePoint</span><span class="sxs-lookup"><span data-stu-id="c2a1d-120">SharePoint site notebooks</span></span>

<span data-ttu-id="c2a1d-121">Para obtener acceso a los blocs de notas que pertenecen a un sitio de grupo de SharePoint, use la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="c2a1d-121">SharePoint site notebooks To access notebooks that are owned by a SharePoint team site, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/sites/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

