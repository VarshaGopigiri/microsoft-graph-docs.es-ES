---
title: tipo de recurso secureScoreControlProfiles
description: Representa la puntuación de seguro de un inquilino por los datos del control. De forma predeterminada, devuelve todos los controles de un inquilino y puede extraer explícitamente los controles individuales.
localization_priority: Normal
ms.openlocfilehash: 866b2086ff5160744f848292cedf30c3cedf6daa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866223"
---
# <a name="securescorecontrolprofiles-resource-type"></a><span data-ttu-id="e6884-104">tipo de recurso secureScoreControlProfiles</span><span class="sxs-lookup"><span data-stu-id="e6884-104">secureScoreControlProfiles resource type</span></span>

> <span data-ttu-id="e6884-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e6884-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e6884-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e6884-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e6884-107">Representa la puntuación de seguro de un inquilino por los datos del control.</span><span class="sxs-lookup"><span data-stu-id="e6884-107">Represents a tenant's secure score per control data.</span></span> <span data-ttu-id="e6884-108">De forma predeterminada, devuelve todos los controles de un inquilino y puede extraer explícitamente los controles individuales.</span><span class="sxs-lookup"><span data-stu-id="e6884-108">By default, it returns all controls for a tenant and can explicitly pull individual controls.</span></span>


## <a name="methods"></a><span data-ttu-id="e6884-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6884-109">Methods</span></span>

| <span data-ttu-id="e6884-110">Método</span><span class="sxs-lookup"><span data-stu-id="e6884-110">Method</span></span>   | <span data-ttu-id="e6884-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6884-111">Return Type</span></span>|<span data-ttu-id="e6884-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6884-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e6884-113">Lista secureScoreControlProfiles</span><span class="sxs-lookup"><span data-stu-id="e6884-113">List secureScoreControlProfiles</span></span>](../api/securescorecontrolprofiles-list.md) | [<span data-ttu-id="e6884-114">secureScoreControlProfiles</span><span class="sxs-lookup"><span data-stu-id="e6884-114">secureScoreControlProfiles</span></span>](securescorecontrolprofiles.md) |<span data-ttu-id="e6884-115">Lea las propiedades y los metadatos de un objeto secureScoreControlProfiles.</span><span class="sxs-lookup"><span data-stu-id="e6884-115">Read properties and metadata of a secureScoreControlProfiles object.</span></span>|


## <a name="properties"></a><span data-ttu-id="e6884-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e6884-116">Properties</span></span>

