# <a name="post-forward"></a><span data-ttu-id="6d746-101">post: forward</span><span class="sxs-lookup"><span data-stu-id="6d746-101">post: forward</span></span>

<span data-ttu-id="6d746-p101">Reenvía una publicación a un destinatario. Puede especificar la conversación y el hilo primarios en la solicitud, o bien, especificar solo el hilo primario sin la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="6d746-p101">Forward a post to a recipient. You can specify both the parent conversation and thread in the request, or, you can specify just the parent thread without the parent conversation.</span></span> 

## <a name="permissions"></a><span data-ttu-id="6d746-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="6d746-104">Permissions</span></span>
<span data-ttu-id="6d746-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6d746-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6d746-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6d746-107">Permission type</span></span>      | <span data-ttu-id="6d746-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6d746-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6d746-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6d746-109">Delegated (work or school account)</span></span> | <span data-ttu-id="6d746-110">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6d746-110">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="6d746-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6d746-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6d746-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d746-112">Not supported.</span></span>    |
|<span data-ttu-id="6d746-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6d746-113">Application</span></span> | <span data-ttu-id="6d746-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6d746-114">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6d746-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6d746-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads/{id}/posts/{id}/forward
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/forward

```
## <a name="request-headers"></a><span data-ttu-id="6d746-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6d746-116">Request headers</span></span>
| <span data-ttu-id="6d746-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d746-117">Header</span></span>       | <span data-ttu-id="6d746-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6d746-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="6d746-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="6d746-119">Authorization</span></span>  | <span data-ttu-id="6d746-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6d746-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="6d746-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6d746-122">Request body</span></span>
<span data-ttu-id="6d746-123">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="6d746-123">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="6d746-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6d746-124">Parameter</span></span>    | <span data-ttu-id="6d746-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d746-125">Type</span></span>   |<span data-ttu-id="6d746-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d746-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6d746-127">comment</span><span class="sxs-lookup"><span data-stu-id="6d746-127">comment</span></span>|<span data-ttu-id="6d746-128">String</span><span class="sxs-lookup"><span data-stu-id="6d746-128">String</span></span>|<span data-ttu-id="6d746-129">Comentario opcional que se envía junto con la publicación.</span><span class="sxs-lookup"><span data-stu-id="6d746-129">Optional comment that is forwarded together with the post.</span></span>|
|<span data-ttu-id="6d746-130">toRecipients</span><span class="sxs-lookup"><span data-stu-id="6d746-130">toRecipients</span></span>|<span data-ttu-id="6d746-131">Colección [recipient](../resources/recipient.md)</span><span class="sxs-lookup"><span data-stu-id="6d746-131">[recipient](../resources/recipient.md) collection</span></span>|<span data-ttu-id="6d746-132">Destinatarios a los que se ha reenviado el encadenado de hilos.</span><span class="sxs-lookup"><span data-stu-id="6d746-132">The recipients to whom the threaded is forwarded to.</span></span>|

## <a name="response"></a><span data-ttu-id="6d746-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d746-133">Response</span></span>

<span data-ttu-id="6d746-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d746-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6d746-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d746-136">Example</span></span>
<span data-ttu-id="6d746-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6d746-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="6d746-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6d746-138">Request</span></span>
<span data-ttu-id="6d746-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d746-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_forward"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts/{id}/forward
Content-type: application/json
Content-length: 166

{
  "comment": "comment-value",
  "toRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ]
}
```

##### <a name="response"></a><span data-ttu-id="6d746-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d746-140">Response</span></span>
<span data-ttu-id="6d746-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d746-141">Here is an example of the response.</span></span>
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
  "description": "post: forward",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
