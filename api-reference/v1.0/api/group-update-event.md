---
title: Actualizar evento
description: Actualiza un objeto de evento.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: dd287032c898e4a56983a77815ce12daef05dae9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27892270"
---
# <a name="update-event"></a><span data-ttu-id="ae662-103">Actualizar evento</span><span class="sxs-lookup"><span data-stu-id="ae662-103">Update event</span></span>
<span data-ttu-id="ae662-104">Actualiza un objeto de [evento](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="ae662-104">Update an [event](../resources/event.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="ae662-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ae662-105">Permissions</span></span>
<span data-ttu-id="ae662-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ae662-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ae662-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ae662-108">Permission type</span></span>      | <span data-ttu-id="ae662-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ae662-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ae662-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ae662-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ae662-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ae662-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ae662-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ae662-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ae662-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ae662-113">Not supported.</span></span>    |
|<span data-ttu-id="ae662-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ae662-114">Application</span></span> | <span data-ttu-id="ae662-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ae662-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ae662-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ae662-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /groups/{id}/events/{id}
PATCH /groups/{id}/calendar/events/{id}
```

## <a name="request-headers"></a><span data-ttu-id="ae662-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ae662-117">Request headers</span></span>
| <span data-ttu-id="ae662-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ae662-118">Name</span></span>       | <span data-ttu-id="ae662-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae662-119">Type</span></span> | <span data-ttu-id="ae662-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae662-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="ae662-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ae662-121">Authorization</span></span>  | <span data-ttu-id="ae662-122">string</span><span class="sxs-lookup"><span data-stu-id="ae662-122">string</span></span>  | <span data-ttu-id="ae662-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ae662-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ae662-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ae662-125">Request body</span></span>
<span data-ttu-id="ae662-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ae662-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

## <a name="response"></a><span data-ttu-id="ae662-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae662-129">Response</span></span>
<span data-ttu-id="ae662-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="ae662-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="ae662-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae662-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="ae662-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ae662-132">Request</span></span>
<span data-ttu-id="ae662-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ae662-133">The following is an example of the request.</span></span>

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

#### <a name="response"></a><span data-ttu-id="ae662-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae662-134">Response</span></span>
<span data-ttu-id="ae662-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae662-135">The following is an example of the response.</span></span>

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
