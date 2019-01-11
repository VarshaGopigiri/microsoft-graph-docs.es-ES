---
title: tipo de recurso meetingParticipants
description: Participantes de una reunión.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: fad06a015429a7264d808b4997c94e90e4799825
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815123"
---
# <a name="meetingparticipants-resource-type"></a><span data-ttu-id="abef6-103">tipo de recurso meetingParticipants</span><span class="sxs-lookup"><span data-stu-id="abef6-103">meetingParticipants resource type</span></span>

> <span data-ttu-id="abef6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="abef6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="abef6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="abef6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="abef6-106">Participantes de una reunión.</span><span class="sxs-lookup"><span data-stu-id="abef6-106">Participants in a meeting.</span></span>

## <a name="properties"></a><span data-ttu-id="abef6-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abef6-107">Properties</span></span>

| <span data-ttu-id="abef6-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="abef6-108">Property</span></span>       | <span data-ttu-id="abef6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="abef6-109">Type</span></span>    | <span data-ttu-id="abef6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="abef6-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="abef6-111">attendees</span><span class="sxs-lookup"><span data-stu-id="abef6-111">attendees</span></span> | <span data-ttu-id="abef6-112">colección de [meetingParticipantInfo](meetingparticipantinfo.md)</span><span class="sxs-lookup"><span data-stu-id="abef6-112">[meetingParticipantInfo](meetingparticipantinfo.md) collection</span></span> |  |
| <span data-ttu-id="abef6-113">organizador</span><span class="sxs-lookup"><span data-stu-id="abef6-113">organizer</span></span> | [<span data-ttu-id="abef6-114">meetingParticipantInfo</span><span class="sxs-lookup"><span data-stu-id="abef6-114">meetingParticipantInfo</span></span>](meetingparticipantinfo.md) |  |

## <a name="json-representation"></a><span data-ttu-id="abef6-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="abef6-115">JSON representation</span></span>

<span data-ttu-id="abef6-116">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="abef6-116">The following is a JSON representation of the resource.</span></span>

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
