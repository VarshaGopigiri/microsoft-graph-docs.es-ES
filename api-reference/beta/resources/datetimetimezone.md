---
title: Tipo de recurso dateTimeTimeZone
description: Describe la fecha, la hora y la zona horaria de un momento dado.
ms.openlocfilehash: a95ebf35d6a47b8b39c34cab8d6d35b92eaae2c3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085670"
---
# <a name="datetimetimezone-resource-type"></a><span data-ttu-id="0b2c7-103">Tipo de recurso dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="0b2c7-103">dateTimeTimeZone resource type</span></span>

> <span data-ttu-id="0b2c7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0b2c7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0b2c7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0b2c7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0b2c7-106">Describe la fecha, la hora y la zona horaria de un momento dado.</span><span class="sxs-lookup"><span data-stu-id="0b2c7-106">Describes the date, time, and time zone of a point in time.</span></span>

## <a name="properties"></a><span data-ttu-id="0b2c7-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b2c7-107">Properties</span></span>
| <span data-ttu-id="0b2c7-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0b2c7-108">Property</span></span>     | <span data-ttu-id="0b2c7-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b2c7-109">Type</span></span>   |<span data-ttu-id="0b2c7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b2c7-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0b2c7-111">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b2c7-111">DateTime</span></span>|<span data-ttu-id="0b2c7-112">String</span><span class="sxs-lookup"><span data-stu-id="0b2c7-112">String</span></span>|<span data-ttu-id="0b2c7-113">Un único momento dado en una fecha combinada y la representación de tiempo (`<date>T<time>`).</span><span class="sxs-lookup"><span data-stu-id="0b2c7-113">A single point of time in a combined date and time representation (`<date>T<time>`).</span></span>|
|<span data-ttu-id="0b2c7-114">TimeZone</span><span class="sxs-lookup"><span data-stu-id="0b2c7-114">TimeZone</span></span>|<span data-ttu-id="0b2c7-115">String</span><span class="sxs-lookup"><span data-stu-id="0b2c7-115">String</span></span>|<span data-ttu-id="0b2c7-116">Uno de los siguientes nombres de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="0b2c7-116">One of the following time zone names.</span></span>|

<span data-ttu-id="0b2c7-117">La propiedad _TimeZone_ puede establecerse en cualquiera de las zonas horarias compatibles con Windows, así como los nombres de zona horaria siguientes.</span><span class="sxs-lookup"><span data-stu-id="0b2c7-117">The _TimeZone_ property can be set to any of the time zones supported by Windows, as well as the following time zones names.</span></span>

<span data-ttu-id="0b2c7-118">Etc/GMT+12</span><span class="sxs-lookup"><span data-stu-id="0b2c7-118">Etc/GMT+12</span></span>

<span data-ttu-id="0b2c7-119">Etc/GMT+11</span><span class="sxs-lookup"><span data-stu-id="0b2c7-119">Etc/GMT+11</span></span>

<span data-ttu-id="0b2c7-120">Pacific/Honolulu</span><span class="sxs-lookup"><span data-stu-id="0b2c7-120">Pacific/Honolulu</span></span>

<span data-ttu-id="0b2c7-121">America/Anchorage</span><span class="sxs-lookup"><span data-stu-id="0b2c7-121">America/Anchorage</span></span>

<span data-ttu-id="0b2c7-122">America/Santa_Isabel</span><span class="sxs-lookup"><span data-stu-id="0b2c7-122">America/Santa_Isabel</span></span>

<span data-ttu-id="0b2c7-123">America/Los_Angeles</span><span class="sxs-lookup"><span data-stu-id="0b2c7-123">America/Los_Angeles</span></span>

<span data-ttu-id="0b2c7-124">America/Phoenix</span><span class="sxs-lookup"><span data-stu-id="0b2c7-124">America/Phoenix</span></span>

<span data-ttu-id="0b2c7-125">America/Chihuahua</span><span class="sxs-lookup"><span data-stu-id="0b2c7-125">America/Chihuahua</span></span>

<span data-ttu-id="0b2c7-126">America/Denver</span><span class="sxs-lookup"><span data-stu-id="0b2c7-126">America/Denver</span></span>

