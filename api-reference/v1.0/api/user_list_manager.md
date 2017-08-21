# <a name="list-manager"></a><span data-ttu-id="cb0df-101">List manager</span><span class="sxs-lookup"><span data-stu-id="cb0df-101">List manager</span></span>

<span data-ttu-id="cb0df-p101">Obtiene el administrador del usuario. Devuelve el usuario o el contacto asignado como administrador del usuario.</span><span class="sxs-lookup"><span data-stu-id="cb0df-p101">Get user's manager. Returns the user or contact assigned as the user's manager.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cb0df-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cb0df-104">Prerequisites</span></span>
<span data-ttu-id="cb0df-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="cb0df-105">One of the following **scopes** is required to execute this API: *User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="cb0df-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cb0df-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/manager
```
## <a name="optional-query-parameters"></a><span data-ttu-id="cb0df-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="cb0df-107">Optional query parameters</span></span>
<span data-ttu-id="cb0df-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb0df-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="cb0df-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cb0df-109">Request headers</span></span>
| <span data-ttu-id="cb0df-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb0df-110">Header</span></span>       | <span data-ttu-id="cb0df-111">Valor</span><span class="sxs-lookup"><span data-stu-id="cb0df-111">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="cb0df-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="cb0df-112">Authorization</span></span>  | <span data-ttu-id="cb0df-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cb0df-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="cb0df-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="cb0df-115">Content-Type</span></span>   | <span data-ttu-id="cb0df-116">application/json</span><span class="sxs-lookup"><span data-stu-id="cb0df-116">application/json</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="cb0df-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cb0df-117">Request body</span></span>
<span data-ttu-id="cb0df-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cb0df-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cb0df-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb0df-119">Response</span></span>

<span data-ttu-id="cb0df-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb0df-120">If successful, this method returns a `200 OK` response code and a [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="cb0df-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cb0df-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cb0df-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cb0df-122">Request</span></span>
<span data-ttu-id="cb0df-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cb0df-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_manager"
}-->
```http
GET https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/manager
```
##### <a name="response"></a><span data-ttu-id="cb0df-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb0df-124">Response</span></span>
<span data-ttu-id="cb0df-125">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb0df-125">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "objectType": "User",
  "id": "111048d2-2761-4347-b978-07354283363b",
  "accountEnabled": true,
  "city": "San Diego",
  "country": "United States",
  "department": "Sales & Marketing",
  "displayName": "Sara Davis",
  "givenName": "Sara",
  "jobTitle": "Finance VP",
  "mail": "SaraD@contoso.onmicrosoft.com",
  "mailNickname": "SaraD",
  "state": "CA",
  "streetAddress": "9256 Towne Center Dr., Suite 400",
  "surname": "Davis",
  "usageLocation": "US",
  "userPrincipalName": "SaraD@contoso.onmicrosoft.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List directReports",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
