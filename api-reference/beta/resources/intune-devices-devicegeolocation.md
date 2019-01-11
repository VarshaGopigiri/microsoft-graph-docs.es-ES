---
title: Tipo de recurso deviceGeoLocation
description: Ubicación del dispositivo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: dd81a0665d3d85a10488f78245449d265c85a8cc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845265"
---
# <a name="devicegeolocation-resource-type"></a><span data-ttu-id="aab37-103">Tipo de recurso deviceGeoLocation</span><span class="sxs-lookup"><span data-stu-id="aab37-103">deviceGeoLocation resource type</span></span>

> <span data-ttu-id="aab37-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="aab37-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="aab37-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="aab37-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="aab37-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="aab37-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="aab37-107">Ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="aab37-107">Device location</span></span>
## <a name="properties"></a><span data-ttu-id="aab37-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aab37-108">Properties</span></span>
|<span data-ttu-id="aab37-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aab37-109">Property</span></span>|<span data-ttu-id="aab37-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="aab37-110">Type</span></span>|<span data-ttu-id="aab37-111">Description</span><span class="sxs-lookup"><span data-stu-id="aab37-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="aab37-112">lastCollectedDateTimeUtc</span><span class="sxs-lookup"><span data-stu-id="aab37-112">lastCollectedDateTimeUtc</span></span>|<span data-ttu-id="aab37-113">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aab37-113">DateTimeOffset</span></span>|<span data-ttu-id="aab37-114">Hora en la que se registró la ubicación, con respecto a UTC</span><span class="sxs-lookup"><span data-stu-id="aab37-114">Time at which location was recorded, relative to UTC</span></span>|
|<span data-ttu-id="aab37-115">lastCollectedDateTime</span><span class="sxs-lookup"><span data-stu-id="aab37-115">lastCollectedDateTime</span></span>|<span data-ttu-id="aab37-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aab37-116">DateTimeOffset</span></span>|<span data-ttu-id="aab37-117">Hora en la que se registró la ubicación, con respecto a UTC</span><span class="sxs-lookup"><span data-stu-id="aab37-117">Time at which location was recorded, relative to UTC</span></span>|
|<span data-ttu-id="aab37-118">longitude</span><span class="sxs-lookup"><span data-stu-id="aab37-118">longitude</span></span>|<span data-ttu-id="aab37-119">Doble</span><span class="sxs-lookup"><span data-stu-id="aab37-119">Double</span></span>|<span data-ttu-id="aab37-120">Coordenadas de longitud de la ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="aab37-120">Longitude coordinate of the device's location</span></span>|
|<span data-ttu-id="aab37-121">latitude</span><span class="sxs-lookup"><span data-stu-id="aab37-121">latitude</span></span>|<span data-ttu-id="aab37-122">Doble</span><span class="sxs-lookup"><span data-stu-id="aab37-122">Double</span></span>|<span data-ttu-id="aab37-123">Coordenadas de latitud de la ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="aab37-123">Latitude coordinate of the device's location</span></span>|
|<span data-ttu-id="aab37-124">altitude</span><span class="sxs-lookup"><span data-stu-id="aab37-124">altitude</span></span>|<span data-ttu-id="aab37-125">Doble</span><span class="sxs-lookup"><span data-stu-id="aab37-125">Double</span></span>|<span data-ttu-id="aab37-126">Altitud, en metros por encima del nivel del mar</span><span class="sxs-lookup"><span data-stu-id="aab37-126">Altitude, given in meters above sea level</span></span>|
|<span data-ttu-id="aab37-127">horizontalAccuracy</span><span class="sxs-lookup"><span data-stu-id="aab37-127">horizontalAccuracy</span></span>|<span data-ttu-id="aab37-128">Doble</span><span class="sxs-lookup"><span data-stu-id="aab37-128">Double</span></span>|<span data-ttu-id="aab37-129">Precisión de longitud y latitud en metros</span><span class="sxs-lookup"><span data-stu-id="aab37-129">Accuracy of longitude and latitude in meters</span></span>|
|<span data-ttu-id="aab37-130">verticalAccuracy</span><span class="sxs-lookup"><span data-stu-id="aab37-130">verticalAccuracy</span></span>|<span data-ttu-id="aab37-131">Doble</span><span class="sxs-lookup"><span data-stu-id="aab37-131">Double</span></span>|<span data-ttu-id="aab37-132">Precisión de altitud en metros</span><span class="sxs-lookup"><span data-stu-id="aab37-132">Accuracy of altitude in meters</span></span>|
|<span data-ttu-id="aab37-133">rumbo</span><span class="sxs-lookup"><span data-stu-id="aab37-133">heading</span></span>|<span data-ttu-id="aab37-134">Doble</span><span class="sxs-lookup"><span data-stu-id="aab37-134">Double</span></span>|<span data-ttu-id="aab37-135">Rumbo en grados desde el norte geográfico</span><span class="sxs-lookup"><span data-stu-id="aab37-135">Heading in degrees from true north</span></span>|
|<span data-ttu-id="aab37-136">velocidad</span><span class="sxs-lookup"><span data-stu-id="aab37-136">speed</span></span>|<span data-ttu-id="aab37-137">Doble</span><span class="sxs-lookup"><span data-stu-id="aab37-137">Double</span></span>|<span data-ttu-id="aab37-138">La velocidad a la que se desplaza el dispositivo en metros por segundo</span><span class="sxs-lookup"><span data-stu-id="aab37-138">Speed the device is traveling in meters per second</span></span>|

## <a name="relationships"></a><span data-ttu-id="aab37-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="aab37-139">Relationships</span></span>
<span data-ttu-id="aab37-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="aab37-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="aab37-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="aab37-141">JSON Representation</span></span>
<span data-ttu-id="aab37-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="aab37-142">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceGeoLocation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceGeoLocation",
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
```





