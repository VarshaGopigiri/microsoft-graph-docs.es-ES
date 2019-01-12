---
title: tipo de recurso playPromptOperation
description: La operación de playPrompt para obtener el resultado de la acción playPrompt.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: d451418482d1adf1a4b7e16dc8a6eb8ca7febdb7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937820"
---
# <a name="playpromptoperation-resource-type"></a><span data-ttu-id="3a6c4-103">tipo de recurso playPromptOperation</span><span class="sxs-lookup"><span data-stu-id="3a6c4-103">playPromptOperation resource type</span></span>

> <span data-ttu-id="3a6c4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3a6c4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3a6c4-106">La operación de playPrompt para obtener el resultado de la acción playPrompt.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-106">The playPrompt operation to obtain the result of the playPrompt action.</span></span>

## <a name="properties"></a><span data-ttu-id="3a6c4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a6c4-107">Properties</span></span>

| <span data-ttu-id="3a6c4-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3a6c4-108">Property</span></span>            | <span data-ttu-id="3a6c4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a6c4-109">Type</span></span>                        | <span data-ttu-id="3a6c4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a6c4-110">Description</span></span>|
|:--------------------|:----------------------------|:-----------------------------------------------------------------------------------|
| <span data-ttu-id="3a6c4-111">clientContext</span><span class="sxs-lookup"><span data-stu-id="3a6c4-111">clientContext</span></span>       | <span data-ttu-id="3a6c4-112">String</span><span class="sxs-lookup"><span data-stu-id="3a6c4-112">String</span></span>                      | <span data-ttu-id="3a6c4-113">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-113">The client context.</span></span>                                                                |
| <span data-ttu-id="3a6c4-114">completionReason</span><span class="sxs-lookup"><span data-stu-id="3a6c4-114">completionReason</span></span>    | <span data-ttu-id="3a6c4-115">String</span><span class="sxs-lookup"><span data-stu-id="3a6c4-115">String</span></span>                      | <span data-ttu-id="3a6c4-116">Los valores posibles son: `unknown`, `completedSuccessfully` y `mediaOperationCanceled`.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-116">Possible values are: `unknown`, `completedSuccessfully`, `mediaOperationCanceled`.</span></span> |
| <span data-ttu-id="3a6c4-117">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="3a6c4-117">createdDateTime</span></span>     | <span data-ttu-id="3a6c4-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3a6c4-118">DateTimeOffset</span></span>              | <span data-ttu-id="3a6c4-119">La hora de inicio de la operación.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-119">The start time of the operation.</span></span>                                                   |
| <span data-ttu-id="3a6c4-120">id</span><span class="sxs-lookup"><span data-stu-id="3a6c4-120">id</span></span>                  | <span data-ttu-id="3a6c4-121">String</span><span class="sxs-lookup"><span data-stu-id="3a6c4-121">String</span></span>                      | <span data-ttu-id="3a6c4-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-122">Read-only.</span></span>                                                                         |
| <span data-ttu-id="3a6c4-123">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="3a6c4-123">lastActionDateTime</span></span>  | <span data-ttu-id="3a6c4-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3a6c4-124">DateTimeOffset</span></span>              | <span data-ttu-id="3a6c4-125">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-125">The time of the last action of the operation.</span></span>                                      |
| <span data-ttu-id="3a6c4-126">resultInfo</span><span class="sxs-lookup"><span data-stu-id="3a6c4-126">resultInfo</span></span>          | [<span data-ttu-id="3a6c4-127">resultInfo</span><span class="sxs-lookup"><span data-stu-id="3a6c4-127">resultInfo</span></span>](resultInfo.md) | <span data-ttu-id="3a6c4-128">La información del resultado.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-128">The result information.</span></span> <span data-ttu-id="3a6c4-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-129">Read-only.</span></span> <span data-ttu-id="3a6c4-130">Servidor que se generó.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-130">Server generated.</span></span>                               |
| <span data-ttu-id="3a6c4-131">status</span><span class="sxs-lookup"><span data-stu-id="3a6c4-131">status</span></span>              | <span data-ttu-id="3a6c4-132">String</span><span class="sxs-lookup"><span data-stu-id="3a6c4-132">String</span></span>                      | <span data-ttu-id="3a6c4-133">Los valores posibles son: `notStarted`, `running`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-133">Possible values are: `notStarted`, `running`, `completed`, `failed`.</span></span>               |

## <a name="relationships"></a><span data-ttu-id="3a6c4-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3a6c4-134">Relationships</span></span>
<span data-ttu-id="3a6c4-135">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3a6c4-135">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="3a6c4-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3a6c4-136">JSON representation</span></span>

<span data-ttu-id="3a6c4-137">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3a6c4-137">The following is a JSON representation of the resource.</span></span>

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
