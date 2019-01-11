---
title: 'llamar a: rechazar'
description: Rechazar una llamada entrante.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: 06037d86be99e162a57b54f77d7b4363062f5858
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849479"
---
# <a name="call-reject"></a><span data-ttu-id="6654c-103">llamar a: rechazar</span><span class="sxs-lookup"><span data-stu-id="6654c-103">call: reject</span></span>

> <span data-ttu-id="6654c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6654c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6654c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6654c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6654c-106">Rechazar una llamada entrante.</span><span class="sxs-lookup"><span data-stu-id="6654c-106">Reject an incoming call.</span></span>

## <a name="permissions"></a><span data-ttu-id="6654c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6654c-107">Permissions</span></span>
<span data-ttu-id="6654c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6654c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="6654c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6654c-110">Permission type</span></span> | <span data-ttu-id="6654c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6654c-111">Permissions (from least to most privileged)</span></span>                |
| :-------------- | :--------------------------------------------------------- |
| <span data-ttu-id="6654c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6654c-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="6654c-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="6654c-113">Not Supported</span></span>                       |
| <span data-ttu-id="6654c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6654c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6654c-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="6654c-115">Not Supported</span></span>                       |
| <span data-ttu-id="6654c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6654c-116">Application</span></span>     | <span data-ttu-id="6654c-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6654c-117">None</span></span>                                                       |

## <a name="http-request"></a><span data-ttu-id="6654c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6654c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/reject
POST /applications/{id}/calls/{id}/reject
```

## <a name="request-headers"></a><span data-ttu-id="6654c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6654c-119">Request headers</span></span>
| <span data-ttu-id="6654c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="6654c-120">Name</span></span>          | <span data-ttu-id="6654c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="6654c-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="6654c-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="6654c-122">Authorization</span></span> | <span data-ttu-id="6654c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6654c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6654c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6654c-125">Request body</span></span>
<span data-ttu-id="6654c-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="6654c-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="6654c-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6654c-127">Parameter</span></span>      | <span data-ttu-id="6654c-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="6654c-128">Type</span></span>    |<span data-ttu-id="6654c-129">Description</span><span class="sxs-lookup"><span data-stu-id="6654c-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6654c-130">motivo</span><span class="sxs-lookup"><span data-stu-id="6654c-130">reason</span></span>|<span data-ttu-id="6654c-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="6654c-131">String</span></span>|<span data-ttu-id="6654c-132">La razón de rechazo.</span><span class="sxs-lookup"><span data-stu-id="6654c-132">The rejection reason.</span></span>|

## <a name="response"></a><span data-ttu-id="6654c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6654c-133">Response</span></span>
<span data-ttu-id="6654c-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6654c-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

```http
Returns `202 Accepted` response code
```

## <a name="example"></a><span data-ttu-id="6654c-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6654c-136">Example</span></span>
<span data-ttu-id="6654c-137">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6654c-137">The following example shows how to call this API.</span></span>

##### <a name="notification---incoming"></a><span data-ttu-id="6654c-138">Notificación - entrante</span><span class="sxs-lookup"><span data-stu-id="6654c-138">Notification - incoming</span></span>

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

##### <a name="request"></a><span data-ttu-id="6654c-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6654c-139">Request</span></span>
<span data-ttu-id="6654c-140">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6654c-140">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call-reject"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/reject
Content-Type: application/json
Content-Length: 24

{
  "reason": "none"
}
```

##### <a name="response"></a><span data-ttu-id="6654c-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6654c-141">Response</span></span>
<span data-ttu-id="6654c-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6654c-142">Here is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 202 Accepted
```

##### <a name="notification---deleted"></a><span data-ttu-id="6654c-143">Notificación - eliminado</span><span class="sxs-lookup"><span data-stu-id="6654c-143">Notification - deleted</span></span>

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
