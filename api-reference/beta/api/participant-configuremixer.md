---
title: 'participante: configureMixer'
description: Configurar cómo audio mixto para los diferentes participantes en una conversación entre varias partes.
ms.openlocfilehash: 32d50d165ed7beb69b99e5d0940b49acbce8f45c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084320"
---
# <a name="participant-configuremixer"></a><span data-ttu-id="4d2d2-103">participante: configureMixer</span><span class="sxs-lookup"><span data-stu-id="4d2d2-103">participant: configureMixer</span></span>

> <span data-ttu-id="4d2d2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4d2d2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4d2d2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4d2d2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4d2d2-106">Configurar cómo audio mixto para los diferentes participantes en una conversación entre varias partes.</span><span class="sxs-lookup"><span data-stu-id="4d2d2-106">Configure how audio is mixed for different participants in a multiparty conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="4d2d2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4d2d2-107">Permissions</span></span>
<span data-ttu-id="4d2d2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4d2d2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="4d2d2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4d2d2-110">Permission type</span></span> | <span data-ttu-id="4d2d2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4d2d2-111">Permissions (from least to most privileged)</span></span> |
| :-------------- | :------------------------------------------ |
| <span data-ttu-id="4d2d2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4d2d2-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="4d2d2-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="4d2d2-113">Not Supported</span></span>        |
| <span data-ttu-id="4d2d2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4d2d2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4d2d2-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="4d2d2-115">Not Supported</span></span>        |
| <span data-ttu-id="4d2d2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4d2d2-116">Application</span></span>     | <span data-ttu-id="4d2d2-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span><span class="sxs-lookup"><span data-stu-id="4d2d2-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4d2d2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4d2d2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/participants/configureMixer
POST /applications/{id}/calls/{id}/participants/configureMixer
```

## <a name="request-headers"></a><span data-ttu-id="4d2d2-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4d2d2-119">Request headers</span></span>
| <span data-ttu-id="4d2d2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="4d2d2-120">Name</span></span>          | <span data-ttu-id="4d2d2-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d2d2-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="4d2d2-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="4d2d2-122">Authorization</span></span> | <span data-ttu-id="4d2d2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4d2d2-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4d2d2-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4d2d2-125">Request body</span></span>
<span data-ttu-id="4d2d2-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="4d2d2-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="4d2d2-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4d2d2-127">Parameter</span></span>      | <span data-ttu-id="4d2d2-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d2d2-128">Type</span></span>    |<span data-ttu-id="4d2d2-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d2d2-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4d2d2-130">participantMixerLevels</span><span class="sxs-lookup"><span data-stu-id="4d2d2-130">participantMixerLevels</span></span>|<span data-ttu-id="4d2d2-131">colección de [participantMixerLevel](../resources/participantmixerlevel.md)</span><span class="sxs-lookup"><span data-stu-id="4d2d2-131">[participantMixerLevel](../resources/participantmixerlevel.md) collection</span></span>| <span data-ttu-id="4d2d2-132">Configuración del Mezclador de niveles para indicar participante de audio.</span><span class="sxs-lookup"><span data-stu-id="4d2d2-132">Configuration of mixer levels for given audio participant.</span></span>|
|<span data-ttu-id="4d2d2-133">clientContext</span><span class="sxs-lookup"><span data-stu-id="4d2d2-133">clientContext</span></span>|<span data-ttu-id="4d2d2-134">String</span><span class="sxs-lookup"><span data-stu-id="4d2d2-134">String</span></span>|<span data-ttu-id="4d2d2-135">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="4d2d2-135">The client context.</span></span>|

## <a name="response"></a><span data-ttu-id="4d2d2-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d2d2-136">Response</span></span>
<span data-ttu-id="4d2d2-137">Devuelve `202 Accepted` código de respuesta y un encabezado de ubicación con un uri para el [commsOperation](../resources/commsoperation.md) creado para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="4d2d2-137">Returns `202 Accepted` response code and a Location header with a uri to the [commsOperation](../resources/commsoperation.md) created for this request.</span></span>

## <a name="example"></a><span data-ttu-id="4d2d2-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d2d2-138">Example</span></span>
<span data-ttu-id="4d2d2-139">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="4d2d2-139">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="4d2d2-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4d2d2-140">Request</span></span>
<span data-ttu-id="4d2d2-141">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4d2d2-141">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "participant_configureMixer"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/participants/configureMixer
Content-Type: application/json
Content-Length: 501

{
  "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c",
  "participantMixerLevels": [
    {
      "participant": "550fae72-d251-43ec-868c-373732c2704f",
      "exclusive": true,
      "ducking": {
        "rampActive": 50,
        "rampInactive": 50,
        "lowerLevel": 10,
        "upperLevel": 50
      },
      "sourceLevels": [
        {
          "participant": "632899f8-2ea1-4604-8413-27bd2892079f",
          "level": 50,
          "duckOthers": false
        }
      ]
    }
  ]
}
```

##### <a name="response"></a><span data-ttu-id="4d2d2-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d2d2-142">Response</span></span>

> <span data-ttu-id="4d2d2-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4d2d2-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.commsOperation"
} -->
```http
HTTP/1.1 202 Accepted
Location: https://graph.microsoft.com/beta/app/calls/57dab8b1-894c-409a-b240-bd8beae78896/operations/0fe0623f-d628-42ed-b4bd-8ac290072cc5
```

##### <a name="notification---operation-completed"></a><span data-ttu-id="4d2d2-145">Notificación: la operación se terminó</span><span class="sxs-lookup"><span data-stu-id="4d2d2-145">Notification - operation completed</span></span>

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
        "@odata.etag": "W/\"1\"",
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
  "description": "participant: configureMixer",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->