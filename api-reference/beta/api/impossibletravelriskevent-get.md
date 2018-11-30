---
title: Obtener impossibleTravelRiskEvent
description: Recuperar las propiedades y relaciones de un objeto impossibletravelriskevent.
ms.openlocfilehash: 3bb5b052cca79e90c26e7e26f2b9cb798e97680f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086162"
---
# <a name="get-impossibletravelriskevent"></a><span data-ttu-id="83f05-103">Obtener impossibleTravelRiskEvent</span><span class="sxs-lookup"><span data-stu-id="83f05-103">Get impossibleTravelRiskEvent</span></span>

> <span data-ttu-id="83f05-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="83f05-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="83f05-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="83f05-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="83f05-106">Recuperar las propiedades y relaciones de un objeto impossibletravelriskevent.</span><span class="sxs-lookup"><span data-stu-id="83f05-106">Retrieve the properties and relationships of an impossibletravelriskevent object.</span></span>
## <a name="permissions"></a><span data-ttu-id="83f05-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="83f05-107">Permissions</span></span>
<span data-ttu-id="83f05-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="83f05-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="83f05-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="83f05-110">Permission type</span></span>      | <span data-ttu-id="83f05-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="83f05-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="83f05-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="83f05-112">Delegated (work or school account)</span></span> | <span data-ttu-id="83f05-113">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="83f05-113">IdentityRiskEvent.Read.All</span></span>    |
|<span data-ttu-id="83f05-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="83f05-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="83f05-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="83f05-115">Not supported.</span></span>    |
|<span data-ttu-id="83f05-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="83f05-116">Application</span></span> | <span data-ttu-id="83f05-117">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="83f05-117">IdentityRiskEvent.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="83f05-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="83f05-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /impossibleTravelRiskEvents/{id}
```
## <a name="request-headers"></a><span data-ttu-id="83f05-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="83f05-119">Request headers</span></span>
| <span data-ttu-id="83f05-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="83f05-120">Name</span></span>      |<span data-ttu-id="83f05-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="83f05-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="83f05-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="83f05-122">Authorization</span></span>  | <span data-ttu-id="83f05-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="83f05-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="83f05-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="83f05-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="83f05-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="83f05-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="83f05-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="83f05-128">Request body</span></span>
<span data-ttu-id="83f05-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="83f05-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="83f05-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="83f05-130">Response</span></span>

<span data-ttu-id="83f05-131">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [impossibleTravelRiskEvent](../resources/impossibletravelriskevent.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="83f05-131">If successful, this method returns a `200 OK` response code and [impossibleTravelRiskEvent](../resources/impossibletravelriskevent.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="83f05-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="83f05-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="83f05-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="83f05-133">Request</span></span>
<span data-ttu-id="83f05-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="83f05-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_impossibletravelriskevent"
}-->
```http
GET https://graph.microsoft.com/v1.0/impossibleTravelRiskEvents/22e65c1f-909a-42b5-c0d2-075f30e27887-0bfdc7a8-6a16-c33e-7de9-a60a28ae533b-15475553-dbc1-8879-5079-23b1edd25bab
```
##### <a name="response"></a><span data-ttu-id="83f05-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="83f05-135">Response</span></span>
<span data-ttu-id="83f05-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="83f05-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.impossibleTravelRiskEvent"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 260

{
  "@odata.type": "#microsoft.graph.impossibleTravelRiskEvent",
  "closedDateTime": "2016-01-29T20:03:57.7872426Z",
  "createdDateTime": "2016-01-29T00:01:49.126468Z",
  "id": "22e65c1f-909a-42b5-c0d2-075f30e27887-0bfdc7a8-6a16-c33e-7de9-a60a28ae533b-15475553-dbc1-8879-5079-23b1edd25bab",
  "ipAddress": "176.10.104.240",
  "isAtypicalLocation": true,
  "location": "Bern, CH",
  "previousIPAddress": "95.31.18.119",
  "previousLocation": "Moskva, Russia, RU",
  "previousSigninDateTime": "2016-01-29T00:00:55.3859274Z",
  "riskEventDateTime": "2016-01-29T00:00:56.2255665Z",
  "riskEventStatus": "remediated",
  "riskLevel": "medium",
  "riskType": "ImpossibleTravelRiskEvent",
  "userAgent": "Firefox 42.0.0.1",
  "userDisplayName": "Jon Doe",
  "userId": "0bfdc7a8-6a16-c33e-7de9-a60a28ae533b",
  "userPrincipalName": "jon@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get impossibleTravelRiskEvent",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
