---
title: Tipo de recurso directoryRole
description: Representa un rol de Active directory de Azure AD. Las funciones de Active directory AD Azure también conocido como son *roles de administrador*. Para obtener más información acerca de las funciones de Active directory (Administrador), vea la asignación de roles de administrador en Azure AD. Con Microsoft Graph, puede asignar a usuarios a roles de Active directory para concederles los permisos de la función de destino. Para leer un rol de Active directory o actualizar a sus miembros, debe activarse en primer lugar en el inquilino. Sólo el rol de Active directory de administradores de la compañía se activa de forma predeterminada. Para activar otros roles de directorio disponible, envíe una solicitud POST con el identificador de la directoryRoleTemplate en el que se basa el rol de Active directory. Se hereda de directoryObject.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: e6753369be070ab04419cab0c870aec7e96b1fb2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27927747"
---
# <a name="directoryrole-resource-type"></a><span data-ttu-id="26129-110">Tipo de recurso directoryRole</span><span class="sxs-lookup"><span data-stu-id="26129-110">directoryRole resource type</span></span>

> <span data-ttu-id="26129-111">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="26129-111">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="26129-112">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="26129-112">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="26129-113">Representa un rol de Active directory de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="26129-113">Represents an Azure AD directory role.</span></span> <span data-ttu-id="26129-114">Las funciones de Active directory AD Azure también conocido como son *roles de administrador*.</span><span class="sxs-lookup"><span data-stu-id="26129-114">Azure AD directory roles are also known as *administrator roles*.</span></span> <span data-ttu-id="26129-115">Para obtener más información acerca de las funciones de Active directory (Administrador), vea [asignación de roles de administrador en Azure AD](https://azure.microsoft.com/documentation/articles/active-directory-assign-admin-roles/).</span><span class="sxs-lookup"><span data-stu-id="26129-115">For more information about directory (administrator) roles, see [Assigning administrator roles in Azure AD](https://azure.microsoft.com/documentation/articles/active-directory-assign-admin-roles/).</span></span> <span data-ttu-id="26129-116">Con Microsoft Graph, puede asignar a usuarios a roles de Active directory para concederles los permisos de la función de destino.</span><span class="sxs-lookup"><span data-stu-id="26129-116">With the Microsoft Graph, you can assign users to directory roles to grant them the permissions of the target role.</span></span> <span data-ttu-id="26129-117">Para leer un rol de Active directory o actualizar a sus miembros, debe activarse en primer lugar en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="26129-117">To read a directory role or update its members, it must first be activated in the tenant.</span></span> <span data-ttu-id="26129-118">Sólo el rol de Active directory de administradores de la compañía se activa de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="26129-118">Only the Company Administrators directory role is activated by default.</span></span> <span data-ttu-id="26129-119">Para activar otros roles de directorio disponible, envíe una solicitud POST con el identificador de la [directoryRoleTemplate](directoryroletemplate.md) en el que se basa el rol de Active directory.</span><span class="sxs-lookup"><span data-stu-id="26129-119">To activate other available directory roles, you send a POST request with the ID of the [directoryRoleTemplate](directoryroletemplate.md) on which the directory role is based.</span></span> <span data-ttu-id="26129-120">Se hereda de [directoryObject](directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="26129-120">Inherits from [directoryObject](directoryobject.md).</span></span>

<span data-ttu-id="26129-121">De forma predeterminada, las funciones de Active directory tengan un ámbito para que todo el inquilino.</span><span class="sxs-lookup"><span data-stu-id="26129-121">By default, directory roles are scoped to be tenant-wide.</span></span>  <span data-ttu-id="26129-122">Sin embargo, las funciones de Active directory (actualmente sólo el *Administrador de la cuenta de usuario* y *Administrador de departamento de soporte técnico*) también pueden aplicarse a [unidades administrativas](administrativeunit.md).</span><span class="sxs-lookup"><span data-stu-id="26129-122">However, directory roles (currently only the *user account admin* and *helpdesk admin*) may also be scoped to [administrative units](administrativeunit.md).</span></span>

<span data-ttu-id="26129-123">Este recurso admite:</span><span class="sxs-lookup"><span data-stu-id="26129-123">This resource supports:</span></span>

- <span data-ttu-id="26129-124">que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/directoryrole-delta.md).</span><span class="sxs-lookup"><span data-stu-id="26129-124">Using [delta query](/graph/delta-query-overview) to track incremental additions, deletions, and updates, by providing a [delta](../api/directoryrole-delta.md) function.</span></span>

