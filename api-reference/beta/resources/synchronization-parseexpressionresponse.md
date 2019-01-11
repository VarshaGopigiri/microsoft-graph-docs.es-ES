---
title: tipo de recurso parseExpressionResponse
description: 'Representa la respuesta de la [synchronizationSchema: parseExpression](../api/synchronization_synchronizationschema_parseexpression.md) acción.'
localization_priority: Normal
ms.openlocfilehash: 550a46b0c27c2ca8d2d4c01baa975d8a204546f2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832952"
---
# <a name="parseexpressionresponse-resource-type"></a><span data-ttu-id="fa611-103">tipo de recurso parseExpressionResponse</span><span class="sxs-lookup"><span data-stu-id="fa611-103">parseExpressionResponse resource type</span></span>

> <span data-ttu-id="fa611-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fa611-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fa611-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fa611-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fa611-106">Representa la respuesta de la [synchronizationSchema: parseExpression](../api/synchronization_synchronizationschema_parseexpression.md) acción.</span><span class="sxs-lookup"><span data-stu-id="fa611-106">Represents the response from the [synchronizationSchema: parseExpression](../api/synchronization_synchronizationschema_parseexpression.md) action.</span></span>

## <a name="properties"></a><span data-ttu-id="fa611-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fa611-107">Properties</span></span>
| <span data-ttu-id="fa611-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fa611-108">Property</span></span>     | <span data-ttu-id="fa611-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa611-109">Type</span></span>   |<span data-ttu-id="fa611-110">Description</span><span class="sxs-lookup"><span data-stu-id="fa611-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fa611-111">error</span><span class="sxs-lookup"><span data-stu-id="fa611-111">error</span></span>|<span data-ttu-id="fa611-112">OData.Error</span><span class="sxs-lookup"><span data-stu-id="fa611-112">odata.error</span></span>|<span data-ttu-id="fa611-113">Detalles del error, si como resultado de la evaluación de expresiones en un error.</span><span class="sxs-lookup"><span data-stu-id="fa611-113">Error details, if expression evaluation resulted in an error.</span></span>|
|<span data-ttu-id="fa611-114">evaluationResult</span><span class="sxs-lookup"><span data-stu-id="fa611-114">evaluationResult</span></span>|<span data-ttu-id="fa611-115">Colección String</span><span class="sxs-lookup"><span data-stu-id="fa611-115">String collection</span></span>|<span data-ttu-id="fa611-116">Una colección de valores generados por la evaluación de la expresión.</span><span class="sxs-lookup"><span data-stu-id="fa611-116">A collection of values produced by the evaluation of the expression.</span></span>|
|<span data-ttu-id="fa611-117">evaluationSucceeded</span><span class="sxs-lookup"><span data-stu-id="fa611-117">evaluationSucceeded</span></span>|<span data-ttu-id="fa611-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa611-118">Boolean</span></span>|<span data-ttu-id="fa611-119">`true`Si la evaluación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fa611-119">`true` if the evaluation was successful.</span></span>|
|<span data-ttu-id="fa611-120">parsedExpression</span><span class="sxs-lookup"><span data-stu-id="fa611-120">parsedExpression</span></span>|[<span data-ttu-id="fa611-121">attributeMappingSource</span><span class="sxs-lookup"><span data-stu-id="fa611-121">attributeMappingSource</span></span>](synchronization-attributemappingsource.md)|<span data-ttu-id="fa611-122">Un objeto [attributeMappingSource](synchronization-attributemappingsource.md) que representa la expresión analizada.</span><span class="sxs-lookup"><span data-stu-id="fa611-122">An [attributeMappingSource](synchronization-attributemappingsource.md) object representing the parsed expression.</span></span>|
|<span data-ttu-id="fa611-123">parsingSucceeded</span><span class="sxs-lookup"><span data-stu-id="fa611-123">parsingSucceeded</span></span>|<span data-ttu-id="fa611-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa611-124">Boolean</span></span>|<span data-ttu-id="fa611-125">`true`Si la expresión se ha analizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="fa611-125">`true` if the expression was parsed successfully.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="fa611-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fa611-126">JSON representation</span></span>

<span data-ttu-id="fa611-127">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fa611-127">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.parseExpressionResponse"
}-->

```json
{
  "error": {"@odata.type": "microsoft.graph.publicError"},
  "evaluationResult": ["String"],
  "evaluationSucceeded": true,
  "parsedExpression": {"@odata.type": "microsoft.graph.attributeMappingSource"},
  "parsingSucceeded": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "parseExpressionResponse resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
