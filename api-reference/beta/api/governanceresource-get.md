---
title: Obtener governanceResource
description: Recuperar las propiedades y relaciones de un objeto governanceResource.
localization_priority: Normal
ms.openlocfilehash: 16442ea971a635aedfd89f09c48ffddf14c83b95
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888035"
---
# <a name="get-governanceresource"></a><span data-ttu-id="86984-103">Obtener governanceResource</span><span class="sxs-lookup"><span data-stu-id="86984-103">Get governanceResource</span></span>

> <span data-ttu-id="86984-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="86984-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="86984-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="86984-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="86984-106">Recuperar las propiedades y relaciones de un objeto [governanceResource](../resources/governanceresource.md) .</span><span class="sxs-lookup"><span data-stu-id="86984-106">Retrieve the properties and relationships of a [governanceResource](../resources/governanceresource.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="86984-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="86984-107">Permissions</span></span>
<span data-ttu-id="86984-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="86984-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="86984-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="86984-110">Permission type</span></span>      | <span data-ttu-id="86984-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="86984-111">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="86984-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="86984-112">Delegated (work or school account)</span></span> | <span data-ttu-id="86984-113">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="86984-113">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="86984-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="86984-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="86984-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="86984-115">Not supported.</span></span>    |
|<span data-ttu-id="86984-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="86984-116">Application</span></span> | <span data-ttu-id="86984-117">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="86984-117">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

<span data-ttu-id="86984-118">Además del ámbito de permiso, esta API requiere el solicitante tener al menos una asignación de funciones en el recurso.</span><span class="sxs-lookup"><span data-stu-id="86984-118">Besides the permission scope, this API requires the requestor to have at least one role assignment on the resource.</span></span>

## <a name="http-request"></a><span data-ttu-id="86984-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="86984-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedAccess/azureResources/resources/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="86984-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="86984-120">Optional query parameters</span></span>
<span data-ttu-id="86984-121">Este método **sólo** es compatible con `$select` y `$expand` de [Parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86984-121">This method **only** supports  `$select` and `$expand` [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="86984-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="86984-122">Request headers</span></span>
| <span data-ttu-id="86984-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="86984-123">Name</span></span>      |<span data-ttu-id="86984-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="86984-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="86984-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="86984-125">Authorization</span></span>  | <span data-ttu-id="86984-126">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="86984-126">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="86984-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="86984-127">Request body</span></span>
<span data-ttu-id="86984-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="86984-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="86984-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86984-129">Response</span></span>
<span data-ttu-id="86984-130">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [governanceResource](../resources/governanceresource.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86984-130">If successful, this method returns a `200 OK` response code and [governanceResource](../resources/governanceresource.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="86984-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="86984-131">Example</span></span>
<span data-ttu-id="86984-132">En este ejemplo se muestra cómo obtener los detalles de la suscripción de Wingtip Toys - Prod (e5e7d29d-5465-45ac-885f-4716a5ee74b5).</span><span class="sxs-lookup"><span data-stu-id="86984-132">This example shows how to get the details of the subscription Wingtip Toys - Prod (e5e7d29d-5465-45ac-885f-4716a5ee74b5).</span></span>
<!-- {
  "blockType": "request",
  "name": "get_governanceresource"
}-->
##### <a name="request"></a><span data-ttu-id="86984-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="86984-133">Request</span></span>
```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/resources/e5e7d29d-5465-45ac-885f-4716a5ee74b5
```
##### <a name="response"></a><span data-ttu-id="86984-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86984-134">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceResource"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-Length: 459

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceResources/$entity",
    "id": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
    "externalId": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d",
    "type": "subscription",
    "displayName": "Wingtip Toys - Prod",
    "status": "Active",
    "registeredDateTime": "2018-04-05T22:30:37.13Z",
    "registeredRoot": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d",    
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get governanceResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
