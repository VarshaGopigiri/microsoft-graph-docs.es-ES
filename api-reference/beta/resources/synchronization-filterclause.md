---
title: tipo de recurso filterClause
description: Representa una aserción único que debe cumplir un objeto candidato y se evalúa alguna `true` (objeto cumple la aserción) o `false` (objeto no cumplen con la aserción).
localization_priority: Normal
ms.openlocfilehash: 89807a6086f661388c8d5b1d5f82bfe973c3af39
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833862"
---
# <a name="filterclause-resource-type"></a><span data-ttu-id="77abc-103">tipo de recurso filterClause</span><span class="sxs-lookup"><span data-stu-id="77abc-103">filterClause resource type</span></span>

> <span data-ttu-id="77abc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="77abc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="77abc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="77abc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="77abc-106">Representa una aserción único que debe cumplir un objeto candidato y se evalúa alguna `true` (objeto cumple la aserción) o `false` (objeto no cumplen con la aserción).</span><span class="sxs-lookup"><span data-stu-id="77abc-106">Represents a single assertion that a candidate object must satisfy, and is evaluated to either `true` (object satisfies the assertion) or `false` (object does not satisfy the assertion).</span></span>

## <a name="properties"></a><span data-ttu-id="77abc-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="77abc-107">Properties</span></span>
| <span data-ttu-id="77abc-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="77abc-108">Property</span></span>     | <span data-ttu-id="77abc-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="77abc-109">Type</span></span>   |<span data-ttu-id="77abc-110">Description</span><span class="sxs-lookup"><span data-stu-id="77abc-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="77abc-111">operatorName</span><span class="sxs-lookup"><span data-stu-id="77abc-111">operatorName</span></span>|<span data-ttu-id="77abc-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="77abc-112">String</span></span>|<span data-ttu-id="77abc-113">Nombre del operador que se aplicará a los operandos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="77abc-113">Name of the operator to be applied to the source and target operands.</span></span> <span data-ttu-id="77abc-114">Debe ser uno de los operadores compatibles.</span><span class="sxs-lookup"><span data-stu-id="77abc-114">Must be one of the supported operators.</span></span> <span data-ttu-id="77abc-115">Se pueden detectar los operadores compatibles.</span><span class="sxs-lookup"><span data-stu-id="77abc-115">Supported operators can be discovered.</span></span>|
|<span data-ttu-id="77abc-116">sourceOperandName</span><span class="sxs-lookup"><span data-stu-id="77abc-116">sourceOperandName</span></span>|<span data-ttu-id="77abc-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="77abc-117">String</span></span>|<span data-ttu-id="77abc-118">Nombre del operando de origen (el operando que se está probando).</span><span class="sxs-lookup"><span data-stu-id="77abc-118">Name of source operand (the operand being tested).</span></span> <span data-ttu-id="77abc-119">El nombre del operando de origen debe coincidir con uno de los nombres de atributo en el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="77abc-119">The source operand name must match one of the attribute names on the source object.</span></span>|
|<span data-ttu-id="77abc-120">targetOperand</span><span class="sxs-lookup"><span data-stu-id="77abc-120">targetOperand</span></span>|[<span data-ttu-id="77abc-121">filterOperand</span><span class="sxs-lookup"><span data-stu-id="77abc-121">filterOperand</span></span>](synchronization-filteroperand.md)|<span data-ttu-id="77abc-122">Valores que se probará contra el operando de origen.</span><span class="sxs-lookup"><span data-stu-id="77abc-122">Values that the source operand will be tested against.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="77abc-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="77abc-123">JSON representation</span></span>

<span data-ttu-id="77abc-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="77abc-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.filterClause"
}-->

```json
{
  "operatorName": "String",
  "sourceOperandName": "String",
  "targetOperand": {"@odata.type": "microsoft.graph.filterOperand"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "filterClause resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
