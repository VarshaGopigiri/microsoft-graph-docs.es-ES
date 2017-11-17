# <a name="create-message"></a><span data-ttu-id="71e09-101">Create Message</span><span class="sxs-lookup"><span data-stu-id="71e09-101">Create Message</span></span>

<span data-ttu-id="71e09-102">Usa esta API para crear un objeto Message en una mailfolder.</span><span class="sxs-lookup"><span data-stu-id="71e09-102">Use this API to create a new Message in a mailfolder.</span></span>
## <a name="permissions"></a><span data-ttu-id="71e09-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="71e09-103">Permissions</span></span>
<span data-ttu-id="71e09-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="71e09-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="71e09-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71e09-106">Permission type</span></span>      | <span data-ttu-id="71e09-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71e09-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="71e09-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71e09-108">Delegated (work or school account)</span></span> | <span data-ttu-id="71e09-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="71e09-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="71e09-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71e09-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="71e09-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="71e09-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="71e09-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71e09-112">Application</span></span> | <span data-ttu-id="71e09-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="71e09-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="71e09-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71e09-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/{id}/messages
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages
```
## <a name="request-headers"></a><span data-ttu-id="71e09-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71e09-115">Request headers</span></span>
| <span data-ttu-id="71e09-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71e09-116">Header</span></span>       | <span data-ttu-id="71e09-117">Valor</span><span class="sxs-lookup"><span data-stu-id="71e09-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="71e09-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="71e09-118">Authorization</span></span>  | <span data-ttu-id="71e09-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="71e09-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="71e09-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="71e09-121">Content-Type</span></span>  | <span data-ttu-id="71e09-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="71e09-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="71e09-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71e09-124">Request body</span></span>
<span data-ttu-id="71e09-125">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="71e09-125">In the request body, supply a JSON representation of [Message](../resources/message.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="71e09-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71e09-126">Response</span></span>

<span data-ttu-id="71e09-127">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71e09-127">If successful, this method returns `201 Created` response code and [Message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="71e09-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71e09-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="71e09-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71e09-129">Request</span></span>
<span data-ttu-id="71e09-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71e09-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_message_from_mailfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/{id}/messages
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
<span data-ttu-id="71e09-131">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="71e09-131">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="71e09-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71e09-132">Response</span></span>
<span data-ttu-id="71e09-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71e09-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Create Message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
