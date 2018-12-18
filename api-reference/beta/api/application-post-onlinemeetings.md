---
title: Crear reunión en línea
description: Crea una reunión en línea en nombre de un usuario especificado en el cuerpo de la solicitud.
author: lleonard-msft
ms.openlocfilehash: 4a68e25156353b41c3ff43685d7b021a2454a927
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331433"
---
# <a name="create-online-meeting"></a><span data-ttu-id="0878a-103">Crear reunión en línea</span><span class="sxs-lookup"><span data-stu-id="0878a-103">Create online meeting</span></span>

> <span data-ttu-id="0878a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0878a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0878a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0878a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0878a-106">Crea una reunión en línea en nombre de un usuario especificado en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0878a-106">Creates an online meeting on behalf of a user specified in the request body.</span></span>

> <span data-ttu-id="0878a-107">**Nota**: no mostrar la reunión en el calendario del usuario.</span><span class="sxs-lookup"><span data-stu-id="0878a-107">**Note**: The meeting does not show on the user's calendar.</span></span>

## <a name="permissions"></a><span data-ttu-id="0878a-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="0878a-108">Permissions</span></span>
<span data-ttu-id="0878a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0878a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="0878a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0878a-111">Permission type</span></span>                        | <span data-ttu-id="0878a-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0878a-112">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="0878a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0878a-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="0878a-114">No se admite</span><span class="sxs-lookup"><span data-stu-id="0878a-114">Not Supported</span></span>                               |
| <span data-ttu-id="0878a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0878a-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0878a-116">No se admite</span><span class="sxs-lookup"><span data-stu-id="0878a-116">Not Supported</span></span>                               |
| <span data-ttu-id="0878a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0878a-117">Application</span></span>                            | <span data-ttu-id="0878a-118">OnlineMeetings.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0878a-118">OnlineMeetings.ReadWrite.All</span></span>                |

## <a name="http-request"></a><span data-ttu-id="0878a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0878a-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/onlineMeetings
POST /applications/{id}/onlineMeetings
```

## <a name="request-headers"></a><span data-ttu-id="0878a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0878a-120">Request headers</span></span>
| <span data-ttu-id="0878a-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="0878a-121">Name</span></span>          | <span data-ttu-id="0878a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="0878a-122">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="0878a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="0878a-123">Authorization</span></span> | <span data-ttu-id="0878a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0878a-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0878a-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0878a-126">Request body</span></span>
<span data-ttu-id="0878a-127">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [onlineMeeting](../resources/onlinemeeting.md) .</span><span class="sxs-lookup"><span data-stu-id="0878a-127">In the request body, supply a JSON representation of an [onlineMeeting](../resources/onlinemeeting.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="0878a-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0878a-128">Response</span></span>
<span data-ttu-id="0878a-129">Si tiene éxito, este método devuelve `201 Created` código de respuesta y un objeto [onlineMeeting](../resources/onlinemeeting.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0878a-129">If successful, this method returns `201 Created` response code and an [onlineMeeting](../resources/onlinemeeting.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0878a-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0878a-130">Example</span></span>

##### <a name="request"></a><span data-ttu-id="0878a-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0878a-131">Request</span></span>
<span data-ttu-id="0878a-132">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0878a-132">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_onlineMeeting_from_application"
}-->
```http
POST https://graph.microsoft.com/beta/app/onlineMeetings
Content-Type: application/json
Content-Length: 1553

{
  "meetingType": "meetNow",
  "participants": {
    "organizer": {
      "identity": {
        "user": {
          "id": "550fae72-d251-43ec-868c-373732c2704f"
        }
      }
    }
  },
  "subject": "subject-value"
}
```

<span data-ttu-id="0878a-133">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [onlineMeeting](../resources/onlinemeeting.md) .</span><span class="sxs-lookup"><span data-stu-id="0878a-133">In the request body, supply a JSON representation of the [onlineMeeting](../resources/onlinemeeting.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="0878a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0878a-134">Response</span></span>

><span data-ttu-id="0878a-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0878a-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onlineMeeting"
} -->
```http
HTTP/1.1 201 Created
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
  "meetingType": "meetNow",
  "participants": {
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
  "description": "Create onlineMeeting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
