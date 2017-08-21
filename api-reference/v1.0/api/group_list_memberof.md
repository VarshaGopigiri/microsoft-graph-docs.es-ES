# <a name="list-memberof"></a><span data-ttu-id="7910e-101">List memberOf</span><span class="sxs-lookup"><span data-stu-id="7910e-101">List memberOf</span></span>

<span data-ttu-id="7910e-102">Obtiene grupos de los que el grupo sea miembro directo.</span><span class="sxs-lookup"><span data-stu-id="7910e-102">Get groups that the group is a direct member of.</span></span> 

<span data-ttu-id="7910e-p101">Esta operación no es transitiva. A diferencia de la obtención de grupos de Office 365 de un usuario, devuelve todos los tipos de grupos, no solo los grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="7910e-p101">This operation is not transitive. Unlike getting a user's Office 365 Groups, this returns all types of groups, not just Office 365 groups.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="7910e-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7910e-105">Prerequisites</span></span>
<span data-ttu-id="7910e-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.Read.All*</span><span class="sxs-lookup"><span data-stu-id="7910e-106">One of the following **scopes** is required to execute this API: *Group.Read.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="7910e-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7910e-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/memberOf
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7910e-108">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7910e-108">Optional query parameters</span></span>
<span data-ttu-id="7910e-109">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7910e-109">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="7910e-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7910e-110">Request headers</span></span>
| <span data-ttu-id="7910e-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="7910e-111">Name</span></span>       | <span data-ttu-id="7910e-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="7910e-112">Type</span></span> | <span data-ttu-id="7910e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="7910e-113">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="7910e-114">Authorization</span><span class="sxs-lookup"><span data-stu-id="7910e-114">Authorization</span></span>  | <span data-ttu-id="7910e-115">string</span><span class="sxs-lookup"><span data-stu-id="7910e-115">string</span></span>  | <span data-ttu-id="7910e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7910e-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7910e-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7910e-118">Request body</span></span>
<span data-ttu-id="7910e-119">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7910e-119">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7910e-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7910e-120">Response</span></span>

<span data-ttu-id="7910e-121">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7910e-121">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7910e-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7910e-122">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7910e-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7910e-123">Request</span></span>
<span data-ttu-id="7910e-124">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7910e-124">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_memberof"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/memberOf
```
##### <a name="response"></a><span data-ttu-id="7910e-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7910e-125">Response</span></span>
<span data-ttu-id="7910e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7910e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List memberOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->