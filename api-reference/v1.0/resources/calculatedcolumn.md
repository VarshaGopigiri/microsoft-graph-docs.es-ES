---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: CalculatedColumn
ms.openlocfilehash: 7e26b3683c2c84d1c413f3214da39e0a3d016f40
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23267846"
---
# <a name="calculatedcolumn-resource-type"></a><span data-ttu-id="8650b-102">Tipo de recurso CalculatedColumn</span><span class="sxs-lookup"><span data-stu-id="8650b-102">CalculatedColumn resource type</span></span>

<span data-ttu-id="8650b-103">El recurso **calculatedColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los datos de la columna se calculan en función de otras columnas en el sitio.</span><span class="sxs-lookup"><span data-stu-id="8650b-103">The **calculatedColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's data is calculated based on other columns in the site.</span></span>

## <a name="json-representation"></a><span data-ttu-id="8650b-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8650b-104">JSON representation</span></span>

<span data-ttu-id="8650b-105">A continuación se incluye una representación JSON de un recurso **calculatedColumn**.</span><span class="sxs-lookup"><span data-stu-id="8650b-105">Here is a JSON representation of a **calculatedColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.calculatedColumn" } -->

```json
{
  "format": "dateOnly | dateTime",
  "formula": "=[Column1]+[Column2]+[Column3]",
  "outputType": "boolean | currency | dateTime | number | text",
}
```

## <a name="properties"></a><span data-ttu-id="8650b-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8650b-106">Properties</span></span>

| <span data-ttu-id="8650b-107">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="8650b-107">Property name</span></span>  | <span data-ttu-id="8650b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8650b-108">Type</span></span>    | <span data-ttu-id="8650b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8650b-109">Description</span></span>
|:---------------|:--------|:--------------------------------------------------
| <span data-ttu-id="8650b-110">**format**</span><span class="sxs-lookup"><span data-stu-id="8650b-110">**format**</span></span>     | <span data-ttu-id="8650b-111">string</span><span class="sxs-lookup"><span data-stu-id="8650b-111">string</span></span>  | <span data-ttu-id="8650b-112">Para tipos de salida `dateTime`, el formato del valor.</span><span class="sxs-lookup"><span data-stu-id="8650b-112">For `dateTime` output types, the format of the value.</span></span> <span data-ttu-id="8650b-113">Debe ser `dateOnly` o `dateTime`.</span><span class="sxs-lookup"><span data-stu-id="8650b-113">Must be one of `dateOnly` or `dateTime`.</span></span>
| <span data-ttu-id="8650b-114">**formula**</span><span class="sxs-lookup"><span data-stu-id="8650b-114">**formula**</span></span>    | <span data-ttu-id="8650b-115">string</span><span class="sxs-lookup"><span data-stu-id="8650b-115">string</span></span>  | <span data-ttu-id="8650b-116">La fórmula usada para calcular el valor de esta columna.</span><span class="sxs-lookup"><span data-stu-id="8650b-116">The formula used to compute the value for this column.</span></span>
| <span data-ttu-id="8650b-117">**outputType**</span><span class="sxs-lookup"><span data-stu-id="8650b-117">**outputType**</span></span> | <span data-ttu-id="8650b-118">string</span><span class="sxs-lookup"><span data-stu-id="8650b-118">string</span></span>  | <span data-ttu-id="8650b-119">El tipo de salida usado para dar formato a los valores de esta columna.</span><span class="sxs-lookup"><span data-stu-id="8650b-119">The output type used to format values in this column.</span></span> <span data-ttu-id="8650b-120">Debe ser `boolean`, `currency`, `dateTime`, `number` o `text`.</span><span class="sxs-lookup"><span data-stu-id="8650b-120">Must be one of `boolean`, `currency`, `dateTime`, `number`, or `text`.</span></span>

<span data-ttu-id="8650b-121">Las fórmulas de SharePoint usan una sintaxis similar a las fórmulas de Excel.</span><span class="sxs-lookup"><span data-stu-id="8650b-121">SharePoint formulas use a syntax similar to Excel formulas.</span></span>
<span data-ttu-id="8650b-122">Vea [Ejemplos de fórmulas comunes en listas de SharePoint][SPFormulas] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8650b-122">See [Examples of common formulas in SharePoint Lists][SPFormulas] for more information.</span></span>

[SPFormulas]: https://support.office.com/en-us/article/Examples-of-common-formulas-in-SharePoint-Lists-d81f5f21-2b4e-45ce-b170-bf7ebf6988b3

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/calculatedcolumn.md:
      Found potential enums in resource example that weren't defined in a table:(dateOnly,dateTime) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/calculatedcolumn.md:
      Found potential enums in resource example that weren't defined in a table:(boolean,currency,dateTime,number,text) are in resource, but () are in table"
  ],
  "tocPath": "Resources/CalculatedColumn"
} -->
