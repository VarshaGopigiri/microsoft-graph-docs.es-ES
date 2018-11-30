---
title: Usar la API de REST de OneNote
description: 'Microsoft Graph permite a la aplicación obtener autorización para obtener acceso a blocs de notas OneNote de un usuario, en las secciones y páginas en una cuenta personal o la organización. Con la correspondiente delegada o permisos de aplicación, la aplicación pueden tener acceso a los datos de OneNote de cualquier usuario en un inquilino o el usuario ha iniciado sesión. '
ms.openlocfilehash: 091dd18cbcfae2a4058aff71df14ed7aa5fd7a03
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090801"
---
# <a name="use-the-onenote-rest-api"></a><span data-ttu-id="14892-104">Usar la API de REST de OneNote</span><span class="sxs-lookup"><span data-stu-id="14892-104">Use the OneNote REST API</span></span>

> <span data-ttu-id="14892-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="14892-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="14892-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="14892-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="14892-107">Microsoft Graph permite a la aplicación obtener autorización para obtener acceso a blocs de notas OneNote de un usuario, en las secciones y páginas en una cuenta personal o la organización.</span><span class="sxs-lookup"><span data-stu-id="14892-107">Microsoft Graph lets your app get authorized access to a user's OneNote notebooks, sections, and pages in a personal or organization account.</span></span> <span data-ttu-id="14892-108">Con los [permisos adecuados de delegado o de la aplicación](/graph/permissions-reference#notes-permissions), la aplicación puede tener acceso a los datos de OneNote del usuario que ha iniciado sesión o cualquier usuario en un inquilino.</span><span class="sxs-lookup"><span data-stu-id="14892-108">With the [appropriate delegated or application permissions](/graph/permissions-reference#notes-permissions), your app can access the OneNote data of the signed-in user or any user in a tenant.</span></span> 

## <a name="root-url"></a><span data-ttu-id="14892-109">Dirección URL raíz</span><span class="sxs-lookup"><span data-stu-id="14892-109">Root URL</span></span>
<span data-ttu-id="14892-110">La dirección URL raíz del servicio OneNote utiliza el siguiente formato para todas las llamadas a la API de OneNote.</span><span class="sxs-lookup"><span data-stu-id="14892-110">The OneNote service root URL uses the following format for all calls to the OneNote API.</span></span>
```
https://graph.microsoft.com/{version}/{location}/onenote/ 
```

<span data-ttu-id="14892-111">El `version` segmento en la dirección URL representa la versión de Microsoft Graph que va a usar:</span><span class="sxs-lookup"><span data-stu-id="14892-111">The `version` segment in the URL represents the version of Microsoft Graph that you want to use:</span></span>

- <span data-ttu-id="14892-112">`v1.0` corresponde al código de producción estable.</span><span class="sxs-lookup"><span data-stu-id="14892-112">`v1.0` is for stable production code.</span></span>
- <span data-ttu-id="14892-113">`beta` corresponde a la prueba de una característica que se encuentra en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="14892-113">`beta` is to try out a feature that's in development.</span></span> <span data-ttu-id="14892-114">Pueden cambiar las características y funcionalidad en el extremo de la versión beta; no se recomienda usarlo en el código de producción.</span><span class="sxs-lookup"><span data-stu-id="14892-114">Features and functionality in the beta endpoint might change; we don't recommend that you use it in your production code.</span></span>

<span data-ttu-id="14892-115">La ubicación puede ser blocs de notas de usuario en Office 365 o consumidor OneDrive, los blocs de notas de grupo o los blocs de notas de equipo hospedada en el sitio de SharePoint en Office 365.</span><span class="sxs-lookup"><span data-stu-id="14892-115">The location can be user notebooks on Office 365 or consumer OneDrive, group notebooks, or SharePoint site-hosted team notebooks on Office 365.</span></span> 

![Pila de desarrollo de API de OneNote](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/onenote-dev-diagram.png)

### <a name="user-notebooks"></a><span data-ttu-id="14892-117">Blocs de notas de usuario</span><span class="sxs-lookup"><span data-stu-id="14892-117">User notebooks</span></span>
<span data-ttu-id="14892-118">Para obtener acceso a blocs de notas personales en consumidor OneDrive o OneDrive para la empresa, utilice una de las siguientes direcciones URL:</span><span class="sxs-lookup"><span data-stu-id="14892-118">To access personal notebooks on consumer OneDrive or OneDrive for Business, use one of the following URLs:</span></span>

```
https://graph.microsoft.com/{version}/me/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{userPrincipalName}/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

- <span data-ttu-id="14892-119">`me` corresponde a contenido de OneNote al que el usuario actual tiene acceso (de su propiedad y compartido).</span><span class="sxs-lookup"><span data-stu-id="14892-119">`me` is for OneNote content that the current user can access (owned and shared).</span></span>
- <span data-ttu-id="14892-120">`users/{id}` corresponde a contenido de OneNote que el usuario especificado (en la dirección URL) ha compartido con el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="14892-120">`users/{id}` is for OneNote content that the specified user (in the URL) has shared with the current user.</span></span> <span data-ttu-id="14892-121">Usar la API de [los usuarios](users.md) .</span><span class="sxs-lookup"><span data-stu-id="14892-121">Use the [users](users.md) API.</span></span>
> <span data-ttu-id="14892-122">**Nota:** Puede obtener los identificadores de usuario mediante la realización de una solicitud GET en `https://graph.microsoft.com/v1.0/users`.</span><span class="sxs-lookup"><span data-stu-id="14892-122">**Note:** You can get user IDs by making a GET request on `https://graph.microsoft.com/v1.0/users`.</span></span>

### <a name="group-notebooks"></a><span data-ttu-id="14892-123">Blocs de notas de grupo</span><span class="sxs-lookup"><span data-stu-id="14892-123">Group notebooks</span></span>

<span data-ttu-id="14892-124">Para obtener acceso a blocs de notas que pertenecen a un grupo, utilice la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="14892-124">To access notebooks that are owned by a group, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/groups/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
### <a name="sharepoint-site-notebooks"></a><span data-ttu-id="14892-125">Blocs de notas del sitio de SharePoint</span><span class="sxs-lookup"><span data-stu-id="14892-125">SharePoint site notebooks</span></span>
<span data-ttu-id="14892-126">Para obtener acceso a blocs de notas que pertenecen a un sitio de grupo de SharePoint, use la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="14892-126">To access notebooks that are owned by a SharePoint team site, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/sites/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
