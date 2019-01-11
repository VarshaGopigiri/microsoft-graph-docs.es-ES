---
title: Tipo de recurso workingHours
description: Representa los días de la semana y las horas de la zona horaria específica en la que trabaja el usuario.
localization_priority: Normal
ms.openlocfilehash: b221b6f4f1fe8dee7fc7a043993f0d0cd3ea5b7c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805246"
---
# <a name="workinghours-resource-type"></a><span data-ttu-id="56219-103">Tipo de recurso workingHours</span><span class="sxs-lookup"><span data-stu-id="56219-103">workingHours resource type</span></span>

<span data-ttu-id="56219-104">Representa los días de la semana y las horas de la zona horaria específica en la que trabaja el usuario.</span><span class="sxs-lookup"><span data-stu-id="56219-104">Represents the days of the week and hours in a specific time zone that the user works.</span></span>

<span data-ttu-id="56219-105">Tener acceso al horario laboral de un usuario resulta útil en escenarios en los que se administran la planeación de recursos o actividades.</span><span class="sxs-lookup"><span data-stu-id="56219-105">Having access to a user's working hours is useful in scenarios that handle activity or resource planning.</span></span> <span data-ttu-id="56219-106">Puede [obtener](../api/user-get-mailboxsettings.md#request-3) y [establecer](../api/user-update-mailboxsettings.md#request-2) el horario laboral de un usuario como parte de la [configuración de buzón](mailboxsettings.md) del usuario.</span><span class="sxs-lookup"><span data-stu-id="56219-106">You can [get](../api/user-get-mailboxsettings.md#request-3) and [set](../api/user-update-mailboxsettings.md#request-2) the working hours of a user as part of the user's [mailbox settings](mailboxsettings.md).</span></span> 

<span data-ttu-id="56219-107">Puede establecer una zona horaria para el horario laboral distinta de la zona horaria que haya configurado en el cliente de Outlook.</span><span class="sxs-lookup"><span data-stu-id="56219-107">You can choose to set a time zone for your working hours differently from the time zone you have set on your Outlook client.</span></span> <span data-ttu-id="56219-108">Esto puede resultar útil, por ejemplo, si se desplaza a una zona horaria distinta de aquella en la que habitualmente trabaja.</span><span class="sxs-lookup"><span data-stu-id="56219-108">This can be useful in cases like when you travel to a different time zone than you usually work in.</span></span> <span data-ttu-id="56219-109">Puede establecer el cliente de Outlook</span><span class="sxs-lookup"><span data-stu-id="56219-109">You can set the Outlook client</span></span>  
<span data-ttu-id="56219-110">en la zona horaria de destino para que los valores de hora de Outlook se muestren en la hora local mientras está allí.</span><span class="sxs-lookup"><span data-stu-id="56219-110">to the destination time zone so that Outlook time values are displayed in local time while you are there.</span></span>
<span data-ttu-id="56219-111">Cuando otras personas solicitan reuniones de trabajo con usted en su lugar de trabajo habitual, aún pueden respetar su horario laboral en la zona horaria correspondiente.</span><span class="sxs-lookup"><span data-stu-id="56219-111">When other people request work meetings with you in your usual place of work, they can still respect your working hours in the appropriate time zone.</span></span>


## <a name="properties"></a><span data-ttu-id="56219-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="56219-112">Properties</span></span>
| <span data-ttu-id="56219-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="56219-113">Property</span></span>     | <span data-ttu-id="56219-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="56219-114">Type</span></span>   |<span data-ttu-id="56219-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="56219-115">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="56219-116">daysOfWeek</span><span class="sxs-lookup"><span data-stu-id="56219-116">daysOfWeek</span></span> | <span data-ttu-id="56219-117">colección de dayOfWeek</span><span class="sxs-lookup"><span data-stu-id="56219-117">dayOfWeek collection</span></span> | <span data-ttu-id="56219-118">Días de la semana en los que el usuario trabaja.</span><span class="sxs-lookup"><span data-stu-id="56219-118">The days of the week on which the user works.</span></span> |
| <span data-ttu-id="56219-119">startTime</span><span class="sxs-lookup"><span data-stu-id="56219-119">startTime</span></span> | <span data-ttu-id="56219-120">Edm.TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="56219-120">Edm.TimeOfDay</span></span> | <span data-ttu-id="56219-121">Hora del día en la que el usuario empieza a trabajar.</span><span class="sxs-lookup"><span data-stu-id="56219-121">The time of the day that the user starts working.</span></span> |
| <span data-ttu-id="56219-122">endTime</span><span class="sxs-lookup"><span data-stu-id="56219-122">endTime</span></span> | <span data-ttu-id="56219-123">Edm.TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="56219-123">Edm.TimeOfDay</span></span> | <span data-ttu-id="56219-124">Hora del día en la que el usuario deja de trabajar.</span><span class="sxs-lookup"><span data-stu-id="56219-124">The time of the day that the user stops working.</span></span> |
| <span data-ttu-id="56219-125">timeZone</span><span class="sxs-lookup"><span data-stu-id="56219-125">timeZone</span></span> | [<span data-ttu-id="56219-126">timeZoneBase</span><span class="sxs-lookup"><span data-stu-id="56219-126">timeZoneBase</span></span>](timezonebase.md) | <span data-ttu-id="56219-127">Zona horaria a la que se aplica el horario laboral.</span><span class="sxs-lookup"><span data-stu-id="56219-127">The time zone to which the working hours apply.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="56219-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="56219-128">JSON representation</span></span>

<span data-ttu-id="56219-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="56219-129">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workingHours"
}-->

```json
{
  "daysOfWeek": ["string"],
  "startTime": "TimeOfDay",
  "endTime": "TimeOfDay",
  "timeZone": {"@odata.type": "microsoft.graph.timeZoneBase"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "workingHours resource",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/workinghours.md/microsoft.graph.workingHours/daysOfWeek:
      Inconsistent types between parameter (String) and table (Object)"
  ],
  "tocPath": ""
}-->
