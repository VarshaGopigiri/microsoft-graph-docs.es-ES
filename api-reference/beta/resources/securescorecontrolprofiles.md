---
title: tipo de recurso secureScoreControlProfiles
description: Representa la puntuación de seguro de un inquilino por los datos del control. De forma predeterminada, devuelve todos los controles de un inquilino y puede extraer explícitamente los controles individuales.
ms.openlocfilehash: e02c9ae3b1431b131576e2e0e115377dd3480bc2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088546"
---
# <a name="securescorecontrolprofiles-resource-type"></a><span data-ttu-id="5dc3c-104">tipo de recurso secureScoreControlProfiles</span><span class="sxs-lookup"><span data-stu-id="5dc3c-104">secureScoreControlProfiles resource type</span></span>

> <span data-ttu-id="5dc3c-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5dc3c-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5dc3c-107">Representa la puntuación de seguro de un inquilino por los datos del control.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-107">Represents a tenant's secure score per control data.</span></span> <span data-ttu-id="5dc3c-108">De forma predeterminada, devuelve todos los controles de un inquilino y puede extraer explícitamente los controles individuales.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-108">By default, it returns all controls for a tenant and can explicitly pull individual controls.</span></span>


## <a name="methods"></a><span data-ttu-id="5dc3c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5dc3c-109">Methods</span></span>

| <span data-ttu-id="5dc3c-110">Método</span><span class="sxs-lookup"><span data-stu-id="5dc3c-110">Method</span></span>   | <span data-ttu-id="5dc3c-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5dc3c-111">Return Type</span></span>|<span data-ttu-id="5dc3c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5dc3c-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="5dc3c-113">Lista secureScoreControlProfiles</span><span class="sxs-lookup"><span data-stu-id="5dc3c-113">List secureScoreControlProfiles</span></span>](../api/securescorecontrolprofiles-list.md) | [<span data-ttu-id="5dc3c-114">secureScoreControlProfiles</span><span class="sxs-lookup"><span data-stu-id="5dc3c-114">secureScoreControlProfiles</span></span>](securescorecontrolprofiles.md) |<span data-ttu-id="5dc3c-115">Lea las propiedades y los metadatos de un objeto secureScoreControlProfiles.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-115">Read properties and metadata of a secureScoreControlProfiles object.</span></span>|


## <a name="properties"></a><span data-ttu-id="5dc3c-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5dc3c-116">Properties</span></span>

