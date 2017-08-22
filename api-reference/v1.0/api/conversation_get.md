# <a name="get-conversation"></a><span data-ttu-id="e9e77-101">Get conversation</span><span class="sxs-lookup"><span data-stu-id="e9e77-101">Get conversation</span></span>

<span data-ttu-id="e9e77-102">Recupera las propiedades y relaciones del objeto conversation.</span><span class="sxs-lookup"><span data-stu-id="e9e77-102">Retrieve the properties and relationships of conversation object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e9e77-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e9e77-103">Prerequisites</span></span>
<span data-ttu-id="e9e77-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All; Group.Read.All*</span><span class="sxs-lookup"><span data-stu-id="e9e77-104">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All; Group.Read.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="e9e77-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9e77-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/conversations/{id}

```
## <a name="optional-query-parameters"></a><span data-ttu-id="e9e77-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e9e77-106">Optional query parameters</span></span>
<span data-ttu-id="e9e77-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9e77-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="e9e77-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9e77-108">Request headers</span></span>
| <span data-ttu-id="e9e77-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9e77-109">Header</span></span>       | <span data-ttu-id="e9e77-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e9e77-110">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e9e77-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="e9e77-111">Authorization</span></span>  | <span data-ttu-id="e9e77-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9e77-p101">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e9e77-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e9e77-114">Request body</span></span>
<span data-ttu-id="e9e77-115">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e9e77-115">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e9e77-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9e77-116">Response</span></span>

<span data-ttu-id="e9e77-117">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [conversation](../resources/conversation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9e77-117">If successful, this method returns a `200 OK` response code and [conversation](../resources/conversation.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e9e77-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9e77-118">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e9e77-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9e77-119">Request</span></span>
<span data-ttu-id="e9e77-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9e77-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_conversation"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/conversations/{id}
```
##### <a name="response"></a><span data-ttu-id="e9e77-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9e77-121">Response</span></span>
<span data-ttu-id="e9e77-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e9e77-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

{
  "topic": "topic-value",
  "hasAttachments": true,
  "lastDeliveredDateTime": "datetime-value",
  "uniqueSenders": [
    "uniqueSenders-value"
  ],
  "preview": "preview-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get conversation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
