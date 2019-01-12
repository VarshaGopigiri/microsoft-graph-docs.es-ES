---
title: Tipo de recurso PivotTable
description: Representa una tabla dinámica de Excel.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 5f6360ce1eacc313f1bcc8a9f59b44b216a87b84
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27958743"
---
# <a name="pivottable-resource-type"></a><span data-ttu-id="b134b-103">Tipo de recurso PivotTable</span><span class="sxs-lookup"><span data-stu-id="b134b-103">pivotTable resource type</span></span>

<span data-ttu-id="b134b-104">Representa una tabla dinámica de Excel.</span><span class="sxs-lookup"><span data-stu-id="b134b-104">Represents an Excel PivotTable.</span></span>

## <a name="methods"></a><span data-ttu-id="b134b-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="b134b-105">Methods</span></span>

| <span data-ttu-id="b134b-106">Método</span><span class="sxs-lookup"><span data-stu-id="b134b-106">Method</span></span>           | <span data-ttu-id="b134b-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b134b-107">Return Type</span></span>    |<span data-ttu-id="b134b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b134b-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="b134b-109">Get workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="b134b-109">Get workbookPivotTable</span></span>](../api/workbookpivottable-get.md) | [<span data-ttu-id="b134b-110">workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="b134b-110">workbookPivotTable</span></span>](workbookpivottable.md) |<span data-ttu-id="b134b-111">Lee las propiedades y relaciones del objeto workbookPivotTable.</span><span class="sxs-lookup"><span data-stu-id="b134b-111">Read properties and relationships of workbookPivotTable object.</span></span>|
|[<span data-ttu-id="b134b-112">Refresh</span><span class="sxs-lookup"><span data-stu-id="b134b-112">Refresh</span></span>](../api/workbookpivottable-refresh.md)|<span data-ttu-id="b134b-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b134b-113">None</span></span>|<span data-ttu-id="b134b-114">Actualiza la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="b134b-114">Refreshes the PivotTable.</span></span> |
|[<span data-ttu-id="b134b-115">Refreshall</span><span class="sxs-lookup"><span data-stu-id="b134b-115">Refreshall</span></span>](../api/workbookpivottable-refreshall.md)|<span data-ttu-id="b134b-116">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b134b-116">None</span></span>|<span data-ttu-id="b134b-p101">Actualizar todas las tablas de una hoja de cálculo. Tenga en cuenta que esta acción sólo está disponible en la colección de tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="b134b-p101">Refresh all tables within given worksheet. Note that this action is available only on the pivot table collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="b134b-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b134b-119">Properties</span></span>
| <span data-ttu-id="b134b-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b134b-120">Property</span></span>     | <span data-ttu-id="b134b-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="b134b-121">Type</span></span>   |<span data-ttu-id="b134b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b134b-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b134b-123">id</span><span class="sxs-lookup"><span data-stu-id="b134b-123">id</span></span>|<span data-ttu-id="b134b-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="b134b-124">String</span></span>| <span data-ttu-id="b134b-p102">ID la tabla dinámica.   Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b134b-p102">Id of the PivotTable.   Read-only.</span></span>|
|<span data-ttu-id="b134b-127">name</span><span class="sxs-lookup"><span data-stu-id="b134b-127">name</span></span>|<span data-ttu-id="b134b-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="b134b-128">String</span></span>|<span data-ttu-id="b134b-129">Nombre de la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="b134b-129">Name of the PivotTable.</span></span>    |

## <a name="relationships"></a><span data-ttu-id="b134b-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b134b-130">Relationships</span></span>
| <span data-ttu-id="b134b-131">Relación</span><span class="sxs-lookup"><span data-stu-id="b134b-131">Relationship</span></span> | <span data-ttu-id="b134b-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="b134b-132">Type</span></span>   |<span data-ttu-id="b134b-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="b134b-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b134b-134">worksheet</span><span class="sxs-lookup"><span data-stu-id="b134b-134">worksheet</span></span>|[<span data-ttu-id="b134b-135">WorkbookWorksheet</span><span class="sxs-lookup"><span data-stu-id="b134b-135">WorkbookWorksheet</span></span>](worksheet.md)| <span data-ttu-id="b134b-p103">La hoja de cálculo que contiene la tabla dinámica actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b134b-p103">The worksheet containing the current PivotTable. Read-only.</span></span>   |

## <a name="json-representation"></a><span data-ttu-id="b134b-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b134b-138">JSON representation</span></span>
<span data-ttu-id="b134b-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b134b-139">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookPivotTable"
}-->

```json
{
  "id": "String (identifier)",
  "name": "String"
}

```
