---
title: 'llamar a: playPrompt'
description: Reproducir un símbolo del sistema en la llamada.
ms.openlocfilehash: a5fb5d34264298726add6cf2742d1319bfcb6c95
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087772"
---
# <a name="call-playprompt"></a><span data-ttu-id="47970-103">llamar a: playPrompt</span><span class="sxs-lookup"><span data-stu-id="47970-103">call: playPrompt</span></span>

> <span data-ttu-id="47970-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="47970-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="47970-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="47970-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="47970-106">Reproducir un símbolo del sistema en la llamada.</span><span class="sxs-lookup"><span data-stu-id="47970-106">Play a prompt in the call.</span></span>

## <a name="permissions"></a><span data-ttu-id="47970-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="47970-107">Permissions</span></span>
<span data-ttu-id="47970-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="47970-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="47970-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="47970-110">Permission type</span></span>                        | <span data-ttu-id="47970-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="47970-111">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="47970-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="47970-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="47970-113">No se admite.</span><span class="sxs-lookup"><span data-stu-id="47970-113">Not Supported.</span></span>                               |
| <span data-ttu-id="47970-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="47970-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="47970-115">No se admite.</span><span class="sxs-lookup"><span data-stu-id="47970-115">Not Supported.</span></span>                               |
| <span data-ttu-id="47970-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="47970-116">Application</span></span>                            | <span data-ttu-id="47970-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="47970-117">None.</span></span>                                        |

## <a name="http-request"></a><span data-ttu-id="47970-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="47970-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/playPrompt
POST /applications/{id}/calls/{id}/playPrompt
```

## <a name="request-headers"></a><span data-ttu-id="47970-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="47970-119">Request headers</span></span>
| <span data-ttu-id="47970-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="47970-120">Name</span></span>          | <span data-ttu-id="47970-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="47970-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="47970-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="47970-122">Authorization</span></span> | <span data-ttu-id="47970-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="47970-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="47970-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="47970-125">Request body</span></span>
<span data-ttu-id="47970-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="47970-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="47970-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="47970-127">Parameter</span></span>      | <span data-ttu-id="47970-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="47970-128">Type</span></span>    |<span data-ttu-id="47970-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="47970-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="47970-130">solicita</span><span class="sxs-lookup"><span data-stu-id="47970-130">prompts</span></span>|<span data-ttu-id="47970-131">colección de [símbolo del sistema](../resources/prompt.md)</span><span class="sxs-lookup"><span data-stu-id="47970-131">[prompt](../resources/prompt.md) collection</span></span>||
|<span data-ttu-id="47970-132">clientContext</span><span class="sxs-lookup"><span data-stu-id="47970-132">clientContext</span></span>|<span data-ttu-id="47970-133">String</span><span class="sxs-lookup"><span data-stu-id="47970-133">String</span></span>|<span data-ttu-id="47970-134">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="47970-134">The client context.</span></span>|

## <a name="response"></a><span data-ttu-id="47970-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47970-135">Response</span></span>
<span data-ttu-id="47970-136">Devuelve `202 Accepted` código de respuesta y un encabezado de ubicación con un uri para el [commsOperation](../resources/commsoperation.md) creado para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="47970-136">Returns `202 Accepted` response code and a Location header with a uri to the [commsOperation](../resources/commsoperation.md) created for this request.</span></span>

## <a name="example"></a><span data-ttu-id="47970-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="47970-137">Example</span></span>
<span data-ttu-id="47970-138">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="47970-138">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="47970-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="47970-139">Request</span></span>
<span data-ttu-id="47970-140">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="47970-140">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call_playPrompt"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/playPrompt
Content-Type: application/json
Content-Length: 166

{
  "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c",
  "prompts": [
    {
      "@odata.type": "#microsoft.graph.mediaPrompt",
      "mediaInfo": {
        "uri": "https://cdn.contoso.com/beep.wav",
        "resourceId": "1D6DE2D4-CD51-4309-8DAA-70768651088E"
      },
      "loop": 5
    }
  ]
}
```

##### <a name="response"></a><span data-ttu-id="47970-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47970-141">Response</span></span>

> <span data-ttu-id="47970-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="47970-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.commsOperation"
} -->
```http
HTTP/1.1 202 Accepted
Location: https://graph.microsoft.com/beta/app/calls/57dab8b1-894c-409a-b240-bd8beae78896/operations/0fe0623f-d628-42ed-b4bd-8ac290072cc5
```

##### <a name="notification---operation-completed"></a><span data-ttu-id="47970-144">Notificación: la operación se terminó</span><span class="sxs-lookup"><span data-stu-id="47970-144">Notification - operation completed</span></span>

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
  "description": "call: playPrompt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->