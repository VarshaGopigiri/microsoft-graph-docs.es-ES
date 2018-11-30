---
title: Lista suspiciousIpRiskEvents
description: Recuperar una lista de objetos de suspiciousipriskevent.
ms.openlocfilehash: fe6d14b4f1c7fc1d65b6293de156a63ed2bd15a4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090639"
---
# <a name="list-suspiciousipriskevents"></a><span data-ttu-id="d3c59-103">Lista suspiciousIpRiskEvents</span><span class="sxs-lookup"><span data-stu-id="d3c59-103">List suspiciousIpRiskEvents</span></span>

> <span data-ttu-id="d3c59-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d3c59-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d3c59-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d3c59-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d3c59-106">Recuperar una lista de objetos de suspiciousipriskevent.</span><span class="sxs-lookup"><span data-stu-id="d3c59-106">Retrieve a list of suspiciousipriskevent objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="d3c59-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d3c59-107">Permissions</span></span>
<span data-ttu-id="d3c59-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d3c59-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d3c59-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d3c59-110">Permission type</span></span>      | <span data-ttu-id="d3c59-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d3c59-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d3c59-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d3c59-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d3c59-113">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="d3c59-113">IdentityRiskEvent.Read.All</span></span>    |
|<span data-ttu-id="d3c59-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d3c59-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d3c59-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d3c59-115">Not supported.</span></span>    |
|<span data-ttu-id="d3c59-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d3c59-116">Application</span></span> | <span data-ttu-id="d3c59-117">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="d3c59-117">IdentityRiskEvent.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d3c59-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d3c59-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /suspiciousIpRiskEvents
```
## <a name="request-headers"></a><span data-ttu-id="d3c59-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d3c59-119">Request headers</span></span>
| <span data-ttu-id="d3c59-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d3c59-120">Name</span></span>      |<span data-ttu-id="d3c59-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3c59-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="d3c59-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="d3c59-122">Authorization</span></span>  | <span data-ttu-id="d3c59-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d3c59-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d3c59-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d3c59-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="d3c59-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d3c59-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d3c59-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d3c59-128">Request body</span></span>
<span data-ttu-id="d3c59-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d3c59-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d3c59-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d3c59-130">Response</span></span>

<span data-ttu-id="d3c59-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [suspiciousIpRiskEvent](../resources/suspiciousipriskevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d3c59-131">If successful, this method returns a `200 OK` response code and collection of [suspiciousIpRiskEvent](../resources/suspiciousipriskevent.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d3c59-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d3c59-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d3c59-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d3c59-133">Request</span></span>
<span data-ttu-id="d3c59-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d3c59-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_suspiciousipriskevents"
}-->
```http
GET https://graph.microsoft.com/v1.0/suspiciousIpRiskEvents
```
##### <a name="response"></a><span data-ttu-id="d3c59-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d3c59-135">Response</span></span>
<span data-ttu-id="d3c59-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d3c59-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.suspiciousIpRiskEvent",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 290

{
  "value": [
    {
      "closedDateTime": null,
      "createdDateTime": "2016-02-03T06:08:35.123512Z",
      "id": "02e8bfd1-5231-1006-01cc-434f84e0859e-97b7301f-bc05-8e2c-fdfa-2004eb66ff70-287e7b9b-1d60-aa96-6ddb-65c81ee31475",
      "ipAddress": "95.31.18.119",
      "location": "Moskva, Russia, RU",
      "riskEventDateTime": "2016-02-03T05:33:49.9516789Z",
      "riskEventStatus": "active",
      "riskLevel": "low",
      "riskType": "SuspiciousIpRiskEvent",
      "userDisplayName": "Jon Doe",
      "userId": "97b7301f-bc05-8e2c-fdfa-2004eb66ff70",
      "userPrincipalName": "jon@contoso.com"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List suspiciousIpRiskEvents",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
