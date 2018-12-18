---
title: Información general sobre los usuarios en Microsoft Graph
description: Los usuarios son la representación de una cuenta de usuario profesional o educativa de Azure Active Directory (Azure AD) o una cuenta Microsoft en Microsoft Graph. El recurso **user** en Microsoft Graph es un centro desde donde puede obtener acceso a las relaciones y recursos que son relevantes para los usuarios.
author: dkershaw10
ms.openlocfilehash: f9e64ecd3f3a46a74b7a6bcd65955419fd102296
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337306"
---
# <a name="overview-of-users-in-microsoft-graph"></a><span data-ttu-id="3443a-104">Información general sobre los usuarios en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="3443a-104">Overview of users in Microsoft Graph</span></span>

<span data-ttu-id="3443a-105">Los usuarios son la representación de una cuenta de usuario profesional o educativa de Azure Active Directory (Azure AD) o una cuenta Microsoft en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="3443a-105">Users are the representation of an Azure Active Directory (Azure AD) work or school user account or a Microsoft account in Microsoft Graph.</span></span> <span data-ttu-id="3443a-106">El recurso **user** en Microsoft Graph es un centro desde donde puede obtener acceso a las relaciones y recursos que son relevantes para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="3443a-106">The **user** resource in Microsoft Graph is a hub from which you can access the relationships and resources that are relevant to your users.</span></span>

![Diagrama donde se muestra un usuario conectado a un calendario, correo electrónico, contactos, reuniones, tareas, sitios y documentos](images/users.png)

## <a name="develop-user-centric-applications"></a><span data-ttu-id="3443a-108">Desarrollar aplicaciones centradas en el usuario</span><span class="sxs-lookup"><span data-stu-id="3443a-108">Develop user-centric applications</span></span>

<span data-ttu-id="3443a-109">Puede usar Microsoft Graph para obtener acceso a las relaciones, documentos, contactos y preferencias que son relevantes contextualmente para el usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="3443a-109">You can use Microsoft Graph to access the relationships, documents, contacts, and preferences that are contextually relevant to the signed-in user.</span></span> <span data-ttu-id="3443a-110">El recurso **user** ofrece una forma sencilla de obtener acceso y manipular recursos de usuario sin tener que realizar llamadas adicionales, buscar información de autenticación específica y enviar directamente las consultas a otros recursos de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="3443a-110">The **user** resource provides straightforward way for you to access and manipulate user resources without having to perform additional calls, look up specific authentication information, and directly issue queries against other Microsoft Graph resources.</span></span>

<span data-ttu-id="3443a-111">Para obtener acceso a la información y los datos de un usuario, necesitará [obtener acceso en su nombre](auth-v2-user.md).</span><span class="sxs-lookup"><span data-stu-id="3443a-111">To access a user's information and data, you'll need to [get access on their behalf](auth-v2-user.md).</span></span> <span data-ttu-id="3443a-112">Al autenticar su aplicación con el [consentimiento del administrador](permissions-reference.md), podrá trabajar con más entidades asociadas a un usuario, así como actualizarlas.</span><span class="sxs-lookup"><span data-stu-id="3443a-112">Authenticating your application with [admin consent](permissions-reference.md) enables you to work with and update a wider range of entities associated with a user.</span></span>

### <a name="manage-your-organization"></a><span data-ttu-id="3443a-113">Administración de su organización</span><span class="sxs-lookup"><span data-stu-id="3443a-113">Manage your organization</span></span>

<span data-ttu-id="3443a-114">Cree usuarios en la organización, o actualice los recursos y las relaciones de los usuarios existentes.</span><span class="sxs-lookup"><span data-stu-id="3443a-114">Create new users in your organization or update the resources and relationships for existing users.</span></span> <span data-ttu-id="3443a-115">Puede usar Microsoft Graph para realizar las siguientes tareas de administración de usuarios:</span><span class="sxs-lookup"><span data-stu-id="3443a-115">You can use Microsoft Graph to perform the following user management tasks:</span></span> 

