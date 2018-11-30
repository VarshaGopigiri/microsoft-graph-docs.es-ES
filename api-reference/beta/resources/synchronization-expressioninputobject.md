---
title: tipo de recurso expressionInputObject
description: 'Representa un objeto que se utilizará como datos de comprobación de la entrada cuando la [synchronizationSchema: parseExpression](../api/synchronization_synchronizationschema_parseexpression.md) acción realiza una evaluación de la expresión.'
ms.openlocfilehash: 06b7344f7e6418db0557f2b12dfa7e964b9d5ab7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090000"
---
# <a name="expressioninputobject-resource-type"></a><span data-ttu-id="e5e87-103">tipo de recurso expressionInputObject</span><span class="sxs-lookup"><span data-stu-id="e5e87-103">expressionInputObject resource type</span></span>

> <span data-ttu-id="e5e87-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e5e87-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e5e87-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e5e87-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e5e87-106">Representa un objeto que se utilizará como datos de comprobación de la entrada cuando la [synchronizationSchema: parseExpression](../api/synchronization_synchronizationschema_parseexpression.md) acción realiza una evaluación de la expresión.</span><span class="sxs-lookup"><span data-stu-id="e5e87-106">Represents an object to be used as input test data when the [synchronizationSchema: parseExpression](../api/synchronization_synchronizationschema_parseexpression.md) action performs an expression evaluation.</span></span>

## <a name="properties"></a><span data-ttu-id="e5e87-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e5e87-107">Properties</span></span>
| <span data-ttu-id="e5e87-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e5e87-108">Property</span></span>     | <span data-ttu-id="e5e87-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5e87-109">Type</span></span>   |<span data-ttu-id="e5e87-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5e87-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e5e87-111">definición</span><span class="sxs-lookup"><span data-stu-id="e5e87-111">definition</span></span>|[<span data-ttu-id="e5e87-112">objectDefinition</span><span class="sxs-lookup"><span data-stu-id="e5e87-112">objectDefinition</span></span>](synchronization-objectdefinition.md)|<span data-ttu-id="e5e87-113">Definición del objeto de prueba.</span><span class="sxs-lookup"><span data-stu-id="e5e87-113">Definition of the test object.</span></span>|
|<span data-ttu-id="e5e87-114">propiedades</span><span class="sxs-lookup"><span data-stu-id="e5e87-114">properties</span></span>|<span data-ttu-id="e5e87-115">colección de [stringKeyObjectValuePair](synchronization-stringkeyobjectvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="e5e87-115">[stringKeyObjectValuePair](synchronization-stringkeyobjectvaluepair.md) collection</span></span>|<span data-ttu-id="e5e87-116">Valores de propiedad del objeto de prueba.</span><span class="sxs-lookup"><span data-stu-id="e5e87-116">Property values of the test object.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e5e87-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e5e87-117">JSON representation</span></span>

<span data-ttu-id="e5e87-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e5e87-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.expressionInputObject"
}-->

```json
{
  "definition": {"@odata.type": "microsoft.graph.objectDefinition"},
  "properties": [{"@odata.type": "microsoft.graph.stringKeyObjectValuePair"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "expressionInputObject resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->