---
title: Tipo de recurso workbookSessionInfo
description: Proporciona información sobre la sesión del libro.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 900ebdcefbdfa83e7b72b1c926a441f1c497626a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826932"
---
# <a name="workbooksessioninfo-resource-type"></a><span data-ttu-id="67490-103">Tipo de recurso workbookSessionInfo</span><span class="sxs-lookup"><span data-stu-id="67490-103">workbookSessionInfo resource type</span></span>

<span data-ttu-id="67490-104">Proporciona información sobre la sesión del libro.</span><span class="sxs-lookup"><span data-stu-id="67490-104">Provides information about workbook session.</span></span>


## <a name="json-representation"></a><span data-ttu-id="67490-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="67490-105">JSON representation</span></span>

<span data-ttu-id="67490-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="67490-106">Here is a JSON representation of the resource</span></span>

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

## <a name="properties"></a><span data-ttu-id="67490-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67490-107">Properties</span></span>

| <span data-ttu-id="67490-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="67490-108">Property</span></span> | <span data-ttu-id="67490-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="67490-109">Type</span></span>  | <span data-ttu-id="67490-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="67490-110">Description</span></span>                               |
|:---------|:------|:------------------------------------------|
| <span data-ttu-id="67490-111">id</span><span class="sxs-lookup"><span data-stu-id="67490-111">id</span></span>  | <span data-ttu-id="67490-112">string</span><span class="sxs-lookup"><span data-stu-id="67490-112">string</span></span> | <span data-ttu-id="67490-113">Identificador de la sesión del libro.</span><span class="sxs-lookup"><span data-stu-id="67490-113">Id of the workbook session.</span></span> |
| <span data-ttu-id="67490-114">persistChanges</span><span class="sxs-lookup"><span data-stu-id="67490-114">persistChanges</span></span> | <span data-ttu-id="67490-115">boolean</span><span class="sxs-lookup"><span data-stu-id="67490-115">boolean</span></span> |  <span data-ttu-id="67490-116">`true` para la sesión persistente.</span><span class="sxs-lookup"><span data-stu-id="67490-116">`true` for persistent session.</span></span> <span data-ttu-id="67490-117">`false` para la sesión no persistente (modo de visualización)</span><span class="sxs-lookup"><span data-stu-id="67490-117">`false` for non-persistent session (view mode)</span></span> |

