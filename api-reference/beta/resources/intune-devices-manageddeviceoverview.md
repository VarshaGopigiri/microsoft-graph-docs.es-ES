---
title: Tipo de recurso managedDeviceOverview
description: Datos de resumen de los dispositivos administrados
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 091871ed88903f4fcb3a3ad8be86e7b997f173b0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932520"
---
# <a name="manageddeviceoverview-resource-type"></a><span data-ttu-id="cae31-103">Tipo de recurso managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="cae31-103">managedDeviceOverview resource type</span></span>

> <span data-ttu-id="cae31-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cae31-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cae31-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cae31-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cae31-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cae31-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cae31-107">Datos de resumen de los dispositivos administrados</span><span class="sxs-lookup"><span data-stu-id="cae31-107">Summary data for managed devices</span></span>
## <a name="methods"></a><span data-ttu-id="cae31-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="cae31-108">Methods</span></span>
|<span data-ttu-id="cae31-109">Método</span><span class="sxs-lookup"><span data-stu-id="cae31-109">Method</span></span>|<span data-ttu-id="cae31-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cae31-110">Return Type</span></span>|<span data-ttu-id="cae31-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="cae31-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="cae31-112">Obtener managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="cae31-112">Get managedDeviceOverview</span></span>](../api/intune-devices-manageddeviceoverview-get.md)|[<span data-ttu-id="cae31-113">managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="cae31-113">managedDeviceOverview</span></span>](../resources/intune-devices-manageddeviceoverview.md)|<span data-ttu-id="cae31-114">Lea las propiedades y las relaciones del objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="cae31-114">Read properties and relationships of the [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>|
|[<span data-ttu-id="cae31-115">Actualizar managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="cae31-115">Update managedDeviceOverview</span></span>](../api/intune-devices-manageddeviceoverview-update.md)|[<span data-ttu-id="cae31-116">managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="cae31-116">managedDeviceOverview</span></span>](../resources/intune-devices-manageddeviceoverview.md)|<span data-ttu-id="cae31-117">Actualice las propiedades de un objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="cae31-117">Update the properties of a [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="cae31-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cae31-118">Properties</span></span>
|<span data-ttu-id="cae31-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cae31-119">Property</span></span>|<span data-ttu-id="cae31-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="cae31-120">Type</span></span>|<span data-ttu-id="cae31-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="cae31-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cae31-122">id</span><span class="sxs-lookup"><span data-stu-id="cae31-122">id</span></span>|<span data-ttu-id="cae31-123">String</span><span class="sxs-lookup"><span data-stu-id="cae31-123">String</span></span>|<span data-ttu-id="cae31-124">Identificador único del resumen</span><span class="sxs-lookup"><span data-stu-id="cae31-124">Unique Identifier for the summary</span></span>|
|<span data-ttu-id="cae31-125">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="cae31-125">enrolledDeviceCount</span></span>|<span data-ttu-id="cae31-126">Int32</span><span class="sxs-lookup"><span data-stu-id="cae31-126">Int32</span></span>|<span data-ttu-id="cae31-127">Número total de dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="cae31-127">Total enrolled device count.</span></span> <span data-ttu-id="cae31-128">No incluye equipos administrados mediante el agente de PC de Intune</span><span class="sxs-lookup"><span data-stu-id="cae31-128">Does not include PC devices managed via Intune PC Agent</span></span>|
|<span data-ttu-id="cae31-129">mdmEnrolledCount</span><span class="sxs-lookup"><span data-stu-id="cae31-129">mdmEnrolledCount</span></span>|<span data-ttu-id="cae31-130">Int32</span><span class="sxs-lookup"><span data-stu-id="cae31-130">Int32</span></span>|<span data-ttu-id="cae31-131">El número de dispositivos inscritos en MDM</span><span class="sxs-lookup"><span data-stu-id="cae31-131">The number of devices enrolled in MDM</span></span>|
|<span data-ttu-id="cae31-132">dualEnrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="cae31-132">dualEnrolledDeviceCount</span></span>|<span data-ttu-id="cae31-133">Int32</span><span class="sxs-lookup"><span data-stu-id="cae31-133">Int32</span></span>|<span data-ttu-id="cae31-134">El número de dispositivos inscritos tanto en MDM como EAS</span><span class="sxs-lookup"><span data-stu-id="cae31-134">The number of devices enrolled in both MDM and EAS</span></span>|
|<span data-ttu-id="cae31-135">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="cae31-135">deviceOperatingSystemSummary</span></span>|[<span data-ttu-id="cae31-136">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="cae31-136">deviceOperatingSystemSummary</span></span>](../resources/intune-devices-deviceoperatingsystemsummary.md)|<span data-ttu-id="cae31-137">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="cae31-137">Device operating system summary.</span></span>|
|<span data-ttu-id="cae31-138">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="cae31-138">deviceExchangeAccessStateSummary</span></span>|[<span data-ttu-id="cae31-139">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="cae31-139">deviceExchangeAccessStateSummary</span></span>](../resources/intune-devices-deviceexchangeaccessstatesummary.md)|<span data-ttu-id="cae31-140">Distribución del estado de acceso de Exchange en Intune</span><span class="sxs-lookup"><span data-stu-id="cae31-140">Distribution of Exchange Access State in Intune</span></span>|
|<span data-ttu-id="cae31-141">managedDeviceModelsAndManufacturers</span><span class="sxs-lookup"><span data-stu-id="cae31-141">managedDeviceModelsAndManufacturers</span></span>|[<span data-ttu-id="cae31-142">managedDeviceModelsAndManufacturers</span><span class="sxs-lookup"><span data-stu-id="cae31-142">managedDeviceModelsAndManufacturers</span></span>](../resources/intune-devices-manageddevicemodelsandmanufacturers.md)|<span data-ttu-id="cae31-143">Modelos y fabricantes meatadata para los dispositivos administrados en la cuenta</span><span class="sxs-lookup"><span data-stu-id="cae31-143">Models and Manufactures meatadata for managed devices in the account</span></span>|
|<span data-ttu-id="cae31-144">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="cae31-144">lastModifiedDateTime</span></span>|<span data-ttu-id="cae31-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cae31-145">DateTimeOffset</span></span>|<span data-ttu-id="cae31-146">Hora última fecha de modificación de información general de dispositivos</span><span class="sxs-lookup"><span data-stu-id="cae31-146">Last modified date time of device overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="cae31-147">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cae31-147">Relationships</span></span>
<span data-ttu-id="cae31-148">Ninguna</span><span class="sxs-lookup"><span data-stu-id="cae31-148">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="cae31-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cae31-149">JSON Representation</span></span>
<span data-ttu-id="cae31-150">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cae31-150">Here is a JSON representation of the resource.</span></span>
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





