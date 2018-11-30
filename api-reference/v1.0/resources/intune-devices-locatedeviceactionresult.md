---
title: Tipo de recurso locateDeviceActionResult
description: Resultado de la acción Buscar dispositivo
ms.openlocfilehash: 3cabeca1ac07dd1911cf4c60300d07bdc1266134
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030310"
---
# <a name="locatedeviceactionresult-resource-type"></a><span data-ttu-id="ad475-103">Tipo de recurso locateDeviceActionResult</span><span class="sxs-lookup"><span data-stu-id="ad475-103">locateDeviceActionResult resource type</span></span>

> <span data-ttu-id="ad475-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ad475-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ad475-105">Resultado de la acción Buscar dispositivo</span><span class="sxs-lookup"><span data-stu-id="ad475-105">Locate device action result</span></span>

<span data-ttu-id="ad475-106">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="ad475-106">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="ad475-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ad475-107">Properties</span></span>
|<span data-ttu-id="ad475-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ad475-108">Property</span></span>|<span data-ttu-id="ad475-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad475-109">Type</span></span>|<span data-ttu-id="ad475-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad475-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ad475-111">actionName</span><span class="sxs-lookup"><span data-stu-id="ad475-111">actionName</span></span>|<span data-ttu-id="ad475-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="ad475-112">String</span></span>|<span data-ttu-id="ad475-113">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="ad475-113">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="ad475-114">actionState</span><span class="sxs-lookup"><span data-stu-id="ad475-114">actionState</span></span>|[<span data-ttu-id="ad475-115">actionState</span><span class="sxs-lookup"><span data-stu-id="ad475-115">actionState</span></span>](../resources/intune-devices-actionstate.md)|<span data-ttu-id="ad475-116">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="ad475-116">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="ad475-117">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="ad475-117">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="ad475-118">startDateTime</span><span class="sxs-lookup"><span data-stu-id="ad475-118">startDateTime</span></span>|<span data-ttu-id="ad475-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ad475-119">DateTimeOffset</span></span>|<span data-ttu-id="ad475-120">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="ad475-120">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="ad475-121">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="ad475-121">lastUpdatedDateTime</span></span>|<span data-ttu-id="ad475-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ad475-122">DateTimeOffset</span></span>|<span data-ttu-id="ad475-123">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="ad475-123">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="ad475-124">deviceLocation</span><span class="sxs-lookup"><span data-stu-id="ad475-124">deviceLocation</span></span>|[<span data-ttu-id="ad475-125">deviceGeoLocation</span><span class="sxs-lookup"><span data-stu-id="ad475-125">deviceGeoLocation</span></span>](../resources/intune-devices-devicegeolocation.md)|<span data-ttu-id="ad475-126">ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ad475-126">device location</span></span>|

## <a name="relationships"></a><span data-ttu-id="ad475-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ad475-127">Relationships</span></span>
<span data-ttu-id="ad475-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ad475-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ad475-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ad475-129">JSON Representation</span></span>
<span data-ttu-id="ad475-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ad475-130">Here is a JSON representation of the resource.</span></span>
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



