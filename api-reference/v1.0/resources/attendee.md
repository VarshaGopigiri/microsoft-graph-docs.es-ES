---
title: Tipo de recurso attendee
description: Asistente a un evento. Esto puede ser una persona o un recurso, como una sala de reuniones o equipamiento que se ha configurado como un recurso en el servidor Exchange del espacio empresarial.
localization_priority: Normal
ms.openlocfilehash: 89c289a342bb0b761bed982f88d0f47470eaa237
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856542"
---
# <a name="attendee-resource-type"></a><span data-ttu-id="3eb35-104">Tipo de recurso attendee</span><span class="sxs-lookup"><span data-stu-id="3eb35-104">attendee resource type</span></span>

<span data-ttu-id="3eb35-105">Asistente a un evento.</span><span class="sxs-lookup"><span data-stu-id="3eb35-105">An event attendee.</span></span> <span data-ttu-id="3eb35-106">Esto puede ser una persona o un recurso, como una sala de reuniones o equipamiento que se ha configurado como un recurso en el servidor Exchange del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="3eb35-106">This can be a person or resource such as a meeting room or equipment, that has been set up as a resource on the Exchange server for the tenant.</span></span>

<span data-ttu-id="3eb35-107">Derivadas de [attendeeBase](attendeebase.md).</span><span class="sxs-lookup"><span data-stu-id="3eb35-107">Derived from [attendeeBase](attendeebase.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3eb35-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3eb35-108">Properties</span></span>
| <span data-ttu-id="3eb35-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3eb35-109">Property</span></span>     | <span data-ttu-id="3eb35-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="3eb35-110">Type</span></span>   |<span data-ttu-id="3eb35-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3eb35-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3eb35-112">status</span><span class="sxs-lookup"><span data-stu-id="3eb35-112">status</span></span>|[<span data-ttu-id="3eb35-113">ResponseStatus</span><span class="sxs-lookup"><span data-stu-id="3eb35-113">ResponseStatus</span></span>](responsestatus.md)|<span data-ttu-id="3eb35-114">Respuesta del asistente (ninguna, aceptada, rechazada, etc.) para el evento y fecha y hora en que se envió la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3eb35-114">The attendee's response (none, accepted, declined, etc.) for the event and date-time that the response was sent.</span></span>|
|<span data-ttu-id="3eb35-115">type</span><span class="sxs-lookup"><span data-stu-id="3eb35-115">type</span></span>|<span data-ttu-id="3eb35-116">String</span><span class="sxs-lookup"><span data-stu-id="3eb35-116">String</span></span>|<span data-ttu-id="3eb35-117">Tipo de asistente: `required`, `optional`, `resource`.</span><span class="sxs-lookup"><span data-stu-id="3eb35-117">The attendee type: `required`, `optional`, `resource`.</span></span>|
|<span data-ttu-id="3eb35-118">emailAddress</span><span class="sxs-lookup"><span data-stu-id="3eb35-118">emailAddress</span></span>|[<span data-ttu-id="3eb35-119">emailAddress</span><span class="sxs-lookup"><span data-stu-id="3eb35-119">emailAddress</span></span>](emailaddress.md)|<span data-ttu-id="3eb35-120">Incluye el nombre y la dirección de SMTP del asistente.</span><span class="sxs-lookup"><span data-stu-id="3eb35-120">Includes the name and SMTP address of the attendee.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3eb35-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3eb35-121">JSON representation</span></span>

<span data-ttu-id="3eb35-122">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3eb35-122">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.attendeeBase",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attendee"
}-->

```json
{
  "status": {"@odata.type": "microsoft.graph.responseStatus"},
  "type": "String",
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendee resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
