---
title: Tipo de recurso PivotTable
description: Representa una tabla dinámica de Excel.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: aead84b21117b896f620a0722cf42c2e6c5d1293
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831545"
---
# <a name="pivottable-resource-type"></a><span data-ttu-id="3089e-103">Tipo de recurso PivotTable</span><span class="sxs-lookup"><span data-stu-id="3089e-103">pivotTable resource type</span></span>

> <span data-ttu-id="3089e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3089e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3089e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3089e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3089e-106">Representa una tabla dinámica de Excel.</span><span class="sxs-lookup"><span data-stu-id="3089e-106">Represents an Excel PivotTable.</span></span>

## <a name="methods"></a><span data-ttu-id="3089e-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="3089e-107">Methods</span></span>

| <span data-ttu-id="3089e-108">Método</span><span class="sxs-lookup"><span data-stu-id="3089e-108">Method</span></span>           | <span data-ttu-id="3089e-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3089e-109">Return Type</span></span>    |<span data-ttu-id="3089e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3089e-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="3089e-111">Get workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="3089e-111">Get workbookPivotTable</span></span>](../api/workbookpivottable-get.md) | [<span data-ttu-id="3089e-112">workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="3089e-112">workbookPivotTable</span></span>](workbookpivottable.md) |<span data-ttu-id="3089e-113">Lee las propiedades y relaciones del objeto workbookPivotTable.</span><span class="sxs-lookup"><span data-stu-id="3089e-113">Read properties and relationships of workbookPivotTable object.</span></span>|
|[<span data-ttu-id="3089e-114">Refresh</span><span class="sxs-lookup"><span data-stu-id="3089e-114">Refresh</span></span>](../api/workbookpivottable-refresh.md)|<span data-ttu-id="3089e-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3089e-115">None</span></span>|<span data-ttu-id="3089e-116">Actualiza la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="3089e-116">Refreshes the PivotTable.</span></span> |
|[<span data-ttu-id="3089e-117">Refreshall</span><span class="sxs-lookup"><span data-stu-id="3089e-117">Refreshall</span></span>](../api/workbookpivottable-refreshall.md)|<span data-ttu-id="3089e-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3089e-118">None</span></span>|<span data-ttu-id="3089e-p102">Actualizar todas las tablas de una hoja de cálculo. Tenga en cuenta que esta acción sólo está disponible en la colección de tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="3089e-p102">Refresh all tables within given worksheet. Note that this action is available only on the pivot table collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="3089e-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3089e-121">Properties</span></span>
| <span data-ttu-id="3089e-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3089e-122">Property</span></span>     | <span data-ttu-id="3089e-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="3089e-123">Type</span></span>   |<span data-ttu-id="3089e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="3089e-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3089e-125">id</span><span class="sxs-lookup"><span data-stu-id="3089e-125">id</span></span>|<span data-ttu-id="3089e-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="3089e-126">String</span></span>| <span data-ttu-id="3089e-p103">ID la tabla dinámica.   Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3089e-p103">Id of the PivotTable.   Read-only.</span></span>|
|<span data-ttu-id="3089e-129">name</span><span class="sxs-lookup"><span data-stu-id="3089e-129">name</span></span>|<span data-ttu-id="3089e-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="3089e-130">String</span></span>|<span data-ttu-id="3089e-131">Nombre de la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="3089e-131">Name of the PivotTable.</span></span>    |

## <a name="relationships"></a><span data-ttu-id="3089e-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3089e-132">Relationships</span></span>
| <span data-ttu-id="3089e-133">Relación</span><span class="sxs-lookup"><span data-stu-id="3089e-133">Relationship</span></span> | <span data-ttu-id="3089e-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="3089e-134">Type</span></span>   |<span data-ttu-id="3089e-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="3089e-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3089e-136">worksheet</span><span class="sxs-lookup"><span data-stu-id="3089e-136">worksheet</span></span>|[<span data-ttu-id="3089e-137">worksheet</span><span class="sxs-lookup"><span data-stu-id="3089e-137">worksheet</span></span>](worksheet.md)| <span data-ttu-id="3089e-p104">La hoja de cálculo que contiene la tabla dinámica actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3089e-p104">The worksheet containing the current PivotTable. Read-only.</span></span>   |

## <a name="json-representation"></a><span data-ttu-id="3089e-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3089e-140">JSON representation</span></span>
<span data-ttu-id="3089e-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3089e-141">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
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
