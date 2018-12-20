---
title: Get de reunión en línea
description: Recuperar las propiedades y relaciones de un objeto **onlineMeeting** .
author: VinodRavichandran
ms.openlocfilehash: bfae4273aba0583e6c10a7e10f9c67865326bacf
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380383"
---
# <a name="get-online-meeting"></a><span data-ttu-id="1c662-103">Get de reunión en línea</span><span class="sxs-lookup"><span data-stu-id="1c662-103">Get Online Meeting</span></span>

> <span data-ttu-id="1c662-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1c662-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1c662-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1c662-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1c662-106">Recuperar las propiedades y relaciones de un objeto **onlineMeeting** .</span><span class="sxs-lookup"><span data-stu-id="1c662-106">Retrieve the properties and relationships of an **onlineMeeting** object.</span></span>

> <span data-ttu-id="1c662-107">**Nota:** El `GET` método se limita a un [identificador de conferencia VTC](https://docs.microsoft.com/microsoftteams/cloud-video-interop-for-teams-set-up). Estos identificadores se generan para la interoperabilidad de vídeo en la nube con licencia a los usuarios y se usa este método para obtener los detalles para unirse a la reunión.</span><span class="sxs-lookup"><span data-stu-id="1c662-107">**Note:** The `GET` method is limited to a [VTC conference id](https://docs.microsoft.com/microsoftteams/cloud-video-interop-for-teams-set-up). These IDs are generated for Cloud-Video-Interop licensed users and this method is used to get the details to join the meeting.</span></span>
> <span data-ttu-id="1c662-108">Para los flujos de regulares, puede usar el robot el `joinURL` para unirse a una reunión y ninguna búsqueda es necesario.</span><span class="sxs-lookup"><span data-stu-id="1c662-108">For regular flows, the bot can use the `joinURL` to join a meeting and no lookup is necessary.</span></span>

## <a name="permissions"></a><span data-ttu-id="1c662-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="1c662-109">Permissions</span></span>

<span data-ttu-id="1c662-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1c662-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="1c662-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1c662-112">Permission type</span></span>                        | <span data-ttu-id="1c662-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1c662-113">Permissions (from least to most privileged)</span></span>           |
|:---------------------------------------|:------------------------------------------------------|
| <span data-ttu-id="1c662-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1c662-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="1c662-115">No se admite.</span><span class="sxs-lookup"><span data-stu-id="1c662-115">Not Supported.</span></span>                                        |
| <span data-ttu-id="1c662-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1c662-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1c662-117">No se admite.</span><span class="sxs-lookup"><span data-stu-id="1c662-117">Not Supported.</span></span>                                        |
| <span data-ttu-id="1c662-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1c662-118">Application</span></span>                            | <span data-ttu-id="1c662-119">OnlineMeetings.Read.All, OnlineMeetings.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1c662-119">OnlineMeetings.Read.All, OnlineMeetings.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="1c662-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1c662-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /app/onlineMeetings/{id}
GET /applications/{id}/onlineMeetings/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="1c662-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1c662-121">Optional query parameters</span></span>
<span data-ttu-id="1c662-122">Este método es compatible con los [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c662-122">This method supports the [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1c662-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1c662-123">Request headers</span></span>
| <span data-ttu-id="1c662-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="1c662-124">Name</span></span>          | <span data-ttu-id="1c662-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c662-125">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="1c662-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="1c662-126">Authorization</span></span> | <span data-ttu-id="1c662-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1c662-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1c662-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1c662-129">Request body</span></span>
<span data-ttu-id="1c662-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1c662-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1c662-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c662-131">Response</span></span>
<span data-ttu-id="1c662-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [onlineMeeting](../resources/onlinemeeting.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c662-132">If successful, this method returns a `200 OK` response code and [onlineMeeting](../resources/onlinemeeting.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1c662-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1c662-133">Example</span></span>

##### <a name="request"></a><span data-ttu-id="1c662-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1c662-134">Request</span></span>
<span data-ttu-id="1c662-135">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1c662-135">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get-onlineMeeting"
}-->
```http
GET https://graph.microsoft.com/beta/app/onlineMeetings/{id}
```

##### <a name="response"></a><span data-ttu-id="1c662-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c662-136">Response</span></span>

> <span data-ttu-id="1c662-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1c662-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onlineMeeting"
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1574

{
  "accessLevel": "everyone",
  "audioConferencing": {
    "tollNumber": "+12525634478",
    "tollFreeNumber": "+18666390588",
    "participantPasscode": "2425999",
    "leaderPasscode": null,
    "dialinUrl": "https://dialin.teams.microsoft.com/22f12fa0-499f-435b-bc69-b8de580ba330?id=2425999"
  },
  "canceledDateTime": "2018-03-19T09:46:02Z",
  "chatInfo": {
    "threadId": "19:meeting_M2IzYzczNTItYmY3OC00MDlmLWJjMzUtYmFiMjNlOTY4MGEz@thread.skype",
    "messageId": "0",
    "replyChainMessageId": "0"
  },
  "creationDateTime": "2018-03-19T09:46:02Z",
  "endDateTime": "2018-03-19T09:46:02Z",
  "entryExitAnnouncement": true,
  "expirationDateTime": "2018-03-19T09:46:02Z",
  "id": "013448345",
  "isCancelled": false,
  "joinUrl": "https://teams.microsoft.com/l/meetup-join/19%3ameeting_M2IzYzczNTItYmY3OC00MDlmLWJjMzUtYmFiMjNlOTY4MGEz%40thread.skype/0?context=%7b%22Tid%22%3a%2272f988bf-86f1-41af-91ab-2d7cd011db47%22%2c%22Oid%22%3a%22550fae72-d251-43ec-868c-373732c2704f%22%7d",
  "meetingType": "scheduled",
  "participants": {
    "attendees": [
      {
        "identity": {
          "user": {
            "id": "550fae72-d251-43ec-868c-373732c2704f",
            "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
            "displayName": "Heidi Steen"
          }
        },
        "upn": "upn-value"
      }
    ],
    "organizer": {
      "identity": {
        "user": {
          "id": "550fae72-d251-43ec-868c-373732c2704f",
          "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
          "displayName": "Heidi Steen"
        }
      },
      "upn": "upn-value"
    }
  },
  "startDateTime": "2018-03-19T09:46:02Z",
  "subject": "Quarterly sales numbers"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get onlineMeeting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
