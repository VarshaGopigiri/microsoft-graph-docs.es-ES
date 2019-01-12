---
title: tipo de recurso participantMixerLevel
description: Configuración del Mezclador de niveles para indicar participante de audio
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 9bf0788b1f7822311882cfa2133083d81deff16b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977790"
---
# <a name="participantmixerlevel-resource-type"></a><span data-ttu-id="6c15d-103">tipo de recurso participantMixerLevel</span><span class="sxs-lookup"><span data-stu-id="6c15d-103">participantMixerLevel resource type</span></span>

> <span data-ttu-id="6c15d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6c15d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6c15d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6c15d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6c15d-106">Configuración del Mezclador de niveles para indicar participante de audio</span><span class="sxs-lookup"><span data-stu-id="6c15d-106">Configuration of mixer levels for given audio participant</span></span>

## <a name="properties"></a><span data-ttu-id="6c15d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6c15d-107">Properties</span></span>

| <span data-ttu-id="6c15d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c15d-108">Property</span></span>               | <span data-ttu-id="6c15d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c15d-109">Type</span></span>                                                      | <span data-ttu-id="6c15d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c15d-110">Description</span></span>                                                                                         |
| :--------------------- | :-------------------------------------------------------- | :---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c15d-111">Evite</span><span class="sxs-lookup"><span data-stu-id="6c15d-111">ducking</span></span>                | [<span data-ttu-id="6c15d-112">audioDuckingConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c15d-112">audioDuckingConfiguration</span></span>](audioduckingconfiguration.md) | <span data-ttu-id="6c15d-113">Configuración de combinación personalizado (introducir paulatinamente de entrada y salida) de otras fuentes para este participante de sobra.</span><span class="sxs-lookup"><span data-stu-id="6c15d-113">Configuration of ducking (phasing in and out) of other sources for this partipant custom mix.</span></span>       |
| <span data-ttu-id="6c15d-114">exclusiveMode</span><span class="sxs-lookup"><span data-stu-id="6c15d-114">exclusiveMode</span></span>          | <span data-ttu-id="6c15d-115">boolean</span><span class="sxs-lookup"><span data-stu-id="6c15d-115">boolean</span></span>                                                   | <span data-ttu-id="6c15d-116">Si deben quitarse orígenes sin nivel de origen explícitas de la combinación.</span><span class="sxs-lookup"><span data-stu-id="6c15d-116">Whether sources without explicit source level should be removed from the mix.</span></span>                       |
| <span data-ttu-id="6c15d-117">participante</span><span class="sxs-lookup"><span data-stu-id="6c15d-117">participant</span></span>            | <span data-ttu-id="6c15d-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c15d-118">String</span></span>                                                    | <span data-ttu-id="6c15d-119">El participante para el que se está configurando el mezclador.</span><span class="sxs-lookup"><span data-stu-id="6c15d-119">The participant for whom the mixer is being configured.</span></span>                                             |
| <span data-ttu-id="6c15d-120">sourceLevels</span><span class="sxs-lookup"><span data-stu-id="6c15d-120">sourceLevels</span></span>           | <span data-ttu-id="6c15d-121">colección de [audioSourceLevel](audiosourcelevel.md)</span><span class="sxs-lookup"><span data-stu-id="6c15d-121">[audioSourceLevel](audiosourcelevel.md) collection</span></span>        | <span data-ttu-id="6c15d-122">Configuración de nivel para otros orígenes.</span><span class="sxs-lookup"><span data-stu-id="6c15d-122">Level configuration for other sources.</span></span>                                                              |

## <a name="json-representation"></a><span data-ttu-id="6c15d-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6c15d-123">JSON representation</span></span>

<span data-ttu-id="6c15d-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6c15d-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.participantMixerLevel"
}-->
```json
{
  "ducking": { "@odata.type": "#microsoft.graph.audioDuckingConfiguration" },
  "exclusiveMode": true,
  "participant": "String",
  "sourceLevels": [ { "@odata.type": "#microsoft.graph.audioSourceLevel" } ]
}
```

## <a name="example---mixer-level"></a><span data-ttu-id="6c15d-125">Por ejemplo, nivel de mezclador</span><span class="sxs-lookup"><span data-stu-id="6c15d-125">Example - Mixer level</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.participantMixerLevel"
}-->
```json
{
  "ducking": {
    "@odata.type": "#microsoft.graph.audioDuckingParameters",
    "rampActive": 1000,
    "rampInactive": 1000,
    "lowerLevel": 20,
    "upperLevel": 100
  },
  "exclusiveMode": true,
  "participant": "123456W77E24E4D85F80597083CB830",
  "sourceLevels": [
    {
      "@odata.type": "#microsoft.graph.audioSourceLevel",
      "duckOthers": false,
      "level": 100,
      "participant": "8A34A46B3D174ADC8DCEDC4E7D572698"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "participantMixerLevel resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
