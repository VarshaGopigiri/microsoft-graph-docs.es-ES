---
title: Tipo de recurso workbookSessionInfo
description: Proporciona información sobre la sesión del libro.
ms.openlocfilehash: 84d0306a7a25aaa29e4f1eb9b87708cc97d6b50f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030484"
---
# <a name="workbooksessioninfo-resource-type"></a><span data-ttu-id="fd520-103">Tipo de recurso workbookSessionInfo</span><span class="sxs-lookup"><span data-stu-id="fd520-103">workbookSessionInfo resource type</span></span>

<span data-ttu-id="fd520-104">Proporciona información sobre la sesión del libro.</span><span class="sxs-lookup"><span data-stu-id="fd520-104">Provides information about workbook session.</span></span>


## <a name="json-representation"></a><span data-ttu-id="fd520-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fd520-105">JSON representation</span></span>

<span data-ttu-id="fd520-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fd520-106">Here is a JSON representation of the resource</span></span>

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

## <a name="properties"></a><span data-ttu-id="fd520-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd520-107">Properties</span></span>

| <span data-ttu-id="fd520-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fd520-108">Property</span></span> | <span data-ttu-id="fd520-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd520-109">Type</span></span>  | <span data-ttu-id="fd520-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd520-110">Description</span></span>                               |
|:---------|:------|:------------------------------------------|
| <span data-ttu-id="fd520-111">id</span><span class="sxs-lookup"><span data-stu-id="fd520-111">id</span></span>  | <span data-ttu-id="fd520-112">string</span><span class="sxs-lookup"><span data-stu-id="fd520-112">string</span></span> | <span data-ttu-id="fd520-113">Identificador de la sesión del libro.</span><span class="sxs-lookup"><span data-stu-id="fd520-113">Id of the workbook session.</span></span> |
| <span data-ttu-id="fd520-114">persistChanges</span><span class="sxs-lookup"><span data-stu-id="fd520-114">persistChanges</span></span> | <span data-ttu-id="fd520-115">boolean</span><span class="sxs-lookup"><span data-stu-id="fd520-115">boolean</span></span> |  <span data-ttu-id="fd520-116">`true` para la sesión persistente.</span><span class="sxs-lookup"><span data-stu-id="fd520-116">`true` for persistent session.</span></span> <span data-ttu-id="fd520-117">`false` para la sesión no persistente (modo de visualización)</span><span class="sxs-lookup"><span data-stu-id="fd520-117">`false` for non-persistent session (view mode)</span></span> |