|<span data-ttu-id="e6884-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="e6884-117">Name</span></span> |<span data-ttu-id="e6884-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6884-118">Type</span></span> |<span data-ttu-id="e6884-119">Description</span><span class="sxs-lookup"><span data-stu-id="e6884-119">Description</span></span> |
|:--|:--|:--|
|   <span data-ttu-id="e6884-120">azureTenantId</span><span class="sxs-lookup"><span data-stu-id="e6884-120">azureTenantId</span></span>   |   <span data-ttu-id="e6884-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6884-121">String</span></span>  |   <span data-ttu-id="e6884-122">Identificador de cadena GUID para el inquilino.</span><span class="sxs-lookup"><span data-stu-id="e6884-122">GUID string for tenant ID.</span></span>  |
|   <span data-ttu-id="e6884-123">controlName</span><span class="sxs-lookup"><span data-stu-id="e6884-123">controlName</span></span> |   <span data-ttu-id="e6884-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6884-124">String</span></span>  |   <span data-ttu-id="e6884-125">Nombre del control.</span><span class="sxs-lookup"><span data-stu-id="e6884-125">Name of the control.</span></span> |
|   <span data-ttu-id="e6884-126">title</span><span class="sxs-lookup"><span data-stu-id="e6884-126">title</span></span>   |   <span data-ttu-id="e6884-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6884-127">String</span></span>  |   <span data-ttu-id="e6884-128">Título del control.</span><span class="sxs-lookup"><span data-stu-id="e6884-128">Title of the control.</span></span>   |
| <span data-ttu-id="e6884-129">complianceInformation</span><span class="sxs-lookup"><span data-stu-id="e6884-129">complianceInformation</span></span> | <span data-ttu-id="e6884-130">colección de [complianceInformation](complianceinformation.md)</span><span class="sxs-lookup"><span data-stu-id="e6884-130">[complianceInformation](complianceinformation.md) collection</span></span> | <span data-ttu-id="e6884-131">La recopilación de información de cumplimiento de normas asociado con garantizar el control de puntuación</span><span class="sxs-lookup"><span data-stu-id="e6884-131">The collection of compliance information associated with secure score control</span></span> |
|   <span data-ttu-id="e6884-132">controlCategory</span><span class="sxs-lookup"><span data-stu-id="e6884-132">controlCategory</span></span> |   <span data-ttu-id="e6884-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6884-133">String</span></span>  |   <span data-ttu-id="e6884-134">Categoría de acción de control (cuenta, datos, dispositivos, aplicaciones, infraestructura).</span><span class="sxs-lookup"><span data-stu-id="e6884-134">Control action category (Account, Data, Device, Apps, Infrastructure).</span></span>  |
|   <span data-ttu-id="e6884-135">actionType</span><span class="sxs-lookup"><span data-stu-id="e6884-135">actionType</span></span>  |   <span data-ttu-id="e6884-136">String</span><span class="sxs-lookup"><span data-stu-id="e6884-136">String</span></span>  |   <span data-ttu-id="e6884-137">Controlar el tipo de acción (Config, revisión, comportamiento).</span><span class="sxs-lookup"><span data-stu-id="e6884-137">Control action type (Config, Review, Behavior).</span></span> |
|   <span data-ttu-id="e6884-138">service</span><span class="sxs-lookup"><span data-stu-id="e6884-138">service</span></span> |   <span data-ttu-id="e6884-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6884-139">String</span></span>  |   <span data-ttu-id="e6884-140">Servicio que posee el control (Exchange, Sharepoint, Azure AD).</span><span class="sxs-lookup"><span data-stu-id="e6884-140">Service that owns the control (Exchange, Sharepoint, Azure AD).</span></span> |
|   <span data-ttu-id="e6884-141">maxScore</span><span class="sxs-lookup"><span data-stu-id="e6884-141">maxScore</span></span> |  <span data-ttu-id="e6884-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6884-142">String</span></span>  |   <span data-ttu-id="e6884-143">Actual había obtenido puntuación máxima en la fecha especificada.</span><span class="sxs-lookup"><span data-stu-id="e6884-143">Current obtained max score on specified date.</span></span>   |
|   <span data-ttu-id="e6884-144">nivel</span><span class="sxs-lookup"><span data-stu-id="e6884-144">tier</span></span> |  <span data-ttu-id="e6884-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6884-145">String</span></span>  |   <span data-ttu-id="e6884-146">Nivel de control (doble núcleo, la estrategia de defensa en profundidad, avanzada.)</span><span class="sxs-lookup"><span data-stu-id="e6884-146">Control tier (Core, Defense in Depth, Advanced.)</span></span>    |
|   <span data-ttu-id="e6884-147">userImpact</span><span class="sxs-lookup"><span data-stu-id="e6884-147">userImpact</span></span> |    <span data-ttu-id="e6884-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6884-148">String</span></span>  | <span data-ttu-id="e6884-149">Impacto de usuario de la implementación de control (bajo, moderado, alta).</span><span class="sxs-lookup"><span data-stu-id="e6884-149">User impact of implementing control (low, moderate, high).</span></span>    |
|   <span data-ttu-id="e6884-150">implementationCost</span><span class="sxs-lookup"><span data-stu-id="e6884-150">implementationCost</span></span> |    <span data-ttu-id="e6884-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6884-151">String</span></span>  |   <span data-ttu-id="e6884-152">Costo de recurso de control de implemmentating (bajo, moderado, alta).</span><span class="sxs-lookup"><span data-stu-id="e6884-152">Resource cost of implemmentating control (low, moderate, high).</span></span> |
|   <span data-ttu-id="e6884-153">rank</span><span class="sxs-lookup"><span data-stu-id="e6884-153">rank</span></span> |  <span data-ttu-id="e6884-154">Int32</span><span class="sxs-lookup"><span data-stu-id="e6884-154">Int32</span></span>   |   <span data-ttu-id="e6884-155">Pila de Microsoft de clasificación de control.</span><span class="sxs-lookup"><span data-stu-id="e6884-155">Microsoft's stack ranking of control.</span></span>   |
|   <span data-ttu-id="e6884-156">amenazas</span><span class="sxs-lookup"><span data-stu-id="e6884-156">threats</span></span> |   <span data-ttu-id="e6884-157">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="e6884-157">String Collection</span></span>   |   <span data-ttu-id="e6884-158">Lista de las amenazas que mitiga el control (accountBreach, dataDeletion, dataExfiltration, dataSpillage, elevationOfPrivilege, maliciousInsider, passwordCracking, phishingOrWhaling, suplantación de identidad).</span><span class="sxs-lookup"><span data-stu-id="e6884-158">List of threats the control mitigates (accountBreach,dataDeletion,dataExfiltration,dataSpillage,elevationOfPrivilege,maliciousInsider,passwordCracking,phishingOrWhaling,spoofing).</span></span> |
|   <span data-ttu-id="e6884-159">en desuso</span><span class="sxs-lookup"><span data-stu-id="e6884-159">deprecated</span></span> |    <span data-ttu-id="e6884-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="e6884-160">Boolean</span></span> |   <span data-ttu-id="e6884-161">Marcar para indicar si se ha eliminado un control.</span><span class="sxs-lookup"><span data-stu-id="e6884-161">Flag to indicate if a control is depreciated.</span></span>   |
|   <span data-ttu-id="e6884-162">corrección</span><span class="sxs-lookup"><span data-stu-id="e6884-162">remediation</span></span> |   <span data-ttu-id="e6884-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6884-163">String</span></span>  |   <span data-ttu-id="e6884-164">Descripción de lo que el control le ayudará a corregir.</span><span class="sxs-lookup"><span data-stu-id="e6884-164">Description of what the control will help remediate.</span></span> |
|   <span data-ttu-id="e6884-165">remediationImpact</span><span class="sxs-lookup"><span data-stu-id="e6884-165">remediationImpact</span></span> | <span data-ttu-id="e6884-166">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6884-166">String</span></span>  |   <span data-ttu-id="e6884-167">Descripción del impacto en los usuarios de la corrección.</span><span class="sxs-lookup"><span data-stu-id="e6884-167">Description of the impact on users of the remediation.</span></span> |
|   <span data-ttu-id="e6884-168">actionUrl</span><span class="sxs-lookup"><span data-stu-id="e6884-168">actionUrl</span></span> | <span data-ttu-id="e6884-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6884-169">String</span></span>  |   <span data-ttu-id="e6884-170">Dirección URL donde el control puede ser ejecutado.</span><span class="sxs-lookup"><span data-stu-id="e6884-170">URL to where the control can be actioned.</span></span> |
|   <span data-ttu-id="e6884-171">controlStateUpdates</span><span class="sxs-lookup"><span data-stu-id="e6884-171">controlStateUpdates</span></span> |   <span data-ttu-id="e6884-172">colección de [secureScoreControlStateUpdate](securescorecontrolstateupdate.md)</span><span class="sxs-lookup"><span data-stu-id="e6884-172">[secureScoreControlStateUpdate](securescorecontrolstateupdate.md)   collection</span></span> |    <span data-ttu-id="e6884-173">Marca para indicar que el inquilino ha marcado un control (omitir, otros, revisado) (admite [Actualizar](../api/securescorecontrolprofiles-update.md)).</span><span class="sxs-lookup"><span data-stu-id="e6884-173">Flag to indicate where the tenant has marked a control (ignore, thirdParty, reviewed) (supports [update](../api/securescorecontrolprofiles-update.md)).</span></span> |

## <a name="relationships"></a><span data-ttu-id="e6884-174">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e6884-174">Relationships</span></span>

<span data-ttu-id="e6884-175">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e6884-175">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e6884-176">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e6884-176">JSON representation</span></span>

<span data-ttu-id="e6884-177">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e6884-177">The following is a JSON representation of the resource.</span></span>

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
