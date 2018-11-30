---
title: Tipo de recurso windowsMinimumOperatingSystem
description: El sistema operativo mínimo necesario para una aplicación móvil de Windows.
ms.openlocfilehash: 077ac386c9f40ca4426f98490241015072b487f7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032044"
---
# <a name="windowsminimumoperatingsystem-resource-type"></a><span data-ttu-id="2739d-103">Tipo de recurso windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2739d-103">windowsMinimumOperatingSystem resource type</span></span>

> <span data-ttu-id="2739d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2739d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2739d-105">El sistema operativo mínimo necesario para una aplicación móvil de Windows.</span><span class="sxs-lookup"><span data-stu-id="2739d-105">The minimum operating system required for a Windows mobile app.</span></span>
## <a name="properties"></a><span data-ttu-id="2739d-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2739d-106">Properties</span></span>
|<span data-ttu-id="2739d-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2739d-107">Property</span></span>|<span data-ttu-id="2739d-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2739d-108">Type</span></span>|<span data-ttu-id="2739d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2739d-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2739d-110">v8_0</span><span class="sxs-lookup"><span data-stu-id="2739d-110">v8_0</span></span>|<span data-ttu-id="2739d-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="2739d-111">Boolean</span></span>|<span data-ttu-id="2739d-112">Windows versión 8.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2739d-112">Windows version 8.0 or later.</span></span>|
|<span data-ttu-id="2739d-113">v8_1</span><span class="sxs-lookup"><span data-stu-id="2739d-113">v8_1</span></span>|<span data-ttu-id="2739d-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="2739d-114">Boolean</span></span>|<span data-ttu-id="2739d-115">Windows versión 8.1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2739d-115">Windows version 8.1 or later.</span></span>|
|<span data-ttu-id="2739d-116">v10_0</span><span class="sxs-lookup"><span data-stu-id="2739d-116">v10_0</span></span>|<span data-ttu-id="2739d-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="2739d-117">Boolean</span></span>|<span data-ttu-id="2739d-118">Windows versión 10.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2739d-118">Windows version 10.0 or later.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2739d-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2739d-119">Relationships</span></span>
<span data-ttu-id="2739d-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2739d-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2739d-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2739d-121">JSON Representation</span></span>
<span data-ttu-id="2739d-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2739d-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsMinimumOperatingSystem",
  "v8_0": true,
  "v8_1": true,
  "v10_0": true
}
```



