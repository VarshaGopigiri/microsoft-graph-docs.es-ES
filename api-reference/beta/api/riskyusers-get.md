---
title: Obtener riskyUsers
description: Recuperar las propiedades y relaciones de un objeto **riskyUsers** .
ms.openlocfilehash: 7212e99e53d990df9cd9fea7dae754a693edc745
ms.sourcegitcommit: 12c6e82f1417022540e534ebadbd0e8d7fb5abde
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/08/2018
ms.locfileid: "27209687"
---
# <a name="get-riskyusers"></a><span data-ttu-id="501e2-103">Obtener riskyUsers</span><span class="sxs-lookup"><span data-stu-id="501e2-103">Get riskyUsers</span></span>

> <span data-ttu-id="501e2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="501e2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="501e2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="501e2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="501e2-106">Recuperar las propiedades y relaciones de un objeto **riskyUsers** .</span><span class="sxs-lookup"><span data-stu-id="501e2-106">Retrieve the properties and relationships of a **riskyUsers** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="501e2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="501e2-107">Permissions</span></span>
<span data-ttu-id="501e2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="501e2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="501e2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="501e2-110">Permission type</span></span>      | <span data-ttu-id="501e2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="501e2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="501e2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="501e2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="501e2-113">IdentityRiskyUser.Read.All</span><span class="sxs-lookup"><span data-stu-id="501e2-113">IdentityRiskyUser.Read.All</span></span>    |
|<span data-ttu-id="501e2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="501e2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="501e2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="501e2-115">Not supported.</span></span>    |
|<span data-ttu-id="501e2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="501e2-116">Application</span></span> | <span data-ttu-id="501e2-117">IdentityRiskyUser.Read.All</span><span class="sxs-lookup"><span data-stu-id="501e2-117">IdentityRiskyUser.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="501e2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="501e2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /riskyUsers/{query}
```


## <a name="request-headers"></a><span data-ttu-id="501e2-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="501e2-119">Request headers</span></span>
| <span data-ttu-id="501e2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="501e2-120">Name</span></span>      |<span data-ttu-id="501e2-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="501e2-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="501e2-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="501e2-122">Authorization</span></span>  | <span data-ttu-id="501e2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="501e2-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="501e2-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="501e2-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="501e2-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="501e2-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="501e2-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="501e2-128">Request body</span></span>
<span data-ttu-id="501e2-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="501e2-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="501e2-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="501e2-130">Response</span></span>

<span data-ttu-id="501e2-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [riskyUser](../resources/riskyuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="501e2-131">If successful, this method returns a `200 OK` response code and a [riskyUser](../resources/riskyuser.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="501e2-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="501e2-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="501e2-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="501e2-133">Request</span></span>
<span data-ttu-id="501e2-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="501e2-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_identityriskevent"
}-->
```http
GET https://graph.microsoft.com/beta/riskyUsers/{id}
```
##### <a name="response"></a><span data-ttu-id="501e2-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="501e2-135">Response</span></span>
<span data-ttu-id="501e2-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="501e2-136">Here is an example of the response.</span></span>
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
