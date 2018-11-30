---
title: Tipo de recurso customTimeZone
description: Representa una zona horaria en la que la transición del horario de verano a la hora estándar, o viceversa, no es estándar.
ms.openlocfilehash: 83375c96e4247cb0ddf2d17b1bede2c295f0b27f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083252"
---
# <a name="customtimezone-resource-type"></a><span data-ttu-id="c3beb-103">Tipo de recurso customTimeZone</span><span class="sxs-lookup"><span data-stu-id="c3beb-103">customTimeZone resource type</span></span>

> <span data-ttu-id="c3beb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c3beb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c3beb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c3beb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c3beb-106">Representa una zona horaria en la que la transición del horario de verano a la hora estándar, o viceversa, no es estándar.</span><span class="sxs-lookup"><span data-stu-id="c3beb-106">Represents a time zone where the transition from standard to daylight saving time, or vice versa is not standard.</span></span>


## <a name="properties"></a><span data-ttu-id="c3beb-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c3beb-107">Properties</span></span>
| <span data-ttu-id="c3beb-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c3beb-108">Property</span></span>     | <span data-ttu-id="c3beb-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c3beb-109">Type</span></span>   |<span data-ttu-id="c3beb-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3beb-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c3beb-111">bias</span><span class="sxs-lookup"><span data-stu-id="c3beb-111">bias</span></span> | <span data-ttu-id="c3beb-112">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="c3beb-112">Edm.Int32</span></span> | <span data-ttu-id="c3beb-113">Diferencia horaria de la zona horaria con respecto a la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="c3beb-113">The time offset of the time zone from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="c3beb-114">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="c3beb-114">This value is in minutes.</span></span><span data-ttu-id="c3beb-115">Las zonas horarias que son anteriores a UTC tienen una diferencia positiva; las zonas horarias que son posteriores a UTC tienen una diferencia negativa.</span><span class="sxs-lookup"><span data-stu-id="c3beb-115"> Time zones that are ahead of UTC have a positive offset; time zones that are behind UTC have a negative offset.</span></span>|
| <span data-ttu-id="c3beb-116">daylightOffset</span><span class="sxs-lookup"><span data-stu-id="c3beb-116">daylightOffset</span></span> | [<span data-ttu-id="c3beb-117">daylightTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="c3beb-117">daylightTimeZoneOffset</span></span>](daylighttimezoneoffset.md) | <span data-ttu-id="c3beb-118">Especifica cuándo la zona horaria cambia de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c3beb-118">Specifies when the time zone switches from standard time to daylight saving time.</span></span> |
| <span data-ttu-id="c3beb-119">name</span><span class="sxs-lookup"><span data-stu-id="c3beb-119">name</span></span> | <span data-ttu-id="c3beb-120">string</span><span class="sxs-lookup"><span data-stu-id="c3beb-120">string</span></span> | <span data-ttu-id="c3beb-121">Nombre de la zona horaria personalizada.</span><span class="sxs-lookup"><span data-stu-id="c3beb-121">The name of the custom time zone.</span></span> |
| <span data-ttu-id="c3beb-122">standardOffset</span><span class="sxs-lookup"><span data-stu-id="c3beb-122">standardOffset</span></span> | [<span data-ttu-id="c3beb-123">standardTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="c3beb-123">standardTimeZoneOffset</span></span>](standardtimezoneoffset.md) | <span data-ttu-id="c3beb-124">Especifica cuándo la zona horaria cambia del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="c3beb-124">Specifies when the time zone switches from daylight saving time to standard time.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="c3beb-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c3beb-125">JSON representation</span></span>

<span data-ttu-id="c3beb-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c3beb-126">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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