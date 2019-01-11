---
title: Tipo de recurso attendee
description: Asistente a un evento. Esto puede ser una persona o un recurso, como una sala de reuniones o equipamiento que se ha configurado como un recurso en el servidor Exchange del espacio empresarial.
localization_priority: Normal
ms.openlocfilehash: 95881d0e2f3dfe51b975e60ba6f8d32cda5e222c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27859328"
---
# <a name="attendee-resource-type"></a><span data-ttu-id="78a92-104">Tipo de recurso attendee</span><span class="sxs-lookup"><span data-stu-id="78a92-104">attendee resource type</span></span>

> <span data-ttu-id="78a92-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="78a92-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="78a92-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="78a92-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="78a92-107">Asistente a un evento.</span><span class="sxs-lookup"><span data-stu-id="78a92-107">An event attendee.</span></span> <span data-ttu-id="78a92-108">Esto puede ser una persona o un recurso, como una sala de reuniones o equipamiento que se ha configurado como un recurso en el servidor Exchange del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="78a92-108">This can be a person or resource such as a meeting room or equipment, that has been set up as a resource on the Exchange server for the tenant.</span></span>

<span data-ttu-id="78a92-109">Derivadas de [attendeeBase](attendeebase.md).</span><span class="sxs-lookup"><span data-stu-id="78a92-109">Derived from [attendeeBase](attendeebase.md).</span></span>

## <a name="properties"></a><span data-ttu-id="78a92-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78a92-110">Properties</span></span>
| <span data-ttu-id="78a92-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78a92-111">Property</span></span>     | <span data-ttu-id="78a92-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="78a92-112">Type</span></span>   |<span data-ttu-id="78a92-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="78a92-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="78a92-114">status</span><span class="sxs-lookup"><span data-stu-id="78a92-114">status</span></span>|[<span data-ttu-id="78a92-115">ResponseStatus</span><span class="sxs-lookup"><span data-stu-id="78a92-115">ResponseStatus</span></span>](responsestatus.md)|<span data-ttu-id="78a92-116">Respuesta del asistente (ninguna, aceptada, rechazada, etc.) para el evento y fecha y hora en que se envió la respuesta.</span><span class="sxs-lookup"><span data-stu-id="78a92-116">The attendee's response (none, accepted, declined, etc.) for the event and date-time that the response was sent.</span></span>|
|<span data-ttu-id="78a92-117">type</span><span class="sxs-lookup"><span data-stu-id="78a92-117">type</span></span>|<span data-ttu-id="78a92-118">String</span><span class="sxs-lookup"><span data-stu-id="78a92-118">String</span></span>|<span data-ttu-id="78a92-119">Tipo de asistente: `required`, `optional`, `resource`.</span><span class="sxs-lookup"><span data-stu-id="78a92-119">The attendee type: `required`, `optional`, `resource`.</span></span>|
|<span data-ttu-id="78a92-120">emailAddress</span><span class="sxs-lookup"><span data-stu-id="78a92-120">emailAddress</span></span>|[<span data-ttu-id="78a92-121">emailAddress</span><span class="sxs-lookup"><span data-stu-id="78a92-121">emailAddress</span></span>](emailaddress.md)|<span data-ttu-id="78a92-122">Incluye el nombre y la dirección de SMTP del asistente.</span><span class="sxs-lookup"><span data-stu-id="78a92-122">Includes the name and SMTP address of the attendee.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="78a92-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="78a92-123">JSON representation</span></span>

<span data-ttu-id="78a92-124">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="78a92-124">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
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
