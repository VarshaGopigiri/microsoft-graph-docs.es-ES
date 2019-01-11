---
title: tipo de recurso licenseAssignmentState
description: 'La propiedad **licenseAssignmentStates** de la entidad de usuario es una colección de **licenseAssignmentState**. Proporciona información detallada acerca de las asignaciones de licencia a un usuario. Los detalles se incluye información como:  '
localization_priority: Normal
ms.openlocfilehash: 51ff878f356902362487eda36d17c1894c33e5f5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855632"
---
# <a name="licenseassignmentstate-resource-type"></a><span data-ttu-id="12923-105">tipo de recurso licenseAssignmentState</span><span class="sxs-lookup"><span data-stu-id="12923-105">licenseAssignmentState resource type</span></span>

> <span data-ttu-id="12923-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="12923-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="12923-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="12923-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="12923-108">La propiedad **licenseAssignmentStates** de la entidad de [usuario](user.md) es una colección de **licenseAssignmentState**.</span><span class="sxs-lookup"><span data-stu-id="12923-108">The **licenseAssignmentStates** property of the [user](user.md) entity is a collection of **licenseAssignmentState**.</span></span> <span data-ttu-id="12923-109">Proporciona información detallada acerca de las asignaciones de licencia a un usuario.</span><span class="sxs-lookup"><span data-stu-id="12923-109">It provides details about license assignments to a user.</span></span> <span data-ttu-id="12923-110">Los detalles se incluye información como:</span><span class="sxs-lookup"><span data-stu-id="12923-110">The details includes information like:</span></span>  

 - <span data-ttu-id="12923-111">¿Qué planes están deshabilitados para un usuario</span><span class="sxs-lookup"><span data-stu-id="12923-111">What plans are disabled for a user</span></span>
 - <span data-ttu-id="12923-112">Si la licencia se ha asignado al usuario directamente o se hereda de un grupo de</span><span class="sxs-lookup"><span data-stu-id="12923-112">Whether the license was assigned to the user directly or inherited from a group</span></span>
 - <span data-ttu-id="12923-113">Estado actual de la asignación</span><span class="sxs-lookup"><span data-stu-id="12923-113">Current state of the assignment</span></span>
 - <span data-ttu-id="12923-114">Si el estado de la asignación es Error, ¿cuál es el detalle de error para el error?</span><span class="sxs-lookup"><span data-stu-id="12923-114">If the assignment state is Error, what is the error detail for the failure?</span></span> 


## <a name="properties"></a><span data-ttu-id="12923-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="12923-115">Properties</span></span>
| <span data-ttu-id="12923-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="12923-116">Property</span></span>     | <span data-ttu-id="12923-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="12923-117">Type</span></span>   |<span data-ttu-id="12923-118">Description</span><span class="sxs-lookup"><span data-stu-id="12923-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="12923-119">assignedByGroup</span><span class="sxs-lookup"><span data-stu-id="12923-119">assignedByGroup</span></span>|<span data-ttu-id="12923-120">string</span><span class="sxs-lookup"><span data-stu-id="12923-120">string</span></span>|<span data-ttu-id="12923-121">El identificador del grupo al que se asigna esta licencia.</span><span class="sxs-lookup"><span data-stu-id="12923-121">The id of the group that assigns this license.</span></span> <span data-ttu-id="12923-122">Si la asignación es una licencia asignada directos, este campo será Null.</span><span class="sxs-lookup"><span data-stu-id="12923-122">If the assignment is a direct-assigned license, this field will be Null.</span></span> <span data-ttu-id="12923-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="12923-123">Read-Only.</span></span>|
|<span data-ttu-id="12923-124">disabledPlans</span><span class="sxs-lookup"><span data-stu-id="12923-124">disabledPlans</span></span>|<span data-ttu-id="12923-125">Collection(String)</span><span class="sxs-lookup"><span data-stu-id="12923-125">Collection(String)</span></span>|<span data-ttu-id="12923-126">Los planes de servicio que están deshabilitados en esta asignación.</span><span class="sxs-lookup"><span data-stu-id="12923-126">The service plans that are disabled in this assignment.</span></span> <span data-ttu-id="12923-127">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="12923-127">Read-Only.</span></span>|
|<span data-ttu-id="12923-128">error</span><span class="sxs-lookup"><span data-stu-id="12923-128">error</span></span>|<span data-ttu-id="12923-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="12923-129">String</span></span>|<span data-ttu-id="12923-130">Error de asignación de licencia.</span><span class="sxs-lookup"><span data-stu-id="12923-130">License assignment failure error.</span></span> <span data-ttu-id="12923-131">Si la licencia está asignada correctamente, este campo será Null.</span><span class="sxs-lookup"><span data-stu-id="12923-131">If the license is assigned successfully, this field will be Null.</span></span> <span data-ttu-id="12923-132">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="12923-132">Read-Only.</span></span> <span data-ttu-id="12923-133">Valores posibles: `CountViolation`, `MutuallyExclusiveViolation`, `DependencyViolation`, `ProhibitedInUsageLocationViolation`, `UniquenessViolation`, y `Others`.</span><span class="sxs-lookup"><span data-stu-id="12923-133">Possible values: `CountViolation`, `MutuallyExclusiveViolation`, `DependencyViolation`, `ProhibitedInUsageLocationViolation`, `UniquenessViolation`, and `Others`.</span></span> <span data-ttu-id="12923-134">Para obtener más información acerca de cómo identificar y resolver la asignación de licencias de errores, consulte [aquí](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-resolve-problems).</span><span class="sxs-lookup"><span data-stu-id="12923-134">For more information on how to identify and resolve license assignment errors see [here](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-resolve-problems).</span></span>|
|<span data-ttu-id="12923-135">skuId</span><span class="sxs-lookup"><span data-stu-id="12923-135">skuId</span></span>|<span data-ttu-id="12923-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="12923-136">String</span></span>|<span data-ttu-id="12923-137">Identificador único de la SKU.</span><span class="sxs-lookup"><span data-stu-id="12923-137">The unique identifier for the SKU.</span></span> <span data-ttu-id="12923-138">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="12923-138">Read-Only.</span></span>|
|<span data-ttu-id="12923-139">state</span><span class="sxs-lookup"><span data-stu-id="12923-139">state</span></span>|<span data-ttu-id="12923-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="12923-140">String</span></span>|<span data-ttu-id="12923-141">Indicar el estado actual de esta asignación.</span><span class="sxs-lookup"><span data-stu-id="12923-141">Indicate the current state of this assignment.</span></span> <span data-ttu-id="12923-142">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="12923-142">Read-Only.</span></span> <span data-ttu-id="12923-143">Valores posibles: activo, ActiveWithError, deshabilitado y Error.</span><span class="sxs-lookup"><span data-stu-id="12923-143">Possible values: Active, ActiveWithError, Disabled and Error.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="12923-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="12923-144">JSON representation</span></span>

<span data-ttu-id="12923-145">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="12923-145">Here is a JSON representation of the resource</span></span>

```json
{
  "assignedByGroup": "String",
  "disabledPlans": "Collection(String)",
  "error": " String ",  
  "skuId": "String ",
  "state": "String"
}

```
