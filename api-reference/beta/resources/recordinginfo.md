---
title: tipo de recurso recordingInfo
description: Información de grabación de un participante.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: 85c2710452905f97235928bae71ff60c2d22983f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27891941"
---
# <a name="recordinginfo-resource-type"></a><span data-ttu-id="41641-103">tipo de recurso recordingInfo</span><span class="sxs-lookup"><span data-stu-id="41641-103">recordingInfo resource type</span></span>

> <span data-ttu-id="41641-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="41641-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="41641-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="41641-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="41641-106">Información de grabación de un participante.</span><span class="sxs-lookup"><span data-stu-id="41641-106">Recording information for a participant.</span></span>

## <a name="properties"></a><span data-ttu-id="41641-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41641-107">Properties</span></span>

| <span data-ttu-id="41641-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="41641-108">Property</span></span>       | <span data-ttu-id="41641-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="41641-109">Type</span></span>    | <span data-ttu-id="41641-110">Description</span><span class="sxs-lookup"><span data-stu-id="41641-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="41641-111">initiatedBy</span><span class="sxs-lookup"><span data-stu-id="41641-111">initiatedBy</span></span> | [<span data-ttu-id="41641-112">participantInfo</span><span class="sxs-lookup"><span data-stu-id="41641-112">participantInfo</span></span>](participantinfo.md) | <span data-ttu-id="41641-113">El participante que inició la grabación.</span><span class="sxs-lookup"><span data-stu-id="41641-113">The participant who initiated the recording.</span></span> |
| <span data-ttu-id="41641-114">status</span><span class="sxs-lookup"><span data-stu-id="41641-114">status</span></span> | <span data-ttu-id="41641-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="41641-115">String</span></span> | <span data-ttu-id="41641-116">Los valores posibles son: `recordingCapable`, `notRecording` y `startedRecording`.</span><span class="sxs-lookup"><span data-stu-id="41641-116">Possible values are: `recordingCapable`, `notRecording`, `startedRecording`.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="41641-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="41641-117">JSON representation</span></span>

<span data-ttu-id="41641-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="41641-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recordingInfo"
}-->
```json
{
  "initiatedBy": {"@odata.type": "#microsoft.graph.participantInfo"},
  "status": "recordingCapable | notRecording | startedRecording"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recordingInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
