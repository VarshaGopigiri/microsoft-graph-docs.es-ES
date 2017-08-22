# <a name="list-threads"></a><span data-ttu-id="e6a4b-101">List threads</span><span class="sxs-lookup"><span data-stu-id="e6a4b-101">List threads</span></span>

<span data-ttu-id="e6a4b-102">Obtiene todos los hilos de un grupo.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-102">Get all the threads of a group.</span></span>

<span data-ttu-id="e6a4b-103">Nota: También puede [obtener todos los hilos de una conversación](conversation_list_threads.md).</span><span class="sxs-lookup"><span data-stu-id="e6a4b-103">Note: You can also [get all the threads of a conversation](conversation_list_threads.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e6a4b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e6a4b-104">Prerequisites</span></span>
<span data-ttu-id="e6a4b-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:  *Group.Read.All* o *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="e6a4b-105">One of the following **scopes** is required to execute this API: *Group.Read.All* or *Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="e6a4b-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6a4b-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e6a4b-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e6a4b-107">Optional query parameters</span></span>
<span data-ttu-id="e6a4b-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="e6a4b-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6a4b-109">Request headers</span></span>
| <span data-ttu-id="e6a4b-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6a4b-110">Header</span></span>       | <span data-ttu-id="e6a4b-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e6a4b-111">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e6a4b-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="e6a4b-112">Authorization</span></span>  | <span data-ttu-id="e6a4b-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-p101">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e6a4b-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e6a4b-115">Request body</span></span>
<span data-ttu-id="e6a4b-116">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-116">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e6a4b-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6a4b-117">Response</span></span>

<span data-ttu-id="e6a4b-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ConversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-118">If successful, this method returns a `200 OK` response code and collection of [ConversationThread](../resources/conversationthread.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e6a4b-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6a4b-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e6a4b-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6a4b-120">Request</span></span>
<span data-ttu-id="e6a4b-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_threads"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/threads
```
##### <a name="response"></a><span data-ttu-id="e6a4b-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6a4b-122">Response</span></span>
<span data-ttu-id="e6a4b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 536

{
  "value": [
    {
      "toRecipients": [
        {
          "emailAddress": {
            "name": "name-value",
            "address": "address-value"
          }
        }
      ],
      "topic": "topic-value",
      "hasAttachments": true,
      "lastDeliveredDateTime": "datetime-value",
      "uniqueSenders": [
        "uniqueSenders-value"
      ],
      "ccRecipients": [
        {
          "emailAddress": {
            "name": "name-value",
            "address": "address-value"
          }
        }
      ]
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List threads",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
