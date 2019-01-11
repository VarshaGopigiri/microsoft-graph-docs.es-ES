---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: CalculatedColumn
localization_priority: Normal
ms.openlocfilehash: 5433b5b5a76d313f8f34e460400906479e6d3d7c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876058"
---
# <a name="calculatedcolumn-resource-type"></a><span data-ttu-id="d17eb-102">Tipo de recurso CalculatedColumn</span><span class="sxs-lookup"><span data-stu-id="d17eb-102">CalculatedColumn resource type</span></span>

> <span data-ttu-id="d17eb-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d17eb-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d17eb-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d17eb-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d17eb-105">El recurso **calculatedColumn** en un recurso [columnDefinition](columndefinition.md) indica que los datos de la columna se calculan en función de otras columnas en el sitio.</span><span class="sxs-lookup"><span data-stu-id="d17eb-105">The **calculatedColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's data is calculated based on other columns in the site.</span></span>

## <a name="json-representation"></a><span data-ttu-id="d17eb-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d17eb-106">JSON representation</span></span>

<span data-ttu-id="d17eb-107">A continuación se incluye una representación JSON de un recurso **calculatedColumn**.</span><span class="sxs-lookup"><span data-stu-id="d17eb-107">Here is a JSON representation of a **calculatedColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.calculatedColumn" } -->

```json
{
  "format": "dateOnly | dateTime",
  "formula": "=[Column1]+[Column2]+[Column3]",
  "outputType": "boolean | currency | dateTime | number | text",
}
```

## <a name="properties"></a><span data-ttu-id="d17eb-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d17eb-108">Properties</span></span>

| <span data-ttu-id="d17eb-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="d17eb-109">Property name</span></span>  | <span data-ttu-id="d17eb-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d17eb-110">Type</span></span>    | <span data-ttu-id="d17eb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d17eb-111">Description</span></span>
|:---------------|:--------|:--------------------------------------------------
| <span data-ttu-id="d17eb-112">**format**</span><span class="sxs-lookup"><span data-stu-id="d17eb-112">**format**</span></span>     | <span data-ttu-id="d17eb-113">string</span><span class="sxs-lookup"><span data-stu-id="d17eb-113">string</span></span>  | <span data-ttu-id="d17eb-114">Para tipos de salida `dateTime`, el formato del valor.</span><span class="sxs-lookup"><span data-stu-id="d17eb-114">For `dateTime` output types, the format of the value.</span></span> <span data-ttu-id="d17eb-115">Debe ser `dateOnly` o `dateTime`.</span><span class="sxs-lookup"><span data-stu-id="d17eb-115">Must be one of `dateOnly` or `dateTime`.</span></span>
| <span data-ttu-id="d17eb-116">**formula**</span><span class="sxs-lookup"><span data-stu-id="d17eb-116">**formula**</span></span>    | <span data-ttu-id="d17eb-117">string</span><span class="sxs-lookup"><span data-stu-id="d17eb-117">string</span></span>  | <span data-ttu-id="d17eb-118">La fórmula usada para calcular el valor de esta columna.</span><span class="sxs-lookup"><span data-stu-id="d17eb-118">The formula used to compute the value for this column.</span></span>
| <span data-ttu-id="d17eb-119">**outputType**</span><span class="sxs-lookup"><span data-stu-id="d17eb-119">**outputType**</span></span> | <span data-ttu-id="d17eb-120">string</span><span class="sxs-lookup"><span data-stu-id="d17eb-120">string</span></span>  | <span data-ttu-id="d17eb-121">El tipo de salida usado para dar formato a los valores de esta columna.</span><span class="sxs-lookup"><span data-stu-id="d17eb-121">The output type used to format values in this column.</span></span> <span data-ttu-id="d17eb-122">Debe ser `boolean`, `currency`, `dateTime`, `number` o `text`.</span><span class="sxs-lookup"><span data-stu-id="d17eb-122">Must be one of `boolean`, `currency`, `dateTime`, `number`, or `text`.</span></span>

<span data-ttu-id="d17eb-123">Las fórmulas de SharePoint usan una sintaxis similar a las fórmulas de Excel.</span><span class="sxs-lookup"><span data-stu-id="d17eb-123">SharePoint formulas use a syntax similar to Excel formulas.</span></span>
<span data-ttu-id="d17eb-124">Vea [Ejemplos de fórmulas comunes en listas de SharePoint][SPFormulas] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d17eb-124">See [Examples of common formulas in SharePoint Lists][SPFormulas] for more information.</span></span>

[SPFormulas]: https://support.office.com/en-us/article/Examples-of-common-formulas-in-SharePoint-Lists-d81f5f21-2b4e-45ce-b170-bf7ebf6988b3

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/CalculatedColumn"
} -->
