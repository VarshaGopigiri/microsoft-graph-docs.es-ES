---
title: Tipo de recurso FormatProtection
description: Representa la protección de formato de un objeto range.
localization_priority: Normal
ms.openlocfilehash: 0b4add2e30a1e475adcb162903f771ce760f9285
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805624"
---
# <a name="formatprotection-resource-type"></a><span data-ttu-id="961aa-103">Tipo de recurso FormatProtection</span><span class="sxs-lookup"><span data-stu-id="961aa-103">FormatProtection resource type</span></span>

> <span data-ttu-id="961aa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="961aa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="961aa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="961aa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="961aa-106">Representa la protección de formato de un objeto range.</span><span class="sxs-lookup"><span data-stu-id="961aa-106">Represents the format protection of a range object.</span></span>


## <a name="methods"></a><span data-ttu-id="961aa-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="961aa-107">Methods</span></span>

| <span data-ttu-id="961aa-108">Método</span><span class="sxs-lookup"><span data-stu-id="961aa-108">Method</span></span>           | <span data-ttu-id="961aa-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="961aa-109">Return Type</span></span>    |<span data-ttu-id="961aa-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="961aa-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="961aa-111">Get FormatProtection</span><span class="sxs-lookup"><span data-stu-id="961aa-111">Get FormatProtection</span></span>](../api/formatprotection-get.md) | [<span data-ttu-id="961aa-112">FormatProtection</span><span class="sxs-lookup"><span data-stu-id="961aa-112">FormatProtection</span></span>](formatprotection.md) |<span data-ttu-id="961aa-113">Lee las propiedades y relaciones del objeto formatProtection.</span><span class="sxs-lookup"><span data-stu-id="961aa-113">Read properties and relationships of formatProtection object.</span></span>|
|[<span data-ttu-id="961aa-114">Update</span><span class="sxs-lookup"><span data-stu-id="961aa-114">Update</span></span>](../api/formatprotection-update.md) | [<span data-ttu-id="961aa-115">FormatProtection</span><span class="sxs-lookup"><span data-stu-id="961aa-115">FormatProtection</span></span>](formatprotection.md)  |<span data-ttu-id="961aa-116">Actualiza el objeto FormatProtection.</span><span class="sxs-lookup"><span data-stu-id="961aa-116">Update FormatProtection object.</span></span> |

## <a name="properties"></a><span data-ttu-id="961aa-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="961aa-117">Properties</span></span>
| <span data-ttu-id="961aa-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="961aa-118">Property</span></span>     | <span data-ttu-id="961aa-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="961aa-119">Type</span></span>   |<span data-ttu-id="961aa-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="961aa-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="961aa-121">formulaHidden</span><span class="sxs-lookup"><span data-stu-id="961aa-121">formulaHidden</span></span>|<span data-ttu-id="961aa-122">boolean</span><span class="sxs-lookup"><span data-stu-id="961aa-122">boolean</span></span>|<span data-ttu-id="961aa-p102">Indica si Excel oculta la fórmula de las celdas del rango. Un valor null indica que el rango no tiene una configuración de fórmula oculta uniforme.</span><span class="sxs-lookup"><span data-stu-id="961aa-p102">Indicates if Excel hides the formula for the cells in the range. A null value indicates that the entire range doesn't have uniform formula hidden setting.</span></span>|
|<span data-ttu-id="961aa-125">locked</span><span class="sxs-lookup"><span data-stu-id="961aa-125">locked</span></span>|<span data-ttu-id="961aa-126">boolean</span><span class="sxs-lookup"><span data-stu-id="961aa-126">boolean</span></span>|<span data-ttu-id="961aa-p103">Indica si Excel bloquea las celdas del objeto. Un valor nulo indica que todo el rango no tiene una configuración de bloqueo uniforme.</span><span class="sxs-lookup"><span data-stu-id="961aa-p103">Indicates if Excel locks the cells in the object. A null value indicates that the entire range doesn't have uniform lock setting.</span></span>|

## <a name="relationships"></a><span data-ttu-id="961aa-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="961aa-129">Relationships</span></span>
<span data-ttu-id="961aa-130">Ninguno</span><span class="sxs-lookup"><span data-stu-id="961aa-130">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="961aa-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="961aa-131">JSON representation</span></span>

<span data-ttu-id="961aa-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="961aa-132">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.formatProtection"
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
