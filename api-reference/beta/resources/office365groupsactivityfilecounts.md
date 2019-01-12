---
title: tipo de recurso office365GroupsActivityFileCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: adff009d9047aa147c8042059fbdab8491288fb7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972561"
---
# <a name="office365groupsactivityfilecounts-resource-type"></a><span data-ttu-id="aeebe-103">tipo de recurso office365GroupsActivityFileCounts</span><span class="sxs-lookup"><span data-stu-id="aeebe-103">office365GroupsActivityFileCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="aeebe-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aeebe-104">Properties</span></span>

| <span data-ttu-id="aeebe-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aeebe-105">Property</span></span>          | <span data-ttu-id="aeebe-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeebe-106">Type</span></span>   | <span data-ttu-id="aeebe-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeebe-107">Description</span></span>                              |
| :---------------- | :----- | ---------------------------------------- |
| <span data-ttu-id="aeebe-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="aeebe-108">reportRefreshDate</span></span> | <span data-ttu-id="aeebe-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="aeebe-109">Date</span></span>   | <span data-ttu-id="aeebe-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="aeebe-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="aeebe-111">total</span><span class="sxs-lookup"><span data-stu-id="aeebe-111">total</span></span>             | <span data-ttu-id="aeebe-112">Int64</span><span class="sxs-lookup"><span data-stu-id="aeebe-112">Int64</span></span>  | <span data-ttu-id="aeebe-113">El número total de archivos en la biblioteca de documentos de SharePoint del grupo.</span><span class="sxs-lookup"><span data-stu-id="aeebe-113">The total number of files in the group's SharePoint document library.</span></span> |
| <span data-ttu-id="aeebe-114">activo</span><span class="sxs-lookup"><span data-stu-id="aeebe-114">active</span></span>            | <span data-ttu-id="aeebe-115">Int64</span><span class="sxs-lookup"><span data-stu-id="aeebe-115">Int64</span></span>  | <span data-ttu-id="aeebe-116">El número de archivos que se han visto, editado, compartidos o sincronizado en la biblioteca de documentos de SharePoint del grupo.</span><span class="sxs-lookup"><span data-stu-id="aeebe-116">The number of files that were viewed, edited, shared, or synced in the group's SharePoint document library.</span></span> |
| <span data-ttu-id="aeebe-117">reportDate</span><span class="sxs-lookup"><span data-stu-id="aeebe-117">reportDate</span></span>        | <span data-ttu-id="aeebe-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="aeebe-118">Date</span></span>   | <span data-ttu-id="aeebe-119">La fecha en la que estaba activo un número de archivos en el sitio de SharePoint del grupo.</span><span class="sxs-lookup"><span data-stu-id="aeebe-119">The date on which a number of files were active in the group's SharePoint site.</span></span> |
| <span data-ttu-id="aeebe-120">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="aeebe-120">reportPeriod</span></span>      | <span data-ttu-id="aeebe-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="aeebe-121">String</span></span> | <span data-ttu-id="aeebe-122">El número de días que cubre el informe.</span><span class="sxs-lookup"><span data-stu-id="aeebe-122">The number of days the report covers.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="aeebe-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="aeebe-123">JSON representation</span></span>

<span data-ttu-id="aeebe-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="aeebe-124">The following is a JSON representation of the resource.</span></span>

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
