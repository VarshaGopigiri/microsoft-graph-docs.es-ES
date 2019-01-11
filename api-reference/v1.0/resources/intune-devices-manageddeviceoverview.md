---
title: Tipo de recurso managedDeviceOverview
description: Datos de resumen de los dispositivos administrados
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7deb73e1fa9557e212d8fab524f62f15bad4b249
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867259"
---
# <a name="manageddeviceoverview-resource-type"></a><span data-ttu-id="e8463-103">Tipo de recurso managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="e8463-103">managedDeviceOverview resource type</span></span>

> <span data-ttu-id="e8463-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e8463-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e8463-105">Datos de resumen de los dispositivos administrados</span><span class="sxs-lookup"><span data-stu-id="e8463-105">Summary data for managed devices</span></span>
## <a name="methods"></a><span data-ttu-id="e8463-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="e8463-106">Methods</span></span>
|<span data-ttu-id="e8463-107">Método</span><span class="sxs-lookup"><span data-stu-id="e8463-107">Method</span></span>|<span data-ttu-id="e8463-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8463-108">Return Type</span></span>|<span data-ttu-id="e8463-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8463-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="e8463-110">Obtener managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="e8463-110">Get managedDeviceOverview</span></span>](../api/intune-devices-manageddeviceoverview-get.md)|[<span data-ttu-id="e8463-111">managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="e8463-111">managedDeviceOverview</span></span>](../resources/intune-devices-manageddeviceoverview.md)|<span data-ttu-id="e8463-112">Lea las propiedades y las relaciones del objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e8463-112">Read properties and relationships of the [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>|
|[<span data-ttu-id="e8463-113">Actualizar managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="e8463-113">Update managedDeviceOverview</span></span>](../api/intune-devices-manageddeviceoverview-update.md)|[<span data-ttu-id="e8463-114">managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="e8463-114">managedDeviceOverview</span></span>](../resources/intune-devices-manageddeviceoverview.md)|<span data-ttu-id="e8463-115">Actualice las propiedades de un objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e8463-115">Update the properties of a [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="e8463-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e8463-116">Properties</span></span>
|<span data-ttu-id="e8463-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e8463-117">Property</span></span>|<span data-ttu-id="e8463-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="e8463-118">Type</span></span>|<span data-ttu-id="e8463-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8463-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e8463-120">id</span><span class="sxs-lookup"><span data-stu-id="e8463-120">id</span></span>|<span data-ttu-id="e8463-121">String</span><span class="sxs-lookup"><span data-stu-id="e8463-121">String</span></span>|<span data-ttu-id="e8463-122">Identificador único del resumen</span><span class="sxs-lookup"><span data-stu-id="e8463-122">Unique Identifier for the summary</span></span>|
|<span data-ttu-id="e8463-123">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="e8463-123">enrolledDeviceCount</span></span>|<span data-ttu-id="e8463-124">Int32</span><span class="sxs-lookup"><span data-stu-id="e8463-124">Int32</span></span>|<span data-ttu-id="e8463-125">Número total de dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="e8463-125">Total enrolled device count.</span></span> <span data-ttu-id="e8463-126">No incluye equipos administrados mediante el agente de PC de Intune</span><span class="sxs-lookup"><span data-stu-id="e8463-126">Does not include PC devices managed via Intune PC Agent</span></span>|
|<span data-ttu-id="e8463-127">mdmEnrolledCount</span><span class="sxs-lookup"><span data-stu-id="e8463-127">mdmEnrolledCount</span></span>|<span data-ttu-id="e8463-128">Int32</span><span class="sxs-lookup"><span data-stu-id="e8463-128">Int32</span></span>|<span data-ttu-id="e8463-129">El número de dispositivos inscritos en MDM</span><span class="sxs-lookup"><span data-stu-id="e8463-129">The number of devices enrolled in MDM</span></span>|
|<span data-ttu-id="e8463-130">dualEnrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="e8463-130">dualEnrolledDeviceCount</span></span>|<span data-ttu-id="e8463-131">Int32</span><span class="sxs-lookup"><span data-stu-id="e8463-131">Int32</span></span>|<span data-ttu-id="e8463-132">El número de dispositivos inscritos tanto en MDM como EAS</span><span class="sxs-lookup"><span data-stu-id="e8463-132">The number of devices enrolled in both MDM and EAS</span></span>|
|<span data-ttu-id="e8463-133">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="e8463-133">deviceOperatingSystemSummary</span></span>|[<span data-ttu-id="e8463-134">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="e8463-134">deviceOperatingSystemSummary</span></span>](../resources/intune-devices-deviceoperatingsystemsummary.md)|<span data-ttu-id="e8463-135">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e8463-135">Device operating system summary.</span></span>|
|<span data-ttu-id="e8463-136">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="e8463-136">deviceExchangeAccessStateSummary</span></span>|[<span data-ttu-id="e8463-137">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="e8463-137">deviceExchangeAccessStateSummary</span></span>](../resources/intune-devices-deviceexchangeaccessstatesummary.md)|<span data-ttu-id="e8463-138">Distribución del estado de acceso de Exchange en Intune</span><span class="sxs-lookup"><span data-stu-id="e8463-138">Distribution of Exchange Access State in Intune</span></span>|

## <a name="relationships"></a><span data-ttu-id="e8463-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e8463-139">Relationships</span></span>
<span data-ttu-id="e8463-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e8463-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e8463-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e8463-141">JSON Representation</span></span>
<span data-ttu-id="e8463-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e8463-142">Here is a JSON representation of the resource.</span></span>
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



