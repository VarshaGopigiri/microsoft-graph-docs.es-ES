# <a name="list-registeredowners"></a><span data-ttu-id="b9f83-101">List registeredOwners</span><span class="sxs-lookup"><span data-stu-id="b9f83-101">List registeredOwners</span></span>

<span data-ttu-id="b9f83-102">Recupera una lista de usuarios que son propietarios registrados del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9f83-102">Retrieve a list of users that are registered owners of the device.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b9f83-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b9f83-103">Prerequisites</span></span>
<span data-ttu-id="b9f83-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="b9f83-104">One of the following **scopes** is required to execute this API:</span></span> 
- <span data-ttu-id="b9f83-105">*Device.ReadWrite.All* y *User.ReadBasic.All*</span><span class="sxs-lookup"><span data-stu-id="b9f83-105">*Device.ReadWrite.All* and *User.ReadBasic.All*</span></span>
- <span data-ttu-id="b9f83-106">*Directory.Read.All*</span><span class="sxs-lookup"><span data-stu-id="b9f83-106">*Directory.Read.All*</span></span>
- <span data-ttu-id="b9f83-107">*Directory.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="b9f83-107">*Directory.ReadWrite.All*</span></span> 
- <span data-ttu-id="b9f83-108">*Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="b9f83-108">*Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="b9f83-109">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b9f83-109">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}/registeredOwners
```
## <a name="optional-query-parameters"></a><span data-ttu-id="b9f83-110">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b9f83-110">Optional query parameters</span></span>
<span data-ttu-id="b9f83-111">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9f83-111">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="b9f83-112">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b9f83-112">Request headers</span></span>
| <span data-ttu-id="b9f83-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="b9f83-113">Name</span></span>       | <span data-ttu-id="b9f83-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9f83-114">Type</span></span> | <span data-ttu-id="b9f83-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9f83-115">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="b9f83-116">Authorization</span><span class="sxs-lookup"><span data-stu-id="b9f83-116">Authorization</span></span>  | <span data-ttu-id="b9f83-117">string</span><span class="sxs-lookup"><span data-stu-id="b9f83-117">string</span></span>  | <span data-ttu-id="b9f83-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9f83-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b9f83-120">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b9f83-120">Request body</span></span>
<span data-ttu-id="b9f83-121">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b9f83-121">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b9f83-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9f83-122">Response</span></span>

<span data-ttu-id="b9f83-123">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9f83-123">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b9f83-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9f83-124">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b9f83-125">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b9f83-125">Request</span></span>
<span data-ttu-id="b9f83-126">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b9f83-126">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_registeredowners"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices/{id}/registeredOwners
```
##### <a name="response"></a><span data-ttu-id="b9f83-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9f83-127">Response</span></span>
<span data-ttu-id="b9f83-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b9f83-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List registeredOwners",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->