---
title: Tipo de recurso FilterDatetime
description: Representa cómo se filtra una fecha cuando se filtran valores.
ms.openlocfilehash: d3cb0df48a1116a64a72413aa64cabdec46da6d9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087337"
---
# <a name="filterdatetime-resource-type"></a><span data-ttu-id="1127a-103">Tipo de recurso FilterDatetime</span><span class="sxs-lookup"><span data-stu-id="1127a-103">FilterDatetime resource type</span></span>

> <span data-ttu-id="1127a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1127a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1127a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1127a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1127a-106">Representa cómo se filtra una fecha cuando se filtran valores.</span><span class="sxs-lookup"><span data-stu-id="1127a-106">Represents how to filter a date when filtering on values.</span></span>

## <a name="properties"></a><span data-ttu-id="1127a-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1127a-107">Properties</span></span>
| <span data-ttu-id="1127a-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1127a-108">Property</span></span>     | <span data-ttu-id="1127a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="1127a-109">Type</span></span>   |<span data-ttu-id="1127a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1127a-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1127a-111">fecha</span><span class="sxs-lookup"><span data-stu-id="1127a-111">date</span></span>|<span data-ttu-id="1127a-112">string</span><span class="sxs-lookup"><span data-stu-id="1127a-112">string</span></span>|<span data-ttu-id="1127a-113">La fecha en formato ISO8601 usada para filtrar los datos.</span><span class="sxs-lookup"><span data-stu-id="1127a-113">The date in ISO8601 format used to filter data.</span></span>|
|<span data-ttu-id="1127a-114">specificity</span><span class="sxs-lookup"><span data-stu-id="1127a-114">specificity</span></span>|<span data-ttu-id="1127a-115">string</span><span class="sxs-lookup"><span data-stu-id="1127a-115">string</span></span>|<span data-ttu-id="1127a-p102">El grado de especificidad de la fecha que se usará para mantener datos. Por ejemplo, si la fecha es 02-04-2005 y la especificidad se establece en "mes", la operación de filtrado conservará todas las filas con fecha de abril de 2009. Valores posibles: `Year`, `Monday`, `Day`, `Hour`, `Minute`, `Second`.</span><span class="sxs-lookup"><span data-stu-id="1127a-p102">How specific the date should be used to keep data. For example, if the date is 2005-04-02 and the specifity is set to "month", the filter operation will keep all rows with a date in the month of april 2009. Possible values are: `Year`, `Monday`, `Day`, `Hour`, `Minute`, `Second`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="1127a-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1127a-119">Relationships</span></span>
<span data-ttu-id="1127a-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1127a-120">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="1127a-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1127a-121">JSON representation</span></span>

<span data-ttu-id="1127a-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1127a-122">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.filterDateTime"
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