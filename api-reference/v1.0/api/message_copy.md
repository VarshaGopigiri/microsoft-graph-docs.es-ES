# <a name="message-copy"></a><span data-ttu-id="f9c87-101">message: copy</span><span class="sxs-lookup"><span data-stu-id="f9c87-101">message: copy</span></span>

<span data-ttu-id="f9c87-102">Copia un mensaje a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f9c87-102">Copy a message to a folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="f9c87-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="f9c87-103">Permissions</span></span>
<span data-ttu-id="f9c87-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f9c87-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f9c87-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f9c87-106">Permission type</span></span>      | <span data-ttu-id="f9c87-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f9c87-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f9c87-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f9c87-108">Delegated (work or school account)</span></span> | <span data-ttu-id="f9c87-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f9c87-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="f9c87-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f9c87-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f9c87-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f9c87-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="f9c87-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f9c87-112">Application</span></span> | <span data-ttu-id="f9c87-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f9c87-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="f9c87-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9c87-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/copy
POST /users/{id | userPrincipalName}/messages/{id}/copy
POST /me/mailFolders/{id}/messages/{id}/copy
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/copy
```
## <a name="request-headers"></a><span data-ttu-id="f9c87-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9c87-115">Request headers</span></span>
| <span data-ttu-id="f9c87-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="f9c87-116">Name</span></span>       | <span data-ttu-id="f9c87-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9c87-117">Type</span></span> | <span data-ttu-id="f9c87-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9c87-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f9c87-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="f9c87-119">Authorization</span></span>  | <span data-ttu-id="f9c87-120">string</span><span class="sxs-lookup"><span data-stu-id="f9c87-120">string</span></span>  | <span data-ttu-id="f9c87-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f9c87-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f9c87-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f9c87-123">Content-Type</span></span> | <span data-ttu-id="f9c87-124">string</span><span class="sxs-lookup"><span data-stu-id="f9c87-124">string</span></span>  | <span data-ttu-id="f9c87-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f9c87-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f9c87-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9c87-127">Request body</span></span>
<span data-ttu-id="f9c87-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f9c87-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f9c87-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f9c87-129">Parameter</span></span>    | <span data-ttu-id="f9c87-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9c87-130">Type</span></span>   |<span data-ttu-id="f9c87-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9c87-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f9c87-132">destinationId</span><span class="sxs-lookup"><span data-stu-id="f9c87-132">destinationId</span></span>|<span data-ttu-id="f9c87-133">String</span><span class="sxs-lookup"><span data-stu-id="f9c87-133">String</span></span>|<span data-ttu-id="f9c87-134">El ID de la carpeta de destino o el nombre de carpeta conocido `Inbox`, `Drafts`, `SentItems` o `DeletedItems`.</span><span class="sxs-lookup"><span data-stu-id="f9c87-134">The destination folder ID, or the `Inbox`, `Drafts`, `SentItems`, or `DeletedItems` well-known folder name.</span></span>|

## <a name="response"></a><span data-ttu-id="f9c87-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9c87-135">Response</span></span>

<span data-ttu-id="f9c87-136">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9c87-136">If successful, this method returns `201, Created` response code and [Message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f9c87-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9c87-137">Example</span></span>
<span data-ttu-id="f9c87-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f9c87-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f9c87-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9c87-139">Request</span></span>
<span data-ttu-id="f9c87-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f9c87-140">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="f9c87-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9c87-141">Response</span></span>
<span data-ttu-id="f9c87-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f9c87-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
