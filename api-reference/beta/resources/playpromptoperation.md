---
title: tipo de recurso playPromptOperation
description: La operación de playPrompt para obtener el resultado de la acción playPrompt.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: bc18b8f64dedd3fa4d758778bbee37c6bcfd46c6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814381"
---
# <a name="playpromptoperation-resource-type"></a><span data-ttu-id="4352c-103">tipo de recurso playPromptOperation</span><span class="sxs-lookup"><span data-stu-id="4352c-103">playPromptOperation resource type</span></span>

> <span data-ttu-id="4352c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4352c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4352c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4352c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4352c-106">La operación de playPrompt para obtener el resultado de la acción playPrompt.</span><span class="sxs-lookup"><span data-stu-id="4352c-106">The playPrompt operation to obtain the result of the playPrompt action.</span></span>

## <a name="properties"></a><span data-ttu-id="4352c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4352c-107">Properties</span></span>

| <span data-ttu-id="4352c-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4352c-108">Property</span></span>            | <span data-ttu-id="4352c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4352c-109">Type</span></span>                        | <span data-ttu-id="4352c-110">Description</span><span class="sxs-lookup"><span data-stu-id="4352c-110">Description</span></span>|
|:--------------------|:----------------------------|:-----------------------------------------------------------------------------------|
| <span data-ttu-id="4352c-111">clientContext</span><span class="sxs-lookup"><span data-stu-id="4352c-111">clientContext</span></span>       | <span data-ttu-id="4352c-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="4352c-112">String</span></span>                      | <span data-ttu-id="4352c-113">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="4352c-113">The client context.</span></span>                                                                |
| <span data-ttu-id="4352c-114">completionReason</span><span class="sxs-lookup"><span data-stu-id="4352c-114">completionReason</span></span>    | <span data-ttu-id="4352c-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="4352c-115">String</span></span>                      | <span data-ttu-id="4352c-116">Los valores posibles son: `unknown`, `completedSuccessfully` y `mediaOperationCanceled`.</span><span class="sxs-lookup"><span data-stu-id="4352c-116">Possible values are: `unknown`, `completedSuccessfully`, `mediaOperationCanceled`.</span></span> |
| <span data-ttu-id="4352c-117">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4352c-117">createdDateTime</span></span>     | <span data-ttu-id="4352c-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4352c-118">DateTimeOffset</span></span>              | <span data-ttu-id="4352c-119">La hora de inicio de la operación.</span><span class="sxs-lookup"><span data-stu-id="4352c-119">The start time of the operation.</span></span>                                                   |
| <span data-ttu-id="4352c-120">id</span><span class="sxs-lookup"><span data-stu-id="4352c-120">id</span></span>                  | <span data-ttu-id="4352c-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="4352c-121">String</span></span>                      | <span data-ttu-id="4352c-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4352c-122">Read-only.</span></span>                                                                         |
| <span data-ttu-id="4352c-123">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="4352c-123">lastActionDateTime</span></span>  | <span data-ttu-id="4352c-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4352c-124">DateTimeOffset</span></span>              | <span data-ttu-id="4352c-125">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="4352c-125">The time of the last action of the operation.</span></span>                                      |
| <span data-ttu-id="4352c-126">resultInfo</span><span class="sxs-lookup"><span data-stu-id="4352c-126">resultInfo</span></span>          | [<span data-ttu-id="4352c-127">resultInfo</span><span class="sxs-lookup"><span data-stu-id="4352c-127">resultInfo</span></span>](resultInfo.md) | <span data-ttu-id="4352c-128">La información del resultado.</span><span class="sxs-lookup"><span data-stu-id="4352c-128">The result information.</span></span> <span data-ttu-id="4352c-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4352c-129">Read-only.</span></span> <span data-ttu-id="4352c-130">Servidor que se generó.</span><span class="sxs-lookup"><span data-stu-id="4352c-130">Server generated.</span></span>                               |
| <span data-ttu-id="4352c-131">status</span><span class="sxs-lookup"><span data-stu-id="4352c-131">status</span></span>              | <span data-ttu-id="4352c-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="4352c-132">String</span></span>                      | <span data-ttu-id="4352c-133">Los valores posibles son: `notStarted`, `running`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="4352c-133">Possible values are: `notStarted`, `running`, `completed`, `failed`.</span></span>               |

## <a name="relationships"></a><span data-ttu-id="4352c-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4352c-134">Relationships</span></span>
<span data-ttu-id="4352c-135">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4352c-135">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="4352c-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4352c-136">JSON representation</span></span>

<span data-ttu-id="4352c-137">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4352c-137">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.playPromptOperation"
}-->
```json
{
  "clientContext": "String",
  "completionReason": "unknown | completedSuccessfully | mediaOperationCanceled",
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "lastActionDateTime": "String (timestamp)",
  "resultInfo": {"@odata.type": "#microsoft.graph.resultInfo"},
  "status": "notStarted | running | completed | failed"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "playPromptOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
