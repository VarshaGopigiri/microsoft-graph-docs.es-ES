---
title: tipo de recurso mediaConfig
description: Configuración de medios que se usa para conectarse a una llamada.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: ec76adf2d3a508ebe2518ed0010a1c653daca546
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867351"
---
# <a name="mediaconfig-resource-type"></a><span data-ttu-id="e3020-103">tipo de recurso mediaConfig</span><span class="sxs-lookup"><span data-stu-id="e3020-103">mediaConfig resource type</span></span>

> <span data-ttu-id="e3020-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e3020-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e3020-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e3020-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e3020-106">Configuración de medios que se usa para conectarse a una llamada.</span><span class="sxs-lookup"><span data-stu-id="e3020-106">The media configuration used to connect to a call.</span></span>

## <a name="properties"></a><span data-ttu-id="e3020-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e3020-107">Properties</span></span>

| <span data-ttu-id="e3020-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e3020-108">Property</span></span>       | <span data-ttu-id="e3020-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3020-109">Type</span></span>    | <span data-ttu-id="e3020-110">Description</span><span class="sxs-lookup"><span data-stu-id="e3020-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="e3020-111">removeFromDefaultAudioGroup</span><span class="sxs-lookup"><span data-stu-id="e3020-111">removeFromDefaultAudioGroup</span></span> | <span data-ttu-id="e3020-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="e3020-112">Boolean</span></span> |  |

## <a name="json-representation"></a><span data-ttu-id="e3020-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e3020-113">JSON representation</span></span>

<span data-ttu-id="e3020-114">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e3020-114">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "removeFromDefaultAudioGroup"
  ],
  "@odata.type": "microsoft.graph.mediaConfig"
}-->
```json
{
  "removeFromDefaultAudioGroup": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mediaConfig resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
