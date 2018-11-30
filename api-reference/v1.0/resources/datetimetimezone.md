---
title: Tipo de recurso dateTimeTimeZone
description: Describe la fecha, la hora y la zona horaria de un momento dado.
ms.openlocfilehash: 3ce02fbf82dabbbe354b2672cfd950812ea0bd32
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029021"
---
# <a name="datetimetimezone-resource-type"></a><span data-ttu-id="ea26f-103">Tipo de recurso dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="ea26f-103">dateTimeTimeZone resource type</span></span>

<span data-ttu-id="ea26f-104">Describe la fecha, la hora y la zona horaria de un momento dado.</span><span class="sxs-lookup"><span data-stu-id="ea26f-104">Describes the date, time, and time zone of a point in time.</span></span>

## <a name="properties"></a><span data-ttu-id="ea26f-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea26f-105">Properties</span></span>
| <span data-ttu-id="ea26f-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea26f-106">Property</span></span>     | <span data-ttu-id="ea26f-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea26f-107">Type</span></span>   |<span data-ttu-id="ea26f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea26f-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ea26f-109">dateTime</span><span class="sxs-lookup"><span data-stu-id="ea26f-109">dateTime</span></span>|<span data-ttu-id="ea26f-110">String</span><span class="sxs-lookup"><span data-stu-id="ea26f-110">String</span></span>|<span data-ttu-id="ea26f-111">Un único momento dado en una fecha combinada y la representación de tiempo (`<date>T<time>`).</span><span class="sxs-lookup"><span data-stu-id="ea26f-111">A single point of time in a combined date and time representation (`<date>T<time>`).</span></span>|
|<span data-ttu-id="ea26f-112">timeZone</span><span class="sxs-lookup"><span data-stu-id="ea26f-112">timeZone</span></span>|<span data-ttu-id="ea26f-113">String</span><span class="sxs-lookup"><span data-stu-id="ea26f-113">String</span></span>|<span data-ttu-id="ea26f-114">Uno de los siguientes nombres de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="ea26f-114">One of the following time zone names.</span></span>|

<span data-ttu-id="ea26f-115">La propiedad _TimeZone_ puede establecerse en cualquiera de las zonas horarias compatibles con Windows, así como los nombres de zona horaria siguientes.</span><span class="sxs-lookup"><span data-stu-id="ea26f-115">The _TimeZone_ property can be set to any of the time zones supported by Windows, as well as the following time zones names.</span></span>

<span data-ttu-id="ea26f-116">Etc/GMT+12</span><span class="sxs-lookup"><span data-stu-id="ea26f-116">Etc/GMT+12</span></span>

<span data-ttu-id="ea26f-117">Etc/GMT+11</span><span class="sxs-lookup"><span data-stu-id="ea26f-117">Etc/GMT+11</span></span>

<span data-ttu-id="ea26f-118">Pacific/Honolulu</span><span class="sxs-lookup"><span data-stu-id="ea26f-118">Pacific/Honolulu</span></span>

<span data-ttu-id="ea26f-119">America/Anchorage</span><span class="sxs-lookup"><span data-stu-id="ea26f-119">America/Anchorage</span></span>

<span data-ttu-id="ea26f-120">America/Santa_Isabel</span><span class="sxs-lookup"><span data-stu-id="ea26f-120">America/Santa_Isabel</span></span>

<span data-ttu-id="ea26f-121">America/Los_Angeles</span><span class="sxs-lookup"><span data-stu-id="ea26f-121">America/Los_Angeles</span></span>

<span data-ttu-id="ea26f-122">America/Phoenix</span><span class="sxs-lookup"><span data-stu-id="ea26f-122">America/Phoenix</span></span>

<span data-ttu-id="ea26f-123">America/Chihuahua</span><span class="sxs-lookup"><span data-stu-id="ea26f-123">America/Chihuahua</span></span>

<span data-ttu-id="ea26f-124">America/Denver</span><span class="sxs-lookup"><span data-stu-id="ea26f-124">America/Denver</span></span>

