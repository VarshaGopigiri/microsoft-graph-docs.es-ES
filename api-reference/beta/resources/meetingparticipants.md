---
title: tipo de recurso meetingParticipants
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 4f91c9198018e903eccff7e8fe07d6668d9fd2c9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090716"
---
# <a name="meetingparticipants-resource-type"></a><span data-ttu-id="30c06-103">tipo de recurso meetingParticipants</span><span class="sxs-lookup"><span data-stu-id="30c06-103">meetingParticipants resource type</span></span>

> <span data-ttu-id="30c06-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="30c06-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="30c06-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="30c06-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="properties"></a><span data-ttu-id="30c06-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="30c06-106">Properties</span></span>

| <span data-ttu-id="30c06-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="30c06-107">Property</span></span>       | <span data-ttu-id="30c06-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="30c06-108">Type</span></span>    | <span data-ttu-id="30c06-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="30c06-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="30c06-110">attendees</span><span class="sxs-lookup"><span data-stu-id="30c06-110">attendees</span></span> | <span data-ttu-id="30c06-111">colección de [meetingParticipantInfo](meetingparticipantinfo.md)</span><span class="sxs-lookup"><span data-stu-id="30c06-111">[meetingParticipantInfo](meetingparticipantinfo.md) collection</span></span> |  |
| <span data-ttu-id="30c06-112">organizador</span><span class="sxs-lookup"><span data-stu-id="30c06-112">organizer</span></span> | [<span data-ttu-id="30c06-113">meetingParticipantInfo</span><span class="sxs-lookup"><span data-stu-id="30c06-113">meetingParticipantInfo</span></span>](meetingparticipantinfo.md) |  |

## <a name="json-representation"></a><span data-ttu-id="30c06-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="30c06-114">JSON representation</span></span>

<span data-ttu-id="30c06-115">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="30c06-115">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingParticipants"
}-->
```json
{
  "attendees": [{"@odata.type": "#microsoft.graph.meetingParticipantInfo"}],
  "organizer": {"@odata.type": "#microsoft.graph.meetingParticipantInfo"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingParticipants resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
