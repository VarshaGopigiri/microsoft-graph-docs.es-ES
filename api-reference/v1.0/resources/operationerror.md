---
title: tipo de recurso operationError
description: Se describen los errores en teamsAsyncOperation.
ms.openlocfilehash: bcd8c989c4c69336165ef1ca29e1d114d524aa9e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031577"
---
# <a name="operationerror-resource-type"></a><span data-ttu-id="6d26e-103">tipo de recurso operationError</span><span class="sxs-lookup"><span data-stu-id="6d26e-103">operationError resource type</span></span>



<span data-ttu-id="6d26e-104">Se describen los errores en [teamsAsyncOperation](teamsasyncoperation.md).</span><span class="sxs-lookup"><span data-stu-id="6d26e-104">Describes errors in [teamsAsyncOperation](teamsasyncoperation.md).</span></span>

## <a name="operationerror-properties"></a><span data-ttu-id="6d26e-105">Propiedades de operationError</span><span class="sxs-lookup"><span data-stu-id="6d26e-105">operationError Properties</span></span>
| <span data-ttu-id="6d26e-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6d26e-106">Property</span></span>     | <span data-ttu-id="6d26e-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d26e-107">Type</span></span>   |<span data-ttu-id="6d26e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d26e-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6d26e-109">código</span><span class="sxs-lookup"><span data-stu-id="6d26e-109">code</span></span>|<span data-ttu-id="6d26e-110">cadena (sólo lectura)</span><span class="sxs-lookup"><span data-stu-id="6d26e-110">string (readonly)</span></span>|<span data-ttu-id="6d26e-111">Código de error de la operación.</span><span class="sxs-lookup"><span data-stu-id="6d26e-111">Operation error code.</span></span>|
|<span data-ttu-id="6d26e-112">mensaje</span><span class="sxs-lookup"><span data-stu-id="6d26e-112">message</span></span>|<span data-ttu-id="6d26e-113">cadena (sólo lectura)</span><span class="sxs-lookup"><span data-stu-id="6d26e-113">string (readonly)</span></span>|<span data-ttu-id="6d26e-114">Mensaje de error de la operación.</span><span class="sxs-lookup"><span data-stu-id="6d26e-114">Operation error message.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="6d26e-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6d26e-115">JSON representation</span></span>

<span data-ttu-id="6d26e-116">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6d26e-116">The following is a JSON representation of the resource.</span></span>

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
