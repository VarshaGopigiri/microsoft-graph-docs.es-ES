---
title: Actualizar el grupo de enrutamiento de audio
description: Modificar orígenes y receptores de un audioRoutingGroup.
ms.openlocfilehash: a6b5d2ed3c11733f7a8e46ed4db61def05395c5c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085631"
---
# <a name="update-audio-routing-group"></a><span data-ttu-id="338e2-103">Actualizar el grupo de enrutamiento de audio</span><span class="sxs-lookup"><span data-stu-id="338e2-103">Update audio routing group</span></span>

> <span data-ttu-id="338e2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="338e2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="338e2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="338e2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="338e2-106">Modificar orígenes y receptores de un [audioRoutingGroup](../resources/audioroutinggroup.md).</span><span class="sxs-lookup"><span data-stu-id="338e2-106">Modify sources and receivers of an [audioRoutingGroup](../resources/audioroutinggroup.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="338e2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="338e2-107">Permissions</span></span>
<span data-ttu-id="338e2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="338e2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="338e2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="338e2-110">Permission type</span></span> | <span data-ttu-id="338e2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="338e2-111">Permissions (from least to most privileged)</span></span>                |
| :-------------- | :--------------------------------------------------------- |
| <span data-ttu-id="338e2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="338e2-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="338e2-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="338e2-113">Not Supported</span></span>                       |
| <span data-ttu-id="338e2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="338e2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="338e2-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="338e2-115">Not Supported</span></span>                       |
| <span data-ttu-id="338e2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="338e2-116">Application</span></span>     | <span data-ttu-id="338e2-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span><span class="sxs-lookup"><span data-stu-id="338e2-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="338e2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="338e2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /app/calls/{id}/audioRoutingGroups/{id}
PATCH /applications/{id}/calls/{id}/audioRoutingGroups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="338e2-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="338e2-119">Request headers</span></span>
| <span data-ttu-id="338e2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="338e2-120">Name</span></span>          | <span data-ttu-id="338e2-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="338e2-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="338e2-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="338e2-122">Authorization</span></span> | <span data-ttu-id="338e2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="338e2-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="338e2-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="338e2-125">Request body</span></span>
<span data-ttu-id="338e2-126">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="338e2-126">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="338e2-127">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="338e2-127">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="338e2-128">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="338e2-128">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="338e2-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="338e2-129">Property</span></span>       | <span data-ttu-id="338e2-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="338e2-130">Type</span></span>    |<span data-ttu-id="338e2-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="338e2-131">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="338e2-132">receptores de</span><span class="sxs-lookup"><span data-stu-id="338e2-132">receivers</span></span> | <span data-ttu-id="338e2-133">Colección String</span><span class="sxs-lookup"><span data-stu-id="338e2-133">String collection</span></span> | <span data-ttu-id="338e2-134">Los participantes de destino en la audioRoutingGroup.</span><span class="sxs-lookup"><span data-stu-id="338e2-134">The target participants in the audioRoutingGroup.</span></span> |
| <span data-ttu-id="338e2-135">routingMode</span><span class="sxs-lookup"><span data-stu-id="338e2-135">routingMode</span></span> | <span data-ttu-id="338e2-136">String</span><span class="sxs-lookup"><span data-stu-id="338e2-136">String</span></span> | <span data-ttu-id="338e2-137">Los valores posibles son: `oneToOne` y `multicast`.</span><span class="sxs-lookup"><span data-stu-id="338e2-137">Possible values are: `oneToOne`, `multicast`.</span></span> |
| <span data-ttu-id="338e2-138">orígenes</span><span class="sxs-lookup"><span data-stu-id="338e2-138">sources</span></span> | <span data-ttu-id="338e2-139">Colección String</span><span class="sxs-lookup"><span data-stu-id="338e2-139">String collection</span></span> | <span data-ttu-id="338e2-140">El participante de origen en el audioRoutingGroup.</span><span class="sxs-lookup"><span data-stu-id="338e2-140">The source participant in the audioRoutingGroup.</span></span> |

## <a name="response"></a><span data-ttu-id="338e2-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="338e2-141">Response</span></span>
<span data-ttu-id="338e2-142">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [audioRoutingGroup](../resources/audioroutinggroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="338e2-142">If successful, this method returns a `200 OK` response code and an updated [audioRoutingGroup](../resources/audioroutinggroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="338e2-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="338e2-143">Example</span></span>

##### <a name="request"></a><span data-ttu-id="338e2-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="338e2-144">Request</span></span>
<span data-ttu-id="338e2-145">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="338e2-145">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_audioRoutingGroup"
}-->
```http
PATCH https://graph.microsoft.com/beta/app/calls/{id}/audioRoutingGroups/{id}
Content-Type: application/json
Content-Length: 233

{
  "id": "oneToOne",
  "routingMode": "oneToOne",
  "sources": [
    "632899f8-2ea1-4604-8413-27bd2892079f"
  ],
  "receivers": [
    "550fae72-d251-43ec-868c-373732c2704f",
    "72f988bf-86f1-41af-91ab-2d7cd011db47"
  ]
}
```
##### <a name="response"></a><span data-ttu-id="338e2-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="338e2-146">Response</span></span>

> <span data-ttu-id="338e2-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="338e2-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.audioRoutingGroup"
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 233

{
  "id": "oneToOne",
  "routingMode": "oneToOne",
  "sources": [
    "632899f8-2ea1-4604-8413-27bd2892079f"
  ],
  "receivers": [
    "550fae72-d251-43ec-868c-373732c2704f",
    "72f988bf-86f1-41af-91ab-2d7cd011db47"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update audioRoutingGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->