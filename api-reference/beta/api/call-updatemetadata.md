---
title: 'llamar a: updateMetadata'
description: Actualizar los metadatos de la aplicación asociado con una llamada.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 19e56c3ac00aa0b61efef6be3a25020166e364d4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976481"
---
# <a name="call-updatemetadata"></a><span data-ttu-id="16b62-103">llamar a: updateMetadata</span><span class="sxs-lookup"><span data-stu-id="16b62-103">call: updateMetadata</span></span>

> <span data-ttu-id="16b62-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="16b62-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="16b62-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="16b62-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="16b62-106">Actualizar los metadatos de la aplicación asociado con una llamada.</span><span class="sxs-lookup"><span data-stu-id="16b62-106">Update the appliation's metadata associated with a call.</span></span>

## <a name="permissions"></a><span data-ttu-id="16b62-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="16b62-107">Permissions</span></span>
<span data-ttu-id="16b62-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="16b62-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="16b62-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="16b62-110">Permission type</span></span>                        | <span data-ttu-id="16b62-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="16b62-111">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="16b62-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="16b62-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="16b62-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="16b62-113">Not Supported</span></span>                               |
| <span data-ttu-id="16b62-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="16b62-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="16b62-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="16b62-115">Not Supported</span></span>                               |
| <span data-ttu-id="16b62-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="16b62-116">Application</span></span>     | <span data-ttu-id="16b62-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span><span class="sxs-lookup"><span data-stu-id="16b62-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="16b62-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="16b62-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/updateMetadata
POST /applications/{id}/calls/{id}/updateMetadata
```

## <a name="request-headers"></a><span data-ttu-id="16b62-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="16b62-119">Request headers</span></span>
| <span data-ttu-id="16b62-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="16b62-120">Name</span></span>          | <span data-ttu-id="16b62-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="16b62-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="16b62-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="16b62-122">Authorization</span></span> | <span data-ttu-id="16b62-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="16b62-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="16b62-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="16b62-125">Request body</span></span>
<span data-ttu-id="16b62-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="16b62-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="16b62-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="16b62-127">Parameter</span></span>      | <span data-ttu-id="16b62-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="16b62-128">Type</span></span>    |<span data-ttu-id="16b62-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="16b62-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="16b62-130">metadatos</span><span class="sxs-lookup"><span data-stu-id="16b62-130">metadata</span></span>|<span data-ttu-id="16b62-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b62-131">String</span></span>|<span data-ttu-id="16b62-132">Un blob de datos proporcionados por el participante en la lista de participantes.</span><span class="sxs-lookup"><span data-stu-id="16b62-132">A blob of data provided by the participant in the roster.</span></span>|
|<span data-ttu-id="16b62-133">clientContext</span><span class="sxs-lookup"><span data-stu-id="16b62-133">clientContext</span></span>|<span data-ttu-id="16b62-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b62-134">String</span></span>|<span data-ttu-id="16b62-135">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="16b62-135">The client context.</span></span>|

## <a name="response"></a><span data-ttu-id="16b62-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16b62-136">Response</span></span>
<span data-ttu-id="16b62-137">Devuelve `202 Accepted` código de respuesta y un encabezado de ubicación con un uri para el [commsOperation](../resources/commsoperation.md) creado para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="16b62-137">Returns `202 Accepted` response code and a Location header with a uri to the [commsOperation](../resources/commsoperation.md) created for this request.</span></span>

## <a name="example"></a><span data-ttu-id="16b62-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="16b62-138">Example</span></span>
<span data-ttu-id="16b62-139">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="16b62-139">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="16b62-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16b62-140">Request</span></span>
<span data-ttu-id="16b62-141">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="16b62-141">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call-updateMetadata"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/updateMetadata
Content-Type: application/json
Content-Length: 79

{
  "metadata": "metadata-value",
  "clientContext": "clientContext-value"
}
```

##### <a name="response"></a><span data-ttu-id="16b62-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16b62-142">Response</span></span>

> <span data-ttu-id="16b62-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="16b62-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.commsOperation"
} -->
```http
HTTP/1.1 202 Accepted
Location: https://graph.microsoft.com/beta/app/calls/57dab8b1-894c-409a-b240-bd8beae78896/operations/0fe0623f-d628-42ed-b4bd-8ac290072cc5
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "call: updateMetadata",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
