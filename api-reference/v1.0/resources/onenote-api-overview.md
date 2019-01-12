---
title: Usar la API de REST de OneNote
description: Microsoft Graph permite a la aplicación obtener autorización para obtener acceso a blocs de notas OneNote de un usuario, en las secciones y páginas en una cuenta personal o la organización. Con la correspondiente delegada o permisos de aplicación, la aplicación pueden tener acceso a los datos de OneNote de cualquier usuario en un inquilino o el usuario ha iniciado sesión.
localization_priority: Priority
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: ceb5ac30786ecfd207a2076d471e9d004b60f8d3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951540"
---
# <a name="use-the-onenote-rest-api"></a><span data-ttu-id="349e2-104">Usar la API de REST de OneNote</span><span class="sxs-lookup"><span data-stu-id="349e2-104">Use the OneNote REST API</span></span>

<span data-ttu-id="349e2-105">Microsoft Graph permite a la aplicación obtener autorización para obtener acceso a blocs de notas OneNote de un usuario, en las secciones y páginas en una cuenta personal o la organización.</span><span class="sxs-lookup"><span data-stu-id="349e2-105">Microsoft Graph lets your app get authorized access to a user's OneNote notebooks, sections, and pages in a personal or organization account.</span></span> <span data-ttu-id="349e2-106">Con los [permisos adecuados de delegado o de la aplicación](/graph/permissions-reference#notes-permissions), la aplicación puede tener acceso a los datos de OneNote del usuario que ha iniciado sesión o cualquier usuario en un inquilino.</span><span class="sxs-lookup"><span data-stu-id="349e2-106">With the [appropriate delegated or application permissions](/graph/permissions-reference#notes-permissions), your app can access the OneNote data of the signed-in user or any user in a tenant.</span></span>

## <a name="root-url"></a><span data-ttu-id="349e2-107">Dirección URL raíz</span><span class="sxs-lookup"><span data-stu-id="349e2-107">Root URL</span></span>
<span data-ttu-id="349e2-108">La dirección URL raíz del servicio OneNote utiliza el siguiente formato para todas las llamadas a la API de OneNote.</span><span class="sxs-lookup"><span data-stu-id="349e2-108">The OneNote service root URL uses the following format for all calls to the OneNote API.</span></span>
```
https://graph.microsoft.com/{version}/{location}/onenote/ 
```
<span data-ttu-id="349e2-109">El `version` segmento en la dirección URL representa la versión de Microsoft Graph que va a usar:</span><span class="sxs-lookup"><span data-stu-id="349e2-109">The `version` segment in the URL represents the version of Microsoft Graph that you want to use:</span></span>

- <span data-ttu-id="349e2-110">`v1.0` corresponde al código de producción estable.</span><span class="sxs-lookup"><span data-stu-id="349e2-110">`v1.0` is for stable production code.</span></span>
- <span data-ttu-id="349e2-111">`beta` corresponde a la prueba de una característica que se encuentra en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="349e2-111">`beta` is to try out a feature that's in development.</span></span> <span data-ttu-id="349e2-112">Pueden cambiar las características y funcionalidad en el extremo de la versión beta; no se recomienda usarlo en el código de producción.</span><span class="sxs-lookup"><span data-stu-id="349e2-112">Features and functionality in the beta endpoint might change; we don't recommend that you use it in your production code.</span></span>

<span data-ttu-id="349e2-113">La ubicación puede ser blocs de notas de usuario en Office 365 o consumidor OneDrive, los blocs de notas de grupo o los blocs de notas de equipo hospedada en el sitio de SharePoint en Office 365.</span><span class="sxs-lookup"><span data-stu-id="349e2-113">The location can be user notebooks on Office 365 or consumer OneDrive, group notebooks, or SharePoint site-hosted team notebooks on Office 365.</span></span> 

![Pila de desarrollo de API de OneNote](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/onenote-dev-diagram.png)

### <a name="user-notebooks"></a><span data-ttu-id="349e2-115">Blocs de notas de usuario</span><span class="sxs-lookup"><span data-stu-id="349e2-115">User notebooks</span></span>
<span data-ttu-id="349e2-116">Para obtener acceso a blocs de notas personales en consumidor OneDrive o OneDrive para la empresa, utilice una de las siguientes direcciones URL:</span><span class="sxs-lookup"><span data-stu-id="349e2-116">To access personal notebooks on consumer OneDrive or OneDrive for Business, use one of the following URLs:</span></span>

```
https://graph.microsoft.com/{version}/me/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{userPrincipalName}/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

- <span data-ttu-id="349e2-117">`me` corresponde a contenido de OneNote al que el usuario actual tiene acceso (de su propiedad y compartido).</span><span class="sxs-lookup"><span data-stu-id="349e2-117">`me` is for OneNote content that the current user can access (owned and shared).</span></span>
- <span data-ttu-id="349e2-118">`users/{id}` corresponde a contenido de OneNote que el usuario especificado (en la dirección URL) ha compartido con el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="349e2-118">`users/{id}` is for OneNote content that the specified user (in the URL) has shared with the current user.</span></span> <span data-ttu-id="349e2-119">Usar la API de [los usuarios](users.md) .</span><span class="sxs-lookup"><span data-stu-id="349e2-119">Use the [users](users.md) API.</span></span>
> <span data-ttu-id="349e2-120">**Nota:** Puede obtener los identificadores de usuario mediante la realización de una solicitud GET en `https://graph.microsoft.com/v1.0/users`.</span><span class="sxs-lookup"><span data-stu-id="349e2-120">**Note:** You can get user IDs by making a GET request on `https://graph.microsoft.com/v1.0/users`.</span></span>

### <a name="group-notebooks"></a><span data-ttu-id="349e2-121">Blocs de notas de grupo</span><span class="sxs-lookup"><span data-stu-id="349e2-121">Group notebooks</span></span>
<span data-ttu-id="349e2-122">Para obtener acceso a blocs de notas que pertenecen a un grupo, utilice la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="349e2-122">To access notebooks that are owned by a group, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/groups/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
### <a name="sharepoint-site-notebooks"></a><span data-ttu-id="349e2-123">Blocs de notas del sitio de SharePoint</span><span class="sxs-lookup"><span data-stu-id="349e2-123">SharePoint site notebooks</span></span>

<span data-ttu-id="349e2-124">Para obtener acceso a blocs de notas que pertenecen a un sitio de grupo de SharePoint, use la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="349e2-124">To access notebooks that are owned by a SharePoint team site, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/sites/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

