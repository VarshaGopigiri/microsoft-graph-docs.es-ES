# <a name="list-attachments"></a><span data-ttu-id="9ebb9-101">List attachments</span><span class="sxs-lookup"><span data-stu-id="9ebb9-101">List attachments</span></span>

<span data-ttu-id="9ebb9-102">Recupera una lista de objetos attachment.</span><span class="sxs-lookup"><span data-stu-id="9ebb9-102">Retrieve a list of attachment objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9ebb9-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9ebb9-103">Prerequisites</span></span>
<span data-ttu-id="9ebb9-104">Se requieren los siguientes **ámbitos** para ejecutar esta API: _Mail.Read_</span><span class="sxs-lookup"><span data-stu-id="9ebb9-104">The following **scopes** are required to execute this API: _Mail.Read_</span></span>
## <a name="http-request"></a><span data-ttu-id="9ebb9-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9ebb9-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}/attachments
GET /users/{id | userPrincipalName}/messages/{id}/attachments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="9ebb9-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9ebb9-106">Optional query parameters</span></span>
<span data-ttu-id="9ebb9-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ebb9-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9ebb9-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9ebb9-108">Request headers</span></span>
| <span data-ttu-id="9ebb9-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="9ebb9-109">Name</span></span>       | <span data-ttu-id="9ebb9-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="9ebb9-110">Type</span></span> | <span data-ttu-id="9ebb9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ebb9-111">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="9ebb9-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="9ebb9-112">Authorization</span></span>  | <span data-ttu-id="9ebb9-113">string</span><span class="sxs-lookup"><span data-stu-id="9ebb9-113">string</span></span>  | <span data-ttu-id="9ebb9-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9ebb9-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9ebb9-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9ebb9-116">Request body</span></span>
<span data-ttu-id="9ebb9-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9ebb9-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9ebb9-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ebb9-118">Response</span></span>

<span data-ttu-id="9ebb9-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ebb9-119">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9ebb9-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ebb9-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9ebb9-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9ebb9-121">Request</span></span>
<span data-ttu-id="9ebb9-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ebb9-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="9ebb9-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ebb9-123">Response</span></span>
<span data-ttu-id="9ebb9-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9ebb9-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "value": [
    {
      "@odata.type": "#Microsoft.OutlookServices.FileAttachment",
      "contentType": "contentType-value",
      "contentLocation": "contentLocation-value",
      "contentBytes": "contentBytes-value",
      "contentId": "null",
      "lastModifiedDateTime": "datetime-value",
      "id": "id-value",
      "isInline": false,
      "isContactPhoto": false,
      "name": "name-value",
      "size": 99
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List attachments",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
