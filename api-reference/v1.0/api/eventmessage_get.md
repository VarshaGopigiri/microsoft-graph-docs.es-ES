# <a name="get-eventmessage"></a><span data-ttu-id="c5c8c-101">Get eventMessage</span><span class="sxs-lookup"><span data-stu-id="c5c8c-101">Get eventMessage</span></span>

<span data-ttu-id="c5c8c-102">Recupera las propiedades y relaciones del objeto [eventMessage](../resources/eventmessage.md).</span><span class="sxs-lookup"><span data-stu-id="c5c8c-102">Retrieve the properties and relationships of [eventMessage](../resources/eventmessage.md) object.</span></span>

<span data-ttu-id="c5c8c-103">Actualmente, esta operación devuelve los cuerpos de los mensajes de evento solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-103">Currently, this operation returns event message bodies in only HTML format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c5c8c-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c5c8c-104">Prerequisites</span></span>
<span data-ttu-id="c5c8c-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.Read*</span><span class="sxs-lookup"><span data-stu-id="c5c8c-105">One of the following **scopes** is required to execute this API: *Mail.Read*</span></span>
## <a name="http-request"></a><span data-ttu-id="c5c8c-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c5c8c-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}
GET /users/{id | userPrincipalName}/messages/{id}

GET /me/mailFolders/{id}/messages/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c5c8c-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c5c8c-107">Optional query parameters</span></span>
<span data-ttu-id="c5c8c-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c5c8c-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c5c8c-109">Request headers</span></span>
| <span data-ttu-id="c5c8c-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="c5c8c-110">Name</span></span>       | <span data-ttu-id="c5c8c-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5c8c-111">Type</span></span> | <span data-ttu-id="c5c8c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5c8c-112">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="c5c8c-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="c5c8c-113">Authorization</span></span>  | <span data-ttu-id="c5c8c-114">string</span><span class="sxs-lookup"><span data-stu-id="c5c8c-114">string</span></span>  | <span data-ttu-id="c5c8c-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c5c8c-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c5c8c-117">Request body</span></span>
<span data-ttu-id="c5c8c-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c5c8c-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5c8c-119">Response</span></span>

<span data-ttu-id="c5c8c-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [eventMessage](../resources/eventmessage.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-120">If successful, this method returns a `200 OK` response code and [eventMessage](../resources/eventmessage.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c5c8c-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c5c8c-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c5c8c-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c5c8c-122">Request</span></span>
<span data-ttu-id="c5c8c-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_eventmessage"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="c5c8c-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5c8c-124">Response</span></span>
<span data-ttu-id="c5c8c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.eventmessage"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "html",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value",
  "meetingMessageType": "meetingMessageType-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get eventMessage",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
