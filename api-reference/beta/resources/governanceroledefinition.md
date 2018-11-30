---
title: tipo de recurso governanceRoleDefinition
description: Representa las definiciones de roles. Para obtener recursos de Azure, puede representar funciones de RBAC Azure, como propietario, lector, Colaborador, etcetera.
ms.openlocfilehash: 057d74276b41abad47eb60ce48a99f1160c401ef
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084781"
---
# <a name="governanceroledefinition-resource-type"></a><span data-ttu-id="e39fa-104">tipo de recurso governanceRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e39fa-104">governanceRoleDefinition resource type</span></span>

> <span data-ttu-id="e39fa-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e39fa-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e39fa-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e39fa-106">Use of these APIs in production applications is not supported.</span></span> 


<span data-ttu-id="e39fa-107">Representa las definiciones de roles.</span><span class="sxs-lookup"><span data-stu-id="e39fa-107">Represents the role definitions.</span></span> <span data-ttu-id="e39fa-108">Para obtener recursos de Azure, puede representar funciones de RBAC Azure, como propietario, lector, Colaborador, etcetera.</span><span class="sxs-lookup"><span data-stu-id="e39fa-108">For Azure resources, it can represent Azure RBAC roles, such as Owner, Reader, Contributor, etc.</span></span>


## <a name="methods"></a><span data-ttu-id="e39fa-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e39fa-109">Methods</span></span>

