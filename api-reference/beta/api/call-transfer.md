---
title: 'llamar a: transferencia'
description: Transferir una llamada activa.
ms.openlocfilehash: d02e028c4d7e3b51f3aee371e22d00b95841d9a0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087782"
---
# <a name="call-transfer"></a><span data-ttu-id="5ad08-103">llamar a: transferencia</span><span class="sxs-lookup"><span data-stu-id="5ad08-103">call: transfer</span></span>

> <span data-ttu-id="5ad08-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5ad08-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5ad08-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5ad08-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5ad08-106">Transferir una llamada activa.</span><span class="sxs-lookup"><span data-stu-id="5ad08-106">Transfer an active call.</span></span>

## <a name="permissions"></a><span data-ttu-id="5ad08-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5ad08-107">Permissions</span></span>
<span data-ttu-id="5ad08-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5ad08-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="5ad08-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5ad08-110">Permission type</span></span> | <span data-ttu-id="5ad08-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5ad08-111">Permissions (from least to most privileged)</span></span>         |
| :-------------- | :-------------------------------------------------- |
| <span data-ttu-id="5ad08-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5ad08-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="5ad08-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="5ad08-113">Not Supported</span></span>                |
| <span data-ttu-id="5ad08-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5ad08-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5ad08-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="5ad08-115">Not Supported</span></span>                |
| <span data-ttu-id="5ad08-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5ad08-116">Application</span></span>     | <span data-ttu-id="5ad08-117">Calls.Initiate.All</span><span class="sxs-lookup"><span data-stu-id="5ad08-117">Calls.Initiate.All</span></span>                                  |

## <a name="http-request"></a><span data-ttu-id="5ad08-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5ad08-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/transfer
POST /applications/{id}/calls/{id}/transfer
```

## <a name="request-headers"></a><span data-ttu-id="5ad08-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5ad08-119">Request headers</span></span>
| <span data-ttu-id="5ad08-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ad08-120">Name</span></span>          | <span data-ttu-id="5ad08-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ad08-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="5ad08-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="5ad08-122">Authorization</span></span> | <span data-ttu-id="5ad08-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5ad08-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5ad08-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5ad08-125">Request body</span></span>
<span data-ttu-id="5ad08-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="5ad08-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="5ad08-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5ad08-127">Parameter</span></span>      | <span data-ttu-id="5ad08-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ad08-128">Type</span></span>    |<span data-ttu-id="5ad08-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ad08-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5ad08-130">transferTarget</span><span class="sxs-lookup"><span data-stu-id="5ad08-130">transferTarget</span></span>|[<span data-ttu-id="5ad08-131">invitationParticipantInfo</span><span class="sxs-lookup"><span data-stu-id="5ad08-131">invitationParticipantInfo</span></span>](../resources/invitationparticipantinfo.md)|<span data-ttu-id="5ad08-132">El participante que es el destino de la transferencia.</span><span class="sxs-lookup"><span data-stu-id="5ad08-132">The participant which is the target of the transfer.</span></span>|
|<span data-ttu-id="5ad08-133">target</span><span class="sxs-lookup"><span data-stu-id="5ad08-133">target</span></span>|[<span data-ttu-id="5ad08-134">identitySet</span><span class="sxs-lookup"><span data-stu-id="5ad08-134">identitySet</span></span>](../resources/identityset.md)||
|<span data-ttu-id="5ad08-135">replacesCallId</span><span class="sxs-lookup"><span data-stu-id="5ad08-135">replacesCallId</span></span>|<span data-ttu-id="5ad08-136">String</span><span class="sxs-lookup"><span data-stu-id="5ad08-136">String</span></span>|<span data-ttu-id="5ad08-137">Identificador de llamada original del participante que se va a transferir.</span><span class="sxs-lookup"><span data-stu-id="5ad08-137">Original call id of the participant that is being transferred.</span></span>|
|<span data-ttu-id="5ad08-138">clientContext</span><span class="sxs-lookup"><span data-stu-id="5ad08-138">clientContext</span></span>|<span data-ttu-id="5ad08-139">String</span><span class="sxs-lookup"><span data-stu-id="5ad08-139">String</span></span>|<span data-ttu-id="5ad08-140">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="5ad08-140">The client context.</span></span>|

## <a name="response"></a><span data-ttu-id="5ad08-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5ad08-141">Response</span></span>
<span data-ttu-id="5ad08-142">Devuelve `202 Accepted` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="5ad08-142">Returns `202 Accepted` response code.</span></span>

## <a name="examples"></a><span data-ttu-id="5ad08-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5ad08-143">Examples</span></span>

### <a name="transfer-call-directly-with-no-user-involvement"></a><span data-ttu-id="5ad08-144">Transferir la llamada directamente, con sin intervención del usuario</span><span class="sxs-lookup"><span data-stu-id="5ad08-144">Transfer call directly, with no user involvement</span></span>

<span data-ttu-id="5ad08-145">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5ad08-145">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="5ad08-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5ad08-146">Request</span></span>
<span data-ttu-id="5ad08-147">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5ad08-147">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call_transfer"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/transfer
Content-Type: application/json
Content-Length: 430

{
  "transferTarget": {
    "endpointType": "default",
    "identity": {
      "user": {
        "id": "550fae72-d251-43ec-868c-373732c2704f",
        "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
        "displayName": "Heidi Steen"
      }
    },
    "languageId": "languageId-value",
    "region": "region-value",
    "replacesCallId": "replacesCallId-value"
  },
  "clientContext": "clientContext-value"
}
```

