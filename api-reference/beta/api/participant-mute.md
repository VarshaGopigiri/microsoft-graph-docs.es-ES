---
title: 'participante: silenciar'
description: Desactivar a un participante específico en la llamada.
ms.openlocfilehash: 939fd0fd94304318786b0ecb7ae72da28b55e4b9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085931"
---
# <a name="participant-mute"></a><span data-ttu-id="8c19c-103">participante: silenciar</span><span class="sxs-lookup"><span data-stu-id="8c19c-103">participant: mute</span></span>

> <span data-ttu-id="8c19c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8c19c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8c19c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8c19c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8c19c-106">Desactivar a un participante específico en la llamada.</span><span class="sxs-lookup"><span data-stu-id="8c19c-106">Mute a specific participant in the call.</span></span>

## <a name="permissions"></a><span data-ttu-id="8c19c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="8c19c-107">Permissions</span></span>
<span data-ttu-id="8c19c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8c19c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="8c19c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8c19c-110">Permission type</span></span> | <span data-ttu-id="8c19c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8c19c-111">Permissions (from least to most privileged)</span></span> |
| :-------------- | :------------------------------------------ |
| <span data-ttu-id="8c19c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8c19c-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="8c19c-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="8c19c-113">Not Supported</span></span>        |
| <span data-ttu-id="8c19c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8c19c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8c19c-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="8c19c-115">Not Supported</span></span>        |
| <span data-ttu-id="8c19c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8c19c-116">Application</span></span>     | <span data-ttu-id="8c19c-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8c19c-117">None</span></span>                                        |

## <a name="http-request"></a><span data-ttu-id="8c19c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8c19c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/participants/{id}/mute
POST /applications/{id}/calls/{id}/participants/{id}/mute
```

## <a name="request-headers"></a><span data-ttu-id="8c19c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8c19c-119">Request headers</span></span>
| <span data-ttu-id="8c19c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="8c19c-120">Name</span></span>          | <span data-ttu-id="8c19c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c19c-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="8c19c-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="8c19c-122">Authorization</span></span> | <span data-ttu-id="8c19c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8c19c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8c19c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8c19c-125">Request body</span></span>
<span data-ttu-id="8c19c-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="8c19c-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="8c19c-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="8c19c-127">Parameter</span></span>      | <span data-ttu-id="8c19c-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c19c-128">Type</span></span>    |<span data-ttu-id="8c19c-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c19c-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8c19c-130">clientContext</span><span class="sxs-lookup"><span data-stu-id="8c19c-130">clientContext</span></span>|<span data-ttu-id="8c19c-131">String</span><span class="sxs-lookup"><span data-stu-id="8c19c-131">String</span></span>|<span data-ttu-id="8c19c-132">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="8c19c-132">The client context.</span></span>|

## <a name="response"></a><span data-ttu-id="8c19c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c19c-133">Response</span></span>
<span data-ttu-id="8c19c-134">Si tiene éxito, este método devuelve `200 OK` objeto de código y [commsOperation](../resources/commsoperation.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c19c-134">If successful, this method returns `200 OK` response code and [commsOperation](../resources/commsoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8c19c-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c19c-135">Example</span></span>
<span data-ttu-id="8c19c-136">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="8c19c-136">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="8c19c-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8c19c-137">Request</span></span>
<span data-ttu-id="8c19c-138">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8c19c-138">The following example shows the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "participant_mute"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/participants/{id}/mute
Content-Type: application/json
Content-Length: 46

{
  "clientContext": "clientContext-value"
}
```

##### <a name="response"></a><span data-ttu-id="8c19c-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c19c-139">Response</span></span>

> <span data-ttu-id="8c19c-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8c19c-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "@odata.type": "microsoft.graph.commsOperation",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 259

{
  "id": "17e3b46c-f61d-4f4d-9635-c626ef18e6ad",
  "status": "completed",
  "createdDateTime": "2018-09-06T15:58:41Z",
  "lastActionDateTime": "2018-09-06T15:58:41Z",
  "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c"
}
```

## <a name="example---mute-specific-participant"></a><span data-ttu-id="8c19c-142">Por ejemplo, desactivar el participante específico</span><span class="sxs-lookup"><span data-stu-id="8c19c-142">Example - Mute specific participant</span></span>

##### <a name="request"></a><span data-ttu-id="8c19c-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8c19c-143">Request</span></span>

```http
POST /app/calls/57DAB8B1894C409AB240BD8BEAE78896/participants/0698446E77E24E4D85F80597083CB830/mute
Authorization: Bearer <TOKEN>
Content-Type: application/json

{
  "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c"
}
```

##### <a name="response"></a><span data-ttu-id="8c19c-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c19c-144">Response</span></span>

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 259
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsOperation",
  "truncated": true
}-->
```json
{
  "id": "17e3b46c-f61d-4f4d-9635-c626ef18e6ad",
  "status": "completed",
  "createdDateTime": "2018-09-06T15:58:41Z",
  "lastActionDateTime": "2018-09-06T15:58:41Z",
  "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c"
}
```

##### <a name="notification---roster-updated-with-participant-muted"></a><span data-ttu-id="8c19c-145">Notificación: lista de participantes se actualizó con participante ha desactivado</span><span class="sxs-lookup"><span data-stu-id="8c19c-145">Notification - roster updated with participant muted</span></span>

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
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896/participants",
      "resourceData": [
        {
          "@odata.type": "#microsoft.graph.participant",
          "id": "0698446E77E24E4D85F80597083CB830",
          "info": {
            "identity": {
              "user": {
                "displayName": "Test User",
                "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
              }
            },
            "region": "westus",
            "languageId": "en-US"
          },
          "mediaStreams": [
            {
              "mediaType": "audio",
              "label": "main-audio",
              "sourceId": "1",
              "direction": "sendReceive",
              "serverMuted": false
            }
          ],
          "isMuted": true,
          "isInLobby": false
        },
        {
          "@odata.type": "#microsoft.graph.participant",
          "id": "123456W77E24E4D85F80597083CB830",
          "info": {
            "identity": {
              "application": {
                "displayName": "Test Bot",
                "id": "1234A46B-3D17-4ADC-8DCE-DC4E7D556789"
              }
            },
            "region": "westus",
            "languageId": "en-US"
          },
          "mediaStreams": [
            {
              "mediaType": "audio",
              "label": "main-audio",
              "sourceId": "2",
              "direction": "sendReceive",
              "serverMuted": false
            }
          ],
          "isInLobby": false
        }
      ]
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "participant: mute",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
