---
title: 'llamar a: reactivar audio'
description: Permite a la aplicación reactivar el audio de sí mismo.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: 3f010b7b7fb790b40455c8e09b785ffe29af0983
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27813681"
---
# <a name="call-unmute"></a><span data-ttu-id="979e0-103">llamar a: reactivar audio</span><span class="sxs-lookup"><span data-stu-id="979e0-103">call: unmute</span></span>

> <span data-ttu-id="979e0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="979e0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="979e0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="979e0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="979e0-106">Permite a la aplicación reactivar el audio de sí mismo.</span><span class="sxs-lookup"><span data-stu-id="979e0-106">Allows the application to unmute itself.</span></span>

## <a name="permissions"></a><span data-ttu-id="979e0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="979e0-107">Permissions</span></span>
<span data-ttu-id="979e0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="979e0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="979e0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="979e0-110">Permission type</span></span>                        | <span data-ttu-id="979e0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="979e0-111">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="979e0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="979e0-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="979e0-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="979e0-113">Not supported.</span></span>                               |
| <span data-ttu-id="979e0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="979e0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="979e0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="979e0-115">Not supported.</span></span>                               |
| <span data-ttu-id="979e0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="979e0-116">Application</span></span>                            | <span data-ttu-id="979e0-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="979e0-117">None.</span></span>                                        |

## <a name="http-request"></a><span data-ttu-id="979e0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="979e0-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/unmute
POST /applications/{id}/calls/{id}/unmute
```

## <a name="request-headers"></a><span data-ttu-id="979e0-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="979e0-119">Request headers</span></span>
| <span data-ttu-id="979e0-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="979e0-120">Name</span></span>          | <span data-ttu-id="979e0-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="979e0-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="979e0-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="979e0-122">Authorization</span></span> | <span data-ttu-id="979e0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="979e0-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="979e0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="979e0-125">Request body</span></span>
<span data-ttu-id="979e0-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="979e0-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="979e0-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="979e0-127">Parameter</span></span>      | <span data-ttu-id="979e0-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="979e0-128">Type</span></span>    |<span data-ttu-id="979e0-129">Description</span><span class="sxs-lookup"><span data-stu-id="979e0-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="979e0-130">clientContext</span><span class="sxs-lookup"><span data-stu-id="979e0-130">clientContext</span></span>|<span data-ttu-id="979e0-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="979e0-131">String</span></span>|<span data-ttu-id="979e0-132">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="979e0-132">The client context.</span></span>|

## <a name="response"></a><span data-ttu-id="979e0-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="979e0-133">Response</span></span>
<span data-ttu-id="979e0-134">Si tiene éxito, este método devuelve `200 OK` objeto de código y [commsOperation](../resources/commsoperation.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="979e0-134">If successful, this method returns `200 OK` response code and [commsOperation](../resources/commsoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="979e0-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="979e0-135">Example</span></span>
<span data-ttu-id="979e0-136">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="979e0-136">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="979e0-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="979e0-137">Request</span></span>
<span data-ttu-id="979e0-138">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="979e0-138">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call-unmute"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/unmute
Content-Type: application/json
Content-Length: 46

{
  "clientContext": "clientContext-value"
}
```

##### <a name="response"></a><span data-ttu-id="979e0-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="979e0-139">Response</span></span>

> <span data-ttu-id="979e0-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="979e0-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
  "description": "call: unmute",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
