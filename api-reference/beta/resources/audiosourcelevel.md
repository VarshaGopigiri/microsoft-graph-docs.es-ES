---
title: tipo de recurso audioSourceLevel
description: Configuración de nivel para otros orígenes.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: adf3c4805271d0a8d02d25fc8e7ecb547db10215
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880643"
---
# <a name="audiosourcelevel-resource-type"></a><span data-ttu-id="251dd-103">tipo de recurso audioSourceLevel</span><span class="sxs-lookup"><span data-stu-id="251dd-103">audioSourceLevel resource type</span></span>

> <span data-ttu-id="251dd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="251dd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="251dd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="251dd-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="251dd-106">Configuración de nivel para otros orígenes.</span><span class="sxs-lookup"><span data-stu-id="251dd-106">Level configuration for other sources.</span></span>

## <a name="properties"></a><span data-ttu-id="251dd-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="251dd-107">Properties</span></span>

| <span data-ttu-id="251dd-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="251dd-108">Property</span></span>               | <span data-ttu-id="251dd-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="251dd-109">Type</span></span>    | <span data-ttu-id="251dd-110">Description</span><span class="sxs-lookup"><span data-stu-id="251dd-110">Description</span></span>                                                                                         |
| :--------------------- | :------ | :---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="251dd-111">duckOthers</span><span class="sxs-lookup"><span data-stu-id="251dd-111">duckOthers</span></span>             | <span data-ttu-id="251dd-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="251dd-112">Boolean</span></span> | <span data-ttu-id="251dd-113">Permite que este origen agacha otros orígenes mientras está activa.</span><span class="sxs-lookup"><span data-stu-id="251dd-113">Enables this source to duck other sources while active.</span></span> <span data-ttu-id="251dd-114">Si se establece en true, nivel de sobra se ha establecido.</span><span class="sxs-lookup"><span data-stu-id="251dd-114">If set to true, ducking level has to be set.</span></span>|
| <span data-ttu-id="251dd-115">nivel</span><span class="sxs-lookup"><span data-stu-id="251dd-115">level</span></span>                  | <span data-ttu-id="251dd-116">Int64</span><span class="sxs-lookup"><span data-stu-id="251dd-116">Int64</span></span>   | <span data-ttu-id="251dd-117">Nivel de la fuente de sobra si `duckOthers` está establecida en `true`.</span><span class="sxs-lookup"><span data-stu-id="251dd-117">Ducking level of the source if `duckOthers` is set to `true`.</span></span>                                     |
| <span data-ttu-id="251dd-118">participante</span><span class="sxs-lookup"><span data-stu-id="251dd-118">participant</span></span>            | <span data-ttu-id="251dd-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="251dd-119">String</span></span>  | <span data-ttu-id="251dd-120">La secuencia de audio participantes de origen.</span><span class="sxs-lookup"><span data-stu-id="251dd-120">The source participant audio stream.</span></span>                                                                |

## <a name="json-representation"></a><span data-ttu-id="251dd-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="251dd-121">JSON representation</span></span>

<span data-ttu-id="251dd-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="251dd-122">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.audioSourceLevel"
}-->
```json
{
  "duckOthers": true,
  "level": 100,
  "participant": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "audioSourceLevel resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
