---
title: Obtener unfamiliarLocationRiskEvent
description: Recuperar las propiedades y relaciones de un objeto unfamiliarlocationriskevent.
ms.openlocfilehash: e75399b79b8f3535741549ce49f5cfcb5ee40077
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091172"
---
# <a name="get-unfamiliarlocationriskevent"></a><span data-ttu-id="37f27-103">Obtener unfamiliarLocationRiskEvent</span><span class="sxs-lookup"><span data-stu-id="37f27-103">Get unfamiliarLocationRiskEvent</span></span>

> <span data-ttu-id="37f27-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="37f27-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="37f27-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="37f27-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="37f27-106">Recuperar las propiedades y relaciones de un objeto unfamiliarlocationriskevent.</span><span class="sxs-lookup"><span data-stu-id="37f27-106">Retrieve the properties and relationships of an unfamiliarlocationriskevent object.</span></span>
## <a name="permissions"></a><span data-ttu-id="37f27-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="37f27-107">Permissions</span></span>
<span data-ttu-id="37f27-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="37f27-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="37f27-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="37f27-110">Permission type</span></span>      | <span data-ttu-id="37f27-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="37f27-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="37f27-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="37f27-112">Delegated (work or school account)</span></span> | <span data-ttu-id="37f27-113">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="37f27-113">IdentityRiskEvent.Read.All</span></span>    |
|<span data-ttu-id="37f27-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="37f27-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="37f27-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37f27-115">Not supported.</span></span>    |
|<span data-ttu-id="37f27-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="37f27-116">Application</span></span> | <span data-ttu-id="37f27-117">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="37f27-117">IdentityRiskEvent.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="37f27-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="37f27-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /unfamiliarLocationRiskEvents/{id}
```
## <a name="request-headers"></a><span data-ttu-id="37f27-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="37f27-119">Request headers</span></span>
| <span data-ttu-id="37f27-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="37f27-120">Name</span></span>      |<span data-ttu-id="37f27-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="37f27-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="37f27-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="37f27-122">Authorization</span></span>  | <span data-ttu-id="37f27-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="37f27-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="37f27-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="37f27-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="37f27-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="37f27-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="37f27-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="37f27-128">Request body</span></span>
<span data-ttu-id="37f27-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="37f27-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="37f27-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37f27-130">Response</span></span>

<span data-ttu-id="37f27-131">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [unfamiliarLocationRiskEvent](../resources/unfamiliarlocationriskevent.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37f27-131">If successful, this method returns a `200 OK` response code and [unfamiliarLocationRiskEvent](../resources/unfamiliarlocationriskevent.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="37f27-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37f27-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="37f27-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="37f27-133">Request</span></span>
<span data-ttu-id="37f27-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="37f27-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_unfamiliarlocationriskevent"
}-->
```http
GET https://graph.microsoft.com/v1.0/unfamiliarLocationRiskEvents/700b6476-8138-4c14-4962-c43614958301-8dce9c6b-21f1-2e3b-2c3b-5164f751e7ad-4e5591fd-2ac1-4e9d-96a9-aca8339e2604
```
##### <a name="response"></a><span data-ttu-id="37f27-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37f27-135">Response</span></span>
<span data-ttu-id="37f27-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="37f27-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.unfamiliarLocationRiskEvent"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 237

{
  "closedDateTime": "2016-01-29T20:03:57.7872426Z",
  "createdDateTime": "2016-01-29T00:01:49.126468Z",
  "id": "700b6476-8138-4c14-4962-c43614958301-8dce9c6b-21f1-2e3b-2c3b-5164f751e7ad-4e5591fd-2ac1-4e9d-96a9-aca8339e2604",
  "ipAddress": "176.10.104.240",
  "location": "Bern, CH",
  "riskEventDateTime": "2016-01-29T00:00:56.2255665Z",
  "riskEventStatus": "remediated",
  "riskLevel": "medium",
  "riskType": "UnfamiliarLocationRiskEvent",
  "userDisplayName": "Jon Doe",
  "userId": "8dce9c6b-21f1-2e3b-2c3b-5164f751e7ad",
  "userPrincipalName": "jon@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get unfamiliarLocationRiskEvent",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
