---
title: Tipo de recurso attendeeBase
description: El tipo de asistente.
ms.openlocfilehash: 6995ac94a600a60313ef26208b441c6ef6fdf001
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031216"
---
# <a name="attendeebase-resource-type"></a><span data-ttu-id="a3855-103">Tipo de recurso attendeeBase</span><span class="sxs-lookup"><span data-stu-id="a3855-103">attendeeBase resource type</span></span>

<span data-ttu-id="a3855-104">El tipo de asistente.</span><span class="sxs-lookup"><span data-stu-id="a3855-104">The type of attendee.</span></span>

<span data-ttu-id="a3855-105">Derivado de [destinatario](recipient.md).</span><span class="sxs-lookup"><span data-stu-id="a3855-105">Derived from [recipient](recipient.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="a3855-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a3855-106">JSON representation</span></span>

<span data-ttu-id="a3855-107">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a3855-107">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.recipient",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attendeeBase"
}-->

```json
{
  "type": "String",
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```
## <a name="properties"></a><span data-ttu-id="a3855-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a3855-108">Properties</span></span>
| <span data-ttu-id="a3855-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a3855-109">Property</span></span>     | <span data-ttu-id="a3855-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a3855-110">Type</span></span>   |<span data-ttu-id="a3855-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3855-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a3855-112">type</span><span class="sxs-lookup"><span data-stu-id="a3855-112">type</span></span>|<span data-ttu-id="a3855-113">attendeeType</span><span class="sxs-lookup"><span data-stu-id="a3855-113">attendeeType</span></span>| <span data-ttu-id="a3855-114">El tipo de asistente.</span><span class="sxs-lookup"><span data-stu-id="a3855-114">The type of attendee.</span></span> <span data-ttu-id="a3855-115">Los valores posibles son: `required`, `optional`, `resource`.</span><span class="sxs-lookup"><span data-stu-id="a3855-115">The possible values are: `required`, `optional`, `resource`.</span></span> <span data-ttu-id="a3855-116">Actualmente si el asistente es una persona, [findMeetingTimes](../api/user-findmeetingtimes.md) siempre considera que es la persona de la `Required` tipo.</span><span class="sxs-lookup"><span data-stu-id="a3855-116">Currently if the attendee is a person, [findMeetingTimes](../api/user-findmeetingtimes.md) always considers the person is of the `Required` type.</span></span>|
|<span data-ttu-id="a3855-117">emailAddress</span><span class="sxs-lookup"><span data-stu-id="a3855-117">emailAddress</span></span>|[<span data-ttu-id="a3855-118">emailAddress</span><span class="sxs-lookup"><span data-stu-id="a3855-118">emailAddress</span></span>](emailaddress.md)|<span data-ttu-id="a3855-119">Incluye el nombre y la dirección de SMTP del asistente.</span><span class="sxs-lookup"><span data-stu-id="a3855-119">Includes the name and SMTP address of the attendee.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendeeBase resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
