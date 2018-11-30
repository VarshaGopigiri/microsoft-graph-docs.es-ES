---
title: tipo de recurso governanceRoleSetting
description: " regla y así sucesivamente."
ms.openlocfilehash: 64245b2d6f0aa9e0ea3ffda4a5eaebfb9fd205df
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087433"
---
# <a name="governancerolesetting-resource-type"></a><span data-ttu-id="5707d-103">tipo de recurso governanceRoleSetting</span><span class="sxs-lookup"><span data-stu-id="5707d-103">governanceRoleSetting resource type</span></span>

> <span data-ttu-id="5707d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5707d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5707d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5707d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5707d-106">Representa un conjunto de configuraciones en cada definición de roles que necesite se evalúa cuando se cree o modifique las asignaciones de roles.</span><span class="sxs-lookup"><span data-stu-id="5707d-106">Represents a set of configurations on each role definition that needs to be evaluated against when role assignments are created or modified.</span></span> <span data-ttu-id="5707d-107">Por ejemplo, la configuración de las funciones puede incluir regla de "asignación máxima duración", "MFA necesarios en activación" regla y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="5707d-107">For example, role settings might include "maximum assignment duration" rule, "MFA required on activation" rule, and so on.</span></span>

## <a name="methods"></a><span data-ttu-id="5707d-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="5707d-108">Methods</span></span>

| <span data-ttu-id="5707d-109">Método</span><span class="sxs-lookup"><span data-stu-id="5707d-109">Method</span></span>          | <span data-ttu-id="5707d-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5707d-110">Return Type</span></span> |<span data-ttu-id="5707d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5707d-111">Description</span></span>|
|:---------------|:--------|:--------|
|[<span data-ttu-id="5707d-112">List</span><span class="sxs-lookup"><span data-stu-id="5707d-112">List</span></span>](../api/governancerolesetting-list.md) | <span data-ttu-id="5707d-113">colección de [governanceRoleSetting](../resources/governancerolesetting.md)</span><span class="sxs-lookup"><span data-stu-id="5707d-113">[governanceRoleSetting](../resources/governancerolesetting.md) collection</span></span>|<span data-ttu-id="5707d-114">Una colección de configuración de las funciones en un recurso de la lista.</span><span class="sxs-lookup"><span data-stu-id="5707d-114">List a collection of role settings on a resource.</span></span>|
|[<span data-ttu-id="5707d-115">Get</span><span class="sxs-lookup"><span data-stu-id="5707d-115">Get</span></span>](../api/governancerolesetting-get.md) |  [<span data-ttu-id="5707d-116">governanceRoleSetting</span><span class="sxs-lookup"><span data-stu-id="5707d-116">governanceRoleSetting</span></span>](../resources/governancerolesetting.md) |<span data-ttu-id="5707d-117">Leer las propiedades y las relaciones de una configuración de rol.</span><span class="sxs-lookup"><span data-stu-id="5707d-117">Read properties and relationships of a role setting.</span></span>|
|[<span data-ttu-id="5707d-118">Update</span><span class="sxs-lookup"><span data-stu-id="5707d-118">Update</span></span>](../api/governancerolesetting-update.md) | [<span data-ttu-id="5707d-119">governanceRoleSetting</span><span class="sxs-lookup"><span data-stu-id="5707d-119">governanceRoleSetting</span></span>](../resources/governancerolesetting.md)  |<span data-ttu-id="5707d-120">Actualizar un objeto de configuración de rol.</span><span class="sxs-lookup"><span data-stu-id="5707d-120">Update a role setting object.</span></span> |

