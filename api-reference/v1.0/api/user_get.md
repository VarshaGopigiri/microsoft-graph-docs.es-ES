# <a name="get-a-user"></a><span data-ttu-id="276b2-101">Obtener un usuario</span><span class="sxs-lookup"><span data-stu-id="276b2-101">Get a user</span></span>

<span data-ttu-id="276b2-102">Recupere las propiedades y las relaciones del objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="276b2-102">Retrieve the properties and relationships of user object.</span></span>

> <span data-ttu-id="276b2-p101">Nota: La obtención de un usuario solo devuelve un conjunto predeterminado de propiedades (*businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName*). Use `$select` para obtener otras propiedades y relaciones del objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="276b2-p101">Note: Getting a user returns a default set of properties only (*businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName*). Use `$select` to get the other properties and relationships for the [user](../resources/user.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="276b2-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="276b2-105">Prerequisites</span></span>
<span data-ttu-id="276b2-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *User.Read; User.ReadWrite; User.ReadBasic.All; User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="276b2-106">One of the following **scopes** is required to execute this API: *User.Read; User.ReadWrite; User.ReadBasic.All; User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="276b2-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="276b2-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="276b2-108">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="276b2-108">Optional query parameters</span></span>
<span data-ttu-id="276b2-109">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="276b2-109">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="276b2-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="276b2-110">Request headers</span></span>
| <span data-ttu-id="276b2-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="276b2-111">Header</span></span>       | <span data-ttu-id="276b2-112">Valor</span><span class="sxs-lookup"><span data-stu-id="276b2-112">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="276b2-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="276b2-113">Authorization</span></span>  | <span data-ttu-id="276b2-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="276b2-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="276b2-116">Content-Type</span><span class="sxs-lookup"><span data-stu-id="276b2-116">Content-Type</span></span>   | <span data-ttu-id="276b2-117">application/json</span><span class="sxs-lookup"><span data-stu-id="276b2-117">application/json</span></span> | 

## <a name="request-body"></a><span data-ttu-id="276b2-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="276b2-118">Request body</span></span>
<span data-ttu-id="276b2-119">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="276b2-119">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="276b2-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="276b2-120">Response</span></span>

<span data-ttu-id="276b2-121">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="276b2-121">If successful, this method returns a `200 OK` response code and [user](../resources/user.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="276b2-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="276b2-122">Example</span></span>
##### <a name="request"></a><span data-ttu-id="276b2-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="276b2-123">Request</span></span>
<span data-ttu-id="276b2-124">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="276b2-124">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_user"
}-->
```http
GET https://graph.microsoft.com/v1.0/me
```
##### <a name="response"></a><span data-ttu-id="276b2-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="276b2-125">Response</span></span>
<span data-ttu-id="276b2-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="276b2-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 491

{
  "businessPhones": [
       "businessPhones-value"
   ],
   "displayName": "displayName-value",
   "givenName": "givenName-value",
   "jobTitle": "jobTitle-value",
   "mail": "mail-value",
   "mobilePhone": "mobilePhone-value",
   "officeLocation": "officeLocation-value",
   "preferredLanguage": "preferredLanguage-value",
   "surname": "surname-value",
   "userPrincipalName": "userPrincipalName-value",
   "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
