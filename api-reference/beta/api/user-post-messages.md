---
title: Create Message
description: Use esta API para crear un mensaje. Pueden crearse borradores en cualquier carpeta y, si quiere, actualizarlos antes de enviarlos. Para guardar en la carpeta Borradores, use el acceso directo /messages.
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 95fb4c385da7115480a2e1e63135bd875a80b598
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952905"
---
# <a name="create-message"></a><span data-ttu-id="b4404-105">Create Message</span><span class="sxs-lookup"><span data-stu-id="b4404-105">Create Message</span></span>

> <span data-ttu-id="b4404-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b4404-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b4404-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b4404-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b4404-p103">Use esta API para crear un mensaje. Pueden crearse borradores en cualquier carpeta y, si quiere, actualizarlos antes de enviarlos. Para guardar en la carpeta Borradores, use el acceso directo /messages.</span><span class="sxs-lookup"><span data-stu-id="b4404-p103">Use this API to create a draft of a new message. Drafts can be created in any folder and optionally updated before sending. To save to the Drafts folder, use the /messages shortcut.</span></span>

<span data-ttu-id="b4404-111">Al crear el borrador en la misma llamada **POST** , se puede:</span><span class="sxs-lookup"><span data-stu-id="b4404-111">While creating the draft in the same **POST** call, you can:</span></span>

- <span data-ttu-id="b4404-112">Incluir [datos adjuntos](../resources/attachment.md)</span><span class="sxs-lookup"><span data-stu-id="b4404-112">Include an [attachment](../resources/attachment.md)</span></span> 
- <span data-ttu-id="b4404-113">Use un [mencione](../resources/mention.md) para llamar a otro usuario en el nuevo mensaje</span><span class="sxs-lookup"><span data-stu-id="b4404-113">Use a [mention](../resources/mention.md) to call out another user in the new message</span></span>

