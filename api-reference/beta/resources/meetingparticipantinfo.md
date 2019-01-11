---
title: tipo de recurso meetingParticipantInfo
description: Información acerca de un participante en una reunión.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: d7b5ae17bd3bfb566bce0da9814b86aab98173da
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834261"
---
# <a name="meetingparticipantinfo-resource-type"></a><span data-ttu-id="a218d-103">tipo de recurso meetingParticipantInfo</span><span class="sxs-lookup"><span data-stu-id="a218d-103">meetingParticipantInfo resource type</span></span>

> <span data-ttu-id="a218d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a218d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a218d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a218d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a218d-106">Información acerca de un participante en una reunión.</span><span class="sxs-lookup"><span data-stu-id="a218d-106">Information about a participant in a meeting.</span></span>

## <a name="properties"></a><span data-ttu-id="a218d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a218d-107">Properties</span></span>

| <span data-ttu-id="a218d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a218d-108">Property</span></span>       | <span data-ttu-id="a218d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a218d-109">Type</span></span>                          | <span data-ttu-id="a218d-110">Description</span><span class="sxs-lookup"><span data-stu-id="a218d-110">Description</span></span>                              |
|:---------------|:------------------------------|:-----------------------------------------|
| <span data-ttu-id="a218d-111">identity</span><span class="sxs-lookup"><span data-stu-id="a218d-111">identity</span></span>       | [<span data-ttu-id="a218d-112">identitySet</span><span class="sxs-lookup"><span data-stu-id="a218d-112">identitySet</span></span>](identityset.md) | <span data-ttu-id="a218d-113">Información de identidad del participante.</span><span class="sxs-lookup"><span data-stu-id="a218d-113">Identity information of the participant.</span></span> |
| <span data-ttu-id="a218d-114">UPN</span><span class="sxs-lookup"><span data-stu-id="a218d-114">upn</span></span>            | <span data-ttu-id="a218d-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="a218d-115">String</span></span>                        | <span data-ttu-id="a218d-116">Nombre principal de usuario del participante.</span><span class="sxs-lookup"><span data-stu-id="a218d-116">User principal name of the participant.</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="a218d-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a218d-117">JSON representation</span></span>

<span data-ttu-id="a218d-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a218d-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingParticipantInfo"
}-->
```json
{
  "identity": {"@odata.type": "#microsoft.graph.identitySet"},
  "upn": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingParticipantInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
