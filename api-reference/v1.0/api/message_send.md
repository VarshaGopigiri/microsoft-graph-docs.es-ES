# <a name="message-send"></a><span data-ttu-id="046fa-101">message: send</span><span class="sxs-lookup"><span data-stu-id="046fa-101">message: send</span></span>

<span data-ttu-id="046fa-p101">Envía un mensaje de la carpeta Borrador. El borrador del mensaje puede ser un borrador de mensaje nuevo, un borrador de respuesta, un borrador de respuesta a todos o un borrador de reenvío. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="046fa-p101">Send a message in the draft folder. The draft message can be a new message draft, reply draft, reply-all draft, or a forward draft. The message is then saved in the Sent Items folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="046fa-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="046fa-105">Permissions</span></span>
<span data-ttu-id="046fa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="046fa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="046fa-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="046fa-108">Permission type</span></span>      | <span data-ttu-id="046fa-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="046fa-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="046fa-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="046fa-110">Delegated (work or school account)</span></span> | <span data-ttu-id="046fa-111">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="046fa-111">Mail.Send</span></span>    |
|<span data-ttu-id="046fa-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="046fa-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="046fa-113">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="046fa-113">Mail.Send</span></span>    |
|<span data-ttu-id="046fa-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="046fa-114">Application</span></span> | <span data-ttu-id="046fa-115">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="046fa-115">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="046fa-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="046fa-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/send
POST /users/{id | userPrincipalName}/messages/{id}/send
```
## <a name="request-headers"></a><span data-ttu-id="046fa-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="046fa-117">Request headers</span></span>
| <span data-ttu-id="046fa-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="046fa-118">Name</span></span>       | <span data-ttu-id="046fa-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="046fa-119">Type</span></span> | <span data-ttu-id="046fa-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="046fa-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="046fa-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="046fa-121">Authorization</span></span>  | <span data-ttu-id="046fa-122">string</span><span class="sxs-lookup"><span data-stu-id="046fa-122">string</span></span>  | <span data-ttu-id="046fa-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="046fa-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="046fa-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="046fa-125">Request body</span></span>

## <a name="response"></a><span data-ttu-id="046fa-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="046fa-126">Response</span></span>

<span data-ttu-id="046fa-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="046fa-p104">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="046fa-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="046fa-129">Example</span></span>
<span data-ttu-id="046fa-130">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="046fa-130">The following example shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="046fa-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="046fa-131">Request</span></span>
<span data-ttu-id="046fa-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="046fa-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_send"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/send
```

##### <a name="response"></a><span data-ttu-id="046fa-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="046fa-133">Response</span></span>

<span data-ttu-id="046fa-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="046fa-134">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: send",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
