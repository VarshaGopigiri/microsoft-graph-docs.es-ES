---
title: Lista identityRiskEvents
description: Recuperar una lista de objetos de identityriskevent.
author: cloudhandler
localization_priority: Normal
ms.openlocfilehash: fbd5e739986ded9fa6f5346e35808f4018bff625
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894253"
---
# <a name="list-identityriskevents"></a><span data-ttu-id="0a9b0-103">Lista identityRiskEvents</span><span class="sxs-lookup"><span data-stu-id="0a9b0-103">List identityRiskEvents</span></span>

> <span data-ttu-id="0a9b0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0a9b0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0a9b0-106">Recuperar una lista de objetos de identityriskevent.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-106">Retrieve a list of identityriskevent objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="0a9b0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0a9b0-107">Permissions</span></span>
<span data-ttu-id="0a9b0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0a9b0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0a9b0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0a9b0-110">Permission type</span></span>      | <span data-ttu-id="0a9b0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0a9b0-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0a9b0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0a9b0-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0a9b0-113">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="0a9b0-113">IdentityRiskEvent.Read.All</span></span>    |
|<span data-ttu-id="0a9b0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0a9b0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0a9b0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-115">Not supported.</span></span>    |
|<span data-ttu-id="0a9b0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0a9b0-116">Application</span></span> | <span data-ttu-id="0a9b0-117">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="0a9b0-117">IdentityRiskEvent.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0a9b0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0a9b0-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /identityRiskEvents
```
## <a name="request-headers"></a><span data-ttu-id="0a9b0-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0a9b0-119">Request headers</span></span>
| <span data-ttu-id="0a9b0-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="0a9b0-120">Name</span></span>      |<span data-ttu-id="0a9b0-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a9b0-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="0a9b0-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="0a9b0-122">Authorization</span></span>  | <span data-ttu-id="0a9b0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0a9b0-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="0a9b0-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="0a9b0-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="0a9b0-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0a9b0-128">Request body</span></span>
<span data-ttu-id="0a9b0-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0a9b0-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a9b0-130">Response</span></span>

<span data-ttu-id="0a9b0-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [identityRiskEvent](../resources/identityriskevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-131">If successful, this method returns a `200 OK` response code and collection of [identityRiskEvent](../resources/identityriskevent.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0a9b0-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a9b0-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0a9b0-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0a9b0-133">Request</span></span>
<span data-ttu-id="0a9b0-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_identityriskevents"
}-->
```http
GET https://graph.microsoft.com/v1.0/identityRiskEvents
```
##### <a name="response"></a><span data-ttu-id="0a9b0-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a9b0-135">Response</span></span>
<span data-ttu-id="0a9b0-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.identityRiskEvent",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 304

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.malwareRiskEvent",
      "malwareName": "CONFICKER",
      "closedDateTime": null,
      "createdDateTime": "2016-02-03T06:06:01.940814Z",
      "deviceInformation": "B62XYZ13OX",
      "id": "74ceb0af-2271-9167-ffa0-b6ac3b4e8781-9eaaa2e3-4681-ae31-1eb6-7e46ae11ac89-0fdc2304-ba4c-ac0c-bdd7-da2d10e93849",
      "ipAddress": "95.31.18.119",
      "location": "Moskva, Russia, RU",
      "riskEventDateTime": "2016-02-03T05:20:33.7208156Z",
      "riskEventStatus": "active",
      "riskLevel": "low",
      "riskType": "MalwareRiskEvent",
      "userDisplayName": "Jon Doe",
      "userId": "9eaaa2e3-4681-ae31-1eb6-7e46ae11ac89",
      "userPrincipalName": "jon@contoso.com"
    },
    {
      "@odata.type": "#microsoft.graph.unfamiliarLocationRiskEvent",
      "closedDateTime": "2016-01-29T20:03:57.7872426Z",
      "createdDateTime": "2016-01-29T00:01:49.126468Z",
      "id": "ec50e9fb-9da1-215b-e18c-b7e2a716b2a6-9eaaa2e3-4681-ae31-1eb6-7e46ae11ac89-db69711e-9324-ec99-f010-6e63fb972e98",
      "ipAddress": "176.10.104.240",
      "location": "Bern, CH",
      "riskEventDateTime": "2016-01-29T00:00:56.2255665Z",
      "riskEventStatus": "remediated",
      "riskLevel": "medium",
      "riskType": "UnfamiliarLocationRiskEvent",
      "userDisplayName": "Jon Doe",
      "userId": "9eaaa2e3-4681-ae31-1eb6-7e46ae11ac89",
      "userPrincipalName": "jon@contoso.com"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List identityRiskEvents",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
