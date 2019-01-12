---
title: Obtener la llamada
description: Recuperar las propiedades y relaciones de un objeto de llamada.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 20243a003cccfc5b39e0aad600afa887e5803849
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966534"
---
# <a name="get-call"></a><span data-ttu-id="93abe-103">Obtener la llamada</span><span class="sxs-lookup"><span data-stu-id="93abe-103">Get call</span></span>

> <span data-ttu-id="93abe-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="93abe-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="93abe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="93abe-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="93abe-106">Recuperar las propiedades y relaciones de un objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="93abe-106">Retrieve the properties and relationships of a call object.</span></span>

## <a name="permissions"></a><span data-ttu-id="93abe-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="93abe-107">Permissions</span></span>
<span data-ttu-id="93abe-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="93abe-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="93abe-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="93abe-110">Permission type</span></span> | <span data-ttu-id="93abe-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="93abe-111">Permissions (from least to most privileged)</span></span>                  |
| :-------------- | :----------------------------------------------------------- |
| <span data-ttu-id="93abe-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="93abe-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="93abe-113">No se admite.</span><span class="sxs-lookup"><span data-stu-id="93abe-113">Not Supported.</span></span>                         |
| <span data-ttu-id="93abe-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="93abe-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="93abe-115">No se admite.</span><span class="sxs-lookup"><span data-stu-id="93abe-115">Not Supported.</span></span>                         |
| <span data-ttu-id="93abe-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="93abe-116">Application</span></span>                            | <span data-ttu-id="93abe-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="93abe-117">None.</span></span>                                  |

## <a name="http-request"></a><span data-ttu-id="93abe-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="93abe-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /app/calls/{id}
GET /applications/{id}/calls/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="93abe-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="93abe-119">Optional query parameters</span></span>
<span data-ttu-id="93abe-120">Este método es compatible con los [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93abe-120">This method supports the [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="93abe-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="93abe-121">Request headers</span></span>
| <span data-ttu-id="93abe-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="93abe-122">Name</span></span>          | <span data-ttu-id="93abe-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="93abe-123">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="93abe-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="93abe-124">Authorization</span></span> | <span data-ttu-id="93abe-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="93abe-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="93abe-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="93abe-127">Request body</span></span>
<span data-ttu-id="93abe-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="93abe-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="93abe-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93abe-129">Response</span></span>
<span data-ttu-id="93abe-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto en el cuerpo de la respuesta [de llamadas](../resources/call.md) .</span><span class="sxs-lookup"><span data-stu-id="93abe-130">If successful, this method returns a `200 OK` response code and a [call](../resources/call.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="93abe-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="93abe-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="93abe-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="93abe-132">Request</span></span>
<span data-ttu-id="93abe-133">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="93abe-133">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get-call"
}-->
```http
GET https://graph.microsoft.com/beta/app/calls/{id}
```

##### <a name="response"></a><span data-ttu-id="93abe-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93abe-134">Response</span></span>

> <span data-ttu-id="93abe-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="93abe-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.call"
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2821

{
  "activeModalities": [
    "unknown"
  ],
  "answeredBy": {
    "identity": {
      "user": {
        "id": "550fae72-d251-43ec-868c-373732c2704f",
        "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
        "displayName": "Heidi Steen"
      }
    },
    "languageId": "languageId-value",
    "region": "region-value"
  },
  "callRoutes": [
    {
      "final": {
        "user": {
          "id": "550fae72-d251-43ec-868c-373732c2704f",
          "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
          "displayName": "Heidi Steen"
        }
      },
      "original": {
        "phone": {
          "id": "+14258828080"
        }
      },
      "routingType": "forwarded"
    }
  ],
  "callbackUri": "callbackUri-value",
  "chatInfo": {
    "threadId": "19:meeting_M2IzYzczNTItYmY3OC00MDlmLWJjMzUtYmFiMjNlOTY4MGEz@thread.skype",
    "messageId": "0",
    "replyChainMessageId": "0"
  },
  "direction": "incoming",
  "id": "id-value",
  "mediaConfig": {
    "@odata.type": "#microsoft.graph.appHostedMediaConfig",
    "blob": "<media config blob>"
  },
  "meetingCapability": {
    "allowAnonymousUsersToDialOut": true,
    "allowAnonymousUsersToStartMeeting": true,
    "autoAdmittedUsers": "everyoneInCompany"
  },
  "meetingInfo": {
    "@odata.type": "#microsoft.graph.organizerMeetingInfo",
    "organizer": {
      "user": {
        "id": "550fae72-d251-43ec-868c-373732c2704f",
        "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
        "displayName": "Heidi Steen"
      }
    },
    "allowConversationWithoutHost": true
  },
  "myParticipantId": "myParticipantId-value",
  "requestedModalities": [
    "audio", "video"
  ],
  "ringingTimeoutInSeconds": 99,
  "routingPolicies": [
    "none"
  ],
  "source": {
    "identity": {
      "user": {
        "id": "550fae72-d251-43ec-868c-373732c2704f",
        "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
        "displayName": "Heidi Steen"
      }
    },
    "languageId": "languageId-value",
    "region": "region-value"
  },
  "state": "incoming",
  "subject": "subject-value",
  "targets": [
    {
      "identity": {
        "user": {
          "id": "550fae72-d251-43ec-868c-373732c2704f",
          "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
          "displayName": "Heidi Steen"
        }
      },
      "languageId": "languageId-value",
      "region": "region-value"
    }
  ],
  "tenantId": "tenantId-value",
  "terminationReason": "terminationReason-value",
  "toneInfo": {
    "sequenceId": 99,
    "tone": "tone0"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get call",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
