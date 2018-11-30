---
title: tipo de recurso attributeMappingFunctionSchema
description: Describe una función que se puede usar en una asignación de atributos para transformar los valores durante la sincronización.
ms.openlocfilehash: 9760669bb29700bfa79c1cd375857b4fd673879b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087044"
---
# <a name="attributemappingfunctionschema-resource-type"></a><span data-ttu-id="2f2e8-103">tipo de recurso attributeMappingFunctionSchema</span><span class="sxs-lookup"><span data-stu-id="2f2e8-103">attributeMappingFunctionSchema resource type</span></span>

> <span data-ttu-id="2f2e8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2f2e8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2f2e8-106">Describe una función que se puede usar en una [asignación de atributos](synchronization-attributemapping.md) para transformar los valores durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-106">Describes a function that can be used in an [attribute mapping](synchronization-attributemapping.md) to transform values during synchronization.</span></span>

## <a name="methods"></a><span data-ttu-id="2f2e8-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="2f2e8-107">Methods</span></span>

| <span data-ttu-id="2f2e8-108">Método</span><span class="sxs-lookup"><span data-stu-id="2f2e8-108">Method</span></span>           | <span data-ttu-id="2f2e8-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f2e8-109">Return Type</span></span>    |<span data-ttu-id="2f2e8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f2e8-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="2f2e8-111">List</span><span class="sxs-lookup"><span data-stu-id="2f2e8-111">List</span></span>](../api/synchronization-synchronizationschema-functions.md) | <span data-ttu-id="2f2e8-112">colección de [attributeMappingFunctionSchema](../resources/synchronization-attributemappingfunctionschema.md)</span><span class="sxs-lookup"><span data-stu-id="2f2e8-112">[attributeMappingFunctionSchema](../resources/synchronization-attributemappingfunctionschema.md) collection</span></span>|<span data-ttu-id="2f2e8-113">Funciones de la asignación de atributo de la lista compatible.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-113">List supported attribute mapping functions.</span></span>|

## <a name="properties"></a><span data-ttu-id="2f2e8-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2f2e8-114">Properties</span></span>

| <span data-ttu-id="2f2e8-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2f2e8-115">Property</span></span>                   | <span data-ttu-id="2f2e8-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f2e8-116">Type</span></span>                      | <span data-ttu-id="2f2e8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f2e8-117">Description</span></span>    |
|:---------------------------|:-------------------------|:---------------|
|<span data-ttu-id="2f2e8-118">name</span><span class="sxs-lookup"><span data-stu-id="2f2e8-118">name</span></span>                        |<span data-ttu-id="2f2e8-119">String</span><span class="sxs-lookup"><span data-stu-id="2f2e8-119">String</span></span>                    |<span data-ttu-id="2f2e8-120">Nombre del operador.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-120">Operator name.</span></span> |
|<span data-ttu-id="2f2e8-121">parameters</span><span class="sxs-lookup"><span data-stu-id="2f2e8-121">parameters</span></span>                  |<span data-ttu-id="2f2e8-122">colección de [attributeMappingParameterSchema](../resources/synchronization-attributemappingparameterschema.md)</span><span class="sxs-lookup"><span data-stu-id="2f2e8-122">[attributeMappingParameterSchema](../resources/synchronization-attributemappingparameterschema.md) collection</span></span>  |<span data-ttu-id="2f2e8-123">Colección de parámetros de la función.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-123">Collection of function parameters.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2f2e8-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2f2e8-124">JSON representation</span></span>

<span data-ttu-id="2f2e8-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="2f2e8-125">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMappingFunctionSchema"
}-->

```json
{
  "name": "String (identifier)",
  "parameters": [{"@odata.type": "microsoft.graph.attributeMappingParameterSchema"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attributeMappingFunctionSchema resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->