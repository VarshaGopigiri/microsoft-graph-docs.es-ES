# <a name="list-ownedobjects"></a><span data-ttu-id="fe513-101">List ownedObjects</span><span class="sxs-lookup"><span data-stu-id="fe513-101">List ownedObjects</span></span>

<span data-ttu-id="fe513-102">Obtiene la lista de objetos de directorio que son propiedad del usuario.</span><span class="sxs-lookup"><span data-stu-id="fe513-102">Get the list of directory objects that are owned by the user.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fe513-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fe513-103">Prerequisites</span></span>
<span data-ttu-id="fe513-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="fe513-104">One of the following **scopes** is required to execute this API: *User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="fe513-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fe513-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/ownedObjects
```
## <a name="optional-query-parameters"></a><span data-ttu-id="fe513-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="fe513-106">Optional query parameters</span></span>
<span data-ttu-id="fe513-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe513-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="fe513-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fe513-108">Request headers</span></span>
| <span data-ttu-id="fe513-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe513-109">Header</span></span>       | <span data-ttu-id="fe513-110">Valor</span><span class="sxs-lookup"><span data-stu-id="fe513-110">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="fe513-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="fe513-111">Authorization</span></span>  | <span data-ttu-id="fe513-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fe513-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="fe513-114">Aceptar</span><span class="sxs-lookup"><span data-stu-id="fe513-114">Accept</span></span>  | <span data-ttu-id="fe513-115">application/json</span><span class="sxs-lookup"><span data-stu-id="fe513-115">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fe513-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fe513-116">Request body</span></span>
<span data-ttu-id="fe513-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fe513-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fe513-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe513-118">Response</span></span>

<span data-ttu-id="fe513-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe513-119">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="fe513-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe513-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fe513-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fe513-121">Request</span></span>
<span data-ttu-id="fe513-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fe513-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_ownedobjects"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/ownedObjects
```
##### <a name="response"></a><span data-ttu-id="fe513-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe513-123">Response</span></span>
<span data-ttu-id="fe513-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fe513-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List ownedObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->