---
title: Obtener governanceRoleAssignment
description: Recuperar las propiedades y relaciones de un governanceRoleAssignment.
ms.openlocfilehash: 622fb890422ed0a4cf00542fede5ebaf662e5e71
ms.sourcegitcommit: 82f9d0d10388572a3073b2dde8ca0a7b409135b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/07/2018
ms.locfileid: "27191077"
---
# <a name="get-governanceroleassignment"></a><span data-ttu-id="4c49a-103">Obtener governanceRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4c49a-103">Get governanceRoleAssignment</span></span>

> <span data-ttu-id="4c49a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4c49a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4c49a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4c49a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4c49a-106">Recuperar las propiedades y relaciones de un [governanceRoleAssignment](../resources/governanceroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="4c49a-106">Retrieve the properties and relationships of a [governanceRoleAssignment](../resources/governanceroleassignment.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="4c49a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4c49a-107">Permissions</span></span>
<span data-ttu-id="4c49a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4c49a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4c49a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4c49a-110">Permission type</span></span>      | <span data-ttu-id="4c49a-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="4c49a-111">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4c49a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4c49a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="4c49a-113">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="4c49a-113">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="4c49a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4c49a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4c49a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4c49a-115">Not supported.</span></span>    |
|<span data-ttu-id="4c49a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4c49a-116">Application</span></span> | <span data-ttu-id="4c49a-117">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="4c49a-117">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

## <a name="http-request"></a><span data-ttu-id="4c49a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4c49a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
1. <span data-ttu-id="4c49a-119">Obtener un [governanceRoleAssignment](../resources/governanceroleassignment.md) en un recurso</span><span class="sxs-lookup"><span data-stu-id="4c49a-119">Get a [governanceRoleAssignment](../resources/governanceroleassignment.md) on a resource</span></span>

    <span data-ttu-id="4c49a-120">*Nota: Además de ámbito de permiso, que requiere el solicitante tener al menos una asignación de funciones en el recurso.*</span><span class="sxs-lookup"><span data-stu-id="4c49a-120">*Note: Besides the permission scope, it requires the requestor to have at least one role assignment on the resource.*</span></span> 
```http
GET /privilegedAccess/azureResources/resources/{resourceId}/roleAssignments/{id}
GET /privilegedAccess/azureResources/roleAssignments/{id}?$filter=resourceId+eq+'{resourceId}'
```
2. <span data-ttu-id="4c49a-121">Obtener un [governanceRoleAssignment](../resources/governanceroleassignment.md) mío</span><span class="sxs-lookup"><span data-stu-id="4c49a-121">Get a [governanceRoleAssignment](../resources/governanceroleassignment.md) of mine</span></span>
```http
GET /privilegedAccess/azureResources/roleAssignments/{id}?$filter=subjectId+eq+'{myId}'
```

## <a name="optional-query-parameters"></a><span data-ttu-id="4c49a-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4c49a-122">Optional query parameters</span></span>
<span data-ttu-id="4c49a-123">Este método **es compatible con [Los parámetros de consulta de OData](/graph/query-parameters) distinto de** `$filter` para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4c49a-123">This method does **not** supports [OData Query Parameters](/graph/query-parameters) other than `$filter` to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="4c49a-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4c49a-124">Request headers</span></span>
| <span data-ttu-id="4c49a-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="4c49a-125">Name</span></span>      |<span data-ttu-id="4c49a-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c49a-126">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="4c49a-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="4c49a-127">Authorization</span></span>  | <span data-ttu-id="4c49a-128">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="4c49a-128">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="4c49a-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4c49a-129">Request body</span></span>
<span data-ttu-id="4c49a-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4c49a-130">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="4c49a-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c49a-131">Response</span></span>
<span data-ttu-id="4c49a-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [governanceRoleAssignment](../resources/governanceroleassignment.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4c49a-132">If successful, this method returns a `200 OK` response code and [governanceRoleAssignment](../resources/governanceroleassignment.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4c49a-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c49a-133">Example</span></span>
<!-- {
  "blockType": "request",
  "name": "get_governanceroleassignment"
}-->
<span data-ttu-id="4c49a-134">Obtener un [governanceRoleAssignment](../resources/governanceroleassignment.md) de suscripción "Wingtip Toys – Prod"</span><span class="sxs-lookup"><span data-stu-id="4c49a-134">Get a [governanceRoleAssignment](../resources/governanceroleassignment.md) on subscription "Wingtip Toys - Prod"</span></span>
##### <a name="request"></a><span data-ttu-id="4c49a-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4c49a-135">Request</span></span>
```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignments/0ba78f41-ee7a-4227-adb9-1499431b2164?$filter=resourceId+eq+'e5e7d29d-5465-45ac-885f-4716a5ee74b5'
```
##### <a name="response"></a><span data-ttu-id="4c49a-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c49a-136">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleAssignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 182

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceRoleAssignments/$entity",
    "id": "0ba78f41-ee7a-4227-adb9-1499431b2164",
    "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
    "roleDefinitionId": "8b4d1d51-08e9-4254-b0a6-b16177aae376",
    "subjectId": "74487eb5-1630-4fa8-9581-0bb076ea5de3",
    "linkedEligibleRoleAssignmentId": null,
    "externalId": null,
    "startDateTime": "2018-01-22T23:47:19.687Z",
    "endDateTime": "2018-07-21T23:47:02.887Z",
    "memberType": "Direct",
    "assignmentState": "Eligible",
    "status": "Provisioned"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get governanceRoleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->