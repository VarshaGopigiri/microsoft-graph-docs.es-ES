---
title: tipo de recurso automaticRepliesMailTips
description: Sugerencias de correo electrónico acerca de las respuestas automáticas que se han configurado en un buzón de correo.
ms.openlocfilehash: 51657578474710d40cfc3feabdf41e50e7105942
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090892"
---
# <a name="automaticrepliesmailtips-resource-type"></a><span data-ttu-id="08f7d-103">tipo de recurso automaticRepliesMailTips</span><span class="sxs-lookup"><span data-stu-id="08f7d-103">automaticRepliesMailTips resource type</span></span>

> <span data-ttu-id="08f7d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="08f7d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="08f7d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="08f7d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="08f7d-106">[Sugerencias de correo electrónico](../resources/mailtips.md) acerca de las respuestas automáticas que se han configurado en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="08f7d-106">[MailTips](../resources/mailtips.md) about any automatic replies that have been set up on a mailbox.</span></span>

## <a name="properties"></a><span data-ttu-id="08f7d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="08f7d-107">Properties</span></span>
| <span data-ttu-id="08f7d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="08f7d-108">Property</span></span>     | <span data-ttu-id="08f7d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="08f7d-109">Type</span></span>   |<span data-ttu-id="08f7d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="08f7d-110">Description</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="08f7d-111">message</span><span class="sxs-lookup"><span data-stu-id="08f7d-111">message</span></span> | <span data-ttu-id="08f7d-112">String</span><span class="sxs-lookup"><span data-stu-id="08f7d-112">String</span></span> | <span data-ttu-id="08f7d-113">El mensaje de respuesta automática.</span><span class="sxs-lookup"><span data-stu-id="08f7d-113">The automatic reply message.</span></span> |
| <span data-ttu-id="08f7d-114">messageLanguage</span><span class="sxs-lookup"><span data-stu-id="08f7d-114">messageLanguage</span></span> | [<span data-ttu-id="08f7d-115">localeInfo</span><span class="sxs-lookup"><span data-stu-id="08f7d-115">localeInfo</span></span>](../resources/localeinfo.md) | <span data-ttu-id="08f7d-116">El idioma que se encuentra el mensaje de respuesta automática en.</span><span class="sxs-lookup"><span data-stu-id="08f7d-116">The language that the automatic reply message is in.</span></span> |
| <span data-ttu-id="08f7d-117">scheduledEndTime</span><span class="sxs-lookup"><span data-stu-id="08f7d-117">scheduledEndTime</span></span> | [<span data-ttu-id="08f7d-118">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="08f7d-118">dateTimeTimeZone</span></span>](../resources/datetimetimezone.md) | <span data-ttu-id="08f7d-119">La fecha y hora en que se establecen las respuestas automáticas para finalizar.</span><span class="sxs-lookup"><span data-stu-id="08f7d-119">The date and time that automatic replies are set to end.</span></span> |
| <span data-ttu-id="08f7d-120">scheduledStartTime</span><span class="sxs-lookup"><span data-stu-id="08f7d-120">scheduledStartTime</span></span> | [<span data-ttu-id="08f7d-121">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="08f7d-121">dateTimeTimeZone</span></span>](../resources/datetimetimezone.md) | <span data-ttu-id="08f7d-122">La fecha y hora en que se establecen las respuestas automáticas para empezar.</span><span class="sxs-lookup"><span data-stu-id="08f7d-122">The date and time that automatic replies are set to begin.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="08f7d-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="08f7d-123">JSON representation</span></span>

<span data-ttu-id="08f7d-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="08f7d-124">Here is a JSON representation of the resource.</span></span>

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