<span data-ttu-id="ea26f-125">America/Guatemala</span><span class="sxs-lookup"><span data-stu-id="ea26f-125">America/Guatemala</span></span>

<span data-ttu-id="ea26f-126">America/Chicago</span><span class="sxs-lookup"><span data-stu-id="ea26f-126">America/Chicago</span></span>

<span data-ttu-id="ea26f-127">America/Mexico_City</span><span class="sxs-lookup"><span data-stu-id="ea26f-127">America/Mexico_City</span></span>

<span data-ttu-id="ea26f-128">America/Regina</span><span class="sxs-lookup"><span data-stu-id="ea26f-128">America/Regina</span></span>

<span data-ttu-id="ea26f-129">America/Bogota</span><span class="sxs-lookup"><span data-stu-id="ea26f-129">America/Bogota</span></span>

<span data-ttu-id="ea26f-130">America/New_York</span><span class="sxs-lookup"><span data-stu-id="ea26f-130">America/New_York</span></span>

<span data-ttu-id="ea26f-131">America/Indiana/Indianapolis</span><span class="sxs-lookup"><span data-stu-id="ea26f-131">America/Indiana/Indianapolis</span></span>

<span data-ttu-id="ea26f-132">America/Caracas</span><span class="sxs-lookup"><span data-stu-id="ea26f-132">America/Caracas</span></span>

<span data-ttu-id="ea26f-133">America/Asuncion</span><span class="sxs-lookup"><span data-stu-id="ea26f-133">America/Asuncion</span></span>

<span data-ttu-id="ea26f-134">America/Halifax</span><span class="sxs-lookup"><span data-stu-id="ea26f-134">America/Halifax</span></span>

<span data-ttu-id="ea26f-135">America/Cuiaba</span><span class="sxs-lookup"><span data-stu-id="ea26f-135">America/Cuiaba</span></span>

<span data-ttu-id="ea26f-136">America/La_Paz</span><span class="sxs-lookup"><span data-stu-id="ea26f-136">America/La_Paz</span></span>

<span data-ttu-id="ea26f-137">America/Santiago</span><span class="sxs-lookup"><span data-stu-id="ea26f-137">America/Santiago</span></span>

<span data-ttu-id="ea26f-138">America/St_Johns</span><span class="sxs-lookup"><span data-stu-id="ea26f-138">America/St_Johns</span></span>

<span data-ttu-id="ea26f-139">America/Sao_Paulo</span><span class="sxs-lookup"><span data-stu-id="ea26f-139">America/Sao_Paulo</span></span>

<span data-ttu-id="ea26f-140">America/Argentina/Buenos_Aires</span><span class="sxs-lookup"><span data-stu-id="ea26f-140">America/Argentina/Buenos_Aires</span></span>

<span data-ttu-id="ea26f-141">America/Cayenne</span><span class="sxs-lookup"><span data-stu-id="ea26f-141">America/Cayenne</span></span>

<span data-ttu-id="ea26f-142">America/Godthab</span><span class="sxs-lookup"><span data-stu-id="ea26f-142">America/Godthab</span></span>

<span data-ttu-id="ea26f-143">America/Montevideo</span><span class="sxs-lookup"><span data-stu-id="ea26f-143">America/Montevideo</span></span>

<span data-ttu-id="ea26f-144">America/Bahia</span><span class="sxs-lookup"><span data-stu-id="ea26f-144">America/Bahia</span></span>

<span data-ttu-id="ea26f-145">Etc/GMT+2</span><span class="sxs-lookup"><span data-stu-id="ea26f-145">Etc/GMT+2</span></span>

<span data-ttu-id="ea26f-146">Atlantic/Azores</span><span class="sxs-lookup"><span data-stu-id="ea26f-146">Atlantic/Azores</span></span>

<span data-ttu-id="ea26f-147">Atlantic/Cape_Verde</span><span class="sxs-lookup"><span data-stu-id="ea26f-147">Atlantic/Cape_Verde</span></span>

<span data-ttu-id="ea26f-148">Africa/Casablanca</span><span class="sxs-lookup"><span data-stu-id="ea26f-148">Africa/Casablanca</span></span>

