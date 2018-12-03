---
title: tipo de recurso synchronizationJob
description: Realiza la sincronización por sondeo para que los cambios en un directorio y la inserción de ellos en otro directorio, periódicamente que se ejecuta en segundo plano. El trabajo de sincronización siempre es específico de una instancia determinada de una aplicación en el inquilino. Como parte de la configuración del trabajo de sincronización, debe conceder autorización para leer y escribir objetos en el directorio de destino y personalizar el esquema de sincronización de la tarea.
ms.openlocfilehash: 0e6428f2a088e5326f4412e743489c4d94b10296
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090579"
---
# <a name="synchronizationjob-resource-type"></a><span data-ttu-id="7d33c-105">tipo de recurso synchronizationJob</span><span class="sxs-lookup"><span data-stu-id="7d33c-105">synchronizationJob resource type</span></span>

> <span data-ttu-id="7d33c-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7d33c-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7d33c-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7d33c-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7d33c-108">Realiza la sincronización por sondeo para que los cambios en un directorio y la inserción de ellos en otro directorio, periódicamente que se ejecuta en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7d33c-108">Performs synchronization by periodically running in the background, polling for changes in one directory, and pushing them to another directory.</span></span> <span data-ttu-id="7d33c-109">El trabajo de sincronización siempre es específico de una instancia determinada de una aplicación en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="7d33c-109">The synchronization job is always specific to a particular instance of an application in your tenant.</span></span> <span data-ttu-id="7d33c-110">Como parte de la configuración del trabajo de sincronización, debe conceder autorización para leer y escribir objetos en el directorio de destino y personalizar el esquema de sincronización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="7d33c-110">As part of the synchronization job setup, you need to give authorization to read and write objects in your target directory, and customize the job's synchronization schema.</span></span>

## <a name="methods"></a><span data-ttu-id="7d33c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="7d33c-111">Methods</span></span>

