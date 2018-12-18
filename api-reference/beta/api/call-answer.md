---
title: 'llamar a: respuesta'
description: Responder a una llamada entrante.
author: VinodRavichandran
ms.openlocfilehash: df864a6a9043853e7c9e5b1f5546c4ae502ec4d6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343207"
---
# <a name="call-answer"></a><span data-ttu-id="cd8ce-103">llamar a: respuesta</span><span class="sxs-lookup"><span data-stu-id="cd8ce-103">call: answer</span></span>

> <span data-ttu-id="cd8ce-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cd8ce-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cd8ce-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cd8ce-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cd8ce-106">Responder a una llamada entrante.</span><span class="sxs-lookup"><span data-stu-id="cd8ce-106">Answer an incoming call.</span></span>

## <a name="permissions"></a><span data-ttu-id="cd8ce-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="cd8ce-107">Permissions</span></span>
<span data-ttu-id="cd8ce-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cd8ce-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="cd8ce-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cd8ce-110">Permission type</span></span> | <span data-ttu-id="cd8ce-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cd8ce-111">Permissions (from least to most privileged)</span></span>                 |
| :-------------- | :-----------------------------------------------------------|
| <span data-ttu-id="cd8ce-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cd8ce-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="cd8ce-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="cd8ce-113">Not Supported</span></span>                        |
| <span data-ttu-id="cd8ce-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cd8ce-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cd8ce-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="cd8ce-115">Not Supported</span></span>                        |
| <span data-ttu-id="cd8ce-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cd8ce-116">Application</span></span>     | <span data-ttu-id="cd8ce-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cd8ce-117">None</span></span>                                                        |

