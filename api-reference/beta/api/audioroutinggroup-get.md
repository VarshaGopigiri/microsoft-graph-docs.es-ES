---
title: Obtener el grupo de enrutamiento de audio
description: Recuperar las propiedades y relaciones de un objeto audioRoutingGroup.
ms.openlocfilehash: ce1c8afea4932427a700970a16d3ec22a7f14d8d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084678"
---
# <a name="get-audio-routing-group"></a><span data-ttu-id="f3cbe-103">Obtener el grupo de enrutamiento de audio</span><span class="sxs-lookup"><span data-stu-id="f3cbe-103">Get audio routing group</span></span>

> <span data-ttu-id="f3cbe-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f3cbe-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f3cbe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f3cbe-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f3cbe-106">Recuperar las propiedades y relaciones de un objeto [audioRoutingGroup](../resources/audioroutinggroup.md) .</span><span class="sxs-lookup"><span data-stu-id="f3cbe-106">Retrieve the properties and relationships of an [audioRoutingGroup](../resources/audioroutinggroup.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="f3cbe-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f3cbe-107">Permissions</span></span>
<span data-ttu-id="f3cbe-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f3cbe-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="f3cbe-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f3cbe-110">Permission type</span></span>                        | <span data-ttu-id="f3cbe-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f3cbe-111">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="f3cbe-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f3cbe-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="f3cbe-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="f3cbe-113">Not Supported</span></span>                               |
| <span data-ttu-id="f3cbe-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f3cbe-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f3cbe-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="f3cbe-115">Not Supported</span></span>                               |
| <span data-ttu-id="f3cbe-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f3cbe-116">Application</span></span>     | <span data-ttu-id="f3cbe-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span><span class="sxs-lookup"><span data-stu-id="f3cbe-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f3cbe-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f3cbe-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /app/calls/{id}/audioRoutingGroups/{id}
GET /applications/{id}/calls/{id}/audioRoutingGroups/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f3cbe-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f3cbe-119">Optional query parameters</span></span>
<span data-ttu-id="f3cbe-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3cbe-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f3cbe-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f3cbe-121">Request headers</span></span>
| <span data-ttu-id="f3cbe-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="f3cbe-122">Name</span></span>          | <span data-ttu-id="f3cbe-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3cbe-123">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="f3cbe-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="f3cbe-124">Authorization</span></span> | <span data-ttu-id="f3cbe-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f3cbe-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f3cbe-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f3cbe-127">Request body</span></span>
<span data-ttu-id="f3cbe-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f3cbe-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f3cbe-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3cbe-129">Response</span></span>
<span data-ttu-id="f3cbe-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [audioRoutingGroup](../resources/audioroutinggroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3cbe-130">If successful, this method returns a `200 OK` response code and an [audioRoutingGroup](../resources/audioroutinggroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f3cbe-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3cbe-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="f3cbe-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3cbe-132">Request</span></span>
<span data-ttu-id="f3cbe-133">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3cbe-133">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_audioRoutingGroup"
}-->
```http
GET https://graph.microsoft.com/beta/app/calls/{id}/audioRoutingGroups/{id}
```

##### <a name="response"></a><span data-ttu-id="f3cbe-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3cbe-134">Response</span></span>

> <span data-ttu-id="f3cbe-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f3cbe-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
  "description": "Get audioRoutingGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->