|<span data-ttu-id="5dc3c-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="5dc3c-117">Name</span></span> |<span data-ttu-id="5dc3c-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="5dc3c-118">Type</span></span> |<span data-ttu-id="5dc3c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5dc3c-119">Description</span></span> |
|:--|:--|:--|
|   <span data-ttu-id="5dc3c-120">azureTenantId</span><span class="sxs-lookup"><span data-stu-id="5dc3c-120">azureTenantId</span></span>   |   <span data-ttu-id="5dc3c-121">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-121">String</span></span>  |   <span data-ttu-id="5dc3c-122">Identificador de cadena GUID para el inquilino.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-122">GUID string for tenant ID.</span></span>  |
|   <span data-ttu-id="5dc3c-123">controlName</span><span class="sxs-lookup"><span data-stu-id="5dc3c-123">controlName</span></span> |   <span data-ttu-id="5dc3c-124">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-124">String</span></span>  |   <span data-ttu-id="5dc3c-125">Nombre del control.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-125">Name of the control.</span></span> |
|   <span data-ttu-id="5dc3c-126">title</span><span class="sxs-lookup"><span data-stu-id="5dc3c-126">title</span></span>   |   <span data-ttu-id="5dc3c-127">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-127">String</span></span>  |   <span data-ttu-id="5dc3c-128">Título del control.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-128">Title of the control.</span></span>   |
|   <span data-ttu-id="5dc3c-129">controlCategory</span><span class="sxs-lookup"><span data-stu-id="5dc3c-129">controlCategory</span></span> |   <span data-ttu-id="5dc3c-130">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-130">String</span></span>  |   <span data-ttu-id="5dc3c-131">Categoría de acción de control (cuenta, datos, dispositivos, aplicaciones, infraestructura).</span><span class="sxs-lookup"><span data-stu-id="5dc3c-131">Control action category (Account, Data, Device, Apps, Infrastructure).</span></span>  |
|   <span data-ttu-id="5dc3c-132">actionType</span><span class="sxs-lookup"><span data-stu-id="5dc3c-132">actionType</span></span>  |   <span data-ttu-id="5dc3c-133">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-133">String</span></span>  |   <span data-ttu-id="5dc3c-134">Controlar el tipo de acción (Config, revisión, comportamiento).</span><span class="sxs-lookup"><span data-stu-id="5dc3c-134">Control action type (Config, Review, Behavior).</span></span> |
|   <span data-ttu-id="5dc3c-135">service</span><span class="sxs-lookup"><span data-stu-id="5dc3c-135">service</span></span> |   <span data-ttu-id="5dc3c-136">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-136">String</span></span>  |   <span data-ttu-id="5dc3c-137">Servicio que posee el control (Exchange, Sharepoint, Azure AD).</span><span class="sxs-lookup"><span data-stu-id="5dc3c-137">Service that owns the control (Exchange, Sharepoint, Azure AD).</span></span> |
|   <span data-ttu-id="5dc3c-138">maxScore</span><span class="sxs-lookup"><span data-stu-id="5dc3c-138">maxScore</span></span> |  <span data-ttu-id="5dc3c-139">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-139">String</span></span>  |   <span data-ttu-id="5dc3c-140">Actual había obtenido puntuación máxima en la fecha especificada.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-140">Current obtained max score on specified date.</span></span>   |
|   <span data-ttu-id="5dc3c-141">nivel</span><span class="sxs-lookup"><span data-stu-id="5dc3c-141">tier</span></span> |  <span data-ttu-id="5dc3c-142">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-142">String</span></span>  |   <span data-ttu-id="5dc3c-143">Nivel de control (doble núcleo, la estrategia de defensa en profundidad, avanzada.)</span><span class="sxs-lookup"><span data-stu-id="5dc3c-143">Control tier (Core, Defense in Depth, Advanced.)</span></span>    |
|   <span data-ttu-id="5dc3c-144">userImpact</span><span class="sxs-lookup"><span data-stu-id="5dc3c-144">userImpact</span></span> |    <span data-ttu-id="5dc3c-145">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-145">String</span></span>  | <span data-ttu-id="5dc3c-146">Impacto de usuario de la implementación de control (bajo, moderado, alta).</span><span class="sxs-lookup"><span data-stu-id="5dc3c-146">User impact of implementing control (low, moderate, high).</span></span>    |
|   <span data-ttu-id="5dc3c-147">implementationCost</span><span class="sxs-lookup"><span data-stu-id="5dc3c-147">implementationCost</span></span> |    <span data-ttu-id="5dc3c-148">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-148">String</span></span>  |   <span data-ttu-id="5dc3c-149">Costo de recurso de control de implemmentating (bajo, moderado, alta).</span><span class="sxs-lookup"><span data-stu-id="5dc3c-149">Resource cost of implemmentating control (low, moderate, high).</span></span> |
|   <span data-ttu-id="5dc3c-150">rank</span><span class="sxs-lookup"><span data-stu-id="5dc3c-150">rank</span></span> |  <span data-ttu-id="5dc3c-151">Int32</span><span class="sxs-lookup"><span data-stu-id="5dc3c-151">Int32</span></span>   |   <span data-ttu-id="5dc3c-152">Pila de Microsoft de clasificación de control.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-152">Microsoft's stack ranking of control.</span></span>   |
|   <span data-ttu-id="5dc3c-153">amenazas</span><span class="sxs-lookup"><span data-stu-id="5dc3c-153">threats</span></span> |   <span data-ttu-id="5dc3c-154">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="5dc3c-154">String Collection</span></span>   |   <span data-ttu-id="5dc3c-155">Lista de las amenazas que mitiga el control (accountBreach, dataDeletion, dataExfiltration, dataSpillage, elevationOfPrivilege, maliciousInsider, passwordCracking, phishingOrWhaling, suplantación de identidad).</span><span class="sxs-lookup"><span data-stu-id="5dc3c-155">List of threats the control mitigates (accountBreach,dataDeletion,dataExfiltration,dataSpillage,elevationOfPrivilege,maliciousInsider,passwordCracking,phishingOrWhaling,spoofing).</span></span> |
|   <span data-ttu-id="5dc3c-156">en desuso</span><span class="sxs-lookup"><span data-stu-id="5dc3c-156">deprecated</span></span> |    <span data-ttu-id="5dc3c-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="5dc3c-157">Boolean</span></span> |   <span data-ttu-id="5dc3c-158">Marcar para indicar si se ha eliminado un control.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-158">Flag to indicate if a control is depreciated.</span></span>   |
|   <span data-ttu-id="5dc3c-159">corrección</span><span class="sxs-lookup"><span data-stu-id="5dc3c-159">remediation</span></span> |   <span data-ttu-id="5dc3c-160">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-160">String</span></span>  |   <span data-ttu-id="5dc3c-161">Descripción de lo que el control le ayudará a corregir.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-161">Description of what the control will help remediate.</span></span> |
|   <span data-ttu-id="5dc3c-162">remediationImpact</span><span class="sxs-lookup"><span data-stu-id="5dc3c-162">remediationImpact</span></span> | <span data-ttu-id="5dc3c-163">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-163">String</span></span>  |   <span data-ttu-id="5dc3c-164">Descripción del impacto en los usuarios de la corrección.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-164">Description of the impact on users of the remediation.</span></span> |
|   <span data-ttu-id="5dc3c-165">actionUrl</span><span class="sxs-lookup"><span data-stu-id="5dc3c-165">actionUrl</span></span> | <span data-ttu-id="5dc3c-166">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-166">String</span></span>  |   <span data-ttu-id="5dc3c-167">Dirección URL donde el control puede ser ejecutado.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-167">URL to where the control can be actioned.</span></span> |
|   <span data-ttu-id="5dc3c-168">controlStateUpdates</span><span class="sxs-lookup"><span data-stu-id="5dc3c-168">controlStateUpdates</span></span> |   <span data-ttu-id="5dc3c-169">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-169">String</span></span>  |   <span data-ttu-id="5dc3c-170">Marca para indicar que el inquilino ha marcado un control (omitir, otros, revisado) (admite [Actualizar](../api/securescorecontrolprofiles-update.md)).</span><span class="sxs-lookup"><span data-stu-id="5dc3c-170">Flag to indicate where the tenant has marked a control (ignore, thirdParty, reviewed) (supports [update](../api/securescorecontrolprofiles-update.md)).</span></span> |
|   <span data-ttu-id="5dc3c-171">tenantNote</span><span class="sxs-lookup"><span data-stu-id="5dc3c-171">tenantNote</span></span> |    <span data-ttu-id="5dc3c-172">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-172">String</span></span>  |   <span data-ttu-id="5dc3c-173">Puede establecer el inquilino por los comentarios de control (admite [Actualizar](../api/securescorecontrolprofiles-update.md)).</span><span class="sxs-lookup"><span data-stu-id="5dc3c-173">Tenant can set per control comments (supports [update](../api/securescorecontrolprofiles-update.md)).</span></span> |
|   <span data-ttu-id="5dc3c-174">assignedTo</span><span class="sxs-lookup"><span data-stu-id="5dc3c-174">assignedTo</span></span> |    <span data-ttu-id="5dc3c-175">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-175">String</span></span>  |   <span data-ttu-id="5dc3c-176">Inquilino puede asignar el control a un individuo (admite [Actualizar](../api/securescorecontrolprofiles-update.md)).</span><span class="sxs-lookup"><span data-stu-id="5dc3c-176">Tenant can assign the control to a individual (supports [update](../api/securescorecontrolprofiles-update.md)).</span></span> |
|   <span data-ttu-id="5dc3c-177">updatedBy</span><span class="sxs-lookup"><span data-stu-id="5dc3c-177">updatedBy</span></span> | <span data-ttu-id="5dc3c-178">String</span><span class="sxs-lookup"><span data-stu-id="5dc3c-178">String</span></span>  |   <span data-ttu-id="5dc3c-179">Nombre principal de usuario de quién realizó cambios en el estado de un control.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-179">User principal name of who made changes to a control's state.</span></span> |

