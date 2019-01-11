---
title: Tipo de recurso attendeeBase
description: El tipo de asistente.
localization_priority: Normal
ms.openlocfilehash: b30e054e6d89765d280340b31355403739381c2a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844985"
---
# <a name="attendeebase-resource-type"></a><span data-ttu-id="ac969-103">Tipo de recurso attendeeBase</span><span class="sxs-lookup"><span data-stu-id="ac969-103">attendeeBase resource type</span></span>

> <span data-ttu-id="ac969-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ac969-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ac969-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ac969-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ac969-106">El tipo de asistente.</span><span class="sxs-lookup"><span data-stu-id="ac969-106">The type of attendee.</span></span>

<span data-ttu-id="ac969-107">Derivado de [destinatario](recipient.md).</span><span class="sxs-lookup"><span data-stu-id="ac969-107">Derived from [recipient](recipient.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="ac969-108">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ac969-108">JSON representation</span></span>

<span data-ttu-id="ac969-109">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ac969-109">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
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
## <a name="properties"></a><span data-ttu-id="ac969-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ac969-110">Properties</span></span>
| <span data-ttu-id="ac969-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac969-111">Property</span></span>     | <span data-ttu-id="ac969-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac969-112">Type</span></span>   |<span data-ttu-id="ac969-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac969-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ac969-114">type</span><span class="sxs-lookup"><span data-stu-id="ac969-114">type</span></span>|<span data-ttu-id="ac969-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac969-115">String</span></span>| <span data-ttu-id="ac969-p102">El tipo de asistente. Los valores posibles son: `required`, `optional`, `resource`. Actualmente, si el asistente es una persona, [findMeetingTimes](../api/user-findmeetingtimes.md) siempre la considera del tipo `Required`.</span><span class="sxs-lookup"><span data-stu-id="ac969-p102">The type of attendee. Possible values are: `required`, `optional`, `resource`. Currently if the attendee is a person, [findMeetingTimes](../api/user-findmeetingtimes.md) always considers the person is of the `Required` type.</span></span>|
|<span data-ttu-id="ac969-119">emailAddress</span><span class="sxs-lookup"><span data-stu-id="ac969-119">emailAddress</span></span>|[<span data-ttu-id="ac969-120">emailAddress</span><span class="sxs-lookup"><span data-stu-id="ac969-120">emailAddress</span></span>](emailaddress.md)|<span data-ttu-id="ac969-121">Incluye el nombre y la dirección de SMTP del asistente.</span><span class="sxs-lookup"><span data-stu-id="ac969-121">Includes the name and SMTP address of the attendee.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendeeBase resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
