---
title: Tipo de recurso managedDeviceOverview
description: Datos de resumen de los dispositivos administrados
ms.openlocfilehash: 11f1012329d0217499d813b94f72474da8c683a6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087187"
---
# <a name="manageddeviceoverview-resource-type"></a><span data-ttu-id="16048-103">Tipo de recurso managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="16048-103">managedDeviceOverview resource type</span></span>

> <span data-ttu-id="16048-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="16048-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="16048-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="16048-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="16048-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="16048-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="16048-107">Datos de resumen de los dispositivos administrados</span><span class="sxs-lookup"><span data-stu-id="16048-107">Summary data for managed devices</span></span>
## <a name="methods"></a><span data-ttu-id="16048-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="16048-108">Methods</span></span>
|<span data-ttu-id="16048-109">Método</span><span class="sxs-lookup"><span data-stu-id="16048-109">Method</span></span>|<span data-ttu-id="16048-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16048-110">Return Type</span></span>|<span data-ttu-id="16048-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="16048-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="16048-112">Obtener managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="16048-112">Get managedDeviceOverview</span></span>](../api/intune-devices-manageddeviceoverview-get.md)|[<span data-ttu-id="16048-113">managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="16048-113">managedDeviceOverview</span></span>](../resources/intune-devices-manageddeviceoverview.md)|<span data-ttu-id="16048-114">Lea las propiedades y las relaciones del objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="16048-114">Read properties and relationships of the [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>|
|[<span data-ttu-id="16048-115">Actualizar managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="16048-115">Update managedDeviceOverview</span></span>](../api/intune-devices-manageddeviceoverview-update.md)|[<span data-ttu-id="16048-116">managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="16048-116">managedDeviceOverview</span></span>](../resources/intune-devices-manageddeviceoverview.md)|<span data-ttu-id="16048-117">Actualice las propiedades de un objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="16048-117">Update the properties of a [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="16048-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="16048-118">Properties</span></span>
|<span data-ttu-id="16048-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16048-119">Property</span></span>|<span data-ttu-id="16048-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="16048-120">Type</span></span>|<span data-ttu-id="16048-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="16048-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="16048-122">id</span><span class="sxs-lookup"><span data-stu-id="16048-122">id</span></span>|<span data-ttu-id="16048-123">String</span><span class="sxs-lookup"><span data-stu-id="16048-123">String</span></span>|<span data-ttu-id="16048-124">Identificador único del resumen</span><span class="sxs-lookup"><span data-stu-id="16048-124">Unique Identifier for the summary</span></span>|
|<span data-ttu-id="16048-125">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="16048-125">enrolledDeviceCount</span></span>|<span data-ttu-id="16048-126">Int32</span><span class="sxs-lookup"><span data-stu-id="16048-126">Int32</span></span>|<span data-ttu-id="16048-127">Número total de dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="16048-127">Total enrolled device count.</span></span> <span data-ttu-id="16048-128">No incluye equipos administrados mediante el agente de PC de Intune</span><span class="sxs-lookup"><span data-stu-id="16048-128">Does not include PC devices managed via Intune PC Agent</span></span>|
|<span data-ttu-id="16048-129">mdmEnrolledCount</span><span class="sxs-lookup"><span data-stu-id="16048-129">mdmEnrolledCount</span></span>|<span data-ttu-id="16048-130">Int32</span><span class="sxs-lookup"><span data-stu-id="16048-130">Int32</span></span>|<span data-ttu-id="16048-131">El número de dispositivos inscritos en MDM</span><span class="sxs-lookup"><span data-stu-id="16048-131">The number of devices enrolled in MDM</span></span>|
|<span data-ttu-id="16048-132">dualEnrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="16048-132">dualEnrolledDeviceCount</span></span>|<span data-ttu-id="16048-133">Int32</span><span class="sxs-lookup"><span data-stu-id="16048-133">Int32</span></span>|<span data-ttu-id="16048-134">El número de dispositivos inscritos tanto en MDM como EAS</span><span class="sxs-lookup"><span data-stu-id="16048-134">The number of devices enrolled in both MDM and EAS</span></span>|
|<span data-ttu-id="16048-135">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="16048-135">deviceOperatingSystemSummary</span></span>|[<span data-ttu-id="16048-136">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="16048-136">deviceOperatingSystemSummary</span></span>](../resources/intune-devices-deviceoperatingsystemsummary.md)|<span data-ttu-id="16048-137">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="16048-137">Device operating system summary.</span></span>|
|<span data-ttu-id="16048-138">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="16048-138">deviceExchangeAccessStateSummary</span></span>|[<span data-ttu-id="16048-139">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="16048-139">deviceExchangeAccessStateSummary</span></span>](../resources/intune-devices-deviceexchangeaccessstatesummary.md)|<span data-ttu-id="16048-140">Distribución del estado de acceso de Exchange en Intune</span><span class="sxs-lookup"><span data-stu-id="16048-140">Distribution of Exchange Access State in Intune</span></span>|
|<span data-ttu-id="16048-141">managedDeviceModelsAndManufacturers</span><span class="sxs-lookup"><span data-stu-id="16048-141">managedDeviceModelsAndManufacturers</span></span>|[<span data-ttu-id="16048-142">managedDeviceModelsAndManufacturers</span><span class="sxs-lookup"><span data-stu-id="16048-142">managedDeviceModelsAndManufacturers</span></span>](../resources/intune-devices-manageddevicemodelsandmanufacturers.md)|<span data-ttu-id="16048-143">Modelos y fabricantes meatadata para los dispositivos administrados en la cuenta</span><span class="sxs-lookup"><span data-stu-id="16048-143">Models and Manufactures meatadata for managed devices in the account</span></span>|
|<span data-ttu-id="16048-144">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="16048-144">lastModifiedDateTime</span></span>|<span data-ttu-id="16048-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="16048-145">DateTimeOffset</span></span>|<span data-ttu-id="16048-146">Hora última fecha de modificación de información general de dispositivos</span><span class="sxs-lookup"><span data-stu-id="16048-146">Last modified date time of device overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="16048-147">Relaciones</span><span class="sxs-lookup"><span data-stu-id="16048-147">Relationships</span></span>
<span data-ttu-id="16048-148">Ninguna</span><span class="sxs-lookup"><span data-stu-id="16048-148">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="16048-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="16048-149">JSON Representation</span></span>
<span data-ttu-id="16048-150">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="16048-150">Here is a JSON representation of the resource.</span></span>
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
  },
  "managedDeviceModelsAndManufacturers": {
    "@odata.type": "microsoft.graph.managedDeviceModelsAndManufacturers",
    "deviceModels": [
      "String"
    ],
    "deviceManufacturers": [
      "String"
    ]
  },
  "lastModifiedDateTime": "String (timestamp)"
}
```





