---
title: tipo de recurso metadataEntry
description: Metadatos para el objeto dado.
localization_priority: Normal
ms.openlocfilehash: ffdb2dd3b6729320b5991b1158e10d145e339968
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27819484"
---
# <a name="metadataentry-resource-type"></a><span data-ttu-id="985b0-103">tipo de recurso metadataEntry</span><span class="sxs-lookup"><span data-stu-id="985b0-103">metadataEntry resource type</span></span>

> <span data-ttu-id="985b0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="985b0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="985b0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="985b0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="985b0-106">Metadatos para el objeto dado.</span><span class="sxs-lookup"><span data-stu-id="985b0-106">Metadata for the given object.</span></span>

## <a name="properties"></a><span data-ttu-id="985b0-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="985b0-107">Properties</span></span>
| <span data-ttu-id="985b0-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="985b0-108">Property</span></span>     | <span data-ttu-id="985b0-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="985b0-109">Type</span></span>   |<span data-ttu-id="985b0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="985b0-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="985b0-111">Key</span><span class="sxs-lookup"><span data-stu-id="985b0-111">key</span></span>|<span data-ttu-id="985b0-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="985b0-112">String</span></span>|<span data-ttu-id="985b0-113">Nombre de la propiedad de metadatos.</span><span class="sxs-lookup"><span data-stu-id="985b0-113">Name of the metadata property.</span></span>|
|<span data-ttu-id="985b0-114">valor</span><span class="sxs-lookup"><span data-stu-id="985b0-114">value</span></span>|<span data-ttu-id="985b0-115">String</span><span class="sxs-lookup"><span data-stu-id="985b0-115">String</span></span>|<span data-ttu-id="985b0-116">Valor de la propiedad de metadatos.</span><span class="sxs-lookup"><span data-stu-id="985b0-116">Value of the metadata property.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="985b0-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="985b0-117">JSON representation</span></span>

<span data-ttu-id="985b0-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="985b0-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.metadataEntry"
}-->

```json
{
  "key": "String",
  "value": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "metadataEntry resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