## <a name="http-request"></a><span data-ttu-id="cd8ce-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cd8ce-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/answer
POST /applications/{id}/calls/{id}/answer
```

## <a name="request-headers"></a><span data-ttu-id="cd8ce-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cd8ce-119">Request headers</span></span>
| <span data-ttu-id="cd8ce-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="cd8ce-120">Name</span></span>          | <span data-ttu-id="cd8ce-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd8ce-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="cd8ce-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="cd8ce-122">Authorization</span></span> | <span data-ttu-id="cd8ce-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cd8ce-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cd8ce-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cd8ce-125">Request body</span></span>
<span data-ttu-id="cd8ce-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="cd8ce-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="cd8ce-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="cd8ce-127">Parameter</span></span>        | <span data-ttu-id="cd8ce-128">Type</span><span class="sxs-lookup"><span data-stu-id="cd8ce-128">Type</span></span>                                     |<span data-ttu-id="cd8ce-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd8ce-129">Description</span></span>                                                                                                                                    |
|:-----------------|:-----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
|<span data-ttu-id="cd8ce-130">callbackUri</span><span class="sxs-lookup"><span data-stu-id="cd8ce-130">callbackUri</span></span>       |<span data-ttu-id="cd8ce-131">String</span><span class="sxs-lookup"><span data-stu-id="cd8ce-131">String</span></span>                                    |<span data-ttu-id="cd8ce-132">El identificador de suscripción o de devolución de llamada en la que se entregarán las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="cd8ce-132">The callback or subscription ID on which callbacks will be delivered.</span></span> <span data-ttu-id="cd8ce-133">(Obligatorio)</span><span class="sxs-lookup"><span data-stu-id="cd8ce-133">(Required)</span></span>                                                               |
|<span data-ttu-id="cd8ce-134">acceptedModalities</span><span class="sxs-lookup"><span data-stu-id="cd8ce-134">acceptedModalities</span></span>|<span data-ttu-id="cd8ce-135">Colección String</span><span class="sxs-lookup"><span data-stu-id="cd8ce-135">String collection</span></span>                         |<span data-ttu-id="cd8ce-136">La lista de Aceptar modalidades.</span><span class="sxs-lookup"><span data-stu-id="cd8ce-136">The list of accept modalities.</span></span> <span data-ttu-id="cd8ce-137">Los valores posibles son: `unknown`, `audio`, `video`, `screenSharing`, `videoBasedScreenSharing`, `data`.</span><span class="sxs-lookup"><span data-stu-id="cd8ce-137">Possible value are: `unknown`, `audio`, `video`, `screenSharing`, `videoBasedScreenSharing`, `data`.</span></span> <span data-ttu-id="cd8ce-138">(Obligatorio)</span><span class="sxs-lookup"><span data-stu-id="cd8ce-138">(Required)</span></span> |
|<span data-ttu-id="cd8ce-139">mediaConfig</span><span class="sxs-lookup"><span data-stu-id="cd8ce-139">mediaConfig</span></span>       |[<span data-ttu-id="cd8ce-140">mediaConfig</span><span class="sxs-lookup"><span data-stu-id="cd8ce-140">mediaConfig</span></span>](../resources/mediaconfig.md)|<span data-ttu-id="cd8ce-141">La configuración de medios.</span><span class="sxs-lookup"><span data-stu-id="cd8ce-141">The media configuration.</span></span> <span data-ttu-id="cd8ce-142">(Obligatorio)</span><span class="sxs-lookup"><span data-stu-id="cd8ce-142">(Required)</span></span>                                                                                                            |

## <a name="response"></a><span data-ttu-id="cd8ce-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd8ce-143">Response</span></span>
<span data-ttu-id="cd8ce-144">Este método devuelve `202 Accepted` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd8ce-144">This method returns `202 Accepted` response code.</span></span>

## <a name="examples"></a><span data-ttu-id="cd8ce-145">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cd8ce-145">Examples</span></span>
<span data-ttu-id="cd8ce-146">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="cd8ce-146">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="cd8ce-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cd8ce-147">Request</span></span>
<span data-ttu-id="cd8ce-148">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cd8ce-148">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call_answer"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/answer
Content-Type: application/json
Content-Length: 211

{
  "callbackUri": "callbackUri-value",
  "mediaConfig": {
    "@odata.type": "#microsoft.graph.appHostedMediaConfig",
    "blob": "<media config blob>"
  },
  "acceptedModalities": [
    "audio"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="cd8ce-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd8ce-149">Response</span></span>
<span data-ttu-id="cd8ce-150">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd8ce-150">Here is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 202 Accepted
```

### <a name="answer-voip-call-with-service-hosted-media"></a><span data-ttu-id="cd8ce-151">Responder a llamadas VOIP con medios de servicio hospedado</span><span class="sxs-lookup"><span data-stu-id="cd8ce-151">Answer VOIP call with service hosted media</span></span>

##### <a name="notification---incoming"></a><span data-ttu-id="cd8ce-152">Notificación - entrante</span><span class="sxs-lookup"><span data-stu-id="cd8ce-152">Notification - incoming</span></span>

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
      "changeType": "created",
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "incoming",
        "direction": "incoming",
        "callRoutes": [
          {
            "routingType": "lookup",
            "original": {
              "phone": {
                "id": "+14258828080"
              }
            },
            "final": {
              "user": {
                "id": "29362BD4-CD58-4ED0-A206-0E4A33DBB0B6",
                "displayName": "Heidi Steen"
              }
            }
          }
        ],
        "source": {
          "identity": {
            "user": {
              "displayName": "Test User",
              "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
            }
          },
          "region": "westus",
          "languageId": "en-US"
        },
        "targets": [
          {
            "identity": {
              "application": {
                "displayName": "Test BOT",
                "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
              }
            },
            "languageId": "en-US"
          }
        ],
        "requestedModalities": [ "audio" ]
      }
    }
  ]
}
```

##### <a name="request"></a><span data-ttu-id="cd8ce-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cd8ce-153">Request</span></span>

```http
POST /app/calls/57DAB8B1894C409AB240BD8BEAE78896/answer
Authorization: Bearer <TOKEN>
Content-Type: application/json
```

<!-- {
  "blockType": "ignored",
  "name": "call_answer"
}-->
```json
{
  "callbackUri": "https://bot.contoso.com/api/calls",
  "acceptedModalities": [ "audio" ],
  "mediaConfig": {
    "@odata.type": "#microsoft.graph.serviceHostedMediaConfig",
    "preFetchMedia": [
      {
        "uri": "https://cdn.contoso.com/beep.wav",
        "resourceId": "1D6DE2D4-CD51-4309-8DAA-70768651088E"
      },
      {
        "uri": "https://cdn.contoso.com/cool.wav",
        "resourceId": "1D6DE2D4-CD51-4309-8DAA-70768651088F"
      }
    ]
  }
}
```

##### <a name="response"></a><span data-ttu-id="cd8ce-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd8ce-154">Response</span></span>

```http
HTTP/1.1 202 Accepted
```

##### <a name="notification---establishing"></a><span data-ttu-id="cd8ce-155">Notificación: establecimiento</span><span class="sxs-lookup"><span data-stu-id="cd8ce-155">Notification - establishing</span></span>

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
      "changeType": "updated",
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "establishing"
      }
    }
  ]
}
```

