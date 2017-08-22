# <a name="get-photo"></a><span data-ttu-id="9e804-101">Get photo</span><span class="sxs-lookup"><span data-stu-id="9e804-101">Get photo</span></span>

<span data-ttu-id="9e804-102">Recupera las propiedades y las relaciones del objeto photo.</span><span class="sxs-lookup"><span data-stu-id="9e804-102">Retrieve the properties and relationships of photo object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9e804-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9e804-103">Prerequisites</span></span>
<span data-ttu-id="9e804-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="9e804-104">One of the following **scopes** is required to execute this API:</span></span>

  * <span data-ttu-id="9e804-105">Files.Read</span><span class="sxs-lookup"><span data-stu-id="9e804-105">Files.Read</span></span>

## <a name="http-request"></a><span data-ttu-id="9e804-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9e804-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/photo
GET /groups/{id}/photo
GET /drive/root/createdByUser/photo
```
## <a name="optional-query-parameters"></a><span data-ttu-id="9e804-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9e804-107">Optional query parameters</span></span>
<span data-ttu-id="9e804-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9e804-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9e804-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9e804-109">Request headers</span></span>
| <span data-ttu-id="9e804-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="9e804-110">Name</span></span>       | <span data-ttu-id="9e804-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="9e804-111">Type</span></span> | <span data-ttu-id="9e804-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e804-112">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="9e804-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="9e804-113">Authorization</span></span>  | <span data-ttu-id="9e804-114">string</span><span class="sxs-lookup"><span data-stu-id="9e804-114">string</span></span>  | <span data-ttu-id="9e804-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9e804-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9e804-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9e804-117">Request body</span></span>
<span data-ttu-id="9e804-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9e804-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9e804-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9e804-119">Response</span></span>

<span data-ttu-id="9e804-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [photo](../resources/photo.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9e804-120">If successful, this method returns a `200 OK` response code and [photo](../resources/photo.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9e804-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9e804-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9e804-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9e804-122">Request</span></span>
<span data-ttu-id="9e804-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9e804-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_photo"
}-->
```http
GET https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/photo
```
##### <a name="response"></a><span data-ttu-id="9e804-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9e804-124">Response</span></span>
<span data-ttu-id="9e804-125">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9e804-125">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.profilePhoto"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 53

{
  "height": 99,
  "width": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
