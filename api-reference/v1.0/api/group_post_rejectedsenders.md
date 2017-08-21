# <a name="create-rejectedsender"></a><span data-ttu-id="e056a-101">Create rejectedSender</span><span class="sxs-lookup"><span data-stu-id="e056a-101">Create rejectedSender</span></span>

<span data-ttu-id="e056a-102">Agrega un nuevo usuario o grupo a la lista de rejectedSender.</span><span class="sxs-lookup"><span data-stu-id="e056a-102">Add a new user or group to the rejectedSender list.</span></span>

<span data-ttu-id="e056a-p101">En el cuerpo de la solicitud, especifique el usuario o grupo en `@odata.id`. Los usuarios de la lista de remitentes rechazados no pueden publicar conversaciones del grupo (identificado en la dirección URL de solicitud POST). Asegúrese de no especificar el mismo usuario o grupo en las listas de remitentes rechazados y de remitentes aceptados, de lo contrario se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="e056a-p101">Specify the user or group in `@odata.id` in the request body. Users in the rejected senders list cannot post to conversations of the group (identified in the POST request URL). Make sure you do not specify the same user or group in the rejected senders and accepted senders lists, otherwise you will get an error.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e056a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e056a-106">Prerequisites</span></span>
<span data-ttu-id="e056a-107">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="e056a-107">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="e056a-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e056a-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/rejectedSenders/$ref
```
## <a name="request-headers"></a><span data-ttu-id="e056a-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e056a-109">Request headers</span></span>
| <span data-ttu-id="e056a-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e056a-110">Header</span></span>       | <span data-ttu-id="e056a-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e056a-111">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e056a-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="e056a-112">Authorization</span></span>  | <span data-ttu-id="e056a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e056a-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e056a-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e056a-115">Request body</span></span>
<span data-ttu-id="e056a-116">En el cuerpo de la solicitud, proporcione el identificador de un objeto de usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="e056a-116">In the request body, supply the id of a user or group object.</span></span>

## <a name="response"></a><span data-ttu-id="e056a-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e056a-117">Response</span></span>

<span data-ttu-id="e056a-118">Este método devuelve el código de respuesta `204, No Content` y ningún cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e056a-118">This method returns `204, No Content` response code and no response body.</span></span>

## <a name="example"></a><span data-ttu-id="e056a-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e056a-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e056a-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e056a-120">Request</span></span>
<span data-ttu-id="e056a-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e056a-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/rejectedSenders/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id":"https://graph.microsoft.com/v1.0/users/alexd@contoso.com"
}
```
##### <a name="response"></a><span data-ttu-id="e056a-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e056a-122">Response</span></span>
<span data-ttu-id="e056a-123">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e056a-123">Here is an example of the response.</span></span>
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
  "description": "Create rejectedSender",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
