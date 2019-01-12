---
title: Obtener identityRiskEvent
description: Recuperar las propiedades y relaciones del objeto identityriskevent.
author: cloudhandler
localization_priority: Normal
ms.prod: security
ms.openlocfilehash: 6b66352010a3f1455dd2598215039c24a2dc819e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27935601"
---
# <a name="get-identityriskevent"></a><span data-ttu-id="f5728-103">Obtener identityRiskEvent</span><span class="sxs-lookup"><span data-stu-id="f5728-103">Get identityRiskEvent</span></span>

> <span data-ttu-id="f5728-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f5728-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f5728-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f5728-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f5728-106">Recuperar las propiedades y relaciones del objeto identityriskevent.</span><span class="sxs-lookup"><span data-stu-id="f5728-106">Retrieve the properties and relationships of identityriskevent object.</span></span>
## <a name="permissions"></a><span data-ttu-id="f5728-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f5728-107">Permissions</span></span>
<span data-ttu-id="f5728-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f5728-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f5728-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f5728-110">Permission type</span></span>      | <span data-ttu-id="f5728-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f5728-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f5728-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f5728-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f5728-113">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="f5728-113">IdentityRiskEvent.Read.All</span></span>    |
|<span data-ttu-id="f5728-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f5728-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f5728-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f5728-115">Not supported.</span></span>    |
|<span data-ttu-id="f5728-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f5728-116">Application</span></span> | <span data-ttu-id="f5728-117">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="f5728-117">IdentityRiskEvent.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f5728-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f5728-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /identityRiskEvents/{id}
```
## <a name="request-headers"></a><span data-ttu-id="f5728-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f5728-119">Request headers</span></span>
| <span data-ttu-id="f5728-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="f5728-120">Name</span></span>      |<span data-ttu-id="f5728-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5728-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f5728-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="f5728-122">Authorization</span></span>  | <span data-ttu-id="f5728-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f5728-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f5728-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f5728-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="f5728-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="f5728-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f5728-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f5728-128">Request body</span></span>
<span data-ttu-id="f5728-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f5728-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f5728-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5728-130">Response</span></span>

<span data-ttu-id="f5728-131">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [identityRiskEvent](../resources/identityriskevent.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5728-131">If successful, this method returns a `200 OK` response code and [identityRiskEvent](../resources/identityriskevent.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f5728-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5728-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f5728-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f5728-133">Request</span></span>
<span data-ttu-id="f5728-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f5728-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_identityriskevent"
}-->
```http
GET https://graph.microsoft.com/beta/identityRiskEvents/ec50e9fb-9da1-215b-e18c-b7e2a716b2a6-c2b6c2b9-dddc-acd0-2b39-d519d803dbc3-db69711e-9324-ec99-f010-6e63fb972e98
```
##### <a name="response"></a><span data-ttu-id="f5728-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5728-135">Response</span></span>
<span data-ttu-id="f5728-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f5728-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.identityRiskEvent"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 251

{
  "@odata.type": "#microsoft.graph.unfamiliarLocationRiskEvent",
  "closedDateTime": "2016-01-29T20:03:57.7872426Z",
  "createdDateTime": "2016-01-29T00:01:49.126468Z",
  "id": "ec50e9fb-9da1-215b-e18c-b7e2a716b2a6-c2b6c2b9-dddc-acd0-2b39-d519d803dbc3-db69711e-9324-ec99-f010-6e63fb972e98",
  "ipAddress": "176.10.104.240",
  "location": "Bern, CH",
  "riskEventDateTime": "2016-01-29T00:00:56.2255665Z",
  "riskEventStatus": "remediated",
  "riskLevel": "medium",
  "riskType": "UnfamiliarLocationRiskEvent",
  "userDisplayName": "Jon Doe",
  "userId": "c2b6c2b9-dddc-acd0-2b39-d519d803dbc3",
  "userPrincipalName": "jon@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get identityRiskEvent",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
