---
title: tipo de recurso privilegedRoleSettings
description: Representa la configuración de un rol con privilegios.
ms.openlocfilehash: 14b4919d653de80c97f06aff507c011162c3c0e4
ms.sourcegitcommit: 2532b8dd7f2533d956e2600855b3daeabdd9b8ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2018
ms.locfileid: "27091227"
---
# <a name="privilegedrolesettings-resource-type"></a><span data-ttu-id="e2dd7-103">tipo de recurso privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="e2dd7-103">privilegedRoleSettings resource type</span></span>

> <span data-ttu-id="e2dd7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e2dd7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e2dd7-106">Representa la configuración de un rol con privilegios.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-106">Represents the settings for a privileged role.</span></span>


## <a name="methods"></a><span data-ttu-id="e2dd7-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2dd7-107">Methods</span></span>

| <span data-ttu-id="e2dd7-108">Método</span><span class="sxs-lookup"><span data-stu-id="e2dd7-108">Method</span></span>           | <span data-ttu-id="e2dd7-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2dd7-109">Return Type</span></span>    |<span data-ttu-id="e2dd7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2dd7-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e2dd7-111">Obtener privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="e2dd7-111">Get privilegedRoleSettings</span></span>](../api/privilegedrolesettings-get.md) | [<span data-ttu-id="e2dd7-112">privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="e2dd7-112">privilegedRoleSettings</span></span>](privilegedrolesettings.md) |<span data-ttu-id="e2dd7-113">Leer las propiedades y las relaciones del objeto privilegedRoleSettings.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-113">Read properties and relationships of privilegedRoleSettings object.</span></span>|
|[<span data-ttu-id="e2dd7-114">Actualizar privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="e2dd7-114">Update privilegedRoleSettings</span></span>](../api/privilegedrolesettings-update.md) | [<span data-ttu-id="e2dd7-115">privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="e2dd7-115">privilegedRoleSettings</span></span>](privilegedrolesettings.md) |<span data-ttu-id="e2dd7-116">Actualizar el objeto privilegedRoleSettings.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-116">Update privilegedRoleSettings object.</span></span>|
## <a name="properties"></a><span data-ttu-id="e2dd7-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2dd7-117">Properties</span></span>
| <span data-ttu-id="e2dd7-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e2dd7-118">Property</span></span>     | <span data-ttu-id="e2dd7-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2dd7-119">Type</span></span>   |<span data-ttu-id="e2dd7-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2dd7-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e2dd7-121">elevationDuration</span><span class="sxs-lookup"><span data-stu-id="e2dd7-121">elevationDuration</span></span>|<span data-ttu-id="e2dd7-122">duration</span><span class="sxs-lookup"><span data-stu-id="e2dd7-122">duration</span></span>|<span data-ttu-id="e2dd7-123">La duración cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-123">The duration when the role is activated.</span></span>|
|<span data-ttu-id="e2dd7-124">id</span><span class="sxs-lookup"><span data-stu-id="e2dd7-124">id</span></span>|<span data-ttu-id="e2dd7-125">string</span><span class="sxs-lookup"><span data-stu-id="e2dd7-125">string</span></span>| <span data-ttu-id="e2dd7-126">El identificador único para la configuración de las funciones.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-126">The unique identifier for the role settings.</span></span> <span data-ttu-id="e2dd7-127">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-127">Read-only.</span></span>|
|<span data-ttu-id="e2dd7-128">isMfaOnElevationConfigurable</span><span class="sxs-lookup"><span data-stu-id="e2dd7-128">isMfaOnElevationConfigurable</span></span>|<span data-ttu-id="e2dd7-129">boolean</span><span class="sxs-lookup"><span data-stu-id="e2dd7-129">boolean</span></span>|<span data-ttu-id="e2dd7-130">**true** si mfaOnElevation es configurable.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-130">**true** if mfaOnElevation is configurable.</span></span> <span data-ttu-id="e2dd7-131">**false** si no se puede configurar mfaOnElevation.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-131">**false** if mfaOnElevation is not configurable.</span></span>|
|<span data-ttu-id="e2dd7-132">lastGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="e2dd7-132">lastGlobalAdmin</span></span>|<span data-ttu-id="e2dd7-133">boolean</span><span class="sxs-lookup"><span data-stu-id="e2dd7-133">boolean</span></span>|<span data-ttu-id="e2dd7-134">Internal que sólo se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-134">Internal used only.</span></span>|
|<span data-ttu-id="e2dd7-135">maxElavationDuration</span><span class="sxs-lookup"><span data-stu-id="e2dd7-135">maxElavationDuration</span></span>|<span data-ttu-id="e2dd7-136">duration</span><span class="sxs-lookup"><span data-stu-id="e2dd7-136">duration</span></span>|<span data-ttu-id="e2dd7-137">Duración máxima de la función activada.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-137">Maximal duration for the activated role.</span></span>|
|<span data-ttu-id="e2dd7-138">mfaOnElevation</span><span class="sxs-lookup"><span data-stu-id="e2dd7-138">mfaOnElevation</span></span>|<span data-ttu-id="e2dd7-139">boolean</span><span class="sxs-lookup"><span data-stu-id="e2dd7-139">boolean</span></span>|<span data-ttu-id="e2dd7-140">**true** si MFA se requiere para activar la función.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-140">**true** if MFA is required to activate the role.</span></span> <span data-ttu-id="e2dd7-141">**false** si no es necesario MFA para activar la función.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-141">**false** if MFA is not required to activate the role.</span></span>|
|<span data-ttu-id="e2dd7-142">minElevationDuration</span><span class="sxs-lookup"><span data-stu-id="e2dd7-142">minElevationDuration</span></span>|<span data-ttu-id="e2dd7-143">duration</span><span class="sxs-lookup"><span data-stu-id="e2dd7-143">duration</span></span>|<span data-ttu-id="e2dd7-144">Duración mínima de la función activada.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-144">Minimal duration for the activated role.</span></span>|
|<span data-ttu-id="e2dd7-145">notificationToUserOnElevation</span><span class="sxs-lookup"><span data-stu-id="e2dd7-145">notificationToUserOnElevation</span></span>|<span data-ttu-id="e2dd7-146">boolean</span><span class="sxs-lookup"><span data-stu-id="e2dd7-146">boolean</span></span>|<span data-ttu-id="e2dd7-147">**true** si enviar notificación para el usuario final cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-147">**true** if send notification to the end user when the role is activated.</span></span> <span data-ttu-id="e2dd7-148">**false** si no enviar notificación cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-148">**false** if do not send notification when the role is activated.</span></span>|
|<span data-ttu-id="e2dd7-149">ticketingInfoOnElevation</span><span class="sxs-lookup"><span data-stu-id="e2dd7-149">ticketingInfoOnElevation</span></span>|<span data-ttu-id="e2dd7-150">boolean</span><span class="sxs-lookup"><span data-stu-id="e2dd7-150">boolean</span></span>|<span data-ttu-id="e2dd7-151">**true** si se requiere la información mediante vales cuándo activar la función.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-151">**true** if the ticketing information is required when activate the role.</span></span> <span data-ttu-id="e2dd7-152">**false** si la información mediante vales no se requiere cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-152">**false** if the ticketing information is not required when activate the role.</span></span>|
|<span data-ttu-id="e2dd7-153">approvalOnElevation</span><span class="sxs-lookup"><span data-stu-id="e2dd7-153">approvalOnElevation</span></span>|<span data-ttu-id="e2dd7-154">boolean</span><span class="sxs-lookup"><span data-stu-id="e2dd7-154">boolean</span></span>|<span data-ttu-id="e2dd7-155">**true** si se requiere la aprobación cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-155">**true** if the approval is required when activate the role.</span></span> <span data-ttu-id="e2dd7-156">**false** si la aprobación no se requiere cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-156">**false** if the approval is not required when activate the role.</span></span>|
|<span data-ttu-id="e2dd7-157">approverIds</span><span class="sxs-lookup"><span data-stu-id="e2dd7-157">approverIds</span></span>|<span data-ttu-id="e2dd7-158">matriz</span><span class="sxs-lookup"><span data-stu-id="e2dd7-158">array</span></span>|<span data-ttu-id="e2dd7-159">Lista de identificadores de aprobación, si se necesita aprobación para la activación.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-159">List of Approval ids, if approval is required for activation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e2dd7-160">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e2dd7-160">Relationships</span></span>
<span data-ttu-id="e2dd7-161">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e2dd7-161">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="e2dd7-162">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e2dd7-162">JSON representation</span></span>

<span data-ttu-id="e2dd7-163">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e2dd7-163">Here is a JSON representation of the resource.</span></span>

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