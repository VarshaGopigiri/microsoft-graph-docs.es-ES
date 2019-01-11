---
title: Tipo de recurso deviceGeoLocation
description: Ubicación del dispositivo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 68e89b2e63b99324332874a3ad6a2f2e3c335832
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816131"
---
# <a name="devicegeolocation-resource-type"></a><span data-ttu-id="408d6-103">Tipo de recurso deviceGeoLocation</span><span class="sxs-lookup"><span data-stu-id="408d6-103">deviceGeoLocation resource type</span></span>

> <span data-ttu-id="408d6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="408d6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="408d6-105">Ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="408d6-105">Device location</span></span>
## <a name="properties"></a><span data-ttu-id="408d6-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="408d6-106">Properties</span></span>
|<span data-ttu-id="408d6-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="408d6-107">Property</span></span>|<span data-ttu-id="408d6-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="408d6-108">Type</span></span>|<span data-ttu-id="408d6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="408d6-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="408d6-110">lastCollectedDateTime</span><span class="sxs-lookup"><span data-stu-id="408d6-110">lastCollectedDateTime</span></span>|<span data-ttu-id="408d6-111">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="408d6-111">DateTimeOffset</span></span>|<span data-ttu-id="408d6-112">Hora en la que se registró la ubicación, con respecto a UTC</span><span class="sxs-lookup"><span data-stu-id="408d6-112">Time at which location was recorded, relative to UTC</span></span>|
|<span data-ttu-id="408d6-113">longitude</span><span class="sxs-lookup"><span data-stu-id="408d6-113">longitude</span></span>|<span data-ttu-id="408d6-114">Doble</span><span class="sxs-lookup"><span data-stu-id="408d6-114">Double</span></span>|<span data-ttu-id="408d6-115">Coordenadas de longitud de la ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="408d6-115">Longitude coordinate of the device's location</span></span>|
|<span data-ttu-id="408d6-116">latitude</span><span class="sxs-lookup"><span data-stu-id="408d6-116">latitude</span></span>|<span data-ttu-id="408d6-117">Doble</span><span class="sxs-lookup"><span data-stu-id="408d6-117">Double</span></span>|<span data-ttu-id="408d6-118">Coordenadas de latitud de la ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="408d6-118">Latitude coordinate of the device's location</span></span>|
|<span data-ttu-id="408d6-119">altitude</span><span class="sxs-lookup"><span data-stu-id="408d6-119">altitude</span></span>|<span data-ttu-id="408d6-120">Doble</span><span class="sxs-lookup"><span data-stu-id="408d6-120">Double</span></span>|<span data-ttu-id="408d6-121">Altitud, en metros por encima del nivel del mar</span><span class="sxs-lookup"><span data-stu-id="408d6-121">Altitude, given in meters above sea level</span></span>|
|<span data-ttu-id="408d6-122">horizontalAccuracy</span><span class="sxs-lookup"><span data-stu-id="408d6-122">horizontalAccuracy</span></span>|<span data-ttu-id="408d6-123">Doble</span><span class="sxs-lookup"><span data-stu-id="408d6-123">Double</span></span>|<span data-ttu-id="408d6-124">Precisión de longitud y latitud en metros</span><span class="sxs-lookup"><span data-stu-id="408d6-124">Accuracy of longitude and latitude in meters</span></span>|
|<span data-ttu-id="408d6-125">verticalAccuracy</span><span class="sxs-lookup"><span data-stu-id="408d6-125">verticalAccuracy</span></span>|<span data-ttu-id="408d6-126">Doble</span><span class="sxs-lookup"><span data-stu-id="408d6-126">Double</span></span>|<span data-ttu-id="408d6-127">Precisión de altitud en metros</span><span class="sxs-lookup"><span data-stu-id="408d6-127">Accuracy of altitude in meters</span></span>|
|<span data-ttu-id="408d6-128">rumbo</span><span class="sxs-lookup"><span data-stu-id="408d6-128">heading</span></span>|<span data-ttu-id="408d6-129">Doble</span><span class="sxs-lookup"><span data-stu-id="408d6-129">Double</span></span>|<span data-ttu-id="408d6-130">Rumbo en grados desde el norte geográfico</span><span class="sxs-lookup"><span data-stu-id="408d6-130">Heading in degrees from true north</span></span>|
|<span data-ttu-id="408d6-131">velocidad</span><span class="sxs-lookup"><span data-stu-id="408d6-131">speed</span></span>|<span data-ttu-id="408d6-132">Doble</span><span class="sxs-lookup"><span data-stu-id="408d6-132">Double</span></span>|<span data-ttu-id="408d6-133">La velocidad a la que se desplaza el dispositivo en metros por segundo</span><span class="sxs-lookup"><span data-stu-id="408d6-133">Speed the device is traveling in meters per second</span></span>|

## <a name="relationships"></a><span data-ttu-id="408d6-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="408d6-134">Relationships</span></span>
<span data-ttu-id="408d6-135">Ninguna</span><span class="sxs-lookup"><span data-stu-id="408d6-135">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="408d6-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="408d6-136">JSON Representation</span></span>
<span data-ttu-id="408d6-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="408d6-137">Here is a JSON representation of the resource.</span></span>
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



