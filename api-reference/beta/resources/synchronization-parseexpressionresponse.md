---
title: tipo de recurso parseExpressionResponse
description: 'Representa la respuesta de la [synchronizationSchema: parseExpression](../api/synchronization_synchronizationschema_parseexpression.md) acción.'
ms.openlocfilehash: 625df0ca16135eaa35c5b679c79dea582c4012e4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090192"
---
# <a name="parseexpressionresponse-resource-type"></a><span data-ttu-id="f5f93-103">tipo de recurso parseExpressionResponse</span><span class="sxs-lookup"><span data-stu-id="f5f93-103">parseExpressionResponse resource type</span></span>

> <span data-ttu-id="f5f93-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f5f93-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f5f93-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f5f93-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f5f93-106">Representa la respuesta de la [synchronizationSchema: parseExpression](../api/synchronization_synchronizationschema_parseexpression.md) acción.</span><span class="sxs-lookup"><span data-stu-id="f5f93-106">Represents the response from the [synchronizationSchema: parseExpression](../api/synchronization_synchronizationschema_parseexpression.md) action.</span></span>

## <a name="properties"></a><span data-ttu-id="f5f93-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5f93-107">Properties</span></span>
| <span data-ttu-id="f5f93-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f5f93-108">Property</span></span>     | <span data-ttu-id="f5f93-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5f93-109">Type</span></span>   |<span data-ttu-id="f5f93-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5f93-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f5f93-111">error</span><span class="sxs-lookup"><span data-stu-id="f5f93-111">error</span></span>|<span data-ttu-id="f5f93-112">OData.Error</span><span class="sxs-lookup"><span data-stu-id="f5f93-112">odata.error</span></span>|<span data-ttu-id="f5f93-113">Detalles del error, si como resultado de la evaluación de expresiones en un error.</span><span class="sxs-lookup"><span data-stu-id="f5f93-113">Error details, if expression evaluation resulted in an error.</span></span>|
|<span data-ttu-id="f5f93-114">evaluationResult</span><span class="sxs-lookup"><span data-stu-id="f5f93-114">evaluationResult</span></span>|<span data-ttu-id="f5f93-115">Colección String</span><span class="sxs-lookup"><span data-stu-id="f5f93-115">String collection</span></span>|<span data-ttu-id="f5f93-116">Una colección de valores generados por la evaluación de la expresión.</span><span class="sxs-lookup"><span data-stu-id="f5f93-116">A collection of values produced by the evaluation of the expression.</span></span>|
|<span data-ttu-id="f5f93-117">evaluationSucceeded</span><span class="sxs-lookup"><span data-stu-id="f5f93-117">evaluationSucceeded</span></span>|<span data-ttu-id="f5f93-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="f5f93-118">Boolean</span></span>|<span data-ttu-id="f5f93-119">`true`Si la evaluación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f5f93-119">`true` if the evaluation was successful.</span></span>|
|<span data-ttu-id="f5f93-120">parsedExpression</span><span class="sxs-lookup"><span data-stu-id="f5f93-120">parsedExpression</span></span>|[<span data-ttu-id="f5f93-121">attributeMappingSource</span><span class="sxs-lookup"><span data-stu-id="f5f93-121">attributeMappingSource</span></span>](synchronization-attributemappingsource.md)|<span data-ttu-id="f5f93-122">Un objeto [attributeMappingSource](synchronization-attributemappingsource.md) que representa la expresión analizada.</span><span class="sxs-lookup"><span data-stu-id="f5f93-122">An [attributeMappingSource](synchronization-attributemappingsource.md) object representing the parsed expression.</span></span>|
|<span data-ttu-id="f5f93-123">parsingSucceeded</span><span class="sxs-lookup"><span data-stu-id="f5f93-123">parsingSucceeded</span></span>|<span data-ttu-id="f5f93-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="f5f93-124">Boolean</span></span>|<span data-ttu-id="f5f93-125">`true`Si la expresión se ha analizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f5f93-125">`true` if the expression was parsed successfully.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f5f93-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f5f93-126">JSON representation</span></span>

<span data-ttu-id="f5f93-127">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f5f93-127">The following is a JSON representation of the resource.</span></span>

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