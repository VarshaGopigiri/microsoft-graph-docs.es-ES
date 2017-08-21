# <a name="list-messages"></a><span data-ttu-id="f5dec-101">Enumerar mensajes</span><span class="sxs-lookup"><span data-stu-id="f5dec-101">List messages</span></span>

<span data-ttu-id="f5dec-102">Obtenga los mensajes del buzón del usuario que ha iniciado sesión (incluidas las carpetas Elementos eliminados y Otros correos).</span><span class="sxs-lookup"><span data-stu-id="f5dec-102">Get the messages in the signed-in user's mailbox (including the Deleted Items and Clutter folders).</span></span>

<span data-ttu-id="f5dec-103">Actualmente, esta operación devuelve los cuerpos de los mensajes solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="f5dec-103">Currently, this operation returns message bodies in only HTML format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f5dec-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f5dec-104">Prerequisites</span></span>
<span data-ttu-id="f5dec-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.Read; Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="f5dec-105">One of the following scopes is required to execute this API: Mail.Read; Mail.ReadWrite</span></span>
## <a name="http-request"></a><span data-ttu-id="f5dec-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f5dec-106">HTTP request</span></span>

<span data-ttu-id="f5dec-107">Para obtener todos los mensajes del buzón de un usuario:</span><span class="sxs-lookup"><span data-stu-id="f5dec-107">To get all the messages in a user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/messages
GET /users/{id | userPrincipalName}/messages
```

<span data-ttu-id="f5dec-108">Para obtener los mensajes de una carpeta específica del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="f5dec-108">To get messages in a specific folder in the user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/messages
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f5dec-109">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f5dec-109">Optional query parameters</span></span>
<span data-ttu-id="f5dec-110">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5dec-110">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f5dec-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f5dec-111">Request headers</span></span>
| <span data-ttu-id="f5dec-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5dec-112">Header</span></span>       | <span data-ttu-id="f5dec-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f5dec-113">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="f5dec-114">Authorization</span><span class="sxs-lookup"><span data-stu-id="f5dec-114">Authorization</span></span>  | <span data-ttu-id="f5dec-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f5dec-p101">Bearer {token}. Required.</span></span>  |
 

## <a name="request-body"></a><span data-ttu-id="f5dec-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f5dec-117">Request body</span></span>
<span data-ttu-id="f5dec-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f5dec-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f5dec-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5dec-119">Response</span></span>

<span data-ttu-id="f5dec-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5dec-120">If successful, this method returns a `200 OK` response code and collection of [Message](../resources/message.md) objects in the response body.</span></span>

<span data-ttu-id="f5dec-121">El tamaño de página predeterminada para esta solicitud es de 10 mensajes.</span><span class="sxs-lookup"><span data-stu-id="f5dec-121">The default page size for this request is 10 messages.</span></span>

## <a name="example"></a><span data-ttu-id="f5dec-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5dec-122">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f5dec-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f5dec-123">Request</span></span>
<span data-ttu-id="f5dec-124">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f5dec-124">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_messages"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages
```
##### <a name="response"></a><span data-ttu-id="f5dec-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5dec-125">Response</span></span>
<span data-ttu-id="f5dec-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f5dec-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
