# <a name="create-message"></a><span data-ttu-id="8a5b0-101">Crear mensaje</span><span class="sxs-lookup"><span data-stu-id="8a5b0-101">Create Message</span></span>

<span data-ttu-id="8a5b0-p101">Use esta API para crear un mensaje. Pueden crearse borradores en cualquier carpeta y, si quiere, actualizarlos antes de enviarlos. Para guardar en la carpeta Borradores, use el acceso directo /messages.</span><span class="sxs-lookup"><span data-stu-id="8a5b0-p101">Use this API to create a draft of a new message. Drafts can be created in any folder and optionally updated before sending. To save to the Drafts folder, use the /messages shortcut.</span></span>

<span data-ttu-id="8a5b0-105">Al crear el borrador en la misma llamada **POST**, puede incluir [datos adjuntos](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="8a5b0-105">While creating the draft in the same **POST** call, you can include an [attachment](../resources/attachment.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="8a5b0-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="8a5b0-106">Permissions</span></span>
<span data-ttu-id="8a5b0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8a5b0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8a5b0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8a5b0-109">Permission type</span></span>      | <span data-ttu-id="8a5b0-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8a5b0-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8a5b0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8a5b0-111">Delegated (work or school account)</span></span> | <span data-ttu-id="8a5b0-112">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8a5b0-112">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="8a5b0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8a5b0-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8a5b0-114">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8a5b0-114">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="8a5b0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8a5b0-115">Application</span></span> | <span data-ttu-id="8a5b0-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8a5b0-116">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="8a5b0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a5b0-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages
POST /users/{id|userPrincipalName}/messages
POST /me/mailFolders/{id}/messages
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages
```
## <a name="request-headers"></a><span data-ttu-id="8a5b0-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a5b0-118">Request headers</span></span>
| <span data-ttu-id="8a5b0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a5b0-119">Header</span></span>       | <span data-ttu-id="8a5b0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8a5b0-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="8a5b0-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="8a5b0-121">Authorization</span></span>  | <span data-ttu-id="8a5b0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a5b0-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="8a5b0-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8a5b0-124">Content-Type</span></span>  | <span data-ttu-id="8a5b0-125">application/json</span><span class="sxs-lookup"><span data-stu-id="8a5b0-125">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="8a5b0-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a5b0-126">Request body</span></span>
<span data-ttu-id="8a5b0-127">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="8a5b0-127">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>

<span data-ttu-id="8a5b0-128">Dado que el recurso **message** admite [extensiones](../../../concepts/extensibility_overview.md), puede utilizar la operación `POST` y agregar propiedades personalizadas con sus propios datos al mensaje al crearla.</span><span class="sxs-lookup"><span data-stu-id="8a5b0-128">Since the **message** resource supports [extensions](../../../concepts/extensibility_overview.md), you can use the `POST` operation and add custom properties with your own data to the message while creating it.</span></span>

## <a name="response"></a><span data-ttu-id="8a5b0-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a5b0-129">Response</span></span>

<span data-ttu-id="8a5b0-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a5b0-130">If successful, this method returns `201 Created` response code and [message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8a5b0-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a5b0-131">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="8a5b0-132">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="8a5b0-132">Request 1</span></span>
<span data-ttu-id="8a5b0-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a5b0-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_message_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages
Content-type: application/json

{
    "subject":"Did you see last night's game?",
    "importance":"Low",
    "body":{
        "contentType":"HTML",
        "content":"They were <b>awesome</b>!"
    },
    "toRecipients":[
        {
            "emailAddress":{
                "address":"AdeleV@contoso.onmicrosoft.com"
            }
        }
    ]
}
```
<span data-ttu-id="8a5b0-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="8a5b0-134">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>
##### <a name="response-1"></a><span data-ttu-id="8a5b0-135">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="8a5b0-135">Response 1</span></span>
<span data-ttu-id="8a5b0-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8a5b0-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "name": "create_message_from_user",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('94447c6e-ea4c-494c-a9ed-d905e366c5cb')/messages/$entity",
    "@odata.etag":"W/\"CQAAABYAAABK4UfANE/UR5clSilZtIuWAAC1vdti\"",
    "id":"AAMkADNlNYjSAAA=",
    "createdDateTime":"2017-07-22T01:53:56Z",
    "lastModifiedDateTime":"2017-07-22T01:53:57Z",
    "changeKey":"CQAAABYAAABK4UfANE/UR5clSilZtIuWAAC1vdti",
    "categories":[

    ],
    "receivedDateTime":"2017-07-22T01:53:57Z",
    "sentDateTime":"2017-07-22T01:53:57Z",
    "hasAttachments":false,
    "internetMessageId":"<MWHPR1301MB@MWHPR1301MB.namprd13.prod.outlook.com>",
    "subject":"Did you see last night's game?",
    "bodyPreview":"They were awesome!",
    "importance":"low",
    "parentFolderId":"AAMkADNlNWAAAAAAEPAAA=",
    "conversationId":"AAQkADNlNFdXGBnqtY=",
    "isDeliveryReceiptRequested":false,
    "isReadReceiptRequested":false,
    "isRead":true,
    "isDraft":true,
    "webLink":"https://outlook.office365.com/owa/?ItemID=AAMkADNlNYjSAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
    "inferenceClassification":"focused",
    "body":{
        "contentType":"html",
        "content":"<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<meta content=\"text/html; charset=us-ascii\">\r\n</head>\r\n<body>\r\nThey were <b>awesome</b>!\r\n</body>\r\n</html>\r\n"
    },
    "toRecipients":[
        {
            "emailAddress":{
                "name":"Adele Vance",
                "address":"AdeleV@contoso.onmicrosoft.com"
            }
        }
    ],
    "ccRecipients":[

    ],
    "bccRecipients":[

    ],
    "replyTo":[

    ]
}
```

##### <a name="request-2"></a><span data-ttu-id="8a5b0-139">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="8a5b0-139">Request 2</span></span>
<span data-ttu-id="8a5b0-140">En el ejemplo siguiente se agrega un par de encabezados de mensaje de Internet del cliente al crear el borrador del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8a5b0-140">The next example adds a couple of customer Internet message headers when creating the message draft.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_message_with_headers_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages
Content-type: application/json

{
    "subject":"9/8/2018: concert",
    "body":{
        "contentType":"HTML",
        "content":"The group represents Washington."
    },
    "toRecipients":[
        {
            "emailAddress":{
                "address":"AlexW@contoso.OnMicrosoft.com"
            }
        }
    ],
    "internetMessageHeaders":[
        {
            "name":"x-custom-header-group-name",
            "value":"Washington"
        },
        {
            "name":"x-custom-header-group-id",
            "value":"WA001"
        }
    ]
}
```
<span data-ttu-id="8a5b0-141">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="8a5b0-141">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>
##### <a name="response-2"></a><span data-ttu-id="8a5b0-142">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="8a5b0-142">Response 2</span></span>
<span data-ttu-id="8a5b0-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a5b0-143">Here is an example of the response.</span></span> <span data-ttu-id="8a5b0-144">Nota: En una respuesta POST no se devuelven de forma predeterminada los encabezados de mensaje de Internet.</span><span class="sxs-lookup"><span data-stu-id="8a5b0-144">Note: Internet message headers are not returned by default in a POST response.</span></span> <span data-ttu-id="8a5b0-145">Es posible que el objeto de respuesta que se muestra aquí esté truncado por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="8a5b0-145">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="8a5b0-146">En una llamada real se devolverán todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="8a5b0-146">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "name": "create_message_with_headers_from_user",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('7f180cbb-a5ae-457c-b7e8-6f5b42ba33e7')/messages/$entity",
    "@odata.etag":"W/\"CQAAABYAAAC4ofQHEIqCSbQPot83AFcbAAAnjjuE\"",
    "id":"AAMkADhNmAAA=",
    "createdDateTime":"2018-09-09T02:54:56Z",
    "lastModifiedDateTime":"2018-09-09T02:54:56Z",
    "changeKey":"CQAAABYAAAC4ofQHEIqCSbQPot83AFcbAAAnjjuE",
    "categories":[

    ],
    "receivedDateTime":"2018-09-09T02:54:56Z",
    "sentDateTime":"2018-09-09T02:54:56Z",
    "hasAttachments":false,
    "internetMessageId":"<MWHPR220MB1120.namprd22.prod.outlook.com>",
    "subject":"9/8/2018: concert",
    "bodyPreview":"The group represents Washington.",
    "importance":"normal",
    "parentFolderId":"AAMkADhAAAAAAEPAAA=",
    "conversationId":"AAQkADhNCuP8OKSm-0NE=",
    "isDeliveryReceiptRequested":false,
    "isReadReceiptRequested":false,
    "isRead":true,
    "isDraft":true,
    "webLink":"https://outlook.office365.com/owa/?ItemID=AAMkADhNmAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
    "inferenceClassification":"focused",
    "body":{
        "contentType":"html",
        "content":"<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<meta content=\"text/html; charset=us-ascii\">\r\n</head>\r\n<body>\r\nThe group represents Washington.\r\n</body>\r\n</html>\r\n"
    },
    "toRecipients":[
        {
            "emailAddress":{
                "name":"Alex Wilber",
                "address":"AlexW@contoso.OnMicrosoft.com"
            }
        }
    ],
    "ccRecipients":[

    ],
    "bccRecipients":[

    ],
    "replyTo":[

    ],
    "flag":{
        "flagStatus":"notFlagged"
    }
}
```

## <a name="see-also"></a><span data-ttu-id="8a5b0-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8a5b0-147">See also</span></span>

- [<span data-ttu-id="8a5b0-148">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="8a5b0-148">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="8a5b0-149">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="8a5b0-149">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
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