<span data-ttu-id="0b2c7-127">America/Guatemala</span><span class="sxs-lookup"><span data-stu-id="0b2c7-127">America/Guatemala</span></span>

<span data-ttu-id="0b2c7-128">America/Chicago</span><span class="sxs-lookup"><span data-stu-id="0b2c7-128">America/Chicago</span></span>

<span data-ttu-id="0b2c7-129">America/Mexico_City</span><span class="sxs-lookup"><span data-stu-id="0b2c7-129">America/Mexico_City</span></span>

<span data-ttu-id="0b2c7-130">America/Regina</span><span class="sxs-lookup"><span data-stu-id="0b2c7-130">America/Regina</span></span>

<span data-ttu-id="0b2c7-131">America/Bogota</span><span class="sxs-lookup"><span data-stu-id="0b2c7-131">America/Bogota</span></span>

<span data-ttu-id="0b2c7-132">America/New_York</span><span class="sxs-lookup"><span data-stu-id="0b2c7-132">America/New_York</span></span>

<span data-ttu-id="0b2c7-133">America/Indiana/Indianapolis</span><span class="sxs-lookup"><span data-stu-id="0b2c7-133">America/Indiana/Indianapolis</span></span>

<span data-ttu-id="0b2c7-134">America/Caracas</span><span class="sxs-lookup"><span data-stu-id="0b2c7-134">America/Caracas</span></span>

<span data-ttu-id="0b2c7-135">America/Asuncion</span><span class="sxs-lookup"><span data-stu-id="0b2c7-135">America/Asuncion</span></span>

<span data-ttu-id="0b2c7-136">America/Halifax</span><span class="sxs-lookup"><span data-stu-id="0b2c7-136">America/Halifax</span></span>

<span data-ttu-id="0b2c7-137">America/Cuiaba</span><span class="sxs-lookup"><span data-stu-id="0b2c7-137">America/Cuiaba</span></span>

<span data-ttu-id="0b2c7-138">America/La_Paz</span><span class="sxs-lookup"><span data-stu-id="0b2c7-138">America/La_Paz</span></span>

<span data-ttu-id="0b2c7-139">America/Santiago</span><span class="sxs-lookup"><span data-stu-id="0b2c7-139">America/Santiago</span></span>

<span data-ttu-id="0b2c7-140">America/St_Johns</span><span class="sxs-lookup"><span data-stu-id="0b2c7-140">America/St_Johns</span></span>

<span data-ttu-id="0b2c7-141">America/Sao_Paulo</span><span class="sxs-lookup"><span data-stu-id="0b2c7-141">America/Sao_Paulo</span></span>

<span data-ttu-id="0b2c7-142">America/Argentina/Buenos_Aires</span><span class="sxs-lookup"><span data-stu-id="0b2c7-142">America/Argentina/Buenos_Aires</span></span>

<span data-ttu-id="0b2c7-143">America/Cayenne</span><span class="sxs-lookup"><span data-stu-id="0b2c7-143">America/Cayenne</span></span>

<span data-ttu-id="0b2c7-144">America/Godthab</span><span class="sxs-lookup"><span data-stu-id="0b2c7-144">America/Godthab</span></span>

<span data-ttu-id="0b2c7-145">America/Montevideo</span><span class="sxs-lookup"><span data-stu-id="0b2c7-145">America/Montevideo</span></span>

<span data-ttu-id="0b2c7-146">America/Bahia</span><span class="sxs-lookup"><span data-stu-id="0b2c7-146">America/Bahia</span></span>

<span data-ttu-id="0b2c7-147">Etc/GMT+2</span><span class="sxs-lookup"><span data-stu-id="0b2c7-147">Etc/GMT+2</span></span>

<span data-ttu-id="0b2c7-148">Atlantic/Azores</span><span class="sxs-lookup"><span data-stu-id="0b2c7-148">Atlantic/Azores</span></span>

<span data-ttu-id="0b2c7-149">Atlantic/Cape_Verde</span><span class="sxs-lookup"><span data-stu-id="0b2c7-149">Atlantic/Cape_Verde</span></span>

<span data-ttu-id="0b2c7-150">Africa/Casablanca</span><span class="sxs-lookup"><span data-stu-id="0b2c7-150">Africa/Casablanca</span></span>

