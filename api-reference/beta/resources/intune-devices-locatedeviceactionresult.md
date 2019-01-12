---
title: Tipo de recurso locateDeviceActionResult
description: Resultado de la acción Buscar dispositivo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f342f26916b1144a317d02871364e25da2d8c4d7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912459"
---
# <a name="locatedeviceactionresult-resource-type"></a><span data-ttu-id="abcf0-103">Tipo de recurso locateDeviceActionResult</span><span class="sxs-lookup"><span data-stu-id="abcf0-103">locateDeviceActionResult resource type</span></span>

> <span data-ttu-id="abcf0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="abcf0-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="abcf0-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="abcf0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="abcf0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="abcf0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="abcf0-107">Resultado de la acción Buscar dispositivo</span><span class="sxs-lookup"><span data-stu-id="abcf0-107">Locate device action result</span></span>

<span data-ttu-id="abcf0-108">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="abcf0-108">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="abcf0-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abcf0-109">Properties</span></span>
|<span data-ttu-id="abcf0-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="abcf0-110">Property</span></span>|<span data-ttu-id="abcf0-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="abcf0-111">Type</span></span>|<span data-ttu-id="abcf0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="abcf0-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="abcf0-113">actionName</span><span class="sxs-lookup"><span data-stu-id="abcf0-113">actionName</span></span>|<span data-ttu-id="abcf0-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="abcf0-114">String</span></span>|<span data-ttu-id="abcf0-115">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="abcf0-115">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="abcf0-116">actionState</span><span class="sxs-lookup"><span data-stu-id="abcf0-116">actionState</span></span>|[<span data-ttu-id="abcf0-117">actionState</span><span class="sxs-lookup"><span data-stu-id="abcf0-117">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="abcf0-118">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="abcf0-118">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="abcf0-119">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="abcf0-119">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="abcf0-120">startDateTime</span><span class="sxs-lookup"><span data-stu-id="abcf0-120">startDateTime</span></span>|<span data-ttu-id="abcf0-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="abcf0-121">DateTimeOffset</span></span>|<span data-ttu-id="abcf0-122">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="abcf0-122">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="abcf0-123">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="abcf0-123">lastUpdatedDateTime</span></span>|<span data-ttu-id="abcf0-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="abcf0-124">DateTimeOffset</span></span>|<span data-ttu-id="abcf0-125">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="abcf0-125">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="abcf0-126">deviceLocation</span><span class="sxs-lookup"><span data-stu-id="abcf0-126">deviceLocation</span></span>|[<span data-ttu-id="abcf0-127">deviceGeoLocation</span><span class="sxs-lookup"><span data-stu-id="abcf0-127">deviceGeoLocation</span></span>](../resources/intune-devices-devicegeolocation.md)|<span data-ttu-id="abcf0-128">ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="abcf0-128">device location</span></span>|

## <a name="relationships"></a><span data-ttu-id="abcf0-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="abcf0-129">Relationships</span></span>
<span data-ttu-id="abcf0-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="abcf0-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="abcf0-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="abcf0-131">JSON Representation</span></span>
<span data-ttu-id="abcf0-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="abcf0-132">Here is a JSON representation of the resource.</span></span>
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
    "lastCollectedDateTimeUtc": "String (timestamp)",
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





