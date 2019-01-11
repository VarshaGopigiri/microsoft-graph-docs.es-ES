---
title: Tipo de recurso customTimeZone
description: Representa una zona horaria en la que la transición del horario de verano a la hora estándar, o viceversa, no es estándar.
localization_priority: Normal
ms.openlocfilehash: bad1a190581592d2d9465284bf8ab1c41fe2370a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818280"
---
# <a name="customtimezone-resource-type"></a><span data-ttu-id="92db4-103">Tipo de recurso customTimeZone</span><span class="sxs-lookup"><span data-stu-id="92db4-103">customTimeZone resource type</span></span>

> <span data-ttu-id="92db4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="92db4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="92db4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="92db4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="92db4-106">Representa una zona horaria en la que la transición del horario de verano a la hora estándar, o viceversa, no es estándar.</span><span class="sxs-lookup"><span data-stu-id="92db4-106">Represents a time zone where the transition from standard to daylight saving time, or vice versa is not standard.</span></span>


## <a name="properties"></a><span data-ttu-id="92db4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="92db4-107">Properties</span></span>
| <span data-ttu-id="92db4-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="92db4-108">Property</span></span>     | <span data-ttu-id="92db4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="92db4-109">Type</span></span>   |<span data-ttu-id="92db4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="92db4-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="92db4-111">bias</span><span class="sxs-lookup"><span data-stu-id="92db4-111">bias</span></span> | <span data-ttu-id="92db4-112">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="92db4-112">Edm.Int32</span></span> | <span data-ttu-id="92db4-113">Diferencia horaria de la zona horaria con respecto a la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="92db4-113">The time offset of the time zone from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="92db4-114">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="92db4-114">This value is in minutes.</span></span><span data-ttu-id="92db4-115">Las zonas horarias que son anteriores a UTC tienen una diferencia positiva; las zonas horarias que son posteriores a UTC tienen una diferencia negativa.</span><span class="sxs-lookup"><span data-stu-id="92db4-115"> Time zones that are ahead of UTC have a positive offset; time zones that are behind UTC have a negative offset.</span></span>|
| <span data-ttu-id="92db4-116">daylightOffset</span><span class="sxs-lookup"><span data-stu-id="92db4-116">daylightOffset</span></span> | [<span data-ttu-id="92db4-117">daylightTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="92db4-117">daylightTimeZoneOffset</span></span>](daylighttimezoneoffset.md) | <span data-ttu-id="92db4-118">Especifica cuándo la zona horaria cambia de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="92db4-118">Specifies when the time zone switches from standard time to daylight saving time.</span></span> |
| <span data-ttu-id="92db4-119">name</span><span class="sxs-lookup"><span data-stu-id="92db4-119">name</span></span> | <span data-ttu-id="92db4-120">string</span><span class="sxs-lookup"><span data-stu-id="92db4-120">string</span></span> | <span data-ttu-id="92db4-121">Nombre de la zona horaria personalizada.</span><span class="sxs-lookup"><span data-stu-id="92db4-121">The name of the custom time zone.</span></span> |
| <span data-ttu-id="92db4-122">standardOffset</span><span class="sxs-lookup"><span data-stu-id="92db4-122">standardOffset</span></span> | [<span data-ttu-id="92db4-123">standardTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="92db4-123">standardTimeZoneOffset</span></span>](standardtimezoneoffset.md) | <span data-ttu-id="92db4-124">Especifica cuándo la zona horaria cambia del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="92db4-124">Specifies when the time zone switches from daylight saving time to standard time.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="92db4-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="92db4-125">JSON representation</span></span>

<span data-ttu-id="92db4-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="92db4-126">Here is a JSON representation of the resource.</span></span>

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
