---
title: tipo de recurso mediaInfo
description: Solicita la información de medios utilizada en las acciones para.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 217b9a5aaa88a1bbf343447fad344b322cfeb611
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924534"
---
# <a name="mediainfo-resource-type"></a><span data-ttu-id="753d4-103">tipo de recurso mediaInfo</span><span class="sxs-lookup"><span data-stu-id="753d4-103">mediaInfo resource type</span></span>

> <span data-ttu-id="753d4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="753d4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="753d4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="753d4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="753d4-106">Solicita la información de medios utilizada en las acciones para.</span><span class="sxs-lookup"><span data-stu-id="753d4-106">The media information used in actions for prompts.</span></span>

## <a name="properties"></a><span data-ttu-id="753d4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="753d4-107">Properties</span></span>
| <span data-ttu-id="753d4-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="753d4-108">Property</span></span>       | <span data-ttu-id="753d4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="753d4-109">Type</span></span>    | <span data-ttu-id="753d4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="753d4-110">Description</span></span>                      |
|:---------------|:--------|:---------------------------------|
| <span data-ttu-id="753d4-111">resourceId</span><span class="sxs-lookup"><span data-stu-id="753d4-111">resourceId</span></span>     | <span data-ttu-id="753d4-112">cadena</span><span class="sxs-lookup"><span data-stu-id="753d4-112">String</span></span>  | <span data-ttu-id="753d4-113">Identidad única del recurso.</span><span class="sxs-lookup"><span data-stu-id="753d4-113">Unique identity of the resource.</span></span> |
| <span data-ttu-id="753d4-114">URI</span><span class="sxs-lookup"><span data-stu-id="753d4-114">uri</span></span>            | <span data-ttu-id="753d4-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="753d4-115">String</span></span>  | <span data-ttu-id="753d4-116">Ruta de acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="753d4-116">Path to the resource.</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="753d4-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="753d4-117">JSON representation</span></span>

<span data-ttu-id="753d4-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="753d4-118">The following is a JSON representation of the resource.</span></span>

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