<span data-ttu-id="ea26f-149">Etc/GMT</span><span class="sxs-lookup"><span data-stu-id="ea26f-149">Etc/GMT</span></span>

<span data-ttu-id="ea26f-150">Europe/London</span><span class="sxs-lookup"><span data-stu-id="ea26f-150">Europe/London</span></span>

<span data-ttu-id="ea26f-151">Atlantic/Reykjavik</span><span class="sxs-lookup"><span data-stu-id="ea26f-151">Atlantic/Reykjavik</span></span>

<span data-ttu-id="ea26f-152">Europe/Berlin</span><span class="sxs-lookup"><span data-stu-id="ea26f-152">Europe/Berlin</span></span>

<span data-ttu-id="ea26f-153">Europe/Budapest</span><span class="sxs-lookup"><span data-stu-id="ea26f-153">Europe/Budapest</span></span>

<span data-ttu-id="ea26f-154">Europe/Paris</span><span class="sxs-lookup"><span data-stu-id="ea26f-154">Europe/Paris</span></span>

<span data-ttu-id="ea26f-155">Europe/Warsaw</span><span class="sxs-lookup"><span data-stu-id="ea26f-155">Europe/Warsaw</span></span>

<span data-ttu-id="ea26f-156">Africa/Lagos</span><span class="sxs-lookup"><span data-stu-id="ea26f-156">Africa/Lagos</span></span>

<span data-ttu-id="ea26f-157">Africa/Windhoek</span><span class="sxs-lookup"><span data-stu-id="ea26f-157">Africa/Windhoek</span></span>

<span data-ttu-id="ea26f-158">Europe/Bucharest</span><span class="sxs-lookup"><span data-stu-id="ea26f-158">Europe/Bucharest</span></span>

<span data-ttu-id="ea26f-159">Asia/Beirut</span><span class="sxs-lookup"><span data-stu-id="ea26f-159">Asia/Beirut</span></span>

<span data-ttu-id="ea26f-160">Africa/Cairo</span><span class="sxs-lookup"><span data-stu-id="ea26f-160">Africa/Cairo</span></span>

<span data-ttu-id="ea26f-161">Asia/Damasco</span><span class="sxs-lookup"><span data-stu-id="ea26f-161">Asia/Damascus</span></span>

<span data-ttu-id="ea26f-162">Africa/Johannesburg</span><span class="sxs-lookup"><span data-stu-id="ea26f-162">Africa/Johannesburg</span></span>

<span data-ttu-id="ea26f-163">Europe/Kyiv (Kiev)</span><span class="sxs-lookup"><span data-stu-id="ea26f-163">Europe/Kyiv (Kiev)</span></span>

<span data-ttu-id="ea26f-164">Europe/Istanbul</span><span class="sxs-lookup"><span data-stu-id="ea26f-164">Europe/Istanbul</span></span>

<span data-ttu-id="ea26f-165">Asia/Jerusalem</span><span class="sxs-lookup"><span data-stu-id="ea26f-165">Asia/Jerusalem</span></span>

<span data-ttu-id="ea26f-166">Asia/Amman</span><span class="sxs-lookup"><span data-stu-id="ea26f-166">Asia/Amman</span></span>

<span data-ttu-id="ea26f-167">Asia/Baghdad</span><span class="sxs-lookup"><span data-stu-id="ea26f-167">Asia/Baghdad</span></span>

<span data-ttu-id="ea26f-168">Europe/Kaliningrad</span><span class="sxs-lookup"><span data-stu-id="ea26f-168">Europe/Kaliningrad</span></span>

<span data-ttu-id="ea26f-169">Asia/Riyadh</span><span class="sxs-lookup"><span data-stu-id="ea26f-169">Asia/Riyadh</span></span>

<span data-ttu-id="ea26f-170">Africa/Nairobi</span><span class="sxs-lookup"><span data-stu-id="ea26f-170">Africa/Nairobi</span></span>

<span data-ttu-id="ea26f-171">Asia/Tehran</span><span class="sxs-lookup"><span data-stu-id="ea26f-171">Asia/Tehran</span></span>

