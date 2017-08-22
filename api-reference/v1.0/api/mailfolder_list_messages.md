# <a name="list-messages"></a><span data-ttu-id="27f33-101">List messages</span><span class="sxs-lookup"><span data-stu-id="27f33-101">List messages</span></span>

<span data-ttu-id="27f33-102">Obtiene todos los mensajes en el buzón del usuario que inició sesión o esos mensajes en una carpeta especificada en el buzón.</span><span class="sxs-lookup"><span data-stu-id="27f33-102">Get all the messages in the signed-in user's mailbox, or those messages in a specified folder in the mailbox.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="27f33-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="27f33-103">Prerequisites</span></span>
<span data-ttu-id="27f33-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.Read; Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="27f33-104">One of the following scopes is required to execute this API: Mail.Read; Mail.ReadWrite</span></span>
## <a name="http-request"></a><span data-ttu-id="27f33-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="27f33-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/messages
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages
```
## <a name="optional-query-parameters"></a><span data-ttu-id="27f33-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="27f33-106">Optional query parameters</span></span>
<span data-ttu-id="27f33-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27f33-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="27f33-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="27f33-108">Request headers</span></span>
| <span data-ttu-id="27f33-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="27f33-109">Name</span></span>       | <span data-ttu-id="27f33-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="27f33-110">Type</span></span> | <span data-ttu-id="27f33-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="27f33-111">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="27f33-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="27f33-112">Authorization</span></span>  | <span data-ttu-id="27f33-113">string</span><span class="sxs-lookup"><span data-stu-id="27f33-113">string</span></span>  | <span data-ttu-id="27f33-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="27f33-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="27f33-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="27f33-116">Request body</span></span>
<span data-ttu-id="27f33-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="27f33-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="27f33-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27f33-118">Response</span></span>

<span data-ttu-id="27f33-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27f33-119">If successful, this method returns a `200 OK` response code and collection of [Message](../resources/message.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="27f33-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="27f33-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="27f33-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="27f33-121">Request</span></span>
<span data-ttu-id="27f33-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="27f33-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_messages"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/{id}/messages
```
##### <a name="response"></a><span data-ttu-id="27f33-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27f33-123">Response</span></span>
<span data-ttu-id="27f33-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="27f33-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 317

{
  "value": [
    {
      "receivedDateTime": "datetime-value",
      "sentDateTime": "datetime-value",
      "hasAttachments": true,
      "subject": "subject-value",
      "body": {
        "contentType": "",
        "content": "content-value"
      },
      "bodyPreview": "bodyPreview-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List messages",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
