---
title: tipo de recurso privilegedRoleSettings
description: Representa la configuración de un rol con privilegios.
localization_priority: Normal
ms.openlocfilehash: 971c48ce3ecdd2a219a111f3a11884377e20430c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842745"
---
# <a name="privilegedrolesettings-resource-type"></a><span data-ttu-id="708fc-103">tipo de recurso privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="708fc-103">privilegedRoleSettings resource type</span></span>

> <span data-ttu-id="708fc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="708fc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="708fc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="708fc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="708fc-106">Representa la configuración de un rol con privilegios.</span><span class="sxs-lookup"><span data-stu-id="708fc-106">Represents the settings for a privileged role.</span></span>


## <a name="methods"></a><span data-ttu-id="708fc-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="708fc-107">Methods</span></span>

| <span data-ttu-id="708fc-108">Método</span><span class="sxs-lookup"><span data-stu-id="708fc-108">Method</span></span>           | <span data-ttu-id="708fc-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="708fc-109">Return Type</span></span>    |<span data-ttu-id="708fc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="708fc-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="708fc-111">Obtener privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="708fc-111">Get privilegedRoleSettings</span></span>](../api/privilegedrolesettings-get.md) | [<span data-ttu-id="708fc-112">privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="708fc-112">privilegedRoleSettings</span></span>](privilegedrolesettings.md) |<span data-ttu-id="708fc-113">Leer las propiedades y las relaciones del objeto privilegedRoleSettings.</span><span class="sxs-lookup"><span data-stu-id="708fc-113">Read properties and relationships of privilegedRoleSettings object.</span></span>|
|[<span data-ttu-id="708fc-114">Actualizar privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="708fc-114">Update privilegedRoleSettings</span></span>](../api/privilegedrolesettings-update.md) | [<span data-ttu-id="708fc-115">privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="708fc-115">privilegedRoleSettings</span></span>](privilegedrolesettings.md) |<span data-ttu-id="708fc-116">Actualizar el objeto privilegedRoleSettings.</span><span class="sxs-lookup"><span data-stu-id="708fc-116">Update privilegedRoleSettings object.</span></span>|
## <a name="properties"></a><span data-ttu-id="708fc-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="708fc-117">Properties</span></span>
| <span data-ttu-id="708fc-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="708fc-118">Property</span></span>     | <span data-ttu-id="708fc-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="708fc-119">Type</span></span>   |<span data-ttu-id="708fc-120">Description</span><span class="sxs-lookup"><span data-stu-id="708fc-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="708fc-121">elevationDuration</span><span class="sxs-lookup"><span data-stu-id="708fc-121">elevationDuration</span></span>|<span data-ttu-id="708fc-122">duration</span><span class="sxs-lookup"><span data-stu-id="708fc-122">duration</span></span>|<span data-ttu-id="708fc-123">La duración cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="708fc-123">The duration when the role is activated.</span></span>|
|<span data-ttu-id="708fc-124">id</span><span class="sxs-lookup"><span data-stu-id="708fc-124">id</span></span>|<span data-ttu-id="708fc-125">string</span><span class="sxs-lookup"><span data-stu-id="708fc-125">string</span></span>| <span data-ttu-id="708fc-126">El identificador único para la configuración de las funciones.</span><span class="sxs-lookup"><span data-stu-id="708fc-126">The unique identifier for the role settings.</span></span> <span data-ttu-id="708fc-127">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="708fc-127">Read-only.</span></span>|
|<span data-ttu-id="708fc-128">isMfaOnElevationConfigurable</span><span class="sxs-lookup"><span data-stu-id="708fc-128">isMfaOnElevationConfigurable</span></span>|<span data-ttu-id="708fc-129">boolean</span><span class="sxs-lookup"><span data-stu-id="708fc-129">boolean</span></span>|<span data-ttu-id="708fc-130">**true** si mfaOnElevation es configurable.</span><span class="sxs-lookup"><span data-stu-id="708fc-130">**true** if mfaOnElevation is configurable.</span></span> <span data-ttu-id="708fc-131">**false** si no se puede configurar mfaOnElevation.</span><span class="sxs-lookup"><span data-stu-id="708fc-131">**false** if mfaOnElevation is not configurable.</span></span>|
|<span data-ttu-id="708fc-132">lastGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="708fc-132">lastGlobalAdmin</span></span>|<span data-ttu-id="708fc-133">boolean</span><span class="sxs-lookup"><span data-stu-id="708fc-133">boolean</span></span>|<span data-ttu-id="708fc-134">Internal que sólo se utiliza.</span><span class="sxs-lookup"><span data-stu-id="708fc-134">Internal used only.</span></span>|
|<span data-ttu-id="708fc-135">maxElavationDuration</span><span class="sxs-lookup"><span data-stu-id="708fc-135">maxElavationDuration</span></span>|<span data-ttu-id="708fc-136">duration</span><span class="sxs-lookup"><span data-stu-id="708fc-136">duration</span></span>|<span data-ttu-id="708fc-137">Duración máxima de la función activada.</span><span class="sxs-lookup"><span data-stu-id="708fc-137">Maximal duration for the activated role.</span></span>|
|<span data-ttu-id="708fc-138">mfaOnElevation</span><span class="sxs-lookup"><span data-stu-id="708fc-138">mfaOnElevation</span></span>|<span data-ttu-id="708fc-139">boolean</span><span class="sxs-lookup"><span data-stu-id="708fc-139">boolean</span></span>|<span data-ttu-id="708fc-140">**true** si MFA se requiere para activar la función.</span><span class="sxs-lookup"><span data-stu-id="708fc-140">**true** if MFA is required to activate the role.</span></span> <span data-ttu-id="708fc-141">**false** si no es necesario MFA para activar la función.</span><span class="sxs-lookup"><span data-stu-id="708fc-141">**false** if MFA is not required to activate the role.</span></span>|
|<span data-ttu-id="708fc-142">minElevationDuration</span><span class="sxs-lookup"><span data-stu-id="708fc-142">minElevationDuration</span></span>|<span data-ttu-id="708fc-143">duration</span><span class="sxs-lookup"><span data-stu-id="708fc-143">duration</span></span>|<span data-ttu-id="708fc-144">Duración mínima de la función activada.</span><span class="sxs-lookup"><span data-stu-id="708fc-144">Minimal duration for the activated role.</span></span>|
|<span data-ttu-id="708fc-145">notificationToUserOnElevation</span><span class="sxs-lookup"><span data-stu-id="708fc-145">notificationToUserOnElevation</span></span>|<span data-ttu-id="708fc-146">boolean</span><span class="sxs-lookup"><span data-stu-id="708fc-146">boolean</span></span>|<span data-ttu-id="708fc-147">**true** si enviar notificación para el usuario final cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="708fc-147">**true** if send notification to the end user when the role is activated.</span></span> <span data-ttu-id="708fc-148">**false** si no enviar notificación cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="708fc-148">**false** if do not send notification when the role is activated.</span></span>|
|<span data-ttu-id="708fc-149">ticketingInfoOnElevation</span><span class="sxs-lookup"><span data-stu-id="708fc-149">ticketingInfoOnElevation</span></span>|<span data-ttu-id="708fc-150">boolean</span><span class="sxs-lookup"><span data-stu-id="708fc-150">boolean</span></span>|<span data-ttu-id="708fc-151">**true** si se requiere la información mediante vales cuándo activar la función.</span><span class="sxs-lookup"><span data-stu-id="708fc-151">**true** if the ticketing information is required when activate the role.</span></span> <span data-ttu-id="708fc-152">**false** si la información mediante vales no se requiere cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="708fc-152">**false** if the ticketing information is not required when activate the role.</span></span>|
|<span data-ttu-id="708fc-153">approvalOnElevation</span><span class="sxs-lookup"><span data-stu-id="708fc-153">approvalOnElevation</span></span>|<span data-ttu-id="708fc-154">boolean</span><span class="sxs-lookup"><span data-stu-id="708fc-154">boolean</span></span>|<span data-ttu-id="708fc-155">**true** si se requiere la aprobación cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="708fc-155">**true** if the approval is required when activate the role.</span></span> <span data-ttu-id="708fc-156">**false** si la aprobación no se requiere cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="708fc-156">**false** if the approval is not required when activate the role.</span></span>|
|<span data-ttu-id="708fc-157">approverIds</span><span class="sxs-lookup"><span data-stu-id="708fc-157">approverIds</span></span>|<span data-ttu-id="708fc-158">matriz</span><span class="sxs-lookup"><span data-stu-id="708fc-158">array</span></span>|<span data-ttu-id="708fc-159">Lista de identificadores de aprobación, si se necesita aprobación para la activación.</span><span class="sxs-lookup"><span data-stu-id="708fc-159">List of Approval ids, if approval is required for activation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="708fc-160">Relaciones</span><span class="sxs-lookup"><span data-stu-id="708fc-160">Relationships</span></span>
<span data-ttu-id="708fc-161">Ninguno</span><span class="sxs-lookup"><span data-stu-id="708fc-161">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="708fc-162">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="708fc-162">JSON representation</span></span>

<span data-ttu-id="708fc-163">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="708fc-163">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedRoleSettings"
}-->

```json
{
  "elevationDuration": "String (timestamp)",
  "id": "string (identifier)",
  "isMfaOnElevationConfigurable": true,
  "lastGlobalAdmin": true,
  "maxElavationDuration": "String (timestamp)",
  "mfaOnElevation": true,
  "minElevationDuration": "String (timestamp)",
  "notificationToUserOnElevation": true,
  "ticketingInfoOnElevation": true,
  "approvalOnElevation": false,
  "approverIds": []
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRoleSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
