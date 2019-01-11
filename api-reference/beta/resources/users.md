---
title: Trabajar con usuarios en Microsoft Graph
description: Puede usar Microsoft Graph para crear experiencias de aplicaciones convincentes basadas en usuarios, sus relaciones con otros usuarios y grupos y su correo, calendario y archivos.
localization_priority: Priority
ms.openlocfilehash: d9b699c008186f165a8be43ab4254213697710dc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860833"
---
# <a name="working-with-users-in-microsoft-graph"></a><span data-ttu-id="7c51e-103">Trabajar con usuarios en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="7c51e-103">Working with users in Microsoft Graph</span></span>

> <span data-ttu-id="7c51e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7c51e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7c51e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7c51e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7c51e-106">Puede usar Microsoft Graph para crear experiencias de aplicaciones convincentes basadas en usuarios, sus relaciones con otros usuarios y grupos y su correo, calendario y archivos.</span><span class="sxs-lookup"><span data-stu-id="7c51e-106">You can use Microsoft Graph to build compelling app experiences based on users, their relationships with other users and groups, and their mail, calendar, and files.</span></span>

<span data-ttu-id="7c51e-107">Puede acceder a los usuarios a través de Microsoft Graph de dos formas:</span><span class="sxs-lookup"><span data-stu-id="7c51e-107">You can access users through Microsoft Graph in two ways:</span></span>

- <span data-ttu-id="7c51e-108">Mediante su identificador, `/users/{id}`</span><span class="sxs-lookup"><span data-stu-id="7c51e-108">By their ID, `/users/{id}`</span></span> 
- <span data-ttu-id="7c51e-109">Mediante el alias `/me` del usuario que ha iniciado sesión, que es el mismo que `/users/{signed-in user's id}`</span><span class="sxs-lookup"><span data-stu-id="7c51e-109">By using the `/me` alias for the signed-in user, which is the same as `/users/{signed-in user's id}`</span></span>

## <a name="authorization"></a><span data-ttu-id="7c51e-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="7c51e-110">Authorization</span></span>
<span data-ttu-id="7c51e-p102">Se requiere uno de los siguientes [permisos](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) para acceder a las operaciones de usuario. Los tres primeros permisos los puede conceder un usuario a una aplicación. El resto solo los puede conceder el administrador a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="7c51e-p102">One of the following [permissions](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) is required to access user operations. The first three permissions can be granted to an app by a user. The rest can only be granted to an app by the administrator.</span></span>

- <span data-ttu-id="7c51e-114">User.ReadBasic.All</span><span class="sxs-lookup"><span data-stu-id="7c51e-114">User.ReadBasic.All</span></span>
- <span data-ttu-id="7c51e-115">User.Read</span><span class="sxs-lookup"><span data-stu-id="7c51e-115">User.Read</span></span>
- <span data-ttu-id="7c51e-116">User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7c51e-116">User.ReadWrite</span></span>
- <span data-ttu-id="7c51e-117">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="7c51e-117">User.Read.All</span></span>
- <span data-ttu-id="7c51e-118">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7c51e-118">User.ReadWrite.All</span></span>
- <span data-ttu-id="7c51e-119">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="7c51e-119">Directory.Read.All</span></span>
- <span data-ttu-id="7c51e-120">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7c51e-120">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="7c51e-121">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7c51e-121">Directory.AccessAsUser.All</span></span>

## <a name="common-properties"></a><span data-ttu-id="7c51e-122">Propiedades comunes</span><span class="sxs-lookup"><span data-stu-id="7c51e-122">Common properties</span></span>

