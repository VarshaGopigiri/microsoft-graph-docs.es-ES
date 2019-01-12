---
title: Tipo de recurso rgbColor
description: Color en RGB.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: fc40b5cc2ffff02bed89847386db6398f76b3953
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967010"
---
# <a name="rgbcolor-resource-type"></a><span data-ttu-id="9b4dd-103">Tipo de recurso rgbColor</span><span class="sxs-lookup"><span data-stu-id="9b4dd-103">rgbColor resource type</span></span>

> <span data-ttu-id="9b4dd-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9b4dd-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9b4dd-105">Color en RGB.</span><span class="sxs-lookup"><span data-stu-id="9b4dd-105">Color in RGB.</span></span>
## <a name="properties"></a><span data-ttu-id="9b4dd-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b4dd-106">Properties</span></span>
|<span data-ttu-id="9b4dd-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9b4dd-107">Property</span></span>|<span data-ttu-id="9b4dd-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b4dd-108">Type</span></span>|<span data-ttu-id="9b4dd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b4dd-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9b4dd-110">r</span><span class="sxs-lookup"><span data-stu-id="9b4dd-110">r</span></span>|<span data-ttu-id="9b4dd-111">Byte</span><span class="sxs-lookup"><span data-stu-id="9b4dd-111">Byte</span></span>|<span data-ttu-id="9b4dd-112">Valor Red (rojo)</span><span class="sxs-lookup"><span data-stu-id="9b4dd-112">Red value</span></span>|
|<span data-ttu-id="9b4dd-113">g</span><span class="sxs-lookup"><span data-stu-id="9b4dd-113">g</span></span>|<span data-ttu-id="9b4dd-114">Byte</span><span class="sxs-lookup"><span data-stu-id="9b4dd-114">Byte</span></span>|<span data-ttu-id="9b4dd-115">Valor Green (verde)</span><span class="sxs-lookup"><span data-stu-id="9b4dd-115">Green value</span></span>|
|<span data-ttu-id="9b4dd-116">b</span><span class="sxs-lookup"><span data-stu-id="9b4dd-116">b</span></span>|<span data-ttu-id="9b4dd-117">Byte</span><span class="sxs-lookup"><span data-stu-id="9b4dd-117">Byte</span></span>|<span data-ttu-id="9b4dd-118">Valor Blue (azul)</span><span class="sxs-lookup"><span data-stu-id="9b4dd-118">Blue value</span></span>|

## <a name="relationships"></a><span data-ttu-id="9b4dd-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9b4dd-119">Relationships</span></span>
<span data-ttu-id="9b4dd-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9b4dd-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9b4dd-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9b4dd-121">JSON Representation</span></span>
<span data-ttu-id="9b4dd-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9b4dd-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.rgbColor"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.rgbColor",
  "r": 1024,
  "g": 1024,
  "b": 1024
}
```



