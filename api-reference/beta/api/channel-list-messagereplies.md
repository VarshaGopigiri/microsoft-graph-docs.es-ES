---
title: Respuestas de mensajes de canal de lista
description: Lista de todas las respuestas de un mensaje en un canal de un equipo.
author: nkramer
ms.openlocfilehash: ac0447e8c0e29e21b60b52c78362c22b0acbd5de
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27336634"
---
# <a name="list-channel-message-replies"></a><span data-ttu-id="b8a34-103">Respuestas de mensajes de canal de lista</span><span class="sxs-lookup"><span data-stu-id="b8a34-103">List channel message replies</span></span>

> <span data-ttu-id="b8a34-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b8a34-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b8a34-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b8a34-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b8a34-106">Lista de todas las respuestas de un [mensaje](../resources/chatmessage.md) en un [canal](../resources/channel.md) de un equipo.</span><span class="sxs-lookup"><span data-stu-id="b8a34-106">List all the replies of a [message](../resources/chatmessage.md) in a [channel](../resources/channel.md) of a team.</span></span>

## <a name="permissions"></a><span data-ttu-id="b8a34-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b8a34-107">Permissions</span></span>
<span data-ttu-id="b8a34-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b8a34-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b8a34-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b8a34-110">Permission Type</span></span>|<span data-ttu-id="b8a34-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b8a34-111">Permissions (from least to most privileged)</span></span>|
|---------|-------------|
|<span data-ttu-id="b8a34-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b8a34-112">Delegated (work or school account)</span></span>|<span data-ttu-id="b8a34-113">Group.Read.All,Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b8a34-113">Group.Read.All,Group.ReadWrite.All</span></span>|
|<span data-ttu-id="b8a34-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b8a34-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b8a34-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="b8a34-115">Not supported</span></span>|
|<span data-ttu-id="b8a34-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b8a34-116">Application</span></span>| <span data-ttu-id="b8a34-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b8a34-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b8a34-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b8a34-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}/channels/{id}/messages/{id}/replies
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b8a34-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b8a34-119">Optional query parameters</span></span>
<span data-ttu-id="b8a34-120">Los [Parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) actualmente no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="b8a34-120">The [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) are not currently supported.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b8a34-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b8a34-121">Request headers</span></span>
| <span data-ttu-id="b8a34-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8a34-122">Header</span></span>       | <span data-ttu-id="b8a34-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b8a34-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b8a34-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="b8a34-124">Authorization</span></span>  | <span data-ttu-id="b8a34-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b8a34-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b8a34-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b8a34-127">Request body</span></span>
<span data-ttu-id="b8a34-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b8a34-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b8a34-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8a34-129">Response</span></span>
<span data-ttu-id="b8a34-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [chatmessage](../resources/channel.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b8a34-130">If successful, this method returns a `200 OK` response code and a collection of [chatmessage](../resources/channel.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b8a34-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b8a34-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b8a34-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b8a34-132">Request</span></span>
<span data-ttu-id="b8a34-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b8a34-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_channel_message_replies"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}/messages/{id}/replies
```
##### <a name="response"></a><span data-ttu-id="b8a34-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8a34-134">Response</span></span>
<span data-ttu-id="b8a34-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b8a34-135">Here is an example of the response.</span></span> 

><span data-ttu-id="b8a34-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b8a34-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chatMessage",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

{
  "value": [
    {
        "id": "id-value",
        "replyToId": "id-value",
        "from" : {
            "user": { 
            "id":  "id-value",
            "displayName": "John Doe"
            }  
        },
        "etag": "id-value",
        "messageType": "message",
        "createdDateTime": "2018-07-09T07:40:20.152Z",
        "lastModifiedDateTime": "2018-07-09T07:40:20.152Z",
        "body": {
            "content": "This is a response to a message.",
            "contentType": "Text"
        },
        "attachments": [
          {
              "id": "5e32f195-168a-474f-a273-123123123",
              "contentType": "reference",
              "contentUrl": "https://test.sharepoint.com/sites/TestSite/Shared%20Documents/General/Test.txt",
              "content": null,
              "name": "Test.txt",
              "thumbnailUrl": null
          }
        ],
        "mentions": [
            {
                "type": "user",
                "id": "id-value ",
                "mentionText": "Test User"
            }
        ],
        "importance": "normal",
        "reactions": [
            {
                "reactionType": "like",
                "user": {
                    "id": "id-value",
                    "displayName": "John Doe"
                },
                "createdDateTime": "2018-07-09T07:40:20.152Z"
            }
        ],
        "locale": "en-us"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get channel message replies",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
