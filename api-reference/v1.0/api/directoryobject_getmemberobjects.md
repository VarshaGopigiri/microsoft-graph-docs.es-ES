# <a name="get-member-objects"></a><span data-ttu-id="457b6-101">Obtener objetos de miembro</span><span class="sxs-lookup"><span data-stu-id="457b6-101">Get member objects</span></span>

 <span data-ttu-id="457b6-p101">Devuelve todos los grupos y roles de directorio de los que un usuario, grupo u objeto de directorio sea miembro. Esta función es transitiva.</span><span class="sxs-lookup"><span data-stu-id="457b6-p101">Returns all the groups and directory roles that a user, group, or directory object is a member of. This function is transitive.</span></span> 
 > <span data-ttu-id="457b6-104">Nota: Solo los usuarios pueden ser miembros de roles de directorio.</span><span class="sxs-lookup"><span data-stu-id="457b6-104">Note: Only users can be members of directory roles.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="457b6-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="457b6-105">Prerequisites</span></span>
<span data-ttu-id="457b6-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="457b6-106">One of the following **scopes** are required to execute this API:</span></span>
- <span data-ttu-id="457b6-107">_User.Read.All_ Y _Group.Read.All_</span><span class="sxs-lookup"><span data-stu-id="457b6-107">_User.Read.All_ AND _Group.Read.All_</span></span>
- <span data-ttu-id="457b6-108">_Directory.Read.All_</span><span class="sxs-lookup"><span data-stu-id="457b6-108">_Directory.Read.All_</span></span>

> <span data-ttu-id="457b6-109">Nota: Los ámbitos de permiso se muestran por orden de privilegio mínimo necesario.</span><span class="sxs-lookup"><span data-stu-id="457b6-109">Note: Permission scopes are listed in least privilege required order.</span></span>

## <a name="http-request"></a><span data-ttu-id="457b6-110">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="457b6-110">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/getMemberObjects
POST /users/{id | userPrincipalName}/getMemberObjects
POST /groups/{id}/getMemberGroups
POST /directoryObjects/{id}/getMemberObjects

```
## <a name="request-headers"></a><span data-ttu-id="457b6-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="457b6-111">Request headers</span></span>
| <span data-ttu-id="457b6-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="457b6-112">Name</span></span>       | <span data-ttu-id="457b6-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="457b6-113">Type</span></span> | <span data-ttu-id="457b6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="457b6-114">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="457b6-115">Authorization</span><span class="sxs-lookup"><span data-stu-id="457b6-115">Authorization</span></span>  | <span data-ttu-id="457b6-116">string</span><span class="sxs-lookup"><span data-stu-id="457b6-116">string</span></span>  | <span data-ttu-id="457b6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="457b6-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="457b6-119">Content-Type</span><span class="sxs-lookup"><span data-stu-id="457b6-119">Content-Type</span></span>  | <span data-ttu-id="457b6-120">application/json</span><span class="sxs-lookup"><span data-stu-id="457b6-120">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="457b6-121">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="457b6-121">Request body</span></span>
<span data-ttu-id="457b6-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="457b6-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="457b6-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="457b6-123">Parameter</span></span>    | <span data-ttu-id="457b6-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="457b6-124">Type</span></span>   |<span data-ttu-id="457b6-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="457b6-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="457b6-126">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="457b6-126">securityEnabledOnly</span></span>|<span data-ttu-id="457b6-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="457b6-127">Boolean</span></span>| <span data-ttu-id="457b6-p103">**true** para especificar que solo deben devolverse los grupos de seguridad de los que la entidad es miembro; **false** para especificar que deben devolverse todos los grupos y roles de directorio de los que la entidad es miembro. **Nota:** Solo se puede llamar la función en un usuario si el parámetro es **true**.</span><span class="sxs-lookup"><span data-stu-id="457b6-p103">**true** to specify that only security groups that the entity is a member of should be returned; **false** to specify that all groups and directory roles that the entity is a member of should be returned. **Note**: The function can only be called on a user if the parameter is **true**.</span></span> |

## <a name="response"></a><span data-ttu-id="457b6-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="457b6-130">Response</span></span>

<span data-ttu-id="457b6-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="457b6-131">If successful, this method returns `200, OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="457b6-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="457b6-132">Example</span></span>

##### <a name="request"></a><span data-ttu-id="457b6-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="457b6-133">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "directoryobject_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/getMemberObjects
Content-type: application/json

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="457b6-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="457b6-134">Response</span></span>
<span data-ttu-id="457b6-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="457b6-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
