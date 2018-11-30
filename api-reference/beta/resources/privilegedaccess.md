---
title: tipo de recurso privilegedAccess
description: " Por ejemplo, `privilegedAccess/azureResources` representa PIM administración con privilegios de acceso a los recursos de Azure."
ms.openlocfilehash: af109c0cc355bfb282630d21cd02bb463b944f38
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090771"
---
# <a name="privilegedaccess-resource-type"></a><span data-ttu-id="f92ae-103">tipo de recurso privilegedAccess</span><span class="sxs-lookup"><span data-stu-id="f92ae-103">privilegedAccess resource type</span></span>

> <span data-ttu-id="f92ae-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f92ae-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f92ae-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f92ae-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f92ae-106">Representa un grupo de funcionalidades proporcionadas por el servicio de administración de identidad con privilegios (PIM).</span><span class="sxs-lookup"><span data-stu-id="f92ae-106">Represents a group of functionalities provided by the Privileged Identity Management (PIM) service.</span></span> <span data-ttu-id="f92ae-107">Instancias diferentes de `privilegedAccess` representan diferentes proveedores administrados por PIM; Por ejemplo, `privilegedAccess/azureResources` representa PIM administración con privilegios de acceso a los recursos de Azure.</span><span class="sxs-lookup"><span data-stu-id="f92ae-107">Different instances of `privilegedAccess` represent different providers managed by PIM; for example, `privilegedAccess/azureResources` represents PIM managing privileged access to Azure resources.</span></span>


<span data-ttu-id="f92ae-108">`privilegedAccess`es de sólo lectura por ahora.</span><span class="sxs-lookup"><span data-stu-id="f92ae-108">`privilegedAccess` is read-only for now.</span></span> <span data-ttu-id="f92ae-109">No `POST`, `PUT`, `PATCH`, o `DELETE` operaciones son compatibles con el `privilegedAccess` conjunto de entidades.</span><span class="sxs-lookup"><span data-stu-id="f92ae-109">No `POST`, `PUT`, `PATCH`, or `DELETE` operations are supported on the `privilegedAccess` entity set.</span></span>

## <a name="properties"></a><span data-ttu-id="f92ae-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f92ae-110">Properties</span></span>
| <span data-ttu-id="f92ae-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f92ae-111">Property</span></span>  | <span data-ttu-id="f92ae-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="f92ae-112">Type</span></span>      |<span data-ttu-id="f92ae-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f92ae-113">Description</span></span>|
|:----------|:----------|:----------|
|<span data-ttu-id="f92ae-114">id</span><span class="sxs-lookup"><span data-stu-id="f92ae-114">id</span></span>         |<span data-ttu-id="f92ae-115">String</span><span class="sxs-lookup"><span data-stu-id="f92ae-115">String</span></span>     |<span data-ttu-id="f92ae-116">El identificador del proveedor administrado por PIM.</span><span class="sxs-lookup"><span data-stu-id="f92ae-116">The id of the provider managed by PIM.</span></span>|
|<span data-ttu-id="f92ae-117">displayName</span><span class="sxs-lookup"><span data-stu-id="f92ae-117">displayName</span></span>|<span data-ttu-id="f92ae-118">String</span><span class="sxs-lookup"><span data-stu-id="f92ae-118">String</span></span>     |<span data-ttu-id="f92ae-119">El nombre para mostrar del proveedor administrado por PIM.</span><span class="sxs-lookup"><span data-stu-id="f92ae-119">The display name of the provider managed by PIM.</span></span>|


## <a name="relationships"></a><span data-ttu-id="f92ae-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f92ae-120">Relationships</span></span>
| <span data-ttu-id="f92ae-121">Relación</span><span class="sxs-lookup"><span data-stu-id="f92ae-121">Relationship</span></span>   | <span data-ttu-id="f92ae-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="f92ae-122">Type</span></span>                                         |<span data-ttu-id="f92ae-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="f92ae-123">Description</span></span>|
|:---------------|:---------------------------------------------|:----------|
|<span data-ttu-id="f92ae-124">recursos</span><span class="sxs-lookup"><span data-stu-id="f92ae-124">resources</span></span>       |<span data-ttu-id="f92ae-125">colección de [governanceResource](../resources/governanceresource.md)</span><span class="sxs-lookup"><span data-stu-id="f92ae-125">[governanceResource](../resources/governanceresource.md) collection</span></span>            |<span data-ttu-id="f92ae-126">Una colección de recursos para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f92ae-126">A collection of resources for the provider.</span></span>|
|<span data-ttu-id="f92ae-127">roleAssignments</span><span class="sxs-lookup"><span data-stu-id="f92ae-127">roleAssignments</span></span> |<span data-ttu-id="f92ae-128">colección de [governanceRoleAssignment](../resources/governanceroleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="f92ae-128">[governanceRoleAssignment](../resources/governanceroleassignment.md) collection</span></span>|<span data-ttu-id="f92ae-129">Una colección de asignaciones de roles para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f92ae-129">A collection of role assignments for the provider.</span></span>|
|<span data-ttu-id="f92ae-130">roleDefinitions</span><span class="sxs-lookup"><span data-stu-id="f92ae-130">roleDefinitions</span></span> |<span data-ttu-id="f92ae-131">colección de [governanceRoleDefinition](../resources/governanceroledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="f92ae-131">[governanceRoleDefinition](../resources/governanceroledefinition.md) collection</span></span>|<span data-ttu-id="f92ae-132">Una colección de definiciones de rol para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f92ae-132">A collection of role defintions for the provider.</span></span>|
|<span data-ttu-id="f92ae-133">roleAssignmentRequests</span><span class="sxs-lookup"><span data-stu-id="f92ae-133">roleAssignmentRequests</span></span> |<span data-ttu-id="f92ae-134">colección de [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md)</span><span class="sxs-lookup"><span data-stu-id="f92ae-134">[governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) collection</span></span>|<span data-ttu-id="f92ae-135">Una colección de solicitudes de asignación de rol para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f92ae-135">A collection of role assignment requests for the provider.</span></span>|
|<span data-ttu-id="f92ae-136">roleSettings</span><span class="sxs-lookup"><span data-stu-id="f92ae-136">roleSettings</span></span> |<span data-ttu-id="f92ae-137">colección de [governanceRoleSetting](../resources/governancerolesetting.md)</span><span class="sxs-lookup"><span data-stu-id="f92ae-137">[governanceRoleSetting](../resources/governancerolesetting.md) collection</span></span>|<span data-ttu-id="f92ae-138">Una colección de configuración de las funciones para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f92ae-138">A collection of role settings for the provider.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="f92ae-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f92ae-139">JSON representation</span></span>

<span data-ttu-id="f92ae-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f92ae-140">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedAccess"
}-->

```json
{
  "id": "String (identifier)",
  "displayName": "String",
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedAccess",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
