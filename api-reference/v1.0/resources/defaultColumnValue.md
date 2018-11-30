---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: DefaultColumnValue
ms.openlocfilehash: f6f4218c4e33937fa510461bc9de4689aefea71f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032370"
---
# <a name="defaultcolumnvalue-resource-type"></a><span data-ttu-id="6468c-102">Tipo de recurso DefaultColumnValue</span><span class="sxs-lookup"><span data-stu-id="6468c-102">DefaultColumnValue resource type</span></span>

<span data-ttu-id="6468c-103">El recurso **defaultColumnValue** en un recurso [columnDefinition](columndefinition.md) especifica el valor predeterminado de esta columna.</span><span class="sxs-lookup"><span data-stu-id="6468c-103">The **defaultColumnValue** on a [columnDefinition](columndefinition.md) resource specifies the default value for this column.</span></span>
<span data-ttu-id="6468c-104">El valor predeterminado puede especificarse directamente o como una fórmula.</span><span class="sxs-lookup"><span data-stu-id="6468c-104">The default value can either be specified directly or as a formula.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6468c-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6468c-105">JSON representation</span></span>

<span data-ttu-id="6468c-106">A continuación se incluye una representación JSON del recurso **defaultColumnValue**.</span><span class="sxs-lookup"><span data-stu-id="6468c-106">Here is a JSON representation of a **defaultColumnValue** resource.</span></span>
<!-- { "blockType": "resource", "@type": "microsoft.graph.defaultColumnValue" } -->

```json
{
  "formula": "=[Column1]+[Column2]+[Column3]",
  "value": "defaultValueString"
}
```

## <a name="properties"></a><span data-ttu-id="6468c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6468c-107">Properties</span></span>

| <span data-ttu-id="6468c-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="6468c-108">Property name</span></span> | <span data-ttu-id="6468c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6468c-109">Type</span></span>   | <span data-ttu-id="6468c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6468c-110">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="6468c-111">**formula**</span><span class="sxs-lookup"><span data-stu-id="6468c-111">**formula**</span></span>   | <span data-ttu-id="6468c-112">string</span><span class="sxs-lookup"><span data-stu-id="6468c-112">string</span></span> | <span data-ttu-id="6468c-113">La fórmula usada para calcular el valor predeterminado de esta columna.</span><span class="sxs-lookup"><span data-stu-id="6468c-113">The formula used to compute the default value for this column.</span></span>
| <span data-ttu-id="6468c-114">**value**</span><span class="sxs-lookup"><span data-stu-id="6468c-114">**value**</span></span>     | <span data-ttu-id="6468c-115">string</span><span class="sxs-lookup"><span data-stu-id="6468c-115">string</span></span> | <span data-ttu-id="6468c-116">El valor directo que se usará como el valor predeterminado de esta columna.</span><span class="sxs-lookup"><span data-stu-id="6468c-116">The direct value to use as the default value for this column.</span></span>

<span data-ttu-id="6468c-117">Solo se puede especificar **formula** o **value** de cada vez.</span><span class="sxs-lookup"><span data-stu-id="6468c-117">Only one of **formula** or **value** may be specified at a time.</span></span>

<span data-ttu-id="6468c-118">Las fórmulas de SharePoint usan una sintaxis similar a las fórmulas de Excel.</span><span class="sxs-lookup"><span data-stu-id="6468c-118">SharePoint formulas use a syntax similar to Excel formulas.</span></span>
<span data-ttu-id="6468c-119">Vea [Ejemplos de fórmulas comunes en listas de SharePoint][SPFormulas] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6468c-119">See [Examples of common formulas in SharePoint Lists][SPFormulas] for more information.</span></span>

[SPFormulas]: https://support.office.com/en-us/article/Examples-of-common-formulas-in-SharePoint-Lists-d81f5f21-2b4e-45ce-b170-bf7ebf6988b3


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/DefaultColumnValue"
} -->
