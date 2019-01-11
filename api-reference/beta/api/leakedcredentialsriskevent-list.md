---
title: Lista leakedCredentialsRiskEvents
description: Recuperar una lista de objetos de leakedcredentialsriskevent.
localization_priority: Normal
ms.openlocfilehash: 695499c2db07f108e1f7dd762a97ce95629cca42
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857438"
---
# <a name="list-leakedcredentialsriskevents"></a><span data-ttu-id="f9feb-103">Lista leakedCredentialsRiskEvents</span><span class="sxs-lookup"><span data-stu-id="f9feb-103">List leakedCredentialsRiskEvents</span></span>

> <span data-ttu-id="f9feb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f9feb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f9feb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f9feb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f9feb-106">Recuperar una lista de objetos de leakedcredentialsriskevent.</span><span class="sxs-lookup"><span data-stu-id="f9feb-106">Retrieve a list of leakedcredentialsriskevent objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="f9feb-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f9feb-107">Permissions</span></span>
<span data-ttu-id="f9feb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f9feb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f9feb-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f9feb-110">Permission type</span></span>      | <span data-ttu-id="f9feb-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f9feb-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f9feb-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f9feb-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f9feb-113">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="f9feb-113">IdentityRiskEvent.Read.All</span></span>    |
|<span data-ttu-id="f9feb-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f9feb-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f9feb-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9feb-115">Not supported.</span></span>    |
|<span data-ttu-id="f9feb-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f9feb-116">Application</span></span> | <span data-ttu-id="f9feb-117">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="f9feb-117">IdentityRiskEvent.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f9feb-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9feb-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /leakedCredentialsRiskEvents
```
## <a name="request-headers"></a><span data-ttu-id="f9feb-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9feb-119">Request headers</span></span>
| <span data-ttu-id="f9feb-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="f9feb-120">Name</span></span>      |<span data-ttu-id="f9feb-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9feb-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f9feb-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="f9feb-122">Authorization</span></span>  | <span data-ttu-id="f9feb-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f9feb-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f9feb-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f9feb-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="f9feb-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="f9feb-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f9feb-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9feb-128">Request body</span></span>
<span data-ttu-id="f9feb-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f9feb-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f9feb-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9feb-130">Response</span></span>

<span data-ttu-id="f9feb-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [leakedCredentialsRiskEvent](../resources/leakedcredentialsriskevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9feb-131">If successful, this method returns a `200 OK` response code and collection of [leakedCredentialsRiskEvent](../resources/leakedcredentialsriskevent.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f9feb-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9feb-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f9feb-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9feb-133">Request</span></span>
<span data-ttu-id="f9feb-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f9feb-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_leakedcredentialsriskevents"
}-->
```http
GET https://graph.microsoft.com/v1.0/leakedCredentialsRiskEvents
```
##### <a name="response"></a><span data-ttu-id="f9feb-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9feb-135">Response</span></span>
<span data-ttu-id="f9feb-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f9feb-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.leakedCredentialsRiskEvent",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 304

{
  "value":
  [
    {
      "closedDateTime": null,
      "createdDateTime": "2016-01-29T00:01:49.126468Z",
      "id": "8c793a18-c86a-b5f9-7d9a-b3d024f33eee-278dc452-4163-dbc6-84eb-a050c37fc931-1a01abd3-b87a-cece-3f4d-c788b055c182",
      "riskEventDateTime": "2016-01-29T00:00:56.2255665Z",
      "riskEventStatus": "active",
      "riskLevel": "high",
      "riskType": "LeakedCredentialsRiskEvent",
      "userDisplayName": "Jon Doe",
      "userId": "278dc452-4163-dbc6-84eb-a050c37fc931",
      "userPrincipalName": "jon@contoso.com"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List leakedCredentialsRiskEvents",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
