---
title: tipo de recurso secureScores
description: 'parte superior = n, donde n = número de días de datos que desea recuperar. '
localization_priority: Normal
ms.openlocfilehash: 332a9656d8237bb07d5c7739b666e09539cf984f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828738"
---
# <a name="securescores-resource-type"></a><span data-ttu-id="b59d6-103">tipo de recurso secureScores</span><span class="sxs-lookup"><span data-stu-id="b59d6-103">secureScores resource type</span></span>

> <span data-ttu-id="b59d6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b59d6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b59d6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b59d6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b59d6-106">Representa la puntuación de seguro de un inquilino por día de los resultados de datos, en el nivel de inquilino y control.</span><span class="sxs-lookup"><span data-stu-id="b59d6-106">Represents a tenant's secure score per day of scoring data, at the tenant and control level.</span></span> <span data-ttu-id="b59d6-107">De forma predeterminada, se mantiene 90 días de datos.</span><span class="sxs-lookup"><span data-stu-id="b59d6-107">By default, 90 days of data is held.</span></span> <span data-ttu-id="b59d6-108">Estos datos se ordenan por **createdDateTime**, de más reciente a más próxima.</span><span class="sxs-lookup"><span data-stu-id="b59d6-108">This data is sorted by **createdDateTime**, from latest to earliest.</span></span> <span data-ttu-id="b59d6-109">Esto le permitirá a las respuestas de la página mediante el uso de $top = n, donde n = número de días de datos que desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="b59d6-109">This will allow you to page responses by using $top=n, where n = the number of days of data that you want to retrieve.</span></span> 


## <a name="methods"></a><span data-ttu-id="b59d6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b59d6-110">Methods</span></span>

| <span data-ttu-id="b59d6-111">Método</span><span class="sxs-lookup"><span data-stu-id="b59d6-111">Method</span></span>   | <span data-ttu-id="b59d6-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b59d6-112">Return Type</span></span>|<span data-ttu-id="b59d6-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b59d6-113">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="b59d6-114">Lista secureScores</span><span class="sxs-lookup"><span data-stu-id="b59d6-114">List secureScores</span></span>](../api/securescores-list.md) | [<span data-ttu-id="b59d6-115">secureScores</span><span class="sxs-lookup"><span data-stu-id="b59d6-115">secureScores</span></span>](securescores.md) |<span data-ttu-id="b59d6-116">Lea las propiedades y los metadatos de un objeto secureScores.</span><span class="sxs-lookup"><span data-stu-id="b59d6-116">Read properties and metadata of a secureScores object.</span></span>|


## <a name="properties"></a><span data-ttu-id="b59d6-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b59d6-117">Properties</span></span>
<span data-ttu-id="b59d6-118">Que contiene propiedades de tipo de entidad de la seguridad del inquilino puntuación (datos de instantánea diaria).</span><span class="sxs-lookup"><span data-stu-id="b59d6-118">Entity type containing properties of the tenant security score (daily snapshot data).</span></span>

