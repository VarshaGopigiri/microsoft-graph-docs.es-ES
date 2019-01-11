---
title: tipo de recurso mediaInfo
description: Solicita la información de medios utilizada en las acciones para.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: 6fe2c49e86bac9d5961310694b21e9439a4896ab
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885606"
---
# <a name="mediainfo-resource-type"></a><span data-ttu-id="110c1-103">tipo de recurso mediaInfo</span><span class="sxs-lookup"><span data-stu-id="110c1-103">mediaInfo resource type</span></span>

> <span data-ttu-id="110c1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="110c1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="110c1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="110c1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="110c1-106">Solicita la información de medios utilizada en las acciones para.</span><span class="sxs-lookup"><span data-stu-id="110c1-106">The media information used in actions for prompts.</span></span>

## <a name="properties"></a><span data-ttu-id="110c1-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="110c1-107">Properties</span></span>
| <span data-ttu-id="110c1-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="110c1-108">Property</span></span>       | <span data-ttu-id="110c1-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="110c1-109">Type</span></span>    | <span data-ttu-id="110c1-110">Description</span><span class="sxs-lookup"><span data-stu-id="110c1-110">Description</span></span>                      |
|:---------------|:--------|:---------------------------------|
| <span data-ttu-id="110c1-111">resourceId</span><span class="sxs-lookup"><span data-stu-id="110c1-111">resourceId</span></span>     | <span data-ttu-id="110c1-112">cadena</span><span class="sxs-lookup"><span data-stu-id="110c1-112">String</span></span>  | <span data-ttu-id="110c1-113">Identidad única del recurso.</span><span class="sxs-lookup"><span data-stu-id="110c1-113">Unique identity of the resource.</span></span> |
| <span data-ttu-id="110c1-114">URI</span><span class="sxs-lookup"><span data-stu-id="110c1-114">uri</span></span>            | <span data-ttu-id="110c1-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="110c1-115">String</span></span>  | <span data-ttu-id="110c1-116">Ruta de acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="110c1-116">Path to the resource.</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="110c1-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="110c1-117">JSON representation</span></span>

<span data-ttu-id="110c1-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="110c1-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mediaInfo"
}-->
```json
{
  "resourceId": "String",
  "uri": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mediaInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
