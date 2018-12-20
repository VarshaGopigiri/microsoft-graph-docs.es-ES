---
title: tipo de recurso secureScoreControlProfiles
description: Representa la puntuación de seguro de un inquilino por los datos del control. De forma predeterminada, devuelve todos los controles de un inquilino y puede extraer explícitamente los controles individuales.
ms.openlocfilehash: 3e7dc463d7521e1980b41034ae4121ab610dd8f5
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380586"
---
# <a name="securescorecontrolprofiles-resource-type"></a><span data-ttu-id="faa6d-104">tipo de recurso secureScoreControlProfiles</span><span class="sxs-lookup"><span data-stu-id="faa6d-104">secureScoreControlProfiles resource type</span></span>

> <span data-ttu-id="faa6d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="faa6d-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="faa6d-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="faa6d-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="faa6d-107">Representa la puntuación de seguro de un inquilino por los datos del control.</span><span class="sxs-lookup"><span data-stu-id="faa6d-107">Represents a tenant's secure score per control data.</span></span> <span data-ttu-id="faa6d-108">De forma predeterminada, devuelve todos los controles de un inquilino y puede extraer explícitamente los controles individuales.</span><span class="sxs-lookup"><span data-stu-id="faa6d-108">By default, it returns all controls for a tenant and can explicitly pull individual controls.</span></span>


## <a name="methods"></a><span data-ttu-id="faa6d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="faa6d-109">Methods</span></span>

| <span data-ttu-id="faa6d-110">Método</span><span class="sxs-lookup"><span data-stu-id="faa6d-110">Method</span></span>   | <span data-ttu-id="faa6d-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="faa6d-111">Return Type</span></span>|<span data-ttu-id="faa6d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="faa6d-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="faa6d-113">Lista secureScoreControlProfiles</span><span class="sxs-lookup"><span data-stu-id="faa6d-113">List secureScoreControlProfiles</span></span>](../api/securescorecontrolprofiles-list.md) | [<span data-ttu-id="faa6d-114">secureScoreControlProfiles</span><span class="sxs-lookup"><span data-stu-id="faa6d-114">secureScoreControlProfiles</span></span>](securescorecontrolprofiles.md) |<span data-ttu-id="faa6d-115">Lea las propiedades y los metadatos de un objeto secureScoreControlProfiles.</span><span class="sxs-lookup"><span data-stu-id="faa6d-115">Read properties and metadata of a secureScoreControlProfiles object.</span></span>|


## <a name="properties"></a><span data-ttu-id="faa6d-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="faa6d-116">Properties</span></span>

