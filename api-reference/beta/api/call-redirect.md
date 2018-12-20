---
title: 'llamar a: redirigir'
description: Redirigir una llamada entrante.
author: VinodRavichandran
ms.openlocfilehash: 9fff752f07f66cf3c236982495897234c9a1c38d
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380222"
---
# <a name="call-redirect"></a><span data-ttu-id="1c95c-103">llamar a: redirigir</span><span class="sxs-lookup"><span data-stu-id="1c95c-103">call: redirect</span></span>

> <span data-ttu-id="1c95c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1c95c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1c95c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1c95c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1c95c-106">Redirigir una llamada entrante.</span><span class="sxs-lookup"><span data-stu-id="1c95c-106">Redirect an incoming call.</span></span>

## <a name="permissions"></a><span data-ttu-id="1c95c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1c95c-107">Permissions</span></span>
<span data-ttu-id="1c95c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1c95c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="1c95c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1c95c-110">Permission type</span></span> | <span data-ttu-id="1c95c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1c95c-111">Permissions (from least to most privileged)</span></span>         |
| :-------------- | :-------------------------------------------------- |
| <span data-ttu-id="1c95c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1c95c-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="1c95c-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="1c95c-113">Not Supported</span></span>                |
| <span data-ttu-id="1c95c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1c95c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1c95c-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="1c95c-115">Not Supported</span></span>                |
| <span data-ttu-id="1c95c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1c95c-116">Application</span></span>     | <span data-ttu-id="1c95c-117">Calls.Initiate.All</span><span class="sxs-lookup"><span data-stu-id="1c95c-117">Calls.Initiate.All</span></span>                                  |

## <a name="http-request"></a><span data-ttu-id="1c95c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1c95c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/redirect
POST /applications/{id}/calls/{id}/redirect
```

## <a name="request-headers"></a><span data-ttu-id="1c95c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1c95c-119">Request headers</span></span>
| <span data-ttu-id="1c95c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="1c95c-120">Name</span></span>          | <span data-ttu-id="1c95c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c95c-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="1c95c-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="1c95c-122">Authorization</span></span> | <span data-ttu-id="1c95c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1c95c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1c95c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1c95c-125">Request body</span></span>
<span data-ttu-id="1c95c-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="1c95c-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="1c95c-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1c95c-127">Parameter</span></span>      | <span data-ttu-id="1c95c-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c95c-128">Type</span></span>    |<span data-ttu-id="1c95c-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c95c-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1c95c-130">objetivos</span><span class="sxs-lookup"><span data-stu-id="1c95c-130">targets</span></span>|<span data-ttu-id="1c95c-131">colección de [invitationParticipantInfo](../resources/invitationparticipantinfo.md)</span><span class="sxs-lookup"><span data-stu-id="1c95c-131">[invitationParticipantInfo](../resources/invitationparticipantinfo.md) collection</span></span>|<span data-ttu-id="1c95c-132">Los participantes de destino de la operación de redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="1c95c-132">The target participants of the redirect operation.</span></span>|
|<span data-ttu-id="1c95c-133">targetDisposition</span><span class="sxs-lookup"><span data-stu-id="1c95c-133">targetDisposition</span></span>|<span data-ttu-id="1c95c-134">String</span><span class="sxs-lookup"><span data-stu-id="1c95c-134">String</span></span>|<span data-ttu-id="1c95c-135">El valor posible es:`default`</span><span class="sxs-lookup"><span data-stu-id="1c95c-135">The possible value is: `default`</span></span>|
|<span data-ttu-id="1c95c-136">timeout</span><span class="sxs-lookup"><span data-stu-id="1c95c-136">timeout</span></span>|<span data-ttu-id="1c95c-137">Int32</span><span class="sxs-lookup"><span data-stu-id="1c95c-137">Int32</span></span>|<span data-ttu-id="1c95c-138">El tiempo de espera en segundos para la operación de redirección.</span><span class="sxs-lookup"><span data-stu-id="1c95c-138">The timeout in seconds for the redirect operation.</span></span>|
|<span data-ttu-id="1c95c-139">maskCallee</span><span class="sxs-lookup"><span data-stu-id="1c95c-139">maskCallee</span></span>|<span data-ttu-id="1c95c-140">Booleano</span><span class="sxs-lookup"><span data-stu-id="1c95c-140">Boolean</span></span>|<span data-ttu-id="1c95c-141">Indica si se va a enmascarar el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="1c95c-141">Indicates whether to mask the callee.</span></span>|
|<span data-ttu-id="1c95c-142">maskCaller</span><span class="sxs-lookup"><span data-stu-id="1c95c-142">maskCaller</span></span>|<span data-ttu-id="1c95c-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="1c95c-143">Boolean</span></span>|<span data-ttu-id="1c95c-144">Indica si se va a enmascarar el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="1c95c-144">Indicates whether to mask the caller.</span></span>|

## <a name="response"></a><span data-ttu-id="1c95c-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c95c-145">Response</span></span>
<span data-ttu-id="1c95c-146">Devuelve `202 Accepted` código de respuesta</span><span class="sxs-lookup"><span data-stu-id="1c95c-146">Returns `202 Accepted` response code</span></span>

## <a name="examples"></a><span data-ttu-id="1c95c-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1c95c-147">Examples</span></span>

### <a name="redirect-a-call"></a><span data-ttu-id="1c95c-148">Redirigir una llamada</span><span class="sxs-lookup"><span data-stu-id="1c95c-148">Redirect a call</span></span>

##### <a name="request"></a><span data-ttu-id="1c95c-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1c95c-149">Request</span></span>
<span data-ttu-id="1c95c-150">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1c95c-150">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call-redirect"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/redirect
Content-Type: application/json
Content-Length: 515

{
  "targets": [
    {
      "endpointType": "default",
      "identity": {
        "user": {
          "id": "550fae72-d251-43ec-868c-373732c2704f",
          "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
          "displayName": "Heidi Steen"
        }
      },
      "languageId": "en-US",
      "region": "westus"
    }
  ],
  "targetDisposition": "default",
  "timeout": 99,
  "maskCallee": false,
  "maskCaller": false
}
```

