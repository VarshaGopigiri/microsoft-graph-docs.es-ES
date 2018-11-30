---
title: tipo de recurso recordingInfo
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 92af3fcb52ab08f3f25a2c16cc720a4053a9bdfa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086466"
---
# <a name="recordinginfo-resource-type"></a><span data-ttu-id="dd658-103">tipo de recurso recordingInfo</span><span class="sxs-lookup"><span data-stu-id="dd658-103">recordingInfo resource type</span></span>

> <span data-ttu-id="dd658-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dd658-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dd658-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dd658-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="properties"></a><span data-ttu-id="dd658-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd658-106">Properties</span></span>

| <span data-ttu-id="dd658-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dd658-107">Property</span></span>       | <span data-ttu-id="dd658-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd658-108">Type</span></span>    | <span data-ttu-id="dd658-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd658-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="dd658-110">initiatedBy</span><span class="sxs-lookup"><span data-stu-id="dd658-110">initiatedBy</span></span> | [<span data-ttu-id="dd658-111">participantInfo</span><span class="sxs-lookup"><span data-stu-id="dd658-111">participantInfo</span></span>](participantinfo.md) | <span data-ttu-id="dd658-112">El participante que inició la grabación.</span><span class="sxs-lookup"><span data-stu-id="dd658-112">The participant who initiated the recording.</span></span> |
| <span data-ttu-id="dd658-113">status</span><span class="sxs-lookup"><span data-stu-id="dd658-113">status</span></span> | <span data-ttu-id="dd658-114">String</span><span class="sxs-lookup"><span data-stu-id="dd658-114">String</span></span> | <span data-ttu-id="dd658-115">Los valores posibles son: `recordingCapable`, `notRecording` y `startedRecording`.</span><span class="sxs-lookup"><span data-stu-id="dd658-115">Possible values are: `recordingCapable`, `notRecording`, `startedRecording`.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="dd658-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dd658-116">JSON representation</span></span>

<span data-ttu-id="dd658-117">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="dd658-117">The following is a JSON representation of the resource.</span></span>

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
