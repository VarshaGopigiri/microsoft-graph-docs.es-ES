---
title: Tipo de recurso workbookSessionInfo
description: Proporciona información sobre la sesión del libro.
author: lumine2008
ms.openlocfilehash: 5a86fd4dfd653f16445eeccad8478db56db0ac5f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316845"
---
# <a name="workbooksessioninfo-resource-type"></a><span data-ttu-id="aaf5e-103">Tipo de recurso workbookSessionInfo</span><span class="sxs-lookup"><span data-stu-id="aaf5e-103">workbookSessionInfo resource type</span></span>

<span data-ttu-id="aaf5e-104">Proporciona información sobre la sesión del libro.</span><span class="sxs-lookup"><span data-stu-id="aaf5e-104">Provides information about workbook session.</span></span>


## <a name="json-representation"></a><span data-ttu-id="aaf5e-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="aaf5e-105">JSON representation</span></span>

<span data-ttu-id="aaf5e-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="aaf5e-106">Here is a JSON representation of the resource</span></span>

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

## <a name="properties"></a><span data-ttu-id="aaf5e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aaf5e-107">Properties</span></span>

| <span data-ttu-id="aaf5e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aaf5e-108">Property</span></span> | <span data-ttu-id="aaf5e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="aaf5e-109">Type</span></span>  | <span data-ttu-id="aaf5e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="aaf5e-110">Description</span></span>                               |
|:---------|:------|:------------------------------------------|
| <span data-ttu-id="aaf5e-111">id</span><span class="sxs-lookup"><span data-stu-id="aaf5e-111">id</span></span>  | <span data-ttu-id="aaf5e-112">string</span><span class="sxs-lookup"><span data-stu-id="aaf5e-112">string</span></span> | <span data-ttu-id="aaf5e-113">Identificador de la sesión del libro.</span><span class="sxs-lookup"><span data-stu-id="aaf5e-113">Id of the workbook session.</span></span> |
| <span data-ttu-id="aaf5e-114">persistChanges</span><span class="sxs-lookup"><span data-stu-id="aaf5e-114">persistChanges</span></span> | <span data-ttu-id="aaf5e-115">string</span><span class="sxs-lookup"><span data-stu-id="aaf5e-115">string</span></span> |  <span data-ttu-id="aaf5e-116">`true` para la sesión persistente.</span><span class="sxs-lookup"><span data-stu-id="aaf5e-116">`true` for persistent session.</span></span> <span data-ttu-id="aaf5e-117">`false` para la sesión no persistente (modo de visualización)</span><span class="sxs-lookup"><span data-stu-id="aaf5e-117">`false` for non-persistent session (view mode)</span></span> |

