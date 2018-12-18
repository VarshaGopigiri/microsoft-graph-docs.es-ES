---
title: 'llamar a: registro'
description: Registro de la llamada.
author: VinodRavichandran
ms.openlocfilehash: 5de56ca417f5a6d06e8116802eeba2dd3d39e399
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303552"
---
# <a name="call-record"></a><span data-ttu-id="4b205-103">llamar a: registro</span><span class="sxs-lookup"><span data-stu-id="4b205-103">call: record</span></span>

> <span data-ttu-id="4b205-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4b205-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4b205-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4b205-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4b205-106">Registro de la llamada.</span><span class="sxs-lookup"><span data-stu-id="4b205-106">Record the call.</span></span>

## <a name="permissions"></a><span data-ttu-id="4b205-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4b205-107">Permissions</span></span>
<span data-ttu-id="4b205-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4b205-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="4b205-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4b205-110">Permission type</span></span> | <span data-ttu-id="4b205-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4b205-111">Permissions (from least to most privileged)</span></span> |
| :-------------- | :------------------------------------------ |
| <span data-ttu-id="4b205-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4b205-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="4b205-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="4b205-113">Not Supported</span></span>        |
| <span data-ttu-id="4b205-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4b205-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4b205-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="4b205-115">Not Supported</span></span>        |
| <span data-ttu-id="4b205-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4b205-116">Application</span></span>     | <span data-ttu-id="4b205-117">Calls.AccessMedia.All</span><span class="sxs-lookup"><span data-stu-id="4b205-117">Calls.AccessMedia.All</span></span>                       |

