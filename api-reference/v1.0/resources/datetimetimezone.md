---
title: Tipo de recurso dateTimeTimeZone
description: Describe la fecha, la hora y la zona horaria de un momento dado.
localization_priority: Priority
ms.openlocfilehash: 9bec62c21f97c58b915ecc40010f8030ea760825
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27827331"
---
# <a name="datetimetimezone-resource-type"></a><span data-ttu-id="f572b-103">Tipo de recurso dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="f572b-103">dateTimeTimeZone resource type</span></span>

<span data-ttu-id="f572b-104">Describe la fecha, la hora y la zona horaria de un momento dado.</span><span class="sxs-lookup"><span data-stu-id="f572b-104">Describes the date, time, and time zone of a point in time.</span></span>

## <a name="properties"></a><span data-ttu-id="f572b-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f572b-105">Properties</span></span>
| <span data-ttu-id="f572b-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f572b-106">Property</span></span>     | <span data-ttu-id="f572b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f572b-107">Type</span></span>   |<span data-ttu-id="f572b-108">Description</span><span class="sxs-lookup"><span data-stu-id="f572b-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f572b-109">dateTime</span><span class="sxs-lookup"><span data-stu-id="f572b-109">dateTime</span></span>|<span data-ttu-id="f572b-110">String</span><span class="sxs-lookup"><span data-stu-id="f572b-110">String</span></span>|<span data-ttu-id="f572b-111">Un único momento dado en una fecha combinada y la representación de tiempo (`<date>T<time>`).</span><span class="sxs-lookup"><span data-stu-id="f572b-111">A single point of time in a combined date and time representation (`<date>T<time>`).</span></span>|
|<span data-ttu-id="f572b-112">timeZone</span><span class="sxs-lookup"><span data-stu-id="f572b-112">timeZone</span></span>|<span data-ttu-id="f572b-113">String</span><span class="sxs-lookup"><span data-stu-id="f572b-113">String</span></span>|<span data-ttu-id="f572b-114">Uno de los siguientes nombres de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="f572b-114">One of the following time zone names.</span></span>|

<span data-ttu-id="f572b-115">La propiedad _TimeZone_ puede establecerse en cualquiera de las zonas horarias compatibles con Windows, así como los nombres de zona horaria siguientes.</span><span class="sxs-lookup"><span data-stu-id="f572b-115">The _TimeZone_ property can be set to any of the time zones supported by Windows, as well as the following time zones names.</span></span>

<span data-ttu-id="f572b-116">Etc/GMT+12</span><span class="sxs-lookup"><span data-stu-id="f572b-116">Etc/GMT+12</span></span>

<span data-ttu-id="f572b-117">Etc/GMT+11</span><span class="sxs-lookup"><span data-stu-id="f572b-117">Etc/GMT+11</span></span>

<span data-ttu-id="f572b-118">Pacific/Honolulu</span><span class="sxs-lookup"><span data-stu-id="f572b-118">Pacific/Honolulu</span></span>

<span data-ttu-id="f572b-119">America/Anchorage</span><span class="sxs-lookup"><span data-stu-id="f572b-119">America/Anchorage</span></span>

<span data-ttu-id="f572b-120">America/Santa_Isabel</span><span class="sxs-lookup"><span data-stu-id="f572b-120">America/Santa_Isabel</span></span>

<span data-ttu-id="f572b-121">America/Los_Angeles</span><span class="sxs-lookup"><span data-stu-id="f572b-121">America/Los_Angeles</span></span>

<span data-ttu-id="f572b-122">America/Phoenix</span><span class="sxs-lookup"><span data-stu-id="f572b-122">America/Phoenix</span></span>

<span data-ttu-id="f572b-123">America/Chihuahua</span><span class="sxs-lookup"><span data-stu-id="f572b-123">America/Chihuahua</span></span>

<span data-ttu-id="f572b-124">America/Denver</span><span class="sxs-lookup"><span data-stu-id="f572b-124">America/Denver</span></span>

