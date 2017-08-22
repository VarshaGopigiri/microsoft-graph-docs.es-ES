# <a name="list-contactfolders"></a><span data-ttu-id="aaed7-101">List contactFolders</span><span class="sxs-lookup"><span data-stu-id="aaed7-101">List contactFolders</span></span>

<span data-ttu-id="aaed7-102">Obtiene la colección de la carpeta de contactos predeterminada del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="aaed7-102">Get the contact folder collection in the default Contacts folder of the signed-in user.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="aaed7-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="aaed7-103">Prerequisites</span></span>
<span data-ttu-id="aaed7-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Contacts.Read; Contacts.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="aaed7-104">One of the following scopes is required to execute this API: Contacts.Read; Contacts.ReadWrite</span></span>
## <a name="http-request"></a><span data-ttu-id="aaed7-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aaed7-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/contactFolders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="aaed7-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="aaed7-106">Optional query parameters</span></span>
<span data-ttu-id="aaed7-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aaed7-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="aaed7-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aaed7-108">Request headers</span></span>
| <span data-ttu-id="aaed7-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aaed7-109">Header</span></span>       | <span data-ttu-id="aaed7-110">Valor</span><span class="sxs-lookup"><span data-stu-id="aaed7-110">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="aaed7-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="aaed7-111">Authorization</span></span>  | <span data-ttu-id="aaed7-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aaed7-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="aaed7-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="aaed7-114">Content-Type</span></span>   | <span data-ttu-id="aaed7-115">application/json</span><span class="sxs-lookup"><span data-stu-id="aaed7-115">application/json</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="aaed7-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aaed7-116">Request body</span></span>
<span data-ttu-id="aaed7-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="aaed7-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="aaed7-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aaed7-118">Response</span></span>

<span data-ttu-id="aaed7-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ContactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aaed7-119">If successful, this method returns a `200 OK` response code and collection of [ContactFolder](../resources/contactfolder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="aaed7-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aaed7-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="aaed7-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aaed7-121">Request</span></span>
<span data-ttu-id="aaed7-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aaed7-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contactfolders"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contactFolders
```
##### <a name="response"></a><span data-ttu-id="aaed7-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aaed7-123">Response</span></span>
<span data-ttu-id="aaed7-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aaed7-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contactFolder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 145

{
  "value": [
    {
      "parentFolderId": "parentFolderId-value",
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
  "description": "List contactFolders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
