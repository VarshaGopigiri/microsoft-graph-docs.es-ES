---
title: Tipo de recurso managedDeviceMobileAppConfigurationDeviceSummary
description: Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de dispositivo de la configuración de aplicaciones móviles de MDM.
ms.openlocfilehash: 459d97fd57987fba1c760f1c716553fa71233c2f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032390"
---
# <a name="manageddevicemobileappconfigurationdevicesummary-resource-type"></a><span data-ttu-id="8bb0a-103">Tipo de recurso managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="8bb0a-103">managedDeviceMobileAppConfigurationDeviceSummary resource type</span></span>

> <span data-ttu-id="8bb0a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8bb0a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8bb0a-105">Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de dispositivo de la configuración de aplicaciones móviles de MDM.</span><span class="sxs-lookup"><span data-stu-id="8bb0a-105">Contains properties, inherited properties and actions for an MDM mobile app configuration device status summary.</span></span>
## <a name="methods"></a><span data-ttu-id="8bb0a-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="8bb0a-106">Methods</span></span>
|<span data-ttu-id="8bb0a-107">Método</span><span class="sxs-lookup"><span data-stu-id="8bb0a-107">Method</span></span>|<span data-ttu-id="8bb0a-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bb0a-108">Return Type</span></span>|<span data-ttu-id="8bb0a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bb0a-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="8bb0a-110">Obtener managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="8bb0a-110">Get managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../api/intune-apps-manageddevicemobileappconfigurationdevicesummary-get.md)|[<span data-ttu-id="8bb0a-111">managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="8bb0a-111">managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md)|<span data-ttu-id="8bb0a-112">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="8bb0a-112">Read properties and relationships of the [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) object.</span></span>|
|[<span data-ttu-id="8bb0a-113">Actualizar managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="8bb0a-113">Update managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../api/intune-apps-manageddevicemobileappconfigurationdevicesummary-update.md)|[<span data-ttu-id="8bb0a-114">managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="8bb0a-114">managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md)|<span data-ttu-id="8bb0a-115">Actualice las propiedades y las relaciones de un objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="8bb0a-115">Update the properties of a [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="8bb0a-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8bb0a-116">Properties</span></span>
|<span data-ttu-id="8bb0a-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8bb0a-117">Property</span></span>|<span data-ttu-id="8bb0a-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="8bb0a-118">Type</span></span>|<span data-ttu-id="8bb0a-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bb0a-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8bb0a-120">id</span><span class="sxs-lookup"><span data-stu-id="8bb0a-120">id</span></span>|<span data-ttu-id="8bb0a-121">String</span><span class="sxs-lookup"><span data-stu-id="8bb0a-121">String</span></span>|<span data-ttu-id="8bb0a-122">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8bb0a-122">Key of the entity.</span></span>|
|<span data-ttu-id="8bb0a-123">pendingCount</span><span class="sxs-lookup"><span data-stu-id="8bb0a-123">pendingCount</span></span>|<span data-ttu-id="8bb0a-124">Int32</span><span class="sxs-lookup"><span data-stu-id="8bb0a-124">Int32</span></span>|<span data-ttu-id="8bb0a-125">Número de dispositivos pendientes</span><span class="sxs-lookup"><span data-stu-id="8bb0a-125">Number of pending devices</span></span>|
|<span data-ttu-id="8bb0a-126">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="8bb0a-126">notApplicableCount</span></span>|<span data-ttu-id="8bb0a-127">Int32</span><span class="sxs-lookup"><span data-stu-id="8bb0a-127">Int32</span></span>|<span data-ttu-id="8bb0a-128">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="8bb0a-128">Number of not applicable devices</span></span>|
|<span data-ttu-id="8bb0a-129">successCount</span><span class="sxs-lookup"><span data-stu-id="8bb0a-129">successCount</span></span>|<span data-ttu-id="8bb0a-130">Int32</span><span class="sxs-lookup"><span data-stu-id="8bb0a-130">Int32</span></span>|<span data-ttu-id="8bb0a-131">Número de dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="8bb0a-131">Number of succeeded devices</span></span>|
|<span data-ttu-id="8bb0a-132">errorCount</span><span class="sxs-lookup"><span data-stu-id="8bb0a-132">errorCount</span></span>|<span data-ttu-id="8bb0a-133">Int32</span><span class="sxs-lookup"><span data-stu-id="8bb0a-133">Int32</span></span>|<span data-ttu-id="8bb0a-134">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="8bb0a-134">Number of error devices</span></span>|
|<span data-ttu-id="8bb0a-135">failedCount</span><span class="sxs-lookup"><span data-stu-id="8bb0a-135">failedCount</span></span>|<span data-ttu-id="8bb0a-136">Int32</span><span class="sxs-lookup"><span data-stu-id="8bb0a-136">Int32</span></span>|<span data-ttu-id="8bb0a-137">Número de dispositivos erróneos</span><span class="sxs-lookup"><span data-stu-id="8bb0a-137">Number of failed devices</span></span>|
|<span data-ttu-id="8bb0a-138">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="8bb0a-138">lastUpdateDateTime</span></span>|<span data-ttu-id="8bb0a-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8bb0a-139">DateTimeOffset</span></span>|<span data-ttu-id="8bb0a-140">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="8bb0a-140">Last update time</span></span>|
|<span data-ttu-id="8bb0a-141">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="8bb0a-141">configurationVersion</span></span>|<span data-ttu-id="8bb0a-142">Int32</span><span class="sxs-lookup"><span data-stu-id="8bb0a-142">Int32</span></span>|<span data-ttu-id="8bb0a-143">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="8bb0a-143">Version of the policy for that overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="8bb0a-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8bb0a-144">Relationships</span></span>
<span data-ttu-id="8bb0a-145">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8bb0a-145">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8bb0a-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8bb0a-146">JSON Representation</span></span>
<span data-ttu-id="8bb0a-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8bb0a-147">Here is a JSON representation of the resource.</span></span>
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
  "successCount": 1024,
  "errorCount": 1024,
  "failedCount": 1024,
  "lastUpdateDateTime": "String (timestamp)",
  "configurationVersion": 1024
}
```



