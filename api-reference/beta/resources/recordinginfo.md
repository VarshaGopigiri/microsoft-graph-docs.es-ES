---
title: tipo de recurso recordingInfo
description: Información de grabación de un participante.
author: VinodRavichandran
ms.openlocfilehash: 709edcc6d473ce610cbba7f628e4ebc5057b779c
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380306"
---
# <a name="recordinginfo-resource-type"></a><span data-ttu-id="6940c-103">tipo de recurso recordingInfo</span><span class="sxs-lookup"><span data-stu-id="6940c-103">recordingInfo resource type</span></span>

> <span data-ttu-id="6940c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6940c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6940c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6940c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6940c-106">Información de grabación de un participante.</span><span class="sxs-lookup"><span data-stu-id="6940c-106">Recording information for a participant.</span></span>

## <a name="properties"></a><span data-ttu-id="6940c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6940c-107">Properties</span></span>

| <span data-ttu-id="6940c-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6940c-108">Property</span></span>       | <span data-ttu-id="6940c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6940c-109">Type</span></span>    | <span data-ttu-id="6940c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6940c-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6940c-111">initiatedBy</span><span class="sxs-lookup"><span data-stu-id="6940c-111">initiatedBy</span></span> | [<span data-ttu-id="6940c-112">participantInfo</span><span class="sxs-lookup"><span data-stu-id="6940c-112">participantInfo</span></span>](participantinfo.md) | <span data-ttu-id="6940c-113">El participante que inició la grabación.</span><span class="sxs-lookup"><span data-stu-id="6940c-113">The participant who initiated the recording.</span></span> |
| <span data-ttu-id="6940c-114">status</span><span class="sxs-lookup"><span data-stu-id="6940c-114">status</span></span> | <span data-ttu-id="6940c-115">String</span><span class="sxs-lookup"><span data-stu-id="6940c-115">String</span></span> | <span data-ttu-id="6940c-116">Los valores posibles son: `recordingCapable`, `notRecording` y `startedRecording`.</span><span class="sxs-lookup"><span data-stu-id="6940c-116">Possible values are: `recordingCapable`, `notRecording`, `startedRecording`.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="6940c-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6940c-117">JSON representation</span></span>

<span data-ttu-id="6940c-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6940c-118">The following is a JSON representation of the resource.</span></span>

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