<span data-ttu-id="ea26f-172">Asia/Dubai</span><span class="sxs-lookup"><span data-stu-id="ea26f-172">Asia/Dubai</span></span>

<span data-ttu-id="ea26f-173">Asia/Baku</span><span class="sxs-lookup"><span data-stu-id="ea26f-173">Asia/Baku</span></span>

<span data-ttu-id="ea26f-174">Europe/Moscow</span><span class="sxs-lookup"><span data-stu-id="ea26f-174">Europe/Moscow</span></span>

<span data-ttu-id="ea26f-175">Indian/Mauritius</span><span class="sxs-lookup"><span data-stu-id="ea26f-175">Indian/Mauritius</span></span>

<span data-ttu-id="ea26f-176">Asia/Tbilisi</span><span class="sxs-lookup"><span data-stu-id="ea26f-176">Asia/Tbilisi</span></span>

<span data-ttu-id="ea26f-177">Asia/Yerevan</span><span class="sxs-lookup"><span data-stu-id="ea26f-177">Asia/Yerevan</span></span>

<span data-ttu-id="ea26f-178">Asia/Kabul</span><span class="sxs-lookup"><span data-stu-id="ea26f-178">Asia/Kabul</span></span>

<span data-ttu-id="ea26f-179">Asia/Karachi</span><span class="sxs-lookup"><span data-stu-id="ea26f-179">Asia/Karachi</span></span>

<span data-ttu-id="ea26f-180">Asia/Toshkent (Tashkent)</span><span class="sxs-lookup"><span data-stu-id="ea26f-180">Asia/Toshkent (Tashkent)</span></span>

<span data-ttu-id="ea26f-181">Asia/Kolkata</span><span class="sxs-lookup"><span data-stu-id="ea26f-181">Asia/Kolkata</span></span>

<span data-ttu-id="ea26f-182">Asia/Colombo</span><span class="sxs-lookup"><span data-stu-id="ea26f-182">Asia/Colombo</span></span>

<span data-ttu-id="ea26f-183">Asia/Kathmandu</span><span class="sxs-lookup"><span data-stu-id="ea26f-183">Asia/Kathmandu</span></span>

<span data-ttu-id="ea26f-184">Asia/Astana (Almaty)</span><span class="sxs-lookup"><span data-stu-id="ea26f-184">Asia/Astana (Almaty)</span></span>

<span data-ttu-id="ea26f-185">Asia/Dhaka</span><span class="sxs-lookup"><span data-stu-id="ea26f-185">Asia/Dhaka</span></span>

<span data-ttu-id="ea26f-186">Asia/Yekaterinburg</span><span class="sxs-lookup"><span data-stu-id="ea26f-186">Asia/Yekaterinburg</span></span>

<span data-ttu-id="ea26f-187">Asia/Yangon (Rangoon)</span><span class="sxs-lookup"><span data-stu-id="ea26f-187">Asia/Yangon (Rangoon)</span></span>

<span data-ttu-id="ea26f-188">Asia/Bangkok</span><span class="sxs-lookup"><span data-stu-id="ea26f-188">Asia/Bangkok</span></span>

<span data-ttu-id="ea26f-189">Asia/Novosibirsk</span><span class="sxs-lookup"><span data-stu-id="ea26f-189">Asia/Novosibirsk</span></span>

<span data-ttu-id="ea26f-190">Asia/Shanghai</span><span class="sxs-lookup"><span data-stu-id="ea26f-190">Asia/Shanghai</span></span>

<span data-ttu-id="ea26f-191">Asia/Krasnoyarsk</span><span class="sxs-lookup"><span data-stu-id="ea26f-191">Asia/Krasnoyarsk</span></span>

<span data-ttu-id="ea26f-192">Asia/Singapore</span><span class="sxs-lookup"><span data-stu-id="ea26f-192">Asia/Singapore</span></span>

<span data-ttu-id="ea26f-193">Australia/Perth</span><span class="sxs-lookup"><span data-stu-id="ea26f-193">Australia/Perth</span></span>

