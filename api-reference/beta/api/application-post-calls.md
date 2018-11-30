---
title: Crear llamada
description: Crear una nueva llamada.
ms.openlocfilehash: 863cde971859cf0b2b4eef8f400f3726eeac74d4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084105"
---
# <a name="create-call"></a><span data-ttu-id="b7ea1-103">Crear llamada</span><span class="sxs-lookup"><span data-stu-id="b7ea1-103">Create call</span></span>

> <span data-ttu-id="b7ea1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b7ea1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b7ea1-106">Crear una nueva llamada.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-106">Create a new call.</span></span>

## <a name="permissions"></a><span data-ttu-id="b7ea1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b7ea1-107">Permissions</span></span>
<span data-ttu-id="b7ea1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b7ea1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="b7ea1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b7ea1-110">Permission type</span></span>                        | <span data-ttu-id="b7ea1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b7ea1-111">Permissions (from least to most privileged)</span></span>                                             |
|:---------------------------------------|:----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ea1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b7ea1-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="b7ea1-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="b7ea1-113">Not Supported</span></span>                                                                           |
| <span data-ttu-id="b7ea1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b7ea1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b7ea1-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="b7ea1-115">Not Supported</span></span>                                                                           |
| <span data-ttu-id="b7ea1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b7ea1-116">Application</span></span>                            | <span data-ttu-id="b7ea1-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.Initiate.All, Calls.InitiateGroupCalls.All</span><span class="sxs-lookup"><span data-stu-id="b7ea1-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.Initiate.All, Calls.InitiateGroupCalls.All</span></span> |

> <span data-ttu-id="b7ea1-118">**Nota:** Para una llamada con medios de aplicación hospedado, se necesita el permiso Calls.AccessMedia.All con uno de los permisos enumerados en la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-118">**Note:** For a call with app hosted media, you need the Calls.AccessMedia.All permission with one of the permissions listed in the previous table.</span></span>

## <a name="http-request"></a><span data-ttu-id="b7ea1-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b7ea1-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls
POST /applications/{id}/calls
```

## <a name="request-headers"></a><span data-ttu-id="b7ea1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ea1-120">Request headers</span></span>
| <span data-ttu-id="b7ea1-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="b7ea1-121">Name</span></span>          | <span data-ttu-id="b7ea1-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7ea1-122">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="b7ea1-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b7ea1-123">Authorization</span></span> | <span data-ttu-id="b7ea1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b7ea1-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ea1-126">Request body</span></span>
<span data-ttu-id="b7ea1-127">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [call](../resources/call.md) .</span><span class="sxs-lookup"><span data-stu-id="b7ea1-127">In the request body, supply a JSON representation of a [call](../resources/call.md) object.</span></span>

> <span data-ttu-id="b7ea1-128">**Nota:** Las propiedades marcan como `Server generated` se pasan por alto al procesar `POST` en `app/calls`.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-128">**Note:** Properties marked as `Server generated` are ignored when processing `POST` on `app/calls`.</span></span>

## <a name="response"></a><span data-ttu-id="b7ea1-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7ea1-129">Response</span></span>
<span data-ttu-id="b7ea1-130">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto en el cuerpo de la respuesta [de llamadas](../resources/call.md) .</span><span class="sxs-lookup"><span data-stu-id="b7ea1-130">If successful, this method returns a `201 Created` response code and a [call](../resources/call.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="b7ea1-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b7ea1-131">Examples</span></span>

### <a name="create-peer-to-peer-voip-call-with-service-hosted-media"></a><span data-ttu-id="b7ea1-132">Creación de llamadas VOIP de punto a punto con medios de servicio hospedado</span><span class="sxs-lookup"><span data-stu-id="b7ea1-132">Create peer to peer VOIP call with service hosted media</span></span>

> <span data-ttu-id="b7ea1-133">**Nota:** Esta llamada necesita el permiso Calls.Initiate.All.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-133">**Note:** This call needs the Calls.Initiate.All permission.</span></span>

##### <a name="request"></a><span data-ttu-id="b7ea1-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ea1-134">Request</span></span>
<span data-ttu-id="b7ea1-135">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-135">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_call_from_application"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls
Content-Type: application/json

{
  "callbackUri": "https://bot.contoso.com/api/calls",
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
  },
  "source": {
    "identity": {
      "application": {
        "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
      }
    },
    "languageId": "languageId-value",
    "region": "region-value"
  },
  "subject": "Test Call",
  "targets": [
    {
      "identity": {
        "user": {
          "id": "550fae72-d251-43ec-868c-373732c2704f",
          "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
          "displayName": "Heidi Steen"
        }
      }
    }
  ],
  "tenantId": "tenantId-value"
}
```