## <a name="permissions"></a><span data-ttu-id="b4404-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="b4404-114">Permissions</span></span>
<span data-ttu-id="b4404-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b4404-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b4404-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b4404-117">Permission type</span></span>      | <span data-ttu-id="b4404-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b4404-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b4404-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b4404-119">Delegated (work or school account)</span></span> | <span data-ttu-id="b4404-120">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b4404-120">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="b4404-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b4404-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b4404-122">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b4404-122">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="b4404-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b4404-123">Application</span></span> | <span data-ttu-id="b4404-124">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b4404-124">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="b4404-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b4404-125">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages
POST /users/{id|userPrincipalName}/messages
POST /me/mailFolders/{id}/messages
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages
```
## <a name="request-headers"></a><span data-ttu-id="b4404-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b4404-126">Request headers</span></span>
| <span data-ttu-id="b4404-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4404-127">Header</span></span>       | <span data-ttu-id="b4404-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b4404-128">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b4404-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="b4404-129">Authorization</span></span>  | <span data-ttu-id="b4404-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b4404-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="b4404-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b4404-132">Content-Type</span></span>  | <span data-ttu-id="b4404-133">application/json</span><span class="sxs-lookup"><span data-stu-id="b4404-133">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b4404-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b4404-134">Request body</span></span>
<span data-ttu-id="b4404-135">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [mensaje](../resources/message.md) .</span><span class="sxs-lookup"><span data-stu-id="b4404-135">In the request body, supply a JSON representation of the [message](../resources/message.md) object.</span></span>

<span data-ttu-id="b4404-136">Si desea usar **mencione** para llamar a otro usuario en el nuevo mensaje:</span><span class="sxs-lookup"><span data-stu-id="b4404-136">If you want to use **mention** to call out another user in the new message:</span></span>

- <span data-ttu-id="b4404-137">Incluir la propiedad necesario **toRecipients** , la propiedad **menciones** y las propiedades de mensaje puede escribir en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b4404-137">Include the required **toRecipients** property, the **mentions** property, and any writable message properties in the request body.</span></span>
- <span data-ttu-id="b4404-138">Para cada mención en la propiedad **menciones** , debe especificar la propiedad **que se mencionan** .</span><span class="sxs-lookup"><span data-stu-id="b4404-138">For each mention in the **mentions** property, you must specify the **mentioned** property.</span></span>

<span data-ttu-id="b4404-139">Dado que el recurso **message** admite [extensiones](/graph/extensibility-overview), puede utilizar la operación `POST` y agregar propiedades personalizadas con sus propios datos al mensaje al crearla.</span><span class="sxs-lookup"><span data-stu-id="b4404-139">Since the **message** resource supports [extensions](/graph/extensibility-overview), you can use the `POST` operation and add custom properties with your own data to the message while creating it.</span></span>

## <a name="response"></a><span data-ttu-id="b4404-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4404-140">Response</span></span>

<span data-ttu-id="b4404-141">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto de [mensaje](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b4404-141">If successful, this method returns a `201 Created` response code and a [message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b4404-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4404-142">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="b4404-143">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="b4404-143">Request 1</span></span>
<span data-ttu-id="b4404-144">Este es un ejemplo de la solicitud para crear un borrador de un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="b4404-144">Here is an example of the request to create a draft of a new message.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_message_from_user"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages
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
<span data-ttu-id="b4404-145">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="b4404-145">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>
##### <a name="response-1"></a><span data-ttu-id="b4404-146">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="b4404-146">Response 1</span></span>
<span data-ttu-id="b4404-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b4404-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('ad787b4f-1fda-4523-8e48-ffedb7f4635f')/messages/$entity",
    "@odata.etag":"W/\"CQAAABYAAAAmXr9SsE/UR4PcnTZcg7qWAAAFS12t\"",
    "id":"AAMkAGRWAAAFSmKXAAA=",
    "createdDateTime":"2017-12-23T07:29:57Z",
    "lastModifiedDateTime":"2017-12-23T07:29:58Z",
    "changeKey":"CQAAABYAAAAmXr9SsE/UR4PcnTZcg7qWAAAFS12t",
    "categories":[

    ],
    "receivedDateTime":"2017-12-23T07:29:58Z",
    "sentDateTime":"2017-12-23T07:29:58Z",
    "hasAttachments":false,
    "internetMessageId":"<MWHPR130@MWHPR130.namprd13.prod.outlook.com>",
    "subject":"Did you see last night's game?",
    "bodyPreview":"They were awesome!",
    "importance":"low",
    "parentFolderId":"AAMkAGRWAAAAAAEPAAA=",
    "conversationId":"AAQkAGRVYAsRJrRdc_mWNaxU=",
    "conversationIndex":"AQHTe7/VAniOJVgCxEmtF1z6ZY1rFQ==",
    "isDeliveryReceiptRequested":false,
    "isReadReceiptRequested":false,
    "isRead":true,
    "isDraft":true,
    "webLink":"https://outlook.office365.com/owa/?ItemID=AAMkAGRWAAAFSmKXAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
    "inferenceClassification":"focused",
    "unsubscribeData":[

    ],
    "unsubscribeEnabled":false,
    "mentionsPreview":null,
    "body":{
        "contentType":"html",
        "content":"<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<meta content=\"text/html; charset=us-ascii\">\r\n</head>\r\n<body>\r\nThey were <b>awesome</b>!\r\n</body>\r\n</html>\r\n"
    },
    "toRecipients":[
        {
            "emailAddress":{
                "name":"AdeleV@contoso.onmicrosoft.com",
                "address":"AdeleV@contoso.onmicrosoft.com"
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

##### <a name="request-2"></a><span data-ttu-id="b4404-150">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="b4404-150">Request 2</span></span>
<span data-ttu-id="b4404-151">En el ejemplo siguiente se muestra un correo electrónico de borrador por Randi Welch a Samantha Booth.</span><span class="sxs-lookup"><span data-stu-id="b4404-151">The next example shows a draft email by Randi Welch to Samantha Booth.</span></span> <span data-ttu-id="b4404-152">El mensaje también incluye una mención de otro usuario, Dana Swope.</span><span class="sxs-lookup"><span data-stu-id="b4404-152">The message also includes a mention of another user, Dana Swope.</span></span>

<span data-ttu-id="b4404-153">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="b4404-153">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_message_with_mentions_from_user"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages
Content-type: application/json

{
    "subject": "Party planning",
    "toRecipients":[
      {
          "emailAddress":{
              "name":"Samantha Booth",
              "address":"samanthab@contoso.onmicrosoft.com"
          }
      }
    ],
    "mentions":[
      {    
        "mentioned":{
          "name":"Dana Swope",
          "address":"danas@contoso.onmicrosoft.com"
         }
      }
    ]
}
```


