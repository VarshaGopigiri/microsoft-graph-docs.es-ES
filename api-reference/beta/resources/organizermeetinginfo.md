---
title: tipo de recurso organizerMeetingInfo
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 00a7978c44c82ddd6b34802f29188a554e7e0b4f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087014"
---
# <a name="organizermeetinginfo-resource-type"></a><span data-ttu-id="af271-103">tipo de recurso organizerMeetingInfo</span><span class="sxs-lookup"><span data-stu-id="af271-103">organizerMeetingInfo resource type</span></span>

> <span data-ttu-id="af271-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="af271-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="af271-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="af271-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="properties"></a><span data-ttu-id="af271-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="af271-106">Properties</span></span>

| <span data-ttu-id="af271-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="af271-107">Property</span></span>                     | <span data-ttu-id="af271-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="af271-108">Type</span></span>                          | <span data-ttu-id="af271-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="af271-109">Description</span></span>                                     |
| :--------------------------- | :---------------------------- | :-----------------------------------------------|
| <span data-ttu-id="af271-110">allowConversationWithoutHost</span><span class="sxs-lookup"><span data-stu-id="af271-110">allowConversationWithoutHost</span></span> | <span data-ttu-id="af271-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="af271-111">Boolean</span></span>                       | <span data-ttu-id="af271-112">Indica si puede continuar una conversación una vez que abandona el host de la conversación.</span><span class="sxs-lookup"><span data-stu-id="af271-112">Indicates if a conversation can continue once the host of the conversation leaves.</span></span> |
| <span data-ttu-id="af271-113">organizador</span><span class="sxs-lookup"><span data-stu-id="af271-113">organizer</span></span>                    | [<span data-ttu-id="af271-114">identitySet</span><span class="sxs-lookup"><span data-stu-id="af271-114">identitySet</span></span>](identityset.md) | <span data-ttu-id="af271-115">El organizador de la identidad de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="af271-115">The organizer Azure Active Directory identity.</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="af271-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="af271-116">JSON representation</span></span>

<span data-ttu-id="af271-117">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="af271-117">The following is a JSON representation of the resource.</span></span>

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

## <a name="example"></a><span data-ttu-id="af271-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="af271-118">Example</span></span>

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
