---
title: Lista governanceRoleDefinitions
description: Obtener una colección de governanceRoleDefinitions en un recurso.
ms.openlocfilehash: ed1d4e7b51d20ed6687c52364399385054db9912
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087781"
---
# <a name="list-governanceroledefinitions"></a><span data-ttu-id="ff0e6-103">Lista governanceRoleDefinitions</span><span class="sxs-lookup"><span data-stu-id="ff0e6-103">List governanceRoleDefinitions</span></span>
> <span data-ttu-id="ff0e6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ff0e6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ff0e6-106">Obtener una colección de [governanceRoleDefinitions](../resources/governanceroledefinition.md) en un recurso.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-106">Get a collection of [governanceRoleDefinitions](../resources/governanceroledefinition.md) on a resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="ff0e6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ff0e6-107">Permissions</span></span>
<span data-ttu-id="ff0e6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ff0e6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ff0e6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ff0e6-110">Permission type</span></span>      | <span data-ttu-id="ff0e6-111">Permissions</span><span class="sxs-lookup"><span data-stu-id="ff0e6-111">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ff0e6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ff0e6-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ff0e6-113">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="ff0e6-113">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="ff0e6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ff0e6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ff0e6-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-115">Not supported.</span></span>    |
|<span data-ttu-id="ff0e6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ff0e6-116">Application</span></span> | <span data-ttu-id="ff0e6-117">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="ff0e6-117">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

<span data-ttu-id="ff0e6-118">Además del ámbito de permiso, esta API requiere el solicitante tener al menos una asignación de funciones en el recurso.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-118">Besides the permission scope, this API requires the requestor to have at least one role assignment on the resource.</span></span>

## <a name="http-request"></a><span data-ttu-id="ff0e6-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ff0e6-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedAccess/azureResources/resources/{resourceId}/roleDefinitions
GET /privilegedAccess/azureResources/roleDefinitions?$filter=resourceId+eq+'{resourceId}'
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ff0e6-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ff0e6-120">Optional query parameters</span></span>
<span data-ttu-id="ff0e6-121">Este método es compatible con los [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-121">This method supports the [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ff0e6-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ff0e6-122">Request headers</span></span>
| <span data-ttu-id="ff0e6-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="ff0e6-123">Name</span></span>      |<span data-ttu-id="ff0e6-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff0e6-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="ff0e6-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="ff0e6-125">Authorization</span></span>  | <span data-ttu-id="ff0e6-126">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="ff0e6-126">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="ff0e6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ff0e6-127">Request body</span></span>
<span data-ttu-id="ff0e6-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="ff0e6-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff0e6-129">Response</span></span>
<span data-ttu-id="ff0e6-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [governanceRoleDefinition](../resources/governanceroledefinition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-130">If successful, this method returns a `200 OK` response code and collection of [governanceRoleDefinition](../resources/governanceroledefinition.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ff0e6-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff0e6-131">Example</span></span>
<!-- {
  "blockType": "request",
  "name": "get_governanceroledefinitions"
}-->
<span data-ttu-id="ff0e6-132">En este ejemplo se muestra cómo obtener todas las definiciones de roles de la suscripción de Wingtip Toys - Prod.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-132">This example shows how to get all role definitions of the subscription Wingtip Toys - Prod.</span></span>
##### <a name="request"></a><span data-ttu-id="ff0e6-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ff0e6-133">Request</span></span>
```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/resources/e5e7d29d-5465-45ac-885f-4716a5ee74b5/roleDefinitions  
```
##### <a name="response"></a><span data-ttu-id="ff0e6-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff0e6-134">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.governanceRoleDefinition",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-Length: 21906

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceRoleDefinitions",
    "value": [
        {
            "id": "00efc9e0-1b96-4e9a-99a3-a3df0735cf88",
            "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
            "externalId": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/providers/Microsoft.Authorization/roleDefinitions/befefa01-2a29-4197-83a8-272ff33ce314",
            "templateId": "befefa01-2a29-4197-83a8-272ff33ce314",
            "displayName": "DNS Zone Contributor"
        },
        {
            "id": "051f7264-a992-429a-b345-90415af9f917",
            "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
            "externalId": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/providers/Microsoft.Authorization/roleDefinitions/c12c1c16-33a1-487b-954d-41c89c60f349",
            "templateId": "c12c1c16-33a1-487b-954d-41c89c60f349",
            "displayName": "Reader and Data Access"
        },
        {
            "id": "0789c03d-445d-40ab-aed3-d110a98146c7",
            "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
            "externalId": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/providers/Microsoft.Authorization/roleDefinitions/5d28c62d-5b37-4476-8438-e587778df237",
            "templateId": "5d28c62d-5b37-4476-8438-e587778df237",
            "displayName": "New Relic APM Account Contributor"
        },
  ]
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List governanceRoleDefinitions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