##### <a name="response"></a><span data-ttu-id="b7ea1-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7ea1-136">Response</span></span>

> <span data-ttu-id="b7ea1-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.call"
} -->
```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "57DAB8B1894C409AB240BD8BEAE78896",
  "callbackUri": "https://bot.contoso.com/api/calls",
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
  },
  "source": {
    "identity": {
      "application": {
        "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
      }
    },
    "languageId": "languageId-value",
    "region": "region-value"
  },
  "subject": "Test Call",
  "targets": [
    {
      "identity": {
        "user": {
          "id": "550fae72-d251-43ec-868c-373732c2704f",
          "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
          "displayName": "Heidi Steen"
        }
      }
    }
  ],
  "tenantId": "tenantId-value"
}
```

##### <a name="notification---establishing"></a><span data-ttu-id="b7ea1-139">Notificación: establecimiento</span><span class="sxs-lookup"><span data-stu-id="b7ea1-139">Notification - establishing</span></span>

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
        "state": "establishing",
        "direction": "outgoing"
      }
    }
  ]
}
```
##### <a name="notification---established"></a><span data-ttu-id="b7ea1-140">Notificación - establecido</span><span class="sxs-lookup"><span data-stu-id="b7ea1-140">Notification - established</span></span>

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

### <a name="create-peer-to-peer-voip-call-with-application-hosted-media"></a><span data-ttu-id="b7ea1-141">Creación de llamadas VOIP de punto a punto con medios de aplicación hospedada</span><span class="sxs-lookup"><span data-stu-id="b7ea1-141">Create peer to peer VOIP call with application hosted media</span></span>

> <span data-ttu-id="b7ea1-142">Nota: Necesita permiso Calls.Initiate.All y Calls.AccessMedia.All.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-142">Note: Needs Calls.Initiate.All and Calls.AccessMedia.All permission.</span></span>

##### <a name="request"></a><span data-ttu-id="b7ea1-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ea1-143">Request</span></span>
<span data-ttu-id="b7ea1-144">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-144">The following example shows the request.</span></span>

```http
POST https://graph.microsoft.com/beta/app/calls
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.call"
}-->
```json
{
  "callbackUri": "https://bot.contoso.com/api/calls",
  "mediaConfig": {
    "@odata.type": "#microsoft.graph.appHostedMediaConfig",
    "blob": "<media config blob>"
  },
  "requestedModalities": [ "audio" ],
  "source": {
    "identity": {
      "application": {
        "id": "550fae72-d251-43ec-868c-373732c2704f",
        "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
        "displayName": "IT Bot"
      }
    },
    "languageId": "languageId-value",
    "region": "region-value"
  },
  "subject": "Test Call",
  "targets": [
    {
      "identity": {
        "user": {
          "id": "550fae72-d251-43ec-868c-373732c2704f",
          "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
          "displayName": "Heidi Steen"
        }
      }
    }
  ],
  "tenantId": "tenantId-value"
}
```

### <a name="create-group-call-with-service-hosted-media"></a><span data-ttu-id="b7ea1-145">Crear llamada de un grupo con medios de servicio hospedado</span><span class="sxs-lookup"><span data-stu-id="b7ea1-145">Create group call with service hosted media</span></span>

> <span data-ttu-id="b7ea1-146">**Nota:** En este ejemplo se necesita los permisos Calls.InitiateGroupCalls.All y Calls.AccessMedia.All.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-146">**Note:** This example needs the Calls.InitiateGroupCalls.All and Calls.AccessMedia.All permissions.</span></span>

##### <a name="request"></a><span data-ttu-id="b7ea1-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ea1-147">Request</span></span>

