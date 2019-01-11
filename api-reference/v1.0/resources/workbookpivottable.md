---
title: Tipo de recurso PivotTable
description: Representa una tabla dinámica de Excel.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: d500d4bc88608b032262cfae505385bf7ed3f072
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889211"
---
# <a name="pivottable-resource-type"></a><span data-ttu-id="32ee3-103">Tipo de recurso PivotTable</span><span class="sxs-lookup"><span data-stu-id="32ee3-103">pivotTable resource type</span></span>

<span data-ttu-id="32ee3-104">Representa una tabla dinámica de Excel.</span><span class="sxs-lookup"><span data-stu-id="32ee3-104">Represents an Excel PivotTable.</span></span>

## <a name="methods"></a><span data-ttu-id="32ee3-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="32ee3-105">Methods</span></span>

| <span data-ttu-id="32ee3-106">Método</span><span class="sxs-lookup"><span data-stu-id="32ee3-106">Method</span></span>           | <span data-ttu-id="32ee3-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32ee3-107">Return Type</span></span>    |<span data-ttu-id="32ee3-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="32ee3-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="32ee3-109">Get workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="32ee3-109">Get workbookPivotTable</span></span>](../api/workbookpivottable-get.md) | [<span data-ttu-id="32ee3-110">workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="32ee3-110">workbookPivotTable</span></span>](workbookpivottable.md) |<span data-ttu-id="32ee3-111">Lee las propiedades y relaciones del objeto workbookPivotTable.</span><span class="sxs-lookup"><span data-stu-id="32ee3-111">Read properties and relationships of workbookPivotTable object.</span></span>|
|[<span data-ttu-id="32ee3-112">Refresh</span><span class="sxs-lookup"><span data-stu-id="32ee3-112">Refresh</span></span>](../api/workbookpivottable-refresh.md)|<span data-ttu-id="32ee3-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="32ee3-113">None</span></span>|<span data-ttu-id="32ee3-114">Actualiza la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="32ee3-114">Refreshes the PivotTable.</span></span> |
|[<span data-ttu-id="32ee3-115">Refreshall</span><span class="sxs-lookup"><span data-stu-id="32ee3-115">Refreshall</span></span>](../api/workbookpivottable-refreshall.md)|<span data-ttu-id="32ee3-116">Ninguno</span><span class="sxs-lookup"><span data-stu-id="32ee3-116">None</span></span>|<span data-ttu-id="32ee3-p101">Actualizar todas las tablas de una hoja de cálculo. Tenga en cuenta que esta acción sólo está disponible en la colección de tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="32ee3-p101">Refresh all tables within given worksheet. Note that this action is available only on the pivot table collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="32ee3-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32ee3-119">Properties</span></span>
| <span data-ttu-id="32ee3-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="32ee3-120">Property</span></span>     | <span data-ttu-id="32ee3-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="32ee3-121">Type</span></span>   |<span data-ttu-id="32ee3-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="32ee3-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="32ee3-123">id</span><span class="sxs-lookup"><span data-stu-id="32ee3-123">id</span></span>|<span data-ttu-id="32ee3-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="32ee3-124">String</span></span>| <span data-ttu-id="32ee3-p102">ID la tabla dinámica.   Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="32ee3-p102">Id of the PivotTable.   Read-only.</span></span>|
|<span data-ttu-id="32ee3-127">name</span><span class="sxs-lookup"><span data-stu-id="32ee3-127">name</span></span>|<span data-ttu-id="32ee3-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="32ee3-128">String</span></span>|<span data-ttu-id="32ee3-129">Nombre de la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="32ee3-129">Name of the PivotTable.</span></span>    |

## <a name="relationships"></a><span data-ttu-id="32ee3-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="32ee3-130">Relationships</span></span>
| <span data-ttu-id="32ee3-131">Relación</span><span class="sxs-lookup"><span data-stu-id="32ee3-131">Relationship</span></span> | <span data-ttu-id="32ee3-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="32ee3-132">Type</span></span>   |<span data-ttu-id="32ee3-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="32ee3-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="32ee3-134">worksheet</span><span class="sxs-lookup"><span data-stu-id="32ee3-134">worksheet</span></span>|[<span data-ttu-id="32ee3-135">WorkbookWorksheet</span><span class="sxs-lookup"><span data-stu-id="32ee3-135">WorkbookWorksheet</span></span>](worksheet.md)| <span data-ttu-id="32ee3-p103">La hoja de cálculo que contiene la tabla dinámica actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="32ee3-p103">The worksheet containing the current PivotTable. Read-only.</span></span>   |

## <a name="json-representation"></a><span data-ttu-id="32ee3-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="32ee3-138">JSON representation</span></span>
<span data-ttu-id="32ee3-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="32ee3-139">Here is a JSON representation of the resource.</span></span>

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
