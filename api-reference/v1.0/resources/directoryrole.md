# <a name="directoryrole-resource-type"></a><span data-ttu-id="e27e7-101">Tipo de recurso directoryRole</span><span class="sxs-lookup"><span data-stu-id="e27e7-101">directoryRole resource type</span></span>

<span data-ttu-id="e27e7-p101">Representa un rol de directorio de Azure AD. Los roles de directorio de Azure AD también se conocen como *roles de administrador*. Para obtener más información sobre los roles de directorio (administrador), consulte [Asignación de roles de administrador en Azure Active Directory](http://azure.microsoft.com/documentation/articles/active-directory-assign-admin-roles/). Con Microsoft Graph, puede asignar usuarios a roles de directorio para concederles los permisos del rol de destino. Para leer un rol de directorio o actualizar sus miembros, debe activarse primero en el inquilino. Solo se activa de manera predeterminada el rol de directorio Administradores de la compañía. Para activar otros roles de directorio disponibles, envíe una solicitud POST con el identificador de la [directoryRoleTemplate](directoryroletemplate.md) en la que se basa el rol de directorio. Hereda de [directoryObject](directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="e27e7-p101">Represents an Azure AD directory role. Azure AD directory roles are also known as *administrator roles*. For more information about directory (administrator) roles, see [Assigning administrator roles in Azure AD](http://azure.microsoft.com/documentation/articles/active-directory-assign-admin-roles/). With the Microsoft Graph, you can assign users to directory roles to grant them the permissions of the target role. To read a directory role or update its members, it must first be activated in the tenant. Only the Company Administrators directory role is activated by default. To activate other available directory roles you send a POST request with the ID of the [directoryRoleTemplate](directoryroletemplate.md) on which the directory role is based. Inherits from [directoryObject](directoryobject.md).</span></span>

## <a name="methods"></a><span data-ttu-id="e27e7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e27e7-110">Methods</span></span>

| <span data-ttu-id="e27e7-111">Método</span><span class="sxs-lookup"><span data-stu-id="e27e7-111">Method</span></span>       | <span data-ttu-id="e27e7-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e27e7-112">Return Type</span></span>  |<span data-ttu-id="e27e7-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e27e7-113">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e27e7-114">Obtener directoryRole</span><span class="sxs-lookup"><span data-stu-id="e27e7-114">Get directoryRole</span></span>](../api/directoryrole_get.md) | [<span data-ttu-id="e27e7-115">directoryRole</span><span class="sxs-lookup"><span data-stu-id="e27e7-115">directoryRole</span></span>](directoryrole.md) | <span data-ttu-id="e27e7-116">Lea las propiedades y las relaciones del objeto directoryRole.</span><span class="sxs-lookup"><span data-stu-id="e27e7-116">Read properties and relationships of directoryRole object.</span></span> |
|[<span data-ttu-id="e27e7-117">List directoryRoles</span><span class="sxs-lookup"><span data-stu-id="e27e7-117">List directoryRoles</span></span>](../api/directoryrole_list.md) | <span data-ttu-id="e27e7-118">Colección [directoryRole](directoryrole.md)</span><span class="sxs-lookup"><span data-stu-id="e27e7-118">[directoryRole](directoryrole.md) collection</span></span> | <span data-ttu-id="e27e7-119">Enumera los roles de directorio que están activados en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="e27e7-119">List the directory roles that are activated in the tenant.</span></span> |
|[<span data-ttu-id="e27e7-120">Agregar miembro</span><span class="sxs-lookup"><span data-stu-id="e27e7-120">Add member</span></span>](../api/directoryrole_post_members.md) |[<span data-ttu-id="e27e7-121">directoryObject</span><span class="sxs-lookup"><span data-stu-id="e27e7-121">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="e27e7-122">Agregue un usuario al rol de directorio; para ello, publique en la propiedad de navegación de miembros.</span><span class="sxs-lookup"><span data-stu-id="e27e7-122">Add a user to the directory role by posting to the members navigation property.</span></span>|
|[<span data-ttu-id="e27e7-123">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="e27e7-123">List members</span></span>](../api/directoryrole_list_members.md) |<span data-ttu-id="e27e7-124">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="e27e7-124">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="e27e7-125">Obtenga los usuarios que son miembros del rol de directorio de la propiedad de navegación de miembros.</span><span class="sxs-lookup"><span data-stu-id="e27e7-125">Get the users that are members of the directory role from the members navigation property.</span></span>|
|[<span data-ttu-id="e27e7-126">Quitar un miembro</span><span class="sxs-lookup"><span data-stu-id="e27e7-126">Remove a member</span></span>](../api/directoryrole_delete_member.md) |[<span data-ttu-id="e27e7-127">directoryObject</span><span class="sxs-lookup"><span data-stu-id="e27e7-127">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="e27e7-128">Elimine un usuario del rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="e27e7-128">Remove a user from the directory role.</span></span>|
|[<span data-ttu-id="e27e7-129">Activar directoryRole</span><span class="sxs-lookup"><span data-stu-id="e27e7-129">Activate directoryRole</span></span>](../api/directoryrole_post_directoryroles.md) |[<span data-ttu-id="e27e7-130">directoryRole</span><span class="sxs-lookup"><span data-stu-id="e27e7-130">directoryRole</span></span>](directoryrole.md) | <span data-ttu-id="e27e7-131">Active un rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="e27e7-131">Activate a directory role.</span></span>|

## <a name="properties"></a><span data-ttu-id="e27e7-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e27e7-132">Properties</span></span>
| <span data-ttu-id="e27e7-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e27e7-133">Property</span></span>   | <span data-ttu-id="e27e7-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="e27e7-134">Type</span></span> | <span data-ttu-id="e27e7-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="e27e7-135">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="e27e7-136">description</span><span class="sxs-lookup"><span data-stu-id="e27e7-136">description</span></span>|<span data-ttu-id="e27e7-137">String</span><span class="sxs-lookup"><span data-stu-id="e27e7-137">String</span></span>|<span data-ttu-id="e27e7-p102">La descripción del rol de directorio. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e27e7-p102">The description for the directory role. Read-only.</span></span> |
|<span data-ttu-id="e27e7-140">displayName</span><span class="sxs-lookup"><span data-stu-id="e27e7-140">displayName</span></span>|<span data-ttu-id="e27e7-141">String</span><span class="sxs-lookup"><span data-stu-id="e27e7-141">String</span></span>|<span data-ttu-id="e27e7-p103">El nombre para mostrar del rol de directorio. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e27e7-p103">The display name for the directory role. Read-only.</span></span> |
|<span data-ttu-id="e27e7-144">id</span><span class="sxs-lookup"><span data-stu-id="e27e7-144">id</span></span>|<span data-ttu-id="e27e7-145">String</span><span class="sxs-lookup"><span data-stu-id="e27e7-145">String</span></span>|<span data-ttu-id="e27e7-p104">El identificador único del rol de directorio. Hereda de [directoryObject](directoryobject.md). Clave, no admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e27e7-p104">The unique identifier for the directory role. Inherited from [directoryObject](directoryobject.md). Key, Not nullable, Read-only.</span></span>|
|<span data-ttu-id="e27e7-149">roleTemplateId</span><span class="sxs-lookup"><span data-stu-id="e27e7-149">roleTemplateId</span></span>|<span data-ttu-id="e27e7-150">String</span><span class="sxs-lookup"><span data-stu-id="e27e7-150">String</span></span>| <span data-ttu-id="e27e7-p105">El **id** de la [directoryRoleTemplate](directoryroletemplate.md) en que se basa este rol. La propiedad debe especificarse al activar un rol de directorio en un inquilino con una operación POST. Una vez activado el rol de directorio, la propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e27e7-p105">The **id** of the [directoryRoleTemplate](directoryroletemplate.md) that this role is based on. The property must be specified when activating a directory role in a tenant with a POST operation. After the directory role has been activated, the property is read only.</span></span> |

## <a name="relationships"></a><span data-ttu-id="e27e7-154">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e27e7-154">Relationships</span></span>
| <span data-ttu-id="e27e7-155">Relación</span><span class="sxs-lookup"><span data-stu-id="e27e7-155">Relationship</span></span> | <span data-ttu-id="e27e7-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="e27e7-156">Type</span></span> |<span data-ttu-id="e27e7-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="e27e7-157">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e27e7-158">members</span><span class="sxs-lookup"><span data-stu-id="e27e7-158">members</span></span>|<span data-ttu-id="e27e7-159">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="e27e7-159">[directoryObject](directoryobject.md) collection</span></span>|<span data-ttu-id="e27e7-p106">Usuarios que son miembros de este rol de directorio. Métodos HTTP: GET, POST, DELETE. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="e27e7-p106">Users that are members of this directory role. HTTP Methods: GET, POST, DELETE. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e27e7-164">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e27e7-164">JSON representation</span></span>

<span data-ttu-id="e27e7-165">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e27e7-165">Here is a JSON representation of the resource</span></span>

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
