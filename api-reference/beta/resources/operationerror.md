---
title: tipo de recurso operationError
description: Se describen los errores en teamsAsyncOperation.
localization_priority: Normal
ms.openlocfilehash: 423f426df92e99754af0abf4c9c8088eea61d5ea
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890296"
---
# <a name="operationerror-resource-type"></a><span data-ttu-id="f4afd-103">tipo de recurso operationError</span><span class="sxs-lookup"><span data-stu-id="f4afd-103">operationError resource type</span></span>

> <span data-ttu-id="f4afd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f4afd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f4afd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f4afd-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f4afd-106">Se describen los errores en [teamsAsyncOperation](teamsasyncoperation.md).</span><span class="sxs-lookup"><span data-stu-id="f4afd-106">Describes errors in [teamsAsyncOperation](teamsasyncoperation.md).</span></span>

## <a name="operationerror-properties"></a><span data-ttu-id="f4afd-107">Propiedades de operationError</span><span class="sxs-lookup"><span data-stu-id="f4afd-107">operationError Properties</span></span>
| <span data-ttu-id="f4afd-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f4afd-108">Property</span></span>     | <span data-ttu-id="f4afd-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4afd-109">Type</span></span>   |<span data-ttu-id="f4afd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4afd-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f4afd-111">código</span><span class="sxs-lookup"><span data-stu-id="f4afd-111">code</span></span>|<span data-ttu-id="f4afd-112">cadena (sólo lectura)</span><span class="sxs-lookup"><span data-stu-id="f4afd-112">string (readonly)</span></span>|<span data-ttu-id="f4afd-113">Código de error de la operación.</span><span class="sxs-lookup"><span data-stu-id="f4afd-113">Operation error code.</span></span>|
|<span data-ttu-id="f4afd-114">mensaje</span><span class="sxs-lookup"><span data-stu-id="f4afd-114">message</span></span>|<span data-ttu-id="f4afd-115">cadena (sólo lectura)</span><span class="sxs-lookup"><span data-stu-id="f4afd-115">string (readonly)</span></span>|<span data-ttu-id="f4afd-116">Mensaje de error de la operación.</span><span class="sxs-lookup"><span data-stu-id="f4afd-116">Operation error message.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f4afd-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f4afd-117">JSON representation</span></span>

<span data-ttu-id="f4afd-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f4afd-118">The following is a JSON representation of the resource.</span></span>

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
