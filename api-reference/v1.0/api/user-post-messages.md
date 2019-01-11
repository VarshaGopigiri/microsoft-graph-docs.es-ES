---
title: Create Message
description: Use esta API para crear un mensaje. Pueden crearse borradores en cualquier carpeta y, si quiere, actualizarlos antes de enviarlos. Para guardar en la carpeta Borradores, use el acceso directo /messages.
localization_priority: Priority
ms.openlocfilehash: 151c555e1195fcef243879c638fa36015395dc20
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816236"
---
# <a name="create-message"></a><span data-ttu-id="ad330-105">Create Message</span><span class="sxs-lookup"><span data-stu-id="ad330-105">Create Message</span></span>

<span data-ttu-id="ad330-p102">Use esta API para crear un mensaje. Pueden crearse borradores en cualquier carpeta y, si quiere, actualizarlos antes de enviarlos. Para guardar en la carpeta Borradores, use el acceso directo /messages.</span><span class="sxs-lookup"><span data-stu-id="ad330-p102">Use this API to create a draft of a new message. Drafts can be created in any folder and optionally updated before sending. To save to the Drafts folder, use the /messages shortcut.</span></span>

<span data-ttu-id="ad330-109">Al crear el borrador en la misma llamada **POST**, puede incluir [datos adjuntos](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="ad330-109">While creating the draft in the same **POST** call, you can include an [attachment](../resources/attachment.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="ad330-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="ad330-110">Permissions</span></span>
<span data-ttu-id="ad330-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ad330-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ad330-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ad330-113">Permission type</span></span>      | <span data-ttu-id="ad330-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ad330-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ad330-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ad330-115">Delegated (work or school account)</span></span> | <span data-ttu-id="ad330-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ad330-116">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ad330-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ad330-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ad330-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ad330-118">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ad330-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ad330-119">Application</span></span> | <span data-ttu-id="ad330-120">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ad330-120">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ad330-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ad330-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages
POST /users/{id|userPrincipalName}/messages
POST /me/mailFolders/{id}/messages
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages
```
## <a name="request-headers"></a><span data-ttu-id="ad330-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ad330-122">Request headers</span></span>
| <span data-ttu-id="ad330-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad330-123">Header</span></span>       | <span data-ttu-id="ad330-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ad330-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ad330-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="ad330-125">Authorization</span></span>  | <span data-ttu-id="ad330-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ad330-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ad330-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ad330-128">Content-Type</span></span>  | <span data-ttu-id="ad330-129">application/json</span><span class="sxs-lookup"><span data-stu-id="ad330-129">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ad330-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ad330-130">Request body</span></span>
<span data-ttu-id="ad330-131">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="ad330-131">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>

<span data-ttu-id="ad330-132">Dado que el recurso **message** admite [extensiones](/graph/extensibility-overview), puede utilizar la operación `POST` y agregar propiedades personalizadas con sus propios datos al mensaje al crearla.</span><span class="sxs-lookup"><span data-stu-id="ad330-132">Since the **message** resource supports [extensions](/graph/extensibility-overview), you can use the `POST` operation and add custom properties with your own data to the message while creating it.</span></span>

## <a name="response"></a><span data-ttu-id="ad330-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad330-133">Response</span></span>

<span data-ttu-id="ad330-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad330-134">If successful, this method returns `201 Created` response code and [message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ad330-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad330-135">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="ad330-136">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="ad330-136">Request 1</span></span>
<span data-ttu-id="ad330-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ad330-137">Here is an example of the request.</span></span>
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
<span data-ttu-id="ad330-138">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="ad330-138">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>
##### <a name="response-1"></a><span data-ttu-id="ad330-139">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="ad330-139">Response 1</span></span>
<span data-ttu-id="ad330-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ad330-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request-2"></a><span data-ttu-id="ad330-143">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="ad330-143">Request 2</span></span>
<span data-ttu-id="ad330-144">En el ejemplo siguiente se agrega un par de encabezados de mensaje de Internet del cliente al crear el borrador del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ad330-144">The next example adds a couple of customer Internet message headers when creating the message draft.</span></span>
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
<span data-ttu-id="ad330-145">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="ad330-145">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>
##### <a name="response-2"></a><span data-ttu-id="ad330-146">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="ad330-146">Response 2</span></span>
<span data-ttu-id="ad330-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad330-147">Here is an example of the response.</span></span> <span data-ttu-id="ad330-148">Nota: No se devuelven los encabezados de mensaje de Internet de forma predeterminada en una respuesta POST.</span><span class="sxs-lookup"><span data-stu-id="ad330-148">Note: Internet message headers are not returned by default in a POST response.</span></span> <span data-ttu-id="ad330-149">También se puede truncar el objeto de respuesta que se muestra aquí por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="ad330-149">The response object shown here may also be truncated for brevity.</span></span> <span data-ttu-id="ad330-150">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ad330-150">All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="ad330-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad330-151">See also</span></span>

- [<span data-ttu-id="ad330-152">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="ad330-152">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="ad330-153">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="ad330-153">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
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
