---
title: Obtener el extremo
description: Recuperar las propiedades y relaciones de un objeto específica del extremo.
localization_priority: Normal
ms.openlocfilehash: 77ad5716e8e30a16f95bf62593a6530d5e759861
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820450"
---
# <a name="get-endpoint"></a><span data-ttu-id="66486-103">Obtener el extremo</span><span class="sxs-lookup"><span data-stu-id="66486-103">Get endpoint</span></span>

> <span data-ttu-id="66486-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="66486-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="66486-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="66486-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="66486-106">Recuperar las propiedades y relaciones de un objeto específica del [extremo](../resources/endpoint.md) .</span><span class="sxs-lookup"><span data-stu-id="66486-106">Retrieve the properties and relationships of a specific [endpoint](../resources/endpoint.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="66486-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="66486-107">Permissions</span></span>
<span data-ttu-id="66486-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="66486-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="66486-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="66486-110">Permission type</span></span>      | <span data-ttu-id="66486-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="66486-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="66486-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="66486-112">Delegated (work or school account)</span></span> | <span data-ttu-id="66486-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="66486-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="66486-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="66486-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="66486-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="66486-115">Not supported.</span></span>    |
|<span data-ttu-id="66486-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="66486-116">Application</span></span> | <span data-ttu-id="66486-117">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="66486-117">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="66486-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="66486-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/endpoints/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="66486-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="66486-119">Optional query parameters</span></span>
<span data-ttu-id="66486-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66486-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="66486-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="66486-121">Request headers</span></span>
| <span data-ttu-id="66486-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="66486-122">Name</span></span>      |<span data-ttu-id="66486-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="66486-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="66486-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="66486-124">Authorization</span></span>  | <span data-ttu-id="66486-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="66486-p103">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="66486-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="66486-127">Content-Type</span></span>   | <span data-ttu-id="66486-128">Application/Json</span><span class="sxs-lookup"><span data-stu-id="66486-128">Application/Json</span></span> |

## <a name="request-body"></a><span data-ttu-id="66486-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="66486-129">Request body</span></span>
<span data-ttu-id="66486-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="66486-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="66486-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66486-131">Response</span></span>

<span data-ttu-id="66486-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto de [extremo](../resources/endpoint.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66486-132">If successful, this method returns a `200 OK` response code and [Endpoint](../resources/endpoint.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="66486-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66486-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="66486-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="66486-134">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_endpoint"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/endpoints/{id}
```
##### <a name="response"></a><span data-ttu-id="66486-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66486-135">Response</span></span>
<span data-ttu-id="66486-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="66486-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.Endpoint"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 208

{
  "capability": "Conversations",
  "providerId": "{Yammer GUID}",
  "providerName": "Yammer",
  "uri": "uri-value",
  "providerResourceId": "Yammer.FeedURL",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get Endpoint",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
