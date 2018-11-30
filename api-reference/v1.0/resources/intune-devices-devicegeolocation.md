---
title: Tipo de recurso deviceGeoLocation
description: Ubicación del dispositivo
ms.openlocfilehash: 1bc72e4fb2d01c55d5d16ff2a45a020c5eaf99e5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031565"
---
# <a name="devicegeolocation-resource-type"></a><span data-ttu-id="5ba04-103">Tipo de recurso deviceGeoLocation</span><span class="sxs-lookup"><span data-stu-id="5ba04-103">deviceGeoLocation resource type</span></span>

> <span data-ttu-id="5ba04-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5ba04-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5ba04-105">Ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="5ba04-105">Device location</span></span>
## <a name="properties"></a><span data-ttu-id="5ba04-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5ba04-106">Properties</span></span>
|<span data-ttu-id="5ba04-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5ba04-107">Property</span></span>|<span data-ttu-id="5ba04-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ba04-108">Type</span></span>|<span data-ttu-id="5ba04-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ba04-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5ba04-110">lastCollectedDateTime</span><span class="sxs-lookup"><span data-stu-id="5ba04-110">lastCollectedDateTime</span></span>|<span data-ttu-id="5ba04-111">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5ba04-111">DateTimeOffset</span></span>|<span data-ttu-id="5ba04-112">Hora en la que se registró la ubicación, con respecto a UTC</span><span class="sxs-lookup"><span data-stu-id="5ba04-112">Time at which location was recorded, relative to UTC</span></span>|
|<span data-ttu-id="5ba04-113">longitude</span><span class="sxs-lookup"><span data-stu-id="5ba04-113">longitude</span></span>|<span data-ttu-id="5ba04-114">Doble</span><span class="sxs-lookup"><span data-stu-id="5ba04-114">Double</span></span>|<span data-ttu-id="5ba04-115">Coordenadas de longitud de la ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="5ba04-115">Longitude coordinate of the device's location</span></span>|
|<span data-ttu-id="5ba04-116">latitude</span><span class="sxs-lookup"><span data-stu-id="5ba04-116">latitude</span></span>|<span data-ttu-id="5ba04-117">Doble</span><span class="sxs-lookup"><span data-stu-id="5ba04-117">Double</span></span>|<span data-ttu-id="5ba04-118">Coordenadas de latitud de la ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="5ba04-118">Latitude coordinate of the device's location</span></span>|
|<span data-ttu-id="5ba04-119">altitude</span><span class="sxs-lookup"><span data-stu-id="5ba04-119">altitude</span></span>|<span data-ttu-id="5ba04-120">Doble</span><span class="sxs-lookup"><span data-stu-id="5ba04-120">Double</span></span>|<span data-ttu-id="5ba04-121">Altitud, en metros por encima del nivel del mar</span><span class="sxs-lookup"><span data-stu-id="5ba04-121">Altitude, given in meters above sea level</span></span>|
|<span data-ttu-id="5ba04-122">horizontalAccuracy</span><span class="sxs-lookup"><span data-stu-id="5ba04-122">horizontalAccuracy</span></span>|<span data-ttu-id="5ba04-123">Doble</span><span class="sxs-lookup"><span data-stu-id="5ba04-123">Double</span></span>|<span data-ttu-id="5ba04-124">Precisión de longitud y latitud en metros</span><span class="sxs-lookup"><span data-stu-id="5ba04-124">Accuracy of longitude and latitude in meters</span></span>|
|<span data-ttu-id="5ba04-125">verticalAccuracy</span><span class="sxs-lookup"><span data-stu-id="5ba04-125">verticalAccuracy</span></span>|<span data-ttu-id="5ba04-126">Doble</span><span class="sxs-lookup"><span data-stu-id="5ba04-126">Double</span></span>|<span data-ttu-id="5ba04-127">Precisión de altitud en metros</span><span class="sxs-lookup"><span data-stu-id="5ba04-127">Accuracy of altitude in meters</span></span>|
|<span data-ttu-id="5ba04-128">rumbo</span><span class="sxs-lookup"><span data-stu-id="5ba04-128">heading</span></span>|<span data-ttu-id="5ba04-129">Doble</span><span class="sxs-lookup"><span data-stu-id="5ba04-129">Double</span></span>|<span data-ttu-id="5ba04-130">Rumbo en grados desde el norte geográfico</span><span class="sxs-lookup"><span data-stu-id="5ba04-130">Heading in degrees from true north</span></span>|
|<span data-ttu-id="5ba04-131">velocidad</span><span class="sxs-lookup"><span data-stu-id="5ba04-131">speed</span></span>|<span data-ttu-id="5ba04-132">Doble</span><span class="sxs-lookup"><span data-stu-id="5ba04-132">Double</span></span>|<span data-ttu-id="5ba04-133">La velocidad a la que se desplaza el dispositivo en metros por segundo</span><span class="sxs-lookup"><span data-stu-id="5ba04-133">Speed the device is traveling in meters per second</span></span>|

## <a name="relationships"></a><span data-ttu-id="5ba04-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5ba04-134">Relationships</span></span>
<span data-ttu-id="5ba04-135">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5ba04-135">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5ba04-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5ba04-136">JSON Representation</span></span>
<span data-ttu-id="5ba04-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5ba04-137">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceGeoLocation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceGeoLocation",
  "lastCollectedDateTime": "String (timestamp)",
  "longitude": "<Unknown Primitive Type Edm.Double>",
  "latitude": "<Unknown Primitive Type Edm.Double>",
  "altitude": "<Unknown Primitive Type Edm.Double>",
  "horizontalAccuracy": "<Unknown Primitive Type Edm.Double>",
  "verticalAccuracy": "<Unknown Primitive Type Edm.Double>",
  "heading": "<Unknown Primitive Type Edm.Double>",
  "speed": "<Unknown Primitive Type Edm.Double>"
}
```



