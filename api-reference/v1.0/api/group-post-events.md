---
title: Crear evento
description: Use esta API para crear un objeto event.
author: dkershaw10
localization_priority: Priority
ms.prod: groups
ms.openlocfilehash: 1d264ec205d8f94027a8121253819c2613d1f4d6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941124"
---
# <a name="create-event"></a><span data-ttu-id="30ca2-103">Crear evento</span><span class="sxs-lookup"><span data-stu-id="30ca2-103">Create event</span></span>
<span data-ttu-id="30ca2-104">Use esta API para crear un objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="30ca2-104">Use this API to create a new [event](../resources/event.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="30ca2-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="30ca2-105">Permissions</span></span>
<span data-ttu-id="30ca2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="30ca2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="30ca2-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="30ca2-108">Permission type</span></span>      | <span data-ttu-id="30ca2-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="30ca2-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="30ca2-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="30ca2-110">Delegated (work or school account)</span></span> | <span data-ttu-id="30ca2-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="30ca2-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="30ca2-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="30ca2-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="30ca2-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30ca2-113">Not supported.</span></span>    |
|<span data-ttu-id="30ca2-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="30ca2-114">Application</span></span> | <span data-ttu-id="30ca2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30ca2-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="30ca2-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="30ca2-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/events
POST /groups/{id}/calendar/events
```

## <a name="request-headers"></a><span data-ttu-id="30ca2-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="30ca2-117">Request headers</span></span>
| <span data-ttu-id="30ca2-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30ca2-118">Header</span></span>       | <span data-ttu-id="30ca2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="30ca2-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="30ca2-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="30ca2-120">Authorization</span></span>  | <span data-ttu-id="30ca2-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="30ca2-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="30ca2-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="30ca2-123">Request body</span></span>
<span data-ttu-id="30ca2-124">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="30ca2-124">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="30ca2-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30ca2-125">Response</span></span>
<span data-ttu-id="30ca2-126">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30ca2-126">If successful, this method returns `201 Created` response code and [event](../resources/event.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="30ca2-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30ca2-127">Example</span></span>
#### <a name="request"></a><span data-ttu-id="30ca2-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="30ca2-128">Request</span></span>
<span data-ttu-id="30ca2-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="30ca2-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_event_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/events
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "datetime-value"
  },
  "iCalUId": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```
<span data-ttu-id="30ca2-130">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="30ca2-130">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>

#### <a name="response"></a><span data-ttu-id="30ca2-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30ca2-131">Response</span></span>
<span data-ttu-id="30ca2-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30ca2-132">The following is an example of the response.</span></span>
><span data-ttu-id="30ca2-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="30ca2-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "datetime-value"
  },
  "iCalUId": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
