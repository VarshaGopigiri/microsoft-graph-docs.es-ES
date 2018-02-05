# <a name="message-copy"></a><span data-ttu-id="18be3-101">message: copy</span><span class="sxs-lookup"><span data-stu-id="18be3-101">message: copy</span></span>

<span data-ttu-id="18be3-102">Copia un mensaje a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="18be3-102">Copy a message to a folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="18be3-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="18be3-103">Permissions</span></span>
<span data-ttu-id="18be3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="18be3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="18be3-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="18be3-106">Permission type</span></span>      | <span data-ttu-id="18be3-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="18be3-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="18be3-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="18be3-108">Delegated (work or school account)</span></span> | <span data-ttu-id="18be3-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="18be3-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="18be3-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="18be3-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="18be3-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="18be3-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="18be3-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="18be3-112">Application</span></span> | <span data-ttu-id="18be3-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="18be3-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="18be3-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="18be3-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/copy
POST /users/{id | userPrincipalName}/messages/{id}/copy
POST /me/mailFolders/{id}/messages/{id}/copy
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/copy
```
## <a name="request-headers"></a><span data-ttu-id="18be3-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="18be3-115">Request headers</span></span>
| <span data-ttu-id="18be3-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="18be3-116">Name</span></span>       | <span data-ttu-id="18be3-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="18be3-117">Type</span></span> | <span data-ttu-id="18be3-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="18be3-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="18be3-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="18be3-119">Authorization</span></span>  | <span data-ttu-id="18be3-120">string</span><span class="sxs-lookup"><span data-stu-id="18be3-120">string</span></span>  | <span data-ttu-id="18be3-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18be3-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="18be3-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="18be3-123">Content-Type</span></span> | <span data-ttu-id="18be3-124">string</span><span class="sxs-lookup"><span data-stu-id="18be3-124">string</span></span>  | <span data-ttu-id="18be3-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18be3-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="18be3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="18be3-127">Request body</span></span>
<span data-ttu-id="18be3-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="18be3-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="18be3-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="18be3-129">Parameter</span></span>    | <span data-ttu-id="18be3-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="18be3-130">Type</span></span>   |<span data-ttu-id="18be3-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="18be3-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="18be3-132">destinationId</span><span class="sxs-lookup"><span data-stu-id="18be3-132">destinationId</span></span>|<span data-ttu-id="18be3-133">String</span><span class="sxs-lookup"><span data-stu-id="18be3-133">String</span></span>|<span data-ttu-id="18be3-134">El identificador de la carpeta de destino o un nombre de carpeta conocido como, por ejemplo, *Inbox*, *Drafts*, *SentItems* o *DeletedItems*.</span><span class="sxs-lookup"><span data-stu-id="18be3-134">The destination folder ID, or a well-known folder name such as *Inbox*, *Drafts*, *SentItems*, or *DeletedItems*.</span></span> <span data-ttu-id="18be3-135">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="18be3-135">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>|

## <a name="response"></a><span data-ttu-id="18be3-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18be3-136">Response</span></span>

<span data-ttu-id="18be3-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18be3-137">If successful, this method returns `201 Created` response code and [Message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="18be3-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="18be3-138">Example</span></span>
<span data-ttu-id="18be3-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="18be3-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="18be3-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="18be3-140">Request</span></span>
<span data-ttu-id="18be3-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18be3-141">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="18be3-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18be3-142">Response</span></span>
<span data-ttu-id="18be3-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="18be3-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
