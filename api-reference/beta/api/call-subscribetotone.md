---
title: 'llamar a: subscribeToTone'
description: " número de teléfono."
ms.openlocfilehash: c3793931c2f06e54cdac278f0f0539b42d7e622c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087689"
---
# <a name="call-subscribetotone"></a><span data-ttu-id="1c882-103">llamar a: subscribeToTone</span><span class="sxs-lookup"><span data-stu-id="1c882-103">call: subscribeToTone</span></span>

> <span data-ttu-id="1c882-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1c882-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1c882-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1c882-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1c882-106">Suscribirse a DTMF (multifrecuencia de tono dual señalización).</span><span class="sxs-lookup"><span data-stu-id="1c882-106">Subscribe to DTMF (dual-tone multi-frequency signaling).</span></span> <span data-ttu-id="1c882-107">Esto le permite recibir una notificación cuando el usuario presiona teclas en un teléfono "teclado".</span><span class="sxs-lookup"><span data-stu-id="1c882-107">This allows you to be notified when the user presses keys on a "touchtone" phone.</span></span>

## <a name="permissions"></a><span data-ttu-id="1c882-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="1c882-108">Permissions</span></span>
<span data-ttu-id="1c882-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1c882-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="1c882-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1c882-111">Permission type</span></span> | <span data-ttu-id="1c882-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1c882-112">Permissions (from least to most privileged)</span></span> |
| :-------------- | :------------------------------------------ |
| <span data-ttu-id="1c882-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1c882-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="1c882-114">No se admite</span><span class="sxs-lookup"><span data-stu-id="1c882-114">Not Supported</span></span>        |
| <span data-ttu-id="1c882-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1c882-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1c882-116">No se admite</span><span class="sxs-lookup"><span data-stu-id="1c882-116">Not Supported</span></span>        |
| <span data-ttu-id="1c882-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1c882-117">Application</span></span>     | <span data-ttu-id="1c882-118">Calls.AccessMedia.All</span><span class="sxs-lookup"><span data-stu-id="1c882-118">Calls.AccessMedia.All</span></span>                       |

## <a name="http-request"></a><span data-ttu-id="1c882-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1c882-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/subscribeToTone
POST /applications/{id}/calls/{id}/subscribeToTone
```

## <a name="request-headers"></a><span data-ttu-id="1c882-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1c882-120">Request headers</span></span>
| <span data-ttu-id="1c882-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="1c882-121">Name</span></span>          | <span data-ttu-id="1c882-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c882-122">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="1c882-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="1c882-123">Authorization</span></span> | <span data-ttu-id="1c882-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1c882-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1c882-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1c882-126">Request body</span></span>
<span data-ttu-id="1c882-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="1c882-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="1c882-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1c882-128">Parameter</span></span>      | <span data-ttu-id="1c882-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c882-129">Type</span></span>    | <span data-ttu-id="1c882-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c882-130">Description</span></span> |
|:---------------|:--------|:------------|
| <span data-ttu-id="1c882-131">clientContext</span><span class="sxs-lookup"><span data-stu-id="1c882-131">clientContext</span></span>  | <span data-ttu-id="1c882-132">String</span><span class="sxs-lookup"><span data-stu-id="1c882-132">String</span></span>  | <span data-ttu-id="1c882-133">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="1c882-133">The client context.</span></span> |

## <a name="response"></a><span data-ttu-id="1c882-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c882-134">Response</span></span>
<span data-ttu-id="1c882-135">Devuelve `202 Accepted` código de respuesta y un encabezado de ubicación con un uri para el [commsOperation](../resources/commsoperation.md) creado para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="1c882-135">Returns `202 Accepted` response code and a Location header with a uri to the [commsOperation](../resources/commsoperation.md) created for this request.</span></span>

## <a name="example"></a><span data-ttu-id="1c882-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1c882-136">Example</span></span>
<span data-ttu-id="1c882-137">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="1c882-137">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="1c882-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1c882-138">Request</span></span>
<span data-ttu-id="1c882-139">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1c882-139">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call_subscribeToTone"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/subscribeToTone
Content-Type: application/json
Content-Length: 46

{
  "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c"
}
```

##### <a name="response"></a><span data-ttu-id="1c882-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c882-140">Response</span></span>

> <span data-ttu-id="1c882-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1c882-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.commsOperation"
} -->
```http
HTTP/1.1 202 Accepted
Location: https://graph.microsoft.com/beta/app/calls/57dab8b1-894c-409a-b240-bd8beae78896/operations/0fe0623f-d628-42ed-b4bd-8ac290072cc5
```

##### <a name="notification---operation-completed"></a><span data-ttu-id="1c882-143">Notificación: la operación se terminó</span><span class="sxs-lookup"><span data-stu-id="1c882-143">Notification - operation completed</span></span>

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
