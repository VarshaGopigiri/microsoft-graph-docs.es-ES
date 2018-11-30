---
title: tipo de recurso de la operación
description: El estado de una operación de larga duración.
ms.openlocfilehash: 622a17233a25709047ea852b7df5020aee3ae343
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029093"
---
# <a name="operation-resource-type"></a><span data-ttu-id="98e9c-103">tipo de recurso de la operación</span><span class="sxs-lookup"><span data-stu-id="98e9c-103">operation resource type</span></span>

<span data-ttu-id="98e9c-104">El estado de una operación de larga duración.</span><span class="sxs-lookup"><span data-stu-id="98e9c-104">The status of a long-running operation.</span></span>

## <a name="json-representation"></a><span data-ttu-id="98e9c-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="98e9c-105">JSON representation</span></span>

<span data-ttu-id="98e9c-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="98e9c-106">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.operation"
}-->

```json
{
  "createdDateTime": "String (timestamp)",
  "lastActionDateTime": "String (timestamp)",
  "status": "notStarted | running | completed | failed"
}

```
## <a name="properties"></a><span data-ttu-id="98e9c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="98e9c-107">Properties</span></span>
| <span data-ttu-id="98e9c-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="98e9c-108">Property</span></span>     | <span data-ttu-id="98e9c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="98e9c-109">Type</span></span>   |<span data-ttu-id="98e9c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="98e9c-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="98e9c-111">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="98e9c-111">createdDateTime</span></span>| <span data-ttu-id="98e9c-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="98e9c-112">DateTimeOffset</span></span> |<span data-ttu-id="98e9c-113">La hora de inicio de la operación.</span><span class="sxs-lookup"><span data-stu-id="98e9c-113">The start time of the operation.</span></span>|
|<span data-ttu-id="98e9c-114">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="98e9c-114">lastActionDateTime</span></span>| <span data-ttu-id="98e9c-115">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="98e9c-115">DateTimeOffset</span></span> |<span data-ttu-id="98e9c-116">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="98e9c-116">The time of the last action of the operation.</span></span>|
|<span data-ttu-id="98e9c-117">status</span><span class="sxs-lookup"><span data-stu-id="98e9c-117">status</span></span>|<span data-ttu-id="98e9c-118">operationStatus</span><span class="sxs-lookup"><span data-stu-id="98e9c-118">operationStatus</span></span>|<span data-ttu-id="98e9c-119">Estado actual de la operación: `notStarted`, `running`, `completed` o `failed`</span><span class="sxs-lookup"><span data-stu-id="98e9c-119">The current status of the operation: `notStarted`, `running`, `completed`, `failed`</span></span> |

<!-- uuid: 13fa92b1-3b41-498b-aab1-f943464a124f
2018-03-30 10:29:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "operation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
