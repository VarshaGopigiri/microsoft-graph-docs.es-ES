---
title: tipo de recurso filterOperatorSchema
description: Describe un operador que se puede usar en un filtro.
localization_priority: Normal
ms.openlocfilehash: 0d26fb58b77369b70ab185fa8ad5214d6b6c1e71
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27848282"
---
# <a name="filteroperatorschema-resource-type"></a><span data-ttu-id="fb503-103">tipo de recurso filterOperatorSchema</span><span class="sxs-lookup"><span data-stu-id="fb503-103">filterOperatorSchema resource type</span></span>

> <span data-ttu-id="fb503-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fb503-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fb503-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fb503-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fb503-106">Describe un operador que se puede usar en un [filtro](synchronization-filter.md).</span><span class="sxs-lookup"><span data-stu-id="fb503-106">Describes an operator that can be used in a [filter](synchronization-filter.md).</span></span>

## <a name="properties"></a><span data-ttu-id="fb503-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb503-107">Properties</span></span>

| <span data-ttu-id="fb503-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb503-108">Property</span></span>                   | <span data-ttu-id="fb503-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb503-109">Type</span></span>                      | <span data-ttu-id="fb503-110">Description</span><span class="sxs-lookup"><span data-stu-id="fb503-110">Description</span></span>    |
|:---------------------------|:--------------------------|:---------------|
|<span data-ttu-id="fb503-111">aridad</span><span class="sxs-lookup"><span data-stu-id="fb503-111">arity</span></span>                       |<span data-ttu-id="fb503-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="fb503-112">String</span></span>          |<span data-ttu-id="fb503-113">Aridad del operador.</span><span class="sxs-lookup"><span data-stu-id="fb503-113">Arity of the operator.</span></span> <span data-ttu-id="fb503-114">Los valores posibles son: `Binary` y `Unary`.</span><span class="sxs-lookup"><span data-stu-id="fb503-114">Possible values are: `Binary`, `Unary`.</span></span> <span data-ttu-id="fb503-115">El valor predeterminado es `Binary`.</span><span class="sxs-lookup"><span data-stu-id="fb503-115">The default is `Binary`.</span></span>|
|<span data-ttu-id="fb503-116">multivaluedComparisonType</span><span class="sxs-lookup"><span data-stu-id="fb503-116">multivaluedComparisonType</span></span>   |<span data-ttu-id="fb503-117">scopeOperatorMultiValuedComparisonType</span><span class="sxs-lookup"><span data-stu-id="fb503-117">scopeOperatorMultiValuedComparisonType</span></span>          |<span data-ttu-id="fb503-118">Los valores posibles son: `All` y `Any`.</span><span class="sxs-lookup"><span data-stu-id="fb503-118">Possible values are: `All`, `Any`.</span></span> <span data-ttu-id="fb503-119">Se aplica sólo a los atributos de múltiples valores.</span><span class="sxs-lookup"><span data-stu-id="fb503-119">Applies only to multivalued attributes.</span></span> <span data-ttu-id="fb503-120">`All`significa que todos los valores deben satisfacer la condición.</span><span class="sxs-lookup"><span data-stu-id="fb503-120">`All` means that all values must satisfy the condition.</span></span> <span data-ttu-id="fb503-121">`Any`significa que tiene al menos un valor satisfacer la condición.</span><span class="sxs-lookup"><span data-stu-id="fb503-121">`Any` means that at least one value has to satisfy the condition.</span></span> <span data-ttu-id="fb503-122">El valor predeterminado es `All`.</span><span class="sxs-lookup"><span data-stu-id="fb503-122">The default is `All`.</span></span>|
|<span data-ttu-id="fb503-123">name</span><span class="sxs-lookup"><span data-stu-id="fb503-123">name</span></span>                        |<span data-ttu-id="fb503-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="fb503-124">String</span></span>                     |<span data-ttu-id="fb503-125">Nombre del operador.</span><span class="sxs-lookup"><span data-stu-id="fb503-125">Operator name.</span></span> |
|<span data-ttu-id="fb503-126">supportedAttributeTypes</span><span class="sxs-lookup"><span data-stu-id="fb503-126">supportedAttributeTypes</span></span>     |<span data-ttu-id="fb503-127">Colección String</span><span class="sxs-lookup"><span data-stu-id="fb503-127">String collection</span></span>         |<span data-ttu-id="fb503-128">Tipos admitidos por el operador de atributo.</span><span class="sxs-lookup"><span data-stu-id="fb503-128">Attribute types supported by the operator.</span></span> <span data-ttu-id="fb503-129">Los valores posibles son: `Boolean`, `Binary`, `Reference`, `Integer` y `String`.</span><span class="sxs-lookup"><span data-stu-id="fb503-129">Possible values are: `Boolean`, `Binary`, `Reference`, `Integer`, `String`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="fb503-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fb503-130">JSON representation</span></span>

<span data-ttu-id="fb503-131">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fb503-131">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.filterOperatorSchema"
}-->

```json
{
  "arity": "String",
  "multivaluedComparisonType": "String",
  "name": "String",
  "supportedAttributeTypes": ["String"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "filterOperatorSchema resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
