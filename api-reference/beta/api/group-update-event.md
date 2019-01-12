---
title: Actualizar evento
description: Actualiza un objeto de evento.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: 092e5fdb8f70ec73d1c8a33230f596b9fdbf3b19
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980002"
---
# <a name="update-event"></a><span data-ttu-id="b84e5-103">Actualizar evento</span><span class="sxs-lookup"><span data-stu-id="b84e5-103">Update event</span></span>

> <span data-ttu-id="b84e5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b84e5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b84e5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b84e5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b84e5-106">Actualiza un objeto de [evento](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="b84e5-106">Update an [event](../resources/event.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="b84e5-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b84e5-107">Permissions</span></span>
<span data-ttu-id="b84e5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b84e5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b84e5-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b84e5-110">Permission type</span></span>      | <span data-ttu-id="b84e5-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b84e5-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b84e5-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b84e5-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b84e5-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b84e5-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="b84e5-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b84e5-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b84e5-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b84e5-115">Not supported.</span></span>    |
|<span data-ttu-id="b84e5-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b84e5-116">Application</span></span> | <span data-ttu-id="b84e5-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b84e5-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b84e5-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b84e5-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /groups/{id}/events/{id}
PATCH /groups/{id}/calendar/events/{id}
```

## <a name="request-headers"></a><span data-ttu-id="b84e5-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b84e5-119">Request headers</span></span>
| <span data-ttu-id="b84e5-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b84e5-120">Name</span></span>       | <span data-ttu-id="b84e5-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="b84e5-121">Type</span></span> | <span data-ttu-id="b84e5-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b84e5-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="b84e5-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b84e5-123">Authorization</span></span>  | <span data-ttu-id="b84e5-124">string</span><span class="sxs-lookup"><span data-stu-id="b84e5-124">string</span></span>  | <span data-ttu-id="b84e5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b84e5-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b84e5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b84e5-127">Request body</span></span>
<span data-ttu-id="b84e5-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="b84e5-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

## <a name="response"></a><span data-ttu-id="b84e5-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b84e5-131">Response</span></span>
<span data-ttu-id="b84e5-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="b84e5-132">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="b84e5-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b84e5-133">Example</span></span>
#### <a name="request"></a><span data-ttu-id="b84e5-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b84e5-134">Request</span></span>
<span data-ttu-id="b84e5-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b84e5-135">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_group_event"
}-->
```http
PATCH https://graph.microsoft.com/beta/groups/{id}/events/{id}
Content-type: application/json
Content-length: 211

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "datetime-value"
  },
  "uid": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```

#### <a name="response"></a><span data-ttu-id="b84e5-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b84e5-136">Response</span></span>
<span data-ttu-id="b84e5-137">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b84e5-137">The following is an example of the response.</span></span>

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
