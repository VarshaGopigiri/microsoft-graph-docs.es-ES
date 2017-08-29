# <a name="message-move"></a><span data-ttu-id="6f90c-101">message: move</span><span class="sxs-lookup"><span data-stu-id="6f90c-101">message: move</span></span>

<span data-ttu-id="6f90c-p101">Mueve un mensaje a una carpeta. Se crea una nueva copia del mensaje en la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="6f90c-p101">Move a message to a folder. This creates a new copy of the message in the destination folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="6f90c-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="6f90c-104">Permissions</span></span>
<span data-ttu-id="6f90c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6f90c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6f90c-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6f90c-107">Permission type</span></span>      | <span data-ttu-id="6f90c-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6f90c-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6f90c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6f90c-109">Delegated (work or school account)</span></span> | <span data-ttu-id="6f90c-110">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6f90c-110">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6f90c-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6f90c-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6f90c-112">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6f90c-112">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6f90c-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6f90c-113">Application</span></span> | <span data-ttu-id="6f90c-114">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6f90c-114">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="6f90c-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6f90c-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/move
POST /users/{id | userPrincipalName}/messages/{id}/move
POST /me/mailFolders/{id}/messages/{id}/move
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/move
```
## <a name="request-headers"></a><span data-ttu-id="6f90c-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6f90c-116">Request headers</span></span>
| <span data-ttu-id="6f90c-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="6f90c-117">Name</span></span>       | <span data-ttu-id="6f90c-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f90c-118">Type</span></span> | <span data-ttu-id="6f90c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f90c-119">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6f90c-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="6f90c-120">Authorization</span></span>  | <span data-ttu-id="6f90c-121">string</span><span class="sxs-lookup"><span data-stu-id="6f90c-121">string</span></span>  | <span data-ttu-id="6f90c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f90c-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6f90c-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6f90c-124">Content-Type</span></span> | <span data-ttu-id="6f90c-125">string</span><span class="sxs-lookup"><span data-stu-id="6f90c-125">string</span></span>  | <span data-ttu-id="6f90c-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f90c-p104">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6f90c-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6f90c-128">Request body</span></span>
<span data-ttu-id="6f90c-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="6f90c-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="6f90c-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6f90c-130">Parameter</span></span>    | <span data-ttu-id="6f90c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f90c-131">Type</span></span>   |<span data-ttu-id="6f90c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f90c-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6f90c-133">DestinationId</span><span class="sxs-lookup"><span data-stu-id="6f90c-133">DestinationId</span></span>|<span data-ttu-id="6f90c-134">String</span><span class="sxs-lookup"><span data-stu-id="6f90c-134">String</span></span>|<span data-ttu-id="6f90c-135">El ID de la carpeta de destino o el nombre de carpeta conocido `Inbox`, `Drafts`, `SentItems` o `DeletedItems`.</span><span class="sxs-lookup"><span data-stu-id="6f90c-135">The destination folder ID, or the `Inbox`, `Drafts`, `SentItems`, or `DeletedItems` well-known folder name.</span></span>|

## <a name="response"></a><span data-ttu-id="6f90c-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f90c-136">Response</span></span>

<span data-ttu-id="6f90c-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f90c-137">If successful, this method returns `201, Created` response code and [Message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6f90c-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f90c-138">Example</span></span>
<span data-ttu-id="6f90c-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6f90c-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="6f90c-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f90c-140">Request</span></span>
<span data-ttu-id="6f90c-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f90c-141">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="6f90c-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f90c-142">Response</span></span>
<span data-ttu-id="6f90c-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6f90c-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
