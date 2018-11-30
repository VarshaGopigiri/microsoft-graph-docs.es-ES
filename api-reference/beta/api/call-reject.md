---
title: 'llamar a: rechazar'
description: Rechazar una llamada entrante.
ms.openlocfilehash: 4731d377021871569fcec895af832aeea66b3431
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086927"
---
# <a name="call-reject"></a><span data-ttu-id="0fc1a-103">llamar a: rechazar</span><span class="sxs-lookup"><span data-stu-id="0fc1a-103">call: reject</span></span>

> <span data-ttu-id="0fc1a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0fc1a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0fc1a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0fc1a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0fc1a-106">Rechazar una llamada entrante.</span><span class="sxs-lookup"><span data-stu-id="0fc1a-106">Reject an incoming call.</span></span>

## <a name="permissions"></a><span data-ttu-id="0fc1a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0fc1a-107">Permissions</span></span>
<span data-ttu-id="0fc1a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0fc1a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="0fc1a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0fc1a-110">Permission type</span></span> | <span data-ttu-id="0fc1a-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0fc1a-111">Permissions (from least to most privileged)</span></span>                |
| :-------------- | :--------------------------------------------------------- |
| <span data-ttu-id="0fc1a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0fc1a-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="0fc1a-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="0fc1a-113">Not Supported</span></span>                       |
| <span data-ttu-id="0fc1a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0fc1a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0fc1a-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="0fc1a-115">Not Supported</span></span>                       |
| <span data-ttu-id="0fc1a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0fc1a-116">Application</span></span>     | <span data-ttu-id="0fc1a-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0fc1a-117">None</span></span>                                                       |

## <a name="http-request"></a><span data-ttu-id="0fc1a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0fc1a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/reject
POST /applications/{id}/calls/{id}/reject
```

## <a name="request-headers"></a><span data-ttu-id="0fc1a-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0fc1a-119">Request headers</span></span>
| <span data-ttu-id="0fc1a-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="0fc1a-120">Name</span></span>          | <span data-ttu-id="0fc1a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fc1a-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="0fc1a-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="0fc1a-122">Authorization</span></span> | <span data-ttu-id="0fc1a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0fc1a-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0fc1a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0fc1a-125">Request body</span></span>
<span data-ttu-id="0fc1a-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="0fc1a-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="0fc1a-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0fc1a-127">Parameter</span></span>      | <span data-ttu-id="0fc1a-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="0fc1a-128">Type</span></span>    |<span data-ttu-id="0fc1a-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fc1a-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0fc1a-130">motivo</span><span class="sxs-lookup"><span data-stu-id="0fc1a-130">reason</span></span>|<span data-ttu-id="0fc1a-131">String</span><span class="sxs-lookup"><span data-stu-id="0fc1a-131">String</span></span>|<span data-ttu-id="0fc1a-132">La razón de rechazo.</span><span class="sxs-lookup"><span data-stu-id="0fc1a-132">The rejection reason.</span></span>|

## <a name="response"></a><span data-ttu-id="0fc1a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0fc1a-133">Response</span></span>
<span data-ttu-id="0fc1a-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0fc1a-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

```http
Returns `202 Accepted` response code
```

## <a name="example"></a><span data-ttu-id="0fc1a-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc1a-136">Example</span></span>
<span data-ttu-id="0fc1a-137">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0fc1a-137">The following example shows how to call this API.</span></span>

##### <a name="notification---incoming"></a><span data-ttu-id="0fc1a-138">Notificación - entrante</span><span class="sxs-lookup"><span data-stu-id="0fc1a-138">Notification - incoming</span></span>

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

##### <a name="request"></a><span data-ttu-id="0fc1a-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0fc1a-139">Request</span></span>
<span data-ttu-id="0fc1a-140">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0fc1a-140">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call_reject"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/reject
Content-Type: application/json
Content-Length: 24

{
  "reason": "none"
}
```

##### <a name="response"></a><span data-ttu-id="0fc1a-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0fc1a-141">Response</span></span>
<span data-ttu-id="0fc1a-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0fc1a-142">Here is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 202 Accepted
```

##### <a name="notification---deleted"></a><span data-ttu-id="0fc1a-143">Notificación - eliminado</span><span class="sxs-lookup"><span data-stu-id="0fc1a-143">Notification - deleted</span></span>

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
        "@odata.etag": "W/\"5445\""
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "call: reject",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
