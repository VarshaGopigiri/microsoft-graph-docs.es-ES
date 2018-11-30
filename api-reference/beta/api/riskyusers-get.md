---
title: Obtener riskyUsers
description: Recuperar las propiedades y relaciones de un objeto **riskyUsers** .
ms.openlocfilehash: f0a6ac24bf66184d0547e9284f5a35b84b9358b4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084134"
---
# <a name="get-riskyusers"></a><span data-ttu-id="c899d-103">Obtener riskyUsers</span><span class="sxs-lookup"><span data-stu-id="c899d-103">Get riskyUsers</span></span>

> <span data-ttu-id="c899d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c899d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c899d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c899d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c899d-106">Recuperar las propiedades y relaciones de un objeto **riskyUsers** .</span><span class="sxs-lookup"><span data-stu-id="c899d-106">Retrieve the properties and relationships of a **riskyUsers** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="c899d-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c899d-107">Permissions</span></span>
<span data-ttu-id="c899d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c899d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c899d-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c899d-110">Permission type</span></span>      | <span data-ttu-id="c899d-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c899d-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c899d-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c899d-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c899d-113">IdentityrRskyUser.Read.All</span><span class="sxs-lookup"><span data-stu-id="c899d-113">IdentityrRskyUser.Read.All</span></span>    |
|<span data-ttu-id="c899d-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c899d-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c899d-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c899d-115">Not supported.</span></span>    |
|<span data-ttu-id="c899d-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c899d-116">Application</span></span> | <span data-ttu-id="c899d-117">IdentityRiskyUser.Read.All</span><span class="sxs-lookup"><span data-stu-id="c899d-117">IdentityRiskyUser.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c899d-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c899d-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /riskyUsers/{query}
```


## <a name="request-headers"></a><span data-ttu-id="c899d-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c899d-119">Request headers</span></span>
| <span data-ttu-id="c899d-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c899d-120">Name</span></span>      |<span data-ttu-id="c899d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c899d-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c899d-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c899d-122">Authorization</span></span>  | <span data-ttu-id="c899d-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c899d-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c899d-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c899d-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="c899d-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c899d-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c899d-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c899d-128">Request body</span></span>
<span data-ttu-id="c899d-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c899d-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c899d-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c899d-130">Response</span></span>

<span data-ttu-id="c899d-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [riskyUser](../resources/riskyuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c899d-131">If successful, this method returns a `200 OK` response code and a [riskyUser](../resources/riskyuser.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c899d-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c899d-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c899d-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c899d-133">Request</span></span>
<span data-ttu-id="c899d-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c899d-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_identityriskevent"
}-->
```http
GET https://graph.microsoft.com/beta/riskyUsers/{id}
```
##### <a name="response"></a><span data-ttu-id="c899d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c899d-135">Response</span></span>
<span data-ttu-id="c899d-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c899d-136">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.riskyUsers"
} -->
```http
HTTP/1.1 200 OK
{
  "id": "c2b6c2b9-dddc-acd0-2b39-d519d803dbc3",
  "riskLastUpdatedDateTime": "2016-01-29T20:03:57.7872426Z",
  "isGuest": "true",
  "isDeleted": "true",
  "riskDetail": "adminConfirmedSigninCompromised",
  "riskLevel": "high",
  "riskState": "atRisk"
  "userDisplayName": "Jon Doe",
  "userPrincipalName": "jon@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get riskyUsers",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