<span data-ttu-id="f572b-125">America/Guatemala</span><span class="sxs-lookup"><span data-stu-id="f572b-125">America/Guatemala</span></span>

<span data-ttu-id="f572b-126">America/Chicago</span><span class="sxs-lookup"><span data-stu-id="f572b-126">America/Chicago</span></span>

<span data-ttu-id="f572b-127">America/Mexico_City</span><span class="sxs-lookup"><span data-stu-id="f572b-127">America/Mexico_City</span></span>

<span data-ttu-id="f572b-128">America/Regina</span><span class="sxs-lookup"><span data-stu-id="f572b-128">America/Regina</span></span>

<span data-ttu-id="f572b-129">America/Bogota</span><span class="sxs-lookup"><span data-stu-id="f572b-129">America/Bogota</span></span>

<span data-ttu-id="f572b-130">America/New_York</span><span class="sxs-lookup"><span data-stu-id="f572b-130">America/New_York</span></span>

<span data-ttu-id="f572b-131">America/Indiana/Indianapolis</span><span class="sxs-lookup"><span data-stu-id="f572b-131">America/Indiana/Indianapolis</span></span>

<span data-ttu-id="f572b-132">America/Caracas</span><span class="sxs-lookup"><span data-stu-id="f572b-132">America/Caracas</span></span>

<span data-ttu-id="f572b-133">America/Asuncion</span><span class="sxs-lookup"><span data-stu-id="f572b-133">America/Asuncion</span></span>

<span data-ttu-id="f572b-134">America/Halifax</span><span class="sxs-lookup"><span data-stu-id="f572b-134">America/Halifax</span></span>

<span data-ttu-id="f572b-135">America/Cuiaba</span><span class="sxs-lookup"><span data-stu-id="f572b-135">America/Cuiaba</span></span>

<span data-ttu-id="f572b-136">America/La_Paz</span><span class="sxs-lookup"><span data-stu-id="f572b-136">America/La_Paz</span></span>

<span data-ttu-id="f572b-137">America/Santiago</span><span class="sxs-lookup"><span data-stu-id="f572b-137">America/Santiago</span></span>

<span data-ttu-id="f572b-138">America/St_Johns</span><span class="sxs-lookup"><span data-stu-id="f572b-138">America/St_Johns</span></span>

<span data-ttu-id="f572b-139">America/Sao_Paulo</span><span class="sxs-lookup"><span data-stu-id="f572b-139">America/Sao_Paulo</span></span>

<span data-ttu-id="f572b-140">America/Argentina/Buenos_Aires</span><span class="sxs-lookup"><span data-stu-id="f572b-140">America/Argentina/Buenos_Aires</span></span>

<span data-ttu-id="f572b-141">America/Cayenne</span><span class="sxs-lookup"><span data-stu-id="f572b-141">America/Cayenne</span></span>

<span data-ttu-id="f572b-142">America/Godthab</span><span class="sxs-lookup"><span data-stu-id="f572b-142">America/Godthab</span></span>

<span data-ttu-id="f572b-143">America/Montevideo</span><span class="sxs-lookup"><span data-stu-id="f572b-143">America/Montevideo</span></span>

<span data-ttu-id="f572b-144">America/Bahia</span><span class="sxs-lookup"><span data-stu-id="f572b-144">America/Bahia</span></span>

<span data-ttu-id="f572b-145">Etc/GMT+2</span><span class="sxs-lookup"><span data-stu-id="f572b-145">Etc/GMT+2</span></span>

<span data-ttu-id="f572b-146">Atlantic/Azores</span><span class="sxs-lookup"><span data-stu-id="f572b-146">Atlantic/Azores</span></span>

<span data-ttu-id="f572b-147">Atlantic/Cape_Verde</span><span class="sxs-lookup"><span data-stu-id="f572b-147">Atlantic/Cape_Verde</span></span>

<span data-ttu-id="f572b-148">Africa/Casablanca</span><span class="sxs-lookup"><span data-stu-id="f572b-148">Africa/Casablanca</span></span>

