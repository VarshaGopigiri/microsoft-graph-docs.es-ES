# <a name="message-move"></a><span data-ttu-id="92764-101">message: move</span><span class="sxs-lookup"><span data-stu-id="92764-101">message: move</span></span>

<span data-ttu-id="92764-p101">Mueve un mensaje a una carpeta. Se crea una nueva copia del mensaje en la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="92764-p101">Move a message to a folder. This creates a new copy of the message in the destination folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="92764-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="92764-104">Permissions</span></span>
<span data-ttu-id="92764-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="92764-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="92764-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="92764-107">Permission type</span></span>      | <span data-ttu-id="92764-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="92764-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="92764-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="92764-109">Delegated (work or school account)</span></span> | <span data-ttu-id="92764-110">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="92764-110">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="92764-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="92764-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="92764-112">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="92764-112">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="92764-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="92764-113">Application</span></span> | <span data-ttu-id="92764-114">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="92764-114">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="92764-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="92764-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/move
POST /users/{id | userPrincipalName}/messages/{id}/move
POST /me/mailFolders/{id}/messages/{id}/move
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/move
```
## <a name="request-headers"></a><span data-ttu-id="92764-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="92764-116">Request headers</span></span>
| <span data-ttu-id="92764-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="92764-117">Name</span></span>       | <span data-ttu-id="92764-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="92764-118">Type</span></span> | <span data-ttu-id="92764-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="92764-119">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="92764-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="92764-120">Authorization</span></span>  | <span data-ttu-id="92764-121">string</span><span class="sxs-lookup"><span data-stu-id="92764-121">string</span></span>  | <span data-ttu-id="92764-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92764-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="92764-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="92764-124">Content-Type</span></span> | <span data-ttu-id="92764-125">string</span><span class="sxs-lookup"><span data-stu-id="92764-125">string</span></span>  | <span data-ttu-id="92764-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92764-p104">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="92764-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="92764-128">Request body</span></span>
<span data-ttu-id="92764-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="92764-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="92764-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="92764-130">Parameter</span></span>    | <span data-ttu-id="92764-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="92764-131">Type</span></span>   |<span data-ttu-id="92764-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="92764-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="92764-133">DestinationId</span><span class="sxs-lookup"><span data-stu-id="92764-133">DestinationId</span></span>|<span data-ttu-id="92764-134">String</span><span class="sxs-lookup"><span data-stu-id="92764-134">String</span></span>|<span data-ttu-id="92764-135">El identificador de la carpeta de destino o un nombre de carpeta conocido como, por ejemplo, *Inbox*, *Drafts*, *SentItems* o *DeletedItems*.</span><span class="sxs-lookup"><span data-stu-id="92764-135">The destination folder ID, or a well-known folder name such as *Inbox*, *Drafts*, *SentItems*, or *DeletedItems*.</span></span> <span data-ttu-id="92764-136">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="92764-136">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>|

## <a name="response"></a><span data-ttu-id="92764-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="92764-137">Response</span></span>

<span data-ttu-id="92764-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="92764-138">If successful, this method returns `201 Created` response code and [Message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="92764-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="92764-139">Example</span></span>
<span data-ttu-id="92764-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="92764-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="92764-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="92764-141">Request</span></span>
<span data-ttu-id="92764-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="92764-142">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="92764-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="92764-143">Response</span></span>
<span data-ttu-id="92764-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="92764-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
