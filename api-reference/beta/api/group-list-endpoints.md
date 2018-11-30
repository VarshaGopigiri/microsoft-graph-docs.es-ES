---
title: Extremos de lista
description: Recuperar una lista de objetos de extremo.
ms.openlocfilehash: 350cf31897a22b5cc6342a7e1fc6537f49fb2daa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084990"
---
# <a name="list-endpoints"></a><span data-ttu-id="974c3-103">Extremos de lista</span><span class="sxs-lookup"><span data-stu-id="974c3-103">List endpoints</span></span>

> <span data-ttu-id="974c3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="974c3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="974c3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="974c3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="974c3-106">Recuperar una lista de objetos de [extremo](../resources/endpoint.md) .</span><span class="sxs-lookup"><span data-stu-id="974c3-106">Retrieve a list of [endpoint](../resources/endpoint.md) objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="974c3-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="974c3-107">Permissions</span></span>
<span data-ttu-id="974c3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="974c3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="974c3-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="974c3-110">Permission type</span></span>      | <span data-ttu-id="974c3-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="974c3-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="974c3-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="974c3-112">Delegated (work or school account)</span></span> | <span data-ttu-id="974c3-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="974c3-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="974c3-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="974c3-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="974c3-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="974c3-115">Not supported.</span></span>    |
|<span data-ttu-id="974c3-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="974c3-116">Application</span></span> | <span data-ttu-id="974c3-117">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="974c3-117">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="974c3-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="974c3-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/endpoints
```
## <a name="optional-query-parameters"></a><span data-ttu-id="974c3-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="974c3-119">Optional query parameters</span></span>
<span data-ttu-id="974c3-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="974c3-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="974c3-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="974c3-121">Request headers</span></span>
| <span data-ttu-id="974c3-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="974c3-122">Name</span></span>      |<span data-ttu-id="974c3-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="974c3-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="974c3-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="974c3-124">Authorization</span></span>  | <span data-ttu-id="974c3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="974c3-p103">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="974c3-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="974c3-127">Content-Type</span></span>   | <span data-ttu-id="974c3-128">Application/Json</span><span class="sxs-lookup"><span data-stu-id="974c3-128">Application/Json</span></span> |

## <a name="request-body"></a><span data-ttu-id="974c3-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="974c3-129">Request body</span></span>
<span data-ttu-id="974c3-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="974c3-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="974c3-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="974c3-131">Response</span></span>

<span data-ttu-id="974c3-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [extremo](../resources/endpoint.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="974c3-132">If successful, this method returns a `200 OK` response code and collection of [Endpoint](../resources/endpoint.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="974c3-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="974c3-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="974c3-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="974c3-134">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_endpoints"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/endpoints
```
##### <a name="response"></a><span data-ttu-id="974c3-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="974c3-135">Response</span></span>
<span data-ttu-id="974c3-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="974c3-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.Endpoint",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 261

{
  "value": [
    {
      "capability": "Conversations",
      "providerId": "{Yammer GUID}",
      "providerName": "Yammer",
      "uri": "uri-value",
      "providerResourceId": "Yammer.FeedURL",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List endpoints",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->