<span data-ttu-id="ea26f-194">Asia/Taipei</span><span class="sxs-lookup"><span data-stu-id="ea26f-194">Asia/Taipei</span></span>

<span data-ttu-id="ea26f-195">Asia/Ulaanbaatar</span><span class="sxs-lookup"><span data-stu-id="ea26f-195">Asia/Ulaanbaatar</span></span>

<span data-ttu-id="ea26f-196">Asia/Irkutsk</span><span class="sxs-lookup"><span data-stu-id="ea26f-196">Asia/Irkutsk</span></span>

<span data-ttu-id="ea26f-197">Asia/Tokyo</span><span class="sxs-lookup"><span data-stu-id="ea26f-197">Asia/Tokyo</span></span>

<span data-ttu-id="ea26f-198">Asia/Seoul</span><span class="sxs-lookup"><span data-stu-id="ea26f-198">Asia/Seoul</span></span>

<span data-ttu-id="ea26f-199">Australia/Adelaide</span><span class="sxs-lookup"><span data-stu-id="ea26f-199">Australia/Adelaide</span></span>

<span data-ttu-id="ea26f-200">Australia/Darwin</span><span class="sxs-lookup"><span data-stu-id="ea26f-200">Australia/Darwin</span></span>

<span data-ttu-id="ea26f-201">Australia/Brisbane</span><span class="sxs-lookup"><span data-stu-id="ea26f-201">Australia/Brisbane</span></span>

<span data-ttu-id="ea26f-202">Australia/Sydney</span><span class="sxs-lookup"><span data-stu-id="ea26f-202">Australia/Sydney</span></span>

<span data-ttu-id="ea26f-203">Pacific/Port_Moresby</span><span class="sxs-lookup"><span data-stu-id="ea26f-203">Pacific/Port_Moresby</span></span>

<span data-ttu-id="ea26f-204">Australia/Hobart</span><span class="sxs-lookup"><span data-stu-id="ea26f-204">Australia/Hobart</span></span>

<span data-ttu-id="ea26f-205">Asia/Yakutsk</span><span class="sxs-lookup"><span data-stu-id="ea26f-205">Asia/Yakutsk</span></span>

<span data-ttu-id="ea26f-206">Pacific/Guadalcanal</span><span class="sxs-lookup"><span data-stu-id="ea26f-206">Pacific/Guadalcanal</span></span>

<span data-ttu-id="ea26f-207">Asia/Vladivostok</span><span class="sxs-lookup"><span data-stu-id="ea26f-207">Asia/Vladivostok</span></span>

<span data-ttu-id="ea26f-208">Pacific/Auckland</span><span class="sxs-lookup"><span data-stu-id="ea26f-208">Pacific/Auckland</span></span>

<span data-ttu-id="ea26f-209">Etc/GMT-12</span><span class="sxs-lookup"><span data-stu-id="ea26f-209">Etc/GMT-12</span></span>

<span data-ttu-id="ea26f-210">Pacific/Fiji</span><span class="sxs-lookup"><span data-stu-id="ea26f-210">Pacific/Fiji</span></span>

<span data-ttu-id="ea26f-211">Asia/Magadan</span><span class="sxs-lookup"><span data-stu-id="ea26f-211">Asia/Magadan</span></span>

<span data-ttu-id="ea26f-212">Pacific/Tongatapu</span><span class="sxs-lookup"><span data-stu-id="ea26f-212">Pacific/Tongatapu</span></span>

<span data-ttu-id="ea26f-213">Pacific/Apia</span><span class="sxs-lookup"><span data-stu-id="ea26f-213">Pacific/Apia</span></span>

<span data-ttu-id="ea26f-214">Pacific/Kiritimati</span><span class="sxs-lookup"><span data-stu-id="ea26f-214">Pacific/Kiritimati</span></span>

## <a name="json-representation"></a><span data-ttu-id="ea26f-215">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ea26f-215">JSON representation</span></span>

<span data-ttu-id="ea26f-216">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ea26f-216">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.dateTimeTimeZone"
}-->

```json
{
  "dateTime": "string",
  "timeZone": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "dateTimeTimeZone resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
