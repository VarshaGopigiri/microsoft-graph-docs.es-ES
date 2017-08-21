# <a name="get-conversationthread"></a><span data-ttu-id="35aa3-101">Get conversationThread</span><span class="sxs-lookup"><span data-stu-id="35aa3-101">Get conversationThread</span></span>

<span data-ttu-id="35aa3-p101">Obtiene un hilo específico que pertenece a un grupo. Puede especificar la conversación primaria y el hilo, o bien, especificar el hilo sin hacer referencia a la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="35aa3-p101">Get a specific thread that belongs to a group. You can specify both the parent conversation and the thread, or, you can specify the thread without referencing the parent conversation.</span></span> 
## <a name="prerequisites"></a><span data-ttu-id="35aa3-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="35aa3-104">Prerequisites</span></span>
<span data-ttu-id="35aa3-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All; Group.Read.All*</span><span class="sxs-lookup"><span data-stu-id="35aa3-105">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All; Group.Read.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="35aa3-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="35aa3-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}
GET /groups/{id}/conversations/{id}/threads/{id}

```
## <a name="optional-query-parameters"></a><span data-ttu-id="35aa3-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="35aa3-107">Optional query parameters</span></span>
<span data-ttu-id="35aa3-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35aa3-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="35aa3-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="35aa3-109">Request headers</span></span>
| <span data-ttu-id="35aa3-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35aa3-110">Header</span></span>       | <span data-ttu-id="35aa3-111">Valor</span><span class="sxs-lookup"><span data-stu-id="35aa3-111">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="35aa3-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="35aa3-112">Authorization</span></span>  | <span data-ttu-id="35aa3-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="35aa3-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="35aa3-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="35aa3-115">Request body</span></span>
<span data-ttu-id="35aa3-116">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="35aa3-116">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="35aa3-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35aa3-117">Response</span></span>

<span data-ttu-id="35aa3-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [conversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35aa3-118">If successful, this method returns a `200 OK` response code and [conversationThread](../resources/conversationthread.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="35aa3-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="35aa3-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="35aa3-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="35aa3-120">Request</span></span>
<span data-ttu-id="35aa3-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="35aa3-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_conversationthread"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}
```
##### <a name="response"></a><span data-ttu-id="35aa3-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35aa3-122">Response</span></span>
<span data-ttu-id="35aa3-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="35aa3-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 419

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get conversationThread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
