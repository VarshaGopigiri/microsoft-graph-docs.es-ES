---
title: tipo de recurso de proceso
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 2e60c9e008ccfddaa0bcc3e78c27cc17c65a3844
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086378"
---
# <a name="process-resource-type"></a><span data-ttu-id="c0403-104">tipo de recurso de proceso</span><span class="sxs-lookup"><span data-stu-id="c0403-104">process resource type</span></span>

 > <span data-ttu-id="c0403-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c0403-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c0403-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c0403-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c0403-107">Contiene información de estado acerca del proceso de relacionados con la alerta.</span><span class="sxs-lookup"><span data-stu-id="c0403-107">Contains stateful information about the process related to the alert.</span></span>

## <a name="properties"></a><span data-ttu-id="c0403-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c0403-108">Properties</span></span>

| <span data-ttu-id="c0403-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c0403-109">Property</span></span>   | <span data-ttu-id="c0403-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0403-110">Type</span></span>|<span data-ttu-id="c0403-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0403-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c0403-112">accountName</span><span class="sxs-lookup"><span data-stu-id="c0403-112">accountName</span></span>|<span data-ttu-id="c0403-113">String</span><span class="sxs-lookup"><span data-stu-id="c0403-113">String</span></span>|<span data-ttu-id="c0403-114">Identificador (se ejecutó el proceso en el contexto de cuenta de usuario) de cuenta de usuario por ejemplo, AccountName, SID y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="c0403-114">User account identifier (user account context the process ran under) for example, AccountName, SID, and so on.</span></span>|
|<span data-ttu-id="c0403-115">commandLine</span><span class="sxs-lookup"><span data-stu-id="c0403-115">commandLine</span></span>|<span data-ttu-id="c0403-116">String</span><span class="sxs-lookup"><span data-stu-id="c0403-116">String</span></span>|<span data-ttu-id="c0403-117">La línea de comandos de invocación de proceso completo incluyendo todos los parámetros.</span><span class="sxs-lookup"><span data-stu-id="c0403-117">The full process invocation commandline including all parameters.</span></span>|
|<span data-ttu-id="c0403-118">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c0403-118">createdDateTime</span></span>|<span data-ttu-id="c0403-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c0403-119">DateTimeOffset</span></span>|<span data-ttu-id="c0403-120">Hora a la que se inició el proceso.</span><span class="sxs-lookup"><span data-stu-id="c0403-120">Time at which the process was started.</span></span> <span data-ttu-id="c0403-121">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="c0403-121">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="c0403-122">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="c0403-122">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="c0403-123">fileHash</span><span class="sxs-lookup"><span data-stu-id="c0403-123">fileHash</span></span>|[<span data-ttu-id="c0403-124">fileHash</span><span class="sxs-lookup"><span data-stu-id="c0403-124">fileHash</span></span>](filehash.md)|<span data-ttu-id="c0403-125">Tipo complejo que contiene los valores de hash de archivo (criptográficas y la ubicación).</span><span class="sxs-lookup"><span data-stu-id="c0403-125">Complex type containing file hashes (cryptographic and location-sensitive).</span></span>|
|<span data-ttu-id="c0403-126">integrityLevel</span><span class="sxs-lookup"><span data-stu-id="c0403-126">integrityLevel</span></span>|<span data-ttu-id="c0403-127">processIntegrityLevel</span><span class="sxs-lookup"><span data-stu-id="c0403-127">processIntegrityLevel</span></span>|<span data-ttu-id="c0403-128">El nivel de la integridad del proceso.</span><span class="sxs-lookup"><span data-stu-id="c0403-128">The integrity level of the process.</span></span> <span data-ttu-id="c0403-129">Los valores posibles son: `unknown`, `untrusted`, `low`, `medium`, `high`, `system`.</span><span class="sxs-lookup"><span data-stu-id="c0403-129">Possible values are: `unknown`, `untrusted`, `low`, `medium`, `high`, `system`.</span></span>|
|<span data-ttu-id="c0403-130">isElevated</span><span class="sxs-lookup"><span data-stu-id="c0403-130">isElevated</span></span>|<span data-ttu-id="c0403-131">Booleano</span><span class="sxs-lookup"><span data-stu-id="c0403-131">Boolean</span></span>|<span data-ttu-id="c0403-132">Es True si el proceso es un elevado.</span><span class="sxs-lookup"><span data-stu-id="c0403-132">True if the process is elevated.</span></span>|
|<span data-ttu-id="c0403-133">name</span><span class="sxs-lookup"><span data-stu-id="c0403-133">name</span></span>|<span data-ttu-id="c0403-134">String</span><span class="sxs-lookup"><span data-stu-id="c0403-134">String</span></span>|<span data-ttu-id="c0403-135">El nombre de archivo de imagen del proceso.</span><span class="sxs-lookup"><span data-stu-id="c0403-135">The name of the process' Image file.</span></span>|
|<span data-ttu-id="c0403-136">parentProcessCreatedDateTime</span><span class="sxs-lookup"><span data-stu-id="c0403-136">parentProcessCreatedDateTime</span></span>|<span data-ttu-id="c0403-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c0403-137">DateTimeOffset</span></span>|<span data-ttu-id="c0403-138">Fecha y hora en que se inició el proceso primario.</span><span class="sxs-lookup"><span data-stu-id="c0403-138">DateTime at which the parent process was started.</span></span> <span data-ttu-id="c0403-139">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="c0403-139">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="c0403-140">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="c0403-140">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="c0403-141">parentProcessId</span><span class="sxs-lookup"><span data-stu-id="c0403-141">parentProcessId</span></span>|<span data-ttu-id="c0403-142">Int32</span><span class="sxs-lookup"><span data-stu-id="c0403-142">Int32</span></span>|<span data-ttu-id="c0403-143">El proceso de identificador (PID) del proceso principal.</span><span class="sxs-lookup"><span data-stu-id="c0403-143">The Process ID (PID) of the parent process.</span></span>|
|<span data-ttu-id="c0403-144">parentProcessName</span><span class="sxs-lookup"><span data-stu-id="c0403-144">parentProcessName</span></span>|<span data-ttu-id="c0403-145">String</span><span class="sxs-lookup"><span data-stu-id="c0403-145">String</span></span>|<span data-ttu-id="c0403-146">El nombre del archivo de imagen del proceso principal.</span><span class="sxs-lookup"><span data-stu-id="c0403-146">The name of the image file of the parent process.</span></span>|
|<span data-ttu-id="c0403-147">ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="c0403-147">path</span></span>|<span data-ttu-id="c0403-148">String</span><span class="sxs-lookup"><span data-stu-id="c0403-148">String</span></span>|<span data-ttu-id="c0403-149">Ruta de acceso completa, incluido el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="c0403-149">Full path, including filename.</span></span>|
|<span data-ttu-id="c0403-150">processId</span><span class="sxs-lookup"><span data-stu-id="c0403-150">processId</span></span>|<span data-ttu-id="c0403-151">Int32</span><span class="sxs-lookup"><span data-stu-id="c0403-151">Int32</span></span>|<span data-ttu-id="c0403-152">El proceso de identificador (PID) del proceso.</span><span class="sxs-lookup"><span data-stu-id="c0403-152">The Process ID (PID) of the process.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c0403-153">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c0403-153">JSON representation</span></span>

<span data-ttu-id="c0403-154">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="c0403-154">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.process"
}-->

```json
{
  "accountName": "String",
  "commandLine": "String",
  "createdDateTime": "String (timestamp)",
  "fileHash": {"@odata.type": "microsoft.graph.fileHash"},
  "integrityLevel": "@odata.type: microsoft.graph.processIntegrityLevel",
  "isElevated": true,
  "name": "String",
  "parentProcessCreatedDateTime": "String (timestamp)",
  "parentProcessId": 1024,
  "parentProcessName": "String",
  "path": "String",
  "processId": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "process resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->