# <a name="process-resource-type"></a><span data-ttu-id="09df5-101">Tipo de recurso de proceso</span><span class="sxs-lookup"><span data-stu-id="09df5-101">process resource type</span></span>

<span data-ttu-id="09df5-102">Contiene información con estado acerca del proceso relacionadocon la alerta.</span><span class="sxs-lookup"><span data-stu-id="09df5-102">Contains stateful information about the process related to the alert.</span></span>

## <a name="properties"></a><span data-ttu-id="09df5-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="09df5-103">Properties</span></span>

| <span data-ttu-id="09df5-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="09df5-104">Property</span></span>   | <span data-ttu-id="09df5-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="09df5-105">Type</span></span>|<span data-ttu-id="09df5-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="09df5-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="09df5-107">accountName</span><span class="sxs-lookup"><span data-stu-id="09df5-107">accountName</span></span>|<span data-ttu-id="09df5-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="09df5-108">String</span></span>|<span data-ttu-id="09df5-109">Identificador de la cuenta de usuario (contexto de la cuenta de usuario bajo el cual se ejcuta el proceso) por ejemplo, AccountName, SID, etc.</span><span class="sxs-lookup"><span data-stu-id="09df5-109">User account identifier (user account context the process ran under) for example, AccountName, SID, and so on.</span></span>|
|<span data-ttu-id="09df5-110">commandLine</span><span class="sxs-lookup"><span data-stu-id="09df5-110">commandLine</span></span>|<span data-ttu-id="09df5-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="09df5-111">String</span></span>|<span data-ttu-id="09df5-112">La línea de comandos de invocación del proceso completo incluidos todos los parámetros.</span><span class="sxs-lookup"><span data-stu-id="09df5-112">The full process invocation commandline including all parameters.</span></span>|
|<span data-ttu-id="09df5-113">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="09df5-113">createdDateTime</span></span>|<span data-ttu-id="09df5-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="09df5-114">DateTimeOffset</span></span>|<span data-ttu-id="09df5-115">Hora a la que se inició el proceso.</span><span class="sxs-lookup"><span data-stu-id="09df5-115">Time at which the process was started.</span></span> <span data-ttu-id="09df5-116">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="09df5-116">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="09df5-117">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="09df5-117">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="09df5-118">fileHash</span><span class="sxs-lookup"><span data-stu-id="09df5-118">fileHash</span></span>|[<span data-ttu-id="09df5-119">fileHash</span><span class="sxs-lookup"><span data-stu-id="09df5-119">fileHash</span></span>](filehash.md)|<span data-ttu-id="09df5-120">Tipo complejo que contiene los valores de hash de archivo (criptográficos y dependientes de la ubicación).</span><span class="sxs-lookup"><span data-stu-id="09df5-120">Complex type containing file hashes (cryptographic and location-sensitive).</span></span>|
|<span data-ttu-id="09df5-121">integrityLevel</span><span class="sxs-lookup"><span data-stu-id="09df5-121">integrityLevel</span></span>|<span data-ttu-id="09df5-122">processIntegrityLevel</span><span class="sxs-lookup"><span data-stu-id="09df5-122">processIntegrityLevel</span></span>|<span data-ttu-id="09df5-123">El nivel de integridad del proceso.</span><span class="sxs-lookup"><span data-stu-id="09df5-123">The integrity level of the process.</span></span> <span data-ttu-id="09df5-124">Los valores posibles son: `unknown`, `untrusted`, `low`, `medium`, `high`, `system`.</span><span class="sxs-lookup"><span data-stu-id="09df5-124">Possible values are: `unknown`, `untrusted`, `low`, `medium`, `high`, `system`.</span></span>|
|<span data-ttu-id="09df5-125">isElevated</span><span class="sxs-lookup"><span data-stu-id="09df5-125">isElevated</span></span>|<span data-ttu-id="09df5-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="09df5-126">Boolean</span></span>|<span data-ttu-id="09df5-127">True si el proceso es elevado.</span><span class="sxs-lookup"><span data-stu-id="09df5-127">True if the process is elevated.</span></span>|
|<span data-ttu-id="09df5-128">nombre</span><span class="sxs-lookup"><span data-stu-id="09df5-128">name</span></span>|<span data-ttu-id="09df5-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="09df5-129">String</span></span>|<span data-ttu-id="09df5-130">El nombre del archivo de imagen del proceso.</span><span class="sxs-lookup"><span data-stu-id="09df5-130">The name of the process' Image file.</span></span>|
|<span data-ttu-id="09df5-131">parentProcessCreatedDateTime</span><span class="sxs-lookup"><span data-stu-id="09df5-131">parentProcessCreatedDateTime</span></span>|<span data-ttu-id="09df5-132">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="09df5-132">DateTimeOffset</span></span>|<span data-ttu-id="09df5-133">Fecha y hora en la que se inició el proceso primario.</span><span class="sxs-lookup"><span data-stu-id="09df5-133">DateTime at which the parent process was started.</span></span> <span data-ttu-id="09df5-134">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="09df5-134">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="09df5-135">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="09df5-135">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="09df5-136">parentProcessId</span><span class="sxs-lookup"><span data-stu-id="09df5-136">parentProcessId</span></span>|<span data-ttu-id="09df5-137">Int32</span><span class="sxs-lookup"><span data-stu-id="09df5-137">Int32</span></span>|<span data-ttu-id="09df5-138">El identificador del proceso (PID) del proceso principal.</span><span class="sxs-lookup"><span data-stu-id="09df5-138">The Process ID (PID) of the parent process.</span></span>|
|<span data-ttu-id="09df5-139">parentProcessName</span><span class="sxs-lookup"><span data-stu-id="09df5-139">parentProcessName</span></span>|<span data-ttu-id="09df5-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="09df5-140">String</span></span>|<span data-ttu-id="09df5-141">El nombre del archivo de imagen del proceso principal.</span><span class="sxs-lookup"><span data-stu-id="09df5-141">The name of the image file of the parent process.</span></span>|
|<span data-ttu-id="09df5-142">ruta</span><span class="sxs-lookup"><span data-stu-id="09df5-142">path</span></span>|<span data-ttu-id="09df5-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="09df5-143">String</span></span>|<span data-ttu-id="09df5-144">Ruta completa, incluido el filename.</span><span class="sxs-lookup"><span data-stu-id="09df5-144">Full path, including filename.</span></span>|
|<span data-ttu-id="09df5-145">processId</span><span class="sxs-lookup"><span data-stu-id="09df5-145">processId</span></span>|<span data-ttu-id="09df5-146">Int32</span><span class="sxs-lookup"><span data-stu-id="09df5-146">Int32</span></span>|<span data-ttu-id="09df5-147">El identificador del proceso (PID) del proceso.</span><span class="sxs-lookup"><span data-stu-id="09df5-147">The Process ID (PID) of the process.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="09df5-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="09df5-148">JSON representation</span></span>

<span data-ttu-id="09df5-149">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="09df5-149">The following is a JSON representation of the resource.</span></span>

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