---
title: tipo de recurso audioDuckingConfiguration
description: Parámetros de sobra de otros orígenes (introducir paulatinamente dentro y fuera de otros orígenes).
ms.openlocfilehash: 16003933bc2436c333a80754eb9c4d5d9049172c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091171"
---
# <a name="audioduckingconfiguration-resource-type"></a><span data-ttu-id="36efa-103">tipo de recurso audioDuckingConfiguration</span><span class="sxs-lookup"><span data-stu-id="36efa-103">audioDuckingConfiguration resource type</span></span>

> <span data-ttu-id="36efa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="36efa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="36efa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="36efa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="36efa-106">Parámetros de sobra de otros orígenes (introducir paulatinamente dentro y fuera de otros orígenes).</span><span class="sxs-lookup"><span data-stu-id="36efa-106">Parameters for ducking of other sources (phasing in and out of other sources.)</span></span>

## <a name="properties"></a><span data-ttu-id="36efa-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36efa-107">Properties</span></span>

| <span data-ttu-id="36efa-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="36efa-108">Property</span></span>      | <span data-ttu-id="36efa-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="36efa-109">Type</span></span>     | <span data-ttu-id="36efa-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="36efa-110">Description</span></span>                                                                     |
| :------------ | :------- | :-------------------------------------------------------------------------------|
| <span data-ttu-id="36efa-111">lowerLevel</span><span class="sxs-lookup"><span data-stu-id="36efa-111">lowerLevel</span></span>    | <span data-ttu-id="36efa-112">Int64</span><span class="sxs-lookup"><span data-stu-id="36efa-112">Int64</span></span>    | <span data-ttu-id="36efa-113">El volumen de orígenes en por ciento cuando se va a ducked los orígenes.</span><span class="sxs-lookup"><span data-stu-id="36efa-113">The volume of sources in percent when the sources are being ducked.</span></span>             |
| <span data-ttu-id="36efa-114">rampActive</span><span class="sxs-lookup"><span data-stu-id="36efa-114">rampActive</span></span>    | <span data-ttu-id="36efa-115">Int64</span><span class="sxs-lookup"><span data-stu-id="36efa-115">Int64</span></span>    | <span data-ttu-id="36efa-116">La cantidad de tiempo (en milisegundos) que tarda orígenes ducked "desaparecer".</span><span class="sxs-lookup"><span data-stu-id="36efa-116">The amount of time (in milliseconds) it takes for ducked sources to "fade out".</span></span> |
| <span data-ttu-id="36efa-117">rampInactive</span><span class="sxs-lookup"><span data-stu-id="36efa-117">rampInactive</span></span>  | <span data-ttu-id="36efa-118">Int64</span><span class="sxs-lookup"><span data-stu-id="36efa-118">Int64</span></span>    | <span data-ttu-id="36efa-119">La cantidad de tiempo (en milisegundos) que tarda orígenes ducked a "desaparecer".</span><span class="sxs-lookup"><span data-stu-id="36efa-119">The amount of time (in milliseconds) it takes for ducked sources to "fade in".</span></span>  |
| <span data-ttu-id="36efa-120">upperLevel</span><span class="sxs-lookup"><span data-stu-id="36efa-120">upperLevel</span></span>    | <span data-ttu-id="36efa-121">Int64</span><span class="sxs-lookup"><span data-stu-id="36efa-121">Int64</span></span>    | <span data-ttu-id="36efa-122">El volumen de orígenes en por ciento cuando no se están ducked los orígenes.</span><span class="sxs-lookup"><span data-stu-id="36efa-122">The volume of sources in percent when the sources are not being ducked.</span></span>         |

> <span data-ttu-id="36efa-123">**Nota:** Duración de mejorar no puede ser más de 5.000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="36efa-123">**Note:** Ramp duration cannot be more than 5,000 milliseconds.</span></span>

## <a name="json-representation"></a><span data-ttu-id="36efa-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="36efa-124">JSON representation</span></span>

<span data-ttu-id="36efa-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="36efa-125">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.audioDuckingConfiguration"
}-->
```json
{
  "lowerLevel": 20,
  "rampActive": 1000,
  "rampInactive": 1000,
  "upperLevel": 100
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "audioDuckingConfiguration resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
