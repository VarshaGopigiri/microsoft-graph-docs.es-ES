---
title: Crear grupo de enrutamiento de audio
description: Crear un nuevo **audioRoutingGroup**.
ms.openlocfilehash: 9e42fb085887cee22ccc8eac0997adf0464e0d55
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084958"
---
# <a name="create-audio-routing-group"></a><span data-ttu-id="96cf8-103">Crear grupo de enrutamiento de audio</span><span class="sxs-lookup"><span data-stu-id="96cf8-103">Create audio routing group</span></span>

> <span data-ttu-id="96cf8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="96cf8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="96cf8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="96cf8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="96cf8-106">Crear un nuevo **audioRoutingGroup**.</span><span class="sxs-lookup"><span data-stu-id="96cf8-106">Create a new **audioRoutingGroup**.</span></span>

## <a name="permissions"></a><span data-ttu-id="96cf8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="96cf8-107">Permissions</span></span>
<span data-ttu-id="96cf8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="96cf8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="96cf8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="96cf8-110">Permission type</span></span>                        | <span data-ttu-id="96cf8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="96cf8-111">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="96cf8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="96cf8-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="96cf8-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="96cf8-113">Not supported.</span></span>                               |
| <span data-ttu-id="96cf8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="96cf8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="96cf8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="96cf8-115">Not supported.</span></span>                               |
| <span data-ttu-id="96cf8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="96cf8-116">Application</span></span>     | <span data-ttu-id="96cf8-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span><span class="sxs-lookup"><span data-stu-id="96cf8-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="96cf8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="96cf8-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/audioRoutingGroups
POST /applications/{id}/calls/{id}/audioRoutingGroups
```

## <a name="request-headers"></a><span data-ttu-id="96cf8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="96cf8-119">Request headers</span></span>
| <span data-ttu-id="96cf8-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="96cf8-120">Name</span></span>          | <span data-ttu-id="96cf8-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="96cf8-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="96cf8-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="96cf8-122">Authorization</span></span> | <span data-ttu-id="96cf8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="96cf8-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="96cf8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="96cf8-125">Request body</span></span>
<span data-ttu-id="96cf8-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [audioRoutingGroup](../resources/audioroutinggroup.md) .</span><span class="sxs-lookup"><span data-stu-id="96cf8-126">In the request body, supply a JSON representation of [audioRoutingGroup](../resources/audioroutinggroup.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="96cf8-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="96cf8-127">Response</span></span>
<span data-ttu-id="96cf8-128">Si tiene éxito, este método devuelve `200 OK` objeto de código y [audioRoutingGroup](../resources/audioroutinggroup.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="96cf8-128">If successful, this method returns `200 OK` response code and [audioRoutingGroup](../resources/audioroutinggroup.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="96cf8-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="96cf8-129">Examples</span></span>

### <a name="example-1-one-to-one-audio-routing-group"></a><span data-ttu-id="96cf8-130">En el ejemplo 1: Grupo uno a uno de enrutamiento de audio</span><span class="sxs-lookup"><span data-stu-id="96cf8-130">Example 1: One-to-one audio routing group</span></span>

##### <a name="request"></a><span data-ttu-id="96cf8-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="96cf8-131">Request</span></span>
<span data-ttu-id="96cf8-132">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="96cf8-132">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_audioRoutingGroup_from_call"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/audioRoutingGroups
Content-Type: application/json
Content-Length: 233

{
  "id": "oneToOne",
  "routingMode": "oneToOne",
  "sources": [
    "632899f8-2ea1-4604-8413-27bd2892079f"
  ],
  "receivers": [
    "550fae72-d251-43ec-868c-373732c2704f"
  ]
}
```

<span data-ttu-id="96cf8-133">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [audioRoutingGroup](../resources/audioroutinggroup.md) .</span><span class="sxs-lookup"><span data-stu-id="96cf8-133">In the request body, supply a JSON representation of [audioRoutingGroup](../resources/audioroutinggroup.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="96cf8-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="96cf8-134">Response</span></span>

> <span data-ttu-id="96cf8-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="96cf8-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
    "550fae72-d251-43ec-868c-373732c2704f"
  ]
}
```
### <a name="example-2-multicast-audioroutinggroup"></a><span data-ttu-id="96cf8-137">Ejemplo 2: Multidifusión audioRoutingGroup</span><span class="sxs-lookup"><span data-stu-id="96cf8-137">Example 2: Multicast audioRoutingGroup</span></span>

##### <a name="request"></a><span data-ttu-id="96cf8-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="96cf8-138">Request</span></span>
<span data-ttu-id="96cf8-139">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="96cf8-139">The following example shows the request.</span></span>

```http
POST https://graph.microsoft.com/beta/app/calls/{id}/audioRoutingGroups
Content-Type: application/json
Content-Length: 233
```

<!-- {
  "blockType": "example",
  "name": "create_audioRoutingGroup_from_call",
  "@odata.type": "microsoft.graph.audioRoutingGroup"
}-->

```json
{
  "id": "multicast",
  "routingMode": "multicast",
  "sources": [
    "632899f8-2ea1-4604-8413-27bd2892079f"
  ],
  "receivers": [
    "550fae72-d251-43ec-868c-373732c2704f",
    "72f988bf-86f1-41af-91ab-2d7cd011db47"
  ]
}
```

<span data-ttu-id="96cf8-140">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [audioRoutingGroup](../resources/audioroutinggroup.md) .</span><span class="sxs-lookup"><span data-stu-id="96cf8-140">In the request body, supply a JSON representation of [audioRoutingGroup](../resources/audioroutinggroup.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="96cf8-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="96cf8-141">Response</span></span>

> <span data-ttu-id="96cf8-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="96cf8-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 233
```
<!-- {
  "blockType": "example",
  "truncated": true,
  "@odata.type": "microsoft.graph.audioRoutingGroup"
} -->

```json
{
  "id": "multicast",
  "routingMode": "multicast",
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
  "description": "Create audioRoutingGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->