<span data-ttu-id="f572b-149">Etc/GMT</span><span class="sxs-lookup"><span data-stu-id="f572b-149">Etc/GMT</span></span>

<span data-ttu-id="f572b-150">Europe/London</span><span class="sxs-lookup"><span data-stu-id="f572b-150">Europe/London</span></span>

<span data-ttu-id="f572b-151">Atlantic/Reykjavik</span><span class="sxs-lookup"><span data-stu-id="f572b-151">Atlantic/Reykjavik</span></span>

<span data-ttu-id="f572b-152">Europe/Berlin</span><span class="sxs-lookup"><span data-stu-id="f572b-152">Europe/Berlin</span></span>

<span data-ttu-id="f572b-153">Europe/Budapest</span><span class="sxs-lookup"><span data-stu-id="f572b-153">Europe/Budapest</span></span>

<span data-ttu-id="f572b-154">Europe/Paris</span><span class="sxs-lookup"><span data-stu-id="f572b-154">Europe/Paris</span></span>

<span data-ttu-id="f572b-155">Europe/Warsaw</span><span class="sxs-lookup"><span data-stu-id="f572b-155">Europe/Warsaw</span></span>

<span data-ttu-id="f572b-156">Africa/Lagos</span><span class="sxs-lookup"><span data-stu-id="f572b-156">Africa/Lagos</span></span>

<span data-ttu-id="f572b-157">Africa/Windhoek</span><span class="sxs-lookup"><span data-stu-id="f572b-157">Africa/Windhoek</span></span>

<span data-ttu-id="f572b-158">Europe/Bucharest</span><span class="sxs-lookup"><span data-stu-id="f572b-158">Europe/Bucharest</span></span>

<span data-ttu-id="f572b-159">Asia/Beirut</span><span class="sxs-lookup"><span data-stu-id="f572b-159">Asia/Beirut</span></span>

<span data-ttu-id="f572b-160">Africa/Cairo</span><span class="sxs-lookup"><span data-stu-id="f572b-160">Africa/Cairo</span></span>

<span data-ttu-id="f572b-161">Asia/Damasco</span><span class="sxs-lookup"><span data-stu-id="f572b-161">Asia/Damascus</span></span>

<span data-ttu-id="f572b-162">Africa/Johannesburg</span><span class="sxs-lookup"><span data-stu-id="f572b-162">Africa/Johannesburg</span></span>

<span data-ttu-id="f572b-163">Europe/Kyiv (Kiev)</span><span class="sxs-lookup"><span data-stu-id="f572b-163">Europe/Kyiv (Kiev)</span></span>

<span data-ttu-id="f572b-164">Europe/Istanbul</span><span class="sxs-lookup"><span data-stu-id="f572b-164">Europe/Istanbul</span></span>

<span data-ttu-id="f572b-165">Asia/Jerusalem</span><span class="sxs-lookup"><span data-stu-id="f572b-165">Asia/Jerusalem</span></span>

<span data-ttu-id="f572b-166">Asia/Amman</span><span class="sxs-lookup"><span data-stu-id="f572b-166">Asia/Amman</span></span>

<span data-ttu-id="f572b-167">Asia/Baghdad</span><span class="sxs-lookup"><span data-stu-id="f572b-167">Asia/Baghdad</span></span>

<span data-ttu-id="f572b-168">Europe/Kaliningrad</span><span class="sxs-lookup"><span data-stu-id="f572b-168">Europe/Kaliningrad</span></span>

<span data-ttu-id="f572b-169">Asia/Riyadh</span><span class="sxs-lookup"><span data-stu-id="f572b-169">Asia/Riyadh</span></span>

<span data-ttu-id="f572b-170">Africa/Nairobi</span><span class="sxs-lookup"><span data-stu-id="f572b-170">Africa/Nairobi</span></span>