| <span data-ttu-id="7d33c-112">Método</span><span class="sxs-lookup"><span data-stu-id="7d33c-112">Method</span></span>        | <span data-ttu-id="7d33c-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d33c-113">Return Type</span></span>               | <span data-ttu-id="7d33c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d33c-114">Description</span></span>                  |
|:--------------|:--------------------------|:-----------------------------|
|[<span data-ttu-id="7d33c-115">List</span><span class="sxs-lookup"><span data-stu-id="7d33c-115">List</span></span>](../api/synchronization-synchronizationjob-list.md)             |<span data-ttu-id="7d33c-116">colección de [synchronizationJob](synchronization-synchronizationjob.md)</span><span class="sxs-lookup"><span data-stu-id="7d33c-116">[synchronizationJob](synchronization-synchronizationjob.md) collection</span></span>  |<span data-ttu-id="7d33c-117">Lista de trabajos existentes para una instancia de aplicación determinada (entidad de seguridad de servicio).</span><span class="sxs-lookup"><span data-stu-id="7d33c-117">List existing jobs for a given application instance (service principal).</span></span>|
|[<span data-ttu-id="7d33c-118">Obtener synchronizationJob</span><span class="sxs-lookup"><span data-stu-id="7d33c-118">Get synchronizationJob</span></span>](../api/synchronization-synchronizationjob-get.md) | [<span data-ttu-id="7d33c-119">synchronizationJob</span><span class="sxs-lookup"><span data-stu-id="7d33c-119">synchronizationJob</span></span>](synchronization-synchronizationjob.md) |<span data-ttu-id="7d33c-120">Leer las propiedades y relaciones de un objeto synchronizationJob.</span><span class="sxs-lookup"><span data-stu-id="7d33c-120">Read properties and relationships of a synchronizationJob object.</span></span>|
|[<span data-ttu-id="7d33c-121">Create</span><span class="sxs-lookup"><span data-stu-id="7d33c-121">Create</span></span>](../api/synchronization-synchronizationjob-post.md)         |[<span data-ttu-id="7d33c-122">synchronizationJob</span><span class="sxs-lookup"><span data-stu-id="7d33c-122">synchronizationJob</span></span>](synchronization-synchronizationjob.md)   |<span data-ttu-id="7d33c-123">Crear nuevo trabajo de una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="7d33c-123">Create new job for a given application.</span></span>|
|[<span data-ttu-id="7d33c-124">Start</span><span class="sxs-lookup"><span data-stu-id="7d33c-124">Start</span></span>](../api/synchronization-synchronizationjob-start.md)          |<span data-ttu-id="7d33c-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7d33c-125">None</span></span>   |<span data-ttu-id="7d33c-126">Iniciar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="7d33c-126">Start synchronization.</span></span> <span data-ttu-id="7d33c-127">Si el trabajo está en un estado en pausa, continúa desde el punto donde se ha pausado el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7d33c-127">If the job is in a paused state, it continues from the point where the job was paused.</span></span> <span data-ttu-id="7d33c-128">Si el trabajo está en cuarentena, se borra el estado de la cuarentena.</span><span class="sxs-lookup"><span data-stu-id="7d33c-128">If the job is in quarantine, the quarantine status is cleared.</span></span>|
|[<span data-ttu-id="7d33c-129">Restart</span><span class="sxs-lookup"><span data-stu-id="7d33c-129">Restart</span></span>](../api/synchronization-synchronizationjob-restart.md)      |<span data-ttu-id="7d33c-130">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7d33c-130">None</span></span>   |<span data-ttu-id="7d33c-131">Forzar el trabajo para empezar de nuevo y volver a procesar todos los objetos en el directorio.</span><span class="sxs-lookup"><span data-stu-id="7d33c-131">Force the job to start over and re-process all the objects in the directory.</span></span>|
|[<span data-ttu-id="7d33c-132">Pause</span><span class="sxs-lookup"><span data-stu-id="7d33c-132">Pause</span></span>](../api/synchronization-synchronizationjob-pause.md)          |<span data-ttu-id="7d33c-133">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7d33c-133">None</span></span>   |<span data-ttu-id="7d33c-134">Detener temporalmente la sincronización.</span><span class="sxs-lookup"><span data-stu-id="7d33c-134">Temporarily stop synchronization.</span></span> <span data-ttu-id="7d33c-135">Se conserva el progreso, incluido el estado de trabajo, y el trabajo continuará desde donde la dejó cuando se realiza una llamada de [Inicio](../api/synchronization-synchronizationjob-start.md) .</span><span class="sxs-lookup"><span data-stu-id="7d33c-135">All the progress, including job state, is persisted, and the job will continue from where it left off when a [Start](../api/synchronization-synchronizationjob-start.md) call is made.</span></span>|
|[<span data-ttu-id="7d33c-136">Delete</span><span class="sxs-lookup"><span data-stu-id="7d33c-136">Delete</span></span>](../api/synchronization-synchronizationjob-delete.md)        |<span data-ttu-id="7d33c-137">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7d33c-137">None</span></span>   |<span data-ttu-id="7d33c-138">Detener la sincronización y eliminar de forma permanente todos los el estado asociado con el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7d33c-138">Stop synchronization, and permanently delete all the state associated with the job.</span></span>|
|[<span data-ttu-id="7d33c-139">Obtener synchrnoizationSchema</span><span class="sxs-lookup"><span data-stu-id="7d33c-139">Get synchrnoizationSchema</span></span>](../api/synchronization-synchronizationschema-get.md)    |[<span data-ttu-id="7d33c-140">synchronizationSchema</span><span class="sxs-lookup"><span data-stu-id="7d33c-140">synchronizationSchema</span></span>](synchronization-synchronizationschema.md)   |<span data-ttu-id="7d33c-141">Recuperar el esquema de sincronización eficaz del trabajo.</span><span class="sxs-lookup"><span data-stu-id="7d33c-141">Retrieve the job's effective synchronization schema.</span></span>|
|[<span data-ttu-id="7d33c-142">Actualizar synchroizationSchema</span><span class="sxs-lookup"><span data-stu-id="7d33c-142">Update synchroizationSchema</span></span>](../api/synchronization-synchronizationschema-update.md)    |<span data-ttu-id="7d33c-143">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7d33c-143">None</span></span>   |<span data-ttu-id="7d33c-144">Actualizar el esquema de sincronización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="7d33c-144">Update the job's synchronization schema.</span></span> |
|[<span data-ttu-id="7d33c-145">Validar credenciales</span><span class="sxs-lookup"><span data-stu-id="7d33c-145">Validate credentials</span></span>](../api/synchronization-synchronizationjob-validatecredentials.md)|<span data-ttu-id="7d33c-146">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7d33c-146">None</span></span>|<span data-ttu-id="7d33c-147">Pruebe las credenciales proporcionadas en el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="7d33c-147">Test provided credentials against target directory.</span></span>|

