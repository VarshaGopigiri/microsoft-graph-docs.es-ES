---
title: Lista governanceResources
description: Recuperar una colección de governanceResource que el solicitante tenga acceso a.
ms.openlocfilehash: 0c50fa03cc8294650fa592e3ff7a1692d89cfbb9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086244"
---
# <a name="list-governanceresources"></a><span data-ttu-id="9b53c-103">Lista governanceResources</span><span class="sxs-lookup"><span data-stu-id="9b53c-103">List governanceResources</span></span>

> <span data-ttu-id="9b53c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b53c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b53c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b53c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9b53c-106">Recuperar una colección de [governanceResource](../resources/governanceresource.md) que el solicitante tenga acceso a.</span><span class="sxs-lookup"><span data-stu-id="9b53c-106">Retrieve a collection of [governanceResource](../resources/governanceresource.md) that the requestor has access to.</span></span>

## <a name="permissions"></a><span data-ttu-id="9b53c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b53c-107">Permissions</span></span>
<span data-ttu-id="9b53c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b53c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9b53c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b53c-110">Permission type</span></span>      | <span data-ttu-id="9b53c-111">Permissions</span><span class="sxs-lookup"><span data-stu-id="9b53c-111">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9b53c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b53c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9b53c-113">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="9b53c-113">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="9b53c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b53c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9b53c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b53c-115">Not supported.</span></span>    |
|<span data-ttu-id="9b53c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b53c-116">Application</span></span> | <span data-ttu-id="9b53c-117">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="9b53c-117">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

## <a name="http-request"></a><span data-ttu-id="9b53c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b53c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedAccess/azureResources/resources
```
## <a name="optional-query-parameters"></a><span data-ttu-id="9b53c-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9b53c-119">Optional query parameters</span></span>
<span data-ttu-id="9b53c-120">Este método es compatible con los [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b53c-120">This method supports the [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9b53c-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b53c-121">Request headers</span></span>
| <span data-ttu-id="9b53c-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b53c-122">Name</span></span>      |<span data-ttu-id="9b53c-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b53c-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="9b53c-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="9b53c-124">Authorization</span></span>  | <span data-ttu-id="9b53c-125">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="9b53c-125">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="9b53c-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b53c-126">Request body</span></span>
<span data-ttu-id="9b53c-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9b53c-127">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="9b53c-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b53c-128">Response</span></span>
<span data-ttu-id="9b53c-129">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [governanceResource](../resources/governanceresource.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b53c-129">If successful, this method returns a `200 OK` response code and collection of [governanceResource](../resources/governanceresource.md) objects in the response body.</span></span>
## <a name="examples"></a><span data-ttu-id="9b53c-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9b53c-130">Examples</span></span>

<span data-ttu-id="9b53c-131">En este ejemplo se enumera todos los recursos que actualmente puedo tener acceso.</span><span class="sxs-lookup"><span data-stu-id="9b53c-131">This example lists all resources I can currently access.</span></span>
##### <a name="request"></a><span data-ttu-id="9b53c-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b53c-132">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_governanceresources"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/resources
```
##### <a name="response"></a><span data-ttu-id="9b53c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b53c-133">Response</span></span>
<span data-ttu-id="9b53c-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b53c-134">Here is an example of the response.</span></span> 

><span data-ttu-id="9b53c-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b53c-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.governanceResource",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-Length: 1289

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceResources",
    "value":[
        {
            "id": "fb016e3a-c3ed-4d9d-96b6-a54cd4f0b735",
            "externalId": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/resourceGroups/AnujRG/providers/Microsoft.Storage/storageAccounts/anujstoragefimdev",
            "type": "Microsoft.Storage/storageAccounts",
            "displayName": "anujstoragefimdev",
            "status": "Active",
            "onboardDateTime": null
        },
        {
            "id": "0e0e4461-0c46-4d13-bf69-7cacbec75471",
            "externalId": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/resourceGroups/ARPJ-TESTRG-01/providers/Microsoft.Compute/virtualMachines/APRJ-VM-01-T",
            "type": "Microsoft.Compute/virtualMachines",
            "displayName": "APRJ-VM-01-T",
            "status": "Active",
            "onboardDateTime": null
        },
        {
            "id": "c072eb85-e47b-4627-81cb-5af82a8fc9fb",
            "externalId": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/resourceGroups/ARPJ-TESTRG-01/providers/Microsoft.Compute/virtualMachines/APRJ-VM-01-T/extensions/IaaSAntimalware",
            "type": "Microsoft.Compute/virtualMachines/extensions",
            "displayName": "APRJ-VM-01-T/IaaSAntimalware",
            "status": "Active",
            "onboardDateTime": null
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List governanceResources",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
