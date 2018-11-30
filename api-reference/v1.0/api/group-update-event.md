---
title: Actualizar evento
description: Actualiza un objeto de evento.
ms.openlocfilehash: e06f08b0c1f0703904c2418ac490be2100e39619
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030744"
---
# <a name="update-event"></a><span data-ttu-id="2bcc3-103">Actualizar evento</span><span class="sxs-lookup"><span data-stu-id="2bcc3-103">Update event</span></span>
<span data-ttu-id="2bcc3-104">Actualiza un objeto de [evento](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="2bcc3-104">Update an [event](../resources/event.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="2bcc3-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2bcc3-105">Permissions</span></span>
<span data-ttu-id="2bcc3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2bcc3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2bcc3-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2bcc3-108">Permission type</span></span>      | <span data-ttu-id="2bcc3-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2bcc3-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2bcc3-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2bcc3-110">Delegated (work or school account)</span></span> | <span data-ttu-id="2bcc3-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2bcc3-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="2bcc3-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2bcc3-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2bcc3-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2bcc3-113">Not supported.</span></span>    |
|<span data-ttu-id="2bcc3-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2bcc3-114">Application</span></span> | <span data-ttu-id="2bcc3-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2bcc3-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2bcc3-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2bcc3-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /groups/{id}/events/{id}
PATCH /groups/{id}/calendar/events/{id}
```

## <a name="request-headers"></a><span data-ttu-id="2bcc3-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2bcc3-117">Request headers</span></span>
| <span data-ttu-id="2bcc3-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="2bcc3-118">Name</span></span>       | <span data-ttu-id="2bcc3-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="2bcc3-119">Type</span></span> | <span data-ttu-id="2bcc3-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bcc3-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="2bcc3-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="2bcc3-121">Authorization</span></span>  | <span data-ttu-id="2bcc3-122">string</span><span class="sxs-lookup"><span data-stu-id="2bcc3-122">string</span></span>  | <span data-ttu-id="2bcc3-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2bcc3-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2bcc3-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2bcc3-125">Request body</span></span>
<span data-ttu-id="2bcc3-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="2bcc3-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

## <a name="response"></a><span data-ttu-id="2bcc3-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bcc3-129">Response</span></span>
<span data-ttu-id="2bcc3-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="2bcc3-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="2bcc3-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2bcc3-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="2bcc3-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2bcc3-132">Request</span></span>
<span data-ttu-id="2bcc3-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2bcc3-133">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_group_event"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/groups/{id}/events/{id}
Content-type: application/json
Content-length: 211

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

#### <a name="response"></a><span data-ttu-id="2bcc3-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bcc3-134">Response</span></span>
<span data-ttu-id="2bcc3-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2bcc3-135">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->