---
title: tipo de recurso stringKeyAttributeMappingSourceValuePair
description: Representa un par de clave y valor donde la clave es una cadena y el valor es attributeMappingSource.
localization_priority: Normal
ms.openlocfilehash: 24695cc64fd3c240d5416a7b37e9a5d373e5a88a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805092"
---
# <a name="stringkeyattributemappingsourcevaluepair-resource-type"></a><span data-ttu-id="b9a8c-103">tipo de recurso stringKeyAttributeMappingSourceValuePair</span><span class="sxs-lookup"><span data-stu-id="b9a8c-103">stringKeyAttributeMappingSourceValuePair resource type</span></span>

> <span data-ttu-id="b9a8c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b9a8c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b9a8c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b9a8c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b9a8c-106">Representa un par de clave y valor donde la clave es una cadena y el valor es [attributeMappingSource](synchronization-attributemappingsource.md).</span><span class="sxs-lookup"><span data-stu-id="b9a8c-106">Represents a key-value pair where the key is a string and the value is [attributeMappingSource](synchronization-attributemappingsource.md).</span></span>

## <a name="properties"></a><span data-ttu-id="b9a8c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9a8c-107">Properties</span></span>
| <span data-ttu-id="b9a8c-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b9a8c-108">Property</span></span>     | <span data-ttu-id="b9a8c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9a8c-109">Type</span></span>   |<span data-ttu-id="b9a8c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9a8c-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b9a8c-111">Key</span><span class="sxs-lookup"><span data-stu-id="b9a8c-111">key</span></span>|<span data-ttu-id="b9a8c-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="b9a8c-112">String</span></span>|<span data-ttu-id="b9a8c-113">Nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="b9a8c-113">The name of the parameter.</span></span>|
|<span data-ttu-id="b9a8c-114">valor</span><span class="sxs-lookup"><span data-stu-id="b9a8c-114">value</span></span>|[<span data-ttu-id="b9a8c-115">attributeMappingSource</span><span class="sxs-lookup"><span data-stu-id="b9a8c-115">attributeMappingSource</span></span>](synchronization-attributemappingsource.md)|<span data-ttu-id="b9a8c-116">El valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="b9a8c-116">The value of the parameter.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b9a8c-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b9a8c-117">JSON representation</span></span>

<span data-ttu-id="b9a8c-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b9a8c-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.stringKeyAttributeMappingSourceValuePair"
}-->

```json
{
  "key": "String",
  "value": {"@odata.type": "microsoft.graph.attributeMappingSource"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "stringKeyAttributeMappingSourceValuePair resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