## <a name="properties"></a><span data-ttu-id="5707d-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5707d-121">Properties</span></span>
|<span data-ttu-id="5707d-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5707d-122">Property</span></span>               |<span data-ttu-id="5707d-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="5707d-123">Type</span></span>                                      |<span data-ttu-id="5707d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="5707d-124">Description</span></span>|
|:--------------------|:---------------------------------------|:----------|
|<span data-ttu-id="5707d-125">id</span><span class="sxs-lookup"><span data-stu-id="5707d-125">id</span></span>                   |<span data-ttu-id="5707d-126">String</span><span class="sxs-lookup"><span data-stu-id="5707d-126">String</span></span>                                  |<span data-ttu-id="5707d-127">El identificador de la roleSetting.</span><span class="sxs-lookup"><span data-stu-id="5707d-127">The id of the roleSetting.</span></span>|
|<span data-ttu-id="5707d-128">resourceId</span><span class="sxs-lookup"><span data-stu-id="5707d-128">resourceId</span></span>           |<span data-ttu-id="5707d-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="5707d-129">String</span></span>                                  |<span data-ttu-id="5707d-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="5707d-130">Required.</span></span> <span data-ttu-id="5707d-131">El identificador del recurso que está asociada la configuración de rol.</span><span class="sxs-lookup"><span data-stu-id="5707d-131">The id of the resource that the role setting is associated with.</span></span>|
|<span data-ttu-id="5707d-132">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="5707d-132">roleDefinitionId</span></span>     |<span data-ttu-id="5707d-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="5707d-133">String</span></span>                                  |<span data-ttu-id="5707d-134">Necesario.</span><span class="sxs-lookup"><span data-stu-id="5707d-134">Required.</span></span> <span data-ttu-id="5707d-135">El identificador de la definición de roles que está asociada la configuración de rol.</span><span class="sxs-lookup"><span data-stu-id="5707d-135">The id of the role definition that the role setting is associated with.</span></span>|
|<span data-ttu-id="5707d-136">isDefault</span><span class="sxs-lookup"><span data-stu-id="5707d-136">isDefault</span></span>            |<span data-ttu-id="5707d-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="5707d-137">Boolean</span></span>                                 |<span data-ttu-id="5707d-138">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5707d-138">Read-only.</span></span> <span data-ttu-id="5707d-139">Indicar si la roleSetting es un roleSetting predeterminada</span><span class="sxs-lookup"><span data-stu-id="5707d-139">Indicate if the roleSetting is a default roleSetting</span></span>|
|<span data-ttu-id="5707d-140">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="5707d-140">lastUpdatedDateTime</span></span>  |<span data-ttu-id="5707d-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5707d-141">DateTimeOffset</span></span>                          |<span data-ttu-id="5707d-142">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5707d-142">Read-only.</span></span> <span data-ttu-id="5707d-143">El tiempo que se actualizaron por última vez la configuración de rol.</span><span class="sxs-lookup"><span data-stu-id="5707d-143">The time when the role setting was last updated.</span></span> <span data-ttu-id="5707d-144">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="5707d-144">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="5707d-145">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="5707d-145">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="5707d-146">lastUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="5707d-146">lastUpdatedBy</span></span>        |<span data-ttu-id="5707d-147">String</span><span class="sxs-lookup"><span data-stu-id="5707d-147">String</span></span>                                  |<span data-ttu-id="5707d-148">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5707d-148">Read-only.</span></span> <span data-ttu-id="5707d-149">El nombre para mostrar del administrador que actualizó por última vez el roleSetting.</span><span class="sxs-lookup"><span data-stu-id="5707d-149">The display name of the administrator who last updated the roleSetting.</span></span>|
|<span data-ttu-id="5707d-150">adminEligibleSettings</span><span class="sxs-lookup"><span data-stu-id="5707d-150">adminEligibleSettings</span></span>|<span data-ttu-id="5707d-151">colección de [governanceRuleSetting](../resources/governancerulesetting.md)</span><span class="sxs-lookup"><span data-stu-id="5707d-151">[governanceRuleSetting](../resources/governancerulesetting.md) collection</span></span>|<span data-ttu-id="5707d-152">La configuración de la regla que se evalúa cuando un administrador intenta agregar una asignación de rol aptos.</span><span class="sxs-lookup"><span data-stu-id="5707d-152">The rule settings that are evaluated when an administrator tries to add an eligible role assignment.</span></span>|
|<span data-ttu-id="5707d-153">adminMemberSettings</span><span class="sxs-lookup"><span data-stu-id="5707d-153">adminMemberSettings</span></span>  |<span data-ttu-id="5707d-154">colección de [governanceRuleSetting](../resources/governancerulesetting.md)</span><span class="sxs-lookup"><span data-stu-id="5707d-154">[governanceRuleSetting](../resources/governancerulesetting.md) collection</span></span>|<span data-ttu-id="5707d-155">La configuración de la regla que se evalúa cuando un administrador intenta agregar una asignación de rol miembro directo.</span><span class="sxs-lookup"><span data-stu-id="5707d-155">The rule settings that are evaluated when an administrator tries to add a direct member role assignment.</span></span>|
|<span data-ttu-id="5707d-156">userEligibleSettings</span><span class="sxs-lookup"><span data-stu-id="5707d-156">userEligibleSettings</span></span> |<span data-ttu-id="5707d-157">colección de [governanceRuleSetting](../resources/governancerulesetting.md)</span><span class="sxs-lookup"><span data-stu-id="5707d-157">[governanceRuleSetting](../resources/governancerulesetting.md) collection</span></span>|<span data-ttu-id="5707d-158">La configuración de la regla que se evalúa cuando un usuario intenta agregar una asignación de rol optan.</span><span class="sxs-lookup"><span data-stu-id="5707d-158">The rule settings that are evaluated when a user tries to add an eligible role assignment.</span></span> <span data-ttu-id="5707d-159">No se admite la configuración por ahora.</span><span class="sxs-lookup"><span data-stu-id="5707d-159">The setting is not supported for now.</span></span>|
|<span data-ttu-id="5707d-160">userMemberSettings</span><span class="sxs-lookup"><span data-stu-id="5707d-160">userMemberSettings</span></span>   |<span data-ttu-id="5707d-161">colección de [governanceRuleSetting](../resources/governancerulesetting.md)</span><span class="sxs-lookup"><span data-stu-id="5707d-161">[governanceRuleSetting](../resources/governancerulesetting.md) collection</span></span>|<span data-ttu-id="5707d-162">La configuración de la regla que se evalúa cuando un usuario intenta activar su asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="5707d-162">The rule settings that are evaluated when a user tries to activate his role assignment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="5707d-163">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5707d-163">Relationships</span></span>
| <span data-ttu-id="5707d-164">Relación</span><span class="sxs-lookup"><span data-stu-id="5707d-164">Relationship</span></span> | <span data-ttu-id="5707d-165">Tipo</span><span class="sxs-lookup"><span data-stu-id="5707d-165">Type</span></span>   |<span data-ttu-id="5707d-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="5707d-166">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5707d-167">resource</span><span class="sxs-lookup"><span data-stu-id="5707d-167">resource</span></span>|[<span data-ttu-id="5707d-168">governanceResource</span><span class="sxs-lookup"><span data-stu-id="5707d-168">governanceResource</span></span>](../resources/governanceresource.md)|<span data-ttu-id="5707d-169">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5707d-169">Read-only.</span></span> <span data-ttu-id="5707d-170">El recurso asociado para esta configuración de rol.</span><span class="sxs-lookup"><span data-stu-id="5707d-170">The associated resource for this role setting.</span></span>|
|<span data-ttu-id="5707d-171">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="5707d-171">roleDefinition</span></span>|[<span data-ttu-id="5707d-172">governanceRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5707d-172">governanceRoleDefinition</span></span>](../resources/governanceroledefinition.md)|<span data-ttu-id="5707d-173">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5707d-173">Read-only.</span></span> <span data-ttu-id="5707d-174">La definición de roles que se aplica con esta configuración de rol.</span><span class="sxs-lookup"><span data-stu-id="5707d-174">The role definition that is enforced with this role setting.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="5707d-175">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5707d-175">JSON representation</span></span>

<span data-ttu-id="5707d-176">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5707d-176">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceRoleSetting"
}-->

```json
{
  "id": "String (identifier)",
  "resourceId": "String",
  "roleDefinitionId": "String",
  "isDefault": true,
  "lastUpdatedDateTime": "String (timestamp)",
  "lastUpdatedBy": "String",
  "adminEligibleSettings": [{"@odata.type": "microsoft.graph.governanceRuleSetting"}],
  "adminMemberSettings": [{"@odata.type": "microsoft.graph.governanceRuleSetting"}],
  "userEligibleSettings": [{"@odata.type": "microsoft.graph.governanceRuleSetting"}],
  "userMemberSettings": [{"@odata.type": "microsoft.graph.governanceRuleSetting"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceRoleSetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
