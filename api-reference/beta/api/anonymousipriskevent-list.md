---
title: Lista anonymousIpRiskEvents
description: Recuperar una lista de objetos de anonymousipriskevent.
ms.openlocfilehash: aa5845d37f36dd59727083650c1737ecedc46187
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084083"
---
# <a name="list-anonymousipriskevents"></a><span data-ttu-id="dca22-103">Lista anonymousIpRiskEvents</span><span class="sxs-lookup"><span data-stu-id="dca22-103">List anonymousIpRiskEvents</span></span>

> <span data-ttu-id="dca22-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dca22-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dca22-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dca22-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dca22-106">Recuperar una lista de objetos de anonymousipriskevent.</span><span class="sxs-lookup"><span data-stu-id="dca22-106">Retrieve a list of anonymousipriskevent objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="dca22-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="dca22-107">Permissions</span></span>
<span data-ttu-id="dca22-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dca22-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dca22-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dca22-110">Permission type</span></span>      | <span data-ttu-id="dca22-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dca22-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dca22-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dca22-112">Delegated (work or school account)</span></span> | <span data-ttu-id="dca22-113">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="dca22-113">IdentityRiskEvent.Read.All</span></span>    |
|<span data-ttu-id="dca22-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dca22-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dca22-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dca22-115">Not supported.</span></span>    |
|<span data-ttu-id="dca22-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dca22-116">Application</span></span> | <span data-ttu-id="dca22-117">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="dca22-117">IdentityRiskEvent.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="dca22-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dca22-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /anonymousIpRiskEvents
```

## <a name="request-headers"></a><span data-ttu-id="dca22-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dca22-119">Request headers</span></span>
| <span data-ttu-id="dca22-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="dca22-120">Name</span></span>      |<span data-ttu-id="dca22-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="dca22-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="dca22-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="dca22-122">Authorization</span></span>  | <span data-ttu-id="dca22-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dca22-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="dca22-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="dca22-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="dca22-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="dca22-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="dca22-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dca22-128">Request body</span></span>
<span data-ttu-id="dca22-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dca22-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dca22-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dca22-130">Response</span></span>

<span data-ttu-id="dca22-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [anonymousIpRiskEvent](../resources/anonymousipriskevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dca22-131">If successful, this method returns a `200 OK` response code and collection of [anonymousIpRiskEvent](../resources/anonymousipriskevent.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="dca22-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dca22-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dca22-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dca22-133">Request</span></span>
<span data-ttu-id="dca22-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dca22-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_anonymousipriskevents"
}-->
```http
GET https://graph.microsoft.com/v1.0/anonymousIpRiskEvents
```
##### <a name="response"></a><span data-ttu-id="dca22-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dca22-135">Response</span></span>
<span data-ttu-id="dca22-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dca22-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.anonymousIpRiskEvent",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 290

{
  "value": [
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List anonymousIpRiskEvents",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
