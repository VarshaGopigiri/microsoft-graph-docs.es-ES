---
title: Tipo de recurso deviceConfigurationUserOverview
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: c844fd17e3287707a5ecacfb89c7b622497e2aac
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310664"
---
# <a name="deviceconfigurationuseroverview-resource-type"></a><span data-ttu-id="11290-103">Tipo de recurso deviceConfigurationUserOverview</span><span class="sxs-lookup"><span data-stu-id="11290-103">deviceConfigurationUserOverview resource type</span></span>

> <span data-ttu-id="11290-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="11290-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="11290-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="11290-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="11290-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="11290-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="11290-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="11290-107">Not yet documented</span></span>
## <a name="methods"></a><span data-ttu-id="11290-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="11290-108">Methods</span></span>
|<span data-ttu-id="11290-109">Método</span><span class="sxs-lookup"><span data-stu-id="11290-109">Method</span></span>|<span data-ttu-id="11290-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11290-110">Return Type</span></span>|<span data-ttu-id="11290-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="11290-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="11290-112">Obtener deviceConfigurationUserOverview</span><span class="sxs-lookup"><span data-stu-id="11290-112">Get deviceConfigurationUserOverview</span></span>](../api/intune-deviceconfig-deviceconfigurationuseroverview-get.md)|[<span data-ttu-id="11290-113">deviceConfigurationUserOverview</span><span class="sxs-lookup"><span data-stu-id="11290-113">deviceConfigurationUserOverview</span></span>](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|<span data-ttu-id="11290-114">Lea las propiedades y las relaciones del objeto [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="11290-114">Read properties and relationships of the [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md) object.</span></span>|
|[<span data-ttu-id="11290-115">Actualizar deviceConfigurationUserOverview</span><span class="sxs-lookup"><span data-stu-id="11290-115">Update deviceConfigurationUserOverview</span></span>](../api/intune-deviceconfig-deviceconfigurationuseroverview-update.md)|[<span data-ttu-id="11290-116">deviceConfigurationUserOverview</span><span class="sxs-lookup"><span data-stu-id="11290-116">deviceConfigurationUserOverview</span></span>](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|<span data-ttu-id="11290-117">Actualice las propiedades de un objeto [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="11290-117">Update the properties of a [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="11290-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11290-118">Properties</span></span>
|<span data-ttu-id="11290-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11290-119">Property</span></span>|<span data-ttu-id="11290-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="11290-120">Type</span></span>|<span data-ttu-id="11290-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="11290-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="11290-122">id</span><span class="sxs-lookup"><span data-stu-id="11290-122">id</span></span>|<span data-ttu-id="11290-123">String</span><span class="sxs-lookup"><span data-stu-id="11290-123">String</span></span>|<span data-ttu-id="11290-124">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="11290-124">Key of the entity.</span></span>|
|<span data-ttu-id="11290-125">pendingCount</span><span class="sxs-lookup"><span data-stu-id="11290-125">pendingCount</span></span>|<span data-ttu-id="11290-126">Int32</span><span class="sxs-lookup"><span data-stu-id="11290-126">Int32</span></span>|<span data-ttu-id="11290-127">Número de usuarios pendientes</span><span class="sxs-lookup"><span data-stu-id="11290-127">Number of pending Users</span></span>|
|<span data-ttu-id="11290-128">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="11290-128">notApplicableCount</span></span>|<span data-ttu-id="11290-129">Int32</span><span class="sxs-lookup"><span data-stu-id="11290-129">Int32</span></span>|<span data-ttu-id="11290-130">Número de usuarios no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="11290-130">Number of not applicable users</span></span>|
|<span data-ttu-id="11290-131">successCount</span><span class="sxs-lookup"><span data-stu-id="11290-131">successCount</span></span>|<span data-ttu-id="11290-132">Int32</span><span class="sxs-lookup"><span data-stu-id="11290-132">Int32</span></span>|<span data-ttu-id="11290-133">Número de usuarios correctos</span><span class="sxs-lookup"><span data-stu-id="11290-133">Number of succeeded Users</span></span>|
|<span data-ttu-id="11290-134">errorCount</span><span class="sxs-lookup"><span data-stu-id="11290-134">errorCount</span></span>|<span data-ttu-id="11290-135">Int32</span><span class="sxs-lookup"><span data-stu-id="11290-135">Int32</span></span>|<span data-ttu-id="11290-136">Número de usuarios con error</span><span class="sxs-lookup"><span data-stu-id="11290-136">Number of error Users</span></span>|
|<span data-ttu-id="11290-137">failedCount</span><span class="sxs-lookup"><span data-stu-id="11290-137">failedCount</span></span>|<span data-ttu-id="11290-138">Int32</span><span class="sxs-lookup"><span data-stu-id="11290-138">Int32</span></span>|<span data-ttu-id="11290-139">Número de usuarios erróneos</span><span class="sxs-lookup"><span data-stu-id="11290-139">Number of failed Users</span></span>|
|<span data-ttu-id="11290-140">conflictCount</span><span class="sxs-lookup"><span data-stu-id="11290-140">conflictCount</span></span>|<span data-ttu-id="11290-141">Int32</span><span class="sxs-lookup"><span data-stu-id="11290-141">Int32</span></span>|<span data-ttu-id="11290-142">Número de usuarios en conflicto</span><span class="sxs-lookup"><span data-stu-id="11290-142">Number of users in conflict</span></span>|
|<span data-ttu-id="11290-143">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="11290-143">lastUpdateDateTime</span></span>|<span data-ttu-id="11290-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="11290-144">DateTimeOffset</span></span>|<span data-ttu-id="11290-145">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="11290-145">Last update time</span></span>|
|<span data-ttu-id="11290-146">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="11290-146">configurationVersion</span></span>|<span data-ttu-id="11290-147">Int32</span><span class="sxs-lookup"><span data-stu-id="11290-147">Int32</span></span>|<span data-ttu-id="11290-148">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="11290-148">Version of the policy for that overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="11290-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="11290-149">Relationships</span></span>
<span data-ttu-id="11290-150">Ninguna</span><span class="sxs-lookup"><span data-stu-id="11290-150">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="11290-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="11290-151">JSON Representation</span></span>
<span data-ttu-id="11290-152">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="11290-152">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationUserOverview"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationUserOverview",
  "id": "String (identifier)",
  "pendingCount": 1024,
  "notApplicableCount": 1024,
  "successCount": 1024,
  "errorCount": 1024,
  "failedCount": 1024,
  "conflictCount": 1024,
  "lastUpdateDateTime": "String (timestamp)",
  "configurationVersion": 1024
}
```





