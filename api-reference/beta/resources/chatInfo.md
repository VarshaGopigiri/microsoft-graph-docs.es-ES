---
title: tipo de recurso chatInfo
description: Información acerca de un mensaje en Microsoft Teams.
ms.openlocfilehash: d7e90cf2cdf5180f6483675d919b4e635a1cd5fa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083146"
---
# <a name="chatinfo-resource-type"></a><span data-ttu-id="998ab-103">tipo de recurso chatInfo</span><span class="sxs-lookup"><span data-stu-id="998ab-103">chatInfo resource type</span></span>

> <span data-ttu-id="998ab-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="998ab-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="998ab-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="998ab-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="998ab-106">Información acerca de un mensaje en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="998ab-106">Information about a message in Microsoft Teams.</span></span>

## <a name="properties"></a><span data-ttu-id="998ab-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="998ab-107">Properties</span></span>

| <span data-ttu-id="998ab-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="998ab-108">Property</span></span>            | <span data-ttu-id="998ab-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="998ab-109">Type</span></span>    | <span data-ttu-id="998ab-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="998ab-110">Description</span></span>|
|:--------------------|:--------|:-----------|
| <span data-ttu-id="998ab-111">messageId</span><span class="sxs-lookup"><span data-stu-id="998ab-111">messageId</span></span>           | <span data-ttu-id="998ab-112">String</span><span class="sxs-lookup"><span data-stu-id="998ab-112">String</span></span>  | <span data-ttu-id="998ab-113">El identificador único para un mensaje en un canal de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="998ab-113">The unique identifier for a message in a Microsoft Teams channel.</span></span> |
| <span data-ttu-id="998ab-114">replyChainMessageId</span><span class="sxs-lookup"><span data-stu-id="998ab-114">replyChainMessageId</span></span> | <span data-ttu-id="998ab-115">String</span><span class="sxs-lookup"><span data-stu-id="998ab-115">String</span></span>  | <span data-ttu-id="998ab-116">El identificador del mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="998ab-116">The ID of the reply message.</span></span> |
| <span data-ttu-id="998ab-117">threadId</span><span class="sxs-lookup"><span data-stu-id="998ab-117">threadId</span></span>            | <span data-ttu-id="998ab-118">String</span><span class="sxs-lookup"><span data-stu-id="998ab-118">String</span></span>  | <span data-ttu-id="998ab-119">El identificador único para un subproceso en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="998ab-119">The unique identifier for a thread in Microsoft Teams.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="998ab-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="998ab-120">JSON representation</span></span>

<span data-ttu-id="998ab-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="998ab-121">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chatInfo"
}-->
```json
{
  "messageId": "String",
  "replyChainMessageId": "String",
  "threadId": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chatInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
