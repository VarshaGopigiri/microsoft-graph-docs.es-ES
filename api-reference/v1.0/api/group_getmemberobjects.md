# <a name="group-getmemberobjects"></a><span data-ttu-id="8fd79-101">group: getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="8fd79-101">group: getMemberObjects</span></span>
<span data-ttu-id="8fd79-p101">Devuelve todos los grupos de los que el grupo es miembro. La comprobación es transitiva. Nota: Los grupos no pueden ser miembros de roles de directorio, por lo que no se devolverá ningún rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="8fd79-p101">Return all of the groups that this group is a member of. The check is transitive. Note: Groups cannot be members of directory roles, so no directory roles will be returned.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8fd79-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8fd79-105">Prerequisites</span></span>
<span data-ttu-id="8fd79-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="8fd79-106">One of the following **scopes** is required to execute this API: One of the following **scopes** is required to execute this API: *Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="8fd79-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8fd79-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/getMemberObjects
```
## <a name="request-headers"></a><span data-ttu-id="8fd79-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8fd79-108">Request headers</span></span>
| <span data-ttu-id="8fd79-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="8fd79-109">Name</span></span>       | <span data-ttu-id="8fd79-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8fd79-110">Type</span></span> | <span data-ttu-id="8fd79-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fd79-111">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="8fd79-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="8fd79-112">Authorization</span></span>  | <span data-ttu-id="8fd79-113">string</span><span class="sxs-lookup"><span data-stu-id="8fd79-113">string</span></span>  | <span data-ttu-id="8fd79-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8fd79-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8fd79-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8fd79-116">Request body</span></span>
<span data-ttu-id="8fd79-117">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="8fd79-117">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="8fd79-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="8fd79-118">Parameter</span></span>    | <span data-ttu-id="8fd79-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="8fd79-119">Type</span></span>   |<span data-ttu-id="8fd79-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fd79-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8fd79-121">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="8fd79-121">securityEnabledOnly</span></span>|<span data-ttu-id="8fd79-122">Boolean</span><span class="sxs-lookup"><span data-stu-id="8fd79-122">Boolean</span></span>| <span data-ttu-id="8fd79-p103">Establecer en **false**. La devolución solo de grupos con la seguridad activada solo es compatible para usuarios.</span><span class="sxs-lookup"><span data-stu-id="8fd79-p103">Set to **false**. Returning only security-enabled groups is supported for users only.</span></span>|

## <a name="response"></a><span data-ttu-id="8fd79-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8fd79-125">Response</span></span>

<span data-ttu-id="8fd79-126">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el grupo sea miembro.</span><span class="sxs-lookup"><span data-stu-id="8fd79-126">If successful, this method returns `200, OK` response code and String collection in the response body that contains the IDs of the groups that the group is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="8fd79-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8fd79-127">Example</span></span>
<span data-ttu-id="8fd79-128">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="8fd79-128">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="8fd79-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8fd79-129">Request</span></span>
<span data-ttu-id="8fd79-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8fd79-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/getMemberObjects
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": false
}
```

##### <a name="response"></a><span data-ttu-id="8fd79-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8fd79-131">Response</span></span>
<span data-ttu-id="8fd79-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8fd79-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "group: getMemberObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
