---
title: tipo de recurso operationError
description: Se describen los errores en teamsAsyncOperation.
ms.openlocfilehash: 0207f490328d377fedab72d2a5300baaf3645150
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085322"
---
# <a name="operationerror-resource-type"></a><span data-ttu-id="d1330-103">tipo de recurso operationError</span><span class="sxs-lookup"><span data-stu-id="d1330-103">operationError resource type</span></span>

> <span data-ttu-id="d1330-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d1330-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d1330-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d1330-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d1330-106">Se describen los errores en [teamsAsyncOperation](teamsasyncoperation.md).</span><span class="sxs-lookup"><span data-stu-id="d1330-106">Describes errors in [teamsAsyncOperation](teamsasyncoperation.md).</span></span>

## <a name="operationerror-properties"></a><span data-ttu-id="d1330-107">Propiedades de operationError</span><span class="sxs-lookup"><span data-stu-id="d1330-107">operationError Properties</span></span>
| <span data-ttu-id="d1330-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d1330-108">Property</span></span>     | <span data-ttu-id="d1330-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1330-109">Type</span></span>   |<span data-ttu-id="d1330-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1330-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d1330-111">código</span><span class="sxs-lookup"><span data-stu-id="d1330-111">code</span></span>|<span data-ttu-id="d1330-112">cadena (sólo lectura)</span><span class="sxs-lookup"><span data-stu-id="d1330-112">string (readonly)</span></span>|<span data-ttu-id="d1330-113">Código de error de la operación.</span><span class="sxs-lookup"><span data-stu-id="d1330-113">Operation error code.</span></span>|
|<span data-ttu-id="d1330-114">mensaje</span><span class="sxs-lookup"><span data-stu-id="d1330-114">message</span></span>|<span data-ttu-id="d1330-115">cadena (sólo lectura)</span><span class="sxs-lookup"><span data-stu-id="d1330-115">string (readonly)</span></span>|<span data-ttu-id="d1330-116">Mensaje de error de la operación.</span><span class="sxs-lookup"><span data-stu-id="d1330-116">Operation error message.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d1330-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d1330-117">JSON representation</span></span>

<span data-ttu-id="d1330-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d1330-118">The following is a JSON representation of the resource.</span></span>

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
