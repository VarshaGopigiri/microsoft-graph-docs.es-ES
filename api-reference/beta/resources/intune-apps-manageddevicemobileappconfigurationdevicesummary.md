---
title: Tipo de recurso managedDeviceMobileAppConfigurationDeviceSummary
description: Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de dispositivo de la configuración de aplicaciones móviles de MDM.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: c6af1ff39fe9626f42003863992ec2e185d67caf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939591"
---
# <a name="manageddevicemobileappconfigurationdevicesummary-resource-type"></a><span data-ttu-id="89677-103">Tipo de recurso managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="89677-103">managedDeviceMobileAppConfigurationDeviceSummary resource type</span></span>

> <span data-ttu-id="89677-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="89677-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="89677-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="89677-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="89677-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="89677-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="89677-107">Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de dispositivo de la configuración de aplicaciones móviles de MDM.</span><span class="sxs-lookup"><span data-stu-id="89677-107">Contains properties, inherited properties and actions for an MDM mobile app configuration device status summary.</span></span>
## <a name="methods"></a><span data-ttu-id="89677-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="89677-108">Methods</span></span>
|<span data-ttu-id="89677-109">Método</span><span class="sxs-lookup"><span data-stu-id="89677-109">Method</span></span>|<span data-ttu-id="89677-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89677-110">Return Type</span></span>|<span data-ttu-id="89677-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="89677-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="89677-112">Obtener managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="89677-112">Get managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../api/intune-apps-manageddevicemobileappconfigurationdevicesummary-get.md)|[<span data-ttu-id="89677-113">managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="89677-113">managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md)|<span data-ttu-id="89677-114">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="89677-114">Read properties and relationships of the [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) object.</span></span>|
|[<span data-ttu-id="89677-115">Actualizar managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="89677-115">Update managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../api/intune-apps-manageddevicemobileappconfigurationdevicesummary-update.md)|[<span data-ttu-id="89677-116">managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="89677-116">managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md)|<span data-ttu-id="89677-117">Actualice las propiedades y las relaciones de un objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="89677-117">Update the properties of a [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="89677-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="89677-118">Properties</span></span>
|<span data-ttu-id="89677-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="89677-119">Property</span></span>|<span data-ttu-id="89677-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="89677-120">Type</span></span>|<span data-ttu-id="89677-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="89677-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="89677-122">id</span><span class="sxs-lookup"><span data-stu-id="89677-122">id</span></span>|<span data-ttu-id="89677-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="89677-123">String</span></span>|<span data-ttu-id="89677-124">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="89677-124">Key of the entity.</span></span>|
|<span data-ttu-id="89677-125">pendingCount</span><span class="sxs-lookup"><span data-stu-id="89677-125">pendingCount</span></span>|<span data-ttu-id="89677-126">Int32</span><span class="sxs-lookup"><span data-stu-id="89677-126">Int32</span></span>|<span data-ttu-id="89677-127">Número de dispositivos pendientes</span><span class="sxs-lookup"><span data-stu-id="89677-127">Number of pending devices</span></span>|
|<span data-ttu-id="89677-128">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="89677-128">notApplicableCount</span></span>|<span data-ttu-id="89677-129">Int32</span><span class="sxs-lookup"><span data-stu-id="89677-129">Int32</span></span>|<span data-ttu-id="89677-130">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="89677-130">Number of not applicable devices</span></span>|
|<span data-ttu-id="89677-131">notApplicablePlatformCount</span><span class="sxs-lookup"><span data-stu-id="89677-131">notApplicablePlatformCount</span></span>|<span data-ttu-id="89677-132">Int32</span><span class="sxs-lookup"><span data-stu-id="89677-132">Int32</span></span>|<span data-ttu-id="89677-133">Número de dispositivos no aplicables debido a la plataforma de error de coincidencia y la directiva</span><span class="sxs-lookup"><span data-stu-id="89677-133">Number of not applicable devices due to mismatch platform and policy</span></span>|
|<span data-ttu-id="89677-134">successCount</span><span class="sxs-lookup"><span data-stu-id="89677-134">successCount</span></span>|<span data-ttu-id="89677-135">Int32</span><span class="sxs-lookup"><span data-stu-id="89677-135">Int32</span></span>|<span data-ttu-id="89677-136">Número de dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="89677-136">Number of succeeded devices</span></span>|
|<span data-ttu-id="89677-137">errorCount</span><span class="sxs-lookup"><span data-stu-id="89677-137">errorCount</span></span>|<span data-ttu-id="89677-138">Int32</span><span class="sxs-lookup"><span data-stu-id="89677-138">Int32</span></span>|<span data-ttu-id="89677-139">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="89677-139">Number of error devices</span></span>|
|<span data-ttu-id="89677-140">failedCount</span><span class="sxs-lookup"><span data-stu-id="89677-140">failedCount</span></span>|<span data-ttu-id="89677-141">Int32</span><span class="sxs-lookup"><span data-stu-id="89677-141">Int32</span></span>|<span data-ttu-id="89677-142">Número de dispositivos erróneos</span><span class="sxs-lookup"><span data-stu-id="89677-142">Number of failed devices</span></span>|
|<span data-ttu-id="89677-143">conflictCount</span><span class="sxs-lookup"><span data-stu-id="89677-143">conflictCount</span></span>|<span data-ttu-id="89677-144">Int32</span><span class="sxs-lookup"><span data-stu-id="89677-144">Int32</span></span>|<span data-ttu-id="89677-145">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="89677-145">Number of devices in conflict</span></span>|
|<span data-ttu-id="89677-146">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="89677-146">lastUpdateDateTime</span></span>|<span data-ttu-id="89677-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="89677-147">DateTimeOffset</span></span>|<span data-ttu-id="89677-148">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="89677-148">Last update time</span></span>|
|<span data-ttu-id="89677-149">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="89677-149">configurationVersion</span></span>|<span data-ttu-id="89677-150">Int32</span><span class="sxs-lookup"><span data-stu-id="89677-150">Int32</span></span>|<span data-ttu-id="89677-151">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="89677-151">Version of the policy for that overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="89677-152">Relaciones</span><span class="sxs-lookup"><span data-stu-id="89677-152">Relationships</span></span>
<span data-ttu-id="89677-153">Ninguna</span><span class="sxs-lookup"><span data-stu-id="89677-153">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="89677-154">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="89677-154">JSON Representation</span></span>
<span data-ttu-id="89677-155">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="89677-155">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfigurationDeviceSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceSummary",
  "id": "String (identifier)",
  "pendingCount": 1024,
  "notApplicableCount": 1024,
  "notApplicablePlatformCount": 1024,
  "successCount": 1024,
  "errorCount": 1024,
  "failedCount": 1024,
  "conflictCount": 1024,
  "lastUpdateDateTime": "String (timestamp)",
  "configurationVersion": 1024
}
```





