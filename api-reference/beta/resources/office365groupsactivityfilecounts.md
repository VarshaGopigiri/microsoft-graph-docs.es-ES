---
title: tipo de recurso office365GroupsActivityFileCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: eb2d967108d4f75064b91670ae43fb7a2dd7ce7a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084336"
---
# <a name="office365groupsactivityfilecounts-resource-type"></a><span data-ttu-id="cd782-103">tipo de recurso office365GroupsActivityFileCounts</span><span class="sxs-lookup"><span data-stu-id="cd782-103">office365GroupsActivityFileCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="cd782-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd782-104">Properties</span></span>

| <span data-ttu-id="cd782-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cd782-105">Property</span></span>          | <span data-ttu-id="cd782-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd782-106">Type</span></span>   | <span data-ttu-id="cd782-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd782-107">Description</span></span>                              |
| :---------------- | :----- | ---------------------------------------- |
| <span data-ttu-id="cd782-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="cd782-108">reportRefreshDate</span></span> | <span data-ttu-id="cd782-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="cd782-109">Date</span></span>   | <span data-ttu-id="cd782-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="cd782-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="cd782-111">total</span><span class="sxs-lookup"><span data-stu-id="cd782-111">total</span></span>             | <span data-ttu-id="cd782-112">Int64</span><span class="sxs-lookup"><span data-stu-id="cd782-112">Int64</span></span>  | <span data-ttu-id="cd782-113">El número total de archivos en la biblioteca de documentos de SharePoint del grupo.</span><span class="sxs-lookup"><span data-stu-id="cd782-113">The total number of files in the group's SharePoint document library.</span></span> |
| <span data-ttu-id="cd782-114">activo</span><span class="sxs-lookup"><span data-stu-id="cd782-114">active</span></span>            | <span data-ttu-id="cd782-115">Int64</span><span class="sxs-lookup"><span data-stu-id="cd782-115">Int64</span></span>  | <span data-ttu-id="cd782-116">El número de archivos que se han visto, editado, compartidos o sincronizado en la biblioteca de documentos de SharePoint del grupo.</span><span class="sxs-lookup"><span data-stu-id="cd782-116">The number of files that were viewed, edited, shared, or synced in the group's SharePoint document library.</span></span> |
| <span data-ttu-id="cd782-117">reportDate</span><span class="sxs-lookup"><span data-stu-id="cd782-117">reportDate</span></span>        | <span data-ttu-id="cd782-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="cd782-118">Date</span></span>   | <span data-ttu-id="cd782-119">La fecha en la que estaba activo un número de archivos en el sitio de SharePoint del grupo.</span><span class="sxs-lookup"><span data-stu-id="cd782-119">The date on which a number of files were active in the group's SharePoint site.</span></span> |
| <span data-ttu-id="cd782-120">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="cd782-120">reportPeriod</span></span>      | <span data-ttu-id="cd782-121">String</span><span class="sxs-lookup"><span data-stu-id="cd782-121">String</span></span> | <span data-ttu-id="cd782-122">El número de días que cubre el informe.</span><span class="sxs-lookup"><span data-stu-id="cd782-122">The number of days the report covers.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="cd782-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cd782-123">JSON representation</span></span>

<span data-ttu-id="cd782-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="cd782-124">The following is a JSON representation of the resource.</span></span>

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
