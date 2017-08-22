# <a name="check-member-groups"></a><span data-ttu-id="14a1e-101">Comprobar grupos de miembro</span><span class="sxs-lookup"><span data-stu-id="14a1e-101">Check member groups</span></span>

<span data-ttu-id="14a1e-p101">Comprueba la pertenencia en una lista especificada de grupos y devuelve de la lista los grupos de los que el objeto especificado de usuario, grupo o directorio sea miembro. Esta función es transitiva.</span><span class="sxs-lookup"><span data-stu-id="14a1e-p101">Check for membership in a specified list of groups, and returns from that list those groups of which the specified user, group, or directory object is a member. This function is transitive.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="14a1e-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="14a1e-104">Prerequisites</span></span>
<span data-ttu-id="14a1e-105">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="14a1e-105">The following **scopes** are required to execute this API:</span></span> 
- <span data-ttu-id="14a1e-106">_User.Read.All_ Y _Group.Read.All_</span><span class="sxs-lookup"><span data-stu-id="14a1e-106">_User.Read.All_ AND _Group.Read.All_</span></span>
- <span data-ttu-id="14a1e-107">_Directory.Read.All_</span><span class="sxs-lookup"><span data-stu-id="14a1e-107">_Directory.Read.All_</span></span>

> <span data-ttu-id="14a1e-108">Nota: Los ámbitos de permiso se muestran por orden de privilegio mínimo necesario.</span><span class="sxs-lookup"><span data-stu-id="14a1e-108">Note: Permission scopes are listed in least privilege required order.</span></span>

## <a name="http-request"></a><span data-ttu-id="14a1e-109">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="14a1e-109">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/checkMemberGroups
POST /users/{id | userPrincipalName}/checkMemberGroups
POST /groups/{id}/checkMemberGroups
POST /directoryObjects/{id}/checkMemberGroups
```
## <a name="request-headers"></a><span data-ttu-id="14a1e-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="14a1e-110">Request headers</span></span>
| <span data-ttu-id="14a1e-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="14a1e-111">Name</span></span>       | <span data-ttu-id="14a1e-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="14a1e-112">Type</span></span> | <span data-ttu-id="14a1e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="14a1e-113">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="14a1e-114">Authorization</span><span class="sxs-lookup"><span data-stu-id="14a1e-114">Authorization</span></span>  | <span data-ttu-id="14a1e-115">string</span><span class="sxs-lookup"><span data-stu-id="14a1e-115">string</span></span>  | <span data-ttu-id="14a1e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="14a1e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="14a1e-118">Content-Type</span><span class="sxs-lookup"><span data-stu-id="14a1e-118">Content-Type</span></span>  | <span data-ttu-id="14a1e-119">application/json</span><span class="sxs-lookup"><span data-stu-id="14a1e-119">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="14a1e-120">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="14a1e-120">Request body</span></span>
<span data-ttu-id="14a1e-121">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="14a1e-121">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="14a1e-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="14a1e-122">Parameter</span></span>    | <span data-ttu-id="14a1e-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="14a1e-123">Type</span></span>   |<span data-ttu-id="14a1e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="14a1e-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="14a1e-125">groupIds</span><span class="sxs-lookup"><span data-stu-id="14a1e-125">groupIds</span></span>|<span data-ttu-id="14a1e-126">String</span><span class="sxs-lookup"><span data-stu-id="14a1e-126">String</span></span>|<span data-ttu-id="14a1e-p103">Colección que contiene los identificadores de objeto de los grupos en los que se comprueba la pertenencia. Pueden especificarse hasta 20 grupos.</span><span class="sxs-lookup"><span data-stu-id="14a1e-p103">A collection that contains the object IDs of the groups in which to check membership. Up to 20 groups may be specified.</span></span>|

## <a name="response"></a><span data-ttu-id="14a1e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="14a1e-129">Response</span></span>

<span data-ttu-id="14a1e-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="14a1e-130">If successful, this method returns `200, OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="14a1e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="14a1e-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="14a1e-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="14a1e-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "directoryobject_checkmembergroups"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/checkMemberGroups
Content-type: application/json

{
  "groupIds": [
        "fee2c45b-915a-4a64-b130-f4eb9e75525e",
        "4fe90ae7-065a-478b-9400-e0a0e1cbd540"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="14a1e-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="14a1e-133">Response</span></span>
<span data-ttu-id="14a1e-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="14a1e-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
