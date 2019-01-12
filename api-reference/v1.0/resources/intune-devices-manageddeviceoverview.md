---
title: Tipo de recurso managedDeviceOverview
description: Datos de resumen de los dispositivos administrados
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7a5abdd3b5455272de7d1cf73044a1356d728dd0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981199"
---
# <a name="manageddeviceoverview-resource-type"></a><span data-ttu-id="55f4e-103">Tipo de recurso managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="55f4e-103">managedDeviceOverview resource type</span></span>

> <span data-ttu-id="55f4e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="55f4e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="55f4e-105">Datos de resumen de los dispositivos administrados</span><span class="sxs-lookup"><span data-stu-id="55f4e-105">Summary data for managed devices</span></span>
## <a name="methods"></a><span data-ttu-id="55f4e-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="55f4e-106">Methods</span></span>
|<span data-ttu-id="55f4e-107">Método</span><span class="sxs-lookup"><span data-stu-id="55f4e-107">Method</span></span>|<span data-ttu-id="55f4e-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55f4e-108">Return Type</span></span>|<span data-ttu-id="55f4e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="55f4e-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="55f4e-110">Obtener managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="55f4e-110">Get managedDeviceOverview</span></span>](../api/intune-devices-manageddeviceoverview-get.md)|[<span data-ttu-id="55f4e-111">managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="55f4e-111">managedDeviceOverview</span></span>](../resources/intune-devices-manageddeviceoverview.md)|<span data-ttu-id="55f4e-112">Lea las propiedades y las relaciones del objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="55f4e-112">Read properties and relationships of the [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>|
|[<span data-ttu-id="55f4e-113">Actualizar managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="55f4e-113">Update managedDeviceOverview</span></span>](../api/intune-devices-manageddeviceoverview-update.md)|[<span data-ttu-id="55f4e-114">managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="55f4e-114">managedDeviceOverview</span></span>](../resources/intune-devices-manageddeviceoverview.md)|<span data-ttu-id="55f4e-115">Actualice las propiedades de un objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="55f4e-115">Update the properties of a [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="55f4e-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55f4e-116">Properties</span></span>
|<span data-ttu-id="55f4e-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="55f4e-117">Property</span></span>|<span data-ttu-id="55f4e-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="55f4e-118">Type</span></span>|<span data-ttu-id="55f4e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="55f4e-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="55f4e-120">id</span><span class="sxs-lookup"><span data-stu-id="55f4e-120">id</span></span>|<span data-ttu-id="55f4e-121">String</span><span class="sxs-lookup"><span data-stu-id="55f4e-121">String</span></span>|<span data-ttu-id="55f4e-122">Identificador único del resumen</span><span class="sxs-lookup"><span data-stu-id="55f4e-122">Unique Identifier for the summary</span></span>|
|<span data-ttu-id="55f4e-123">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="55f4e-123">enrolledDeviceCount</span></span>|<span data-ttu-id="55f4e-124">Int32</span><span class="sxs-lookup"><span data-stu-id="55f4e-124">Int32</span></span>|<span data-ttu-id="55f4e-125">Número total de dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="55f4e-125">Total enrolled device count.</span></span> <span data-ttu-id="55f4e-126">No incluye equipos administrados mediante el agente de PC de Intune</span><span class="sxs-lookup"><span data-stu-id="55f4e-126">Does not include PC devices managed via Intune PC Agent</span></span>|
|<span data-ttu-id="55f4e-127">mdmEnrolledCount</span><span class="sxs-lookup"><span data-stu-id="55f4e-127">mdmEnrolledCount</span></span>|<span data-ttu-id="55f4e-128">Int32</span><span class="sxs-lookup"><span data-stu-id="55f4e-128">Int32</span></span>|<span data-ttu-id="55f4e-129">El número de dispositivos inscritos en MDM</span><span class="sxs-lookup"><span data-stu-id="55f4e-129">The number of devices enrolled in MDM</span></span>|
|<span data-ttu-id="55f4e-130">dualEnrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="55f4e-130">dualEnrolledDeviceCount</span></span>|<span data-ttu-id="55f4e-131">Int32</span><span class="sxs-lookup"><span data-stu-id="55f4e-131">Int32</span></span>|<span data-ttu-id="55f4e-132">El número de dispositivos inscritos tanto en MDM como EAS</span><span class="sxs-lookup"><span data-stu-id="55f4e-132">The number of devices enrolled in both MDM and EAS</span></span>|
|<span data-ttu-id="55f4e-133">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="55f4e-133">deviceOperatingSystemSummary</span></span>|[<span data-ttu-id="55f4e-134">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="55f4e-134">deviceOperatingSystemSummary</span></span>](../resources/intune-devices-deviceoperatingsystemsummary.md)|<span data-ttu-id="55f4e-135">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="55f4e-135">Device operating system summary.</span></span>|
|<span data-ttu-id="55f4e-136">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="55f4e-136">deviceExchangeAccessStateSummary</span></span>|[<span data-ttu-id="55f4e-137">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="55f4e-137">deviceExchangeAccessStateSummary</span></span>](../resources/intune-devices-deviceexchangeaccessstatesummary.md)|<span data-ttu-id="55f4e-138">Distribución del estado de acceso de Exchange en Intune</span><span class="sxs-lookup"><span data-stu-id="55f4e-138">Distribution of Exchange Access State in Intune</span></span>|

## <a name="relationships"></a><span data-ttu-id="55f4e-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="55f4e-139">Relationships</span></span>
<span data-ttu-id="55f4e-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="55f4e-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="55f4e-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="55f4e-141">JSON Representation</span></span>
<span data-ttu-id="55f4e-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="55f4e-142">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceOverview"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceOverview",
  "id": "String (identifier)",
  "enrolledDeviceCount": 1024,
  "mdmEnrolledCount": 1024,
  "dualEnrolledDeviceCount": 1024,
  "deviceOperatingSystemSummary": {
    "@odata.type": "microsoft.graph.deviceOperatingSystemSummary",
    "androidCount": 1024,
    "iosCount": 1024,
    "macOSCount": 1024,
    "windowsMobileCount": 1024,
    "windowsCount": 1024,
    "unknownCount": 1024
  },
  "deviceExchangeAccessStateSummary": {
    "@odata.type": "microsoft.graph.deviceExchangeAccessStateSummary",
    "allowedDeviceCount": 1024,
    "blockedDeviceCount": 1024,
    "quarantinedDeviceCount": 1024,
    "unknownDeviceCount": 1024,
    "unavailableDeviceCount": 1024
  }
}
```



