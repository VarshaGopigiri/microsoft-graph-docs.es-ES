# <a name="message-reply"></a><span data-ttu-id="58d5d-101">message: reply</span><span class="sxs-lookup"><span data-stu-id="58d5d-101">message: reply</span></span>

<span data-ttu-id="58d5d-p101">Responde al remitente de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="58d5d-p101">Reply to the sender of a message. The message is then saved in the Sent Items folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="58d5d-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="58d5d-104">Permissions</span></span>
<span data-ttu-id="58d5d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="58d5d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="58d5d-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="58d5d-107">Permission type</span></span>      | <span data-ttu-id="58d5d-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="58d5d-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="58d5d-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="58d5d-109">Delegated (work or school account)</span></span> | <span data-ttu-id="58d5d-110">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="58d5d-110">Mail.Send</span></span>    |
|<span data-ttu-id="58d5d-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="58d5d-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="58d5d-112">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="58d5d-112">Mail.Send</span></span>    |
|<span data-ttu-id="58d5d-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="58d5d-113">Application</span></span> | <span data-ttu-id="58d5d-114">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="58d5d-114">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="58d5d-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="58d5d-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/reply
POST /users/{id | userPrincipalName}/messages/{id}/reply
POST /me/mailFolders/{id}/messages/{id}/reply
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/reply
```
## <a name="request-headers"></a><span data-ttu-id="58d5d-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="58d5d-116">Request headers</span></span>
| <span data-ttu-id="58d5d-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="58d5d-117">Name</span></span>       | <span data-ttu-id="58d5d-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="58d5d-118">Type</span></span> | <span data-ttu-id="58d5d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="58d5d-119">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="58d5d-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="58d5d-120">Authorization</span></span>  | <span data-ttu-id="58d5d-121">string</span><span class="sxs-lookup"><span data-stu-id="58d5d-121">string</span></span>  | <span data-ttu-id="58d5d-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="58d5d-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="58d5d-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="58d5d-124">Content-Type</span></span> | <span data-ttu-id="58d5d-125">string</span><span class="sxs-lookup"><span data-stu-id="58d5d-125">string</span></span>  | <span data-ttu-id="58d5d-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="58d5d-p104">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="58d5d-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="58d5d-128">Request body</span></span>
<span data-ttu-id="58d5d-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="58d5d-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="58d5d-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="58d5d-130">Parameter</span></span>    | <span data-ttu-id="58d5d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="58d5d-131">Type</span></span>   |<span data-ttu-id="58d5d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="58d5d-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="58d5d-133">comment</span><span class="sxs-lookup"><span data-stu-id="58d5d-133">comment</span></span>|<span data-ttu-id="58d5d-134">String</span><span class="sxs-lookup"><span data-stu-id="58d5d-134">String</span></span>|<span data-ttu-id="58d5d-p105">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="58d5d-p105">A comment to include. Can be an empty string.</span></span>|

## <a name="response"></a><span data-ttu-id="58d5d-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58d5d-137">Response</span></span>

<span data-ttu-id="58d5d-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58d5d-p106">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="58d5d-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="58d5d-140">Example</span></span>
<span data-ttu-id="58d5d-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="58d5d-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="58d5d-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="58d5d-142">Request</span></span>
<span data-ttu-id="58d5d-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="58d5d-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_reply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/reply
Content-type: application/json
Content-length: 32

{
  "comment": "comment-value"
}
```

##### <a name="response"></a><span data-ttu-id="58d5d-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58d5d-144">Response</span></span>
##### <a name="response"></a><span data-ttu-id="58d5d-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58d5d-145">Response</span></span>
<span data-ttu-id="58d5d-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58d5d-146">Here is an example of the response.</span></span>
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
  "description": "message: reply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
