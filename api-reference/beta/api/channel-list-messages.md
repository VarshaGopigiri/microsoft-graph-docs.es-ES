---
title: Mensajes del canal de lista
description: 'Recuperar la lista de los mensajes (sin las respuestas) en un canal de un equipo. Para obtener las respuestas para un mensaje, llame a la lista de mensajes de respuesta o la respuesta de mensaje get API. '
localization_priority: Priority
ms.openlocfilehash: c972b84b0ec4de9389f8a0e861cafb74d7b23020
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867098"
---
# <a name="list-channel-messages"></a><span data-ttu-id="9b499-104">Mensajes del canal de lista</span><span class="sxs-lookup"><span data-stu-id="9b499-104">List channel messages</span></span>

> <span data-ttu-id="9b499-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b499-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b499-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b499-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9b499-107">Recuperar la lista de [los mensajes](../resources/chatmessage.md) (sin las respuestas) en un [canal](../resources/channel.md) de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="9b499-107">Retrieve the list of [messages](../resources/chatmessage.md) (without the replies) in a [channel](../resources/channel.md) of a [team](../resources/team.md).</span></span> <span data-ttu-id="9b499-108">Para obtener las respuestas para un mensaje, llame a las [respuestas de mensajes de la lista](channel-get-messagereply.md) o [obtener respuesta de mensaje](channel-list-messagereplies.md) API.</span><span class="sxs-lookup"><span data-stu-id="9b499-108">To get the replies for a message, call the [list message replies](channel-get-messagereply.md) or the [get message reply](channel-list-messagereplies.md) API.</span></span> 

## <a name="permissions"></a><span data-ttu-id="9b499-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b499-109">Permissions</span></span>
<span data-ttu-id="9b499-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b499-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9b499-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b499-112">Permission Type</span></span>|<span data-ttu-id="9b499-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b499-113">Permissions (from least to most privileged)</span></span>|
|---------|-------------|
|<span data-ttu-id="9b499-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b499-114">Delegated (work or school account)</span></span>|<span data-ttu-id="9b499-115">Group.Read.All,Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9b499-115">Group.Read.All,Group.ReadWrite.All</span></span>|
|<span data-ttu-id="9b499-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b499-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9b499-117">No admitido</span><span class="sxs-lookup"><span data-stu-id="9b499-117">Not supported</span></span>|
|<span data-ttu-id="9b499-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b499-118">Application</span></span>| <span data-ttu-id="9b499-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b499-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9b499-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b499-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}/channels/{id}/messages
```

## <a name="optional-query-parameters"></a><span data-ttu-id="9b499-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9b499-121">Optional query parameters</span></span>
<span data-ttu-id="9b499-122">Los [Parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) actualmente no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="9b499-122">The [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) are not currently supported.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9b499-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b499-123">Request headers</span></span>
| <span data-ttu-id="9b499-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b499-124">Header</span></span>       | <span data-ttu-id="9b499-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9b499-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9b499-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b499-126">Authorization</span></span>  | <span data-ttu-id="9b499-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b499-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="9b499-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b499-129">Request body</span></span>
<span data-ttu-id="9b499-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9b499-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9b499-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b499-131">Response</span></span>

<span data-ttu-id="9b499-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [chatmessage](../resources/channel.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b499-132">If successful, this method returns a `200 OK` response code and a collection of [chatmessage](../resources/channel.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9b499-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b499-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9b499-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b499-134">Request</span></span>
<span data-ttu-id="9b499-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b499-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_channel_messages"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}/messages
```
##### <a name="response"></a><span data-ttu-id="9b499-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b499-136">Response</span></span>
<span data-ttu-id="9b499-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b499-137">Here is an example of the response.</span></span> 

><span data-ttu-id="9b499-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b499-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
            "content": "Hello World",
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
  "description": "Get channel messages",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