<span data-ttu-id="0b2c7-151">Etc/GMT</span><span class="sxs-lookup"><span data-stu-id="0b2c7-151">Etc/GMT</span></span>

<span data-ttu-id="0b2c7-152">Europe/London</span><span class="sxs-lookup"><span data-stu-id="0b2c7-152">Europe/London</span></span>

<span data-ttu-id="0b2c7-153">Atlantic/Reykjavik</span><span class="sxs-lookup"><span data-stu-id="0b2c7-153">Atlantic/Reykjavik</span></span>

<span data-ttu-id="0b2c7-154">Europe/Berlin</span><span class="sxs-lookup"><span data-stu-id="0b2c7-154">Europe/Berlin</span></span>

<span data-ttu-id="0b2c7-155">Europe/Budapest</span><span class="sxs-lookup"><span data-stu-id="0b2c7-155">Europe/Budapest</span></span>

<span data-ttu-id="0b2c7-156">Europe/Paris</span><span class="sxs-lookup"><span data-stu-id="0b2c7-156">Europe/Paris</span></span>

<span data-ttu-id="0b2c7-157">Europe/Warsaw</span><span class="sxs-lookup"><span data-stu-id="0b2c7-157">Europe/Warsaw</span></span>

<span data-ttu-id="0b2c7-158">Africa/Lagos</span><span class="sxs-lookup"><span data-stu-id="0b2c7-158">Africa/Lagos</span></span>

<span data-ttu-id="0b2c7-159">Africa/Windhoek</span><span class="sxs-lookup"><span data-stu-id="0b2c7-159">Africa/Windhoek</span></span>

<span data-ttu-id="0b2c7-160">Europe/Bucharest</span><span class="sxs-lookup"><span data-stu-id="0b2c7-160">Europe/Bucharest</span></span>

<span data-ttu-id="0b2c7-161">Asia/Beirut</span><span class="sxs-lookup"><span data-stu-id="0b2c7-161">Asia/Beirut</span></span>

<span data-ttu-id="0b2c7-162">Africa/Cairo</span><span class="sxs-lookup"><span data-stu-id="0b2c7-162">Africa/Cairo</span></span>

<span data-ttu-id="0b2c7-163">Asia/Damasco</span><span class="sxs-lookup"><span data-stu-id="0b2c7-163">Asia/Damascus</span></span>

<span data-ttu-id="0b2c7-164">Africa/Johannesburg</span><span class="sxs-lookup"><span data-stu-id="0b2c7-164">Africa/Johannesburg</span></span>

<span data-ttu-id="0b2c7-165">Europe/Kyiv (Kiev)</span><span class="sxs-lookup"><span data-stu-id="0b2c7-165">Europe/Kyiv (Kiev)</span></span>

<span data-ttu-id="0b2c7-166">Europe/Istanbul</span><span class="sxs-lookup"><span data-stu-id="0b2c7-166">Europe/Istanbul</span></span>

<span data-ttu-id="0b2c7-167">Asia/Jerusalem</span><span class="sxs-lookup"><span data-stu-id="0b2c7-167">Asia/Jerusalem</span></span>

<span data-ttu-id="0b2c7-168">Asia/Amman</span><span class="sxs-lookup"><span data-stu-id="0b2c7-168">Asia/Amman</span></span>

<span data-ttu-id="0b2c7-169">Asia/Baghdad</span><span class="sxs-lookup"><span data-stu-id="0b2c7-169">Asia/Baghdad</span></span>

<span data-ttu-id="0b2c7-170">Europe/Kaliningrad</span><span class="sxs-lookup"><span data-stu-id="0b2c7-170">Europe/Kaliningrad</span></span>

<span data-ttu-id="0b2c7-171">Asia/Riyadh</span><span class="sxs-lookup"><span data-stu-id="0b2c7-171">Asia/Riyadh</span></span>

<span data-ttu-id="0b2c7-172">Africa/Nairobi</span><span class="sxs-lookup"><span data-stu-id="0b2c7-172">Africa/Nairobi</span></span>

<span data-ttu-id="0b2c7-173">Asia/Tehran</span><span class="sxs-lookup"><span data-stu-id="0b2c7-173">Asia/Tehran</span></span>

