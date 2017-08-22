# <a name="list-mailfolders"></a><span data-ttu-id="fca8f-101">List mailFolders</span><span class="sxs-lookup"><span data-stu-id="fca8f-101">List mailFolders</span></span>

<span data-ttu-id="fca8f-102">Obtiene la colección de carpetas de correo en la carpeta raíz del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="fca8f-102">Get the mail folder collection under the root folder of the signed-in user.</span></span> 
## <a name="prerequisites"></a><span data-ttu-id="fca8f-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fca8f-103">Prerequisites</span></span>
<span data-ttu-id="fca8f-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.Read; Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="fca8f-104">One of the following scopes is required to execute this API: Mail.Read; Mail.ReadWrite</span></span>
## <a name="http-request"></a><span data-ttu-id="fca8f-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fca8f-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/mailFolders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="fca8f-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="fca8f-106">Optional query parameters</span></span>
<span data-ttu-id="fca8f-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fca8f-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="fca8f-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fca8f-108">Request headers</span></span>
| <span data-ttu-id="fca8f-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fca8f-109">Header</span></span>       | <span data-ttu-id="fca8f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="fca8f-110">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="fca8f-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="fca8f-111">Authorization</span></span>  | <span data-ttu-id="fca8f-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fca8f-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="fca8f-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="fca8f-114">Content-Type</span></span>   | <span data-ttu-id="fca8f-115">application/json</span><span class="sxs-lookup"><span data-stu-id="fca8f-115">application/json</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="fca8f-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fca8f-116">Request body</span></span>
<span data-ttu-id="fca8f-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fca8f-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fca8f-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fca8f-118">Response</span></span>

<span data-ttu-id="fca8f-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fca8f-119">If successful, this method returns a `200 OK` response code and collection of [MailFolder](../resources/mailfolder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="fca8f-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fca8f-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fca8f-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fca8f-121">Request</span></span>
<span data-ttu-id="fca8f-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fca8f-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailfolders"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders
```
##### <a name="response"></a><span data-ttu-id="fca8f-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fca8f-123">Response</span></span>
<span data-ttu-id="fca8f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fca8f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List mailFolders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
