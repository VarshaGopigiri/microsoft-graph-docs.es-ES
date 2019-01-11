---
title: Tipo de recurso onenoteOperationError
description: Error de una operación de OneNote que no se pudo completar.
author: Jewan-microsoft
localization_priority: Normal
ms.openlocfilehash: df0bfd768d26c751a303f42e1f1123b863388faa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27837341"
---
# <a name="onenoteoperationerror-resource-type"></a><span data-ttu-id="95b74-103">Tipo de recurso onenoteOperationError</span><span class="sxs-lookup"><span data-stu-id="95b74-103">onenoteOperationError resource type</span></span>

<span data-ttu-id="95b74-104">Error de una operación de OneNote que no se pudo completar.</span><span class="sxs-lookup"><span data-stu-id="95b74-104">An error from a failed OneNote operation.</span></span>

## <a name="json-representation"></a><span data-ttu-id="95b74-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="95b74-105">JSON representation</span></span>

<span data-ttu-id="95b74-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="95b74-106">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onenoteOperationError"
}-->

```json
{
  "code": "string",
  "message": "string"
}

```
## <a name="properties"></a><span data-ttu-id="95b74-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95b74-107">Properties</span></span>
| <span data-ttu-id="95b74-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="95b74-108">Property</span></span>     | <span data-ttu-id="95b74-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="95b74-109">Type</span></span>   |<span data-ttu-id="95b74-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="95b74-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="95b74-111">código</span><span class="sxs-lookup"><span data-stu-id="95b74-111">code</span></span>|<span data-ttu-id="95b74-112">string</span><span class="sxs-lookup"><span data-stu-id="95b74-112">string</span></span>|<span data-ttu-id="95b74-113">Código de error.</span><span class="sxs-lookup"><span data-stu-id="95b74-113">The error code.</span></span>|
|<span data-ttu-id="95b74-114">message</span><span class="sxs-lookup"><span data-stu-id="95b74-114">message</span></span>|<span data-ttu-id="95b74-115">string</span><span class="sxs-lookup"><span data-stu-id="95b74-115">string</span></span>|<span data-ttu-id="95b74-116">Mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="95b74-116">The error message.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteOperationError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