|<span data-ttu-id="faa6d-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="faa6d-117">Name</span></span> |<span data-ttu-id="faa6d-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="faa6d-118">Type</span></span> |<span data-ttu-id="faa6d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="faa6d-119">Description</span></span> |
|:--|:--|:--|
|   <span data-ttu-id="faa6d-120">azureTenantId</span><span class="sxs-lookup"><span data-stu-id="faa6d-120">azureTenantId</span></span>   |   <span data-ttu-id="faa6d-121">String</span><span class="sxs-lookup"><span data-stu-id="faa6d-121">String</span></span>  |   <span data-ttu-id="faa6d-122">Identificador de cadena GUID para el inquilino.</span><span class="sxs-lookup"><span data-stu-id="faa6d-122">GUID string for tenant ID.</span></span>  |
|   <span data-ttu-id="faa6d-123">controlName</span><span class="sxs-lookup"><span data-stu-id="faa6d-123">controlName</span></span> |   <span data-ttu-id="faa6d-124">String</span><span class="sxs-lookup"><span data-stu-id="faa6d-124">String</span></span>  |   <span data-ttu-id="faa6d-125">Nombre del control.</span><span class="sxs-lookup"><span data-stu-id="faa6d-125">Name of the control.</span></span> |
|   <span data-ttu-id="faa6d-126">title</span><span class="sxs-lookup"><span data-stu-id="faa6d-126">title</span></span>   |   <span data-ttu-id="faa6d-127">String</span><span class="sxs-lookup"><span data-stu-id="faa6d-127">String</span></span>  |   <span data-ttu-id="faa6d-128">Título del control.</span><span class="sxs-lookup"><span data-stu-id="faa6d-128">Title of the control.</span></span>   |
| <span data-ttu-id="faa6d-129">complianceInformation</span><span class="sxs-lookup"><span data-stu-id="faa6d-129">complianceInformation</span></span> | <span data-ttu-id="faa6d-130">colección de [complianceInformation](complianceinformation.md)</span><span class="sxs-lookup"><span data-stu-id="faa6d-130">[complianceInformation](complianceinformation.md) collection</span></span> | <span data-ttu-id="faa6d-131">La recopilación de información de cumplimiento de normas asociado con garantizar el control de puntuación</span><span class="sxs-lookup"><span data-stu-id="faa6d-131">The collection of compliance information associated with secure score control</span></span> |
|   <span data-ttu-id="faa6d-132">controlCategory</span><span class="sxs-lookup"><span data-stu-id="faa6d-132">controlCategory</span></span> |   <span data-ttu-id="faa6d-133">String</span><span class="sxs-lookup"><span data-stu-id="faa6d-133">String</span></span>  |   <span data-ttu-id="faa6d-134">Categoría de acción de control (cuenta, datos, dispositivos, aplicaciones, infraestructura).</span><span class="sxs-lookup"><span data-stu-id="faa6d-134">Control action category (Account, Data, Device, Apps, Infrastructure).</span></span>  |
|   <span data-ttu-id="faa6d-135">actionType</span><span class="sxs-lookup"><span data-stu-id="faa6d-135">actionType</span></span>  |   <span data-ttu-id="faa6d-136">String</span><span class="sxs-lookup"><span data-stu-id="faa6d-136">String</span></span>  |   <span data-ttu-id="faa6d-137">Controlar el tipo de acción (Config, revisión, comportamiento).</span><span class="sxs-lookup"><span data-stu-id="faa6d-137">Control action type (Config, Review, Behavior).</span></span> |
|   <span data-ttu-id="faa6d-138">service</span><span class="sxs-lookup"><span data-stu-id="faa6d-138">service</span></span> |   <span data-ttu-id="faa6d-139">String</span><span class="sxs-lookup"><span data-stu-id="faa6d-139">String</span></span>  |   <span data-ttu-id="faa6d-140">Servicio que posee el control (Exchange, Sharepoint, Azure AD).</span><span class="sxs-lookup"><span data-stu-id="faa6d-140">Service that owns the control (Exchange, Sharepoint, Azure AD).</span></span> |
|   <span data-ttu-id="faa6d-141">maxScore</span><span class="sxs-lookup"><span data-stu-id="faa6d-141">maxScore</span></span> |  <span data-ttu-id="faa6d-142">String</span><span class="sxs-lookup"><span data-stu-id="faa6d-142">String</span></span>  |   <span data-ttu-id="faa6d-143">Actual había obtenido puntuación máxima en la fecha especificada.</span><span class="sxs-lookup"><span data-stu-id="faa6d-143">Current obtained max score on specified date.</span></span>   |
|   <span data-ttu-id="faa6d-144">nivel</span><span class="sxs-lookup"><span data-stu-id="faa6d-144">tier</span></span> |  <span data-ttu-id="faa6d-145">String</span><span class="sxs-lookup"><span data-stu-id="faa6d-145">String</span></span>  |   <span data-ttu-id="faa6d-146">Nivel de control (doble núcleo, la estrategia de defensa en profundidad, avanzada.)</span><span class="sxs-lookup"><span data-stu-id="faa6d-146">Control tier (Core, Defense in Depth, Advanced.)</span></span>    |
|   <span data-ttu-id="faa6d-147">userImpact</span><span class="sxs-lookup"><span data-stu-id="faa6d-147">userImpact</span></span> |    <span data-ttu-id="faa6d-148">String</span><span class="sxs-lookup"><span data-stu-id="faa6d-148">String</span></span>  | <span data-ttu-id="faa6d-149">Impacto de usuario de la implementación de control (bajo, moderado, alta).</span><span class="sxs-lookup"><span data-stu-id="faa6d-149">User impact of implementing control (low, moderate, high).</span></span>    |
|   <span data-ttu-id="faa6d-150">implementationCost</span><span class="sxs-lookup"><span data-stu-id="faa6d-150">implementationCost</span></span> |    <span data-ttu-id="faa6d-151">String</span><span class="sxs-lookup"><span data-stu-id="faa6d-151">String</span></span>  |   <span data-ttu-id="faa6d-152">Costo de recurso de control de implemmentating (bajo, moderado, alta).</span><span class="sxs-lookup"><span data-stu-id="faa6d-152">Resource cost of implemmentating control (low, moderate, high).</span></span> |
|   <span data-ttu-id="faa6d-153">rank</span><span class="sxs-lookup"><span data-stu-id="faa6d-153">rank</span></span> |  <span data-ttu-id="faa6d-154">Int32</span><span class="sxs-lookup"><span data-stu-id="faa6d-154">Int32</span></span>   |   <span data-ttu-id="faa6d-155">Pila de Microsoft de clasificación de control.</span><span class="sxs-lookup"><span data-stu-id="faa6d-155">Microsoft's stack ranking of control.</span></span>   |
|   <span data-ttu-id="faa6d-156">amenazas</span><span class="sxs-lookup"><span data-stu-id="faa6d-156">threats</span></span> |   <span data-ttu-id="faa6d-157">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="faa6d-157">String Collection</span></span>   |   <span data-ttu-id="faa6d-158">Lista de las amenazas que mitiga el control (accountBreach, dataDeletion, dataExfiltration, dataSpillage, elevationOfPrivilege, maliciousInsider, passwordCracking, phishingOrWhaling, suplantación de identidad).</span><span class="sxs-lookup"><span data-stu-id="faa6d-158">List of threats the control mitigates (accountBreach,dataDeletion,dataExfiltration,dataSpillage,elevationOfPrivilege,maliciousInsider,passwordCracking,phishingOrWhaling,spoofing).</span></span> |
|   <span data-ttu-id="faa6d-159">en desuso</span><span class="sxs-lookup"><span data-stu-id="faa6d-159">deprecated</span></span> |    <span data-ttu-id="faa6d-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="faa6d-160">Boolean</span></span> |   <span data-ttu-id="faa6d-161">Marcar para indicar si se ha eliminado un control.</span><span class="sxs-lookup"><span data-stu-id="faa6d-161">Flag to indicate if a control is depreciated.</span></span>   |
|   <span data-ttu-id="faa6d-162">corrección</span><span class="sxs-lookup"><span data-stu-id="faa6d-162">remediation</span></span> |   <span data-ttu-id="faa6d-163">String</span><span class="sxs-lookup"><span data-stu-id="faa6d-163">String</span></span>  |   <span data-ttu-id="faa6d-164">Descripción de lo que el control le ayudará a corregir.</span><span class="sxs-lookup"><span data-stu-id="faa6d-164">Description of what the control will help remediate.</span></span> |
|   <span data-ttu-id="faa6d-165">remediationImpact</span><span class="sxs-lookup"><span data-stu-id="faa6d-165">remediationImpact</span></span> | <span data-ttu-id="faa6d-166">String</span><span class="sxs-lookup"><span data-stu-id="faa6d-166">String</span></span>  |   <span data-ttu-id="faa6d-167">Descripción del impacto en los usuarios de la corrección.</span><span class="sxs-lookup"><span data-stu-id="faa6d-167">Description of the impact on users of the remediation.</span></span> |
|   <span data-ttu-id="faa6d-168">actionUrl</span><span class="sxs-lookup"><span data-stu-id="faa6d-168">actionUrl</span></span> | <span data-ttu-id="faa6d-169">String</span><span class="sxs-lookup"><span data-stu-id="faa6d-169">String</span></span>  |   <span data-ttu-id="faa6d-170">Dirección URL donde el control puede ser ejecutado.</span><span class="sxs-lookup"><span data-stu-id="faa6d-170">URL to where the control can be actioned.</span></span> |
|   <span data-ttu-id="faa6d-171">controlStateUpdates</span><span class="sxs-lookup"><span data-stu-id="faa6d-171">controlStateUpdates</span></span> |   <span data-ttu-id="faa6d-172">colección de [secureScoreControlStateUpdate](securescorecontrolstateupdate.md)</span><span class="sxs-lookup"><span data-stu-id="faa6d-172">[secureScoreControlStateUpdate](securescorecontrolstateupdate.md)   collection</span></span> |    <span data-ttu-id="faa6d-173">Marca para indicar que el inquilino ha marcado un control (omitir, otros, revisado) (admite [Actualizar](../api/securescorecontrolprofiles-update.md)).</span><span class="sxs-lookup"><span data-stu-id="faa6d-173">Flag to indicate where the tenant has marked a control (ignore, thirdParty, reviewed) (supports [update](../api/securescorecontrolprofiles-update.md)).</span></span> |

## <a name="relationships"></a><span data-ttu-id="faa6d-174">Relaciones</span><span class="sxs-lookup"><span data-stu-id="faa6d-174">Relationships</span></span>

<span data-ttu-id="faa6d-175">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="faa6d-175">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="faa6d-176">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="faa6d-176">JSON representation</span></span>

<span data-ttu-id="faa6d-177">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="faa6d-177">The following is a JSON representation of the resource.</span></span>

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
