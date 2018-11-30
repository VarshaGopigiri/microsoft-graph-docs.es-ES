---
title: tipo de recurso synchronizationTaskExecution
description: Resuma los resultados de la ejecución del trabajo de sincronización.
ms.openlocfilehash: 4aefba4bdf9ab850892344e6e34683e81d1a1afa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086913"
---
# <a name="synchronizationtaskexecution-resource-type"></a><span data-ttu-id="a62b2-103">tipo de recurso synchronizationTaskExecution</span><span class="sxs-lookup"><span data-stu-id="a62b2-103">synchronizationTaskExecution resource type</span></span>

> <span data-ttu-id="a62b2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a62b2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a62b2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a62b2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a62b2-106">Resuma los resultados de la ejecución del trabajo de sincronización.</span><span class="sxs-lookup"><span data-stu-id="a62b2-106">Summarizes the results of the synchronization job run.</span></span>

## <a name="properties"></a><span data-ttu-id="a62b2-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a62b2-107">Properties</span></span>
| <span data-ttu-id="a62b2-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a62b2-108">Property</span></span>     | <span data-ttu-id="a62b2-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a62b2-109">Type</span></span>   |<span data-ttu-id="a62b2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a62b2-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a62b2-111">activityIdentifier</span><span class="sxs-lookup"><span data-stu-id="a62b2-111">activityIdentifier</span></span>           |<span data-ttu-id="a62b2-112">String</span><span class="sxs-lookup"><span data-stu-id="a62b2-112">String</span></span> |<span data-ttu-id="a62b2-113">Identificador de la ejecución del trabajo.</span><span class="sxs-lookup"><span data-stu-id="a62b2-113">Identifier of the job run.</span></span>|
|<span data-ttu-id="a62b2-114">countEntitled</span><span class="sxs-lookup"><span data-stu-id="a62b2-114">countEntitled</span></span>                |<span data-ttu-id="a62b2-115">Int64</span><span class="sxs-lookup"><span data-stu-id="a62b2-115">Int64</span></span>  |<span data-ttu-id="a62b2-116">Recuento de procesado entradas que se han asignado a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="a62b2-116">Count of processed entries that were assigned for this application.</span></span>|
|<span data-ttu-id="a62b2-117">countEntitledForProvisioning</span><span class="sxs-lookup"><span data-stu-id="a62b2-117">countEntitledForProvisioning</span></span> |<span data-ttu-id="a62b2-118">Int64</span><span class="sxs-lookup"><span data-stu-id="a62b2-118">Int64</span></span>  |<span data-ttu-id="a62b2-119">Recuento de procesado entradas que se han asignado para el aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="a62b2-119">Count of processed entries that were assigned for provisioning.</span></span>|
|<span data-ttu-id="a62b2-120">countEscrowed</span><span class="sxs-lookup"><span data-stu-id="a62b2-120">countEscrowed</span></span>                |<span data-ttu-id="a62b2-121">Int64</span><span class="sxs-lookup"><span data-stu-id="a62b2-121">Int64</span></span>  |<span data-ttu-id="a62b2-122">Número de entradas que se han custodiadas (errores).</span><span class="sxs-lookup"><span data-stu-id="a62b2-122">Count of entries that were escrowed (errors).</span></span>|
|<span data-ttu-id="a62b2-123">countEscrowedRaw</span><span class="sxs-lookup"><span data-stu-id="a62b2-123">countEscrowedRaw</span></span>             |<span data-ttu-id="a62b2-124">Int64</span><span class="sxs-lookup"><span data-stu-id="a62b2-124">Int64</span></span>  |<span data-ttu-id="a62b2-125">Recuento de las entradas que se han custodiadas, incluidos los depósitos de garantía generados por el sistema.</span><span class="sxs-lookup"><span data-stu-id="a62b2-125">Count of entries that were escrowed, including system-generated escrows.</span></span>|
|<span data-ttu-id="a62b2-126">countExported</span><span class="sxs-lookup"><span data-stu-id="a62b2-126">countExported</span></span>                |<span data-ttu-id="a62b2-127">Int64</span><span class="sxs-lookup"><span data-stu-id="a62b2-127">Int64</span></span>  |<span data-ttu-id="a62b2-128">Recuento de movimientos exportados.</span><span class="sxs-lookup"><span data-stu-id="a62b2-128">Count of exported entries.</span></span>|
|<span data-ttu-id="a62b2-129">countExports</span><span class="sxs-lookup"><span data-stu-id="a62b2-129">countExports</span></span>                 |<span data-ttu-id="a62b2-130">Int64</span><span class="sxs-lookup"><span data-stu-id="a62b2-130">Int64</span></span>  |<span data-ttu-id="a62b2-131">Recuento de las entradas que se esperaban que se va a exportar.</span><span class="sxs-lookup"><span data-stu-id="a62b2-131">Count of entries that were expected to be exported.</span></span>|
|<span data-ttu-id="a62b2-132">countImported</span><span class="sxs-lookup"><span data-stu-id="a62b2-132">countImported</span></span>                |<span data-ttu-id="a62b2-133">Int64</span><span class="sxs-lookup"><span data-stu-id="a62b2-133">Int64</span></span>  |<span data-ttu-id="a62b2-134">Número de entradas importadas.</span><span class="sxs-lookup"><span data-stu-id="a62b2-134">Count of imported entries.</span></span>|
|<span data-ttu-id="a62b2-135">countImportedDeltas</span><span class="sxs-lookup"><span data-stu-id="a62b2-135">countImportedDeltas</span></span>          |<span data-ttu-id="a62b2-136">Int64</span><span class="sxs-lookup"><span data-stu-id="a62b2-136">Int64</span></span>  |<span data-ttu-id="a62b2-137">Número de cambios de delta importados.</span><span class="sxs-lookup"><span data-stu-id="a62b2-137">Count of imported delta-changes.</span></span>|
|<span data-ttu-id="a62b2-138">countImportedReferenceDeltas</span><span class="sxs-lookup"><span data-stu-id="a62b2-138">countImportedReferenceDeltas</span></span> |<span data-ttu-id="a62b2-139">Int64</span><span class="sxs-lookup"><span data-stu-id="a62b2-139">Int64</span></span>  |<span data-ttu-id="a62b2-140">Recuento de cambios delta importados relativas a los cambios de referencia.</span><span class="sxs-lookup"><span data-stu-id="a62b2-140">Count of imported delta-changes pertaining to reference changes.</span></span>|
|<span data-ttu-id="a62b2-141">error</span><span class="sxs-lookup"><span data-stu-id="a62b2-141">error</span></span>                        |[<span data-ttu-id="a62b2-142">synchronizationError</span><span class="sxs-lookup"><span data-stu-id="a62b2-142">synchronizationError</span></span>](synchronization-synchronizationerror.md)|<span data-ttu-id="a62b2-143">Si se ha encontrado un error, contiene un objeto **synchronizationError** con detalles.</span><span class="sxs-lookup"><span data-stu-id="a62b2-143">If an error was encountered, contains a **synchronizationError** object with details.</span></span>|
|<span data-ttu-id="a62b2-144">estado</span><span class="sxs-lookup"><span data-stu-id="a62b2-144">state</span></span>                        |<span data-ttu-id="a62b2-145">String</span><span class="sxs-lookup"><span data-stu-id="a62b2-145">String</span></span> |<span data-ttu-id="a62b2-146">Resumir los resultados de esta ejecución de código.</span><span class="sxs-lookup"><span data-stu-id="a62b2-146">Code summarizing the result of this run.</span></span> <span data-ttu-id="a62b2-147">Los valores posibles son: `Succeeded`, `Failed` y `EntryLevelErrors`.</span><span class="sxs-lookup"><span data-stu-id="a62b2-147">Possible values are: `Succeeded`, `Failed`, `EntryLevelErrors`.</span></span>|
|<span data-ttu-id="a62b2-148">timeBegan</span><span class="sxs-lookup"><span data-stu-id="a62b2-148">timeBegan</span></span>                    |<span data-ttu-id="a62b2-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a62b2-149">DateTimeOffset</span></span>|<span data-ttu-id="a62b2-150">Empezó a tiempo cuando se ejecuta este trabajo.</span><span class="sxs-lookup"><span data-stu-id="a62b2-150">Time when this job run began.</span></span> <span data-ttu-id="a62b2-151">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="a62b2-151">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="a62b2-152">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="a62b2-152">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="a62b2-153">timeEnded</span><span class="sxs-lookup"><span data-stu-id="a62b2-153">timeEnded</span></span>                    |<span data-ttu-id="a62b2-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a62b2-154">DateTimeOffset</span></span>|<span data-ttu-id="a62b2-155">Finalizó el tiempo cuando se ejecuta este trabajo.</span><span class="sxs-lookup"><span data-stu-id="a62b2-155">Time when this job run ended.</span></span> <span data-ttu-id="a62b2-156">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="a62b2-156">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="a62b2-157">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="a62b2-157">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a62b2-158">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a62b2-158">JSON representation</span></span>

<span data-ttu-id="a62b2-159">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a62b2-159">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationTaskExecution"
}-->

```json
{
  "activityIdentifier": "String",
  "countEntitled": 1024,
  "countEntitledForProvisioning": 1024,
  "countEscrowed": 1024,
  "countEscrowedRaw": 1024,
  "countExported": 1024,
  "countExports": 1024,
  "countImported": 1024,
  "countImportedDeltas": 1024,
  "countImportedReferenceDeltas": 1024,
  "error": {"@odata.type": "microsoft.graph.synchronizationError"},
  "state": "String",
  "timeBegan": "String (timestamp)",
  "timeEnded": "String (timestamp)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationTaskExecution resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->