| <span data-ttu-id="7c51e-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7c51e-123">Property</span></span> | <span data-ttu-id="7c51e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c51e-124">Description</span></span> |
|----------|-------------|
| <span data-ttu-id="7c51e-125">displayName</span><span class="sxs-lookup"><span data-stu-id="7c51e-125">displayName</span></span> | <span data-ttu-id="7c51e-126">El nombre del usuario que aparece en la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="7c51e-126">The name displayed in the address book for the user.</span></span>|
|<span data-ttu-id="7c51e-127">givenName</span><span class="sxs-lookup"><span data-stu-id="7c51e-127">givenName</span></span>| <span data-ttu-id="7c51e-128">El nombre de pila del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c51e-128">The first name of the user.</span></span> |
|<span data-ttu-id="7c51e-129">surname</span><span class="sxs-lookup"><span data-stu-id="7c51e-129">surname</span></span>| <span data-ttu-id="7c51e-130">El apellido del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c51e-130">The last name of the user.</span></span> |
|<span data-ttu-id="7c51e-131">mail</span><span class="sxs-lookup"><span data-stu-id="7c51e-131">mail</span></span>| <span data-ttu-id="7c51e-132">La dirección de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c51e-132">The user's email address.</span></span> |
|<span data-ttu-id="7c51e-133">photo</span><span class="sxs-lookup"><span data-stu-id="7c51e-133">photo</span></span>| <span data-ttu-id="7c51e-134">Fotografías del perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c51e-134">The user's profile photo.</span></span> |

<span data-ttu-id="7c51e-135">Para obtener información detallada y una lista de todas las propiedades, consulte el objeto [user](user.md).</span><span class="sxs-lookup"><span data-stu-id="7c51e-135">For details and a list of all the properties, see the [user](user.md) object.</span></span>

## <a name="common-operations"></a><span data-ttu-id="7c51e-136">Operaciones comunes</span><span class="sxs-lookup"><span data-stu-id="7c51e-136">Common operations</span></span>
><span data-ttu-id="7c51e-137">**Nota:** Algunas de estas operaciones requieren permisos adicionales.</span><span class="sxs-lookup"><span data-stu-id="7c51e-137">**Note:** Some of these operations require additional permissions.</span></span>

| <span data-ttu-id="7c51e-138">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="7c51e-138">Path</span></span>    | <span data-ttu-id="7c51e-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c51e-139">Description</span></span> |
|---------|-------------|
|[`/users`](../api/user-list.md) | <span data-ttu-id="7c51e-140">Enumera los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="7c51e-140">Lists users in the organization.</span></span> |
|[`/users/{id}`](../api/user-get.md) | <span data-ttu-id="7c51e-141">Obtiene un usuario específico por su identificador.</span><span class="sxs-lookup"><span data-stu-id="7c51e-141">Gets a specific user by id.</span></span> |
|[`/users/{id}/photo/$value`](../api/profilephoto-get.md)| <span data-ttu-id="7c51e-142">Obtiene la foto de perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c51e-142">Gets the user's profile photo.</span></span> |
|[`/users/{id}/manager`](../api/user-list-manager.md) | <span data-ttu-id="7c51e-143">Obtiene el administrador del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c51e-143">Gets the user's manager.</span></span> |
|[`/users/{id}/messages`](../api/user-list-messages.md)| <span data-ttu-id="7c51e-144">Enumera los mensajes de correo electrónico del usuario en su bandeja de entrada principal.</span><span class="sxs-lookup"><span data-stu-id="7c51e-144">Lists the user's email messages in their primary inbox.</span></span> |
|[`/users/{id}/events`](../api/user-list-events.md) | <span data-ttu-id="7c51e-145">Enumera los eventos próximos del usuario en su calendario.</span><span class="sxs-lookup"><span data-stu-id="7c51e-145">Lists the user's upcoming events in their calendar.</span></span> |
|[`/users/{id}/drive`](../api/drive-get.md)| <span data-ttu-id="7c51e-146">Obtiene el almacén de archivos del OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c51e-146">Gets the user's OneDrive file store.</span></span> |
|[`/users/{id}/memberOf`](../api/user-list-memberof.md)| <span data-ttu-id="7c51e-147">Enumera los grupos de los que el usuario es miembro.</span><span class="sxs-lookup"><span data-stu-id="7c51e-147">Lists the groups that the user is a member of.</span></span> |
|[`/users/{id}/joinedTeams`](../api/user-list-joinedteams.md)| <span data-ttu-id="7c51e-148">Se enumeran los Teams Microsoft que el usuario es un miembro de.</span><span class="sxs-lookup"><span data-stu-id="7c51e-148">Lists the Microsoft Teams that the user is a member of.</span></span> |
