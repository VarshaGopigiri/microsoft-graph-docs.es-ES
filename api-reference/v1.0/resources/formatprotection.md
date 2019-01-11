---
title: Tipo de recurso FormatProtection
description: Representa la protección de formato de un objeto range.
localization_priority: Normal
ms.openlocfilehash: e4c32c8be8f6ef3aeaaf763ee88998bcbe235503
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876779"
---
# <a name="formatprotection-resource-type"></a><span data-ttu-id="e3200-103">Tipo de recurso FormatProtection</span><span class="sxs-lookup"><span data-stu-id="e3200-103">FormatProtection resource type</span></span>

<span data-ttu-id="e3200-104">Representa la protección de formato de un objeto range.</span><span class="sxs-lookup"><span data-stu-id="e3200-104">Represents the format protection of a range object.</span></span>


## <a name="methods"></a><span data-ttu-id="e3200-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="e3200-105">Methods</span></span>

| <span data-ttu-id="e3200-106">Método</span><span class="sxs-lookup"><span data-stu-id="e3200-106">Method</span></span>           | <span data-ttu-id="e3200-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3200-107">Return Type</span></span>    |<span data-ttu-id="e3200-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3200-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e3200-109">Get FormatProtection</span><span class="sxs-lookup"><span data-stu-id="e3200-109">Get FormatProtection</span></span>](../api/formatprotection-get.md) | [<span data-ttu-id="e3200-110">FormatProtection</span><span class="sxs-lookup"><span data-stu-id="e3200-110">FormatProtection</span></span>](formatprotection.md) |<span data-ttu-id="e3200-111">Lee las propiedades y relaciones del objeto formatProtection.</span><span class="sxs-lookup"><span data-stu-id="e3200-111">Read properties and relationships of formatProtection object.</span></span>|
|[<span data-ttu-id="e3200-112">Update</span><span class="sxs-lookup"><span data-stu-id="e3200-112">Update</span></span>](../api/formatprotection-update.md) | [<span data-ttu-id="e3200-113">FormatProtection</span><span class="sxs-lookup"><span data-stu-id="e3200-113">FormatProtection</span></span>](formatprotection.md)  |<span data-ttu-id="e3200-114">Actualiza el objeto FormatProtection.</span><span class="sxs-lookup"><span data-stu-id="e3200-114">Update FormatProtection object.</span></span> |

## <a name="properties"></a><span data-ttu-id="e3200-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e3200-115">Properties</span></span>
| <span data-ttu-id="e3200-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e3200-116">Property</span></span>     | <span data-ttu-id="e3200-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3200-117">Type</span></span>   |<span data-ttu-id="e3200-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3200-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e3200-119">formulaHidden</span><span class="sxs-lookup"><span data-stu-id="e3200-119">formulaHidden</span></span>|<span data-ttu-id="e3200-120">boolean</span><span class="sxs-lookup"><span data-stu-id="e3200-120">boolean</span></span>|<span data-ttu-id="e3200-p101">Indica si Excel oculta la fórmula de las celdas del rango. Un valor null indica que el rango no tiene una configuración de fórmula oculta uniforme.</span><span class="sxs-lookup"><span data-stu-id="e3200-p101">Indicates if Excel hides the formula for the cells in the range. A null value indicates that the entire range doesn't have uniform formula hidden setting.</span></span>|
|<span data-ttu-id="e3200-123">locked</span><span class="sxs-lookup"><span data-stu-id="e3200-123">locked</span></span>|<span data-ttu-id="e3200-124">boolean</span><span class="sxs-lookup"><span data-stu-id="e3200-124">boolean</span></span>|<span data-ttu-id="e3200-p102">Indica si Excel bloquea las celdas del objeto. Un valor nulo indica que todo el rango no tiene una configuración de bloqueo uniforme.</span><span class="sxs-lookup"><span data-stu-id="e3200-p102">Indicates if Excel locks the cells in the object. A null value indicates that the entire range doesn't have uniform lock setting.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e3200-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e3200-127">Relationships</span></span>
<span data-ttu-id="e3200-128">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e3200-128">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="e3200-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e3200-129">JSON representation</span></span>

<span data-ttu-id="e3200-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e3200-130">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookFormatProtection"
}-->

```json
{
  "formulaHidden": true,
  "locked": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "FormatProtection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
