---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: DefaultColumnValue
localization_priority: Normal
ms.openlocfilehash: 6ceca45d09654771f161db63707682a4558b0d29
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815550"
---
# <a name="defaultcolumnvalue-resource-type"></a><span data-ttu-id="afc0a-102">Tipo de recurso DefaultColumnValue</span><span class="sxs-lookup"><span data-stu-id="afc0a-102">DefaultColumnValue resource type</span></span>

> <span data-ttu-id="afc0a-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="afc0a-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="afc0a-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="afc0a-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="afc0a-105">El recurso **defaultColumnValue** en un recurso [columnDefinition](columndefinition.md) especifica el valor predeterminado de esta columna.</span><span class="sxs-lookup"><span data-stu-id="afc0a-105">The **defaultColumnValue** on a [columnDefinition](columndefinition.md) resource specifies the default value for this column.</span></span>
<span data-ttu-id="afc0a-106">El valor predeterminado puede especificarse directamente o como una fórmula.</span><span class="sxs-lookup"><span data-stu-id="afc0a-106">The default value can either be specified directly or as a formula.</span></span>

## <a name="json-representation"></a><span data-ttu-id="afc0a-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="afc0a-107">JSON representation</span></span>

<span data-ttu-id="afc0a-108">A continuación se incluye una representación JSON del recurso **defaultColumnValue**.</span><span class="sxs-lookup"><span data-stu-id="afc0a-108">Here is a JSON representation of a **defaultColumnValue** resource.</span></span>
<!-- { "blockType": "resource", "@type": "microsoft.graph.defaultColumnValue" } -->

```json
{
  "formula": "=[Column1]+[Column2]+[Column3]",
  "value": "defaultValueString"
}
```

## <a name="properties"></a><span data-ttu-id="afc0a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="afc0a-109">Properties</span></span>

| <span data-ttu-id="afc0a-110">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="afc0a-110">Property name</span></span> | <span data-ttu-id="afc0a-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="afc0a-111">Type</span></span>   | <span data-ttu-id="afc0a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="afc0a-112">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="afc0a-113">**formula**</span><span class="sxs-lookup"><span data-stu-id="afc0a-113">**formula**</span></span>   | <span data-ttu-id="afc0a-114">string</span><span class="sxs-lookup"><span data-stu-id="afc0a-114">string</span></span> | <span data-ttu-id="afc0a-115">La fórmula usada para calcular el valor predeterminado de esta columna.</span><span class="sxs-lookup"><span data-stu-id="afc0a-115">The formula used to compute the default value for this column.</span></span>
| <span data-ttu-id="afc0a-116">**value**</span><span class="sxs-lookup"><span data-stu-id="afc0a-116">**value**</span></span>     | <span data-ttu-id="afc0a-117">string</span><span class="sxs-lookup"><span data-stu-id="afc0a-117">string</span></span> | <span data-ttu-id="afc0a-118">El valor directo que se usará como el valor predeterminado de esta columna.</span><span class="sxs-lookup"><span data-stu-id="afc0a-118">The direct value to use as the default value for this column.</span></span>

<span data-ttu-id="afc0a-119">Solo se puede especificar **formula** o **value** de cada vez.</span><span class="sxs-lookup"><span data-stu-id="afc0a-119">Only one of **formula** or **value** may be specified at a time.</span></span>

<span data-ttu-id="afc0a-120">Las fórmulas de SharePoint usan una sintaxis similar a las fórmulas de Excel.</span><span class="sxs-lookup"><span data-stu-id="afc0a-120">SharePoint formulas use a syntax similar to Excel formulas.</span></span>
<span data-ttu-id="afc0a-121">Vea [Ejemplos de fórmulas comunes en listas de SharePoint][SPFormulas] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="afc0a-121">See [Examples of common formulas in SharePoint Lists][SPFormulas] for more information.</span></span>

[SPFormulas]: https://support.office.com/en-us/article/Examples-of-common-formulas-in-SharePoint-Lists-d81f5f21-2b4e-45ce-b170-bf7ebf6988b3


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/DefaultColumnValue"
} -->