##### <a name="notification---established"></a><span data-ttu-id="cd8ce-156">Notificación - establecido</span><span class="sxs-lookup"><span data-stu-id="cd8ce-156">Notification - established</span></span>

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
      "changeType": "updated",
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "established"
      }
    }
  ]
}
```

### <a name="answer-voip-call-with-application-hosted-media"></a><span data-ttu-id="cd8ce-157">Responder a llamadas VOIP con medios de aplicación hospedada</span><span class="sxs-lookup"><span data-stu-id="cd8ce-157">Answer VOIP call with application hosted media</span></span>

##### <a name="notification---incoming"></a><span data-ttu-id="cd8ce-158">Notificación - entrante</span><span class="sxs-lookup"><span data-stu-id="cd8ce-158">Notification - incoming</span></span>

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
      "changeType": "created",
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "incoming",
        "direction": "incoming",
        "source": {
          "@odata.type": "#microsoft.graph.participantInfo",
          "identity": {
            "user": {
              "displayName": "Test User",
              "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
            }
          },
          "region": "westus",
          "languageId": "en-US"
        },
        "targets": [
          {
            "@odata.type": "#microsoft.graph.participantInfo",
            "identity": {
              "application": {
                "displayName": "Test BOT",
                "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
              }
            },
            "region": "westus",
            "languageId": "en-US"
          }
        ],
        "requestedModalities": [ "audio" ]
      }
    }
  ]
}
```

##### <a name="request"></a><span data-ttu-id="cd8ce-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cd8ce-159">Request</span></span>

```http
POST /app/calls/57DAB8B1894C409AB240BD8BEAE78896/answer
Authorization: Bearer <TOKEN>
Content-Type: application/json
```

<!-- {
  "blockType": "ignored",
  "name": "call_answer"
}-->
```json
{
  "callbackUri": "https://bot.contoso.com/api/calls",
  "acceptedModalities": [ "audio" ],
  "mediaConfig": {
    "@odata.type": "#microsoft.graph.appHostedMediaConfig",
    "blob": "<media config blob>"
  }
}
```

##### <a name="response"></a><span data-ttu-id="cd8ce-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd8ce-160">Response</span></span>

```http
HTTP/1.1 202 Accepted
```

##### <a name="notification---establishing"></a><span data-ttu-id="cd8ce-161">Notificación: establecimiento</span><span class="sxs-lookup"><span data-stu-id="cd8ce-161">Notification - establishing</span></span>

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
      "changeType": "updated",
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "establishing"
      }
    }
  ]
}
```

##### <a name="notification---established"></a><span data-ttu-id="cd8ce-162">Notificación - establecido</span><span class="sxs-lookup"><span data-stu-id="cd8ce-162">Notification - established</span></span>

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
      "changeType": "updated",
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "established"
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "call: answer",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
