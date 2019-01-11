---
title: tipo de recurso synchronizationStatus
description: Representa el estado actual de la synchronizationJob.
localization_priority: Normal
ms.openlocfilehash: 01f30338d7f6d4388554df08bf91655136c24a12
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817034"
---
# <a name="synchronizationstatus-resource-type"></a><span data-ttu-id="297b0-103">tipo de recurso synchronizationStatus</span><span class="sxs-lookup"><span data-stu-id="297b0-103">synchronizationStatus resource type</span></span>

> <span data-ttu-id="297b0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="297b0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="297b0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="297b0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="297b0-106">Representa el estado actual de la [synchronizationJob](synchronization-synchronizationjob.md).</span><span class="sxs-lookup"><span data-stu-id="297b0-106">Represents the current status of the [synchronizationJob](synchronization-synchronizationjob.md).</span></span>

## <a name="properties"></a><span data-ttu-id="297b0-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="297b0-107">Properties</span></span>

| <span data-ttu-id="297b0-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="297b0-108">Property</span></span>                              | <span data-ttu-id="297b0-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="297b0-109">Type</span></span>      | <span data-ttu-id="297b0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="297b0-110">Description</span></span>    |
|:--------------------------------------|:----------|:---------------|
|<span data-ttu-id="297b0-111">código</span><span class="sxs-lookup"><span data-stu-id="297b0-111">code</span></span>|<span data-ttu-id="297b0-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="297b0-112">String</span></span>|<span data-ttu-id="297b0-113">Código de estado de alto nivel del trabajo de sincronización.</span><span class="sxs-lookup"><span data-stu-id="297b0-113">High-level status code of the synchronization job.</span></span> <span data-ttu-id="297b0-114">Los valores posibles son: `NotConfigured`, `NotRun`, `Active`, `Paused` y `Quarantine`.</span><span class="sxs-lookup"><span data-stu-id="297b0-114">Possible values are: `NotConfigured`, `NotRun`, `Active`, `Paused`, `Quarantine`.</span></span>|
|<span data-ttu-id="297b0-115">countSuccessiveCompleteFailures</span><span class="sxs-lookup"><span data-stu-id="297b0-115">countSuccessiveCompleteFailures</span></span>|<span data-ttu-id="297b0-116">Int64</span><span class="sxs-lookup"><span data-stu-id="297b0-116">Int64</span></span>|<span data-ttu-id="297b0-117">Número de consecutivos veces este error del trabajo.</span><span class="sxs-lookup"><span data-stu-id="297b0-117">Number of consecutive times this job failed.</span></span>|
|<span data-ttu-id="297b0-118">escrowsPruned</span><span class="sxs-lookup"><span data-stu-id="297b0-118">escrowsPruned</span></span>|<span data-ttu-id="297b0-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="297b0-119">Boolean</span></span>|<span data-ttu-id="297b0-120">`true`Si se han eliminado depósitos de garantía del trabajo (errores de nivel de objeto) durante la sincronización inicial.</span><span class="sxs-lookup"><span data-stu-id="297b0-120">`true` if the job's escrows (object-level errors) were pruned during initial synchronization.</span></span> <span data-ttu-id="297b0-121">Si durante la sincronización inicial, alcanza el umbral de errores que normalmente se debería colocar el trabajo en cuarentena, se pueden eliminar depósitos de garantía.</span><span class="sxs-lookup"><span data-stu-id="297b0-121">Escrows can be pruned if during the initial synchronization, you reach the threshold of errors that would normally put the job in quarantine.</span></span> <span data-ttu-id="297b0-122">En lugar de entrar en cuarentena, el proceso de sincronización borra los errores del trabajo y continúa hasta que se complete la sincronización inicial.</span><span class="sxs-lookup"><span data-stu-id="297b0-122">Instead of going into quarantine, the synchronization process clears the job's errors and continues until the initial synchronization is completed.</span></span> <span data-ttu-id="297b0-123">Cuando se complete la sincronización inicial, el trabajo pausar y espere a que el cliente limpiar los errores.</span><span class="sxs-lookup"><span data-stu-id="297b0-123">When the initial synchronization is completed, the job will pause and wait for the customer to clean up the errors.</span></span>|
|<span data-ttu-id="297b0-124">lastExecution</span><span class="sxs-lookup"><span data-stu-id="297b0-124">lastExecution</span></span>|[<span data-ttu-id="297b0-125">synchronizationTaskExecution</span><span class="sxs-lookup"><span data-stu-id="297b0-125">synchronizationTaskExecution</span></span>](synchronization-synchronizationtaskexecution.md)|<span data-ttu-id="297b0-126">Detalles de la última ejecución del trabajo.</span><span class="sxs-lookup"><span data-stu-id="297b0-126">Details of the last execution of the job.</span></span>|
|<span data-ttu-id="297b0-127">lastSuccessfulExecution</span><span class="sxs-lookup"><span data-stu-id="297b0-127">lastSuccessfulExecution</span></span>|[<span data-ttu-id="297b0-128">synchronizationTaskExecution</span><span class="sxs-lookup"><span data-stu-id="297b0-128">synchronizationTaskExecution</span></span>](synchronization-synchronizationtaskexecution.md)|<span data-ttu-id="297b0-129">Detalles de la última ejecución de este trabajo, que no tiene errores.</span><span class="sxs-lookup"><span data-stu-id="297b0-129">Details of the last execution of this job, which didn't have any errors.</span></span>|
|<span data-ttu-id="297b0-130">lastSuccessfulExecutionWithExports</span><span class="sxs-lookup"><span data-stu-id="297b0-130">lastSuccessfulExecutionWithExports</span></span>|[<span data-ttu-id="297b0-131">synchronizationTaskExecution</span><span class="sxs-lookup"><span data-stu-id="297b0-131">synchronizationTaskExecution</span></span>](synchronization-synchronizationtaskexecution.md)|<span data-ttu-id="297b0-132">Detalles de la última ejecución del trabajo, que los objetos exportados en el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="297b0-132">Details of the last execution of the job, which exported objects into the target directory.</span></span>|
|<span data-ttu-id="297b0-133">progreso</span><span class="sxs-lookup"><span data-stu-id="297b0-133">progress</span></span>|<span data-ttu-id="297b0-134">colección de [synchronizationProgress](synchronization-synchronizationprogress.md)</span><span class="sxs-lookup"><span data-stu-id="297b0-134">[synchronizationProgress](synchronization-synchronizationprogress.md) collection</span></span>|<span data-ttu-id="297b0-135">Detalles del progreso de una tarea hasta su finalización.</span><span class="sxs-lookup"><span data-stu-id="297b0-135">Details of the progress of a job toward completion.</span></span>|
|<span data-ttu-id="297b0-136">cuarentena</span><span class="sxs-lookup"><span data-stu-id="297b0-136">quarantine</span></span>|[<span data-ttu-id="297b0-137">synchronizationQuarantine</span><span class="sxs-lookup"><span data-stu-id="297b0-137">synchronizationQuarantine</span></span>](synchronization-quarantine.md)|<span data-ttu-id="297b0-138">Si el trabajo está en cuarentena, detalles de cuarentena.</span><span class="sxs-lookup"><span data-stu-id="297b0-138">If job is in quarantine, quarantine details.</span></span>|
|<span data-ttu-id="297b0-139">steadyStateFirstAchievedTime</span><span class="sxs-lookup"><span data-stu-id="297b0-139">steadyStateFirstAchievedTime</span></span>|<span data-ttu-id="297b0-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="297b0-140">DateTimeOffset</span></span>|<span data-ttu-id="297b0-141">El tiempo cuando se ha conseguido en primer lugar estado estable (no hay más cambios en el proceso).</span><span class="sxs-lookup"><span data-stu-id="297b0-141">The time when steady state (no more changes to the process) was first achieved.</span></span> <span data-ttu-id="297b0-142">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="297b0-142">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="297b0-143">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="297b0-143">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="297b0-144">steadyStateLastAchievedTime</span><span class="sxs-lookup"><span data-stu-id="297b0-144">steadyStateLastAchievedTime</span></span>|<span data-ttu-id="297b0-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="297b0-145">DateTimeOffset</span></span>|<span data-ttu-id="297b0-146">El tiempo cuando se ha conseguido por última vez el estado estable (no hay más cambios en el proceso).</span><span class="sxs-lookup"><span data-stu-id="297b0-146">The time when steady state (no more changes to the process) was last achieved.</span></span> <span data-ttu-id="297b0-147">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="297b0-147">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="297b0-148">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="297b0-148">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="297b0-149">synchronizedEntryCountByType</span><span class="sxs-lookup"><span data-stu-id="297b0-149">synchronizedEntryCountByType</span></span>|<span data-ttu-id="297b0-150">colección de [stringKeyLongValuePair](synchronization-stringkeylongvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="297b0-150">[stringKeyLongValuePair](synchronization-stringkeylongvaluepair.md) collection</span></span>|<span data-ttu-id="297b0-151">Recuento de los objetos sincronizados, enumeradas por tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="297b0-151">Count of synchronized objects, listed by object type.</span></span>|
|<span data-ttu-id="297b0-152">troubleshootingUrl</span><span class="sxs-lookup"><span data-stu-id="297b0-152">troubleshootingUrl</span></span>|<span data-ttu-id="297b0-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="297b0-153">String</span></span>|<span data-ttu-id="297b0-154">En el caso de un error, la dirección URL con los pasos de solución de problemas para el problema.</span><span class="sxs-lookup"><span data-stu-id="297b0-154">In the event of an error, the URL with the troubleshooting steps for the issue.</span></span>|

### <a name="synchronization-status-code-details"></a><span data-ttu-id="297b0-155">Detalles del código de estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="297b0-155">Synchronization status code details</span></span>

| <span data-ttu-id="297b0-156">Valor</span><span class="sxs-lookup"><span data-stu-id="297b0-156">Value</span></span>                              | <span data-ttu-id="297b0-157">Description</span><span class="sxs-lookup"><span data-stu-id="297b0-157">Description</span></span>    |
|:-----------------------------------|:---------------|
|<span data-ttu-id="297b0-158">No configurado</span><span class="sxs-lookup"><span data-stu-id="297b0-158">NotConfigured</span></span>                       |<span data-ttu-id="297b0-159">Trabajo no configuró y nunca se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="297b0-159">Job was not configured and never run.</span></span> <span data-ttu-id="297b0-160">No hay autorización le ha proporcionado.</span><span class="sxs-lookup"><span data-stu-id="297b0-160">No authorization was provided.</span></span> |
|<span data-ttu-id="297b0-161">NotRun</span><span class="sxs-lookup"><span data-stu-id="297b0-161">NotRun</span></span>                              |<span data-ttu-id="297b0-162">Trabajo se ha configurado y, posiblemente, se ha iniciado, pero no ha completado su primera ejecución.</span><span class="sxs-lookup"><span data-stu-id="297b0-162">Job was configured, and possibly started, but hasn't completed its first run.</span></span>|
|<span data-ttu-id="297b0-163">Activo</span><span class="sxs-lookup"><span data-stu-id="297b0-163">Active</span></span>                              |<span data-ttu-id="297b0-164">Trabajo periódicamente se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="297b0-164">Job is running periodically.</span></span>|
|<span data-ttu-id="297b0-165">En pausa</span><span class="sxs-lookup"><span data-stu-id="297b0-165">Paused</span></span>                              |<span data-ttu-id="297b0-166">Trabajo se pausó (normalmente por un administrador) y actualmente no se está ejecutando, pero se conserva el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="297b0-166">Job was paused (usually by an administrator) and currently is not running, but the state of the job is preserved.</span></span>|
|<span data-ttu-id="297b0-167">Cuarentena</span><span class="sxs-lookup"><span data-stu-id="297b0-167">Quarantine</span></span>                          |<span data-ttu-id="297b0-168">El trabajo está en cuarentena.</span><span class="sxs-lookup"><span data-stu-id="297b0-168">Job is in quarantine.</span></span> <span data-ttu-id="297b0-169">Esto puede suceder cuando hay un gran volumen de errores o errores críticos, como las credenciales revocado o ha caducado.</span><span class="sxs-lookup"><span data-stu-id="297b0-169">This might happen when there is a high volume of errors, or critical errors such as revoked/expired credentials.</span></span> <span data-ttu-id="297b0-170">Mientras está en cuarentena, el proceso de sincronización se intentará ejecutar el trabajo con frecuencia reducida.</span><span class="sxs-lookup"><span data-stu-id="297b0-170">While in quarantine, the synchronization process will attempt to run the job with reduced frequency.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="297b0-171">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="297b0-171">JSON representation</span></span>

<span data-ttu-id="297b0-172">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="297b0-172">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationStatus"
}-->

```json
{
  "code": "String",
  "countSuccessiveCompleteFailures": 1024,
  "escrowsPruned": true,
  "lastExecution": {"@odata.type": "microsoft.graph.synchronizationTaskExecution"},
  "lastSuccessfulExecution": {"@odata.type": "microsoft.graph.synchronizationTaskExecution"},
  "lastSuccessfulExecutionWithExports": {"@odata.type": "microsoft.graph.synchronizationTaskExecution"},
  "progress": [{"@odata.type": "microsoft.graph.synchronizationProgress"}],
  "quarantine": {"@odata.type": "microsoft.graph.synchronizationQuarantine"},
  "steadyStateFirstAchievedTime": "String (timestamp)",
  "steadyStateLastAchievedTime": "String (timestamp)",
  "synchronizedEntryCountByType": [{"@odata.type": "microsoft.graph.stringKeyLongValuePair"}],
  "troubleshootingUrl": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationStatus resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
