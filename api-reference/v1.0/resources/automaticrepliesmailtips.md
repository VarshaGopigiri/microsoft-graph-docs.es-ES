---
title: tipo de recurso automaticRepliesMailTips
description: Sugerencias de correo electrónico acerca de las respuestas automáticas que se han configurado en un buzón de correo.
localization_priority: Normal
ms.openlocfilehash: bb477979b975996f70e4b8ac624befab7f254f46
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816278"
---
# <a name="automaticrepliesmailtips-resource-type"></a><span data-ttu-id="82986-103">tipo de recurso automaticRepliesMailTips</span><span class="sxs-lookup"><span data-stu-id="82986-103">automaticRepliesMailTips resource type</span></span>


<span data-ttu-id="82986-104">[Sugerencias de correo electrónico](../resources/mailtips.md) acerca de las respuestas automáticas que se han configurado en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="82986-104">[MailTips](../resources/mailtips.md) about any automatic replies that have been set up on a mailbox.</span></span>

## <a name="properties"></a><span data-ttu-id="82986-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="82986-105">Properties</span></span>
| <span data-ttu-id="82986-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82986-106">Property</span></span>     | <span data-ttu-id="82986-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="82986-107">Type</span></span>   |<span data-ttu-id="82986-108">Description</span><span class="sxs-lookup"><span data-stu-id="82986-108">Description</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="82986-109">message</span><span class="sxs-lookup"><span data-stu-id="82986-109">message</span></span> | <span data-ttu-id="82986-110">String</span><span class="sxs-lookup"><span data-stu-id="82986-110">String</span></span> | <span data-ttu-id="82986-111">El mensaje de respuesta automática.</span><span class="sxs-lookup"><span data-stu-id="82986-111">The automatic reply message.</span></span> |
| <span data-ttu-id="82986-112">messageLanguage</span><span class="sxs-lookup"><span data-stu-id="82986-112">messageLanguage</span></span> | [<span data-ttu-id="82986-113">localeInfo</span><span class="sxs-lookup"><span data-stu-id="82986-113">localeInfo</span></span>](../resources/localeinfo.md) | <span data-ttu-id="82986-114">El idioma que se encuentra el mensaje de respuesta automática en.</span><span class="sxs-lookup"><span data-stu-id="82986-114">The language that the automatic reply message is in.</span></span> |
| <span data-ttu-id="82986-115">scheduledEndTime</span><span class="sxs-lookup"><span data-stu-id="82986-115">scheduledEndTime</span></span> | [<span data-ttu-id="82986-116">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="82986-116">dateTimeTimeZone</span></span>](../resources/datetimetimezone.md) | <span data-ttu-id="82986-117">La fecha y hora en que se establecen las respuestas automáticas para finalizar.</span><span class="sxs-lookup"><span data-stu-id="82986-117">The date and time that automatic replies are set to end.</span></span> |
| <span data-ttu-id="82986-118">scheduledStartTime</span><span class="sxs-lookup"><span data-stu-id="82986-118">scheduledStartTime</span></span> | [<span data-ttu-id="82986-119">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="82986-119">dateTimeTimeZone</span></span>](../resources/datetimetimezone.md) | <span data-ttu-id="82986-120">La fecha y hora en que se establecen las respuestas automáticas para empezar.</span><span class="sxs-lookup"><span data-stu-id="82986-120">The date and time that automatic replies are set to begin.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="82986-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="82986-121">JSON representation</span></span>

<span data-ttu-id="82986-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="82986-122">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "messageLanguage",
    "scheduledEndTime",
    "scheduledStartTime"
  ],
  "@odata.type": "microsoft.graph.automaticRepliesMailTips"
}-->

```json
{
  "message": "string",
  "messageLanguage": {"@odata.type": "microsoft.graph.localeInfo"},
  "scheduledEndTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "scheduledStartTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "automaticRepliesMailTips resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
