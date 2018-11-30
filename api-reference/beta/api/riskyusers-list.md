---
title: Lista riskyUsers
description: Recuperar las propiedades y relaciones de un objeto **riskyUsers** .
ms.openlocfilehash: 152171ff098bb58e8cbb247ca687841e77594ead
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091132"
---
# <a name="list-riskyusers"></a><span data-ttu-id="35618-103">Lista riskyUsers</span><span class="sxs-lookup"><span data-stu-id="35618-103">List riskyUsers</span></span>

> <span data-ttu-id="35618-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="35618-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="35618-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="35618-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="35618-106">Recuperar las propiedades y relaciones de un objeto **riskyUsers** .</span><span class="sxs-lookup"><span data-stu-id="35618-106">Retrieve the properties and relationships of a **riskyUsers** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="35618-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="35618-107">Permissions</span></span>
<span data-ttu-id="35618-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="35618-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="35618-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="35618-110">Permission type</span></span>      | <span data-ttu-id="35618-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="35618-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="35618-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="35618-112">Delegated (work or school account)</span></span> | <span data-ttu-id="35618-113">IdentityriskyUser.Read.All</span><span class="sxs-lookup"><span data-stu-id="35618-113">IdentityriskyUser.Read.All</span></span>    |
|<span data-ttu-id="35618-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="35618-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="35618-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="35618-115">Not supported.</span></span>    |
|<span data-ttu-id="35618-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="35618-116">Application</span></span> | <span data-ttu-id="35618-117">IdentityriskyUser.Read.All</span><span class="sxs-lookup"><span data-stu-id="35618-117">IdentityriskyUser.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="35618-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="35618-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /riskyUsers/{query}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="35618-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="35618-119">Optional query parameters</span></span>
<span data-ttu-id="35618-120">Este método es compatible con `$filter` para personalizar la respuesta de consulta.</span><span class="sxs-lookup"><span data-stu-id="35618-120">This method supports `$filter` to customize the query response.</span></span> <span data-ttu-id="35618-121">Vea el ejemplo más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="35618-121">See the example later in this topic.</span></span> 

## <a name="request-headers"></a><span data-ttu-id="35618-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="35618-122">Request headers</span></span>
| <span data-ttu-id="35618-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="35618-123">Name</span></span>      |<span data-ttu-id="35618-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="35618-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="35618-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="35618-125">Authorization</span></span>  | <span data-ttu-id="35618-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="35618-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="35618-128">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="35618-128">Workbook-Session-Id</span></span>  | <span data-ttu-id="35618-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="35618-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="35618-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="35618-131">Request body</span></span>
<span data-ttu-id="35618-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="35618-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="35618-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35618-133">Response</span></span>

<span data-ttu-id="35618-134">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [identityRiskEvent](../resources/identityriskevent.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35618-134">If successful, this method returns a `200 OK` response code and [identityRiskEvent](../resources/identityriskevent.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="35618-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="35618-135">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="35618-136">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="35618-136">Request 1</span></span>
<span data-ttu-id="35618-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="35618-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_identityriskevent"
}-->
```http
GET https://graph.microsoft.com/beta/riskyUsers
```
##### <a name="response-1"></a><span data-ttu-id="35618-138">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="35618-138">Response 1</span></span>
<span data-ttu-id="35618-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35618-139">Here is an example of the response.</span></span>
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
##### <a name="request-2"></a><span data-ttu-id="35618-140">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="35618-140">Request 2</span></span>
<span data-ttu-id="35618-141">En el ejemplo siguiente se muestra cómo usar `$filter` para obtener la colección de riskyUser cuyo riesgo agregado nivel es Medium.</span><span class="sxs-lookup"><span data-stu-id="35618-141">The following example shows how to use `$filter` to get the collection of riskyUser whose aggregate risk level is Medium.</span></span>
<!-- {
  "blockType": "request",
  "name": "list_riskyusers"
}-->
```http
GET https://graph.microsoft.com/beta/riskyUsers?$filter=riskLevel eq microsoft.graph.riskLevel'medium'
```
##### <a name="response-2"></a><span data-ttu-id="35618-142">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="35618-142">Response 2</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.riskyUsers"
} -->
```http
HTTP/1.1 200 OK
{
      "id": "c2b6c2b9-dddc-acd0-2b39-d519d803dbc3",
      "riskLastUpdatedDateTime": "2018-09-22T00:04:49.1195968Z",
      "isGuest": false,
      "isDeleted": false,
      "riskDetail": "none",
      "riskLevel": "medium",
      "riskState": "atRisk",
      "userDisplayName": "Jon Doe",
      "userPrincipalName": "jon@contoso.com",
      }
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
