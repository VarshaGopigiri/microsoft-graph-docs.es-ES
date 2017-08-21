# <a name="message-move"></a><span data-ttu-id="2d154-101">message: move</span><span class="sxs-lookup"><span data-stu-id="2d154-101">message: move</span></span>

<span data-ttu-id="2d154-p101">Mueve un mensaje a una carpeta. Se crea una nueva copia del mensaje en la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="2d154-p101">Move a message to a folder. This creates a new copy of the message in the destination folder.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2d154-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2d154-104">Prerequisites</span></span>
<span data-ttu-id="2d154-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="2d154-105">One of the following **scopes** is required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="2d154-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2d154-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/move
POST /users/{id | userPrincipalName}/messages/{id}/move
POST /me/mailFolders/{id}/messages/{id}/move
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/move
```
## <a name="request-headers"></a><span data-ttu-id="2d154-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2d154-107">Request headers</span></span>
| <span data-ttu-id="2d154-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="2d154-108">Name</span></span>       | <span data-ttu-id="2d154-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d154-109">Type</span></span> | <span data-ttu-id="2d154-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d154-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="2d154-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="2d154-111">Authorization</span></span>  | <span data-ttu-id="2d154-112">string</span><span class="sxs-lookup"><span data-stu-id="2d154-112">string</span></span>  | <span data-ttu-id="2d154-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2d154-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2d154-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2d154-115">Content-Type</span></span> | <span data-ttu-id="2d154-116">string</span><span class="sxs-lookup"><span data-stu-id="2d154-116">string</span></span>  | <span data-ttu-id="2d154-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2d154-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2d154-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2d154-119">Request body</span></span>
<span data-ttu-id="2d154-120">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="2d154-120">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="2d154-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2d154-121">Parameter</span></span>    | <span data-ttu-id="2d154-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d154-122">Type</span></span>   |<span data-ttu-id="2d154-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d154-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2d154-124">DestinationId</span><span class="sxs-lookup"><span data-stu-id="2d154-124">DestinationId</span></span>|<span data-ttu-id="2d154-125">String</span><span class="sxs-lookup"><span data-stu-id="2d154-125">String</span></span>|<span data-ttu-id="2d154-126">El ID de la carpeta de destino o el nombre de carpeta conocido `Inbox`, `Drafts`, `SentItems` o `DeletedItems`.</span><span class="sxs-lookup"><span data-stu-id="2d154-126">The destination folder ID, or the `Inbox`, `Drafts`, `SentItems`, or `DeletedItems` well-known folder name.</span></span>|

## <a name="response"></a><span data-ttu-id="2d154-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d154-127">Response</span></span>

<span data-ttu-id="2d154-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d154-128">If successful, this method returns `201, Created` response code and [message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2d154-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2d154-129">Example</span></span>
<span data-ttu-id="2d154-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2d154-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="2d154-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2d154-131">Request</span></span>
<span data-ttu-id="2d154-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2d154-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_move"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/move
Content-type: application/json
Content-length: 44

{
  "DestinationId": "destinationId-value"
}
```

##### <a name="response"></a><span data-ttu-id="2d154-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d154-133">Response</span></span>
<span data-ttu-id="2d154-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2d154-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
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
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: move",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
