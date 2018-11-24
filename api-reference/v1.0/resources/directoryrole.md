# <a name="directoryrole-resource-type"></a><span data-ttu-id="ed39f-101">Tipo de recurso directoryRole</span><span class="sxs-lookup"><span data-stu-id="ed39f-101">directoryRole resource type</span></span>

<span data-ttu-id="ed39f-102">Representa un rol de Active directory de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ed39f-102">Represents an Azure AD directory role.</span></span> <span data-ttu-id="ed39f-103">Las funciones de Active directory AD Azure también conocido como son *roles de administrador*.</span><span class="sxs-lookup"><span data-stu-id="ed39f-103">Azure AD directory roles are also known as *administrator roles*.</span></span> <span data-ttu-id="ed39f-104">Para obtener más información acerca de las funciones de Active directory (Administrador), vea [asignación de roles de administrador en Azure AD](http://azure.microsoft.com/documentation/articles/active-directory-assign-admin-roles/).</span><span class="sxs-lookup"><span data-stu-id="ed39f-104">For more information about directory (administrator) roles, see [Assigning administrator roles in Azure AD](http://azure.microsoft.com/documentation/articles/active-directory-assign-admin-roles/).</span></span> <span data-ttu-id="ed39f-105">Con Microsoft Graph, puede asignar a usuarios a roles de Active directory para concederles los permisos de la función de destino.</span><span class="sxs-lookup"><span data-stu-id="ed39f-105">With the Microsoft Graph, you can assign users to directory roles to grant them the permissions of the target role.</span></span> <span data-ttu-id="ed39f-106">Para leer un rol de Active directory o actualizar a sus miembros, debe activarse en primer lugar en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="ed39f-106">To read a directory role or update its members, it must first be activated in the tenant.</span></span> <span data-ttu-id="ed39f-107">Sólo el rol de Active directory de administradores de la compañía se activa de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ed39f-107">Only the Company Administrators directory role is activated by default.</span></span> <span data-ttu-id="ed39f-108">Para activar otros roles de Active directory disponibles que enviar una solicitud POST con el identificador de la [directoryRoleTemplate](directoryroletemplate.md) en el que se basa el rol de Active directory.</span><span class="sxs-lookup"><span data-stu-id="ed39f-108">To activate other available directory roles you send a POST request with the ID of the [directoryRoleTemplate](directoryroletemplate.md) on which the directory role is based.</span></span> <span data-ttu-id="ed39f-109">Se hereda de [directoryObject](directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="ed39f-109">Inherits from [directoryObject](directoryobject.md).</span></span>
<span data-ttu-id="ed39f-110">Este recurso admite:</span><span class="sxs-lookup"><span data-stu-id="ed39f-110">This resource supports:</span></span>

- <span data-ttu-id="ed39f-111">que use una [consulta delta](../../../concepts/delta_query_overview.md) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/directoryrole_delta.md).</span><span class="sxs-lookup"><span data-stu-id="ed39f-111">Using [delta query](../../../concepts/delta_query_overview.md) to track incremental additions, deletions, and updates, by providing a [delta](../api/directoryrole_delta.md) function.</span></span>

## <a name="methods"></a><span data-ttu-id="ed39f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ed39f-112">Methods</span></span>