<span data-ttu-id="f572b-171">Asia/Tehran</span><span class="sxs-lookup"><span data-stu-id="f572b-171">Asia/Tehran</span></span>

<span data-ttu-id="f572b-172">Asia/Dubai</span><span class="sxs-lookup"><span data-stu-id="f572b-172">Asia/Dubai</span></span>

<span data-ttu-id="f572b-173">Asia/Baku</span><span class="sxs-lookup"><span data-stu-id="f572b-173">Asia/Baku</span></span>

<span data-ttu-id="f572b-174">Europe/Moscow</span><span class="sxs-lookup"><span data-stu-id="f572b-174">Europe/Moscow</span></span>

<span data-ttu-id="f572b-175">Indian/Mauritius</span><span class="sxs-lookup"><span data-stu-id="f572b-175">Indian/Mauritius</span></span>

<span data-ttu-id="f572b-176">Asia/Tbilisi</span><span class="sxs-lookup"><span data-stu-id="f572b-176">Asia/Tbilisi</span></span>

<span data-ttu-id="f572b-177">Asia/Yerevan</span><span class="sxs-lookup"><span data-stu-id="f572b-177">Asia/Yerevan</span></span>

<span data-ttu-id="f572b-178">Asia/Kabul</span><span class="sxs-lookup"><span data-stu-id="f572b-178">Asia/Kabul</span></span>

<span data-ttu-id="f572b-179">Asia/Karachi</span><span class="sxs-lookup"><span data-stu-id="f572b-179">Asia/Karachi</span></span>

<span data-ttu-id="f572b-180">Asia/Toshkent (Tashkent)</span><span class="sxs-lookup"><span data-stu-id="f572b-180">Asia/Toshkent (Tashkent)</span></span>

<span data-ttu-id="f572b-181">Asia/Kolkata</span><span class="sxs-lookup"><span data-stu-id="f572b-181">Asia/Kolkata</span></span>

<span data-ttu-id="f572b-182">Asia/Colombo</span><span class="sxs-lookup"><span data-stu-id="f572b-182">Asia/Colombo</span></span>

<span data-ttu-id="f572b-183">Asia/Kathmandu</span><span class="sxs-lookup"><span data-stu-id="f572b-183">Asia/Kathmandu</span></span>

<span data-ttu-id="f572b-184">Asia/Astana (Almaty)</span><span class="sxs-lookup"><span data-stu-id="f572b-184">Asia/Astana (Almaty)</span></span>

<span data-ttu-id="f572b-185">Asia/Dhaka</span><span class="sxs-lookup"><span data-stu-id="f572b-185">Asia/Dhaka</span></span>

<span data-ttu-id="f572b-186">Asia/Yekaterinburg</span><span class="sxs-lookup"><span data-stu-id="f572b-186">Asia/Yekaterinburg</span></span>

<span data-ttu-id="f572b-187">Asia/Yangon (Rangoon)</span><span class="sxs-lookup"><span data-stu-id="f572b-187">Asia/Yangon (Rangoon)</span></span>

<span data-ttu-id="f572b-188">Asia/Bangkok</span><span class="sxs-lookup"><span data-stu-id="f572b-188">Asia/Bangkok</span></span>

<span data-ttu-id="f572b-189">Asia/Novosibirsk</span><span class="sxs-lookup"><span data-stu-id="f572b-189">Asia/Novosibirsk</span></span>

<span data-ttu-id="f572b-190">Asia/Shanghai</span><span class="sxs-lookup"><span data-stu-id="f572b-190">Asia/Shanghai</span></span>

<span data-ttu-id="f572b-191">Asia/Krasnoyarsk</span><span class="sxs-lookup"><span data-stu-id="f572b-191">Asia/Krasnoyarsk</span></span>

<span data-ttu-id="f572b-192">Asia/Singapore</span><span class="sxs-lookup"><span data-stu-id="f572b-192">Asia/Singapore</span></span>

<span data-ttu-id="f572b-193">Australia/Perth</span><span class="sxs-lookup"><span data-stu-id="f572b-193">Australia/Perth</span></span>

