---
title: Lista riskyUsers
description: Recuperar las propiedades y relaciones de un objeto **riskyUsers** .
ms.openlocfilehash: d800f37c1e7e2d03edc0273d30e2be37c799d0d4
ms.sourcegitcommit: ba6b1d1a12dcb54916b4d3e529c856f6514e01e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2018
ms.locfileid: "27241044"
---
# <a name="list-riskyusers"></a><span data-ttu-id="156fa-103">Lista riskyUsers</span><span class="sxs-lookup"><span data-stu-id="156fa-103">List riskyUsers</span></span>

> <span data-ttu-id="156fa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="156fa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="156fa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="156fa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="156fa-106">Recuperar las propiedades y relaciones de un objeto **riskyUsers** .</span><span class="sxs-lookup"><span data-stu-id="156fa-106">Retrieve the properties and relationships of a **riskyUsers** object.</span></span>

> <span data-ttu-id="156fa-107">**Nota:** Esta API requiere una licencia de P2 de Azure AD Premium.</span><span class="sxs-lookup"><span data-stu-id="156fa-107">**Note:** This API requires an Azure AD Premium P2 license.</span></span>

## <a name="permissions"></a><span data-ttu-id="156fa-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="156fa-108">Permissions</span></span>
<span data-ttu-id="156fa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="156fa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="156fa-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="156fa-111">Permission type</span></span>      | <span data-ttu-id="156fa-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="156fa-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="156fa-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="156fa-113">Delegated (work or school account)</span></span> | <span data-ttu-id="156fa-114">IdentityriskyUser.Read.All</span><span class="sxs-lookup"><span data-stu-id="156fa-114">IdentityriskyUser.Read.All</span></span>    |
|<span data-ttu-id="156fa-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="156fa-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="156fa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="156fa-116">Not supported.</span></span>    |
|<span data-ttu-id="156fa-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="156fa-117">Application</span></span> | <span data-ttu-id="156fa-118">IdentityriskyUser.Read.All</span><span class="sxs-lookup"><span data-stu-id="156fa-118">IdentityriskyUser.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="156fa-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="156fa-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /riskyUsers/{query}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="156fa-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="156fa-120">Optional query parameters</span></span>
<span data-ttu-id="156fa-121">Este método es compatible con `$filter` para personalizar la respuesta de consulta.</span><span class="sxs-lookup"><span data-stu-id="156fa-121">This method supports `$filter` to customize the query response.</span></span> <span data-ttu-id="156fa-122">Vea el ejemplo más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="156fa-122">See the example later in this topic.</span></span> 

## <a name="request-headers"></a><span data-ttu-id="156fa-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="156fa-123">Request headers</span></span>
| <span data-ttu-id="156fa-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="156fa-124">Name</span></span>      |<span data-ttu-id="156fa-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="156fa-125">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="156fa-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="156fa-126">Authorization</span></span>  | <span data-ttu-id="156fa-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="156fa-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="156fa-129">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="156fa-129">Workbook-Session-Id</span></span>  | <span data-ttu-id="156fa-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="156fa-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="156fa-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="156fa-132">Request body</span></span>
<span data-ttu-id="156fa-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="156fa-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="156fa-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="156fa-134">Response</span></span>

<span data-ttu-id="156fa-135">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [identityRiskEvent](../resources/identityriskevent.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="156fa-135">If successful, this method returns a `200 OK` response code and [identityRiskEvent](../resources/identityriskevent.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="156fa-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="156fa-136">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="156fa-137">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="156fa-137">Request 1</span></span>
<span data-ttu-id="156fa-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="156fa-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_identityriskevent"
}-->
```http
GET https://graph.microsoft.com/beta/riskyUsers
```
##### <a name="response-1"></a><span data-ttu-id="156fa-139">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="156fa-139">Response 1</span></span>
<span data-ttu-id="156fa-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="156fa-140">Here is an example of the response.</span></span>
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
##### <a name="request-2"></a><span data-ttu-id="156fa-141">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="156fa-141">Request 2</span></span>
<span data-ttu-id="156fa-142">En el ejemplo siguiente se muestra cómo usar `$filter` para obtener la colección de riskyUser cuyo riesgo agregado nivel es Medium.</span><span class="sxs-lookup"><span data-stu-id="156fa-142">The following example shows how to use `$filter` to get the collection of riskyUser whose aggregate risk level is Medium.</span></span>
<!-- {
  "blockType": "request",
  "name": "list_riskyusers"
}-->
```http
GET https://graph.microsoft.com/beta/riskyUsers?$filter=riskLevel eq microsoft.graph.riskLevel'medium'
```
##### <a name="response-2"></a><span data-ttu-id="156fa-143">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="156fa-143">Response 2</span></span>
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
