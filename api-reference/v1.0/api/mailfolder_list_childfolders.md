# <a name="list-childfolders"></a><span data-ttu-id="a47d6-101">List childFolders</span><span class="sxs-lookup"><span data-stu-id="a47d6-101">List childFolders</span></span>

<span data-ttu-id="a47d6-p101">Obtiene la colección de carpetas en la carpeta especificada. Puede usar el acceso directo de `.../me/MailFolders` para obtener la colección de carpetas de nivel superior y navegar a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="a47d6-p101">Get the folder collection under the specified folder. You can use the `.../me/MailFolders` shortcut to get the top-level folder collection and navigate to another folder.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a47d6-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a47d6-104">Prerequisites</span></span>
<span data-ttu-id="a47d6-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.Read; Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="a47d6-105">One of the following scopes is required to execute this API: Mail.Read; Mail.ReadWrite</span></span>
## <a name="http-request"></a><span data-ttu-id="a47d6-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a47d6-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/childFolders
GET /users/{id | userPrincipalName}/mailFolders/{id}/childFolders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a47d6-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a47d6-107">Optional query parameters</span></span>
<span data-ttu-id="a47d6-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a47d6-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="a47d6-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a47d6-109">Request headers</span></span>
| <span data-ttu-id="a47d6-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="a47d6-110">Name</span></span>       | <span data-ttu-id="a47d6-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="a47d6-111">Type</span></span> | <span data-ttu-id="a47d6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a47d6-112">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="a47d6-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="a47d6-113">Authorization</span></span>  | <span data-ttu-id="a47d6-114">string</span><span class="sxs-lookup"><span data-stu-id="a47d6-114">string</span></span>  | <span data-ttu-id="a47d6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a47d6-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a47d6-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a47d6-117">Request body</span></span>
<span data-ttu-id="a47d6-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a47d6-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a47d6-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a47d6-119">Response</span></span>

<span data-ttu-id="a47d6-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a47d6-120">If successful, this method returns a `200 OK` response code and collection of [MailFolder](../resources/mailfolder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a47d6-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a47d6-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a47d6-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a47d6-122">Request</span></span>
<span data-ttu-id="a47d6-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a47d6-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_childfolders"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/{id}/childFolders
```
##### <a name="response"></a><span data-ttu-id="a47d6-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a47d6-124">Response</span></span>
<span data-ttu-id="a47d6-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a47d6-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 232

{
  "value": [
    {
      "displayName": "displayName-value",
      "parentFolderId": "parentFolderId-value",
      "childFolderCount": 99,
      "unreadItemCount": 99,
      "totalItemCount": 99,
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List childFolders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
