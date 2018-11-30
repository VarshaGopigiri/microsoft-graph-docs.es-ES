---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: DefaultColumnValue
ms.openlocfilehash: 3a486b6cc90dffb75343390102ecb3b17576e6fb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087461"
---
# <a name="defaultcolumnvalue-resource-type"></a><span data-ttu-id="15d7f-102">Tipo de recurso DefaultColumnValue</span><span class="sxs-lookup"><span data-stu-id="15d7f-102">DefaultColumnValue resource type</span></span>

> <span data-ttu-id="15d7f-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="15d7f-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="15d7f-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="15d7f-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="15d7f-105">El recurso **defaultColumnValue** en un recurso [columnDefinition](columndefinition.md) especifica el valor predeterminado de esta columna.</span><span class="sxs-lookup"><span data-stu-id="15d7f-105">The **defaultColumnValue** on a [columnDefinition](columndefinition.md) resource specifies the default value for this column.</span></span>
<span data-ttu-id="15d7f-106">El valor predeterminado puede especificarse directamente o como una fórmula.</span><span class="sxs-lookup"><span data-stu-id="15d7f-106">The default value can either be specified directly or as a formula.</span></span>

## <a name="json-representation"></a><span data-ttu-id="15d7f-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="15d7f-107">JSON representation</span></span>

<span data-ttu-id="15d7f-108">A continuación se incluye una representación JSON del recurso **defaultColumnValue**.</span><span class="sxs-lookup"><span data-stu-id="15d7f-108">Here is a JSON representation of a **defaultColumnValue** resource.</span></span>
<!-- { "blockType": "resource", "@type": "microsoft.graph.defaultColumnValue" } -->

```json
{
  "formula": "=[Column1]+[Column2]+[Column3]",
  "value": "defaultValueString"
}
```

## <a name="properties"></a><span data-ttu-id="15d7f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15d7f-109">Properties</span></span>

| <span data-ttu-id="15d7f-110">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="15d7f-110">Property name</span></span> | <span data-ttu-id="15d7f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="15d7f-111">Type</span></span>   | <span data-ttu-id="15d7f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="15d7f-112">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="15d7f-113">**formula**</span><span class="sxs-lookup"><span data-stu-id="15d7f-113">**formula**</span></span>   | <span data-ttu-id="15d7f-114">string</span><span class="sxs-lookup"><span data-stu-id="15d7f-114">string</span></span> | <span data-ttu-id="15d7f-115">La fórmula usada para calcular el valor predeterminado de esta columna.</span><span class="sxs-lookup"><span data-stu-id="15d7f-115">The formula used to compute the default value for this column.</span></span>
| <span data-ttu-id="15d7f-116">**value**</span><span class="sxs-lookup"><span data-stu-id="15d7f-116">**value**</span></span>     | <span data-ttu-id="15d7f-117">string</span><span class="sxs-lookup"><span data-stu-id="15d7f-117">string</span></span> | <span data-ttu-id="15d7f-118">El valor directo que se usará como el valor predeterminado de esta columna.</span><span class="sxs-lookup"><span data-stu-id="15d7f-118">The direct value to use as the default value for this column.</span></span>

<span data-ttu-id="15d7f-119">Solo se puede especificar **formula** o **value** de cada vez.</span><span class="sxs-lookup"><span data-stu-id="15d7f-119">Only one of **formula** or **value** may be specified at a time.</span></span>

<span data-ttu-id="15d7f-120">Las fórmulas de SharePoint usan una sintaxis similar a las fórmulas de Excel.</span><span class="sxs-lookup"><span data-stu-id="15d7f-120">SharePoint formulas use a syntax similar to Excel formulas.</span></span>
<span data-ttu-id="15d7f-121">Vea [Ejemplos de fórmulas comunes en listas de SharePoint][SPFormulas] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="15d7f-121">See [Examples of common formulas in SharePoint Lists][SPFormulas] for more information.</span></span>

[SPFormulas]: https://support.office.com/en-us/article/Examples-of-common-formulas-in-SharePoint-Lists-d81f5f21-2b4e-45ce-b170-bf7ebf6988b3


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/DefaultColumnValue"
} -->