<span data-ttu-id="f572b-194">Asia/Taipei</span><span class="sxs-lookup"><span data-stu-id="f572b-194">Asia/Taipei</span></span>

<span data-ttu-id="f572b-195">Asia/Ulaanbaatar</span><span class="sxs-lookup"><span data-stu-id="f572b-195">Asia/Ulaanbaatar</span></span>

<span data-ttu-id="f572b-196">Asia/Irkutsk</span><span class="sxs-lookup"><span data-stu-id="f572b-196">Asia/Irkutsk</span></span>

<span data-ttu-id="f572b-197">Asia/Tokyo</span><span class="sxs-lookup"><span data-stu-id="f572b-197">Asia/Tokyo</span></span>

<span data-ttu-id="f572b-198">Asia/Seoul</span><span class="sxs-lookup"><span data-stu-id="f572b-198">Asia/Seoul</span></span>

<span data-ttu-id="f572b-199">Australia/Adelaide</span><span class="sxs-lookup"><span data-stu-id="f572b-199">Australia/Adelaide</span></span>

<span data-ttu-id="f572b-200">Australia/Darwin</span><span class="sxs-lookup"><span data-stu-id="f572b-200">Australia/Darwin</span></span>

<span data-ttu-id="f572b-201">Australia/Brisbane</span><span class="sxs-lookup"><span data-stu-id="f572b-201">Australia/Brisbane</span></span>

<span data-ttu-id="f572b-202">Australia/Sydney</span><span class="sxs-lookup"><span data-stu-id="f572b-202">Australia/Sydney</span></span>

<span data-ttu-id="f572b-203">Pacific/Port_Moresby</span><span class="sxs-lookup"><span data-stu-id="f572b-203">Pacific/Port_Moresby</span></span>

<span data-ttu-id="f572b-204">Australia/Hobart</span><span class="sxs-lookup"><span data-stu-id="f572b-204">Australia/Hobart</span></span>

<span data-ttu-id="f572b-205">Asia/Yakutsk</span><span class="sxs-lookup"><span data-stu-id="f572b-205">Asia/Yakutsk</span></span>

<span data-ttu-id="f572b-206">Pacific/Guadalcanal</span><span class="sxs-lookup"><span data-stu-id="f572b-206">Pacific/Guadalcanal</span></span>

<span data-ttu-id="f572b-207">Asia/Vladivostok</span><span class="sxs-lookup"><span data-stu-id="f572b-207">Asia/Vladivostok</span></span>

<span data-ttu-id="f572b-208">Pacific/Auckland</span><span class="sxs-lookup"><span data-stu-id="f572b-208">Pacific/Auckland</span></span>

<span data-ttu-id="f572b-209">Etc/GMT-12</span><span class="sxs-lookup"><span data-stu-id="f572b-209">Etc/GMT-12</span></span>

<span data-ttu-id="f572b-210">Pacific/Fiji</span><span class="sxs-lookup"><span data-stu-id="f572b-210">Pacific/Fiji</span></span>

<span data-ttu-id="f572b-211">Asia/Magadan</span><span class="sxs-lookup"><span data-stu-id="f572b-211">Asia/Magadan</span></span>

<span data-ttu-id="f572b-212">Pacific/Tongatapu</span><span class="sxs-lookup"><span data-stu-id="f572b-212">Pacific/Tongatapu</span></span>

<span data-ttu-id="f572b-213">Pacific/Apia</span><span class="sxs-lookup"><span data-stu-id="f572b-213">Pacific/Apia</span></span>

<span data-ttu-id="f572b-214">Pacific/Kiritimati</span><span class="sxs-lookup"><span data-stu-id="f572b-214">Pacific/Kiritimati</span></span>

## <a name="json-representation"></a><span data-ttu-id="f572b-215">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f572b-215">JSON representation</span></span>

<span data-ttu-id="f572b-216">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f572b-216">Here is a JSON representation of the resource</span></span>

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
