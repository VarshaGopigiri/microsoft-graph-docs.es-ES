---
title: tipo de recurso chatMessageReaction
description: 'Representa una reacción a una entidad de chatMessage. '
ms.openlocfilehash: 1ad1f7948405a8891ec9aa13065b71108e9c47c5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090853"
---
# <a name="chatmessagereaction-resource-type"></a><span data-ttu-id="ac09f-103">tipo de recurso chatMessageReaction</span><span class="sxs-lookup"><span data-stu-id="ac09f-103">chatMessageReaction resource type</span></span>

<span data-ttu-id="ac09f-104">Representa una reacción a una entidad de [chatMessage](chatmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="ac09f-104">Represents a reaction to a [chatMessage](chatmessage.md) entity.</span></span> 

<span data-ttu-id="ac09f-105">Una entidad de tipo `chatMessageReaction` se devuelve como parte de los [mensajes del canal de obtener](../api/channel-get-message.md) API, como parte de la entidad [chatMessage](chatmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="ac09f-105">An entity of type `chatMessageReaction` is returned as part of the [Get channel messages](../api/channel-get-message.md) API, as a part of [chatMessage](chatmessage.md) entity.</span></span>

## <a name="properties"></a><span data-ttu-id="ac09f-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ac09f-106">Properties</span></span>
| <span data-ttu-id="ac09f-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac09f-107">Property</span></span>     | <span data-ttu-id="ac09f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac09f-108">Type</span></span>   |<span data-ttu-id="ac09f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac09f-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ac09f-110">reactionType</span><span class="sxs-lookup"><span data-stu-id="ac09f-110">reactionType</span></span>|<span data-ttu-id="ac09f-111">string</span><span class="sxs-lookup"><span data-stu-id="ac09f-111">string</span></span>| <span data-ttu-id="ac09f-112">El tipo de reacción.</span><span class="sxs-lookup"><span data-stu-id="ac09f-112">The type of reaction.</span></span> <span data-ttu-id="ac09f-113">Los valores planeados incluyen:</span><span class="sxs-lookup"><span data-stu-id="ac09f-113">Planned values include:</span></span> <br><ul><li><span data-ttu-id="ac09f-114">Al igual que - como un mensaje, contenido está en blanco en este caso.</span><span class="sxs-lookup"><span data-stu-id="ac09f-114">Like - Like a message, content is blank in this case.</span></span></li><li><span data-ttu-id="ac09f-115">Emoji - Emoji reacción.</span><span class="sxs-lookup"><span data-stu-id="ac09f-115">Emoji - Emoji reaction.</span></span> <span data-ttu-id="ac09f-116">Contenido se establece en el valor de la emoji unicode.</span><span class="sxs-lookup"><span data-stu-id="ac09f-116">Content is set to unicode value of the emoji.</span></span></li><li><span data-ttu-id="ac09f-117">Etiqueta - contenido está establecido en la cadena de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="ac09f-117">Label - Content is set to the string in the label.</span></span></li></ul>|
|<span data-ttu-id="ac09f-118">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ac09f-118">createdDateTime</span></span>|<span data-ttu-id="ac09f-119">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ac09f-119">dateTimeOffset</span></span>|<span data-ttu-id="ac09f-120">Marca de tiempo UTC del mensaje raíz en formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="ac09f-120">UTC timestamp of the root message in ISO-8601 format.</span></span>|
|<span data-ttu-id="ac09f-121">usuario</span><span class="sxs-lookup"><span data-stu-id="ac09f-121">user</span></span>|<span data-ttu-id="ac09f-122">identitySet</span><span class="sxs-lookup"><span data-stu-id="ac09f-122">identitySet</span></span>|<span data-ttu-id="ac09f-123">El usuario que reacciona al mensaje.</span><span class="sxs-lookup"><span data-stu-id="ac09f-123">The user who reacted to the message.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ac09f-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ac09f-124">JSON representation</span></span>

<span data-ttu-id="ac09f-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ac09f-125">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "content"
  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.chatMessageReaction"
}-->

```json
{
  "reactionType": "string ",
  "createdDateTime": "string (timestamp)",
  "user": {"@odata.type": "microsoft.graph.identitySet"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chat message reaction resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
