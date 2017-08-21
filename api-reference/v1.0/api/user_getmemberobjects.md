# <a name="user-getmemberobjects"></a><span data-ttu-id="7d2c1-101">user: getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="7d2c1-101">user: getMemberObjects</span></span>
<span data-ttu-id="7d2c1-p101">Devuelve todos los grupos, roles de directorio y unidades administrativas de los que el usuario es miembro. La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="7d2c1-p101">Return all of the groups, directory roles and administrative units that the user is a member of. The check is transitive.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7d2c1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7d2c1-104">Prerequisites</span></span>
<span data-ttu-id="7d2c1-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="7d2c1-105">One of the following **scopes** is required to execute this API: *Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="7d2c1-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7d2c1-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/getMemberObjects
```
## <a name="request-headers"></a><span data-ttu-id="7d2c1-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7d2c1-107">Request headers</span></span>
| <span data-ttu-id="7d2c1-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d2c1-108">Header</span></span>       | <span data-ttu-id="7d2c1-109">Valor</span><span class="sxs-lookup"><span data-stu-id="7d2c1-109">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="7d2c1-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="7d2c1-110">Authorization</span></span>  | <span data-ttu-id="7d2c1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7d2c1-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="7d2c1-113">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7d2c1-113">Content-Type</span></span>  | <span data-ttu-id="7d2c1-114">application/json</span><span class="sxs-lookup"><span data-stu-id="7d2c1-114">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7d2c1-115">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="7d2c1-115">Request body</span></span>
<span data-ttu-id="7d2c1-116">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="7d2c1-116">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="7d2c1-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7d2c1-117">Parameter</span></span>    | <span data-ttu-id="7d2c1-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d2c1-118">Type</span></span>   |<span data-ttu-id="7d2c1-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d2c1-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7d2c1-120">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="7d2c1-120">securityEnabledOnly</span></span>|<span data-ttu-id="7d2c1-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="7d2c1-121">Boolean</span></span>|<span data-ttu-id="7d2c1-p103">**true** para especificar que solo deben devolverse los grupos de seguridad de los que el usuario sea miembro; **false** para especificar que deben devolverse todos los grupos y roles de directorio de los que el usuario sea miembro. Nota: Establecer este parámetro en **verdadero** solo es posible al llamar este método en un usuario.</span><span class="sxs-lookup"><span data-stu-id="7d2c1-p103">**true** to specify that only security groups that the user is a member of should be returned; **false** to specify that all groups and directory roles that the user is a member of should be returned. Note: Setting this parameter to **true** is only supported when calling this method on a user.</span></span>|

## <a name="response"></a><span data-ttu-id="7d2c1-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d2c1-124">Response</span></span>

<span data-ttu-id="7d2c1-125">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y la colección de cadenas en el cuerpo de la respuesta que contiene los identificadores de los grupos y los roles de directorio de los que el usuario sea miembro.</span><span class="sxs-lookup"><span data-stu-id="7d2c1-125">If successful, this method returns `200, OK` response code and String collection in the response body that contains the IDs of the groups and directory roles that the user is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="7d2c1-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7d2c1-126">Example</span></span>
<span data-ttu-id="7d2c1-127">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="7d2c1-127">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="7d2c1-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7d2c1-128">Request</span></span>
<span data-ttu-id="7d2c1-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d2c1-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/getMemberObjects
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="7d2c1-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d2c1-130">Response</span></span>
<span data-ttu-id="7d2c1-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7d2c1-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "value": [
    "string-value"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: getMemberObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
