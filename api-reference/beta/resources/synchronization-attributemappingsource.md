---
title: tipo de recurso attributeMappingSource
description: 'Define cómo debe ser un valor extrajo (o transforma) desde el objeto de origen. Por ejemplo, puede ser un valor simple tomado de un atributo determinado en el objeto de origen, o puede ser una expresión de cadena concatenación/extracción/sustitución en función de varios atributos de origen más compleja. '
ms.openlocfilehash: aeb39c829d7be081fe9ee08aa5845e6ced1194dc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086493"
---
# <a name="attributemappingsource-resource-type"></a><span data-ttu-id="62e65-104">tipo de recurso attributeMappingSource</span><span class="sxs-lookup"><span data-stu-id="62e65-104">attributeMappingSource resource type</span></span>

> <span data-ttu-id="62e65-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="62e65-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="62e65-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="62e65-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="62e65-107">Define cómo debe ser un valor extrajo (o transforma) desde el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="62e65-107">Defines how a value should be extracted (or transformed) from the source object.</span></span> <span data-ttu-id="62e65-108">Por ejemplo, puede ser un valor simple tomado de un atributo determinado en el objeto de origen, o puede ser una expresión de cadena concatenación/extracción/sustitución en función de varios atributos de origen más compleja.</span><span class="sxs-lookup"><span data-stu-id="62e65-108">For example, it can be a simple value taken from a given attribute on the source object, or it can be a more complex expression of string concatenation/extraction/replacement based on several source attributes.</span></span> 

## <a name="properties"></a><span data-ttu-id="62e65-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="62e65-109">Properties</span></span>

| <span data-ttu-id="62e65-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="62e65-110">Property</span></span>              | <span data-ttu-id="62e65-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="62e65-111">Type</span></span>                      | <span data-ttu-id="62e65-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="62e65-112">Description</span></span>               |
|:----------------------|:--------------------------|:--------------------------|
|<span data-ttu-id="62e65-113">expresión</span><span class="sxs-lookup"><span data-stu-id="62e65-113">expression</span></span>             |<span data-ttu-id="62e65-114">String</span><span class="sxs-lookup"><span data-stu-id="62e65-114">String</span></span>                     |<span data-ttu-id="62e65-115">Representación de la expresión equivalente de este objeto **attributeMappingSource** .</span><span class="sxs-lookup"><span data-stu-id="62e65-115">Equivalent expression representation of this **attributeMappingSource** object.</span></span>|
|<span data-ttu-id="62e65-116">name</span><span class="sxs-lookup"><span data-stu-id="62e65-116">name</span></span>                   |<span data-ttu-id="62e65-117">String</span><span class="sxs-lookup"><span data-stu-id="62e65-117">String</span></span>                     |<span data-ttu-id="62e65-118">Parámetro nombre de origen de la asignación.</span><span class="sxs-lookup"><span data-stu-id="62e65-118">Name parameter of the mapping source.</span></span> <span data-ttu-id="62e65-119">Según el valor de la propiedad **type** , esto puede ser el nombre de la función, el nombre del atributo de origen, o un valor constante que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="62e65-119">Depending on the **type** property value, this can be the name of the function, the name of the source attribute, or a constant value to be used.</span></span> |
|<span data-ttu-id="62e65-120">parameters</span><span class="sxs-lookup"><span data-stu-id="62e65-120">parameters</span></span>             |<span data-ttu-id="62e65-121">colección de [stringKeyAttributeMappingSourceValuePair](synchronization-stringkeyattributemappingsourcevaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="62e65-121">[stringKeyAttributeMappingSourceValuePair](synchronization-stringkeyattributemappingsourcevaluepair.md) collection</span></span> | <span data-ttu-id="62e65-122">Si este objeto representa una función, enumera los parámetros de la función.</span><span class="sxs-lookup"><span data-stu-id="62e65-122">If this object represents a function, lists function parameters.</span></span> <span data-ttu-id="62e65-123">Parámetros constan de objetos de **attributeMappingSource** ellos mismos, lo que permite para expresiones complejas.</span><span class="sxs-lookup"><span data-stu-id="62e65-123">Parameters consist of **attributeMappingSource** objects themselves, allowing for complex expressions.</span></span> <span data-ttu-id="62e65-124">Si no es del **tipo** `Function`, esta propiedad será null o vacío matriz.</span><span class="sxs-lookup"><span data-stu-id="62e65-124">If **type** is not `Function`, this property will be null/empty array.</span></span> |
|<span data-ttu-id="62e65-125">type</span><span class="sxs-lookup"><span data-stu-id="62e65-125">type</span></span>                   | <span data-ttu-id="62e65-126">String</span><span class="sxs-lookup"><span data-stu-id="62e65-126">String</span></span>                    |<span data-ttu-id="62e65-127">El tipo de este origen de asignación de atributo.</span><span class="sxs-lookup"><span data-stu-id="62e65-127">The type of this attribute mapping source.</span></span> <span data-ttu-id="62e65-128">Los valores posibles son: `Attribute`, `Constant` y `Function`.</span><span class="sxs-lookup"><span data-stu-id="62e65-128">Possible values are: `Attribute`, `Constant`, `Function`.</span></span> <span data-ttu-id="62e65-129">El valor predeterminado es `Attribute`.</span><span class="sxs-lookup"><span data-stu-id="62e65-129">Default is `Attribute`.</span></span>| 

## <a name="json-representation"></a><span data-ttu-id="62e65-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="62e65-130">JSON representation</span></span>

<span data-ttu-id="62e65-131">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="62e65-131">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMappingSource"
}-->

```json
{
  "expression": "String",
  "name": "String",
  "parameters": [{"@odata.type": "microsoft.graph.stringKeyAttributeMappingSourceValuePair"}],
  "type": "String"
}
```

## <a name="json-examples"></a><span data-ttu-id="62e65-132">Ejemplos JSON</span><span class="sxs-lookup"><span data-stu-id="62e65-132">JSON Examples</span></span>

<span data-ttu-id="62e65-133">Asignación de atributo para el atributo simple</span><span class="sxs-lookup"><span data-stu-id="62e65-133">Simple attribute to attribute mapping</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMappingSource"
}-->

```json
{
    "expression": "[mail]",
    "name": "mail",
    "type": "Attribute"
}
```

<span data-ttu-id="62e65-134">Expresión de extracción de 8 primeros caracteres del atributo de origen</span><span class="sxs-lookup"><span data-stu-id="62e65-134">Expression extracting first 8 characters from the source attribute</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMappingSource"
}-->

```json
 {
    "expression": "Mid([userPrincipalName], 1, 8)",
    "name": "Mid",
    "parameters": [
        {
            "key": "source",
            "value": {
                "expression": "[userPrincipalName]",
                "name": "userPrincipalName",
                "parameters": [],
                "type": "Attribute"
            }
        },
        {
            "key": "start",
            "value": {
                "expression": "\"1\"",
                "name": "1",
                "parameters": [],
                "type": "Constant"
            }
        },
        {
            "key": "length",
            "value": {
                "expression": "\"8\"",
                "name": "8",
                "parameters": [],
                "type": "Constant"
            }
        }
    ],
    "type": "Function"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attributeMappingSource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
