# <a name="list-conversations"></a><span data-ttu-id="e7b6d-101">List conversations</span><span class="sxs-lookup"><span data-stu-id="e7b6d-101">List conversations</span></span>

<span data-ttu-id="e7b6d-102">Recupera la lista de conversaciones en este grupo.</span><span class="sxs-lookup"><span data-stu-id="e7b6d-102">Retrieve the list of conversations in this group.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e7b6d-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e7b6d-103">Prerequisites</span></span>
<span data-ttu-id="e7b6d-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.Read.All* o *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="e7b6d-104">One of the following **scopes** is required to execute this API: *Group.Read.All* or *Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="e7b6d-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e7b6d-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/conversations
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e7b6d-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e7b6d-106">Optional query parameters</span></span>
<span data-ttu-id="e7b6d-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e7b6d-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="e7b6d-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e7b6d-108">Request headers</span></span>
| <span data-ttu-id="e7b6d-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7b6d-109">Header</span></span>       | <span data-ttu-id="e7b6d-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e7b6d-110">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e7b6d-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="e7b6d-111">Authorization</span></span>  | <span data-ttu-id="e7b6d-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e7b6d-p101">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e7b6d-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e7b6d-114">Request body</span></span>
<span data-ttu-id="e7b6d-115">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e7b6d-115">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e7b6d-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7b6d-116">Response</span></span>

<span data-ttu-id="e7b6d-117">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Conversation](../resources/conversation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e7b6d-117">If successful, this method returns a `200 OK` response code and collection of [Conversation](../resources/conversation.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e7b6d-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e7b6d-118">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e7b6d-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e7b6d-119">Request</span></span>
<span data-ttu-id="e7b6d-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e7b6d-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_conversations"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/conversations
```
##### <a name="response"></a><span data-ttu-id="e7b6d-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7b6d-121">Response</span></span>
<span data-ttu-id="e7b6d-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e7b6d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 262

{
  "value": [
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List conversations",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->