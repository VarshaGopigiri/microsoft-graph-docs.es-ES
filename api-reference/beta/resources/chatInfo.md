---
title: tipo de recurso chatInfo
description: Información acerca de un mensaje en Microsoft Teams.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: c2cc0dd288abdab7852017600c4c55b9a40b0aa7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852944"
---
# <a name="chatinfo-resource-type"></a><span data-ttu-id="cf38a-103">tipo de recurso chatInfo</span><span class="sxs-lookup"><span data-stu-id="cf38a-103">chatInfo resource type</span></span>

> <span data-ttu-id="cf38a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cf38a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cf38a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cf38a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cf38a-106">Información acerca de un mensaje en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cf38a-106">Information about a message in Microsoft Teams.</span></span>

## <a name="properties"></a><span data-ttu-id="cf38a-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf38a-107">Properties</span></span>

| <span data-ttu-id="cf38a-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf38a-108">Property</span></span>            | <span data-ttu-id="cf38a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf38a-109">Type</span></span>    | <span data-ttu-id="cf38a-110">Description</span><span class="sxs-lookup"><span data-stu-id="cf38a-110">Description</span></span>|
|:--------------------|:--------|:-----------|
| <span data-ttu-id="cf38a-111">messageId</span><span class="sxs-lookup"><span data-stu-id="cf38a-111">messageId</span></span>           | <span data-ttu-id="cf38a-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf38a-112">String</span></span>  | <span data-ttu-id="cf38a-113">El identificador único para un mensaje en un canal de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cf38a-113">The unique identifier for a message in a Microsoft Teams channel.</span></span> |
| <span data-ttu-id="cf38a-114">replyChainMessageId</span><span class="sxs-lookup"><span data-stu-id="cf38a-114">replyChainMessageId</span></span> | <span data-ttu-id="cf38a-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf38a-115">String</span></span>  | <span data-ttu-id="cf38a-116">El identificador del mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf38a-116">The ID of the reply message.</span></span> |
| <span data-ttu-id="cf38a-117">threadId</span><span class="sxs-lookup"><span data-stu-id="cf38a-117">threadId</span></span>            | <span data-ttu-id="cf38a-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf38a-118">String</span></span>  | <span data-ttu-id="cf38a-119">El identificador único para un subproceso en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cf38a-119">The unique identifier for a thread in Microsoft Teams.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="cf38a-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cf38a-120">JSON representation</span></span>

<span data-ttu-id="cf38a-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="cf38a-121">The following is a JSON representation of the resource.</span></span>

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
