# <a name="list-owners"></a><span data-ttu-id="30d2d-101">Enumerar propietarios</span><span class="sxs-lookup"><span data-stu-id="30d2d-101">List owners</span></span>

<span data-ttu-id="30d2d-p101">Recupera una lista de propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="30d2d-p101">Retrieve a list of the group's owners. The owners are a set of non-admin users who are allowed to modify the group object.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="30d2d-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="30d2d-104">Prerequisites</span></span>
<span data-ttu-id="30d2d-105">Se requieren los siguientes **ámbitos** para ejecutar esta API: *Group.Read.All* y uno de *User.ReadBasic.All* o *User.Read.All* o *User.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="30d2d-105">The following **scopes** are required to execute this API: *Group.Read.All* and one of *User.ReadBasic.All* or *User.Read.All* or *User.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="30d2d-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="30d2d-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/owners
```
## <a name="optional-query-parameters"></a><span data-ttu-id="30d2d-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="30d2d-107">Optional query parameters</span></span>
<span data-ttu-id="30d2d-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30d2d-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="30d2d-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="30d2d-109">Request headers</span></span>
| <span data-ttu-id="30d2d-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="30d2d-110">Name</span></span>       | <span data-ttu-id="30d2d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="30d2d-111">Type</span></span> | <span data-ttu-id="30d2d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="30d2d-112">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="30d2d-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="30d2d-113">Authorization</span></span>  | <span data-ttu-id="30d2d-114">string</span><span class="sxs-lookup"><span data-stu-id="30d2d-114">string</span></span>  | <span data-ttu-id="30d2d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="30d2d-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="30d2d-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="30d2d-117">Request body</span></span>
<span data-ttu-id="30d2d-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="30d2d-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="30d2d-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30d2d-119">Response</span></span>

<span data-ttu-id="30d2d-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30d2d-120">If successful, this method returns a `200 OK` response code and collection of [user](../resources/user.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="30d2d-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30d2d-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="30d2d-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="30d2d-122">Request</span></span>
<span data-ttu-id="30d2d-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="30d2d-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_owners"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/owners
```
##### <a name="response"></a><span data-ttu-id="30d2d-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30d2d-124">Response</span></span>
<span data-ttu-id="30d2d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="30d2d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "@odata.type": "#microsoft.graph.user"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List owners",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