## <a name="properties"></a><span data-ttu-id="7d33c-148">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7d33c-148">Properties</span></span>

| <span data-ttu-id="7d33c-149">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7d33c-149">Property</span></span>      | <span data-ttu-id="7d33c-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d33c-150">Type</span></span>      | <span data-ttu-id="7d33c-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d33c-151">Description</span></span>    |
|:--------------|:----------|:---------------|
|<span data-ttu-id="7d33c-152">id</span><span class="sxs-lookup"><span data-stu-id="7d33c-152">id</span></span>             |<span data-ttu-id="7d33c-153">String</span><span class="sxs-lookup"><span data-stu-id="7d33c-153">String</span></span>                     |<span data-ttu-id="7d33c-154">Identificador de trabajo de sincronización únicas.</span><span class="sxs-lookup"><span data-stu-id="7d33c-154">Unique synchronization job identifier.</span></span> <span data-ttu-id="7d33c-155">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7d33c-155">Read-only.</span></span>|
|<span data-ttu-id="7d33c-156">programación</span><span class="sxs-lookup"><span data-stu-id="7d33c-156">schedule</span></span>       |[<span data-ttu-id="7d33c-157">synchronizationSchedule</span><span class="sxs-lookup"><span data-stu-id="7d33c-157">synchronizationSchedule</span></span>](synchronization-synchronizationschedule.md)|<span data-ttu-id="7d33c-158">Programación que se usa para ejecutar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7d33c-158">Schedule used to run the job.</span></span> <span data-ttu-id="7d33c-159">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7d33c-159">Read-only.</span></span>|
|<span data-ttu-id="7d33c-160">status</span><span class="sxs-lookup"><span data-stu-id="7d33c-160">status</span></span>         |[<span data-ttu-id="7d33c-161">synchronizationStatus</span><span class="sxs-lookup"><span data-stu-id="7d33c-161">synchronizationStatus</span></span>](synchronization-synchronizationstatus.md)     |<span data-ttu-id="7d33c-162">Estado del trabajo, que incluye cuando se ejecutó el trabajo por última vez, el estado actual del trabajo y los errores.</span><span class="sxs-lookup"><span data-stu-id="7d33c-162">Status of the job, which includes when the job was last run, current job state, and errors.</span></span>|
|<span data-ttu-id="7d33c-163">templateId</span><span class="sxs-lookup"><span data-stu-id="7d33c-163">templateId</span></span>     |<span data-ttu-id="7d33c-164">String</span><span class="sxs-lookup"><span data-stu-id="7d33c-164">String</span></span>    |<span data-ttu-id="7d33c-165">Identificador de la [plantilla de sincronización](synchronization-synchronizationtemplate.md) de en que este trabajo se basa.</span><span class="sxs-lookup"><span data-stu-id="7d33c-165">Identifier of the [synchronization template](synchronization-synchronizationtemplate.md) this job is based on.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7d33c-166">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7d33c-166">Relationships</span></span>
| <span data-ttu-id="7d33c-167">Relación</span><span class="sxs-lookup"><span data-stu-id="7d33c-167">Relationship</span></span> | <span data-ttu-id="7d33c-168">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d33c-168">Type</span></span>   |<span data-ttu-id="7d33c-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d33c-169">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7d33c-170">esquema</span><span class="sxs-lookup"><span data-stu-id="7d33c-170">schema</span></span>|[<span data-ttu-id="7d33c-171">synchronizationSchema</span><span class="sxs-lookup"><span data-stu-id="7d33c-171">synchronizationSchema</span></span>](synchronization-synchronizationschema.md)| <span data-ttu-id="7d33c-172">El esquema de sincronización configurado para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7d33c-172">The synchronization schema configured for the job.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7d33c-173">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7d33c-173">JSON representation</span></span>

<span data-ttu-id="7d33c-174">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7d33c-174">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationJob"
}-->

```json
{
  "id": "String (identifier)",
  "schedule": {"@odata.type": "microsoft.graph.synchronizationSchedule"},
  "status": {"@odata.type": "microsoft.graph.synchronizationStatus"},
  "templateId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationJob resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->