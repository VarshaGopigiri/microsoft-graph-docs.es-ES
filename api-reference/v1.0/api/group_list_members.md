# <a name="list-members"></a><span data-ttu-id="70e31-101">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="70e31-101">List members</span></span>

<span data-ttu-id="70e31-p101">Obtiene una lista de los miembros directos del grupo. Un grupo puede tener usuarios, contactos y otros grupos como miembros. Esta operación no es transitiva.</span><span class="sxs-lookup"><span data-stu-id="70e31-p101">Get a list of the group's direct members. A group can have users, contacts, and other groups as members. This operation is not transitive.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="70e31-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="70e31-105">Prerequisites</span></span>
<span data-ttu-id="70e31-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All*, *Directory.AccessAsUser.All*, *User.ReadBasic.All* o *User.Read.All*</span><span class="sxs-lookup"><span data-stu-id="70e31-106">One of the following **scopes** is required to execute this API: *Directory.Read.All*, *Directory.AccessAsUser.All*, *User.ReadBasic.All*, or *User.Read.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="70e31-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="70e31-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/members
```
## <a name="optional-query-parameters"></a><span data-ttu-id="70e31-108">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="70e31-108">Optional query parameters</span></span>
<span data-ttu-id="70e31-109">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70e31-109">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="70e31-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="70e31-110">Request headers</span></span>
| <span data-ttu-id="70e31-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="70e31-111">Name</span></span>       | <span data-ttu-id="70e31-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="70e31-112">Type</span></span> | <span data-ttu-id="70e31-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="70e31-113">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="70e31-114">Authorization</span><span class="sxs-lookup"><span data-stu-id="70e31-114">Authorization</span></span>  | <span data-ttu-id="70e31-115">string</span><span class="sxs-lookup"><span data-stu-id="70e31-115">string</span></span>  | <span data-ttu-id="70e31-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="70e31-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="70e31-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="70e31-118">Request body</span></span>
<span data-ttu-id="70e31-119">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="70e31-119">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="70e31-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70e31-120">Response</span></span>

<span data-ttu-id="70e31-121">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70e31-121">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="70e31-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="70e31-122">Example</span></span>
##### <a name="request"></a><span data-ttu-id="70e31-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="70e31-123">Request</span></span>
<span data-ttu-id="70e31-124">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="70e31-124">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_members"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/members
```
##### <a name="response"></a><span data-ttu-id="70e31-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70e31-125">Response</span></span>
<span data-ttu-id="70e31-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="70e31-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List members",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->