|<span data-ttu-id="b59d6-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b59d6-119">Property</span></span> |<span data-ttu-id="b59d6-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="b59d6-120">Type</span></span> |<span data-ttu-id="b59d6-121">Description</span><span class="sxs-lookup"><span data-stu-id="b59d6-121">Description</span></span> |
|:--|:--|:--|
|   <span data-ttu-id="b59d6-122">azureTenantId</span><span class="sxs-lookup"><span data-stu-id="b59d6-122">azureTenantId</span></span>   |   <span data-ttu-id="b59d6-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="b59d6-123">String</span></span>  |   <span data-ttu-id="b59d6-124">Identificador de cadena GUID para el inquilino.</span><span class="sxs-lookup"><span data-stu-id="b59d6-124">GUID string for tenant ID.</span></span>  |
|   <span data-ttu-id="b59d6-125">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b59d6-125">createdDateTime</span></span> |   <span data-ttu-id="b59d6-126">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b59d6-126">DateTimeOffset</span></span>  |   <span data-ttu-id="b59d6-127">La fecha cuando se crea la entidad.</span><span class="sxs-lookup"><span data-stu-id="b59d6-127">The date when the entity is created.</span></span>  |
|   <span data-ttu-id="b59d6-128">id</span><span class="sxs-lookup"><span data-stu-id="b59d6-128">id</span></span>  |   <span data-ttu-id="b59d6-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="b59d6-129">String</span></span>  |   <span data-ttu-id="b59d6-130">Combinación de azureTenantId_createdDateTime.</span><span class="sxs-lookup"><span data-stu-id="b59d6-130">Combination of azureTenantId_createdDateTime.</span></span>   |
|   <span data-ttu-id="b59d6-131">licensedUserCount</span><span class="sxs-lookup"><span data-stu-id="b59d6-131">licensedUserCount</span></span>   |   <span data-ttu-id="b59d6-132">Int32</span><span class="sxs-lookup"><span data-stu-id="b59d6-132">Int32</span></span>   |   <span data-ttu-id="b59d6-133">Con una licencia de recuento de usuarios del inquilino determinado.</span><span class="sxs-lookup"><span data-stu-id="b59d6-133">Licensed user count of the given tenant.</span></span>    |
|   <span data-ttu-id="b59d6-134">activeUserCount</span><span class="sxs-lookup"><span data-stu-id="b59d6-134">activeUserCount</span></span> |   <span data-ttu-id="b59d6-135">Int32</span><span class="sxs-lookup"><span data-stu-id="b59d6-135">Int32</span></span>   |   <span data-ttu-id="b59d6-136">Recuento de usuario activo del inquilino determinado.</span><span class="sxs-lookup"><span data-stu-id="b59d6-136">Active user count of the given tenant.</span></span>  |
|   <span data-ttu-id="b59d6-137">currentScore</span><span class="sxs-lookup"><span data-stu-id="b59d6-137">currentScore</span></span>    |   <span data-ttu-id="b59d6-138">Doble</span><span class="sxs-lookup"><span data-stu-id="b59d6-138">Double</span></span>  |   <span data-ttu-id="b59d6-139">Puntuación actual del inquilino alcanzado en la fecha especificada.</span><span class="sxs-lookup"><span data-stu-id="b59d6-139">Tenant current attained score on specified date.</span></span>    |
|   <span data-ttu-id="b59d6-140">maxScore</span><span class="sxs-lookup"><span data-stu-id="b59d6-140">maxScore</span></span> |  <span data-ttu-id="b59d6-141">Doble</span><span class="sxs-lookup"><span data-stu-id="b59d6-141">Double</span></span>  |   <span data-ttu-id="b59d6-142">Inquilino máxima puntuación posible en la fecha especificada.</span><span class="sxs-lookup"><span data-stu-id="b59d6-142">Tenant maximum possible score on specified date.</span></span>    |
|   <span data-ttu-id="b59d6-143">enabledServices</span><span class="sxs-lookup"><span data-stu-id="b59d6-143">enabledServices</span></span> |   <span data-ttu-id="b59d6-144">Colección String</span><span class="sxs-lookup"><span data-stu-id="b59d6-144">String collection</span></span>   |   <span data-ttu-id="b59d6-145">Servicios proporcionados por Microsoft para el inquilino (por ejemplo, Exchange online, Skype, Sharepoint).</span><span class="sxs-lookup"><span data-stu-id="b59d6-145">Microsoft-provided services for the tenant (for example, Exchange online, Skype, Sharepoint).</span></span>   |
|   <span data-ttu-id="b59d6-146">averageComparativeScores</span><span class="sxs-lookup"><span data-stu-id="b59d6-146">averageComparativeScores</span></span> |  <span data-ttu-id="b59d6-147">colección de [averageComparativeScore](averagecomparativescore.md)</span><span class="sxs-lookup"><span data-stu-id="b59d6-147">[averageComparativeScore](averagecomparativescore.md) collection</span></span>    |<span data-ttu-id="b59d6-148">Promedio de la puntuación por distintos ámbitos (por ejemplo, promedio según el sector, promedio por asiento) y categoría de control (identidad, datos, dispositivos, aplicaciones, infraestructura) dentro del ámbito.</span><span class="sxs-lookup"><span data-stu-id="b59d6-148">Average score by different scopes (for example, average by industry, average by seating) and control category (Identity, Data, Device, Apps, Infrastructure) within the scope.</span></span> |
|   <span data-ttu-id="b59d6-149">controlScores</span><span class="sxs-lookup"><span data-stu-id="b59d6-149">controlScores</span></span> | <span data-ttu-id="b59d6-150">colección de [controlScore](controlscore.md)</span><span class="sxs-lookup"><span data-stu-id="b59d6-150">[controlScore](controlscore.md) collection</span></span>  |   <span data-ttu-id="b59d6-151">Contiene las puntuaciones del inquilino para un conjunto de controles.</span><span class="sxs-lookup"><span data-stu-id="b59d6-151">Contains tenant scores for a set of controls.</span></span>   |


## <a name="relationships"></a><span data-ttu-id="b59d6-152">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b59d6-152">Relationships</span></span>

<span data-ttu-id="b59d6-153">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b59d6-153">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b59d6-154">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b59d6-154">JSON representation</span></span>

<span data-ttu-id="b59d6-155">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b59d6-155">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.secureScores"
}-->

```json
{
"id": "String",
"azureTenantId": "Guid",
"createdDate": "DateTimeOffset",
"licensedUserCount": "Int32",
"activeUserCount": "Int32",
"currentScore": "Int32",
"maxScore": "Int32",
"averageScore": "Double",
"enabledServices": "Collection(string)",
"averageComparativeScores": "Collection(microsoft.graph.SecureScore.averageComparativeScores)",
"controlScores": "Collection(microsoft.graph.SecureScore.controlScores)",
}

```


<!-- {
  "type": "#page.annotation",
  "description": "secureScores resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
