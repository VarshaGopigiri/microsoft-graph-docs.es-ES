# <a name="list-directoryroles"></a><span data-ttu-id="7326d-101">List directoryRoles</span><span class="sxs-lookup"><span data-stu-id="7326d-101">List directoryRoles</span></span>

<span data-ttu-id="7326d-102">Enumera los roles de directorio que están activados en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="7326d-102">List the directory roles that are activated in the tenant.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7326d-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7326d-103">Prerequisites</span></span>
<span data-ttu-id="7326d-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="7326d-104">One of the following **scopes** is required to execute this API: *Directory.Read.All* or *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="7326d-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7326d-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7326d-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7326d-106">Optional query parameters</span></span>
<span data-ttu-id="7326d-107">Este método **no** es compatible con los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="7326d-107">This method does **not** support the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="7326d-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7326d-108">Request headers</span></span>
| <span data-ttu-id="7326d-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="7326d-109">Name</span></span>       | <span data-ttu-id="7326d-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="7326d-110">Type</span></span> | <span data-ttu-id="7326d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7326d-111">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="7326d-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="7326d-112">Authorization</span></span>  | <span data-ttu-id="7326d-113">string</span><span class="sxs-lookup"><span data-stu-id="7326d-113">string</span></span>  | <span data-ttu-id="7326d-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7326d-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7326d-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7326d-116">Request body</span></span>
<span data-ttu-id="7326d-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7326d-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7326d-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7326d-118">Response</span></span>

<span data-ttu-id="7326d-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7326d-119">If successful, this method returns a `200 OK` response code and collection of [directoryRole](../resources/directoryrole.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7326d-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7326d-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7326d-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7326d-121">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_directoryroles"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryRoles
```
##### <a name="response"></a><span data-ttu-id="7326d-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7326d-122">Response</span></span>
<span data-ttu-id="7326d-p102">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7326d-p102">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRole",
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
      "roleTemplateId": "roleTemplateId-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List directoryRoles",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
