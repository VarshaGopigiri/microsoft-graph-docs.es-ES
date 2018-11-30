---
title: Tipo de recurso FilterDatetime
description: Representa cómo se filtra una fecha cuando se filtran valores.
ms.openlocfilehash: 8156b9f5779dd8d70ff3a839d8a6ef4f5753bacd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028737"
---
# <a name="filterdatetime-resource-type"></a><span data-ttu-id="089f5-103">Tipo de recurso FilterDatetime</span><span class="sxs-lookup"><span data-stu-id="089f5-103">FilterDatetime resource type</span></span>

<span data-ttu-id="089f5-104">Representa cómo se filtra una fecha cuando se filtran valores.</span><span class="sxs-lookup"><span data-stu-id="089f5-104">Represents how to filter a date when filtering on values.</span></span>

## <a name="properties"></a><span data-ttu-id="089f5-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="089f5-105">Properties</span></span>
| <span data-ttu-id="089f5-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="089f5-106">Property</span></span>     | <span data-ttu-id="089f5-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="089f5-107">Type</span></span>   |<span data-ttu-id="089f5-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="089f5-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="089f5-109">fecha</span><span class="sxs-lookup"><span data-stu-id="089f5-109">date</span></span>|<span data-ttu-id="089f5-110">string</span><span class="sxs-lookup"><span data-stu-id="089f5-110">string</span></span>|<span data-ttu-id="089f5-111">La fecha en formato ISO8601 usada para filtrar los datos.</span><span class="sxs-lookup"><span data-stu-id="089f5-111">The date in ISO8601 format used to filter data.</span></span>|
|<span data-ttu-id="089f5-112">specificity</span><span class="sxs-lookup"><span data-stu-id="089f5-112">specificity</span></span>|<span data-ttu-id="089f5-113">string</span><span class="sxs-lookup"><span data-stu-id="089f5-113">string</span></span>|<span data-ttu-id="089f5-114">¿Cómo específica la fecha debe usarse para mantener los datos.</span><span class="sxs-lookup"><span data-stu-id="089f5-114">How specific the date should be used to keep data.</span></span> <span data-ttu-id="089f5-115">Por ejemplo, si la fecha es 2005-04-02 y el specifity se establece en "mes", la operación de filtrado mantener todas las filas con una fecha en el mes de abril de 2009.</span><span class="sxs-lookup"><span data-stu-id="089f5-115">For example, if the date is 2005-04-02 and the specifity is set to "month", the filter operation will keep all rows with a date in the month of april 2009.</span></span> <span data-ttu-id="089f5-116">Los valores posibles son: `Year`, `Monday`, `Day`, `Hour`, `Minute`, `Second`.</span><span class="sxs-lookup"><span data-stu-id="089f5-116">The possible values are: `Year`, `Monday`, `Day`, `Hour`, `Minute`, `Second`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="089f5-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="089f5-117">Relationships</span></span>
<span data-ttu-id="089f5-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="089f5-118">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="089f5-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="089f5-119">JSON representation</span></span>

<span data-ttu-id="089f5-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="089f5-120">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookFilterDateTime"
}-->

```json
{
  "date": "string",
  "specificity": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "FilterDatetime resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->