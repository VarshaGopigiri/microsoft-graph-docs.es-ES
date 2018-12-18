---
title: Obtener el grupo de enrutamiento de audio
description: Recuperar las propiedades y relaciones de un objeto audioRoutingGroup.
author: VinodRavichandran
ms.openlocfilehash: e6aca0300287e502fd065d69db1ce4855a42b823
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331426"
---
# <a name="get-audio-routing-group"></a><span data-ttu-id="908a6-103">Obtener el grupo de enrutamiento de audio</span><span class="sxs-lookup"><span data-stu-id="908a6-103">Get audio routing group</span></span>

> <span data-ttu-id="908a6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="908a6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="908a6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="908a6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="908a6-106">Recuperar las propiedades y relaciones de un objeto [audioRoutingGroup](../resources/audioroutinggroup.md) .</span><span class="sxs-lookup"><span data-stu-id="908a6-106">Retrieve the properties and relationships of an [audioRoutingGroup](../resources/audioroutinggroup.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="908a6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="908a6-107">Permissions</span></span>
<span data-ttu-id="908a6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="908a6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="908a6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="908a6-110">Permission type</span></span>                        | <span data-ttu-id="908a6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="908a6-111">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="908a6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="908a6-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="908a6-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="908a6-113">Not Supported</span></span>                               |
| <span data-ttu-id="908a6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="908a6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="908a6-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="908a6-115">Not Supported</span></span>                               |
| <span data-ttu-id="908a6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="908a6-116">Application</span></span>     | <span data-ttu-id="908a6-117">Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span><span class="sxs-lookup"><span data-stu-id="908a6-117">Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="908a6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="908a6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /app/calls/{id}/audioRoutingGroups/{id}
GET /applications/{id}/calls/{id}/audioRoutingGroups/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="908a6-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="908a6-119">Optional query parameters</span></span>
<span data-ttu-id="908a6-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="908a6-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="908a6-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="908a6-121">Request headers</span></span>
| <span data-ttu-id="908a6-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="908a6-122">Name</span></span>          | <span data-ttu-id="908a6-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="908a6-123">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="908a6-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="908a6-124">Authorization</span></span> | <span data-ttu-id="908a6-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="908a6-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="908a6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="908a6-127">Request body</span></span>
<span data-ttu-id="908a6-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="908a6-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="908a6-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="908a6-129">Response</span></span>
<span data-ttu-id="908a6-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [audioRoutingGroup](../resources/audioroutinggroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="908a6-130">If successful, this method returns a `200 OK` response code and an [audioRoutingGroup](../resources/audioroutinggroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="908a6-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="908a6-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="908a6-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="908a6-132">Request</span></span>
<span data-ttu-id="908a6-133">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="908a6-133">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_audioRoutingGroup"
}-->
```http
GET https://graph.microsoft.com/beta/app/calls/{id}/audioRoutingGroups/{id}
```

##### <a name="response"></a><span data-ttu-id="908a6-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="908a6-134">Response</span></span>

> <span data-ttu-id="908a6-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="908a6-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
