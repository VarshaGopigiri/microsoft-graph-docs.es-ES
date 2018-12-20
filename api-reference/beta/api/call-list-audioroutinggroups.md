---
title: Grupos de enrutamiento de audio de lista
description: Recuperar una lista de objetos de **audioRoutingGroup** .
author: VinodRavichandran
ms.openlocfilehash: 7ed00bbd3d000e71afe55a5e663408139174640b
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380138"
---
# <a name="list-audio-routing-groups"></a><span data-ttu-id="ee271-103">Grupos de enrutamiento de audio de lista</span><span class="sxs-lookup"><span data-stu-id="ee271-103">List audio routing groups</span></span>

> <span data-ttu-id="ee271-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ee271-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ee271-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ee271-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ee271-106">Recuperar una lista de objetos de **audioRoutingGroup** .</span><span class="sxs-lookup"><span data-stu-id="ee271-106">Retrieve a list of **audioRoutingGroup** objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="ee271-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ee271-107">Permissions</span></span>
<span data-ttu-id="ee271-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ee271-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ee271-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ee271-110">Permission type</span></span>                        | <span data-ttu-id="ee271-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ee271-111">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="ee271-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ee271-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="ee271-113">No se admite.</span><span class="sxs-lookup"><span data-stu-id="ee271-113">Not Supported.</span></span>                               |
| <span data-ttu-id="ee271-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ee271-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ee271-115">No se admite.</span><span class="sxs-lookup"><span data-stu-id="ee271-115">Not Supported.</span></span>                               |
| <span data-ttu-id="ee271-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ee271-116">Application</span></span>     | <span data-ttu-id="ee271-117">Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span><span class="sxs-lookup"><span data-stu-id="ee271-117">Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ee271-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ee271-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /app/calls/{id}/audioRoutingGroups
GET /applications/{id}/calls/{id}/audioRoutingGroups
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ee271-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ee271-119">Optional query parameters</span></span>
<span data-ttu-id="ee271-120">Este método es compatible con los [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee271-120">This method supports the [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ee271-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ee271-121">Request headers</span></span>
| <span data-ttu-id="ee271-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="ee271-122">Name</span></span>          | <span data-ttu-id="ee271-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee271-123">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="ee271-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ee271-124">Authorization</span></span> | <span data-ttu-id="ee271-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ee271-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ee271-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ee271-127">Request body</span></span>
<span data-ttu-id="ee271-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ee271-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ee271-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee271-129">Response</span></span>
<span data-ttu-id="ee271-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [audioRoutingGroup](../resources/audioroutinggroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee271-130">If successful, this method returns a `200 OK` response code and a collection of [audioRoutingGroup](../resources/audioroutinggroup.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ee271-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee271-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="ee271-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ee271-132">Request</span></span>
<span data-ttu-id="ee271-133">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ee271-133">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get-audioRoutingGroups"
}-->
```http
GET https://graph.microsoft.com/beta/app/calls/{id}/audioRoutingGroups
```

##### <a name="response"></a><span data-ttu-id="ee271-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee271-134">Response</span></span>

> <span data-ttu-id="ee271-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ee271-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.audioRoutingGroup",
  "isCollection": true 
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 302

{
  "value": [
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List audioRoutingGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
