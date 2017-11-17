# <a name="list-registeredusers"></a><span data-ttu-id="522ac-101">List registeredUsers</span><span class="sxs-lookup"><span data-stu-id="522ac-101">List registeredUsers</span></span>

<span data-ttu-id="522ac-102">Recuperar una lista de usuarios que son usuarios registrados del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="522ac-102">Retrieve a list of users that are registered users of the device.</span></span>
## <a name="permissions"></a><span data-ttu-id="522ac-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="522ac-103">Permissions</span></span>
<span data-ttu-id="522ac-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="522ac-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

- <span data-ttu-id="522ac-106">Device.ReadWrite.All y User.ReadBasic.All</span><span class="sxs-lookup"><span data-stu-id="522ac-106">Device.ReadWrite.All and User.ReadBasic.All</span></span>
- <span data-ttu-id="522ac-107">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="522ac-107">Directory.Read.All</span></span>
- <span data-ttu-id="522ac-108">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="522ac-108">Directory.ReadWrite.All</span></span> 
- <span data-ttu-id="522ac-109">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="522ac-109">Directory.AccessAsUser.All</span></span>

## <a name="http-request"></a><span data-ttu-id="522ac-110">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="522ac-110">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}/registeredUsers
```
## <a name="optional-query-parameters"></a><span data-ttu-id="522ac-111">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="522ac-111">Optional query parameters</span></span>
<span data-ttu-id="522ac-112">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="522ac-112">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="522ac-113">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="522ac-113">Request headers</span></span>
| <span data-ttu-id="522ac-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="522ac-114">Name</span></span>       | <span data-ttu-id="522ac-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="522ac-115">Type</span></span> | <span data-ttu-id="522ac-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="522ac-116">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="522ac-117">Authorization</span><span class="sxs-lookup"><span data-stu-id="522ac-117">Authorization</span></span>  | <span data-ttu-id="522ac-118">string</span><span class="sxs-lookup"><span data-stu-id="522ac-118">string</span></span>  | <span data-ttu-id="522ac-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="522ac-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="522ac-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="522ac-121">Request body</span></span>
<span data-ttu-id="522ac-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="522ac-122">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="522ac-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="522ac-123">Response</span></span>

<span data-ttu-id="522ac-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="522ac-124">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="522ac-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="522ac-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="522ac-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="522ac-126">Request</span></span>
<span data-ttu-id="522ac-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="522ac-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_registeredusers"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices/{id}/registeredUsers
```
##### <a name="response"></a><span data-ttu-id="522ac-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="522ac-128">Response</span></span>
<span data-ttu-id="522ac-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="522ac-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List registeredUsers",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->