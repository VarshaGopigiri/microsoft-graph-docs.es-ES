---
title: tipo de recurso privilegedRoleSummary
description: Las estadísticas de resumen para un rol determinado.
ms.openlocfilehash: f6c66433651eff188ce6fdaa07c2422d3bb6e0ce
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089654"
---
# <a name="privilegedrolesummary-resource-type"></a><span data-ttu-id="8ec86-103">tipo de recurso privilegedRoleSummary</span><span class="sxs-lookup"><span data-stu-id="8ec86-103">privilegedRoleSummary resource type</span></span>

> <span data-ttu-id="8ec86-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8ec86-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8ec86-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8ec86-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8ec86-106">Las estadísticas de resumen para un rol determinado.</span><span class="sxs-lookup"><span data-stu-id="8ec86-106">The statistics summary for a particular role.</span></span>


## <a name="methods"></a><span data-ttu-id="8ec86-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="8ec86-107">Methods</span></span>

| <span data-ttu-id="8ec86-108">Método</span><span class="sxs-lookup"><span data-stu-id="8ec86-108">Method</span></span>           | <span data-ttu-id="8ec86-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ec86-109">Return Type</span></span>    |<span data-ttu-id="8ec86-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ec86-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="8ec86-111">Obtener privilegedRoleSummary</span><span class="sxs-lookup"><span data-stu-id="8ec86-111">Get privilegedRoleSummary</span></span>](../api/privilegedrolesummary-get.md) | [<span data-ttu-id="8ec86-112">privilegedRoleSummary</span><span class="sxs-lookup"><span data-stu-id="8ec86-112">privilegedRoleSummary</span></span>](privilegedrolesummary.md) |<span data-ttu-id="8ec86-113">Leer las propiedades y las relaciones del objeto privilegedRoleSummary.</span><span class="sxs-lookup"><span data-stu-id="8ec86-113">Read properties and relationships of privilegedRoleSummary object.</span></span>|

## <a name="properties"></a><span data-ttu-id="8ec86-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8ec86-114">Properties</span></span>
| <span data-ttu-id="8ec86-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8ec86-115">Property</span></span>     | <span data-ttu-id="8ec86-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ec86-116">Type</span></span>   |<span data-ttu-id="8ec86-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ec86-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8ec86-118">elevatedCount</span><span class="sxs-lookup"><span data-stu-id="8ec86-118">elevatedCount</span></span>|<span data-ttu-id="8ec86-119">int32</span><span class="sxs-lookup"><span data-stu-id="8ec86-119">int32</span></span>|<span data-ttu-id="8ec86-120">El número de usuarios que tienen el rol asignado y la función está activado.</span><span class="sxs-lookup"><span data-stu-id="8ec86-120">The number of users that have the role assigned and the role is activated.</span></span>|
|<span data-ttu-id="8ec86-121">id</span><span class="sxs-lookup"><span data-stu-id="8ec86-121">id</span></span>|<span data-ttu-id="8ec86-122">string</span><span class="sxs-lookup"><span data-stu-id="8ec86-122">string</span></span>| <span data-ttu-id="8ec86-123">El identificador único para el rol.</span><span class="sxs-lookup"><span data-stu-id="8ec86-123">The unique identifier for the role.</span></span> <span data-ttu-id="8ec86-124">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8ec86-124">Read-only.</span></span>|
|<span data-ttu-id="8ec86-125">managedCount</span><span class="sxs-lookup"><span data-stu-id="8ec86-125">managedCount</span></span>|<span data-ttu-id="8ec86-126">int32</span><span class="sxs-lookup"><span data-stu-id="8ec86-126">int32</span></span>|<span data-ttu-id="8ec86-127">El número de usuarios que tienen el rol asignado, pero la función se desactiva.</span><span class="sxs-lookup"><span data-stu-id="8ec86-127">The number of users that have the role assigned but the role is deactivated.</span></span>|
|<span data-ttu-id="8ec86-128">mfaEnabled</span><span class="sxs-lookup"><span data-stu-id="8ec86-128">mfaEnabled</span></span>|<span data-ttu-id="8ec86-129">boolean</span><span class="sxs-lookup"><span data-stu-id="8ec86-129">boolean</span></span>|<span data-ttu-id="8ec86-130">**true** si la activación de la función requiere MFA.</span><span class="sxs-lookup"><span data-stu-id="8ec86-130">**true** if the role activation requires MFA.</span></span> <span data-ttu-id="8ec86-131">**false** si la activación de la función no requiere MFA.</span><span class="sxs-lookup"><span data-stu-id="8ec86-131">**false** if the role activation doesn't require MFA.</span></span>|
|<span data-ttu-id="8ec86-132">status</span><span class="sxs-lookup"><span data-stu-id="8ec86-132">status</span></span>|<span data-ttu-id="8ec86-133">string</span><span class="sxs-lookup"><span data-stu-id="8ec86-133">string</span></span>| <span data-ttu-id="8ec86-134">Los valores posibles son: `ok` y `bad`.</span><span class="sxs-lookup"><span data-stu-id="8ec86-134">Possible values are: `ok`, `bad`.</span></span> <span data-ttu-id="8ec86-135">El valor depende de la relación entre (managedCount / usersCount).</span><span class="sxs-lookup"><span data-stu-id="8ec86-135">The value depends on the ratio of (managedCount / usersCount).</span></span> <span data-ttu-id="8ec86-136">Si la proporción es menor que un umbral predefinido, `ok` se devuelve.</span><span class="sxs-lookup"><span data-stu-id="8ec86-136">If the ratio is less than a predefined threshold, `ok` is returned.</span></span> <span data-ttu-id="8ec86-137">De lo contrario, `bad` se devuelve.</span><span class="sxs-lookup"><span data-stu-id="8ec86-137">Otherwise, `bad` is returned.</span></span>|
|<span data-ttu-id="8ec86-138">usersCount</span><span class="sxs-lookup"><span data-stu-id="8ec86-138">usersCount</span></span>|<span data-ttu-id="8ec86-139">int32</span><span class="sxs-lookup"><span data-stu-id="8ec86-139">int32</span></span>|<span data-ttu-id="8ec86-140">El número de usuarios que están asignados a la función.</span><span class="sxs-lookup"><span data-stu-id="8ec86-140">The number of users that are assigned with the role.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8ec86-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8ec86-141">Relationships</span></span>
<span data-ttu-id="8ec86-142">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8ec86-142">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="8ec86-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8ec86-143">JSON representation</span></span>

<span data-ttu-id="8ec86-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8ec86-144">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedRoleSummary"
}-->

```json
{
  "elevatedCount": 1024,
  "id": "string (identifier)",
  "managedCount": 1024,
  "mfaEnabled": true,
  "status": "string",
  "usersCount": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRoleSummary resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->