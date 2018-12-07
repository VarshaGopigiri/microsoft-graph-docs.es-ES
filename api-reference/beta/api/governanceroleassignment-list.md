---
title: Lista governanceRoleAssignments
description: Recuperar una colección de governanceRoleAssignments.
ms.openlocfilehash: 0f4680c8998191fa07af993e8ee3712557b7010d
ms.sourcegitcommit: 82f9d0d10388572a3073b2dde8ca0a7b409135b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/07/2018
ms.locfileid: "27191070"
---
# <a name="list-governanceroleassignments"></a><span data-ttu-id="6ab56-103">Lista governanceRoleAssignments</span><span class="sxs-lookup"><span data-stu-id="6ab56-103">List governanceRoleAssignments</span></span>

> <span data-ttu-id="6ab56-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6ab56-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6ab56-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6ab56-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6ab56-106">Recuperar una colección de [governanceRoleAssignments](../resources/governanceroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="6ab56-106">Retrieve a collection of [governanceRoleAssignments](../resources/governanceroleassignment.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="6ab56-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6ab56-107">Permissions</span></span>
<span data-ttu-id="6ab56-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6ab56-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6ab56-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ab56-110">Permission type</span></span>      | <span data-ttu-id="6ab56-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="6ab56-111">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6ab56-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ab56-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6ab56-113">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="6ab56-113">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="6ab56-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ab56-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6ab56-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ab56-115">Not supported.</span></span>    |
|<span data-ttu-id="6ab56-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ab56-116">Application</span></span> | <span data-ttu-id="6ab56-117">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="6ab56-117">PrivilegedAccess.ReadWrite.AzureResources</span></span> |


## <a name="http-request"></a><span data-ttu-id="6ab56-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ab56-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

<span data-ttu-id="6ab56-119">Una colección de [governanceRoleAssignments](../resources/governanceroleassignment.md) en un recurso de la lista.</span><span class="sxs-lookup"><span data-stu-id="6ab56-119">List a collection of [governanceRoleAssignments](../resources/governanceroleassignment.md) on a resource.</span></span>

><span data-ttu-id="6ab56-120">**Nota:** Además el ámbito de permiso, esta solicitud requiere que el solicitante puede tener al menos una asignación de funciones en el recurso.</span><span class="sxs-lookup"><span data-stu-id="6ab56-120">**Note:** Besides the permission scope, this request requires the requestor to have at least one role assignment on the resource.</span></span> 
```http
GET /privilegedAccess/azureResources/resources/{resourceId}/roleAssignments
GET /privilegedAccess/azureResources/roleAssignments?$filter=resourceId+eq+'{resourceId}'
```
<span data-ttu-id="6ab56-121">Lista de una colección de [governanceRoleAssignments](../resources/governanceroleassignment.md) mío.</span><span class="sxs-lookup"><span data-stu-id="6ab56-121">List a collection of [governanceRoleAssignments](../resources/governanceroleassignment.md) of mine.</span></span>
```http
GET /privilegedAccess/azureResources/roleAssignments?$filter=subjectId+eq+'{myId}'
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6ab56-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6ab56-122">Optional query parameters</span></span>
<span data-ttu-id="6ab56-123">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ab56-123">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6ab56-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6ab56-124">Request headers</span></span>
| <span data-ttu-id="6ab56-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="6ab56-125">Name</span></span>      |<span data-ttu-id="6ab56-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ab56-126">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="6ab56-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="6ab56-127">Authorization</span></span>  | <span data-ttu-id="6ab56-128">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="6ab56-128">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="6ab56-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ab56-129">Request body</span></span>
<span data-ttu-id="6ab56-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6ab56-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6ab56-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ab56-131">Response</span></span>
<span data-ttu-id="6ab56-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [governanceRoleAssignment](../resources/governanceroleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ab56-132">If successful, this method returns a `200 OK` response code and a collection of [governanceRoleAssignment](../resources/governanceroleassignment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6ab56-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ab56-133">Example</span></span>

<span data-ttu-id="6ab56-134">En este ejemplo se muestra cómo obtener Mis asignaciones de roles en la suscripción de Wingtip Toys - Prod.</span><span class="sxs-lookup"><span data-stu-id="6ab56-134">This example shows how to get my role assignments on the subscription Wingtip Toys - Prod.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_governanceroleassignments"
}-->
##### <a name="request"></a><span data-ttu-id="6ab56-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ab56-135">Request</span></span>

```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignments?$filter=subjectId+eq+'918e54be-12c4-4f4c-a6d3-2ee0e3661c51'
```
##### <a name="response"></a><span data-ttu-id="6ab56-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ab56-136">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.governanceRoleAssignment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-Length: 2062

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceRoleAssignments",
    "value": [
        {
            "id": "20f4157d-5837-4356-9630-ebd3a832f227",
            "resourceId": "fb016e3a-c3ed-4d9d-96b6-a54cd4f0b735",
            "roleDefinitionId": "bc75b4e6-7403-4243-bf2f-d1f6990be122",
            "subjectId": "918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
            "linkedEligibleRoleAssignmentId": null,
            "externalId": null,
            "startDateTime": "2018-03-13T01:19:08.59Z",
            "endDateTime": "2018-06-11T01:18:37.08Z",
            "memberType": "Direct",
            "assignmentState": "Eligible",
            "status": "Provisioned"
        },
        {
            "id": "e327f4be-42a0-47a2-8579-0a39b025b394",
            "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
            "roleDefinitionId": "8b4d1d51-08e9-4254-b0a6-b16177aae376",
            "subjectId": "918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
            "linkedEligibleRoleAssignmentId": null,
            "externalId": null,
            "startDateTime": "2018-03-28T16:56:48.243Z",
            "endDateTime": "2018-09-24T16:56:30.547Z",
            "memberType": "Direct",
            "assignmentState": "Eligible",
            "status": "Provisioned"
        },
        ...
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List roleAssignments",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
