# <a name="message-copy"></a><span data-ttu-id="343ef-101">message: copy</span><span class="sxs-lookup"><span data-stu-id="343ef-101">message: copy</span></span>

<span data-ttu-id="343ef-102">Copia un mensaje a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="343ef-102">Copy a message to a folder.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="343ef-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="343ef-103">Prerequisites</span></span>
<span data-ttu-id="343ef-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="343ef-104">One of the following **scopes** is required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="343ef-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="343ef-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/copy
POST /users/{id | userPrincipalName}/messages/{id}/copy
POST /me/mailFolders/{id}/messages/{id}/copy
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/copy
```
## <a name="request-headers"></a><span data-ttu-id="343ef-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="343ef-106">Request headers</span></span>
| <span data-ttu-id="343ef-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="343ef-107">Name</span></span>       | <span data-ttu-id="343ef-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="343ef-108">Type</span></span> | <span data-ttu-id="343ef-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="343ef-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="343ef-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="343ef-110">Authorization</span></span>  | <span data-ttu-id="343ef-111">string</span><span class="sxs-lookup"><span data-stu-id="343ef-111">string</span></span>  | <span data-ttu-id="343ef-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="343ef-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="343ef-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="343ef-114">Content-Type</span></span> | <span data-ttu-id="343ef-115">string</span><span class="sxs-lookup"><span data-stu-id="343ef-115">string</span></span>  | <span data-ttu-id="343ef-p102">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="343ef-p102">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="343ef-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="343ef-118">Request body</span></span>
<span data-ttu-id="343ef-119">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="343ef-119">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="343ef-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="343ef-120">Parameter</span></span>    | <span data-ttu-id="343ef-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="343ef-121">Type</span></span>   |<span data-ttu-id="343ef-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="343ef-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="343ef-123">destinationId</span><span class="sxs-lookup"><span data-stu-id="343ef-123">destinationId</span></span>|<span data-ttu-id="343ef-124">String</span><span class="sxs-lookup"><span data-stu-id="343ef-124">String</span></span>|<span data-ttu-id="343ef-125">El ID de la carpeta de destino o el nombre de carpeta conocido `Inbox`, `Drafts`, `SentItems` o `DeletedItems`.</span><span class="sxs-lookup"><span data-stu-id="343ef-125">The destination folder ID, or the `Inbox`, `Drafts`, `SentItems`, or `DeletedItems` well-known folder name.</span></span>|

## <a name="response"></a><span data-ttu-id="343ef-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="343ef-126">Response</span></span>

<span data-ttu-id="343ef-127">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="343ef-127">If successful, this method returns `201, Created` response code and [message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="343ef-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="343ef-128">Example</span></span>
<span data-ttu-id="343ef-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="343ef-129">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="343ef-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="343ef-130">Request</span></span>
<span data-ttu-id="343ef-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="343ef-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_copy"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/copy
Content-type: application/json
Content-length: 44

{
  "destinationId": "destinationId-value"
}
```

##### <a name="response"></a><span data-ttu-id="343ef-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="343ef-132">Response</span></span>
<span data-ttu-id="343ef-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="343ef-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "message: copy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
