---
title: Tipo de recurso iosMinimumOperatingSystem
description: Contiene las propiedades del sistema operativo mínimo necesario para una aplicación móvil de iOS.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7243b337a53cca31054f99ae807e5c17cdd3e372
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876274"
---
# <a name="iosminimumoperatingsystem-resource-type"></a><span data-ttu-id="34bee-103">Tipo de recurso iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="34bee-103">iosMinimumOperatingSystem resource type</span></span>

> <span data-ttu-id="34bee-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="34bee-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="34bee-105">Contiene las propiedades del sistema operativo mínimo necesario para una aplicación móvil de iOS.</span><span class="sxs-lookup"><span data-stu-id="34bee-105">Contains properties of the minimum operating system required for an iOS mobile app.</span></span>
## <a name="properties"></a><span data-ttu-id="34bee-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="34bee-106">Properties</span></span>
|<span data-ttu-id="34bee-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="34bee-107">Property</span></span>|<span data-ttu-id="34bee-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="34bee-108">Type</span></span>|<span data-ttu-id="34bee-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="34bee-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="34bee-110">v8_0</span><span class="sxs-lookup"><span data-stu-id="34bee-110">v8_0</span></span>|<span data-ttu-id="34bee-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="34bee-111">Boolean</span></span>|<span data-ttu-id="34bee-112">Versión 8.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="34bee-112">Version 8.0 or later.</span></span>|
|<span data-ttu-id="34bee-113">v9_0</span><span class="sxs-lookup"><span data-stu-id="34bee-113">v9_0</span></span>|<span data-ttu-id="34bee-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="34bee-114">Boolean</span></span>|<span data-ttu-id="34bee-115">Versión 9.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="34bee-115">Version 9.0 or later.</span></span>|
|<span data-ttu-id="34bee-116">v10_0</span><span class="sxs-lookup"><span data-stu-id="34bee-116">v10_0</span></span>|<span data-ttu-id="34bee-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="34bee-117">Boolean</span></span>|<span data-ttu-id="34bee-118">Versión 10.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="34bee-118">Version 10.0 or later.</span></span>|
|<span data-ttu-id="34bee-119">v11_0</span><span class="sxs-lookup"><span data-stu-id="34bee-119">v11_0</span></span>|<span data-ttu-id="34bee-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="34bee-120">Boolean</span></span>|<span data-ttu-id="34bee-121">Versión 11.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="34bee-121">Version 11.0 or later.</span></span>|
|<span data-ttu-id="34bee-122">v12_0</span><span class="sxs-lookup"><span data-stu-id="34bee-122">v12_0</span></span>|<span data-ttu-id="34bee-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="34bee-123">Boolean</span></span>|<span data-ttu-id="34bee-124">Versión 12.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="34bee-124">Version 12.0 or later.</span></span>|

## <a name="relationships"></a><span data-ttu-id="34bee-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="34bee-125">Relationships</span></span>
<span data-ttu-id="34bee-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="34bee-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="34bee-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="34bee-127">JSON Representation</span></span>
<span data-ttu-id="34bee-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="34bee-128">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosMinimumOperatingSystem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosMinimumOperatingSystem",
  "v8_0": true,
  "v9_0": true,
  "v10_0": true,
  "v11_0": true,
  "v12_0": true
}
```



