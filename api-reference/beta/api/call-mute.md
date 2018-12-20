---
title: 'llamar a: silenciar'
description: Permite a la aplicación silenciar a sí mismo.
author: VinodRavichandran
ms.openlocfilehash: dc1baddb65521f4874f108dd28c7e9ec7b778a25
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380174"
---
# <a name="call-mute"></a><span data-ttu-id="df3aa-103">llamar a: silenciar</span><span class="sxs-lookup"><span data-stu-id="df3aa-103">call: mute</span></span>

> <span data-ttu-id="df3aa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="df3aa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="df3aa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="df3aa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="df3aa-106">Permite a la aplicación silenciar a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="df3aa-106">Allows the application to mute itself.</span></span>

## <a name="permissions"></a><span data-ttu-id="df3aa-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="df3aa-107">Permissions</span></span>
<span data-ttu-id="df3aa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="df3aa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="df3aa-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="df3aa-110">Permission type</span></span>                        | <span data-ttu-id="df3aa-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="df3aa-111">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="df3aa-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="df3aa-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="df3aa-113">No se admite.</span><span class="sxs-lookup"><span data-stu-id="df3aa-113">Not Supported.</span></span>                               |
| <span data-ttu-id="df3aa-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="df3aa-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="df3aa-115">No se admite.</span><span class="sxs-lookup"><span data-stu-id="df3aa-115">Not Supported.</span></span>                               |
| <span data-ttu-id="df3aa-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="df3aa-116">Application</span></span>                            | <span data-ttu-id="df3aa-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="df3aa-117">None.</span></span>                                        |

## <a name="http-request"></a><span data-ttu-id="df3aa-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="df3aa-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/mute
POST /applications/{id}/calls/{id}/mute
```

## <a name="request-headers"></a><span data-ttu-id="df3aa-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="df3aa-119">Request headers</span></span>
| <span data-ttu-id="df3aa-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="df3aa-120">Name</span></span>          | <span data-ttu-id="df3aa-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="df3aa-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="df3aa-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="df3aa-122">Authorization</span></span> | <span data-ttu-id="df3aa-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="df3aa-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="df3aa-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="df3aa-125">Request body</span></span>
<span data-ttu-id="df3aa-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="df3aa-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="df3aa-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="df3aa-127">Parameter</span></span>      | <span data-ttu-id="df3aa-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="df3aa-128">Type</span></span>    |<span data-ttu-id="df3aa-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="df3aa-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="df3aa-130">clientContext</span><span class="sxs-lookup"><span data-stu-id="df3aa-130">clientContext</span></span>|<span data-ttu-id="df3aa-131">String</span><span class="sxs-lookup"><span data-stu-id="df3aa-131">String</span></span>|<span data-ttu-id="df3aa-132">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="df3aa-132">The client context.</span></span>|

## <a name="response"></a><span data-ttu-id="df3aa-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df3aa-133">Response</span></span>
<span data-ttu-id="df3aa-134">Si tiene éxito, este método devuelve `200 OK` código de respuesta y un objeto [commsOperation](../resources/commsoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="df3aa-134">If successful, this method returns `200 OK` response code and a [commsOperation](../resources/commsoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="df3aa-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df3aa-135">Example</span></span>
<span data-ttu-id="df3aa-136">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="df3aa-136">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="df3aa-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="df3aa-137">Request</span></span>
<span data-ttu-id="df3aa-138">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="df3aa-138">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call-mute"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/mute
Content-Type: application/json
Content-Length: 46

{
  "clientContext": "clientContext-value"
}
```

##### <a name="response"></a><span data-ttu-id="df3aa-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df3aa-139">Response</span></span>

> <span data-ttu-id="df3aa-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="df3aa-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
  "description": "call: mute",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
