# <a name="create-acceptedsender"></a><span data-ttu-id="4bf10-101">Create acceptedSender</span><span class="sxs-lookup"><span data-stu-id="4bf10-101">Create acceptedSender</span></span>
<span data-ttu-id="4bf10-102">Agrega un nuevo usuario o grupo a la lista de acceptedSender.</span><span class="sxs-lookup"><span data-stu-id="4bf10-102">Add a new user or group to the acceptedSender list.</span></span>

<span data-ttu-id="4bf10-p101">En el cuerpo de la solicitud, especifique el usuario o grupo en `@odata.id`. Los usuarios de la lista de remitentes aceptados pueden publicar conversaciones del grupo. Asegúrese de no especificar el mismo usuario o grupo en las listas de remitentes aceptados y de remitentes rechazados, de lo contrario se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="4bf10-p101">Specify the user or group in `@odata.id` in the request body. Users in the accepted senders list can post to conversations of the group . Make sure you do not specify the same user or group in the accepted senders and rejected senders lists, otherwise you will get an error.</span></span>

## <a name="permissions"></a><span data-ttu-id="4bf10-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="4bf10-106">Permissions</span></span>
<span data-ttu-id="4bf10-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4bf10-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4bf10-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4bf10-109">Permission type</span></span>      | <span data-ttu-id="4bf10-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4bf10-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4bf10-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4bf10-111">Delegated (work or school account)</span></span> | <span data-ttu-id="4bf10-112">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4bf10-112">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="4bf10-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4bf10-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4bf10-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4bf10-114">Not supported.</span></span>    |
|<span data-ttu-id="4bf10-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4bf10-115">Application</span></span> | <span data-ttu-id="4bf10-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4bf10-116">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4bf10-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4bf10-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/acceptedSenders/$ref
```
## <a name="request-headers"></a><span data-ttu-id="4bf10-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4bf10-118">Request headers</span></span>
| <span data-ttu-id="4bf10-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bf10-119">Header</span></span>       | <span data-ttu-id="4bf10-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4bf10-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="4bf10-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="4bf10-121">Authorization</span></span>  | <span data-ttu-id="4bf10-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4bf10-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4bf10-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4bf10-124">Request body</span></span>
<span data-ttu-id="4bf10-125">En el cuerpo de la solicitud, proporcione el identificador de un objeto de usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="4bf10-125">In the request body, supply the id of a user or group object.</span></span>

## <a name="response"></a><span data-ttu-id="4bf10-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4bf10-126">Response</span></span>
<span data-ttu-id="4bf10-127">Este método devuelve el código de respuesta `204 No Content` y ningún cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4bf10-127">This method returns `204 No Content` response code and no response body.</span></span>

## <a name="example"></a><span data-ttu-id="4bf10-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4bf10-128">Example</span></span>
#### <a name="request"></a><span data-ttu-id="4bf10-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4bf10-129">Request</span></span>
<span data-ttu-id="4bf10-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4bf10-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_acceptedsender"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/acceptedSenders/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id":"https://graph.microsoft.com/v1.0/users/alexd@contoso.com"
}
```

#### <a name="response"></a><span data-ttu-id="4bf10-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4bf10-131">Response</span></span>
<span data-ttu-id="4bf10-132">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4bf10-132">The following is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create acceptedSender",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