##### <a name="response"></a><span data-ttu-id="1c95c-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c95c-151">Response</span></span>

> <span data-ttu-id="1c95c-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1c95c-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 202 Accepted
```

### <a name="forward-a-call"></a><span data-ttu-id="1c95c-154">Transferir una llamada</span><span class="sxs-lookup"><span data-stu-id="1c95c-154">Forward a call</span></span>

##### <a name="notification---incoming"></a><span data-ttu-id="1c95c-155">Notificación - entrante</span><span class="sxs-lookup"><span data-stu-id="1c95c-155">Notification - incoming</span></span>

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
            "region": "westus",
            "languageId": "en-US"
          }
        ],
        "requestedModalities": [ "audio", "video" ]
      }
    }
  ]
}
```

##### <a name="request"></a><span data-ttu-id="1c95c-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1c95c-156">Request</span></span>

```http
POST https://graph.microsoft.com/beta/app/calls/57DAB8B1894C409AB240BD8BEAE78896/redirect
Authorization: Bearer <TOKEN>
Content-Type: application/json

{
  "targets": [
    {
      "endpointType": "default",
      "identity": {
        "user": {
          "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572699"
        }
      },
      "languageId": "en-US",
      "region": "westus"
    }
  ],
  "targetDisposition": "default",
  "timeout": 60,
  "maskCallee": false,
  "maskCaller": false
}
```

##### <a name="response"></a><span data-ttu-id="1c95c-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c95c-157">Response</span></span>

```http
HTTP/1.1 202 Accepted
```

##### <a name="notification---redirecting"></a><span data-ttu-id="1c95c-158">Notificación - redirigir</span><span class="sxs-lookup"><span data-stu-id="1c95c-158">Notification - redirecting</span></span>

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
        "state": "redirecting"
      }
    }
  ]
}
```

##### <a name="notification---terminated"></a><span data-ttu-id="1c95c-159">Notificación - terminada</span><span class="sxs-lookup"><span data-stu-id="1c95c-159">Notification - terminated</span></span>

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
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "terminated",
        "answeredBy": {
          "identity": {
            "user": {
              "displayName": "Test User 2",
              "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572699"
            }
          }
        },
        "terminationReason": "AppRedirected"
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "call: redirect",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