##### <a name="response"></a><span data-ttu-id="5ad08-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5ad08-148">Response</span></span>

> <span data-ttu-id="5ad08-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5ad08-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
}-->
```http
HTTP/1.1 202 Accepted
```

##### <a name="notification---transferring"></a><span data-ttu-id="5ad08-151">Notificación - transferencia</span><span class="sxs-lookup"><span data-stu-id="5ad08-151">Notification - transferring</span></span>

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
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896/operations/0FE0623FD62842EDB4BD8AC290072CC5",
      "resourceData": {
        "@odata.type": "#microsoft.graph.commsOperation",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896/operations/0FE0623FD62842EDB4BD8AC290072CC5",
        "@odata.etag": "W/\"54451\"",
        "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c",
        "resultInfo": {
          "code": "200",
          "subCode": "transferring"
        },
        "status": "running"
      }
    }
  ]
}
```

##### <a name="notification---transfer-accepted"></a><span data-ttu-id="5ad08-152">Notificación - transferencia aceptado</span><span class="sxs-lookup"><span data-stu-id="5ad08-152">Notification - transfer accepted</span></span>

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
        "resultInfo": {
          "code": "200",
          "subCode": "transferAccepted"
        },
        "status": "completed"
      }
    }
  ]
}
```

##### <a name="notification---terminated"></a><span data-ttu-id="5ad08-153">Notificación - terminada</span><span class="sxs-lookup"><span data-stu-id="5ad08-153">Notification - terminated</span></span>

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
        "terminationReason": "AppTransferred"
      }
    }
  ]
}
```

### <a name="consultative-transfer"></a><span data-ttu-id="5ad08-154">Transferencia de consulta</span><span class="sxs-lookup"><span data-stu-id="5ad08-154">Consultative transfer</span></span>

##### <a name="request"></a><span data-ttu-id="5ad08-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5ad08-155">Request</span></span>

```http
POST /app/calls/57DAB8B1894C409AB240BD8BEAE78896/transfer
Authorization: Bearer <TOKEN>
Content-Type: application/json
```
<!-- {
  "blockType": "ignored",
  "@odata.type": "call_transfer"
}-->
```json
{
  "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c",
  "transferTarget": {
    "endpointType": "default",
    "identity": {
      "user": {
        "id": "550fae72-d251-43ec-868c-373732c2704f",
        "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
        "displayName": "Heidi Steen"
      }
    },
    "languageId": "en-US",
    "region": "westus",
    "replacesCallId": "e5d39592-99bd-4db8-bca8-30fb894ec51d"
  }
}
```

##### <a name="response"></a><span data-ttu-id="5ad08-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5ad08-156">Response</span></span>

> <span data-ttu-id="5ad08-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5ad08-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 202 Accepted
```

##### <a name="notification---transferring"></a><span data-ttu-id="5ad08-159">Notificación - transferencia</span><span class="sxs-lookup"><span data-stu-id="5ad08-159">Notification - transferring</span></span>

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
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896/operations/0FE0623FD62842EDB4BD8AC290072CC5",
      "resourceData": {
        "@odata.type": "#microsoft.graph.commsOperation",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896/operations/0FE0623FD62842EDB4BD8AC290072CC5",
        "@odata.etag": "W/\"54451\"",
        "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c",
        "resultInfo": {
          "code": "200",
          "subCode": "transferring"
        },
        "status": "running"
      }
    }
  ]
}
```

##### <a name="notification---transfer-accepted"></a><span data-ttu-id="5ad08-160">Notificación - transferencia aceptado</span><span class="sxs-lookup"><span data-stu-id="5ad08-160">Notification - transfer accepted</span></span>

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
        "resultInfo": {
          "code": "200",
          "subCode": "transferAccepted"
        },
        "status": "completed"
      }
    }
  ]
}
```

##### <a name="notification---terminated"></a><span data-ttu-id="5ad08-161">Notificación - terminada</span><span class="sxs-lookup"><span data-stu-id="5ad08-161">Notification - terminated</span></span>

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
        "terminationReason": "AppTransferred"
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "call: transfer",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
