---
title: Tipo de recurso PivotTable
description: Representa una tabla dinámica de Excel.
author: lumine2008
ms.openlocfilehash: 68075aebeac9c0846e48739daf65e5bf97e4d6f5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334114"
---
# <a name="pivottable-resource-type"></a><span data-ttu-id="5f0db-103">Tipo de recurso PivotTable</span><span class="sxs-lookup"><span data-stu-id="5f0db-103">pivotTable resource type</span></span>

<span data-ttu-id="5f0db-104">Representa una tabla dinámica de Excel.</span><span class="sxs-lookup"><span data-stu-id="5f0db-104">Represents an Excel PivotTable.</span></span>

## <a name="methods"></a><span data-ttu-id="5f0db-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f0db-105">Methods</span></span>

| <span data-ttu-id="5f0db-106">Método</span><span class="sxs-lookup"><span data-stu-id="5f0db-106">Method</span></span>           | <span data-ttu-id="5f0db-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f0db-107">Return Type</span></span>    |<span data-ttu-id="5f0db-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f0db-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="5f0db-109">Get workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="5f0db-109">Get workbookPivotTable</span></span>](../api/workbookpivottable-get.md) | [<span data-ttu-id="5f0db-110">workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="5f0db-110">workbookPivotTable</span></span>](workbookpivottable.md) |<span data-ttu-id="5f0db-111">Lee las propiedades y relaciones del objeto workbookPivotTable.</span><span class="sxs-lookup"><span data-stu-id="5f0db-111">Read properties and relationships of workbookPivotTable object.</span></span>|
|[<span data-ttu-id="5f0db-112">Refresh</span><span class="sxs-lookup"><span data-stu-id="5f0db-112">Refresh</span></span>](../api/workbookpivottable-refresh.md)|<span data-ttu-id="5f0db-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5f0db-113">None</span></span>|<span data-ttu-id="5f0db-114">Actualiza la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="5f0db-114">Refreshes the PivotTable.</span></span> |
|[<span data-ttu-id="5f0db-115">Refreshall</span><span class="sxs-lookup"><span data-stu-id="5f0db-115">Refreshall</span></span>](../api/workbookpivottable-refreshall.md)|<span data-ttu-id="5f0db-116">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5f0db-116">None</span></span>|<span data-ttu-id="5f0db-p101">Actualizar todas las tablas de una hoja de cálculo. Tenga en cuenta que esta acción sólo está disponible en la colección de tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="5f0db-p101">Refresh all tables within given worksheet. Note that this action is available only on the pivot table collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="5f0db-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f0db-119">Properties</span></span>
| <span data-ttu-id="5f0db-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5f0db-120">Property</span></span>     | <span data-ttu-id="5f0db-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f0db-121">Type</span></span>   |<span data-ttu-id="5f0db-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f0db-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5f0db-123">id</span><span class="sxs-lookup"><span data-stu-id="5f0db-123">id</span></span>|<span data-ttu-id="5f0db-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="5f0db-124">String</span></span>| <span data-ttu-id="5f0db-p102">ID la tabla dinámica.   Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5f0db-p102">Id of the PivotTable.   Read-only.</span></span>|
|<span data-ttu-id="5f0db-127">name</span><span class="sxs-lookup"><span data-stu-id="5f0db-127">name</span></span>|<span data-ttu-id="5f0db-128">String</span><span class="sxs-lookup"><span data-stu-id="5f0db-128">String</span></span>|<span data-ttu-id="5f0db-129">Nombre de la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="5f0db-129">Name of the PivotTable.</span></span>    |

## <a name="relationships"></a><span data-ttu-id="5f0db-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5f0db-130">Relationships</span></span>
| <span data-ttu-id="5f0db-131">Relación</span><span class="sxs-lookup"><span data-stu-id="5f0db-131">Relationship</span></span> | <span data-ttu-id="5f0db-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f0db-132">Type</span></span>   |<span data-ttu-id="5f0db-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f0db-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5f0db-134">worksheet</span><span class="sxs-lookup"><span data-stu-id="5f0db-134">worksheet</span></span>|[<span data-ttu-id="5f0db-135">WorkbookWorksheet</span><span class="sxs-lookup"><span data-stu-id="5f0db-135">WorkbookWorksheet</span></span>](worksheet.md)| <span data-ttu-id="5f0db-p103">La hoja de cálculo que contiene la tabla dinámica actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5f0db-p103">The worksheet containing the current PivotTable. Read-only.</span></span>   |

## <a name="json-representation"></a><span data-ttu-id="5f0db-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5f0db-138">JSON representation</span></span>
<span data-ttu-id="5f0db-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5f0db-139">Here is a JSON representation of the resource.</span></span>

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
