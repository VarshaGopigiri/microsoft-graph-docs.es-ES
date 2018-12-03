---
title: tipo de recurso attributeMappingParameterSchema
description: Describe un solo parámetro empleado en una attributeMappingFunctionSchema.
ms.openlocfilehash: 164387a345f245f390d24b89a349e02ee2242041
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089840"
---
# <a name="attributemappingparameterschema-resource-type"></a><span data-ttu-id="0ec9f-103">tipo de recurso attributeMappingParameterSchema</span><span class="sxs-lookup"><span data-stu-id="0ec9f-103">attributeMappingParameterSchema resource type</span></span>

> <span data-ttu-id="0ec9f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0ec9f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0ec9f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0ec9f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0ec9f-106">Describe un solo parámetro empleado en una [attributeMappingFunctionSchema](../resources/synchronization-attributemappingfunctionschema.md).</span><span class="sxs-lookup"><span data-stu-id="0ec9f-106">Describes a single parameter used in an [attributeMappingFunctionSchema](../resources/synchronization-attributemappingfunctionschema.md).</span></span>

## <a name="properties"></a><span data-ttu-id="0ec9f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0ec9f-107">Properties</span></span>

| <span data-ttu-id="0ec9f-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0ec9f-108">Property</span></span>                   | <span data-ttu-id="0ec9f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ec9f-109">Type</span></span>                      | <span data-ttu-id="0ec9f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ec9f-110">Description</span></span>    |
|:---------------------------|:-------------------------|:---------------|
|<span data-ttu-id="0ec9f-111">allowMultipleOccurrences</span><span class="sxs-lookup"><span data-stu-id="0ec9f-111">allowMultipleOccurrences</span></span>    |<span data-ttu-id="0ec9f-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="0ec9f-112">Boolean</span></span>                   |<span data-ttu-id="0ec9f-113">El parámetro determinado se puede proporcionar varias veces (por ejemplo, cadenas de varias entradas en el `Concatenate(string,string,...)` (función)).</span><span class="sxs-lookup"><span data-stu-id="0ec9f-113">The given parameter can be provided multiple times (for example, multiple input strings in the `Concatenate(string,string,...)` function).</span></span> |
|<span data-ttu-id="0ec9f-114">name</span><span class="sxs-lookup"><span data-stu-id="0ec9f-114">name</span></span>                        |<span data-ttu-id="0ec9f-115">String</span><span class="sxs-lookup"><span data-stu-id="0ec9f-115">String</span></span>                    |<span data-ttu-id="0ec9f-116">Nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="0ec9f-116">Parameter name.</span></span> |
|<span data-ttu-id="0ec9f-117">necesario</span><span class="sxs-lookup"><span data-stu-id="0ec9f-117">required</span></span>                    |<span data-ttu-id="0ec9f-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="0ec9f-118">Boolean</span></span>                   |<span data-ttu-id="0ec9f-119">`true`Si el parámetro es necesario; en caso contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="0ec9f-119">`true` if the parameter is required; otherwise `false`.</span></span> |
|<span data-ttu-id="0ec9f-120">type</span><span class="sxs-lookup"><span data-stu-id="0ec9f-120">type</span></span>                        |<span data-ttu-id="0ec9f-121">String</span><span class="sxs-lookup"><span data-stu-id="0ec9f-121">String</span></span>                    |<span data-ttu-id="0ec9f-122">Valores posibles: `Boolean`, `Binary`, `Reference`, `Integer`, `String`.</span><span class="sxs-lookup"><span data-stu-id="0ec9f-122">Possible values are: `Boolean`, `Binary`, `Reference`, `Integer`, `String`.</span></span> <span data-ttu-id="0ec9f-123">El valor predeterminado es `String`.</span><span class="sxs-lookup"><span data-stu-id="0ec9f-123">Default is `String`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="0ec9f-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0ec9f-124">JSON representation</span></span>

<span data-ttu-id="0ec9f-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0ec9f-125">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMappingParameterSchema"
}-->

```json
{
  "allowMultipleOccurrences": "Boolean",
  "name": "String",
  "required": "Boolean",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attributeMappingParameterSchema resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->