---
title: Tipo de recurso PivotTable
description: Representa una tabla dinámica de Excel.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 91035b607d8c44f2d1515e9c004abd4c2235c0ec
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950861"
---
# <a name="pivottable-resource-type"></a><span data-ttu-id="9a9dc-103">Tipo de recurso PivotTable</span><span class="sxs-lookup"><span data-stu-id="9a9dc-103">pivotTable resource type</span></span>

> <span data-ttu-id="9a9dc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9a9dc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9a9dc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9a9dc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9a9dc-106">Representa una tabla dinámica de Excel.</span><span class="sxs-lookup"><span data-stu-id="9a9dc-106">Represents an Excel PivotTable.</span></span>

## <a name="methods"></a><span data-ttu-id="9a9dc-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="9a9dc-107">Methods</span></span>

| <span data-ttu-id="9a9dc-108">Método</span><span class="sxs-lookup"><span data-stu-id="9a9dc-108">Method</span></span>           | <span data-ttu-id="9a9dc-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a9dc-109">Return Type</span></span>    |<span data-ttu-id="9a9dc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a9dc-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9a9dc-111">Get workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="9a9dc-111">Get workbookPivotTable</span></span>](../api/workbookpivottable-get.md) | [<span data-ttu-id="9a9dc-112">workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="9a9dc-112">workbookPivotTable</span></span>](workbookpivottable.md) |<span data-ttu-id="9a9dc-113">Lee las propiedades y relaciones del objeto workbookPivotTable.</span><span class="sxs-lookup"><span data-stu-id="9a9dc-113">Read properties and relationships of workbookPivotTable object.</span></span>|
|[<span data-ttu-id="9a9dc-114">Refresh</span><span class="sxs-lookup"><span data-stu-id="9a9dc-114">Refresh</span></span>](../api/workbookpivottable-refresh.md)|<span data-ttu-id="9a9dc-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9a9dc-115">None</span></span>|<span data-ttu-id="9a9dc-116">Actualiza la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="9a9dc-116">Refreshes the PivotTable.</span></span> |
|[<span data-ttu-id="9a9dc-117">Refreshall</span><span class="sxs-lookup"><span data-stu-id="9a9dc-117">Refreshall</span></span>](../api/workbookpivottable-refreshall.md)|<span data-ttu-id="9a9dc-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9a9dc-118">None</span></span>|<span data-ttu-id="9a9dc-p102">Actualizar todas las tablas de una hoja de cálculo. Tenga en cuenta que esta acción sólo está disponible en la colección de tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="9a9dc-p102">Refresh all tables within given worksheet. Note that this action is available only on the pivot table collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="9a9dc-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a9dc-121">Properties</span></span>
| <span data-ttu-id="9a9dc-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9a9dc-122">Property</span></span>     | <span data-ttu-id="9a9dc-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a9dc-123">Type</span></span>   |<span data-ttu-id="9a9dc-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a9dc-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9a9dc-125">id</span><span class="sxs-lookup"><span data-stu-id="9a9dc-125">id</span></span>|<span data-ttu-id="9a9dc-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="9a9dc-126">String</span></span>| <span data-ttu-id="9a9dc-p103">ID la tabla dinámica.   Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a9dc-p103">Id of the PivotTable.   Read-only.</span></span>|
|<span data-ttu-id="9a9dc-129">name</span><span class="sxs-lookup"><span data-stu-id="9a9dc-129">name</span></span>|<span data-ttu-id="9a9dc-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="9a9dc-130">String</span></span>|<span data-ttu-id="9a9dc-131">Nombre de la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="9a9dc-131">Name of the PivotTable.</span></span>    |

## <a name="relationships"></a><span data-ttu-id="9a9dc-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9a9dc-132">Relationships</span></span>
| <span data-ttu-id="9a9dc-133">Relación</span><span class="sxs-lookup"><span data-stu-id="9a9dc-133">Relationship</span></span> | <span data-ttu-id="9a9dc-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a9dc-134">Type</span></span>   |<span data-ttu-id="9a9dc-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a9dc-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9a9dc-136">worksheet</span><span class="sxs-lookup"><span data-stu-id="9a9dc-136">worksheet</span></span>|[<span data-ttu-id="9a9dc-137">worksheet</span><span class="sxs-lookup"><span data-stu-id="9a9dc-137">worksheet</span></span>](worksheet.md)| <span data-ttu-id="9a9dc-p104">La hoja de cálculo que contiene la tabla dinámica actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a9dc-p104">The worksheet containing the current PivotTable. Read-only.</span></span>   |

## <a name="json-representation"></a><span data-ttu-id="9a9dc-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9a9dc-140">JSON representation</span></span>
<span data-ttu-id="9a9dc-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9a9dc-141">Here is a JSON representation of the resource.</span></span>

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
