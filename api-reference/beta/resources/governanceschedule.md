---
title: tipo de recurso governanceSchedule
description: 'Representa la programación de un governanceRoleAssignmentRequest. Para una solicitud de asignación de rol, la programación controla cuándo se debe realizar la operación de asignación de rol, cuándo se debe detener la asignación de roles y la frecuencia con que realizar la operación de asignación de rol. '
ms.openlocfilehash: 6eff3977aa7806c975f968b8706f2e8c21e5d99e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088205"
---
# <a name="governanceschedule-resource-type"></a><span data-ttu-id="65584-104">tipo de recurso governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="65584-104">governanceSchedule resource type</span></span>

> <span data-ttu-id="65584-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="65584-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="65584-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="65584-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="65584-107">Representa la programación de un [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span><span class="sxs-lookup"><span data-stu-id="65584-107">Represents the schedule for a [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span></span> <span data-ttu-id="65584-108">Para una solicitud de asignación de rol, la programación controla cuándo se debe realizar la operación de asignación de rol, cuándo se debe detener la asignación de roles y la frecuencia con que realizar la operación de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="65584-108">For a role assignment request, the schedule controls when to perform the role assignment operation, when to stop the role assignment, and how frequently to do the role assignment operation.</span></span> 



## <a name="properties"></a><span data-ttu-id="65584-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65584-109">Properties</span></span>
| <span data-ttu-id="65584-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="65584-110">Property</span></span>     | <span data-ttu-id="65584-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="65584-111">Type</span></span>   |<span data-ttu-id="65584-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="65584-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="65584-113">startDateTime</span><span class="sxs-lookup"><span data-stu-id="65584-113">startDateTime</span></span>|<span data-ttu-id="65584-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="65584-114">DateTimeOffset</span></span>|<span data-ttu-id="65584-115">La hora de inicio de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="65584-115">The start time of the role assignment.</span></span> <span data-ttu-id="65584-116">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="65584-116">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="65584-117">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="65584-117">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="65584-118">endDateTime</span><span class="sxs-lookup"><span data-stu-id="65584-118">endDateTime</span></span>|<span data-ttu-id="65584-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="65584-119">DateTimeOffset</span></span>|<span data-ttu-id="65584-120">La hora de finalización de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="65584-120">The end time of the role assignment.</span></span> <span data-ttu-id="65584-121">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="65584-121">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="65584-122">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="65584-122">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span> <span data-ttu-id="65584-123">*Nota: si el valor es `null`, indica una asignación permanente.*</span><span class="sxs-lookup"><span data-stu-id="65584-123">*Note: if the value is `null`, it indicates a permanent assignment.*</span></span>|
|<span data-ttu-id="65584-124">type</span><span class="sxs-lookup"><span data-stu-id="65584-124">type</span></span>|<span data-ttu-id="65584-125">String</span><span class="sxs-lookup"><span data-stu-id="65584-125">String</span></span>|<span data-ttu-id="65584-126">Tipo de programación de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="65584-126">The role assignment schedule type.</span></span> <span data-ttu-id="65584-127">Sólo `Once` es compatible con este momento.</span><span class="sxs-lookup"><span data-stu-id="65584-127">Only `Once` is supported for now.</span></span>
|<span data-ttu-id="65584-128">duration</span><span class="sxs-lookup"><span data-stu-id="65584-128">duration</span></span>|<span data-ttu-id="65584-129">Duración</span><span class="sxs-lookup"><span data-stu-id="65584-129">Duration</span></span>|<span data-ttu-id="65584-130">La duración de una asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="65584-130">The duration of a role assignment.</span></span> <span data-ttu-id="65584-131">Está en formato de un objeto TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="65584-131">It is in format of a TimeSpan.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="65584-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="65584-132">JSON representation</span></span>

<span data-ttu-id="65584-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="65584-133">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceSchedule"
}-->

```json
{
  "duration": "String (timespan)",
  "startDateTime": "String (timestamp)",
  "endDateTime": "String (timestamp)",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceSchedule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
