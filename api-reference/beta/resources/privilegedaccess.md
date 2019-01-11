---
title: tipo de recurso privilegedAccess
description: " Por ejemplo, `privilegedAccess/azureResources` representa PIM administración con privilegios de acceso a los recursos de Azure."
localization_priority: Normal
ms.openlocfilehash: f4166fb539d627730c68c7e039fd8d672ff4c785
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810055"
---
# <a name="privilegedaccess-resource-type"></a><span data-ttu-id="27c8b-103">tipo de recurso privilegedAccess</span><span class="sxs-lookup"><span data-stu-id="27c8b-103">privilegedAccess resource type</span></span>

> <span data-ttu-id="27c8b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="27c8b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="27c8b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="27c8b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="27c8b-106">Representa un grupo de funcionalidades proporcionadas por el servicio de administración de identidad con privilegios (PIM).</span><span class="sxs-lookup"><span data-stu-id="27c8b-106">Represents a group of functionalities provided by the Privileged Identity Management (PIM) service.</span></span> <span data-ttu-id="27c8b-107">Instancias diferentes de `privilegedAccess` representan diferentes proveedores administrados por PIM; Por ejemplo, `privilegedAccess/azureResources` representa PIM administración con privilegios de acceso a los recursos de Azure.</span><span class="sxs-lookup"><span data-stu-id="27c8b-107">Different instances of `privilegedAccess` represent different providers managed by PIM; for example, `privilegedAccess/azureResources` represents PIM managing privileged access to Azure resources.</span></span>


<span data-ttu-id="27c8b-108">`privilegedAccess`es de sólo lectura por ahora.</span><span class="sxs-lookup"><span data-stu-id="27c8b-108">`privilegedAccess` is read-only for now.</span></span> <span data-ttu-id="27c8b-109">No `POST`, `PUT`, `PATCH`, o `DELETE` operaciones son compatibles con el `privilegedAccess` conjunto de entidades.</span><span class="sxs-lookup"><span data-stu-id="27c8b-109">No `POST`, `PUT`, `PATCH`, or `DELETE` operations are supported on the `privilegedAccess` entity set.</span></span>

## <a name="properties"></a><span data-ttu-id="27c8b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27c8b-110">Properties</span></span>
| <span data-ttu-id="27c8b-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27c8b-111">Property</span></span>  | <span data-ttu-id="27c8b-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="27c8b-112">Type</span></span>      |<span data-ttu-id="27c8b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="27c8b-113">Description</span></span>|
|:----------|:----------|:----------|
|<span data-ttu-id="27c8b-114">id</span><span class="sxs-lookup"><span data-stu-id="27c8b-114">id</span></span>         |<span data-ttu-id="27c8b-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="27c8b-115">String</span></span>     |<span data-ttu-id="27c8b-116">El identificador del proveedor administrado por PIM.</span><span class="sxs-lookup"><span data-stu-id="27c8b-116">The id of the provider managed by PIM.</span></span>|
|<span data-ttu-id="27c8b-117">displayName</span><span class="sxs-lookup"><span data-stu-id="27c8b-117">displayName</span></span>|<span data-ttu-id="27c8b-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="27c8b-118">String</span></span>     |<span data-ttu-id="27c8b-119">El nombre para mostrar del proveedor administrado por PIM.</span><span class="sxs-lookup"><span data-stu-id="27c8b-119">The display name of the provider managed by PIM.</span></span>|


## <a name="relationships"></a><span data-ttu-id="27c8b-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="27c8b-120">Relationships</span></span>
| <span data-ttu-id="27c8b-121">Relación</span><span class="sxs-lookup"><span data-stu-id="27c8b-121">Relationship</span></span>   | <span data-ttu-id="27c8b-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="27c8b-122">Type</span></span>                                         |<span data-ttu-id="27c8b-123">Description</span><span class="sxs-lookup"><span data-stu-id="27c8b-123">Description</span></span>|
|:---------------|:---------------------------------------------|:----------|
|<span data-ttu-id="27c8b-124">recursos</span><span class="sxs-lookup"><span data-stu-id="27c8b-124">resources</span></span>       |<span data-ttu-id="27c8b-125">colección de [governanceResource](../resources/governanceresource.md)</span><span class="sxs-lookup"><span data-stu-id="27c8b-125">[governanceResource](../resources/governanceresource.md) collection</span></span>            |<span data-ttu-id="27c8b-126">Una colección de recursos para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="27c8b-126">A collection of resources for the provider.</span></span>|
|<span data-ttu-id="27c8b-127">roleAssignments</span><span class="sxs-lookup"><span data-stu-id="27c8b-127">roleAssignments</span></span> |<span data-ttu-id="27c8b-128">colección de [governanceRoleAssignment](../resources/governanceroleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="27c8b-128">[governanceRoleAssignment](../resources/governanceroleassignment.md) collection</span></span>|<span data-ttu-id="27c8b-129">Una colección de asignaciones de roles para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="27c8b-129">A collection of role assignments for the provider.</span></span>|
|<span data-ttu-id="27c8b-130">roleDefinitions</span><span class="sxs-lookup"><span data-stu-id="27c8b-130">roleDefinitions</span></span> |<span data-ttu-id="27c8b-131">colección de [governanceRoleDefinition](../resources/governanceroledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="27c8b-131">[governanceRoleDefinition](../resources/governanceroledefinition.md) collection</span></span>|<span data-ttu-id="27c8b-132">Una colección de definiciones de rol para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="27c8b-132">A collection of role defintions for the provider.</span></span>|
|<span data-ttu-id="27c8b-133">roleAssignmentRequests</span><span class="sxs-lookup"><span data-stu-id="27c8b-133">roleAssignmentRequests</span></span> |<span data-ttu-id="27c8b-134">colección de [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md)</span><span class="sxs-lookup"><span data-stu-id="27c8b-134">[governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) collection</span></span>|<span data-ttu-id="27c8b-135">Una colección de solicitudes de asignación de rol para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="27c8b-135">A collection of role assignment requests for the provider.</span></span>|
|<span data-ttu-id="27c8b-136">roleSettings</span><span class="sxs-lookup"><span data-stu-id="27c8b-136">roleSettings</span></span> |<span data-ttu-id="27c8b-137">colección de [governanceRoleSetting](../resources/governancerolesetting.md)</span><span class="sxs-lookup"><span data-stu-id="27c8b-137">[governanceRoleSetting](../resources/governancerolesetting.md) collection</span></span>|<span data-ttu-id="27c8b-138">Una colección de configuración de las funciones para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="27c8b-138">A collection of role settings for the provider.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="27c8b-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="27c8b-139">JSON representation</span></span>

<span data-ttu-id="27c8b-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="27c8b-140">Here is a JSON representation of the resource.</span></span>

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
