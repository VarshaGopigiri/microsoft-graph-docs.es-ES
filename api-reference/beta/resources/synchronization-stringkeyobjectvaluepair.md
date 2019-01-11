---
title: tipo de recurso stringKeyObjectValuePair
description: Representa un par de clave y valor donde la clave es una cadena y el valor es un objeto JSON arbitrario. Esto es un tipo abierto de OData que espera tener una propiedad denominada `value` es un objeto JSON válido.
localization_priority: Normal
ms.openlocfilehash: 8545a4ef5a4931d3b886c95b4f39218bc418f53d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831454"
---
# <a name="stringkeyobjectvaluepair-resource-type"></a><span data-ttu-id="18656-104">tipo de recurso stringKeyObjectValuePair</span><span class="sxs-lookup"><span data-stu-id="18656-104">stringKeyObjectValuePair resource type</span></span>

> <span data-ttu-id="18656-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="18656-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="18656-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="18656-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="18656-107">Representa un par de clave y valor donde la clave es una cadena y el valor es un objeto JSON arbitrario.</span><span class="sxs-lookup"><span data-stu-id="18656-107">Represents a key-value pair where the key is a string and the value is an arbitrary JSON object.</span></span> <span data-ttu-id="18656-108">Esto es un tipo abierto de OData que espera tener una propiedad denominada `value` es un objeto JSON válido.</span><span class="sxs-lookup"><span data-stu-id="18656-108">This is an OData open type that expects to have a property named `value` that is a valid JSON object.</span></span>

## <a name="properties"></a><span data-ttu-id="18656-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="18656-109">Properties</span></span>
| <span data-ttu-id="18656-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="18656-110">Property</span></span>     | <span data-ttu-id="18656-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="18656-111">Type</span></span>   |<span data-ttu-id="18656-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="18656-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="18656-113">Key</span><span class="sxs-lookup"><span data-stu-id="18656-113">key</span></span>|<span data-ttu-id="18656-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="18656-114">String</span></span>|<span data-ttu-id="18656-115">Clave.</span><span class="sxs-lookup"><span data-stu-id="18656-115">Key.</span></span>|
|<span data-ttu-id="18656-116">valor</span><span class="sxs-lookup"><span data-stu-id="18656-116">value</span></span>|<span data-ttu-id="18656-117">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="18656-117">Any</span></span>|<span data-ttu-id="18656-118">Objeto JSON arbitrario.</span><span class="sxs-lookup"><span data-stu-id="18656-118">Arbitrary JSON object.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="18656-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="18656-119">JSON representation</span></span>

<span data-ttu-id="18656-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="18656-120">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.stringKeyObjectValuePair"
}-->

```json
{
  "key": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "stringKeyObjectValuePair resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