- <span data-ttu-id="3443a-116">Crear o eliminar usuarios en la organización de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3443a-116">Create or delete users in your Azure AD organization.</span></span>
- <span data-ttu-id="3443a-117">Mostrar una lista de pertenencias a grupos de un usuario y determinar si es miembro de un grupo.</span><span class="sxs-lookup"><span data-stu-id="3443a-117">List a user's group memberships and determine whether a user is a member of a group.</span></span>
- <span data-ttu-id="3443a-118">Mostrar una lista de los usuarios subordinados de otro usuario y asignar responsables a un usuario.</span><span class="sxs-lookup"><span data-stu-id="3443a-118">List the users who report to a user and assign managers to a user.</span></span>
- <span data-ttu-id="3443a-119">Cargar o recuperar una foto para el usuario.</span><span class="sxs-lookup"><span data-stu-id="3443a-119">Upload or retrieve a photo for the user.</span></span>

### <a name="work-with-calendars-and-tasks"></a><span data-ttu-id="3443a-120">Trabajar con calendarios y tareas</span><span class="sxs-lookup"><span data-stu-id="3443a-120">Work with calendars and tasks</span></span>

<span data-ttu-id="3443a-121">Puede ver, consultar y actualizar el calendario de un usuario y los grupos de calendarios asociados con un usuario; por ejemplo, puede:</span><span class="sxs-lookup"><span data-stu-id="3443a-121">You can view, query, and update user calendar and calendar groups associated with a user, including:</span></span>

- <span data-ttu-id="3443a-122">Mostrar una lista y crear eventos en el calendario de un usuario.</span><span class="sxs-lookup"><span data-stu-id="3443a-122">List and create events on a users calendar.</span></span>
- <span data-ttu-id="3443a-123">Ver las tareas asignadas a un usuario.</span><span class="sxs-lookup"><span data-stu-id="3443a-123">View tasks assigned to a user.</span></span>
- <span data-ttu-id="3443a-124">Encontrar horas para reuniones libres para un conjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="3443a-124">Find free meeting times for a set of users.</span></span>
- <span data-ttu-id="3443a-125">Obtener una lista de avisos establecidos en el calendario de un usuario.</span><span class="sxs-lookup"><span data-stu-id="3443a-125">Get a list of reminders set on a user's calendar.</span></span>

### <a name="administer-mail-and-handle-contacts"></a><span data-ttu-id="3443a-126">Administrar correos y contactos</span><span class="sxs-lookup"><span data-stu-id="3443a-126">Administer mail and handle contacts</span></span>

<span data-ttu-id="3443a-127">Puede configurar las opciones de correo de un usuario y las listas de contactos, así como enviar correo en nombre de un usuario; por ejemplo, puede:</span><span class="sxs-lookup"><span data-stu-id="3443a-127">You can configure user mail settings and contact lists and send mail on a user's behalf, including:</span></span>

- <span data-ttu-id="3443a-128">Mostrar una lista de mensajes de correo y enviar nuevos correos.</span><span class="sxs-lookup"><span data-stu-id="3443a-128">List mail messages and send new mail.</span></span>
- <span data-ttu-id="3443a-129">Crear y mostrar listas de contactos del usuario, y organizar los contactos en carpetas.</span><span class="sxs-lookup"><span data-stu-id="3443a-129">Create and list user contacts and organize contacts in folders.</span></span>
- <span data-ttu-id="3443a-130">Recuperar y actualizar opciones de configuración y carpetas de buzones.</span><span class="sxs-lookup"><span data-stu-id="3443a-130">Retrieve and update mailbox folders and settings.</span></span>

### <a name="enrich-your-app-with-user-insights"></a><span data-ttu-id="3443a-131">Enriquecer la aplicación con información del usuario</span><span class="sxs-lookup"><span data-stu-id="3443a-131">Enrich your app with user insights</span></span>

