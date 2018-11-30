---
title: tipo de recurso de proceso
description: Contiene información de estado acerca del proceso de relacionados con la alerta.
ms.openlocfilehash: 67bc65cfa47cda877578d89aa20c4e34b3a0c501
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031524"
---
# <a name="process-resource-type"></a><span data-ttu-id="1d37c-103">tipo de recurso de proceso</span><span class="sxs-lookup"><span data-stu-id="1d37c-103">process resource type</span></span>

<span data-ttu-id="1d37c-104">Contiene información de estado acerca del proceso de relacionados con la alerta.</span><span class="sxs-lookup"><span data-stu-id="1d37c-104">Contains stateful information about the process related to the alert.</span></span>

## <a name="properties"></a><span data-ttu-id="1d37c-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d37c-105">Properties</span></span>

| <span data-ttu-id="1d37c-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1d37c-106">Property</span></span>   | <span data-ttu-id="1d37c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d37c-107">Type</span></span>|<span data-ttu-id="1d37c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d37c-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1d37c-109">accountName</span><span class="sxs-lookup"><span data-stu-id="1d37c-109">accountName</span></span>|<span data-ttu-id="1d37c-110">String</span><span class="sxs-lookup"><span data-stu-id="1d37c-110">String</span></span>|<span data-ttu-id="1d37c-111">Identificador (se ejecutó el proceso en el contexto de cuenta de usuario) de cuenta de usuario por ejemplo, AccountName, SID y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="1d37c-111">User account identifier (user account context the process ran under) for example, AccountName, SID, and so on.</span></span>|
|<span data-ttu-id="1d37c-112">commandLine</span><span class="sxs-lookup"><span data-stu-id="1d37c-112">commandLine</span></span>|<span data-ttu-id="1d37c-113">String</span><span class="sxs-lookup"><span data-stu-id="1d37c-113">String</span></span>|<span data-ttu-id="1d37c-114">La línea de comandos de invocación de proceso completo incluyendo todos los parámetros.</span><span class="sxs-lookup"><span data-stu-id="1d37c-114">The full process invocation commandline including all parameters.</span></span>|
|<span data-ttu-id="1d37c-115">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1d37c-115">createdDateTime</span></span>|<span data-ttu-id="1d37c-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1d37c-116">DateTimeOffset</span></span>|<span data-ttu-id="1d37c-117">Hora a la que se inició el proceso.</span><span class="sxs-lookup"><span data-stu-id="1d37c-117">Time at which the process was started.</span></span> <span data-ttu-id="1d37c-118">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="1d37c-118">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="1d37c-119">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="1d37c-119">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="1d37c-120">fileHash</span><span class="sxs-lookup"><span data-stu-id="1d37c-120">fileHash</span></span>|[<span data-ttu-id="1d37c-121">fileHash</span><span class="sxs-lookup"><span data-stu-id="1d37c-121">fileHash</span></span>](filehash.md)|<span data-ttu-id="1d37c-122">Tipo complejo que contiene los valores de hash de archivo (criptográficas y la ubicación).</span><span class="sxs-lookup"><span data-stu-id="1d37c-122">Complex type containing file hashes (cryptographic and location-sensitive).</span></span>|
|<span data-ttu-id="1d37c-123">integrityLevel</span><span class="sxs-lookup"><span data-stu-id="1d37c-123">integrityLevel</span></span>|<span data-ttu-id="1d37c-124">processIntegrityLevel</span><span class="sxs-lookup"><span data-stu-id="1d37c-124">processIntegrityLevel</span></span>|<span data-ttu-id="1d37c-125">El nivel de la integridad del proceso.</span><span class="sxs-lookup"><span data-stu-id="1d37c-125">The integrity level of the process.</span></span> <span data-ttu-id="1d37c-126">Los valores posibles son: `unknown`, `untrusted`, `low`, `medium`, `high`, `system`.</span><span class="sxs-lookup"><span data-stu-id="1d37c-126">Possible values are: `unknown`, `untrusted`, `low`, `medium`, `high`, `system`.</span></span>|
|<span data-ttu-id="1d37c-127">isElevated</span><span class="sxs-lookup"><span data-stu-id="1d37c-127">isElevated</span></span>|<span data-ttu-id="1d37c-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d37c-128">Boolean</span></span>|<span data-ttu-id="1d37c-129">Es True si el proceso es un elevado.</span><span class="sxs-lookup"><span data-stu-id="1d37c-129">True if the process is elevated.</span></span>|
|<span data-ttu-id="1d37c-130">name</span><span class="sxs-lookup"><span data-stu-id="1d37c-130">name</span></span>|<span data-ttu-id="1d37c-131">String</span><span class="sxs-lookup"><span data-stu-id="1d37c-131">String</span></span>|<span data-ttu-id="1d37c-132">El nombre de archivo de imagen del proceso.</span><span class="sxs-lookup"><span data-stu-id="1d37c-132">The name of the process' Image file.</span></span>|
|<span data-ttu-id="1d37c-133">parentProcessCreatedDateTime</span><span class="sxs-lookup"><span data-stu-id="1d37c-133">parentProcessCreatedDateTime</span></span>|<span data-ttu-id="1d37c-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1d37c-134">DateTimeOffset</span></span>|<span data-ttu-id="1d37c-135">Fecha y hora en que se inició el proceso primario.</span><span class="sxs-lookup"><span data-stu-id="1d37c-135">DateTime at which the parent process was started.</span></span> <span data-ttu-id="1d37c-136">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="1d37c-136">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="1d37c-137">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="1d37c-137">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="1d37c-138">parentProcessId</span><span class="sxs-lookup"><span data-stu-id="1d37c-138">parentProcessId</span></span>|<span data-ttu-id="1d37c-139">Int32</span><span class="sxs-lookup"><span data-stu-id="1d37c-139">Int32</span></span>|<span data-ttu-id="1d37c-140">El proceso de identificador (PID) del proceso principal.</span><span class="sxs-lookup"><span data-stu-id="1d37c-140">The Process ID (PID) of the parent process.</span></span>|
|<span data-ttu-id="1d37c-141">parentProcessName</span><span class="sxs-lookup"><span data-stu-id="1d37c-141">parentProcessName</span></span>|<span data-ttu-id="1d37c-142">String</span><span class="sxs-lookup"><span data-stu-id="1d37c-142">String</span></span>|<span data-ttu-id="1d37c-143">El nombre del archivo de imagen del proceso principal.</span><span class="sxs-lookup"><span data-stu-id="1d37c-143">The name of the image file of the parent process.</span></span>|
|<span data-ttu-id="1d37c-144">ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="1d37c-144">path</span></span>|<span data-ttu-id="1d37c-145">String</span><span class="sxs-lookup"><span data-stu-id="1d37c-145">String</span></span>|<span data-ttu-id="1d37c-146">Ruta de acceso completa, incluido el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="1d37c-146">Full path, including filename.</span></span>|
|<span data-ttu-id="1d37c-147">processId</span><span class="sxs-lookup"><span data-stu-id="1d37c-147">processId</span></span>|<span data-ttu-id="1d37c-148">Int32</span><span class="sxs-lookup"><span data-stu-id="1d37c-148">Int32</span></span>|<span data-ttu-id="1d37c-149">El proceso de identificador (PID) del proceso.</span><span class="sxs-lookup"><span data-stu-id="1d37c-149">The Process ID (PID) of the process.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1d37c-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1d37c-150">JSON representation</span></span>

<span data-ttu-id="1d37c-151">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="1d37c-151">The following is a JSON representation of the resource.</span></span>

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