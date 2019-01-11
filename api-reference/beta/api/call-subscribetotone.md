---
title: 'llamar a: subscribeToTone'
description: Suscribirse a DTMF (multifrecuencia de tono dual señalización). Esto le permite recibir una notificación cuando el usuario presiona teclas en un teléfono 'teclado'.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: 226edd59e7d826dd7304ae45ec58c360e8ef3191
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833435"
---
# <a name="call-subscribetotone"></a><span data-ttu-id="06df6-104">llamar a: subscribeToTone</span><span class="sxs-lookup"><span data-stu-id="06df6-104">call: subscribeToTone</span></span>

> <span data-ttu-id="06df6-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="06df6-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="06df6-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="06df6-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="06df6-107">Suscribirse a DTMF (multifrecuencia de tono dual señalización).</span><span class="sxs-lookup"><span data-stu-id="06df6-107">Subscribe to DTMF (dual-tone multi-frequency signaling).</span></span> <span data-ttu-id="06df6-108">Esto le permite recibir una notificación cuando el usuario presiona teclas en un teléfono "teclado".</span><span class="sxs-lookup"><span data-stu-id="06df6-108">This allows you to be notified when the user presses keys on a "touchtone" phone.</span></span>

## <a name="permissions"></a><span data-ttu-id="06df6-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="06df6-109">Permissions</span></span>
<span data-ttu-id="06df6-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="06df6-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="06df6-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="06df6-112">Permission type</span></span> | <span data-ttu-id="06df6-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="06df6-113">Permissions (from least to most privileged)</span></span> |
| :-------------- | :------------------------------------------ |
| <span data-ttu-id="06df6-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="06df6-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="06df6-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="06df6-115">Not Supported</span></span>        |
| <span data-ttu-id="06df6-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="06df6-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="06df6-117">No se admite</span><span class="sxs-lookup"><span data-stu-id="06df6-117">Not Supported</span></span>        |
| <span data-ttu-id="06df6-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="06df6-118">Application</span></span>     | <span data-ttu-id="06df6-119">Calls.AccessMedia.All</span><span class="sxs-lookup"><span data-stu-id="06df6-119">Calls.AccessMedia.All</span></span>                       |

## <a name="http-request"></a><span data-ttu-id="06df6-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="06df6-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/subscribeToTone
POST /applications/{id}/calls/{id}/subscribeToTone
```

## <a name="request-headers"></a><span data-ttu-id="06df6-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="06df6-121">Request headers</span></span>
| <span data-ttu-id="06df6-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="06df6-122">Name</span></span>          | <span data-ttu-id="06df6-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="06df6-123">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="06df6-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="06df6-124">Authorization</span></span> | <span data-ttu-id="06df6-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="06df6-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="06df6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="06df6-127">Request body</span></span>
<span data-ttu-id="06df6-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="06df6-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="06df6-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="06df6-129">Parameter</span></span>      | <span data-ttu-id="06df6-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="06df6-130">Type</span></span>    | <span data-ttu-id="06df6-131">Description</span><span class="sxs-lookup"><span data-stu-id="06df6-131">Description</span></span> |
|:---------------|:--------|:------------|
| <span data-ttu-id="06df6-132">clientContext</span><span class="sxs-lookup"><span data-stu-id="06df6-132">clientContext</span></span>  | <span data-ttu-id="06df6-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="06df6-133">String</span></span>  | <span data-ttu-id="06df6-134">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="06df6-134">The client context.</span></span> |

## <a name="response"></a><span data-ttu-id="06df6-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06df6-135">Response</span></span>
<span data-ttu-id="06df6-136">Devuelve `202 Accepted` código de respuesta y un encabezado de ubicación con un uri para el [commsOperation](../resources/commsoperation.md) creado para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="06df6-136">Returns `202 Accepted` response code and a Location header with a uri to the [commsOperation](../resources/commsoperation.md) created for this request.</span></span>

## <a name="example"></a><span data-ttu-id="06df6-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="06df6-137">Example</span></span>
<span data-ttu-id="06df6-138">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="06df6-138">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="06df6-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="06df6-139">Request</span></span>
<span data-ttu-id="06df6-140">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06df6-140">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call-subscribeToTone"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/subscribeToTone
Content-Type: application/json
Content-Length: 46

{
  "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c"
}
```

##### <a name="response"></a><span data-ttu-id="06df6-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06df6-141">Response</span></span>

> <span data-ttu-id="06df6-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="06df6-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.commsOperation"
} -->
```http
HTTP/1.1 202 Accepted
Location: https://graph.microsoft.com/beta/app/calls/57dab8b1-894c-409a-b240-bd8beae78896/operations/0fe0623f-d628-42ed-b4bd-8ac290072cc5
```

##### <a name="notification---operation-completed"></a><span data-ttu-id="06df6-144">Notificación: la operación se terminó</span><span class="sxs-lookup"><span data-stu-id="06df6-144">Notification - operation completed</span></span>

```http
POST https://bot.contoso.com/api/calls
Authorization: Bearer <TOKEN>
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsNotifications"
}-->
```json
{
  "value": [
    {
      "changeType": "deleted",
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896/operations/0FE0623FD62842EDB4BD8AC290072CC5",
      "resourceData": {
        "@odata.type": "#microsoft.graph.commsOperation",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896/operations/0FE0623FD62842EDB4BD8AC290072CC5",
        "@odata.etag": "W/\"54451\"",
        "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c",
        "status": "completed"
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "call: subscribeToTone",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