## <a name="relationships"></a><span data-ttu-id="5dc3c-180">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5dc3c-180">Relationships</span></span>

<span data-ttu-id="5dc3c-181">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5dc3c-181">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="5dc3c-182">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5dc3c-182">JSON representation</span></span>

<span data-ttu-id="5dc3c-183">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5dc3c-183">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.secureScores"
}-->

```json
{
"title": "String", 
"azureTenantId": "Guid", 
"referenceId": "String", 
"controlName": "String", 
"maxScore": "Int32",
"actionCategory": "Collection(microsoft.graph.SecureScore.actionCategory)",
"actionType": "Collection(microsoft.graph.SecureScore.actionType)",
"service": "String",
"tier": "Collection(microsoft.graph.SecureScore.tier)",
"userImpact": "Collection(microsoft.graph.SecureScore.ranking)",
"implementationCost ": "Collection(microsoft.graph.SecureScore.ranking)",
"rank ": "Int32",
"threats": "Collection(microsoft.graph.SecureScore.threat)",
"deprecated ": "Boolean",
"remediation": "String",
"remediationImpact ": "String",
"actionUrl": "String",
"controlStateUpdates": "Collection(microsoft.graph.SecureScore.controlStateUpdates)",
"tenantNotes": "String",
"upn": "String",
"comments": "String",
}


```


<!-- {
  "type": "#page.annotation",
  "description": "secureScoreControlProfiles resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
