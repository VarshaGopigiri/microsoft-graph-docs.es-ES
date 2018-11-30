---
title: tipo de recurso meetingParticipantInfo
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 1d9c22924f8f05255b5e01bad4bbcd6ae5957ffe
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086810"
---
# <a name="meetingparticipantinfo-resource-type"></a><span data-ttu-id="63239-103">tipo de recurso meetingParticipantInfo</span><span class="sxs-lookup"><span data-stu-id="63239-103">meetingParticipantInfo resource type</span></span>

> <span data-ttu-id="63239-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="63239-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="63239-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="63239-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="properties"></a><span data-ttu-id="63239-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63239-106">Properties</span></span>

| <span data-ttu-id="63239-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63239-107">Property</span></span>       | <span data-ttu-id="63239-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="63239-108">Type</span></span>                          | <span data-ttu-id="63239-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="63239-109">Description</span></span>                              |
|:---------------|:------------------------------|:-----------------------------------------|
| <span data-ttu-id="63239-110">identity</span><span class="sxs-lookup"><span data-stu-id="63239-110">identity</span></span>       | [<span data-ttu-id="63239-111">identitySet</span><span class="sxs-lookup"><span data-stu-id="63239-111">identitySet</span></span>](identityset.md) | <span data-ttu-id="63239-112">Información de identidad del participante.</span><span class="sxs-lookup"><span data-stu-id="63239-112">Identity information of the participant.</span></span> |
| <span data-ttu-id="63239-113">UPN</span><span class="sxs-lookup"><span data-stu-id="63239-113">upn</span></span>            | <span data-ttu-id="63239-114">String</span><span class="sxs-lookup"><span data-stu-id="63239-114">String</span></span>                        | <span data-ttu-id="63239-115">Nombre principal de usuario del participante.</span><span class="sxs-lookup"><span data-stu-id="63239-115">User principal name of the participant.</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="63239-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="63239-116">JSON representation</span></span>

<span data-ttu-id="63239-117">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="63239-117">The following is a JSON representation of the resource.</span></span>

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
