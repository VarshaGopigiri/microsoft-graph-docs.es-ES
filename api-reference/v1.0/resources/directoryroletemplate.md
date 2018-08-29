# <a name="directoryroletemplate-resource-type"></a><span data-ttu-id="1bad5-101">Tipo de recurso directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="1bad5-101">directoryRoleTemplate resource type</span></span>

<span data-ttu-id="1bad5-p101">Representa una plantilla de rol de directorio. Una plantilla de rol de directorio especifica los valores de propiedad de un rol de directorio ([directoryRole](directoryrole.md)). Existe un objeto de plantilla de rol de directorio asociado para cada uno de los roles de directorio que puedan activarse en un inquilino. Para leer un rol de directorio o actualizar sus miembros, debe activarse primero en el inquilino. Solo se activa de manera predeterminada el rol de directorio Administradores de la compañía. Para activar otros roles de directorio disponibles, envíe una solicitud POST al extremo `/directoryRoles` con el identificador de la plantilla de rol de directorio en que se basa el rol de directorio especificado en el parámetro **roleTemplateId** de la solicitud. Al completar esta solicitud, puede empezar a leer y asignar miembros al rol de directorio. **Nota**: Una plantilla de rol de directorio se expone para el rol de directorio Usuarios. El rol de directorio Usuarios es implícito y no lo pueden ver los clientes del directorio. La infraestructura asigna a todos los usuarios del inquilino a este rol. El rol ya está activado. No use esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="1bad5-p101">Represents a directory role template. A directory role template specifies the property values of a directory role ([directoryRole](directoryrole.md)). There is an associated directory role template object for each of the directory roles that may be activated in a tenant. To read a directory role or update its members, it must first be activated in the tenant. Only the Company Administrators directory role is activated by default. To activate other available directory roles you send a POST request to the `/directoryRoles` endpoint with the ID of the directory role template on which the directory role is based specified in the **roleTemplateId** parameter of the request. Upon successful completion of this request, you can then start to read and assign members to the directory role. **Note**: A directory role template is exposed for the Users directory role. The Users directory role is implicit and is not visible to directory clients. Every User in the tenant is assigned to this role by the infrastructure. The role is already activated. Do not use this template.</span></span>


## <a name="methods"></a><span data-ttu-id="1bad5-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="1bad5-114">Methods</span></span>

| <span data-ttu-id="1bad5-115">Método</span><span class="sxs-lookup"><span data-stu-id="1bad5-115">Method</span></span>       | <span data-ttu-id="1bad5-116">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1bad5-116">Return Type</span></span>  |<span data-ttu-id="1bad5-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1bad5-117">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="1bad5-118">Obtener directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="1bad5-118">Get directoryRoleTemplate</span></span>](../api/directoryroletemplate_get.md) | [<span data-ttu-id="1bad5-119">directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="1bad5-119">directoryRoleTemplate</span></span>](directoryroletemplate.md) |<span data-ttu-id="1bad5-120">Lea las propiedades y las relaciones del objeto directoryRoleTemplate.</span><span class="sxs-lookup"><span data-stu-id="1bad5-120">Read properties and relationships of directoryRoleTemplate object.</span></span>|
|[<span data-ttu-id="1bad5-121">Listar directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="1bad5-121">List directoryRoleTemplate</span></span>](../api/directoryroletemplate_list.md) | <span data-ttu-id="1bad5-122">Colección [directoryRoleTemplate](directoryroletemplate.md)</span><span class="sxs-lookup"><span data-stu-id="1bad5-122">[directoryRoleTemplate](directoryroletemplate.md) collection</span></span> |<span data-ttu-id="1bad5-123">Recupere una lista de objetos directoryRoleTemplate.</span><span class="sxs-lookup"><span data-stu-id="1bad5-123">Retrieve a list of directoryRoleTemplate objects.</span></span>|

## <a name="properties"></a><span data-ttu-id="1bad5-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1bad5-124">Properties</span></span>
| <span data-ttu-id="1bad5-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1bad5-125">Property</span></span>     | <span data-ttu-id="1bad5-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="1bad5-126">Type</span></span>   |<span data-ttu-id="1bad5-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="1bad5-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1bad5-128">description</span><span class="sxs-lookup"><span data-stu-id="1bad5-128">description</span></span>|<span data-ttu-id="1bad5-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="1bad5-129">String</span></span>|<span data-ttu-id="1bad5-p102">La descripción del rol de directorio que se establecerá. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1bad5-p102">The description to set for the directory role. Read-only.</span></span>|
|<span data-ttu-id="1bad5-132">displayName</span><span class="sxs-lookup"><span data-stu-id="1bad5-132">displayName</span></span>|<span data-ttu-id="1bad5-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="1bad5-133">String</span></span>|<span data-ttu-id="1bad5-p103">El nombre para mostrar del rol de directorio que se establecerá. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1bad5-p103">The display name to set for the directory role. Read-only.</span></span> |
|<span data-ttu-id="1bad5-136">id</span><span class="sxs-lookup"><span data-stu-id="1bad5-136">id</span></span>|<span data-ttu-id="1bad5-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="1bad5-137">String</span></span>|<span data-ttu-id="1bad5-p104">El identificador único de la plantilla. Hereda de [directoryObject](directoryobject.md). Especifique el **id** de la plantilla de rol de directorio de la propiedad **roleTemplateId** en la solicitud POST para activar un [directoryRole](directoryrole.md) en un inquilino. Clave, no admite valores NULL. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1bad5-p104">The unique identifier for the template. Inherited from [directoryObject](directoryobject.md). You specify the **id** of the directory role template for the **roleTemplateId** property in the POST request activate a [directoryRole](directoryrole.md) in a tenant. Key, Not nullable. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="1bad5-143">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1bad5-143">Relationships</span></span>
<span data-ttu-id="1bad5-144">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1bad5-144">None</span></span>



## <a name="json-representation"></a><span data-ttu-id="1bad5-145">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1bad5-145">JSON representation</span></span>

<span data-ttu-id="1bad5-146">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="1bad5-146">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.directoryObject",
  "@odata.type": "microsoft.graph.directoryRoleTemplate",
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
  "id": "string (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryRoleTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
