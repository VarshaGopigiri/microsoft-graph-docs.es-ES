---
title: Exportar governanceRoleAssignmentRequests
description: Recuperar una colección de governanceRoleAssignmentRequests en el formato `application/octet-stream`, que se puede analizar como un archivo .csv en el explorador.
ms.openlocfilehash: 8b9e64faeb8134f5b0bb964d296b1bab309021d9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084982"
---
# <a name="export-governanceroleassignmentrequests"></a><span data-ttu-id="bb960-103">Exportar governanceRoleAssignmentRequests</span><span class="sxs-lookup"><span data-stu-id="bb960-103">Export governanceRoleAssignmentRequests</span></span>

> <span data-ttu-id="bb960-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bb960-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bb960-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bb960-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bb960-106">Recuperar una colección de [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) en el formato `application/octet-stream`, que se puede analizar como un archivo .csv en el explorador.</span><span class="sxs-lookup"><span data-stu-id="bb960-106">Retrieve a collection of [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) in the format `application/octet-stream`, which can be parsed as a .csv file in the browser.</span></span>

## <a name="permissions"></a><span data-ttu-id="bb960-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="bb960-107">Permissions</span></span>
<span data-ttu-id="bb960-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bb960-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bb960-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bb960-110">Permission type</span></span>      | <span data-ttu-id="bb960-111">Permissions</span><span class="sxs-lookup"><span data-stu-id="bb960-111">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bb960-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bb960-112">Delegated (work or school account)</span></span> | <span data-ttu-id="bb960-113">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="bb960-113">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="bb960-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bb960-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bb960-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb960-115">Not supported.</span></span>    |
|<span data-ttu-id="bb960-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bb960-116">Application</span></span> | <span data-ttu-id="bb960-117">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="bb960-117">PrivilegedAccess.ReadWrite.AzureResources</span></span> |


## <a name="http-request"></a><span data-ttu-id="bb960-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bb960-118">HTTP request</span></span>
<span data-ttu-id="bb960-119"><!-- { "blockType": "ignored" } -->Exportar un conjunto de [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) en un recurso</span><span class="sxs-lookup"><span data-stu-id="bb960-119"><!-- { "blockType": "ignored" } --> Export a collection of [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) on a resource</span></span>
    
><span data-ttu-id="bb960-120">**Nota:** Además el ámbito de permiso, esta solicitud requiere que el solicitante puede tener al menos una asignación de funciones en el recurso.</span><span class="sxs-lookup"><span data-stu-id="bb960-120">**Note:** Besides the permission scope, this request requires the requestor to have at least one role assignment on the resource.</span></span> 
    
```http
GET /privilegedAccess/azureResources/roleAssignments/export?$filter=resourceId+eq+'{resourceId}'
```

<span data-ttu-id="bb960-121">Exportar un conjunto de [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) mío</span><span class="sxs-lookup"><span data-stu-id="bb960-121">Export a collection of [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) of mine</span></span>
```http
GET /privilegedAccess/azureResources/roleAssignments/export?$filter=subjectId+eq+'{myId}'
```
## <a name="optional-query-parameters"></a><span data-ttu-id="bb960-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bb960-122">Optional query parameters</span></span>
<span data-ttu-id="bb960-123">Este método es compatible con los [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb960-123">This method supports the [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="bb960-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bb960-124">Request headers</span></span>
| <span data-ttu-id="bb960-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="bb960-125">Name</span></span>      |<span data-ttu-id="bb960-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb960-126">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="bb960-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="bb960-127">Authorization</span></span>  | <span data-ttu-id="bb960-128">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="bb960-128">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="bb960-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bb960-129">Request body</span></span>
<span data-ttu-id="bb960-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bb960-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bb960-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb960-131">Response</span></span>
<span data-ttu-id="bb960-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el contenido de tipo `application/octet-stream`.</span><span class="sxs-lookup"><span data-stu-id="bb960-132">If successful, this method returns a `200 OK` response code and content of type `application/octet-stream`.</span></span>

## <a name="example"></a><span data-ttu-id="bb960-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bb960-133">Example</span></span>
<span data-ttu-id="bb960-134">En este ejemplo se guarda todas las asignaciones de funciones como un archivo .csv en la suscripción Wingtip Toys - Prod.</span><span class="sxs-lookup"><span data-stu-id="bb960-134">This example saves all role assignments as a .csv file in the subscription Wingtip Toys - Prod.</span></span> 

##### <a name="request"></a><span data-ttu-id="bb960-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bb960-135">Request</span></span>
```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignments/export?filter=resourceId+eq+'85dfe48a-55d3-49fc-8f36-ee14b7f6f720'
```
##### <a name="response"></a><span data-ttu-id="bb960-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb960-136">Response</span></span>
<span data-ttu-id="bb960-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb960-137">Here is an example of the response.</span></span> 
```http
HTTP/1.1 200 OK
Content-Type:application/octet-stream
Content-Length:126

77u/77u/QXNzaWdubWVudCBMZXZlbCxVc2VyIEdyb3VwIE5hbWUsUm9sZSBOYW1lLEVtYWlsLEFzc2lnbm1lbnQgVHlwZSxBc3NpZ25tZW43IFN0YXJ0IFRpbWUgKFVUQyksQXNzaWdubWVudCBFbmQgVGltZdAoVVRDKQ0K

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Export governanceRoleAssignmentRequests",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
