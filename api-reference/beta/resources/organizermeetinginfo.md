---
title: tipo de recurso organizerMeetingInfo
description: Información de la reunión que contiene el organizador de la reunión.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 66a08b30741d488edf2d514568a17f292e588c23
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957707"
---
# <a name="organizermeetinginfo-resource-type"></a><span data-ttu-id="4c246-103">tipo de recurso organizerMeetingInfo</span><span class="sxs-lookup"><span data-stu-id="4c246-103">organizerMeetingInfo resource type</span></span>

> <span data-ttu-id="4c246-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4c246-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4c246-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4c246-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4c246-106">Información de la reunión que contiene el organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="4c246-106">Meeting information containing the organizer of the meeting.</span></span>

## <a name="properties"></a><span data-ttu-id="4c246-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4c246-107">Properties</span></span>

| <span data-ttu-id="4c246-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4c246-108">Property</span></span>                     | <span data-ttu-id="4c246-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c246-109">Type</span></span>                          | <span data-ttu-id="4c246-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c246-110">Description</span></span>                                     |
| :--------------------------- | :---------------------------- | :-----------------------------------------------|
| <span data-ttu-id="4c246-111">allowConversationWithoutHost</span><span class="sxs-lookup"><span data-stu-id="4c246-111">allowConversationWithoutHost</span></span> | <span data-ttu-id="4c246-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="4c246-112">Boolean</span></span>                       | <span data-ttu-id="4c246-113">Indica si puede continuar una conversación una vez que abandona el host de la conversación.</span><span class="sxs-lookup"><span data-stu-id="4c246-113">Indicates if a conversation can continue once the host of the conversation leaves.</span></span> |
| <span data-ttu-id="4c246-114">organizador</span><span class="sxs-lookup"><span data-stu-id="4c246-114">organizer</span></span>                    | [<span data-ttu-id="4c246-115">identitySet</span><span class="sxs-lookup"><span data-stu-id="4c246-115">identitySet</span></span>](identityset.md) | <span data-ttu-id="4c246-116">El organizador de la identidad de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4c246-116">The organizer Azure Active Directory identity.</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="4c246-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4c246-117">JSON representation</span></span>

<span data-ttu-id="4c246-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4c246-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.organizerMeetingInfo"
}-->
```json
{
  "allowConversationWithoutHost": true,
  "organizer": { "@odata.type": "#microsoft.graph.identitySet" }
}
```

## <a name="example"></a><span data-ttu-id="4c246-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c246-119">Example</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.organizerMeetingInfo"
}-->
```json
{
  "allowConversationWithoutHost": true,
  "organizer": {
    "user": {
      "id": "90ED37DC-D8E3-4E11-9DE3-30A955DDA06F",
      "tenantId": "49BFC225-8482-4AB8-94E7-76B48FDB9849"
    }
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "organizerMeetingInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