## <a name="methods"></a><span data-ttu-id="26129-125">Métodos</span><span class="sxs-lookup"><span data-stu-id="26129-125">Methods</span></span>

| <span data-ttu-id="26129-126">Método</span><span class="sxs-lookup"><span data-stu-id="26129-126">Method</span></span>       | <span data-ttu-id="26129-127">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26129-127">Return Type</span></span>  |<span data-ttu-id="26129-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="26129-128">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="26129-129">Obtener directoryRole</span><span class="sxs-lookup"><span data-stu-id="26129-129">Get directoryRole</span></span>](../api/directoryrole-get.md) | [<span data-ttu-id="26129-130">directoryRole</span><span class="sxs-lookup"><span data-stu-id="26129-130">directoryRole</span></span>](directoryrole.md) |<span data-ttu-id="26129-131">Lea las propiedades y las relaciones del objeto directoryRole.</span><span class="sxs-lookup"><span data-stu-id="26129-131">Read properties and relationships of directoryRole object.</span></span>|
|[<span data-ttu-id="26129-132">List directoryRoles</span><span class="sxs-lookup"><span data-stu-id="26129-132">List directoryRoles</span></span>](../api/directoryrole-list.md) | <span data-ttu-id="26129-133">Colección [directoryRole](directoryrole.md)</span><span class="sxs-lookup"><span data-stu-id="26129-133">[directoryRole](directoryrole.md) collection</span></span> | <span data-ttu-id="26129-134">Enumera los roles de directorio que están activados en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="26129-134">List the directory roles that are activated in the tenant.</span></span> |
|[<span data-ttu-id="26129-135">Agregar miembro</span><span class="sxs-lookup"><span data-stu-id="26129-135">Add member</span></span>](../api/directoryrole-post-members.md) |[<span data-ttu-id="26129-136">directoryObject</span><span class="sxs-lookup"><span data-stu-id="26129-136">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="26129-137">Agregue un usuario al rol de directorio; para ello, publique en la propiedad de navegación de miembros.</span><span class="sxs-lookup"><span data-stu-id="26129-137">Add a user to the directory role by posting to the members navigation property.</span></span>|
|[<span data-ttu-id="26129-138">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="26129-138">List members</span></span>](../api/directoryrole-list-members.md) |<span data-ttu-id="26129-139">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="26129-139">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="26129-140">Obtenga los usuarios que son miembros del rol de directorio de la propiedad de navegación de miembros.</span><span class="sxs-lookup"><span data-stu-id="26129-140">Get the users that are members of the directory role from the members navigation property.</span></span>|
|[<span data-ttu-id="26129-141">Quitar un miembro</span><span class="sxs-lookup"><span data-stu-id="26129-141">Remove a member</span></span>](../api/directoryrole-delete-member.md) |[<span data-ttu-id="26129-142">directoryObject</span><span class="sxs-lookup"><span data-stu-id="26129-142">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="26129-143">Elimine un usuario del rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="26129-143">Remove a user from the directory role.</span></span>|
|[<span data-ttu-id="26129-144">Miembros de la función con ámbito de lista</span><span class="sxs-lookup"><span data-stu-id="26129-144">List scoped-role members</span></span>](../api/directoryrole-list-members.md) |<span data-ttu-id="26129-145">colección de [scopedRoleMembership](scopedrolemembership.md)</span><span class="sxs-lookup"><span data-stu-id="26129-145">[scopedRoleMembership](scopedrolemembership.md) collection</span></span>| <span data-ttu-id="26129-146">Lista de los miembros de este rol de Active directory que pertenecen al ámbito de [unidades administrativas](administrativeunit.md)a través de la colección de recursos de scopedRoleMembership.</span><span class="sxs-lookup"><span data-stu-id="26129-146">List the members of this directory role that are scoped to [administrative units](administrativeunit.md), through the scopedRoleMembership resource collection.</span></span>|
|[<span data-ttu-id="26129-147">delta</span><span class="sxs-lookup"><span data-stu-id="26129-147">delta</span></span>](../api/directoryrole-delta.md)|<span data-ttu-id="26129-148">Colección directoryRole</span><span class="sxs-lookup"><span data-stu-id="26129-148">directoryRole collection</span></span>| <span data-ttu-id="26129-149">Obtener cambios incrementales para funciones de Active directory.</span><span class="sxs-lookup"><span data-stu-id="26129-149">Get incremental changes for directory roles.</span></span> |

## <a name="properties"></a><span data-ttu-id="26129-150">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26129-150">Properties</span></span>
| <span data-ttu-id="26129-151">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26129-151">Property</span></span>   | <span data-ttu-id="26129-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="26129-152">Type</span></span> |<span data-ttu-id="26129-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="26129-153">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="26129-154">description</span><span class="sxs-lookup"><span data-stu-id="26129-154">description</span></span>|<span data-ttu-id="26129-155">String</span><span class="sxs-lookup"><span data-stu-id="26129-155">String</span></span>|<span data-ttu-id="26129-p105">La descripción del rol de directorio. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="26129-p105">The description for the directory role. Read-only.</span></span> |
|<span data-ttu-id="26129-158">displayName</span><span class="sxs-lookup"><span data-stu-id="26129-158">displayName</span></span>|<span data-ttu-id="26129-159">String</span><span class="sxs-lookup"><span data-stu-id="26129-159">String</span></span>|<span data-ttu-id="26129-p106">El nombre para mostrar del rol de directorio. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="26129-p106">The display name for the directory role. Read-only.</span></span> |
|<span data-ttu-id="26129-162">id</span><span class="sxs-lookup"><span data-stu-id="26129-162">id</span></span>|<span data-ttu-id="26129-163">String</span><span class="sxs-lookup"><span data-stu-id="26129-163">String</span></span>|<span data-ttu-id="26129-p107">El identificador único del rol de directorio. Hereda de [directoryObject](directoryobject.md). Clave, no admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="26129-p107">The unique identifier for the directory role. Inherited from [directoryObject](directoryobject.md). Key, Not nullable, Read-only.</span></span>|
|<span data-ttu-id="26129-167">roleTemplateId</span><span class="sxs-lookup"><span data-stu-id="26129-167">roleTemplateId</span></span>|<span data-ttu-id="26129-168">String</span><span class="sxs-lookup"><span data-stu-id="26129-168">String</span></span>| <span data-ttu-id="26129-p108">El **id** de la [directoryRoleTemplate](directoryroletemplate.md) en que se basa este rol. La propiedad debe especificarse al activar un rol de directorio en un inquilino con una operación POST. Una vez activado el rol de directorio, la propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="26129-p108">The **id** of the [directoryRoleTemplate](directoryroletemplate.md) that this role is based on. The property must be specified when activating a directory role in a tenant with a POST operation. After the directory role has been activated, the property is read only.</span></span> |

## <a name="relationships"></a><span data-ttu-id="26129-172">Relaciones</span><span class="sxs-lookup"><span data-stu-id="26129-172">Relationships</span></span>
| <span data-ttu-id="26129-173">Relación</span><span class="sxs-lookup"><span data-stu-id="26129-173">Relationship</span></span> | <span data-ttu-id="26129-174">Tipo</span><span class="sxs-lookup"><span data-stu-id="26129-174">Type</span></span> |<span data-ttu-id="26129-175">Descripción</span><span class="sxs-lookup"><span data-stu-id="26129-175">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="26129-176">members</span><span class="sxs-lookup"><span data-stu-id="26129-176">members</span></span>|<span data-ttu-id="26129-177">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="26129-177">[directoryObject](directoryobject.md) collection</span></span>|<span data-ttu-id="26129-p109">Usuarios que son miembros de este rol de directorio. Métodos HTTP: GET, POST, DELETE. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="26129-p109">Users that are members of this directory role. HTTP Methods: GET, POST, DELETE. Read-only. Nullable.</span></span>|
|<span data-ttu-id="26129-182">scopedMembers</span><span class="sxs-lookup"><span data-stu-id="26129-182">scopedMembers</span></span>|<span data-ttu-id="26129-183">colección de [scopedRoleMembership](scopedrolemembership.md)</span><span class="sxs-lookup"><span data-stu-id="26129-183">[scopedRoleMembership](scopedrolemembership.md) collection</span></span>| <span data-ttu-id="26129-184">Miembros de este rol de Active directory que pertenecen al ámbito de [unidades administrativas](administrativeunit.md).</span><span class="sxs-lookup"><span data-stu-id="26129-184">Members of this directory role that are scoped to [administrative units](administrativeunit.md).</span></span> <span data-ttu-id="26129-185">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="26129-185">Read-only.</span></span> <span data-ttu-id="26129-186">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="26129-186">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="26129-187">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="26129-187">JSON representation</span></span>

<span data-ttu-id="26129-188">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="26129-188">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "memberOf",
    "members",
    "ownedObjects",
    "owners"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.directoryRole"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)",
  "roleTemplateId": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryRole resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
