---
title: Tipo de recurso workbookSessionInfo
description: Proporciona información sobre la sesión del libro.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 502781c4049c9451f5ed67ff97222abf4df462d7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960276"
---
# <a name="workbooksessioninfo-resource-type"></a><span data-ttu-id="20bea-103">Tipo de recurso workbookSessionInfo</span><span class="sxs-lookup"><span data-stu-id="20bea-103">workbookSessionInfo resource type</span></span>

<span data-ttu-id="20bea-104">Proporciona información sobre la sesión del libro.</span><span class="sxs-lookup"><span data-stu-id="20bea-104">Provides information about workbook session.</span></span>


## <a name="json-representation"></a><span data-ttu-id="20bea-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="20bea-105">JSON representation</span></span>

<span data-ttu-id="20bea-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="20bea-106">Here is a JSON representation of the resource</span></span>

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

## <a name="properties"></a><span data-ttu-id="20bea-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20bea-107">Properties</span></span>

| <span data-ttu-id="20bea-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="20bea-108">Property</span></span> | <span data-ttu-id="20bea-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="20bea-109">Type</span></span>  | <span data-ttu-id="20bea-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="20bea-110">Description</span></span>                               |
|:---------|:------|:------------------------------------------|
| <span data-ttu-id="20bea-111">id</span><span class="sxs-lookup"><span data-stu-id="20bea-111">id</span></span>  | <span data-ttu-id="20bea-112">string</span><span class="sxs-lookup"><span data-stu-id="20bea-112">string</span></span> | <span data-ttu-id="20bea-113">Identificador de la sesión del libro.</span><span class="sxs-lookup"><span data-stu-id="20bea-113">Id of the workbook session.</span></span> |
| <span data-ttu-id="20bea-114">persistChanges</span><span class="sxs-lookup"><span data-stu-id="20bea-114">persistChanges</span></span> | <span data-ttu-id="20bea-115">boolean</span><span class="sxs-lookup"><span data-stu-id="20bea-115">boolean</span></span> |  <span data-ttu-id="20bea-116">`true` para la sesión persistente.</span><span class="sxs-lookup"><span data-stu-id="20bea-116">`true` for persistent session.</span></span> <span data-ttu-id="20bea-117">`false` para la sesión no persistente (modo de visualización)</span><span class="sxs-lookup"><span data-stu-id="20bea-117">`false` for non-persistent session (view mode)</span></span> |

