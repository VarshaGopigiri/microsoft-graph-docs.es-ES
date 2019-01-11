---
title: tipo de recurso office365GroupsActivityFileCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 856bb4c74c8af35775b6fe71cb75d89935440bdb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27819190"
---
# <a name="office365groupsactivityfilecounts-resource-type"></a><span data-ttu-id="163ea-103">tipo de recurso office365GroupsActivityFileCounts</span><span class="sxs-lookup"><span data-stu-id="163ea-103">office365GroupsActivityFileCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="163ea-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="163ea-104">Properties</span></span>

| <span data-ttu-id="163ea-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="163ea-105">Property</span></span>          | <span data-ttu-id="163ea-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="163ea-106">Type</span></span>   | <span data-ttu-id="163ea-107">Description</span><span class="sxs-lookup"><span data-stu-id="163ea-107">Description</span></span>                              |
| :---------------- | :----- | ---------------------------------------- |
| <span data-ttu-id="163ea-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="163ea-108">reportRefreshDate</span></span> | <span data-ttu-id="163ea-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="163ea-109">Date</span></span>   | <span data-ttu-id="163ea-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="163ea-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="163ea-111">total</span><span class="sxs-lookup"><span data-stu-id="163ea-111">total</span></span>             | <span data-ttu-id="163ea-112">Int64</span><span class="sxs-lookup"><span data-stu-id="163ea-112">Int64</span></span>  | <span data-ttu-id="163ea-113">El número total de archivos en la biblioteca de documentos de SharePoint del grupo.</span><span class="sxs-lookup"><span data-stu-id="163ea-113">The total number of files in the group's SharePoint document library.</span></span> |
| <span data-ttu-id="163ea-114">activo</span><span class="sxs-lookup"><span data-stu-id="163ea-114">active</span></span>            | <span data-ttu-id="163ea-115">Int64</span><span class="sxs-lookup"><span data-stu-id="163ea-115">Int64</span></span>  | <span data-ttu-id="163ea-116">El número de archivos que se han visto, editado, compartidos o sincronizado en la biblioteca de documentos de SharePoint del grupo.</span><span class="sxs-lookup"><span data-stu-id="163ea-116">The number of files that were viewed, edited, shared, or synced in the group's SharePoint document library.</span></span> |
| <span data-ttu-id="163ea-117">reportDate</span><span class="sxs-lookup"><span data-stu-id="163ea-117">reportDate</span></span>        | <span data-ttu-id="163ea-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="163ea-118">Date</span></span>   | <span data-ttu-id="163ea-119">La fecha en la que estaba activo un número de archivos en el sitio de SharePoint del grupo.</span><span class="sxs-lookup"><span data-stu-id="163ea-119">The date on which a number of files were active in the group's SharePoint site.</span></span> |
| <span data-ttu-id="163ea-120">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="163ea-120">reportPeriod</span></span>      | <span data-ttu-id="163ea-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="163ea-121">String</span></span> | <span data-ttu-id="163ea-122">El número de días que cubre el informe.</span><span class="sxs-lookup"><span data-stu-id="163ea-122">The number of days the report covers.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="163ea-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="163ea-123">JSON representation</span></span>

<span data-ttu-id="163ea-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="163ea-124">The following is a JSON representation of the resource.</span></span>

<!-- {

  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365GroupsActivityFileCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "total": 1024, 
  "active": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