<span data-ttu-id="3443a-132">Maximice la relevancia en la aplicación al promocionar los documentos y contactos con más actividad, o bien usados recientemente, que estén asociados a un usuario.</span><span class="sxs-lookup"><span data-stu-id="3443a-132">Maximize relevance in your application by promoting recently used or trending documents and contacts associated with a user.</span></span> <span data-ttu-id="3443a-133">Puede usar Microsoft Graph para:</span><span class="sxs-lookup"><span data-stu-id="3443a-133">You can use Microsoft Graph to:</span></span>

- <span data-ttu-id="3443a-134">Devolver documentos vistos o modificados recientemente por un usuario.</span><span class="sxs-lookup"><span data-stu-id="3443a-134">Return documents recently viewed and modified by a user.</span></span>
- <span data-ttu-id="3443a-135">Devolver los documentos y sitios con más actividad de un usuario.</span><span class="sxs-lookup"><span data-stu-id="3443a-135">Return documents and sites trending around a user's activity.</span></span>
- <span data-ttu-id="3443a-136">Mostrar una lista de documentos compartidos con un usuario por correo electrónico o con OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="3443a-136">List documents shared with a user through email or OneDrive for Business.</span></span>

## <a name="api-reference"></a><span data-ttu-id="3443a-137">Referencia de la API</span><span class="sxs-lookup"><span data-stu-id="3443a-137">API reference</span></span>
<span data-ttu-id="3443a-138">¿Busca la referencia de la API para este servicio?</span><span class="sxs-lookup"><span data-stu-id="3443a-138">Looking for the API reference for this service?</span></span>

- [<span data-ttu-id="3443a-139">API de usuarios en Microsoft Graph v1.0</span><span class="sxs-lookup"><span data-stu-id="3443a-139">Users API in Microsoft Graph v1.0</span></span>](/graph/api/resources/users?view=graph-rest-1.0)
- [<span data-ttu-id="3443a-140">API de usuarios en Microsoft Graph beta</span><span class="sxs-lookup"><span data-stu-id="3443a-140">Users API in Microsoft Graph beta</span></span>](/graph/api/resources/users?view=graph-rest-beta)

## <a name="next-steps"></a><span data-ttu-id="3443a-141">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="3443a-141">Next steps</span></span>

- <span data-ttu-id="3443a-142">Obtenga más información sobre cómo [trabajar con usuarios](/graph/api/resources/users?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="3443a-142">Learn more about how to [work with users](/graph/api/resources/users?view=graph-rest-1.0).</span></span>
- <span data-ttu-id="3443a-143">Explore sus propios datos desde el recurso **user** en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="3443a-143">Explore your own data from the **user** resource in the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer).</span></span>
- <span data-ttu-id="3443a-144">Autentíquese con Microsoft Graph [en nombre de un usuario](auth-v2-user.md), o bien [como un demonio o servicio con el consentimiento de un administrador](auth-v2-service.md).</span><span class="sxs-lookup"><span data-stu-id="3443a-144">Authenticate with Microsoft Graph [on behalf of a user](auth-v2-user.md) or [as a daemon or service by consent of an administator](auth-v2-service.md).</span></span>
- <span data-ttu-id="3443a-145">Establezca directivas y control de acceso para usuarios con la [API de Azure AD](/graph/api/resources/azure-ad-overview?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="3443a-145">Set access control and policies for users with the [Azure AD API](/graph/api/resources/azure-ad-overview?view=graph-rest-1.0).</span></span>
- <span data-ttu-id="3443a-146">Revise los [permisos](permissions-reference.md) de la aplicación necesarios para obtener acceso a datos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="3443a-146">Review the [permissions](permissions-reference.md) your app will need to access user data.</span></span> 
<!-- This isn't really a next step; let's remove to keep the list of links concise.>
- Stay up to date with Microsoft Graph [changelog](changelog.md).
-->