<span data-ttu-id="0b2c7-174">Asia/Dubai</span><span class="sxs-lookup"><span data-stu-id="0b2c7-174">Asia/Dubai</span></span>

<span data-ttu-id="0b2c7-175">Asia/Baku</span><span class="sxs-lookup"><span data-stu-id="0b2c7-175">Asia/Baku</span></span>

<span data-ttu-id="0b2c7-176">Europe/Moscow</span><span class="sxs-lookup"><span data-stu-id="0b2c7-176">Europe/Moscow</span></span>

<span data-ttu-id="0b2c7-177">Indian/Mauritius</span><span class="sxs-lookup"><span data-stu-id="0b2c7-177">Indian/Mauritius</span></span>

<span data-ttu-id="0b2c7-178">Asia/Tbilisi</span><span class="sxs-lookup"><span data-stu-id="0b2c7-178">Asia/Tbilisi</span></span>

<span data-ttu-id="0b2c7-179">Asia/Yerevan</span><span class="sxs-lookup"><span data-stu-id="0b2c7-179">Asia/Yerevan</span></span>

<span data-ttu-id="0b2c7-180">Asia/Kabul</span><span class="sxs-lookup"><span data-stu-id="0b2c7-180">Asia/Kabul</span></span>

<span data-ttu-id="0b2c7-181">Asia/Karachi</span><span class="sxs-lookup"><span data-stu-id="0b2c7-181">Asia/Karachi</span></span>

<span data-ttu-id="0b2c7-182">Asia/Toshkent (Tashkent)</span><span class="sxs-lookup"><span data-stu-id="0b2c7-182">Asia/Toshkent (Tashkent)</span></span>

<span data-ttu-id="0b2c7-183">Asia/Kolkata</span><span class="sxs-lookup"><span data-stu-id="0b2c7-183">Asia/Kolkata</span></span>

<span data-ttu-id="0b2c7-184">Asia/Colombo</span><span class="sxs-lookup"><span data-stu-id="0b2c7-184">Asia/Colombo</span></span>

<span data-ttu-id="0b2c7-185">Asia/Kathmandu</span><span class="sxs-lookup"><span data-stu-id="0b2c7-185">Asia/Kathmandu</span></span>

<span data-ttu-id="0b2c7-186">Asia/Astana (Almaty)</span><span class="sxs-lookup"><span data-stu-id="0b2c7-186">Asia/Astana (Almaty)</span></span>

<span data-ttu-id="0b2c7-187">Asia/Dhaka</span><span class="sxs-lookup"><span data-stu-id="0b2c7-187">Asia/Dhaka</span></span>

<span data-ttu-id="0b2c7-188">Asia/Yekaterinburg</span><span class="sxs-lookup"><span data-stu-id="0b2c7-188">Asia/Yekaterinburg</span></span>

<span data-ttu-id="0b2c7-189">Asia/Yangon (Rangoon)</span><span class="sxs-lookup"><span data-stu-id="0b2c7-189">Asia/Yangon (Rangoon)</span></span>

<span data-ttu-id="0b2c7-190">Asia/Bangkok</span><span class="sxs-lookup"><span data-stu-id="0b2c7-190">Asia/Bangkok</span></span>

<span data-ttu-id="0b2c7-191">Asia/Novosibirsk</span><span class="sxs-lookup"><span data-stu-id="0b2c7-191">Asia/Novosibirsk</span></span>

<span data-ttu-id="0b2c7-192">Asia/Shanghai</span><span class="sxs-lookup"><span data-stu-id="0b2c7-192">Asia/Shanghai</span></span>

<span data-ttu-id="0b2c7-193">Asia/Krasnoyarsk</span><span class="sxs-lookup"><span data-stu-id="0b2c7-193">Asia/Krasnoyarsk</span></span>

<span data-ttu-id="0b2c7-194">Asia/Singapore</span><span class="sxs-lookup"><span data-stu-id="0b2c7-194">Asia/Singapore</span></span>

<span data-ttu-id="0b2c7-195">Australia/Perth</span><span class="sxs-lookup"><span data-stu-id="0b2c7-195">Australia/Perth</span></span>

