---
title: Trabajar con usuarios en Microsoft Graph
description: Puede usar Microsoft Graph para crear experiencias de aplicaciones convincentes basadas en usuarios, sus relaciones con otros usuarios y grupos y su correo, calendario y archivos.
ms.openlocfilehash: edbf9eb36f3c4d3276b5ddd594b9514e0d8ae15e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030832"
---
# <a name="working-with-users-in-microsoft-graph"></a><span data-ttu-id="7b467-103">Trabajar con usuarios en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="7b467-103">Working with users in Microsoft Graph</span></span>

<span data-ttu-id="7b467-104">Puede usar Microsoft Graph para crear experiencias de aplicaciones convincentes basadas en usuarios, sus relaciones con otros usuarios y grupos y su correo, calendario y archivos.</span><span class="sxs-lookup"><span data-stu-id="7b467-104">You can use Microsoft Graph to build compelling app experiences based on users, their relationships with other users and groups, and their mail, calendar, and files.</span></span>

<span data-ttu-id="7b467-105">Puede acceder a los [usuarios](user.md) a través de Microsoft Graph de dos formas:</span><span class="sxs-lookup"><span data-stu-id="7b467-105">You can access [users](user.md) through Microsoft Graph in two ways:</span></span>

- <span data-ttu-id="7b467-106">Mediante su identificador, `/users/{id | userPrincipalName}`</span><span class="sxs-lookup"><span data-stu-id="7b467-106">By their ID, `/users/{id | userPrincipalName}`</span></span> 
- <span data-ttu-id="7b467-107">Mediante el alias `/me` del usuario que ha iniciado sesión, que es el mismo que `/users/{signed-in user's id}`</span><span class="sxs-lookup"><span data-stu-id="7b467-107">By using the `/me` alias for the signed-in user, which is the same as `/users/{signed-in user's id}`</span></span>

## <a name="authorization"></a><span data-ttu-id="7b467-108">Authorization</span><span class="sxs-lookup"><span data-stu-id="7b467-108">Authorization</span></span>

<span data-ttu-id="7b467-p101">Se requiere uno de los siguientes [permisos](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) para acceder a las operaciones de usuario. Los tres primeros permisos los puede conceder un usuario a una aplicación. El resto solo los puede conceder el administrador a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="7b467-p101">One of the following [permissions](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) is required to access user operations. The first three permissions can be granted to an app by a user. The rest can only be granted to an app by the administrator.</span></span>

- <span data-ttu-id="7b467-112">User.ReadBasic.All</span><span class="sxs-lookup"><span data-stu-id="7b467-112">User.ReadBasic.All</span></span>
- <span data-ttu-id="7b467-113">User.Read</span><span class="sxs-lookup"><span data-stu-id="7b467-113">User.Read</span></span>
- <span data-ttu-id="7b467-114">User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7b467-114">User.ReadWrite</span></span>
- <span data-ttu-id="7b467-115">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="7b467-115">User.Read.All</span></span>
- <span data-ttu-id="7b467-116">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7b467-116">User.ReadWrite.All</span></span>
- <span data-ttu-id="7b467-117">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="7b467-117">Directory.Read.All</span></span>
- <span data-ttu-id="7b467-118">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7b467-118">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="7b467-119">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7b467-119">Directory.AccessAsUser.All</span></span>

## <a name="common-properties"></a><span data-ttu-id="7b467-120">Propiedades comunes</span><span class="sxs-lookup"><span data-stu-id="7b467-120">Common properties</span></span>

<span data-ttu-id="7b467-121">Las siguientes propiedades representan el conjunto predeterminado de propiedades que se devuelven al obtener un usuario o enumerar usuarios.</span><span class="sxs-lookup"><span data-stu-id="7b467-121">The following represent the default set of properties that are returned when getting a user or listing users.</span></span> <span data-ttu-id="7b467-122">Son un subconjunto de todas las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="7b467-122">These are a subset of all available properties.</span></span> <span data-ttu-id="7b467-123">Para obtener más propiedades de usuario, use el parámetro de consulta `$select`.</span><span class="sxs-lookup"><span data-stu-id="7b467-123">To get more user properties, use the `$select` query parameter.</span></span> 

