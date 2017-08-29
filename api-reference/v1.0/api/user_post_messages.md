# <a name="create-message"></a><span data-ttu-id="9b0ae-101">Create Message</span><span class="sxs-lookup"><span data-stu-id="9b0ae-101">Create Message</span></span>

<span data-ttu-id="9b0ae-p101">Use esta API para crear un mensaje. Pueden crearse borradores en cualquier carpeta y, si quiere, actualizarlos antes de enviarlos. Para guardar en la carpeta Borradores, use el acceso directo /messages.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-p101">Use this API to create a draft of a new message. Drafts can be created in any folder and optionally updated before sending. To save to the Drafts folder, use the /messages shortcut.</span></span>

<span data-ttu-id="9b0ae-105">Al crear el borrador en la misma llamada **POST**, puede incluir [datos adjuntos](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="9b0ae-105">While creating the draft in the same **POST** call, you can include an [attachment](../resources/attachment.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="9b0ae-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b0ae-106">Permissions</span></span>
<span data-ttu-id="9b0ae-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9b0ae-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9b0ae-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b0ae-109">Permission type</span></span>      | <span data-ttu-id="9b0ae-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b0ae-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9b0ae-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b0ae-111">Delegated (work or school account)</span></span> | <span data-ttu-id="9b0ae-112">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9b0ae-112">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="9b0ae-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b0ae-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9b0ae-114">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9b0ae-114">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="9b0ae-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b0ae-115">Application</span></span> | <span data-ttu-id="9b0ae-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9b0ae-116">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="9b0ae-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b0ae-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages
POST /users/{id|userPrincipalName}/messages
POST /me/mailFolders/{id}/messages
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages
```
## <a name="request-headers"></a><span data-ttu-id="9b0ae-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b0ae-118">Request headers</span></span>
| <span data-ttu-id="9b0ae-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b0ae-119">Header</span></span>       | <span data-ttu-id="9b0ae-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9b0ae-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9b0ae-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b0ae-121">Authorization</span></span>  | <span data-ttu-id="9b0ae-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="9b0ae-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9b0ae-124">Content-Type</span></span>  | <span data-ttu-id="9b0ae-125">application/json</span><span class="sxs-lookup"><span data-stu-id="9b0ae-125">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="9b0ae-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b0ae-126">Request body</span></span>
<span data-ttu-id="9b0ae-127">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="9b0ae-127">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>

<span data-ttu-id="9b0ae-128">Dado que el recurso **message** admite [extensiones](../../../concepts/extensibility_overview.md), puede utilizar la operación `POST` y agregar propiedades personalizadas con sus propios datos al mensaje al crearla.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-128">Since the **message** resource supports [extensions](../../../concepts/extensibility_overview.md), you can use the `POST` operation and add custom properties with your own data to the message while creating it.</span></span>

## <a name="response"></a><span data-ttu-id="9b0ae-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b0ae-129">Response</span></span>

<span data-ttu-id="9b0ae-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-130">If successful, this method returns `201, Created` response code and [message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9b0ae-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b0ae-131">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="9b0ae-132">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="9b0ae-132">Request 1</span></span>
<span data-ttu-id="9b0ae-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_message_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages
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
<span data-ttu-id="9b0ae-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="9b0ae-134">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>
##### <a name="response-1"></a><span data-ttu-id="9b0ae-135">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="9b0ae-135">Response 1</span></span>
<span data-ttu-id="9b0ae-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 201 Created
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

## <a name="see-also"></a><span data-ttu-id="9b0ae-139">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9b0ae-139">See also</span></span>

- [<span data-ttu-id="9b0ae-140">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="9b0ae-140">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="9b0ae-141">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="9b0ae-141">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
<!--
- [Add custom data to groups using schema extensions (preview)](../../../concepts/extensibility_schema_groups.md)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
