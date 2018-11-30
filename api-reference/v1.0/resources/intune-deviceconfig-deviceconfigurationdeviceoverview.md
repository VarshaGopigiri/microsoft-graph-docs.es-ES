---
title: Tipo de recurso deviceConfigurationDeviceOverview
description: Todavía no documentado
ms.openlocfilehash: 068292de3f8f128e9052cada73ab1e00107741b8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030185"
---
# <a name="deviceconfigurationdeviceoverview-resource-type"></a><span data-ttu-id="550ac-103">Tipo de recurso deviceConfigurationDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="550ac-103">deviceConfigurationDeviceOverview resource type</span></span>

> <span data-ttu-id="550ac-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="550ac-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="550ac-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="550ac-105">Not yet documented</span></span>
## <a name="methods"></a><span data-ttu-id="550ac-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="550ac-106">Methods</span></span>
|<span data-ttu-id="550ac-107">Método</span><span class="sxs-lookup"><span data-stu-id="550ac-107">Method</span></span>|<span data-ttu-id="550ac-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="550ac-108">Return Type</span></span>|<span data-ttu-id="550ac-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="550ac-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="550ac-110">Obtener deviceConfigurationDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="550ac-110">Get deviceConfigurationDeviceOverview</span></span>](../api/intune-deviceconfig-deviceconfigurationdeviceoverview-get.md)|[<span data-ttu-id="550ac-111">deviceConfigurationDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="550ac-111">deviceConfigurationDeviceOverview</span></span>](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|<span data-ttu-id="550ac-112">Lea las propiedades y las relaciones del objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="550ac-112">Read properties and relationships of the [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md) object.</span></span>|
|[<span data-ttu-id="550ac-113">Actualizar deviceConfigurationDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="550ac-113">Update deviceConfigurationDeviceOverview</span></span>](../api/intune-deviceconfig-deviceconfigurationdeviceoverview-update.md)|[<span data-ttu-id="550ac-114">deviceConfigurationDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="550ac-114">deviceConfigurationDeviceOverview</span></span>](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|<span data-ttu-id="550ac-115">Actualice las propiedades de un objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="550ac-115">Update the properties of a [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="550ac-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="550ac-116">Properties</span></span>
|<span data-ttu-id="550ac-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="550ac-117">Property</span></span>|<span data-ttu-id="550ac-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="550ac-118">Type</span></span>|<span data-ttu-id="550ac-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="550ac-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="550ac-120">id</span><span class="sxs-lookup"><span data-stu-id="550ac-120">id</span></span>|<span data-ttu-id="550ac-121">String</span><span class="sxs-lookup"><span data-stu-id="550ac-121">String</span></span>|<span data-ttu-id="550ac-122">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="550ac-122">Key of the entity.</span></span>|
|<span data-ttu-id="550ac-123">pendingCount</span><span class="sxs-lookup"><span data-stu-id="550ac-123">pendingCount</span></span>|<span data-ttu-id="550ac-124">Int32</span><span class="sxs-lookup"><span data-stu-id="550ac-124">Int32</span></span>|<span data-ttu-id="550ac-125">Número de dispositivos pendientes</span><span class="sxs-lookup"><span data-stu-id="550ac-125">Number of pending devices</span></span>|
|<span data-ttu-id="550ac-126">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="550ac-126">notApplicableCount</span></span>|<span data-ttu-id="550ac-127">Int32</span><span class="sxs-lookup"><span data-stu-id="550ac-127">Int32</span></span>|<span data-ttu-id="550ac-128">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="550ac-128">Number of not applicable devices</span></span>|
|<span data-ttu-id="550ac-129">successCount</span><span class="sxs-lookup"><span data-stu-id="550ac-129">successCount</span></span>|<span data-ttu-id="550ac-130">Int32</span><span class="sxs-lookup"><span data-stu-id="550ac-130">Int32</span></span>|<span data-ttu-id="550ac-131">Número de dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="550ac-131">Number of succeeded devices</span></span>|
|<span data-ttu-id="550ac-132">errorCount</span><span class="sxs-lookup"><span data-stu-id="550ac-132">errorCount</span></span>|<span data-ttu-id="550ac-133">Int32</span><span class="sxs-lookup"><span data-stu-id="550ac-133">Int32</span></span>|<span data-ttu-id="550ac-134">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="550ac-134">Number of error devices</span></span>|
|<span data-ttu-id="550ac-135">failedCount</span><span class="sxs-lookup"><span data-stu-id="550ac-135">failedCount</span></span>|<span data-ttu-id="550ac-136">Int32</span><span class="sxs-lookup"><span data-stu-id="550ac-136">Int32</span></span>|<span data-ttu-id="550ac-137">Número de dispositivos erróneos</span><span class="sxs-lookup"><span data-stu-id="550ac-137">Number of failed devices</span></span>|
|<span data-ttu-id="550ac-138">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="550ac-138">lastUpdateDateTime</span></span>|<span data-ttu-id="550ac-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="550ac-139">DateTimeOffset</span></span>|<span data-ttu-id="550ac-140">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="550ac-140">Last update time</span></span>|
|<span data-ttu-id="550ac-141">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="550ac-141">configurationVersion</span></span>|<span data-ttu-id="550ac-142">Int32</span><span class="sxs-lookup"><span data-stu-id="550ac-142">Int32</span></span>|<span data-ttu-id="550ac-143">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="550ac-143">Version of the policy for that overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="550ac-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="550ac-144">Relationships</span></span>
<span data-ttu-id="550ac-145">Ninguna</span><span class="sxs-lookup"><span data-stu-id="550ac-145">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="550ac-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="550ac-146">JSON Representation</span></span>
<span data-ttu-id="550ac-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="550ac-147">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationDeviceOverview"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceOverview",
  "id": "String (identifier)",
  "pendingCount": 1024,
  "notApplicableCount": 1024,
  "successCount": 1024,
  "errorCount": 1024,
  "failedCount": 1024,
  "lastUpdateDateTime": "String (timestamp)",
  "configurationVersion": 1024
}
```