| <span data-ttu-id="e39fa-110">Método</span><span class="sxs-lookup"><span data-stu-id="e39fa-110">Method</span></span>          | <span data-ttu-id="e39fa-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e39fa-111">Return Type</span></span> |<span data-ttu-id="e39fa-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e39fa-112">Description</span></span>|
|:---------------|:--------|:--------|:----------|
|[<span data-ttu-id="e39fa-113">List</span><span class="sxs-lookup"><span data-stu-id="e39fa-113">List</span></span>](../api/governanceroledefinition-list.md) | <span data-ttu-id="e39fa-114">colección de [governanceRoleDefinition](../resources/governanceroledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="e39fa-114">[governanceRoleDefinition](../resources/governanceroledefinition.md) collection</span></span> |<span data-ttu-id="e39fa-115">Una colección de definiciones de roles en un recurso de la lista.</span><span class="sxs-lookup"><span data-stu-id="e39fa-115">List a collection of role definitions on a resource.</span></span>|
|[<span data-ttu-id="e39fa-116">Get</span><span class="sxs-lookup"><span data-stu-id="e39fa-116">Get</span></span>](../api/governanceroledefinition-get.md) | [<span data-ttu-id="e39fa-117">governanceRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e39fa-117">governanceRoleDefinition</span></span>](../resources/governanceroledefinition.md) |<span data-ttu-id="e39fa-118">Leer las propiedades y las relaciones de una entidad de definición de rol especificado por id.</span><span class="sxs-lookup"><span data-stu-id="e39fa-118">Read properties and relationships of a role definition entity specified by id.</span></span>|
<span data-ttu-id="e39fa-119">No `POST`, `PUT`, `PATCH`, `DELETE` es compatible con `roleDefinitions` conjunto de entidades por ahora.</span><span class="sxs-lookup"><span data-stu-id="e39fa-119">No `POST`, `PUT`, `PATCH`, `DELETE` is supported on `roleDefinitions` entity set for now.</span></span>
## <a name="properties"></a><span data-ttu-id="e39fa-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e39fa-120">Properties</span></span>
| <span data-ttu-id="e39fa-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e39fa-121">Property</span></span>  | <span data-ttu-id="e39fa-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="e39fa-122">Type</span></span>      |<span data-ttu-id="e39fa-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="e39fa-123">Description</span></span>|
|:----|:----------|:----------|:----------|
|<span data-ttu-id="e39fa-124">id</span><span class="sxs-lookup"><span data-stu-id="e39fa-124">id</span></span>         |<span data-ttu-id="e39fa-125">String</span><span class="sxs-lookup"><span data-stu-id="e39fa-125">String</span></span>     |<span data-ttu-id="e39fa-126">El identificador de la definición de roles.</span><span class="sxs-lookup"><span data-stu-id="e39fa-126">The id of the role definition.</span></span> |
|<span data-ttu-id="e39fa-127">resourceId</span><span class="sxs-lookup"><span data-stu-id="e39fa-127">resourceId</span></span> |<span data-ttu-id="e39fa-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="e39fa-128">String</span></span>     |<span data-ttu-id="e39fa-129">Necesario.</span><span class="sxs-lookup"><span data-stu-id="e39fa-129">Required.</span></span> <span data-ttu-id="e39fa-130">El identificador de recurso asociado a la definición de roles.</span><span class="sxs-lookup"><span data-stu-id="e39fa-130">The id of the resource associated with the role definition.</span></span> |
|<span data-ttu-id="e39fa-131">externalId</span><span class="sxs-lookup"><span data-stu-id="e39fa-131">externalId</span></span>   |<span data-ttu-id="e39fa-132">String</span><span class="sxs-lookup"><span data-stu-id="e39fa-132">String</span></span>     |<span data-ttu-id="e39fa-133">El identificador externo de la definición de roles.</span><span class="sxs-lookup"><span data-stu-id="e39fa-133">The external id of the role definition.</span></span>|
|<span data-ttu-id="e39fa-134">displayName</span><span class="sxs-lookup"><span data-stu-id="e39fa-134">displayName</span></span>|<span data-ttu-id="e39fa-135">String</span><span class="sxs-lookup"><span data-stu-id="e39fa-135">String</span></span>     |<span data-ttu-id="e39fa-136">El nombre para mostrar de la definición de roles.</span><span class="sxs-lookup"><span data-stu-id="e39fa-136">The display name of the role definition.</span></span>|
|<span data-ttu-id="e39fa-137">subjectCount</span><span class="sxs-lookup"><span data-stu-id="e39fa-137">subjectCount</span></span>|<span data-ttu-id="e39fa-138">Int32</span><span class="sxs-lookup"><span data-stu-id="e39fa-138">Int32</span></span>     |<span data-ttu-id="e39fa-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e39fa-139">Optional.</span></span> <span data-ttu-id="e39fa-140">El número de asuntos que se asignan al rol.</span><span class="sxs-lookup"><span data-stu-id="e39fa-140">The number of subjects that are assigned to the role.</span></span> <span data-ttu-id="e39fa-141">Representa el estado de acceso del solicitante para el recurso.</span><span class="sxs-lookup"><span data-stu-id="e39fa-141">It represents the status of the requestor's access to the resource.</span></span> <span data-ttu-id="e39fa-142">Para obtener la propiedad, por favor, use explícitamente `$select=subjectCount` en la consulta.</span><span class="sxs-lookup"><span data-stu-id="e39fa-142">To get the property, please explictly use `$select=subjectCount` in the query.</span></span>|
|<span data-ttu-id="e39fa-143">eligibleAssignmentCount</span><span class="sxs-lookup"><span data-stu-id="e39fa-143">eligibleAssignmentCount</span></span>|<span data-ttu-id="e39fa-144">Int32</span><span class="sxs-lookup"><span data-stu-id="e39fa-144">Int32</span></span>|<span data-ttu-id="e39fa-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e39fa-145">Optional.</span></span> <span data-ttu-id="e39fa-146">El número de asignaciones de roles optan asociado con la definición de roles.</span><span class="sxs-lookup"><span data-stu-id="e39fa-146">The number of eligible role assignments associated with the role definition.</span></span> <span data-ttu-id="e39fa-147">Para obtener la propiedad, por favor, use explícitamente `$select=eligibleAssignmentCount` en la consulta.</span><span class="sxs-lookup"><span data-stu-id="e39fa-147">To get the property, please explictly use `$select=eligibleAssignmentCount` in the query.</span></span>|
|<span data-ttu-id="e39fa-148">activeAssignmentCount</span><span class="sxs-lookup"><span data-stu-id="e39fa-148">activeAssignmentCount</span></span>|<span data-ttu-id="e39fa-149">Int32</span><span class="sxs-lookup"><span data-stu-id="e39fa-149">Int32</span></span>    |<span data-ttu-id="e39fa-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e39fa-150">Optional.</span></span> <span data-ttu-id="e39fa-151">El número de asignaciones de rol activo asociado con la definición de roles.</span><span class="sxs-lookup"><span data-stu-id="e39fa-151">The number of active role assignments associated with the role definition.</span></span>  <span data-ttu-id="e39fa-152">Para obtener la propiedad, por favor, use explícitamente `$select=activeAssignmentCount` en la consulta.</span><span class="sxs-lookup"><span data-stu-id="e39fa-152">To get the property, please explictly use `$select=activeAssignmentCount` in the query.</span></span>|


## <a name="relationships"></a><span data-ttu-id="e39fa-153">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e39fa-153">Relationships</span></span>
| <span data-ttu-id="e39fa-154">Relación</span><span class="sxs-lookup"><span data-stu-id="e39fa-154">Relationship</span></span> | <span data-ttu-id="e39fa-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="e39fa-155">Type</span></span>   |<span data-ttu-id="e39fa-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="e39fa-156">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e39fa-157">resource</span><span class="sxs-lookup"><span data-stu-id="e39fa-157">resource</span></span>|[<span data-ttu-id="e39fa-158">governanceResource</span><span class="sxs-lookup"><span data-stu-id="e39fa-158">governanceResource</span></span>](../resources/governanceresource.md)|<span data-ttu-id="e39fa-159">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e39fa-159">Read-only.</span></span> <span data-ttu-id="e39fa-160">El recurso asociado para la definición de roles.</span><span class="sxs-lookup"><span data-stu-id="e39fa-160">The associated resource for the role definition.</span></span>|
|<span data-ttu-id="e39fa-161">roleSetting</span><span class="sxs-lookup"><span data-stu-id="e39fa-161">roleSetting</span></span>|[<span data-ttu-id="e39fa-162">governanceRoleSetting</span><span class="sxs-lookup"><span data-stu-id="e39fa-162">governanceRoleSetting</span></span>](../resources/governancerolesetting.md)|<span data-ttu-id="e39fa-163">Configuración de la función asociada para la definición de roles.</span><span class="sxs-lookup"><span data-stu-id="e39fa-163">The associated role setting for the role definition.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e39fa-164">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e39fa-164">JSON representation</span></span>

<span data-ttu-id="e39fa-165">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e39fa-165">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceRoleDefinition"
}-->

```json
{
  "id": "String (identifier)",
  "resourceId": "String",
  "externalId": "String",
  "displayName": "String",
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceRoleDefinition",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->