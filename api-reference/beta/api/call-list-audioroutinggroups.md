---
title: Grupos de enrutamiento de audio de lista
description: Recuperar una lista de objetos de **audioRoutingGroup** .
ms.openlocfilehash: da6724f95fbc2c4365a1b1e4d34d317c130f12df
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087678"
---
# <a name="list-audio-routing-groups"></a><span data-ttu-id="bd978-103">Grupos de enrutamiento de audio de lista</span><span class="sxs-lookup"><span data-stu-id="bd978-103">List audio routing groups</span></span>

> <span data-ttu-id="bd978-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bd978-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bd978-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bd978-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bd978-106">Recuperar una lista de objetos de **audioRoutingGroup** .</span><span class="sxs-lookup"><span data-stu-id="bd978-106">Retrieve a list of **audioRoutingGroup** objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="bd978-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="bd978-107">Permissions</span></span>
<span data-ttu-id="bd978-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bd978-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="bd978-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bd978-110">Permission type</span></span>                        | <span data-ttu-id="bd978-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bd978-111">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="bd978-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bd978-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="bd978-113">No se admite.</span><span class="sxs-lookup"><span data-stu-id="bd978-113">Not Supported.</span></span>                               |
| <span data-ttu-id="bd978-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bd978-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bd978-115">No se admite.</span><span class="sxs-lookup"><span data-stu-id="bd978-115">Not Supported.</span></span>                               |
| <span data-ttu-id="bd978-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bd978-116">Application</span></span>     | <span data-ttu-id="bd978-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span><span class="sxs-lookup"><span data-stu-id="bd978-117">Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="bd978-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bd978-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /app/calls/{id}/audioRoutingGroups
GET /applications/{id}/calls/{id}/audioRoutingGroups
```

## <a name="optional-query-parameters"></a><span data-ttu-id="bd978-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bd978-119">Optional query parameters</span></span>
<span data-ttu-id="bd978-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd978-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="bd978-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bd978-121">Request headers</span></span>
| <span data-ttu-id="bd978-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="bd978-122">Name</span></span>          | <span data-ttu-id="bd978-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd978-123">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="bd978-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="bd978-124">Authorization</span></span> | <span data-ttu-id="bd978-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bd978-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bd978-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bd978-127">Request body</span></span>
<span data-ttu-id="bd978-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bd978-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bd978-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd978-129">Response</span></span>
<span data-ttu-id="bd978-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [audioRoutingGroup](../resources/audioroutinggroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd978-130">If successful, this method returns a `200 OK` response code and a collection of [audioRoutingGroup](../resources/audioroutinggroup.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bd978-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd978-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="bd978-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bd978-132">Request</span></span>
<span data-ttu-id="bd978-133">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd978-133">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_audioRoutingGroups"
}-->
```http
GET https://graph.microsoft.com/beta/app/calls/{id}/audioRoutingGroups
```

##### <a name="response"></a><span data-ttu-id="bd978-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd978-134">Response</span></span>

> <span data-ttu-id="bd978-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bd978-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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