|<span data-ttu-id="7b467-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7b467-124">Property</span></span> |<span data-ttu-id="7b467-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b467-125">Description</span></span> |
|:----------|:-------------|
|<span data-ttu-id="7b467-126">id</span><span class="sxs-lookup"><span data-stu-id="7b467-126">id</span></span> | <span data-ttu-id="7b467-127">El identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b467-127">The unique identifier for the user.</span></span>|
|<span data-ttu-id="7b467-128">businessPhones</span><span class="sxs-lookup"><span data-stu-id="7b467-128">businessPhones</span></span> | <span data-ttu-id="7b467-129">Los números de teléfono del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b467-129">The user's phone numbers.</span></span>|
|<span data-ttu-id="7b467-130">displayName</span><span class="sxs-lookup"><span data-stu-id="7b467-130">displayName</span></span> | <span data-ttu-id="7b467-131">El nombre del usuario que aparece en la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="7b467-131">The name displayed in the address book for the user.</span></span>|
|<span data-ttu-id="7b467-132">givenName</span><span class="sxs-lookup"><span data-stu-id="7b467-132">givenName</span></span>| <span data-ttu-id="7b467-133">El nombre de pila del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b467-133">The first name of the user.</span></span> |
|<span data-ttu-id="7b467-134">jobTitle</span><span class="sxs-lookup"><span data-stu-id="7b467-134">jobTitle</span></span> | <span data-ttu-id="7b467-135">El puesto del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b467-135">The user's job title.</span></span>|
|<span data-ttu-id="7b467-136">mail</span><span class="sxs-lookup"><span data-stu-id="7b467-136">mail</span></span>| <span data-ttu-id="7b467-137">La dirección de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b467-137">The user's email address.</span></span> |
|<span data-ttu-id="7b467-138">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="7b467-138">mobilePhone</span></span> | <span data-ttu-id="7b467-139">El número de teléfono móvil del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b467-139">The user's cellphone number.</span></span>|
|<span data-ttu-id="7b467-140">officeLocation</span><span class="sxs-lookup"><span data-stu-id="7b467-140">officeLocation</span></span> | <span data-ttu-id="7b467-141">La ubicación de la oficina física del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b467-141">The user's physical office location.</span></span>|
|<span data-ttu-id="7b467-142">preferredLanguage</span><span class="sxs-lookup"><span data-stu-id="7b467-142">preferredLanguage</span></span> | <span data-ttu-id="7b467-143">El idioma de preferencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b467-143">The user's language of preference.</span></span>|
|<span data-ttu-id="7b467-144">surname</span><span class="sxs-lookup"><span data-stu-id="7b467-144">surname</span></span>| <span data-ttu-id="7b467-145">El apellido del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b467-145">The last name of the user.</span></span> |
|<span data-ttu-id="7b467-146">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7b467-146">userPrincipalName</span></span>| <span data-ttu-id="7b467-147">El nombre principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b467-147">The user's principal name.</span></span> |

<br/>

<span data-ttu-id="7b467-148">Para obtener información detallada y una lista de todas las propiedades, consulte el objeto [user](user.md).</span><span class="sxs-lookup"><span data-stu-id="7b467-148">For details and a list of all the properties, see the [user](user.md) object.</span></span>

## <a name="common-operations"></a><span data-ttu-id="7b467-149">Operaciones comunes</span><span class="sxs-lookup"><span data-stu-id="7b467-149">Common operations</span></span>

> <span data-ttu-id="7b467-150">**Nota:** Algunas de estas operaciones requieren permisos adicionales.</span><span class="sxs-lookup"><span data-stu-id="7b467-150">**Note:** Some of these operations require additional permissions.</span></span>

| <span data-ttu-id="7b467-151">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="7b467-151">Path</span></span>    | <span data-ttu-id="7b467-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b467-152">Description</span></span> |
|:---------|:-------------|
|[`/users`](../api/user-list.md) | <span data-ttu-id="7b467-153">Enumera los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="7b467-153">Lists users in the organization.</span></span> |
|[`/users/{id}`](../api/user-get.md) | <span data-ttu-id="7b467-154">Obtiene un usuario específico por su identificador.</span><span class="sxs-lookup"><span data-stu-id="7b467-154">Gets a specific user by id.</span></span> |
|[`/users/{id}/photo/$value`](../api/profilephoto-get.md)| <span data-ttu-id="7b467-155">Obtiene la foto de perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b467-155">Gets the user's profile photo.</span></span> |
|[`/users/{id}/manager`](../api/user-list-manager.md) | <span data-ttu-id="7b467-156">Obtiene el administrador del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b467-156">Gets the user's manager.</span></span> |
|[`/users/{id}/messages`](../api/user-list-messages.md)| <span data-ttu-id="7b467-157">Enumera los mensajes de correo electrónico del usuario en su bandeja de entrada principal.</span><span class="sxs-lookup"><span data-stu-id="7b467-157">Lists the user's email messages in their primary inbox.</span></span> |
|[`/users/{id}/events`](../api/user-list-events.md) | <span data-ttu-id="7b467-158">Enumera los eventos próximos del usuario en su calendario.</span><span class="sxs-lookup"><span data-stu-id="7b467-158">Lists the user's upcoming events in their calendar.</span></span> |
|[`/users/{id}/drive`](../api/drive-get.md)| <span data-ttu-id="7b467-159">Obtiene el almacén de archivos del OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b467-159">Gets the user's OneDrive file store.</span></span> |
|[`/users/{id}/memberOf`](../api/user-list-memberof.md)| <span data-ttu-id="7b467-160">Enumera los grupos de los que el usuario es miembro.</span><span class="sxs-lookup"><span data-stu-id="7b467-160">Lists the groups that the user is a member of.</span></span> |
