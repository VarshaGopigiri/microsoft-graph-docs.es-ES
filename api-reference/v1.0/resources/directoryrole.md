---
title: Tipo de recurso directoryRole
description: Representa un rol de Active directory de Azure AD. Las funciones de Active directory AD Azure también conocido como son *roles de administrador*. Para obtener más información acerca de las funciones de Active directory (Administrador), vea la asignación de roles de administrador en Azure AD. Con Microsoft Graph, puede asignar a usuarios a roles de Active directory para concederles los permisos de la función de destino. Para leer un rol de Active directory o actualizar a sus miembros, debe activarse en primer lugar en el inquilino. Sólo el rol de Active directory de administradores de la compañía se activa de forma predeterminada. Para activar otros roles de Active directory disponibles que enviar una solicitud POST con el identificador de la directoryRoleTemplate en el que se basa el rol de Active directory. Se hereda de directoryObject.
localization_priority: Priority
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 4b3379bbbecd86612043dcc3cb8455f5c43ba9cf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939549"
---
# <a name="directoryrole-resource-type"></a><span data-ttu-id="73a35-110">Tipo de recurso directoryRole</span><span class="sxs-lookup"><span data-stu-id="73a35-110">directoryRole resource type</span></span>

<span data-ttu-id="73a35-111">Representa un rol de Active directory de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="73a35-111">Represents an Azure AD directory role.</span></span> <span data-ttu-id="73a35-112">Las funciones de Active directory AD Azure también conocido como son *roles de administrador*.</span><span class="sxs-lookup"><span data-stu-id="73a35-112">Azure AD directory roles are also known as *administrator roles*.</span></span> <span data-ttu-id="73a35-113">Para obtener más información acerca de las funciones de Active directory (Administrador), vea [asignación de roles de administrador en Azure AD](http://azure.microsoft.com/documentation/articles/active-directory-assign-admin-roles/).</span><span class="sxs-lookup"><span data-stu-id="73a35-113">For more information about directory (administrator) roles, see [Assigning administrator roles in Azure AD](http://azure.microsoft.com/documentation/articles/active-directory-assign-admin-roles/).</span></span> <span data-ttu-id="73a35-114">Con Microsoft Graph, puede asignar a usuarios a roles de Active directory para concederles los permisos de la función de destino.</span><span class="sxs-lookup"><span data-stu-id="73a35-114">With the Microsoft Graph, you can assign users to directory roles to grant them the permissions of the target role.</span></span> <span data-ttu-id="73a35-115">Para leer un rol de Active directory o actualizar a sus miembros, debe activarse en primer lugar en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="73a35-115">To read a directory role or update its members, it must first be activated in the tenant.</span></span> <span data-ttu-id="73a35-116">Sólo el rol de Active directory de administradores de la compañía se activa de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="73a35-116">Only the Company Administrators directory role is activated by default.</span></span> <span data-ttu-id="73a35-117">Para activar otros roles de Active directory disponibles que enviar una solicitud POST con el identificador de la [directoryRoleTemplate](directoryroletemplate.md) en el que se basa el rol de Active directory.</span><span class="sxs-lookup"><span data-stu-id="73a35-117">To activate other available directory roles you send a POST request with the ID of the [directoryRoleTemplate](directoryroletemplate.md) on which the directory role is based.</span></span> <span data-ttu-id="73a35-118">Se hereda de [directoryObject](directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="73a35-118">Inherits from [directoryObject](directoryobject.md).</span></span>
<span data-ttu-id="73a35-119">Este recurso admite:</span><span class="sxs-lookup"><span data-stu-id="73a35-119">This resource supports:</span></span>

- <span data-ttu-id="73a35-120">que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/directoryrole-delta.md).</span><span class="sxs-lookup"><span data-stu-id="73a35-120">Using [delta query](/graph/delta-query-overview) to track incremental additions, deletions, and updates, by providing a [delta](../api/directoryrole-delta.md) function.</span></span>

## <a name="methods"></a><span data-ttu-id="73a35-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="73a35-121">Methods</span></span>

