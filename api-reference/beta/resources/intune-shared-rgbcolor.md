---
title: Tipo de recurso rgbColor
description: Color en RGB.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: fd734d2cb7c1c03cfdab62b8a8f1acd9acac6814
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846728"
---
# <a name="rgbcolor-resource-type"></a><span data-ttu-id="2f54d-103">Tipo de recurso rgbColor</span><span class="sxs-lookup"><span data-stu-id="2f54d-103">rgbColor resource type</span></span>

> <span data-ttu-id="2f54d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2f54d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2f54d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2f54d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2f54d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2f54d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2f54d-107">Color en RGB.</span><span class="sxs-lookup"><span data-stu-id="2f54d-107">Color in RGB.</span></span>
## <a name="properties"></a><span data-ttu-id="2f54d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2f54d-108">Properties</span></span>
|<span data-ttu-id="2f54d-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2f54d-109">Property</span></span>|<span data-ttu-id="2f54d-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f54d-110">Type</span></span>|<span data-ttu-id="2f54d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f54d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2f54d-112">r</span><span class="sxs-lookup"><span data-stu-id="2f54d-112">r</span></span>|<span data-ttu-id="2f54d-113">Byte</span><span class="sxs-lookup"><span data-stu-id="2f54d-113">Byte</span></span>|<span data-ttu-id="2f54d-114">Valor Red (rojo)</span><span class="sxs-lookup"><span data-stu-id="2f54d-114">Red value</span></span>|
|<span data-ttu-id="2f54d-115">g</span><span class="sxs-lookup"><span data-stu-id="2f54d-115">g</span></span>|<span data-ttu-id="2f54d-116">Byte</span><span class="sxs-lookup"><span data-stu-id="2f54d-116">Byte</span></span>|<span data-ttu-id="2f54d-117">Valor Green (verde)</span><span class="sxs-lookup"><span data-stu-id="2f54d-117">Green value</span></span>|
|<span data-ttu-id="2f54d-118">b</span><span class="sxs-lookup"><span data-stu-id="2f54d-118">b</span></span>|<span data-ttu-id="2f54d-119">Byte</span><span class="sxs-lookup"><span data-stu-id="2f54d-119">Byte</span></span>|<span data-ttu-id="2f54d-120">Valor Blue (azul)</span><span class="sxs-lookup"><span data-stu-id="2f54d-120">Blue value</span></span>|

## <a name="relationships"></a><span data-ttu-id="2f54d-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2f54d-121">Relationships</span></span>
<span data-ttu-id="2f54d-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2f54d-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2f54d-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2f54d-123">JSON Representation</span></span>
<span data-ttu-id="2f54d-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2f54d-124">Here is a JSON representation of the resource.</span></span>
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





