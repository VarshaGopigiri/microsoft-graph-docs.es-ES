---
title: Tipo de recurso workbookSessionInfo
description: Proporciona información sobre la sesión del libro.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 25812d48626c7dc5e468915f7308941a4f74b38e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860966"
---
# <a name="workbooksessioninfo-resource-type"></a><span data-ttu-id="75ec5-103">Tipo de recurso workbookSessionInfo</span><span class="sxs-lookup"><span data-stu-id="75ec5-103">workbookSessionInfo resource type</span></span>

<span data-ttu-id="75ec5-104">Proporciona información sobre la sesión del libro.</span><span class="sxs-lookup"><span data-stu-id="75ec5-104">Provides information about workbook session.</span></span>


## <a name="json-representation"></a><span data-ttu-id="75ec5-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="75ec5-105">JSON representation</span></span>

<span data-ttu-id="75ec5-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="75ec5-106">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.workbookSessionInfo"
}-->

```json
{
  "id": "string",
  "persistChanges": true
}
```

## <a name="properties"></a><span data-ttu-id="75ec5-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75ec5-107">Properties</span></span>

| <span data-ttu-id="75ec5-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75ec5-108">Property</span></span> | <span data-ttu-id="75ec5-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="75ec5-109">Type</span></span>  | <span data-ttu-id="75ec5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="75ec5-110">Description</span></span>                               |
|:---------|:------|:------------------------------------------|
| <span data-ttu-id="75ec5-111">id</span><span class="sxs-lookup"><span data-stu-id="75ec5-111">id</span></span>  | <span data-ttu-id="75ec5-112">string</span><span class="sxs-lookup"><span data-stu-id="75ec5-112">string</span></span> | <span data-ttu-id="75ec5-113">Identificador de la sesión del libro.</span><span class="sxs-lookup"><span data-stu-id="75ec5-113">Id of the workbook session.</span></span> |
| <span data-ttu-id="75ec5-114">persistChanges</span><span class="sxs-lookup"><span data-stu-id="75ec5-114">persistChanges</span></span> | <span data-ttu-id="75ec5-115">string</span><span class="sxs-lookup"><span data-stu-id="75ec5-115">string</span></span> |  <span data-ttu-id="75ec5-116">`true` para la sesión persistente.</span><span class="sxs-lookup"><span data-stu-id="75ec5-116">`true` for persistent session.</span></span> <span data-ttu-id="75ec5-117">`false` para la sesión no persistente (modo de visualización)</span><span class="sxs-lookup"><span data-stu-id="75ec5-117">`false` for non-persistent session (view mode)</span></span> |