##### <a name="response-2"></a><span data-ttu-id="b4404-154">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="b4404-154">Response 2</span></span>
<span data-ttu-id="b4404-p108">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b4404-p108">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#me/Messages/$entity",
  "@odata.id":"https://graph.microsoft.com/beta/users('266efe5a-0fd7-4edd-877b-b2d1e561f193@ae01a323-3934-4475-a32d-af1274312bb0')/messages('AQMkADJmMTUAAAW1fsAAAAA==')",
  "@odata.etag":"W/\"CQAAABYAAAAPFhK2FclcRbABBJhCde8iAAAAbYj7\"",
  "id":"AQMkADJmMTUAAAW1fsAAAAA==",
  "body":{
    "contentType":"Text",
    "content":""
  },
  "bodyPreview":"",
  "sender":null,
  "from":null,
  "subject": "Party planning",
  "toRecipients":[
    {
      "emailAddress":{
        "name":"Samantha Booth",
        "address":"samanthab@contoso.onmicrosoft.com"
      }
    }
  ],
  "mentionsPreview":{
    "isMentioned":false
  },
  "mentions@odata.context":"https://graph.microsoft.com/beta/$metadata#me/messages('AQMkADJmMTUAAAW1fsAAAAA%3D%3D')/mentions",
  "mentions":[
    {
      "@odata.id":"https://graph.microsoft.com/beta/users('266efe5a-0fd7-4edd-877b-b2d1e561f193@ae01a323-3934-4475-a32d-af1274312bb0')/messages('AQMkADJmMTUAAAW1fsAAAAA==')/mentions('4577bba4-b063-4cea-9073-6f7ca815fcec')",
      "id":"4577bba4-b063-4cea-9073-6f7ca815fcec",
      "mentioned":{
        "name":"Dana Swope",
        "address":"danas@contoso.onmicrosoft.com"
      },
      "mentionText":null,
      "clientReference":null,
      "createdBy":{
        "name":"Randi Welch",
        "address":"randiw@contoso.onmicrosoft.com"
      },
      "createdDateTime":"2016-07-22T02:22:44Z",
      "serverCreatedDateTime":"2016-07-22T02:22:44.201Z",
      "deepLink":null,
      "application":null
    }
  ]
}

```

##### <a name="request-3"></a><span data-ttu-id="b4404-158">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="b4404-158">Request 3</span></span>
<span data-ttu-id="b4404-159">En el ejemplo siguiente se agrega un par de encabezados de mensaje de Internet del cliente al crear el borrador del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b4404-159">The next example adds a couple of customer Internet message headers when creating the message draft.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_message_with_headers_from_user"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages
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
<span data-ttu-id="b4404-160">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="b4404-160">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>
##### <a name="response-3"></a><span data-ttu-id="b4404-161">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="b4404-161">Response 3</span></span>
<span data-ttu-id="b4404-162">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b4404-162">Here is an example of the response.</span></span> <span data-ttu-id="b4404-163">Nota: No se devuelven los encabezados de mensaje de Internet de forma predeterminada en una respuesta POST.</span><span class="sxs-lookup"><span data-stu-id="b4404-163">Note: Internet message headers are not returned by default in a POST response.</span></span> <span data-ttu-id="b4404-164">También se puede truncar el objeto de respuesta que se muestra aquí por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="b4404-164">The response object shown here may also be truncated for brevity.</span></span> <span data-ttu-id="b4404-165">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b4404-165">All of the properties will be returned from an actual call.</span></span>
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
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('7f180cbb-a5ae-457c-b7e8-6f5b42ba33e7')/messages/$entity",
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
    "unsubscribeData":[

    ],
    "unsubscribeEnabled":false,
    "mentionsPreview":null,
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

## <a name="see-also"></a><span data-ttu-id="b4404-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4404-166">See also</span></span>

- [<span data-ttu-id="b4404-167">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="b4404-167">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="b4404-168">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="b4404-168">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="b4404-169">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="b4404-169">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
