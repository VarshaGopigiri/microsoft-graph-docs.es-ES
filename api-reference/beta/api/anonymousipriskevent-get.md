---
title: Obtener anonymousIpRiskEvent
description: Recuperar las propiedades y relaciones de un objeto anonymousipriskevent.
ms.openlocfilehash: 0dbc53f53ed029939cc02454041b63e6360d83c6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084651"
---
# <a name="get-anonymousipriskevent"></a><span data-ttu-id="5151c-103">Obtener anonymousIpRiskEvent</span><span class="sxs-lookup"><span data-stu-id="5151c-103">Get anonymousIpRiskEvent</span></span>

> <span data-ttu-id="5151c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5151c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5151c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5151c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5151c-106">Recuperar las propiedades y relaciones de un objeto anonymousipriskevent.</span><span class="sxs-lookup"><span data-stu-id="5151c-106">Retrieve the properties and relationships of an anonymousipriskevent object.</span></span>
## <a name="permissions"></a><span data-ttu-id="5151c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5151c-107">Permissions</span></span>
<span data-ttu-id="5151c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5151c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5151c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5151c-110">Permission type</span></span>      | <span data-ttu-id="5151c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5151c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5151c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5151c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5151c-113">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="5151c-113">IdentityRiskEvent.Read.All</span></span>    |
|<span data-ttu-id="5151c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5151c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5151c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5151c-115">Not supported.</span></span>    |
|<span data-ttu-id="5151c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5151c-116">Application</span></span> | <span data-ttu-id="5151c-117">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="5151c-117">IdentityRiskEvent.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5151c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5151c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /anonymousIpRiskEvents/{id}
```

## <a name="request-headers"></a><span data-ttu-id="5151c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5151c-119">Request headers</span></span>
| <span data-ttu-id="5151c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="5151c-120">Name</span></span>      |<span data-ttu-id="5151c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="5151c-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="5151c-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="5151c-122">Authorization</span></span>  | <span data-ttu-id="5151c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5151c-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5151c-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="5151c-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="5151c-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="5151c-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="5151c-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5151c-128">Request body</span></span>
<span data-ttu-id="5151c-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5151c-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5151c-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5151c-130">Response</span></span>

<span data-ttu-id="5151c-131">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [anonymousIpRiskEvent](../resources/anonymousipriskevent.md) de respuesta en el valor del cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5151c-131">If successful, this method returns a `200 OK` response code and [anonymousIpRiskEvent](../resources/anonymousipriskevent.md) object in the value of response body.</span></span>
## <a name="example"></a><span data-ttu-id="5151c-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5151c-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5151c-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5151c-133">Request</span></span>
<span data-ttu-id="5151c-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5151c-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_anonymousipriskevent"
}-->
```http
GET https://graph.microsoft.com/v1.0/anonymousIpRiskEvents/2016-01-29T00:00:56.22556656a56d0b2-3c51-7c5e-bc1a-1ccdb3bd9c71
```
##### <a name="response"></a><span data-ttu-id="5151c-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5151c-135">Response</span></span>
<span data-ttu-id="5151c-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5151c-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.anonymousIpRiskEvent"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 237

{
  "closedDateTime": "2016-01-29T20:03:57.7872426Z",
  "createdDateTime": "2016-01-29T00:01:49.126468Z",
  "id": "2016-01-29T00:00:56.22556656a56d0b2-3c51-7c5e-bc1a-1ccdb3bd9c71",
  "ipAddress": null,
  "location": null,
  "riskEventDateTime": "2016-01-29T00:00:56.2255665Z",
  "riskEventStatus": "remediated",
  "riskLevel": "medium",
  "riskType": "AnonymousIpRiskEvent",
  "userDisplayName": "Jon Doe",
  "userId": "6a56d0b2-3c51-7c5e-bc1a-1ccdb3bd9c71",
  "userPrincipalName": "jon@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get anonymousIpRiskEvent",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