```http
POST https://graph.microsoft.com/beta/app/calls
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.call"
}-->
```json
{
  "subject": "Test Call",
  "callbackUri": "https://bot.contoso.com/api/calls",
  "source": {
    "identity": {
      "application": {
        "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
      }
    }
  },
  "targets": [
    {
      "identity": {
        "user": {
          "id": "29362BD4-CD58-4ED0-A206-0E4A33DBB0B6",
          "displayName": "Heidi Steen"
        }
      }
    },
    {
      "identity": {
        "phone": {
          "displayName": "+12345678890",
          "id": "+12345678890"
        }
      }
    }
  ],
  "requestedModalities": [ "audio", "video" ],
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
  },
  "chatInfo": {
    "threadId": "19:meeting_NTg0NmQ3NTctZDVkZC00YzRhLThmNmEtOGQ3M2E0ODdmZDZk@thread.v2",
    "messageId": "0",
    "replyChainMessageId": null
  }
}
```

### <a name="join-private-meeting-with-service-hosted-media"></a><span data-ttu-id="b7ea1-148">Unirse a la reunión privada con medios de servicio hospedado</span><span class="sxs-lookup"><span data-stu-id="b7ea1-148">Join private meeting with service hosted media</span></span>

> <span data-ttu-id="b7ea1-149">**Nota:** En este ejemplo se necesita el permiso Calls.JoinGroupCalls.All.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-149">**Note:** This example needs the Calls.JoinGroupCalls.All permission.</span></span>

##### <a name="request"></a><span data-ttu-id="b7ea1-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ea1-150">Request</span></span>

```http
POST https://graph.microsoft.com/beta/app/calls
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.call"
}-->
```json
{
  "subject": "Test Call",
  "callbackUri": "https://bot.contoso.com/api/calls",
  "source": {
    "identity": {
      "application": {
        "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
      }
    }
  },
  "requestedModalities": [ "audio", "video" ],
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
  },
  "chatInfo": {
    "threadId": "19:meeting_NTg0NmQ3NTctZDVkZC00YzRhLThmNmEtOGQ3M2E0ODdmZDZk@thread.v2",
    "messageId": "0"
  },
  "meetingInfo": {
    "@odata.type": "#microsoft.graph.organizerMeetingInfo",
    "organizer": {
      "user": {
        "id": "90ED37DC-D8E3-4E11-9DE3-30A955DDA06F",
        "tenantId": "49BFC225-8482-4AB8-94E7-76B48FDB9849"
      }
    }
  }
}
```

### <a name="join-channel-meeting-with-service-hosted-media"></a><span data-ttu-id="b7ea1-151">Unirse a la reunión de canal con medios de servicio hospedado</span><span class="sxs-lookup"><span data-stu-id="b7ea1-151">Join channel meeting with service hosted media</span></span>

> <span data-ttu-id="b7ea1-152">**Nota:** En este ejemplo se necesita el permiso Calls.JoinGroupCalls.All.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-152">**Note:** This example needs the Calls.JoinGroupCalls.All permission.</span></span>

##### <a name="request"></a><span data-ttu-id="b7ea1-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ea1-153">Request</span></span>

```http
POST https://graph.microsoft.com/beta/app/calls
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.call"
}-->
```json
{
  "subject": "Test Call",
  "callbackUri": "https://bot.contoso.com/api/calls",
  "source": {
    "identity": {
      "application": {
        "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
      }
    }
  },
  "requestedModalities": [ "audio", "video" ],
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
  },
  "chatInfo": {
    "threadId": "19:meeting_NTg0NmQ3NTctZDVkZC00YzRhLThmNmEtOGQ3M2E0ODdmZDZk@thread.v2",
    "messageId": "1507228578052",
    "replyChainMessageId": null
  },
  "meetingInfo": {
    "@odata.type": "#microsoft.graph.organizerMeetingInfo",
    "organizer": {
      "user": {
        "id": "90ED37DC-D8E3-4E11-9DE3-30A955DDA06F",
        "tenantId": "49BFC225-8482-4AB8-94E7-76B48FDB9849"
      }
    }
  }
}
```

### <a name="join-channel-meeting-as-a-guest-with-service-hosted-media"></a><span data-ttu-id="b7ea1-154">Unirse a reuniones de canal como invitado con medios de servicio hospedado</span><span class="sxs-lookup"><span data-stu-id="b7ea1-154">Join channel meeting as a guest with service hosted media</span></span>

> <span data-ttu-id="b7ea1-155">**Nota:** En este ejemplo se necesita el permiso Calls.JoinGroupCallsAsGuest.All.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-155">**Note:** This example needs the Calls.JoinGroupCallsAsGuest.All permission.</span></span>

##### <a name="request"></a><span data-ttu-id="b7ea1-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ea1-156">Request</span></span>

```http
POST https://graph.microsoft.com/beta/app/calls
Content-Type: application/json
```
<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.call"
}-->
```json
{
  "subject": "Test Call",
  "callbackUri": "https://bot.contoso.com/api/calls",
  "source": {
    "identity": {
      "user": {
        "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698",
        "displayName": "App_Guest_DisplayName",
        "identityProvider": "None"
      }
    }
  },
  "requestedModalities": [ "audio", "video" ],
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
  },
  "chatInfo": {
    "threadId": "19:meeting_NTg0NmQ3NTctZDVkZC00YzRhLThmNmEtOGQ3M2E0ODdmZDZk@thread.v2",
    "messageId": "1507228578052",
    "replyChainMessageId": null
  },
  "meetingInfo": {
    "@odata.type": "#microsoft.graph.organizerMeetingInfo",
    "organizer": {
      "user": {
        "id": "90ED37DC-D8E3-4E11-9DE3-30A955DDA06F",
        "tenantId": "49BFC225-8482-4AB8-94E7-76B48FDB9849"
      }
    }
  }
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create call",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
