# <a name="list-directoryroletemplates"></a><span data-ttu-id="a6851-101">List directoryRoleTemplates</span><span class="sxs-lookup"><span data-stu-id="a6851-101">List directoryRoleTemplates</span></span>

<span data-ttu-id="a6851-102">Recupera una lista de objetos directoryRoleTemplate.</span><span class="sxs-lookup"><span data-stu-id="a6851-102">Retrieve a list of directoryRoleTemplate objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a6851-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a6851-103">Prerequisites</span></span>
<span data-ttu-id="a6851-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All*, *Directory.ReadWrite.All* O *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="a6851-104">One of the following **scopes** is required to execute this API: *Directory.Read.All* or *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="a6851-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a6851-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoleTemplates
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a6851-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a6851-106">Optional query parameters</span></span>
<span data-ttu-id="a6851-107">Este método **no** es compatible con los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="a6851-107">This method does **not** support the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="a6851-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a6851-108">Request headers</span></span>
| <span data-ttu-id="a6851-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="a6851-109">Name</span></span>       | <span data-ttu-id="a6851-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6851-110">Type</span></span> | <span data-ttu-id="a6851-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6851-111">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="a6851-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="a6851-112">Authorization</span></span>  | <span data-ttu-id="a6851-113">string</span><span class="sxs-lookup"><span data-stu-id="a6851-113">string</span></span>  | <span data-ttu-id="a6851-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a6851-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a6851-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a6851-116">Request body</span></span>
<span data-ttu-id="a6851-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a6851-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a6851-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6851-118">Response</span></span>

<span data-ttu-id="a6851-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryRoleTemplate](../resources/directoryroletemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6851-119">If successful, this method returns a `200 OK` response code and collection of [directoryRoleTemplate](../resources/directoryroletemplate.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a6851-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a6851-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a6851-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a6851-121">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_directoryroletemplates"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryRoleTemplates
```
##### <a name="response"></a><span data-ttu-id="a6851-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6851-122">Response</span></span>
<span data-ttu-id="a6851-p102">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a6851-p102">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRoleTemplate",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "description": "description-value",
      "displayName": "displayName-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List directoryRoleTemplates",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
