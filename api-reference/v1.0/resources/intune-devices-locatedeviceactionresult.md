---
title: Tipo de recurso locateDeviceActionResult
description: Resultado de la acción Buscar dispositivo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f6a4db661c706f62f170ae0a869d491d26d602eb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888196"
---
# <a name="locatedeviceactionresult-resource-type"></a><span data-ttu-id="4b66f-103">Tipo de recurso locateDeviceActionResult</span><span class="sxs-lookup"><span data-stu-id="4b66f-103">locateDeviceActionResult resource type</span></span>

> <span data-ttu-id="4b66f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4b66f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4b66f-105">Resultado de la acción Buscar dispositivo</span><span class="sxs-lookup"><span data-stu-id="4b66f-105">Locate device action result</span></span>

<span data-ttu-id="4b66f-106">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="4b66f-106">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="4b66f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4b66f-107">Properties</span></span>
|<span data-ttu-id="4b66f-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4b66f-108">Property</span></span>|<span data-ttu-id="4b66f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b66f-109">Type</span></span>|<span data-ttu-id="4b66f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b66f-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4b66f-111">actionName</span><span class="sxs-lookup"><span data-stu-id="4b66f-111">actionName</span></span>|<span data-ttu-id="4b66f-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="4b66f-112">String</span></span>|<span data-ttu-id="4b66f-113">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="4b66f-113">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="4b66f-114">actionState</span><span class="sxs-lookup"><span data-stu-id="4b66f-114">actionState</span></span>|[<span data-ttu-id="4b66f-115">actionState</span><span class="sxs-lookup"><span data-stu-id="4b66f-115">actionState</span></span>](../resources/intune-devices-actionstate.md)|<span data-ttu-id="4b66f-116">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="4b66f-116">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="4b66f-117">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="4b66f-117">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="4b66f-118">startDateTime</span><span class="sxs-lookup"><span data-stu-id="4b66f-118">startDateTime</span></span>|<span data-ttu-id="4b66f-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4b66f-119">DateTimeOffset</span></span>|<span data-ttu-id="4b66f-120">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="4b66f-120">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="4b66f-121">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="4b66f-121">lastUpdatedDateTime</span></span>|<span data-ttu-id="4b66f-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4b66f-122">DateTimeOffset</span></span>|<span data-ttu-id="4b66f-123">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="4b66f-123">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="4b66f-124">deviceLocation</span><span class="sxs-lookup"><span data-stu-id="4b66f-124">deviceLocation</span></span>|[<span data-ttu-id="4b66f-125">deviceGeoLocation</span><span class="sxs-lookup"><span data-stu-id="4b66f-125">deviceGeoLocation</span></span>](../resources/intune-devices-devicegeolocation.md)|<span data-ttu-id="4b66f-126">ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="4b66f-126">device location</span></span>|

## <a name="relationships"></a><span data-ttu-id="4b66f-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4b66f-127">Relationships</span></span>
<span data-ttu-id="4b66f-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4b66f-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4b66f-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4b66f-129">JSON Representation</span></span>
<span data-ttu-id="4b66f-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4b66f-130">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.locateDeviceActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.locateDeviceActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "deviceLocation": {
    "@odata.type": "microsoft.graph.deviceGeoLocation",
    "lastCollectedDateTime": "String (timestamp)",
    "longitude": "<Unknown Primitive Type Edm.Double>",
    "latitude": "<Unknown Primitive Type Edm.Double>",
    "altitude": "<Unknown Primitive Type Edm.Double>",
    "horizontalAccuracy": "<Unknown Primitive Type Edm.Double>",
    "verticalAccuracy": "<Unknown Primitive Type Edm.Double>",
    "heading": "<Unknown Primitive Type Edm.Double>",
    "speed": "<Unknown Primitive Type Edm.Double>"
  }
}
```



