---
title: tipo de recurso mediaConfig
description: Configuración de medios que se usa para conectarse a una llamada.
author: VinodRavichandran
ms.openlocfilehash: 1b68d9236ba78ae1a83228b3382c96fc81516d1f
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380264"
---
# <a name="mediaconfig-resource-type"></a><span data-ttu-id="d5b51-103">tipo de recurso mediaConfig</span><span class="sxs-lookup"><span data-stu-id="d5b51-103">mediaConfig resource type</span></span>

> <span data-ttu-id="d5b51-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d5b51-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d5b51-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d5b51-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d5b51-106">Configuración de medios que se usa para conectarse a una llamada.</span><span class="sxs-lookup"><span data-stu-id="d5b51-106">The media configuration used to connect to a call.</span></span>

## <a name="properties"></a><span data-ttu-id="d5b51-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d5b51-107">Properties</span></span>

| <span data-ttu-id="d5b51-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d5b51-108">Property</span></span>       | <span data-ttu-id="d5b51-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d5b51-109">Type</span></span>    | <span data-ttu-id="d5b51-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5b51-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="d5b51-111">removeFromDefaultAudioGroup</span><span class="sxs-lookup"><span data-stu-id="d5b51-111">removeFromDefaultAudioGroup</span></span> | <span data-ttu-id="d5b51-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="d5b51-112">Boolean</span></span> |  |

## <a name="json-representation"></a><span data-ttu-id="d5b51-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d5b51-113">JSON representation</span></span>

<span data-ttu-id="d5b51-114">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d5b51-114">The following is a JSON representation of the resource.</span></span>

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