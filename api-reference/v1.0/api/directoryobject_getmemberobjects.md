# <a name="get-member-objects"></a><span data-ttu-id="66bc9-101">Obtener objetos de miembro</span><span class="sxs-lookup"><span data-stu-id="66bc9-101">Get member objects</span></span>

 <span data-ttu-id="66bc9-p101">Devuelve todos los grupos y roles de directorio de los que un usuario, grupo u objeto de directorio sea miembro. Esta función es transitiva.</span><span class="sxs-lookup"><span data-stu-id="66bc9-p101">Returns all the groups and directory roles that a user, group, or directory object is a member of. This function is transitive.</span></span> 
 > <span data-ttu-id="66bc9-104">Nota: Solo los usuarios pueden ser miembros de roles de directorio.</span><span class="sxs-lookup"><span data-stu-id="66bc9-104">Note: Only users can be members of directory roles.</span></span>

## <a name="permissions"></a><span data-ttu-id="66bc9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="66bc9-105">Permissions</span></span>
<span data-ttu-id="66bc9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="66bc9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="66bc9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="66bc9-108">Permission type</span></span>      | <span data-ttu-id="66bc9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="66bc9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="66bc9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="66bc9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="66bc9-111">User.Read.All y Group.Read.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="66bc9-111">User.Read.All and Group.Read.All, Directory.Read.All</span></span>    |
|<span data-ttu-id="66bc9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="66bc9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="66bc9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="66bc9-113">Not supported.</span></span>    |
|<span data-ttu-id="66bc9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="66bc9-114">Application</span></span> | <span data-ttu-id="66bc9-115">User.Read.All y Group.Read.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="66bc9-115">User.Read.All and Group.Read.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="66bc9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="66bc9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/getMemberObjects
POST /users/{id | userPrincipalName}/getMemberObjects
POST /groups/{id}/getMemberGroups
POST /directoryObjects/{id}/getMemberObjects

```
## <a name="request-headers"></a><span data-ttu-id="66bc9-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="66bc9-117">Request headers</span></span>
| <span data-ttu-id="66bc9-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="66bc9-118">Name</span></span>       | <span data-ttu-id="66bc9-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="66bc9-119">Type</span></span> | <span data-ttu-id="66bc9-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="66bc9-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="66bc9-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="66bc9-121">Authorization</span></span>  | <span data-ttu-id="66bc9-122">cadena</span><span class="sxs-lookup"><span data-stu-id="66bc9-122">string</span></span>  | <span data-ttu-id="66bc9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="66bc9-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="66bc9-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="66bc9-125">Content-Type</span></span>   | <span data-ttu-id="66bc9-126">string</span><span class="sxs-lookup"><span data-stu-id="66bc9-126">string</span></span>  | <span data-ttu-id="66bc9-127">application/json</span><span class="sxs-lookup"><span data-stu-id="66bc9-127">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="66bc9-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="66bc9-128">Request body</span></span>
<span data-ttu-id="66bc9-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="66bc9-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="66bc9-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="66bc9-130">Parameter</span></span>    | <span data-ttu-id="66bc9-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="66bc9-131">Type</span></span>   |<span data-ttu-id="66bc9-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="66bc9-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="66bc9-133">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="66bc9-133">securityEnabledOnly</span></span>|<span data-ttu-id="66bc9-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="66bc9-134">Boolean</span></span>| <span data-ttu-id="66bc9-p104">**true** para especificar que solo deben devolverse los grupos de seguridad de los que la entidad es miembro; **false** para especificar que deben devolverse todos los grupos y roles de directorio de los que la entidad es miembro. **Nota:** Solo se puede llamar la función en un usuario si el parámetro es **true**.</span><span class="sxs-lookup"><span data-stu-id="66bc9-p104">**true** to specify that only security groups that the entity is a member of should be returned; **false** to specify that all groups and directory roles that the entity is a member of should be returned. **Note**: The function can only be called on a user if the parameter is **true**.</span></span> |

## <a name="response"></a><span data-ttu-id="66bc9-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66bc9-137">Response</span></span>

<span data-ttu-id="66bc9-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66bc9-138">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="66bc9-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66bc9-139">Example</span></span>

##### <a name="request"></a><span data-ttu-id="66bc9-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="66bc9-140">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "directoryobject_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/v1.0/directoryObjects/{object-id}/getMemberObjects
Content-type: application/json

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="66bc9-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66bc9-141">Response</span></span>
<span data-ttu-id="66bc9-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="66bc9-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Collection(Edm.String)",
    "value": [
        "fee2c45b-915a-4a64-b130-f4eb9e75525e",
        "4fe90ae7-065a-478b-9400-e0a0e1cbd540",
        "c9ee2d50-9e8a-4352-b97c-4c2c99557c22",
        "e0c3beaf-eeb4-43d8-abc5-94f037a65697"
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject: getMemberObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
