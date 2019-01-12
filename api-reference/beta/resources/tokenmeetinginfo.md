---
title: tipo de recurso tokenMeetingInfo
description: El tipo de tokenMeetingInfo.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 0d68b60cdfc1470bb1c1c3846c34dfc76c5c5a1b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919270"
---
# <a name="tokenmeetinginfo-resource-type"></a><span data-ttu-id="91860-103">tipo de recurso tokenMeetingInfo</span><span class="sxs-lookup"><span data-stu-id="91860-103">tokenMeetingInfo resource type</span></span>

> <span data-ttu-id="91860-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="91860-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="91860-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="91860-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="91860-106">El tipo de tokenMeetingInfo.</span><span class="sxs-lookup"><span data-stu-id="91860-106">The tokenMeetingInfo type.</span></span>

## <a name="properties"></a><span data-ttu-id="91860-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="91860-107">Properties</span></span>

| <span data-ttu-id="91860-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="91860-108">Property</span></span>                     | <span data-ttu-id="91860-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="91860-109">Type</span></span>    | <span data-ttu-id="91860-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="91860-110">Description</span></span>                                                                    |
| :--------------------------- | :------ | :----------------------------------------------------------------------------- |
| <span data-ttu-id="91860-111">allowConversationWithoutHost</span><span class="sxs-lookup"><span data-stu-id="91860-111">allowConversationWithoutHost</span></span> | <span data-ttu-id="91860-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="91860-112">Boolean</span></span> | <span data-ttu-id="91860-113">Indica si puede continuar una conversación una vez que abandona el host de la conversación.</span><span class="sxs-lookup"><span data-stu-id="91860-113">Indicates if a conversation can continue once the host of the conversation leaves.</span></span> |
| <span data-ttu-id="91860-114">token</span><span class="sxs-lookup"><span data-stu-id="91860-114">token</span></span>                        | <span data-ttu-id="91860-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="91860-115">String</span></span>  | <span data-ttu-id="91860-116">El token de combinación o activar la reunión.</span><span class="sxs-lookup"><span data-stu-id="91860-116">The token to join/activate the meeting.</span></span>                                        |

## <a name="json-representation"></a><span data-ttu-id="91860-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="91860-117">JSON representation</span></span>

<span data-ttu-id="91860-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="91860-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.tokenMeetingInfo"
}-->
```json
{
  "allowConversationWithoutHost": true,
  "token": "String"
}
```

## <a name="example"></a><span data-ttu-id="91860-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="91860-119">Example</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.tokenMeetingInfo"
}-->
```json
{
  "allowConversationWithoutHost": true,
  "token": "ABCD123"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "tokenMeetingInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
