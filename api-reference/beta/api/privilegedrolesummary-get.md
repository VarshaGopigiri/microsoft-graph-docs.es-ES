---
title: Obtener privilegedRoleSummary
description: Recuperar las propiedades y relaciones del objeto privilegedRoleSummary.
ms.openlocfilehash: 8be8fd91cbe3601953cfc0a760e31ca49ae1cf56
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088695"
---
# <a name="get-privilegedrolesummary"></a><span data-ttu-id="f943e-103">Obtener privilegedRoleSummary</span><span class="sxs-lookup"><span data-stu-id="f943e-103">Get privilegedRoleSummary</span></span>

> <span data-ttu-id="f943e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f943e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f943e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f943e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f943e-106">Recuperar las propiedades y relaciones del objeto [privilegedRoleSummary](../resources/privilegedrolesummary.md) .</span><span class="sxs-lookup"><span data-stu-id="f943e-106">Retrieve the properties and relationships of [privilegedRoleSummary](../resources/privilegedrolesummary.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="f943e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f943e-107">Permissions</span></span>
<span data-ttu-id="f943e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f943e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="f943e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f943e-110">Permission type</span></span>      | <span data-ttu-id="f943e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f943e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f943e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f943e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f943e-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f943e-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="f943e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f943e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f943e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f943e-115">Not supported.</span></span>    |
|<span data-ttu-id="f943e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f943e-116">Application</span></span> | <span data-ttu-id="f943e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f943e-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f943e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f943e-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedRoles/{id}?$expand=summary
```
## <a name="optional-query-parameters"></a><span data-ttu-id="f943e-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f943e-119">Optional query parameters</span></span>
<span data-ttu-id="f943e-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f943e-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f943e-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f943e-121">Request headers</span></span>
| <span data-ttu-id="f943e-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="f943e-122">Name</span></span>      |<span data-ttu-id="f943e-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="f943e-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f943e-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="f943e-124">Authorization</span></span>  | <span data-ttu-id="f943e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f943e-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f943e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f943e-127">Request body</span></span>
<span data-ttu-id="f943e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f943e-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f943e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f943e-129">Response</span></span>

<span data-ttu-id="f943e-130">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [privilegedRoleSummary](../resources/privilegedrolesummary.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f943e-130">If successful, this method returns a `200 OK` response code and [privilegedRoleSummary](../resources/privilegedrolesummary.md) object in the response body.</span></span>

<span data-ttu-id="f943e-131">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="f943e-131">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="f943e-132">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="f943e-132">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="f943e-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f943e-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f943e-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f943e-134">Request</span></span>
<span data-ttu-id="f943e-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f943e-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_privilegedrolesummary"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedRoles/{id}/summary
```
##### <a name="response"></a><span data-ttu-id="f943e-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f943e-136">Response</span></span>
<span data-ttu-id="f943e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f943e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleSummary"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 137

{
  "id": "id-value",
  "status": "status-value",
  "usersCount": 99,
  "managedCount": 99,
  "elevatedCount": 99,
  "mfaEnabled": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get privilegedRoleSummary",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->