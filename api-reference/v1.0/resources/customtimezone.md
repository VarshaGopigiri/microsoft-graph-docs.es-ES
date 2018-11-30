---
title: Tipo de recurso customTimeZone
description: Representa una zona horaria en la que la transición del horario de verano a la hora estándar, o viceversa, no es estándar.
ms.openlocfilehash: 36d497e3e6ad52ca5a59f4bc322410ee271e73bf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029920"
---
# <a name="customtimezone-resource-type"></a><span data-ttu-id="41f30-103">Tipo de recurso customTimeZone</span><span class="sxs-lookup"><span data-stu-id="41f30-103">customTimeZone resource type</span></span>

<span data-ttu-id="41f30-104">Representa una zona horaria en la que la transición del horario de verano a la hora estándar, o viceversa, no es estándar.</span><span class="sxs-lookup"><span data-stu-id="41f30-104">Represents a time zone where the transition from standard to daylight saving time, or vice versa is not standard.</span></span>


## <a name="properties"></a><span data-ttu-id="41f30-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41f30-105">Properties</span></span>
| <span data-ttu-id="41f30-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="41f30-106">Property</span></span>     | <span data-ttu-id="41f30-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="41f30-107">Type</span></span>   |<span data-ttu-id="41f30-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="41f30-108">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="41f30-109">bias</span><span class="sxs-lookup"><span data-stu-id="41f30-109">bias</span></span> | <span data-ttu-id="41f30-110">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="41f30-110">Edm.Int32</span></span> | <span data-ttu-id="41f30-111">Diferencia horaria de la zona horaria con respecto a la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="41f30-111">The time offset of the time zone from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="41f30-112">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="41f30-112">This value is in minutes.</span></span><span data-ttu-id="41f30-113">Las zonas horarias que son anteriores a UTC tienen una diferencia positiva; las zonas horarias que son posteriores a UTC tienen una diferencia negativa.</span><span class="sxs-lookup"><span data-stu-id="41f30-113"> Time zones that are ahead of UTC have a positive offset; time zones that are behind UTC have a negative offset.</span></span>|
| <span data-ttu-id="41f30-114">daylightOffset</span><span class="sxs-lookup"><span data-stu-id="41f30-114">daylightOffset</span></span> | [<span data-ttu-id="41f30-115">daylightTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="41f30-115">daylightTimeZoneOffset</span></span>](daylighttimezoneoffset.md) | <span data-ttu-id="41f30-116">Especifica cuándo la zona horaria cambia de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="41f30-116">Specifies when the time zone switches from standard time to daylight saving time.</span></span> |
| <span data-ttu-id="41f30-117">name</span><span class="sxs-lookup"><span data-stu-id="41f30-117">name</span></span> | <span data-ttu-id="41f30-118">string</span><span class="sxs-lookup"><span data-stu-id="41f30-118">string</span></span> | <span data-ttu-id="41f30-119">Nombre de la zona horaria personalizada.</span><span class="sxs-lookup"><span data-stu-id="41f30-119">The name of the custom time zone.</span></span> |
| <span data-ttu-id="41f30-120">standardOffset</span><span class="sxs-lookup"><span data-stu-id="41f30-120">standardOffset</span></span> | [<span data-ttu-id="41f30-121">standardTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="41f30-121">standardTimeZoneOffset</span></span>](standardtimezoneoffset.md) | <span data-ttu-id="41f30-122">Especifica cuándo la zona horaria cambia del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="41f30-122">Specifies when the time zone switches from daylight saving time to standard time.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="41f30-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="41f30-123">JSON representation</span></span>

<span data-ttu-id="41f30-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="41f30-124">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "baseType": "microsoft.graph.timeZoneBase",
  "@odata.type": "microsoft.graph.customTimeZone"
}-->

```json
{
  "bias": "Int32",
  "daylightOffset": {"@odata.type": "microsoft.graph.daylightTimeZoneOffset"},
  "name": "string",
  "standardOffset": {"@odata.type": "microsoft.graph.standardTimeZoneOffset"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "customTimeZone resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->