## <a name="http-request"></a><span data-ttu-id="4b205-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4b205-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/record
POST /applications/{id}/calls/{id}/record
```

## <a name="request-headers"></a><span data-ttu-id="4b205-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4b205-119">Request headers</span></span>
| <span data-ttu-id="4b205-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="4b205-120">Name</span></span>          | <span data-ttu-id="4b205-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b205-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="4b205-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="4b205-122">Authorization</span></span> | <span data-ttu-id="4b205-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4b205-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4b205-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4b205-125">Request body</span></span>
<span data-ttu-id="4b205-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="4b205-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="4b205-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4b205-127">Parameter</span></span>      | <span data-ttu-id="4b205-128">Type</span><span class="sxs-lookup"><span data-stu-id="4b205-128">Type</span></span>    |<span data-ttu-id="4b205-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b205-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4b205-130">solicita</span><span class="sxs-lookup"><span data-stu-id="4b205-130">prompts</span></span>|<span data-ttu-id="4b205-131">colección de [mediaprompt](../resources/mediaprompt.md)</span><span class="sxs-lookup"><span data-stu-id="4b205-131">[mediaprompt](../resources/mediaprompt.md) collection</span></span> | <span data-ttu-id="4b205-132">Colección de indicaciones para reproducir (si hay alguno) antes de la grabación se iniciará.</span><span class="sxs-lookup"><span data-stu-id="4b205-132">Collection of prompts to play (if any) before recording starts.</span></span> <span data-ttu-id="4b205-133">Los clientes pueden elegir especificar la acción "playPrompt" por separado o especificar como parte de "registro" - principalmente todos los registros están precedido por un símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="4b205-133">Customers can choose to specify "playPrompt" action separately or specify as part of "record" - mostly all records are preceeded by a prompt</span></span> |
|<span data-ttu-id="4b205-134">bargeInAllowed</span><span class="sxs-lookup"><span data-stu-id="4b205-134">bargeInAllowed</span></span>|<span data-ttu-id="4b205-135">Boolean</span><span class="sxs-lookup"><span data-stu-id="4b205-135">Boolean</span></span>| <span data-ttu-id="4b205-136">Permitir que los usuarios escriban opción antes de que finalice el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="4b205-136">Allow users to enter choice before prompt finishes.</span></span>                                                                 |
|<span data-ttu-id="4b205-137">initialSilenceTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="4b205-137">initialSilenceTimeoutInSeconds</span></span> | <span data-ttu-id="4b205-138">Int32</span><span class="sxs-lookup"><span data-stu-id="4b205-138">Int32</span></span>| <span data-ttu-id="4b205-139">Silencio inicial máximo permitido desde el momento en que se inicia la operación de registro antes de la operación de conmutación por error y tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="4b205-139">Maximum initial silence allowed from the time we start the record operation before we timeout and fail the operation.</span></span> <span data-ttu-id="4b205-140">Si se está reproduciendo un símbolo del sistema, este temporizador se inicia después de que finalice el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="4b205-140">If we are playing a prompt, then this timer starts after prompt finishes.</span></span> |
|<span data-ttu-id="4b205-141">maxSilenceTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="4b205-141">maxSilenceTimeoutInSeconds</span></span>|<span data-ttu-id="4b205-142">Int32</span><span class="sxs-lookup"><span data-stu-id="4b205-142">Int32</span></span>| <span data-ttu-id="4b205-143">El tiempo de espera máximo silencio en segundos.</span><span class="sxs-lookup"><span data-stu-id="4b205-143">The maximum silence timeout in seconds.</span></span>|
|<span data-ttu-id="4b205-144">maxRecordDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="4b205-144">maxRecordDurationInSeconds</span></span>|<span data-ttu-id="4b205-145">Int32</span><span class="sxs-lookup"><span data-stu-id="4b205-145">Int32</span></span>| <span data-ttu-id="4b205-146">La duración de registro máximo en segundos.</span><span class="sxs-lookup"><span data-stu-id="4b205-146">The maximum record duration in seconds.</span></span>|
|<span data-ttu-id="4b205-147">playBeep</span><span class="sxs-lookup"><span data-stu-id="4b205-147">playBeep</span></span>|<span data-ttu-id="4b205-148">Boolean</span><span class="sxs-lookup"><span data-stu-id="4b205-148">Boolean</span></span>| <span data-ttu-id="4b205-149">Emite un pitido tras reproducir el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="4b205-149">Plays a beep after playing the prompt.</span></span>|
|<span data-ttu-id="4b205-150">streamWhileRecording</span><span class="sxs-lookup"><span data-stu-id="4b205-150">streamWhileRecording</span></span>|<span data-ttu-id="4b205-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="4b205-151">Boolean</span></span>|<span data-ttu-id="4b205-152">Si se establece en true, una ubicación de recursos será proporcionado en cuanto se inicia la grabación.</span><span class="sxs-lookup"><span data-stu-id="4b205-152">If set to true, a resource location will be provided as soon as the recording starts.</span></span> |
|<span data-ttu-id="4b205-153">stopTones</span><span class="sxs-lookup"><span data-stu-id="4b205-153">stopTones</span></span>|<span data-ttu-id="4b205-154">Colección String</span><span class="sxs-lookup"><span data-stu-id="4b205-154">String collection</span></span>|<span data-ttu-id="4b205-155">Detener tonos especificados para finalizar la grabación.</span><span class="sxs-lookup"><span data-stu-id="4b205-155">Stop tones specified to end recording.</span></span>|
|<span data-ttu-id="4b205-156">clientContext</span><span class="sxs-lookup"><span data-stu-id="4b205-156">clientContext</span></span>|<span data-ttu-id="4b205-157">String</span><span class="sxs-lookup"><span data-stu-id="4b205-157">String</span></span>|<span data-ttu-id="4b205-158">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="4b205-158">The client context.</span></span>|

## <a name="response"></a><span data-ttu-id="4b205-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4b205-159">Response</span></span>
<span data-ttu-id="4b205-160">Devuelve `202 Accepted` código de respuesta y un encabezado de ubicación con un uri para el [commsOperation](../resources/commsoperation.md) creado para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b205-160">Returns `202 Accepted` response code and a Location header with a uri to the [commsOperation](../resources/commsoperation.md) created for this request.</span></span>

## <a name="example"></a><span data-ttu-id="4b205-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4b205-161">Example</span></span>
<span data-ttu-id="4b205-162">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="4b205-162">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="4b205-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4b205-163">Request</span></span>
<span data-ttu-id="4b205-164">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b205-164">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call_record"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/record
Content-Type: application/json
Content-Length: 394

{
  "bargeInAllowed": true,
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
  ],
  "maxRecordDurationInSeconds": 1800,
  "initialSilenceTimeoutInSeconds": 10,
  "maxSilenceTimeoutInSeconds": 2,
  "recordingFormat": "wav",
  "playBeep": true,
  "streamWhileRecording": true,
  "stopTones": [ "#", "11", "*" ]
}
```

##### <a name="response"></a><span data-ttu-id="4b205-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4b205-165">Response</span></span>

> <span data-ttu-id="4b205-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4b205-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.recordOperation"
} -->
```http
HTTP/1.1 202 Accepted
Location: https://graph.microsoft.com/beta/app/calls/57dab8b1-894c-409a-b240-bd8beae78896/operations/0fe0623f-d628-42ed-b4bd-8ac290072cc5
```

##### <a name="notification---operation-completed"></a><span data-ttu-id="4b205-168">Notificación: la operación se terminó</span><span class="sxs-lookup"><span data-stu-id="4b205-168">Notification - operation completed</span></span>

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
        "@odata.type": "#microsoft.graph.recordOperation",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896/operations/0FE0623FD62842EDB4BD8AC290072CC5",
        "@odata.etag": "W/\"54451\"",
        "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c",
        "status": "completed",
        "recordResourceLocation": "https://file.location/17e3b46c-f61d-4f4d-9635-c626ef18e6ad",
        "recordResourceAccessToken": "<access-token>",
        "completionReason": "stopToneDetected"
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "call: record",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
