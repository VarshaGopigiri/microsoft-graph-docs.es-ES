---
title: 'message: move'
description: Mover un mensaje a una carpeta. Esto crea una nueva copia del mensaje en la carpeta de destino y quita el mensaje original.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 7ad9ac2b8f64d75950c9b2cac17a4c5dc5a9b3eb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843291"
---
# <a name="message-move"></a><span data-ttu-id="103d5-104">message: move</span><span class="sxs-lookup"><span data-stu-id="103d5-104">message: move</span></span>

> <span data-ttu-id="103d5-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="103d5-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="103d5-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="103d5-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="103d5-107">Mover un mensaje a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="103d5-107">Move a message to a folder.</span></span> <span data-ttu-id="103d5-108">Esto crea una nueva copia del mensaje en la carpeta de destino y quita el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="103d5-108">This creates a new copy of the message in the destination folder and removes the original message.</span></span>

## <a name="permissions"></a><span data-ttu-id="103d5-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="103d5-109">Permissions</span></span>

<span data-ttu-id="103d5-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="103d5-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="103d5-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="103d5-112">Permission type</span></span> | <span data-ttu-id="103d5-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="103d5-113">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="103d5-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="103d5-114">Delegated (work or school account)</span></span> | <span data-ttu-id="103d5-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="103d5-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="103d5-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="103d5-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="103d5-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="103d5-117">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="103d5-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="103d5-118">Application</span></span> | <span data-ttu-id="103d5-119">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="103d5-119">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="103d5-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="103d5-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/messages/{id}/move
POST /users/{id | userPrincipalName}/messages/{id}/move
POST /me/mailFolders/{id}/messages/{id}/move
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/move
```

## <a name="request-headers"></a><span data-ttu-id="103d5-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="103d5-121">Request headers</span></span>

| <span data-ttu-id="103d5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="103d5-122">Header</span></span> | <span data-ttu-id="103d5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="103d5-123">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="103d5-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="103d5-124">Authorization</span></span> | <span data-ttu-id="103d5-125">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="103d5-125"></span></span> <span data-ttu-id="103d5-126">Necesario.</span><span class="sxs-lookup"><span data-stu-id="103d5-126">Required.</span></span> |
| <span data-ttu-id="103d5-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="103d5-127">Content-Type</span></span> | <span data-ttu-id="103d5-128">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="103d5-128"></span></span> <span data-ttu-id="103d5-129">Necesario.</span><span class="sxs-lookup"><span data-stu-id="103d5-129">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="103d5-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="103d5-130">Request body</span></span>

<span data-ttu-id="103d5-131">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="103d5-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="103d5-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="103d5-132">Parameter</span></span>   | <span data-ttu-id="103d5-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="103d5-133">Type</span></span> |<span data-ttu-id="103d5-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="103d5-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="103d5-135">DestinationId</span><span class="sxs-lookup"><span data-stu-id="103d5-135">DestinationId</span></span>|<span data-ttu-id="103d5-136">String</span><span class="sxs-lookup"><span data-stu-id="103d5-136">String</span></span>|<span data-ttu-id="103d5-137">El identificador de la carpeta de destino, o un nombre de carpeta conocida.</span><span class="sxs-lookup"><span data-stu-id="103d5-137">The destination folder ID, or a well-known folder name.</span></span> <span data-ttu-id="103d5-138">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="103d5-138">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>|

## <a name="response"></a><span data-ttu-id="103d5-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="103d5-139">Response</span></span>

<span data-ttu-id="103d5-140">Si tiene éxito, este método devuelve `201 Created` código de respuesta y un recurso de [mensaje](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="103d5-140">If successful, this method returns `201 Created` response code and a [message](../resources/message.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="103d5-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="103d5-141">Example</span></span>

<span data-ttu-id="103d5-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="103d5-142">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="103d5-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="103d5-143">Request</span></span>

<span data-ttu-id="103d5-144">La solicitud siguiente mueve el mensaje especificado a la carpeta Elementos eliminados, identificada por su nombre de carpeta Well-known `deleteditems`.</span><span class="sxs-lookup"><span data-stu-id="103d5-144">The following request moves the specified message to the Deleted Items folder, identified by its well-known folder name `deleteditems`.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADhAAATs28OAAA="],
  "name": "message_move"
}-->

```http
POST https://graph.microsoft.com/beta/me/messages/AAMkADhAAATs28OAAA=/move
Content-type: application/json

{
  "destinationId": "deleteditems"
}
```

##### <a name="response"></a><span data-ttu-id="103d5-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="103d5-145">Response</span></span>

<span data-ttu-id="103d5-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="103d5-146">Here is an example of the response.</span></span>

> <span data-ttu-id="103d5-147">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="103d5-147">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="103d5-148">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="103d5-148">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#message",
    "@odata.type":"#microsoft.graph.message",
    "@odata.etag":"W/\"FwAAABYAAAC4ofQHEIqCSbQPot83AFcbAAAW/0tB\"",
    "id":"AAMkADhAAAW-VPeAAA=",
    "createdDateTime":"2018-08-12T08:43:22Z",
    "lastModifiedDateTime":"2018-08-15T19:47:54Z",
    "changeKey":"FwAAABYAAAC4ofQHEIqCSbQPot83AFcbAAAW/0tB",
    "categories":[

    ],
    "receivedDateTime":"2018-08-12T08:43:22Z",
    "sentDateTime":"2018-08-12T08:43:20Z",
    "hasAttachments":false,
    "internetMessageId":"<00535324-5988-4b6a-b9af-d44cf2d0b691@MWHPR2201MB1022.namprd22.prod.outlook.com>",
    "subject":"Undeliverable: Meet for lunch?",
    "bodyPreview":"Delivery has failed to these recipients or groups:\r\n\r\nfannyd@contoso.onmicrosoft.com (fannyd@contoso.onmicrosoft.com)\r\nYour message couldn't be delivered. Despite repeated attempts to deliver your message, querying the Domain Name System (DNS) for the rec",
    "importance":"normal",
    "parentFolderId":"AAMkADhAAAAAAEKAAA=",
    "conversationId":"AAQkADhJzfbkARFhe5kKhjihSA=",
    "isDeliveryReceiptRequested":null,
    "isReadReceiptRequested":false,
    "isRead":false,
    "isDraft":false,
    "webLink":"https://outlook.office365.com/owa/?ItemID=AAMkADhAAAW%2FVPeAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
    "inferenceClassification":"focused",
    "body":{
        "contentType":"html",
        "content":"<html></html>"
    },
    "sender":{
        "emailAddress":{
            "name":"Microsoft Outlook",
            "address":"MicrosoftExchange329e71ec88ae4615bbc36ab6ce41109e@contoso.onmicrosoft.com"
        }
    },
    "from":{
        "emailAddress":{
            "name":"Microsoft Outlook",
            "address":"MicrosoftExchange329e71ec88ae4615bbc36ab6ce41109e@contoso.onmicrosoft.com"
        }
    },
    "toRecipients":[
        {
            "emailAddress":{
                "name":"fannyd@contoso.onmicrosoft.com",
                "address":"fannyd@contoso.onmicrosoft.com"
            }
        },
        {
            "emailAddress":{
                "name":"danas@contoso.onmicrosoft.com",
                "address":"danas@contoso.onmicrosoft.com"
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: move",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
