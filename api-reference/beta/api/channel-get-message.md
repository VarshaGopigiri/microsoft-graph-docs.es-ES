---
title: Obtener el mensaje de canal
description: Recuperar un único mensaje (sin sus respuestas) en un canal de un equipo.
ms.openlocfilehash: dcafeeddf80f5a2313136291bf528b2cf9683036
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083627"
---
# <a name="get-channel-message"></a><span data-ttu-id="8732c-103">Obtener el mensaje de canal</span><span class="sxs-lookup"><span data-stu-id="8732c-103">Get channel message</span></span>

> <span data-ttu-id="8732c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8732c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8732c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8732c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8732c-106">Recuperar un único [mensaje](../resources/chatmessage.md) (sin sus respuestas) en un [canal](../resources/channel.md) de un equipo.</span><span class="sxs-lookup"><span data-stu-id="8732c-106">Retrieve a single [message](../resources/chatmessage.md) (without its replies) in a [channel](../resources/channel.md) of a team.</span></span>

## <a name="permissions"></a><span data-ttu-id="8732c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="8732c-107">Permissions</span></span>
<span data-ttu-id="8732c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8732c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8732c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8732c-110">Permission Type</span></span>|<span data-ttu-id="8732c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8732c-111">Permissions (from least to most privileged)</span></span>|
|---------|-------------|
|<span data-ttu-id="8732c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8732c-112">Delegated (work or school account)</span></span>|<span data-ttu-id="8732c-113">Group.Read.All,Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8732c-113">Group.Read.All,Group.ReadWrite.All</span></span>|
|<span data-ttu-id="8732c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8732c-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8732c-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="8732c-115">Not supported</span></span>|
|<span data-ttu-id="8732c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8732c-116">Application</span></span>| <span data-ttu-id="8732c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8732c-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8732c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8732c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}/channels/{id}/messages/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="8732c-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8732c-119">Optional query parameters</span></span>
<span data-ttu-id="8732c-120">Los [Parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) actualmente no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8732c-120">The [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) are not currently supported.</span></span>

## <a name="request-headers"></a><span data-ttu-id="8732c-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8732c-121">Request headers</span></span>
| <span data-ttu-id="8732c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8732c-122">Header</span></span>       | <span data-ttu-id="8732c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8732c-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="8732c-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="8732c-124">Authorization</span></span>  | <span data-ttu-id="8732c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8732c-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="8732c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8732c-127">Request body</span></span>
<span data-ttu-id="8732c-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8732c-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8732c-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8732c-129">Response</span></span>

<span data-ttu-id="8732c-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [chatmessage](../resources/chatmessage.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8732c-130">If successful, this method returns a `200 OK` response code and a collection of [chatmessage](../resources/chatmessage.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8732c-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8732c-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8732c-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8732c-132">Request</span></span>
<span data-ttu-id="8732c-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8732c-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_channel_message"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="8732c-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8732c-134">Response</span></span>
<span data-ttu-id="8732c-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8732c-135">Here is an example of the response.</span></span> 

><span data-ttu-id="8732c-136">**Nota:** El objeto de respuesta que se muestra aquí se acortan para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="8732c-136">**Note:** The response object shown here are shortened for readability.</span></span> <span data-ttu-id="8732c-137">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8732c-137">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chatMessage"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

{
  "id": "id-value",
  "replyToId": "id-value",
  "from": {
      "user": { 
        "id": "id-value",
        "displayName": "John Doe"
      }  
  },
  "etag": "id-value",
  "messageType": "message",
  "createdDateTime": "2018-07-09T07:40:20.152Z",
  "lastModifiedDateTime": "2018-07-09T07:40:20.152Z",
  "body": {
      "content": "Hello World",
      "contentType": "text"
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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get channel message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->