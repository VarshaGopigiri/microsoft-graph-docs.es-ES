---
title: 'participante: muteAll'
description: Silenciar a todos los participantes de la llamada.
ms.openlocfilehash: f0da6f44801559fe7258d61fff9d5c87cc606702
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084147"
---
# <a name="participant-muteall"></a><span data-ttu-id="c70c6-103">participante: muteAll</span><span class="sxs-lookup"><span data-stu-id="c70c6-103">participant: muteAll</span></span>

> <span data-ttu-id="c70c6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c70c6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c70c6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c70c6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c70c6-106">Silenciar a todos los participantes de la llamada.</span><span class="sxs-lookup"><span data-stu-id="c70c6-106">Mute all participants in the call.</span></span>

## <a name="permissions"></a><span data-ttu-id="c70c6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c70c6-107">Permissions</span></span>
<span data-ttu-id="c70c6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c70c6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="c70c6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c70c6-110">Permission type</span></span>                        | <span data-ttu-id="c70c6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c70c6-111">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="c70c6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c70c6-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="c70c6-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="c70c6-113">Not Supported</span></span>                               |
| <span data-ttu-id="c70c6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c70c6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c70c6-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="c70c6-115">Not Supported</span></span>                               |
| <span data-ttu-id="c70c6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c70c6-116">Application</span></span>                            | <span data-ttu-id="c70c6-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c70c6-117">None</span></span>                                        |

## <a name="http-request"></a><span data-ttu-id="c70c6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c70c6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/participants/muteAll
POST /applications/{id}/calls/{id}/participants/muteAll
```

## <a name="request-headers"></a><span data-ttu-id="c70c6-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c70c6-119">Request headers</span></span>
| <span data-ttu-id="c70c6-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c70c6-120">Name</span></span>          | <span data-ttu-id="c70c6-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c70c6-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="c70c6-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c70c6-122">Authorization</span></span> | <span data-ttu-id="c70c6-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c70c6-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c70c6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c70c6-125">Request body</span></span>
<span data-ttu-id="c70c6-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c70c6-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c70c6-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c70c6-127">Parameter</span></span>      | <span data-ttu-id="c70c6-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="c70c6-128">Type</span></span>    |<span data-ttu-id="c70c6-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="c70c6-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c70c6-130">participants</span><span class="sxs-lookup"><span data-stu-id="c70c6-130">participants</span></span>|<span data-ttu-id="c70c6-131">Colección String</span><span class="sxs-lookup"><span data-stu-id="c70c6-131">String collection</span></span>|<span data-ttu-id="c70c6-132">Los participantes que se ha desactivado.</span><span class="sxs-lookup"><span data-stu-id="c70c6-132">The participants to be muted.</span></span>|
|<span data-ttu-id="c70c6-133">clientContext</span><span class="sxs-lookup"><span data-stu-id="c70c6-133">clientContext</span></span>|<span data-ttu-id="c70c6-134">String</span><span class="sxs-lookup"><span data-stu-id="c70c6-134">String</span></span>|<span data-ttu-id="c70c6-135">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="c70c6-135">The client context.</span></span>|

## <a name="response"></a><span data-ttu-id="c70c6-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c70c6-136">Response</span></span>
<span data-ttu-id="c70c6-137">Si tiene éxito, este método devuelve `200 OK` objeto de código y [commsOperation](../resources/commsoperation.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c70c6-137">If successful, this method returns `200 OK` response code and [commsOperation](../resources/commsoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c70c6-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c70c6-138">Example</span></span>
<span data-ttu-id="c70c6-139">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c70c6-139">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="c70c6-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c70c6-140">Request</span></span>
<span data-ttu-id="c70c6-141">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c70c6-141">The following example shows the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "participant_muteAll"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/participants/muteAll
Content-Type: application/json
Content-Length: 81

{
  "participants": [
    ""
  ],
  "clientContext": "clientContext-value"
}
```

##### <a name="response"></a><span data-ttu-id="c70c6-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c70c6-142">Response</span></span>

> <span data-ttu-id="c70c6-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c70c6-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.commsOperation"
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "participant: muteAll",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->