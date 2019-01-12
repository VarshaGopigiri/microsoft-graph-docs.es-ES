---
title: Tipo de recurso deviceGeoLocation
description: Ubicación del dispositivo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ef73925c31b58327f0e0b89d5682035d14d38afc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943104"
---
# <a name="devicegeolocation-resource-type"></a><span data-ttu-id="e0e88-103">Tipo de recurso deviceGeoLocation</span><span class="sxs-lookup"><span data-stu-id="e0e88-103">deviceGeoLocation resource type</span></span>

> <span data-ttu-id="e0e88-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e0e88-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e0e88-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e0e88-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e0e88-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e0e88-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e0e88-107">Ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e0e88-107">Device location</span></span>
## <a name="properties"></a><span data-ttu-id="e0e88-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e0e88-108">Properties</span></span>
|<span data-ttu-id="e0e88-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e0e88-109">Property</span></span>|<span data-ttu-id="e0e88-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0e88-110">Type</span></span>|<span data-ttu-id="e0e88-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0e88-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e0e88-112">lastCollectedDateTimeUtc</span><span class="sxs-lookup"><span data-stu-id="e0e88-112">lastCollectedDateTimeUtc</span></span>|<span data-ttu-id="e0e88-113">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e0e88-113">DateTimeOffset</span></span>|<span data-ttu-id="e0e88-114">Hora en la que se registró la ubicación, con respecto a UTC</span><span class="sxs-lookup"><span data-stu-id="e0e88-114">Time at which location was recorded, relative to UTC</span></span>|
|<span data-ttu-id="e0e88-115">lastCollectedDateTime</span><span class="sxs-lookup"><span data-stu-id="e0e88-115">lastCollectedDateTime</span></span>|<span data-ttu-id="e0e88-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e0e88-116">DateTimeOffset</span></span>|<span data-ttu-id="e0e88-117">Hora en la que se registró la ubicación, con respecto a UTC</span><span class="sxs-lookup"><span data-stu-id="e0e88-117">Time at which location was recorded, relative to UTC</span></span>|
|<span data-ttu-id="e0e88-118">longitude</span><span class="sxs-lookup"><span data-stu-id="e0e88-118">longitude</span></span>|<span data-ttu-id="e0e88-119">Doble</span><span class="sxs-lookup"><span data-stu-id="e0e88-119">Double</span></span>|<span data-ttu-id="e0e88-120">Coordenadas de longitud de la ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e0e88-120">Longitude coordinate of the device's location</span></span>|
|<span data-ttu-id="e0e88-121">latitude</span><span class="sxs-lookup"><span data-stu-id="e0e88-121">latitude</span></span>|<span data-ttu-id="e0e88-122">Doble</span><span class="sxs-lookup"><span data-stu-id="e0e88-122">Double</span></span>|<span data-ttu-id="e0e88-123">Coordenadas de latitud de la ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e0e88-123">Latitude coordinate of the device's location</span></span>|
|<span data-ttu-id="e0e88-124">altitude</span><span class="sxs-lookup"><span data-stu-id="e0e88-124">altitude</span></span>|<span data-ttu-id="e0e88-125">Doble</span><span class="sxs-lookup"><span data-stu-id="e0e88-125">Double</span></span>|<span data-ttu-id="e0e88-126">Altitud, en metros por encima del nivel del mar</span><span class="sxs-lookup"><span data-stu-id="e0e88-126">Altitude, given in meters above sea level</span></span>|
|<span data-ttu-id="e0e88-127">horizontalAccuracy</span><span class="sxs-lookup"><span data-stu-id="e0e88-127">horizontalAccuracy</span></span>|<span data-ttu-id="e0e88-128">Doble</span><span class="sxs-lookup"><span data-stu-id="e0e88-128">Double</span></span>|<span data-ttu-id="e0e88-129">Precisión de longitud y latitud en metros</span><span class="sxs-lookup"><span data-stu-id="e0e88-129">Accuracy of longitude and latitude in meters</span></span>|
|<span data-ttu-id="e0e88-130">verticalAccuracy</span><span class="sxs-lookup"><span data-stu-id="e0e88-130">verticalAccuracy</span></span>|<span data-ttu-id="e0e88-131">Doble</span><span class="sxs-lookup"><span data-stu-id="e0e88-131">Double</span></span>|<span data-ttu-id="e0e88-132">Precisión de altitud en metros</span><span class="sxs-lookup"><span data-stu-id="e0e88-132">Accuracy of altitude in meters</span></span>|
|<span data-ttu-id="e0e88-133">rumbo</span><span class="sxs-lookup"><span data-stu-id="e0e88-133">heading</span></span>|<span data-ttu-id="e0e88-134">Doble</span><span class="sxs-lookup"><span data-stu-id="e0e88-134">Double</span></span>|<span data-ttu-id="e0e88-135">Rumbo en grados desde el norte geográfico</span><span class="sxs-lookup"><span data-stu-id="e0e88-135">Heading in degrees from true north</span></span>|
|<span data-ttu-id="e0e88-136">velocidad</span><span class="sxs-lookup"><span data-stu-id="e0e88-136">speed</span></span>|<span data-ttu-id="e0e88-137">Doble</span><span class="sxs-lookup"><span data-stu-id="e0e88-137">Double</span></span>|<span data-ttu-id="e0e88-138">La velocidad a la que se desplaza el dispositivo en metros por segundo</span><span class="sxs-lookup"><span data-stu-id="e0e88-138">Speed the device is traveling in meters per second</span></span>|

## <a name="relationships"></a><span data-ttu-id="e0e88-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e0e88-139">Relationships</span></span>
<span data-ttu-id="e0e88-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e0e88-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e0e88-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e0e88-141">JSON Representation</span></span>
<span data-ttu-id="e0e88-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e0e88-142">Here is a JSON representation of the resource.</span></span>
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





