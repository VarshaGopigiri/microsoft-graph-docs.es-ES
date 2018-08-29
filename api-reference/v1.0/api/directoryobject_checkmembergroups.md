# <a name="check-member-groups"></a><span data-ttu-id="871f5-101">Comprobar grupos de miembro</span><span class="sxs-lookup"><span data-stu-id="871f5-101">Check member groups</span></span>

<span data-ttu-id="871f5-p101">Comprueba la pertenencia en una lista especificada de grupos y devuelve de la lista los grupos de los que el objeto especificado de usuario, grupo o directorio sea miembro. Esta función es transitiva.</span><span class="sxs-lookup"><span data-stu-id="871f5-p101">Check for membership in a specified list of groups, and returns from that list those groups of which the specified user, group, or directory object is a member. This function is transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="871f5-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="871f5-104">Permissions</span></span>
<span data-ttu-id="871f5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="871f5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="871f5-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="871f5-107">Permission type</span></span>      | <span data-ttu-id="871f5-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="871f5-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="871f5-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="871f5-109">Delegated (work or school account)</span></span> | <span data-ttu-id="871f5-110">User.Read.All y Group.Read.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="871f5-110">User.Read.All and Group.Read.All, Directory.Read.All</span></span>    |
|<span data-ttu-id="871f5-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="871f5-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="871f5-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="871f5-112">Not supported.</span></span>    |
|<span data-ttu-id="871f5-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="871f5-113">Application</span></span> | <span data-ttu-id="871f5-114">User.Read.All y Group.Read.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="871f5-114">User.Read.All and Group.Read.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="871f5-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="871f5-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/checkMemberGroups
POST /users/{id | userPrincipalName}/checkMemberGroups
POST /groups/{id}/checkMemberGroups
POST /directoryObjects/{id}/checkMemberGroups
```
## <a name="request-headers"></a><span data-ttu-id="871f5-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="871f5-116">Request headers</span></span>
| <span data-ttu-id="871f5-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="871f5-117">Name</span></span>       | <span data-ttu-id="871f5-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="871f5-118">Type</span></span> | <span data-ttu-id="871f5-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="871f5-119">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="871f5-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="871f5-120">Authorization</span></span>  | <span data-ttu-id="871f5-121">cadena</span><span class="sxs-lookup"><span data-stu-id="871f5-121">string</span></span>  | <span data-ttu-id="871f5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="871f5-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="871f5-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="871f5-124">Content-Type</span></span>  | <span data-ttu-id="871f5-125">cadena</span><span class="sxs-lookup"><span data-stu-id="871f5-125">string</span></span> | <span data-ttu-id="871f5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="871f5-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="871f5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="871f5-127">Request body</span></span>
<span data-ttu-id="871f5-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="871f5-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="871f5-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="871f5-129">Parameter</span></span>    | <span data-ttu-id="871f5-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="871f5-130">Type</span></span>   |<span data-ttu-id="871f5-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="871f5-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="871f5-132">groupIds</span><span class="sxs-lookup"><span data-stu-id="871f5-132">groupIds</span></span>|<span data-ttu-id="871f5-133">Colección String</span><span class="sxs-lookup"><span data-stu-id="871f5-133">String collection</span></span>|<span data-ttu-id="871f5-p104">Colección que contiene los identificadores de objeto de los grupos en los que se comprueba la pertenencia. Pueden especificarse hasta 20 grupos.</span><span class="sxs-lookup"><span data-stu-id="871f5-p104">A collection that contains the object IDs of the groups in which to check membership. Up to 20 groups may be specified.</span></span>|

## <a name="response"></a><span data-ttu-id="871f5-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="871f5-136">Response</span></span>

<span data-ttu-id="871f5-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="871f5-137">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="871f5-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="871f5-138">Example</span></span>

##### <a name="request"></a><span data-ttu-id="871f5-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="871f5-139">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "directoryobject_checkmembergroups"
}-->
```http
POST https://graph.microsoft.com/v1.0/directoryObjects/{id}/checkMemberGroups
Content-type: application/json

{
  "groupIds": [
        "fee2c45b-915a-4a64b130f4eb9e75525e",
        "4fe90ae065a-478b9400e0a0e1cbd540"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="871f5-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="871f5-140">Response</span></span>
<span data-ttu-id="871f5-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="871f5-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "value": [
        "fee2c45b-915a-4a64-b130-f4eb9e75525e"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject: checkMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
