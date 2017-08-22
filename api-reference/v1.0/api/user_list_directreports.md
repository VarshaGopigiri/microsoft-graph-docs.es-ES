# <a name="list-directreports"></a><span data-ttu-id="52d7e-101">List directReports</span><span class="sxs-lookup"><span data-stu-id="52d7e-101">List directReports</span></span>

<span data-ttu-id="52d7e-p101">Obtiene los subordinados directos del usuario. Devuelve los usuarios y los contactos para los que se asigna este usuario como administrador.</span><span class="sxs-lookup"><span data-stu-id="52d7e-p101">Get user's direct reports. Returns the users and contacts for whom this user is assigned as manager.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="52d7e-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="52d7e-104">Prerequisites</span></span>
<span data-ttu-id="52d7e-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *User.Read; User.ReadWrite; User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="52d7e-105">One of the following **scopes** is required to execute this API: *User.Read; User.ReadWrite; User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="52d7e-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52d7e-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/directReports
```
## <a name="optional-query-parameters"></a><span data-ttu-id="52d7e-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="52d7e-107">Optional query parameters</span></span>
<span data-ttu-id="52d7e-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52d7e-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="52d7e-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="52d7e-109">Request headers</span></span>
| <span data-ttu-id="52d7e-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52d7e-110">Header</span></span>       | <span data-ttu-id="52d7e-111">Valor</span><span class="sxs-lookup"><span data-stu-id="52d7e-111">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="52d7e-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="52d7e-112">Authorization</span></span>  | <span data-ttu-id="52d7e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="52d7e-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="52d7e-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="52d7e-115">Content-Type</span></span>   | <span data-ttu-id="52d7e-116">application/json</span><span class="sxs-lookup"><span data-stu-id="52d7e-116">application/json</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="52d7e-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="52d7e-117">Request body</span></span>
<span data-ttu-id="52d7e-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="52d7e-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="52d7e-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52d7e-119">Response</span></span>

<span data-ttu-id="52d7e-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52d7e-120">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="52d7e-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="52d7e-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="52d7e-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="52d7e-122">Request</span></span>
<span data-ttu-id="52d7e-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="52d7e-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directreports"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/directReports
```
##### <a name="response"></a><span data-ttu-id="52d7e-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52d7e-124">Response</span></span>
<span data-ttu-id="52d7e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="52d7e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
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