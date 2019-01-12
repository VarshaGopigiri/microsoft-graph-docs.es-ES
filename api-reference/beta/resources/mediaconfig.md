---
title: tipo de recurso mediaConfig
description: Configuración de medios que se usa para conectarse a una llamada.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 74b3b5dc4c71db80e94216756a3513a03011572a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27948922"
---
# <a name="mediaconfig-resource-type"></a><span data-ttu-id="7e63b-103">tipo de recurso mediaConfig</span><span class="sxs-lookup"><span data-stu-id="7e63b-103">mediaConfig resource type</span></span>

> <span data-ttu-id="7e63b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7e63b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7e63b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7e63b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7e63b-106">Configuración de medios que se usa para conectarse a una llamada.</span><span class="sxs-lookup"><span data-stu-id="7e63b-106">The media configuration used to connect to a call.</span></span>

## <a name="properties"></a><span data-ttu-id="7e63b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e63b-107">Properties</span></span>

| <span data-ttu-id="7e63b-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7e63b-108">Property</span></span>       | <span data-ttu-id="7e63b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e63b-109">Type</span></span>    | <span data-ttu-id="7e63b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e63b-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7e63b-111">removeFromDefaultAudioGroup</span><span class="sxs-lookup"><span data-stu-id="7e63b-111">removeFromDefaultAudioGroup</span></span> | <span data-ttu-id="7e63b-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="7e63b-112">Boolean</span></span> |  |

## <a name="json-representation"></a><span data-ttu-id="7e63b-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7e63b-113">JSON representation</span></span>

<span data-ttu-id="7e63b-114">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7e63b-114">The following is a JSON representation of the resource.</span></span>

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
