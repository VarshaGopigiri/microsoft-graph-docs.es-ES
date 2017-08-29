# <a name="message-replyall"></a><span data-ttu-id="90058-101">message: replyAll</span><span class="sxs-lookup"><span data-stu-id="90058-101">message: replyAll</span></span>

<span data-ttu-id="90058-p101">Responde a todos los remitentes de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="90058-p101">Reply to all recipients of a message. The message is then saved in the Sent Items folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="90058-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="90058-104">Permissions</span></span>
<span data-ttu-id="90058-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="90058-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="90058-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="90058-107">Permission type</span></span>      | <span data-ttu-id="90058-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="90058-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="90058-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="90058-109">Delegated (work or school account)</span></span> | <span data-ttu-id="90058-110">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="90058-110">Mail.Send</span></span>    |
|<span data-ttu-id="90058-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="90058-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="90058-112">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="90058-112">Mail.Send</span></span>    |
|<span data-ttu-id="90058-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="90058-113">Application</span></span> | <span data-ttu-id="90058-114">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="90058-114">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="90058-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="90058-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/me/messages/{id}/replyAll
POST /users/{id | userPrincipalName}/messages/{id}/replyAll
POST /me/mailFolders/{id}/messages/{id}/replyAll
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/replyAll
```
## <a name="request-headers"></a><span data-ttu-id="90058-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="90058-116">Request headers</span></span>
| <span data-ttu-id="90058-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="90058-117">Name</span></span>       | <span data-ttu-id="90058-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="90058-118">Type</span></span> | <span data-ttu-id="90058-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="90058-119">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="90058-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="90058-120">Authorization</span></span>  | <span data-ttu-id="90058-121">string</span><span class="sxs-lookup"><span data-stu-id="90058-121">string</span></span>  | <span data-ttu-id="90058-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90058-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="90058-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="90058-124">Content-Type</span></span> | <span data-ttu-id="90058-125">string</span><span class="sxs-lookup"><span data-stu-id="90058-125">string</span></span>  | <span data-ttu-id="90058-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90058-p104">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="90058-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="90058-128">Request body</span></span>
<span data-ttu-id="90058-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="90058-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="90058-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="90058-130">Parameter</span></span>    | <span data-ttu-id="90058-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="90058-131">Type</span></span>   |<span data-ttu-id="90058-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="90058-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="90058-133">comment</span><span class="sxs-lookup"><span data-stu-id="90058-133">comment</span></span>|<span data-ttu-id="90058-134">String</span><span class="sxs-lookup"><span data-stu-id="90058-134">String</span></span>|<span data-ttu-id="90058-p105">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="90058-p105">A comment to include. Can be an empty string.</span></span>|

## <a name="response"></a><span data-ttu-id="90058-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90058-137">Response</span></span>

<span data-ttu-id="90058-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90058-p106">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="90058-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90058-140">Example</span></span>
<span data-ttu-id="90058-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="90058-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="90058-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="90058-142">Request</span></span>
<span data-ttu-id="90058-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="90058-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_replyall"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/replyAll
Content-type: application/json
Content-length: 32

{
  "comment": "comment-value"
}
```


##### <a name="response"></a><span data-ttu-id="90058-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90058-144">Response</span></span>
<span data-ttu-id="90058-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90058-145">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: replyAll",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