| <span data-ttu-id="ed39f-113">Método</span><span class="sxs-lookup"><span data-stu-id="ed39f-113">Method</span></span>       | <span data-ttu-id="ed39f-114">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed39f-114">Return Type</span></span>  |<span data-ttu-id="ed39f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed39f-115">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ed39f-116">Obtener directoryRole</span><span class="sxs-lookup"><span data-stu-id="ed39f-116">Get directoryRole</span></span>](../api/directoryrole_get.md) | [<span data-ttu-id="ed39f-117">directoryRole</span><span class="sxs-lookup"><span data-stu-id="ed39f-117">directoryRole</span></span>](directoryrole.md) | <span data-ttu-id="ed39f-118">Lea las propiedades y las relaciones del objeto directoryRole.</span><span class="sxs-lookup"><span data-stu-id="ed39f-118">Read properties and relationships of directoryRole object.</span></span> |
|[<span data-ttu-id="ed39f-119">List directoryRoles</span><span class="sxs-lookup"><span data-stu-id="ed39f-119">List directoryRoles</span></span>](../api/directoryrole_list.md) | <span data-ttu-id="ed39f-120">Colección [directoryRole](directoryrole.md)</span><span class="sxs-lookup"><span data-stu-id="ed39f-120">[directoryRole](directoryrole.md) collection</span></span> | <span data-ttu-id="ed39f-121">Enumera los roles de directorio que están activados en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="ed39f-121">List the directory roles that are activated in the tenant.</span></span> |
|[<span data-ttu-id="ed39f-122">Agregar miembro</span><span class="sxs-lookup"><span data-stu-id="ed39f-122">Add member</span></span>](../api/directoryrole_post_members.md) |[<span data-ttu-id="ed39f-123">directoryObject</span><span class="sxs-lookup"><span data-stu-id="ed39f-123">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="ed39f-124">Agregue un usuario al rol de directorio; para ello, publique en la propiedad de navegación de miembros.</span><span class="sxs-lookup"><span data-stu-id="ed39f-124">Add a user to the directory role by posting to the members navigation property.</span></span>|
|[<span data-ttu-id="ed39f-125">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="ed39f-125">List members</span></span>](../api/directoryrole_list_members.md) |<span data-ttu-id="ed39f-126">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="ed39f-126">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="ed39f-127">Obtenga los usuarios que son miembros del rol de directorio de la propiedad de navegación de miembros.</span><span class="sxs-lookup"><span data-stu-id="ed39f-127">Get the users that are members of the directory role from the members navigation property.</span></span>|
|[<span data-ttu-id="ed39f-128">Quitar un miembro</span><span class="sxs-lookup"><span data-stu-id="ed39f-128">Remove a member</span></span>](../api/directoryrole_delete_member.md) |[<span data-ttu-id="ed39f-129">directoryObject</span><span class="sxs-lookup"><span data-stu-id="ed39f-129">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="ed39f-130">Elimine un usuario del rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="ed39f-130">Remove a user from the directory role.</span></span>|
|[<span data-ttu-id="ed39f-131">Activar directoryRole</span><span class="sxs-lookup"><span data-stu-id="ed39f-131">Activate directoryRole</span></span>](../api/directoryrole_post_directoryroles.md) |[<span data-ttu-id="ed39f-132">directoryRole</span><span class="sxs-lookup"><span data-stu-id="ed39f-132">directoryRole</span></span>](directoryrole.md) | <span data-ttu-id="ed39f-133">Activa un rol del directorio.</span><span class="sxs-lookup"><span data-stu-id="ed39f-133">Activate a directory role.</span></span>|
|[<span data-ttu-id="ed39f-134">delta</span><span class="sxs-lookup"><span data-stu-id="ed39f-134">delta</span></span>](../api/directoryrole_delta.md)|<span data-ttu-id="ed39f-135">Colección directoryRole</span><span class="sxs-lookup"><span data-stu-id="ed39f-135">directoryRole collection</span></span>| <span data-ttu-id="ed39f-136">Obtener cambios incrementales para funciones de Active directory.</span><span class="sxs-lookup"><span data-stu-id="ed39f-136">Get incremental changes for directory roles.</span></span> |

## <a name="properties"></a><span data-ttu-id="ed39f-137">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed39f-137">Properties</span></span>
| <span data-ttu-id="ed39f-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ed39f-138">Property</span></span>   | <span data-ttu-id="ed39f-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed39f-139">Type</span></span> | <span data-ttu-id="ed39f-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed39f-140">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="ed39f-141">description</span><span class="sxs-lookup"><span data-stu-id="ed39f-141">description</span></span>|<span data-ttu-id="ed39f-142">String</span><span class="sxs-lookup"><span data-stu-id="ed39f-142">String</span></span>|<span data-ttu-id="ed39f-p102">La descripción del rol de directorio. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ed39f-p102">The description for the directory role. Read-only.</span></span> |
|<span data-ttu-id="ed39f-145">displayName</span><span class="sxs-lookup"><span data-stu-id="ed39f-145">displayName</span></span>|<span data-ttu-id="ed39f-146">String</span><span class="sxs-lookup"><span data-stu-id="ed39f-146">String</span></span>|<span data-ttu-id="ed39f-p103">El nombre para mostrar del rol de directorio. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ed39f-p103">The display name for the directory role. Read-only.</span></span> |
|<span data-ttu-id="ed39f-149">id</span><span class="sxs-lookup"><span data-stu-id="ed39f-149">id</span></span>|<span data-ttu-id="ed39f-150">String</span><span class="sxs-lookup"><span data-stu-id="ed39f-150">String</span></span>|<span data-ttu-id="ed39f-p104">El identificador único del rol de directorio. Hereda de [directoryObject](directoryobject.md). Clave, no admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ed39f-p104">The unique identifier for the directory role. Inherited from [directoryObject](directoryobject.md). Key, Not nullable, Read-only.</span></span>|
|<span data-ttu-id="ed39f-154">roleTemplateId</span><span class="sxs-lookup"><span data-stu-id="ed39f-154">roleTemplateId</span></span>|<span data-ttu-id="ed39f-155">String</span><span class="sxs-lookup"><span data-stu-id="ed39f-155">String</span></span>| <span data-ttu-id="ed39f-p105">El **id** de la [directoryRoleTemplate](directoryroletemplate.md) en que se basa este rol. La propiedad debe especificarse al activar un rol de directorio en un inquilino con una operación POST. Una vez activado el rol de directorio, la propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ed39f-p105">The **id** of the [directoryRoleTemplate](directoryroletemplate.md) that this role is based on. The property must be specified when activating a directory role in a tenant with a POST operation. After the directory role has been activated, the property is read only.</span></span> |

## <a name="relationships"></a><span data-ttu-id="ed39f-159">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ed39f-159">Relationships</span></span>
| <span data-ttu-id="ed39f-160">Relación</span><span class="sxs-lookup"><span data-stu-id="ed39f-160">Relationship</span></span> | <span data-ttu-id="ed39f-161">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed39f-161">Type</span></span> |<span data-ttu-id="ed39f-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed39f-162">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ed39f-163">members</span><span class="sxs-lookup"><span data-stu-id="ed39f-163">members</span></span>|<span data-ttu-id="ed39f-164">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="ed39f-164">[directoryObject](directoryobject.md) collection</span></span>|<span data-ttu-id="ed39f-p106">Usuarios que son miembros de este rol de directorio. Métodos HTTP: GET, POST, DELETE. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="ed39f-p106">Users that are members of this directory role. HTTP Methods: GET, POST, DELETE. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ed39f-169">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ed39f-169">JSON representation</span></span>

<span data-ttu-id="ed39f-170">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ed39f-170">Here is a JSON representation of the resource</span></span>

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