| <span data-ttu-id="73a35-122">Método</span><span class="sxs-lookup"><span data-stu-id="73a35-122">Method</span></span>       | <span data-ttu-id="73a35-123">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73a35-123">Return Type</span></span>  |<span data-ttu-id="73a35-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="73a35-124">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="73a35-125">Obtener directoryRole</span><span class="sxs-lookup"><span data-stu-id="73a35-125">Get directoryRole</span></span>](../api/directoryrole-get.md) | [<span data-ttu-id="73a35-126">directoryRole</span><span class="sxs-lookup"><span data-stu-id="73a35-126">directoryRole</span></span>](directoryrole.md) | <span data-ttu-id="73a35-127">Lea las propiedades y las relaciones del objeto directoryRole.</span><span class="sxs-lookup"><span data-stu-id="73a35-127">Read properties and relationships of directoryRole object.</span></span> |
|[<span data-ttu-id="73a35-128">List directoryRoles</span><span class="sxs-lookup"><span data-stu-id="73a35-128">List directoryRoles</span></span>](../api/directoryrole-list.md) | <span data-ttu-id="73a35-129">Colección [directoryRole](directoryrole.md)</span><span class="sxs-lookup"><span data-stu-id="73a35-129">[directoryRole](directoryrole.md) collection</span></span> | <span data-ttu-id="73a35-130">Enumera los roles de directorio que están activados en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="73a35-130">List the directory roles that are activated in the tenant.</span></span> |
|[<span data-ttu-id="73a35-131">Agregar miembro</span><span class="sxs-lookup"><span data-stu-id="73a35-131">Add member</span></span>](../api/directoryrole-post-members.md) |[<span data-ttu-id="73a35-132">directoryObject</span><span class="sxs-lookup"><span data-stu-id="73a35-132">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="73a35-133">Agregue un usuario al rol de directorio; para ello, publique en la propiedad de navegación de miembros.</span><span class="sxs-lookup"><span data-stu-id="73a35-133">Add a user to the directory role by posting to the members navigation property.</span></span>|
|[<span data-ttu-id="73a35-134">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="73a35-134">List members</span></span>](../api/directoryrole-list-members.md) |<span data-ttu-id="73a35-135">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="73a35-135">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="73a35-136">Obtenga los usuarios que son miembros del rol de directorio de la propiedad de navegación de miembros.</span><span class="sxs-lookup"><span data-stu-id="73a35-136">Get the users that are members of the directory role from the members navigation property.</span></span>|
|[<span data-ttu-id="73a35-137">Quitar un miembro</span><span class="sxs-lookup"><span data-stu-id="73a35-137">Remove a member</span></span>](../api/directoryrole-delete-member.md) |[<span data-ttu-id="73a35-138">directoryObject</span><span class="sxs-lookup"><span data-stu-id="73a35-138">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="73a35-139">Elimine un usuario del rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="73a35-139">Remove a user from the directory role.</span></span>|
|[<span data-ttu-id="73a35-140">Activar directoryRole</span><span class="sxs-lookup"><span data-stu-id="73a35-140">Activate directoryRole</span></span>](../api/directoryrole-post-directoryroles.md) |[<span data-ttu-id="73a35-141">directoryRole</span><span class="sxs-lookup"><span data-stu-id="73a35-141">directoryRole</span></span>](directoryrole.md) | <span data-ttu-id="73a35-142">Activa un rol del directorio.</span><span class="sxs-lookup"><span data-stu-id="73a35-142">Activate a directory role.</span></span>|
|[<span data-ttu-id="73a35-143">delta</span><span class="sxs-lookup"><span data-stu-id="73a35-143">delta</span></span>](../api/directoryrole-delta.md)|<span data-ttu-id="73a35-144">Colección directoryRole</span><span class="sxs-lookup"><span data-stu-id="73a35-144">directoryRole collection</span></span>| <span data-ttu-id="73a35-145">Obtener cambios incrementales para funciones de Active directory.</span><span class="sxs-lookup"><span data-stu-id="73a35-145">Get incremental changes for directory roles.</span></span> |

## <a name="properties"></a><span data-ttu-id="73a35-146">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73a35-146">Properties</span></span>
| <span data-ttu-id="73a35-147">Propiedad</span><span class="sxs-lookup"><span data-stu-id="73a35-147">Property</span></span>   | <span data-ttu-id="73a35-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="73a35-148">Type</span></span> | <span data-ttu-id="73a35-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="73a35-149">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="73a35-150">description</span><span class="sxs-lookup"><span data-stu-id="73a35-150">description</span></span>|<span data-ttu-id="73a35-151">String</span><span class="sxs-lookup"><span data-stu-id="73a35-151">String</span></span>|<span data-ttu-id="73a35-p103">La descripción del rol de directorio. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="73a35-p103">The description for the directory role. Read-only.</span></span> |
|<span data-ttu-id="73a35-154">displayName</span><span class="sxs-lookup"><span data-stu-id="73a35-154">displayName</span></span>|<span data-ttu-id="73a35-155">String</span><span class="sxs-lookup"><span data-stu-id="73a35-155">String</span></span>|<span data-ttu-id="73a35-p104">El nombre para mostrar del rol de directorio. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="73a35-p104">The display name for the directory role. Read-only.</span></span> |
|<span data-ttu-id="73a35-158">id</span><span class="sxs-lookup"><span data-stu-id="73a35-158">id</span></span>|<span data-ttu-id="73a35-159">String</span><span class="sxs-lookup"><span data-stu-id="73a35-159">String</span></span>|<span data-ttu-id="73a35-p105">El identificador único del rol de directorio. Hereda de [directoryObject](directoryobject.md). Clave, no admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="73a35-p105">The unique identifier for the directory role. Inherited from [directoryObject](directoryobject.md). Key, Not nullable, Read-only.</span></span>|
|<span data-ttu-id="73a35-163">roleTemplateId</span><span class="sxs-lookup"><span data-stu-id="73a35-163">roleTemplateId</span></span>|<span data-ttu-id="73a35-164">String</span><span class="sxs-lookup"><span data-stu-id="73a35-164">String</span></span>| <span data-ttu-id="73a35-p106">El **id** de la [directoryRoleTemplate](directoryroletemplate.md) en que se basa este rol. La propiedad debe especificarse al activar un rol de directorio en un inquilino con una operación POST. Una vez activado el rol de directorio, la propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="73a35-p106">The **id** of the [directoryRoleTemplate](directoryroletemplate.md) that this role is based on. The property must be specified when activating a directory role in a tenant with a POST operation. After the directory role has been activated, the property is read only.</span></span> |

## <a name="relationships"></a><span data-ttu-id="73a35-168">Relaciones</span><span class="sxs-lookup"><span data-stu-id="73a35-168">Relationships</span></span>
| <span data-ttu-id="73a35-169">Relación</span><span class="sxs-lookup"><span data-stu-id="73a35-169">Relationship</span></span> | <span data-ttu-id="73a35-170">Tipo</span><span class="sxs-lookup"><span data-stu-id="73a35-170">Type</span></span> |<span data-ttu-id="73a35-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="73a35-171">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="73a35-172">members</span><span class="sxs-lookup"><span data-stu-id="73a35-172">members</span></span>|<span data-ttu-id="73a35-173">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="73a35-173">[directoryObject](directoryobject.md) collection</span></span>|<span data-ttu-id="73a35-p107">Usuarios que son miembros de este rol de directorio. Métodos HTTP: GET, POST, DELETE. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="73a35-p107">Users that are members of this directory role. HTTP Methods: GET, POST, DELETE. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="73a35-178">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="73a35-178">JSON representation</span></span>

<span data-ttu-id="73a35-179">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="73a35-179">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [
    "memberOf",
    "members",
    "ownedObjects",
    "owners"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.directoryObject",
  "@odata.type": "microsoft.graph.directoryRole",
  "@odata.annotations": [
    {
      "capabilities": {
        "toppable": false
      }
    }
  ]
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
