---
title: Obtener governanceRoleDefinition
description: Recuperar las propiedades y relaciones de un governanceRoleDefinition.
localization_priority: Normal
ms.openlocfilehash: 99f19e1942c198259d9df7dd6e0f9e5a7685bc09
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27865068"
---
# <a name="get-governanceroledefinition"></a><span data-ttu-id="7721b-103">Obtener governanceRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7721b-103">Get governanceRoleDefinition</span></span>

> <span data-ttu-id="7721b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7721b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7721b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7721b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7721b-106">Recuperar las propiedades y relaciones de un [governanceRoleDefinition](../resources/governanceroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="7721b-106">Retrieve the properties and relationships of a [governanceRoleDefinition](../resources/governanceroledefinition.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="7721b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7721b-107">Permissions</span></span>
<span data-ttu-id="7721b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7721b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7721b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7721b-110">Permission type</span></span>      | <span data-ttu-id="7721b-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="7721b-111">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7721b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7721b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7721b-113">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="7721b-113">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="7721b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7721b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7721b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7721b-115">Not supported.</span></span>    |
|<span data-ttu-id="7721b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7721b-116">Application</span></span> | <span data-ttu-id="7721b-117">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="7721b-117">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

<span data-ttu-id="7721b-118">Además el ámbito de permiso, esta API requiere el solicitante tener al menos una asignación de funciones en el recurso, que pertenece el [governanceRoleDefinition](../resources/governanceroledefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="7721b-118">Besides the permission scope, this API requires the requestor to have at least one role assignment on the resource, which the [governanceRoleDefinition](../resources/governanceroledefinition.md) belongs to.</span></span>

## <a name="http-request"></a><span data-ttu-id="7721b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7721b-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedAccess/azureResources/resources/{resourceId}/roleDefinitions/{id}
GET /privilegedAccess/azureResources/roleDefinitions/{id}?$filter=resourceId+eq+'{resourceId}'
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7721b-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7721b-120">Optional query parameters</span></span>
<span data-ttu-id="7721b-121">Este método no **no** hay compatibilidad con los [Parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7721b-121">This method does **not** support the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7721b-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7721b-122">Request headers</span></span>
| <span data-ttu-id="7721b-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="7721b-123">Name</span></span>      |<span data-ttu-id="7721b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7721b-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="7721b-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="7721b-125">Authorization</span></span>  | <span data-ttu-id="7721b-126">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="7721b-126">Bearer {code}</span></span>|


## <a name="request-body"></a><span data-ttu-id="7721b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7721b-127">Request body</span></span>
<span data-ttu-id="7721b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7721b-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="7721b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7721b-129">Response</span></span>
<span data-ttu-id="7721b-130">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [governanceRoleDefinition](../resources/governanceroledefinition.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7721b-130">If successful, this method returns a `200 OK` response code and [governanceRoleDefinition](../resources/governanceroledefinition.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7721b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7721b-131">Example</span></span>
<span data-ttu-id="7721b-132">En este ejemplo se muestra cómo obtener detalles de la definición de rol Colaborador de zona de DNS en la suscripción Wingtip Toys - Prod.</span><span class="sxs-lookup"><span data-stu-id="7721b-132">This example shows how to get details of role definition DNS Zone Contributor in the subscription Wingtip Toys - Prod.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_governanceroledefinition"
}-->
##### <a name="request"></a><span data-ttu-id="7721b-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7721b-133">Request</span></span>
```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/resources/e5e7d29d-5465-45ac-885f-4716a5ee74b5/roleDefinitions/00efc9e0-1b96-4e9a-99a3-a3df0735cf88
```
##### <a name="response"></a><span data-ttu-id="7721b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7721b-134">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleDefinition"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 174

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceRoleDefinitions/$entity",
    "id": "00efc9e0-1b96-4e9a-99a3-a3df0735cf88",
    "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
    "externalId": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/providers/Microsoft.Authorization/roleDefinitions/befefa01-2a29-4197-83a8-272ff33ce314",
    "templateId": "befefa01-2a29-4197-83a8-272ff33ce314",
    "displayName": "DNS Zone Contributor"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get governanceRoleDefinition",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
