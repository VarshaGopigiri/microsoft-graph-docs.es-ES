---
title: Crear evento
description: Use esta API para crear un objeto event.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 4b7e0803b6eb59a2446da658815c19d08256587b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883912"
---
# <a name="create-event"></a><span data-ttu-id="16d02-103">Crear evento</span><span class="sxs-lookup"><span data-stu-id="16d02-103">Create event</span></span>

> <span data-ttu-id="16d02-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="16d02-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="16d02-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="16d02-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="16d02-106">Use esta API para crear un objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="16d02-106">Use this API to create a new [event](../resources/event.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="16d02-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="16d02-107">Permissions</span></span>
<span data-ttu-id="16d02-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="16d02-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="16d02-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="16d02-110">Permission type</span></span>      | <span data-ttu-id="16d02-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="16d02-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="16d02-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="16d02-112">Delegated (work or school account)</span></span> | <span data-ttu-id="16d02-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="16d02-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="16d02-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="16d02-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="16d02-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16d02-115">Not supported.</span></span>    |
|<span data-ttu-id="16d02-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="16d02-116">Application</span></span> | <span data-ttu-id="16d02-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16d02-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="16d02-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="16d02-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/events
POST /groups/{id}/calendar/events
```

## <a name="request-headers"></a><span data-ttu-id="16d02-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="16d02-119">Request headers</span></span>
| <span data-ttu-id="16d02-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16d02-120">Header</span></span>       | <span data-ttu-id="16d02-121">Valor</span><span class="sxs-lookup"><span data-stu-id="16d02-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="16d02-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="16d02-122">Authorization</span></span>  | <span data-ttu-id="16d02-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="16d02-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="16d02-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="16d02-125">Request body</span></span>
<span data-ttu-id="16d02-126">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="16d02-126">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="16d02-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16d02-127">Response</span></span>
<span data-ttu-id="16d02-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="16d02-128">If successful, this method returns `201 Created` response code and [event](../resources/event.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="16d02-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="16d02-129">Example</span></span>
#### <a name="request"></a><span data-ttu-id="16d02-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16d02-130">Request</span></span>
<span data-ttu-id="16d02-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="16d02-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_event_from_group"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/events
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "2016-10-19T10:37:00Z"
  },
  "uid": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```
<span data-ttu-id="16d02-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="16d02-132">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>

#### <a name="response"></a><span data-ttu-id="16d02-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16d02-133">Response</span></span>
<span data-ttu-id="16d02-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="16d02-134">The following is an example of the response.</span></span>
><span data-ttu-id="16d02-135">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="16d02-135">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="16d02-136">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="16d02-136">All the properties will be returned from an actual call.</span></span>
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
    "time": "2016-10-19T10:37:00Z"
  },
  "uid": "iCalUId-value",
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
