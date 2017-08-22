# <a name="list-createdobjects"></a><span data-ttu-id="39407-101">List createdObjects</span><span class="sxs-lookup"><span data-stu-id="39407-101">List createdObjects</span></span>

<span data-ttu-id="39407-102">Obtiene una lista de objetos de directorio creados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="39407-102">Get a list of directory objects that were created by the user.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="39407-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="39407-103">Prerequisites</span></span>
<span data-ttu-id="39407-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *User.Read; User.ReadWrite; User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="39407-104">One of the following **scopes** is required to execute this API: *User.Read; User.ReadWrite; User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="39407-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="39407-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/createdObjects
```
## <a name="optional-query-parameters"></a><span data-ttu-id="39407-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="39407-106">Optional query parameters</span></span>
<span data-ttu-id="39407-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39407-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="39407-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="39407-108">Request headers</span></span>
| <span data-ttu-id="39407-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39407-109">Header</span></span>       | <span data-ttu-id="39407-110">Valor</span><span class="sxs-lookup"><span data-stu-id="39407-110">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="39407-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="39407-111">Authorization</span></span>  | <span data-ttu-id="39407-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="39407-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="39407-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="39407-114">Content-Type</span></span>  | <span data-ttu-id="39407-115">application/json</span><span class="sxs-lookup"><span data-stu-id="39407-115">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="39407-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="39407-116">Request body</span></span>
<span data-ttu-id="39407-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="39407-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="39407-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39407-118">Response</span></span>

<span data-ttu-id="39407-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39407-119">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="39407-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39407-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="39407-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="39407-121">Request</span></span>
<span data-ttu-id="39407-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39407-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_createdobjects"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/createdObjects
```
##### <a name="response"></a><span data-ttu-id="39407-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39407-123">Response</span></span>
<span data-ttu-id="39407-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="39407-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List createdObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->