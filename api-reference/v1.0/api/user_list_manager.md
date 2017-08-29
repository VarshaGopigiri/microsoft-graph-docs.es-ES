# <a name="list-manager"></a><span data-ttu-id="ede57-101">List manager</span><span class="sxs-lookup"><span data-stu-id="ede57-101">List manager</span></span>

<span data-ttu-id="ede57-p101">Obtiene el administrador del usuario. Devuelve el usuario o el contacto asignado como administrador del usuario.</span><span class="sxs-lookup"><span data-stu-id="ede57-p101">Get user's manager. Returns the user or contact assigned as the user's manager.</span></span>
## <a name="permissions"></a><span data-ttu-id="ede57-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="ede57-104">Permissions</span></span>
<span data-ttu-id="ede57-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ede57-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ede57-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ede57-107">Permission type</span></span>      | <span data-ttu-id="ede57-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ede57-108">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="ede57-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ede57-109">Delegated (work or school account)</span></span> | <span data-ttu-id="ede57-110">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="ede57-110">One of the following scopes is required to execute this API: User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span>    | 
|<span data-ttu-id="ede57-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ede57-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ede57-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ede57-112">Not supported.</span></span>    | 
|<span data-ttu-id="ede57-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ede57-113">Application</span></span> | <span data-ttu-id="ede57-114">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ede57-114">One of the following scopes is required to execute this API: User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="ede57-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ede57-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/manager
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ede57-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ede57-116">Optional query parameters</span></span>
<span data-ttu-id="ede57-117">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ede57-117">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ede57-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ede57-118">Request headers</span></span>
| <span data-ttu-id="ede57-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ede57-119">Header</span></span>       | <span data-ttu-id="ede57-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ede57-120">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="ede57-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="ede57-121">Authorization</span></span>  | <span data-ttu-id="ede57-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ede57-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ede57-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ede57-124">Content-Type</span></span>   | <span data-ttu-id="ede57-125">application/json</span><span class="sxs-lookup"><span data-stu-id="ede57-125">application/json</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="ede57-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ede57-126">Request body</span></span>
<span data-ttu-id="ede57-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ede57-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ede57-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ede57-128">Response</span></span>

<span data-ttu-id="ede57-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ede57-129">If successful, this method returns a `200 OK` response code and a [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ede57-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ede57-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ede57-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ede57-131">Request</span></span>
<span data-ttu-id="ede57-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ede57-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_manager"
}-->
```http
GET https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/manager
```
##### <a name="response"></a><span data-ttu-id="ede57-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ede57-133">Response</span></span>
<span data-ttu-id="ede57-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ede57-134">Here is an example of the response.</span></span>
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