<span data-ttu-id="0b2c7-196">Asia/Taipei</span><span class="sxs-lookup"><span data-stu-id="0b2c7-196">Asia/Taipei</span></span>

<span data-ttu-id="0b2c7-197">Asia/Ulaanbaatar</span><span class="sxs-lookup"><span data-stu-id="0b2c7-197">Asia/Ulaanbaatar</span></span>

<span data-ttu-id="0b2c7-198">Asia/Irkutsk</span><span class="sxs-lookup"><span data-stu-id="0b2c7-198">Asia/Irkutsk</span></span>

<span data-ttu-id="0b2c7-199">Asia/Tokyo</span><span class="sxs-lookup"><span data-stu-id="0b2c7-199">Asia/Tokyo</span></span>

<span data-ttu-id="0b2c7-200">Asia/Seoul</span><span class="sxs-lookup"><span data-stu-id="0b2c7-200">Asia/Seoul</span></span>

<span data-ttu-id="0b2c7-201">Australia/Adelaide</span><span class="sxs-lookup"><span data-stu-id="0b2c7-201">Australia/Adelaide</span></span>

<span data-ttu-id="0b2c7-202">Australia/Darwin</span><span class="sxs-lookup"><span data-stu-id="0b2c7-202">Australia/Darwin</span></span>

<span data-ttu-id="0b2c7-203">Australia/Brisbane</span><span class="sxs-lookup"><span data-stu-id="0b2c7-203">Australia/Brisbane</span></span>

<span data-ttu-id="0b2c7-204">Australia/Sydney</span><span class="sxs-lookup"><span data-stu-id="0b2c7-204">Australia/Sydney</span></span>

<span data-ttu-id="0b2c7-205">Pacific/Port_Moresby</span><span class="sxs-lookup"><span data-stu-id="0b2c7-205">Pacific/Port_Moresby</span></span>

<span data-ttu-id="0b2c7-206">Australia/Hobart</span><span class="sxs-lookup"><span data-stu-id="0b2c7-206">Australia/Hobart</span></span>

<span data-ttu-id="0b2c7-207">Asia/Yakutsk</span><span class="sxs-lookup"><span data-stu-id="0b2c7-207">Asia/Yakutsk</span></span>

<span data-ttu-id="0b2c7-208">Pacific/Guadalcanal</span><span class="sxs-lookup"><span data-stu-id="0b2c7-208">Pacific/Guadalcanal</span></span>

<span data-ttu-id="0b2c7-209">Asia/Vladivostok</span><span class="sxs-lookup"><span data-stu-id="0b2c7-209">Asia/Vladivostok</span></span>

<span data-ttu-id="0b2c7-210">Pacific/Auckland</span><span class="sxs-lookup"><span data-stu-id="0b2c7-210">Pacific/Auckland</span></span>

<span data-ttu-id="0b2c7-211">Etc/GMT-12</span><span class="sxs-lookup"><span data-stu-id="0b2c7-211">Etc/GMT-12</span></span>

<span data-ttu-id="0b2c7-212">Pacific/Fiji</span><span class="sxs-lookup"><span data-stu-id="0b2c7-212">Pacific/Fiji</span></span>

<span data-ttu-id="0b2c7-213">Asia/Magadan</span><span class="sxs-lookup"><span data-stu-id="0b2c7-213">Asia/Magadan</span></span>

<span data-ttu-id="0b2c7-214">Pacific/Tongatapu</span><span class="sxs-lookup"><span data-stu-id="0b2c7-214">Pacific/Tongatapu</span></span>

<span data-ttu-id="0b2c7-215">Pacific/Apia</span><span class="sxs-lookup"><span data-stu-id="0b2c7-215">Pacific/Apia</span></span>

<span data-ttu-id="0b2c7-216">Pacific/Kiritimati</span><span class="sxs-lookup"><span data-stu-id="0b2c7-216">Pacific/Kiritimati</span></span>

## <a name="json-representation"></a><span data-ttu-id="0b2c7-217">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0b2c7-217">JSON representation</span></span>

<span data-ttu-id="0b2c7-218">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0b2c7-218">Here is a JSON representation of the resource</span></span>

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
