---
title: tipo de recurso operationError
description: Se describen los errores en teamsAsyncOperation.
localization_priority: Normal
ms.openlocfilehash: 22590d7d955cf01385292d2796ad960b1c0ced41
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824587"
---
# <a name="operationerror-resource-type"></a><span data-ttu-id="b978b-103">tipo de recurso operationError</span><span class="sxs-lookup"><span data-stu-id="b978b-103">operationError resource type</span></span>



<span data-ttu-id="b978b-104">Se describen los errores en [teamsAsyncOperation](teamsasyncoperation.md).</span><span class="sxs-lookup"><span data-stu-id="b978b-104">Describes errors in [teamsAsyncOperation](teamsasyncoperation.md).</span></span>

## <a name="operationerror-properties"></a><span data-ttu-id="b978b-105">Propiedades de operationError</span><span class="sxs-lookup"><span data-stu-id="b978b-105">operationError Properties</span></span>
| <span data-ttu-id="b978b-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b978b-106">Property</span></span>     | <span data-ttu-id="b978b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="b978b-107">Type</span></span>   |<span data-ttu-id="b978b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b978b-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b978b-109">código</span><span class="sxs-lookup"><span data-stu-id="b978b-109">code</span></span>|<span data-ttu-id="b978b-110">cadena (sólo lectura)</span><span class="sxs-lookup"><span data-stu-id="b978b-110">string (readonly)</span></span>|<span data-ttu-id="b978b-111">Código de error de la operación.</span><span class="sxs-lookup"><span data-stu-id="b978b-111">Operation error code.</span></span>|
|<span data-ttu-id="b978b-112">mensaje</span><span class="sxs-lookup"><span data-stu-id="b978b-112">message</span></span>|<span data-ttu-id="b978b-113">cadena (sólo lectura)</span><span class="sxs-lookup"><span data-stu-id="b978b-113">string (readonly)</span></span>|<span data-ttu-id="b978b-114">Mensaje de error de la operación.</span><span class="sxs-lookup"><span data-stu-id="b978b-114">Operation error message.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b978b-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b978b-115">JSON representation</span></span>

<span data-ttu-id="b978b-116">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b978b-116">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.operationError"
}-->

```json
{
    "code": "TeamUnavailable",
    "message": "The team was not found."
}
```

<!-- uuid: 069fadaa-52db-4ced-85d5-74f7caa2c66f
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "operation error resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
