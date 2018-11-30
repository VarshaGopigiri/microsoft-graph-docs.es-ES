---
title: Tipo de recurso PivotTable
description: Representa una tabla dinámica de Excel.
ms.openlocfilehash: b4ddd0c1bb9e4ee13aaf3d1b4472c4e750e3a755
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029258"
---
# <a name="pivottable-resource-type"></a><span data-ttu-id="d976a-103">Tipo de recurso PivotTable</span><span class="sxs-lookup"><span data-stu-id="d976a-103">pivotTable resource type</span></span>

<span data-ttu-id="d976a-104">Representa una tabla dinámica de Excel.</span><span class="sxs-lookup"><span data-stu-id="d976a-104">Represents an Excel PivotTable.</span></span>

## <a name="methods"></a><span data-ttu-id="d976a-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="d976a-105">Methods</span></span>

| <span data-ttu-id="d976a-106">Método</span><span class="sxs-lookup"><span data-stu-id="d976a-106">Method</span></span>           | <span data-ttu-id="d976a-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d976a-107">Return Type</span></span>    |<span data-ttu-id="d976a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d976a-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d976a-109">Get workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="d976a-109">Get workbookPivotTable</span></span>](../api/workbookpivottable-get.md) | [<span data-ttu-id="d976a-110">workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="d976a-110">workbookPivotTable</span></span>](workbookpivottable.md) |<span data-ttu-id="d976a-111">Lee las propiedades y relaciones del objeto workbookPivotTable.</span><span class="sxs-lookup"><span data-stu-id="d976a-111">Read properties and relationships of workbookPivotTable object.</span></span>|
|[<span data-ttu-id="d976a-112">Refresh</span><span class="sxs-lookup"><span data-stu-id="d976a-112">Refresh</span></span>](../api/workbookpivottable-refresh.md)|<span data-ttu-id="d976a-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d976a-113">None</span></span>|<span data-ttu-id="d976a-114">Actualiza la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="d976a-114">Refreshes the PivotTable.</span></span> |
|[<span data-ttu-id="d976a-115">Refreshall</span><span class="sxs-lookup"><span data-stu-id="d976a-115">Refreshall</span></span>](../api/workbookpivottable-refreshall.md)|<span data-ttu-id="d976a-116">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d976a-116">None</span></span>|<span data-ttu-id="d976a-p101">Actualizar todas las tablas de una hoja de cálculo. Tenga en cuenta que esta acción sólo está disponible en la colección de tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="d976a-p101">Refresh all tables within given worksheet. Note that this action is available only on the pivot table collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="d976a-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d976a-119">Properties</span></span>
| <span data-ttu-id="d976a-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d976a-120">Property</span></span>     | <span data-ttu-id="d976a-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="d976a-121">Type</span></span>   |<span data-ttu-id="d976a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d976a-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d976a-123">id</span><span class="sxs-lookup"><span data-stu-id="d976a-123">id</span></span>|<span data-ttu-id="d976a-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="d976a-124">String</span></span>| <span data-ttu-id="d976a-p102">ID la tabla dinámica.   Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d976a-p102">Id of the PivotTable.   Read-only.</span></span>|
|<span data-ttu-id="d976a-127">name</span><span class="sxs-lookup"><span data-stu-id="d976a-127">name</span></span>|<span data-ttu-id="d976a-128">String</span><span class="sxs-lookup"><span data-stu-id="d976a-128">String</span></span>|<span data-ttu-id="d976a-129">Nombre de la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="d976a-129">Name of the PivotTable.</span></span>    |

## <a name="relationships"></a><span data-ttu-id="d976a-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d976a-130">Relationships</span></span>
| <span data-ttu-id="d976a-131">Relación</span><span class="sxs-lookup"><span data-stu-id="d976a-131">Relationship</span></span> | <span data-ttu-id="d976a-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="d976a-132">Type</span></span>   |<span data-ttu-id="d976a-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="d976a-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d976a-134">worksheet</span><span class="sxs-lookup"><span data-stu-id="d976a-134">worksheet</span></span>|[<span data-ttu-id="d976a-135">WorkbookWorksheet</span><span class="sxs-lookup"><span data-stu-id="d976a-135">WorkbookWorksheet</span></span>](worksheet.md)| <span data-ttu-id="d976a-p103">La hoja de cálculo que contiene la tabla dinámica actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d976a-p103">The worksheet containing the current PivotTable. Read-only.</span></span>   |

## <a name="json-representation"></a><span data-ttu-id="d976a-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d976a-138">JSON representation</span></span>
<span data-ttu-id="d976a-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d976a-139">Here is a JSON representation of the resource.</span></span>

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
