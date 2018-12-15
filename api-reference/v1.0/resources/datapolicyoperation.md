# <a name="datapolicyoperation-resource-type"></a><span data-ttu-id="61864-101">tipo de recurso dataPolicyOperation</span><span class="sxs-lookup"><span data-stu-id="61864-101">dataPolicyOperation resource type</span></span>

<span data-ttu-id="61864-102">Representa una operación de la directiva de datos enviados.</span><span class="sxs-lookup"><span data-stu-id="61864-102">Represents a submitted data policy operation.</span></span> <span data-ttu-id="61864-103">Contiene la información necesaria para realizar un seguimiento del estado de una operación.</span><span class="sxs-lookup"><span data-stu-id="61864-103">It contains necessary information for tracking the status of an operation.</span></span> <span data-ttu-id="61864-104">Por ejemplo, un administrador de la compañía puede enviar una solicitud de operación de directiva de datos para exportar datos de un empleado de la compañía y, a continuación, más adelante realizar un seguimiento de dicha solicitud.</span><span class="sxs-lookup"><span data-stu-id="61864-104">For example, a company administrator can submit a data policy operation request to export an employee's company data, and then later track that request.</span></span>

## <a name="methods"></a><span data-ttu-id="61864-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="61864-105">Methods</span></span>

| <span data-ttu-id="61864-106">Método</span><span class="sxs-lookup"><span data-stu-id="61864-106">Method</span></span>           | <span data-ttu-id="61864-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61864-107">Return Type</span></span>    |<span data-ttu-id="61864-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="61864-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="61864-109">Obtener dataPolicyOperation</span><span class="sxs-lookup"><span data-stu-id="61864-109">Get dataPolicyOperation</span></span>](../api/datapolicyoperation-get.md) | [<span data-ttu-id="61864-110">dataPolicyOperation</span><span class="sxs-lookup"><span data-stu-id="61864-110">dataPolicyOperation</span></span>](datapolicyoperation.md) |<span data-ttu-id="61864-111">Recuperar las propiedades del objeto **dataPolicyOperation** .</span><span class="sxs-lookup"><span data-stu-id="61864-111">Retrieve properties of the **dataPolicyOperation** object.</span></span>|
|[<span data-ttu-id="61864-112">Exportar datos personales</span><span class="sxs-lookup"><span data-stu-id="61864-112">Export personal data</span></span>](../api/user-exportpersonaldata.md) | <span data-ttu-id="61864-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="61864-113">None</span></span> |<span data-ttu-id="61864-114">Enviar una solicitud de operación de directiva de datos para exportar los datos del usuario organizativa que más adelante se pueden leer mediante [Get dataPolicyOperation](../api/datapolicyoperation-get.md)</span><span class="sxs-lookup"><span data-stu-id="61864-114">Submit a data policy operation request to export organizational user's data which can later be read using [Get dataPolicyOperation](../api/datapolicyoperation-get.md)</span></span>|

## <a name="properties"></a><span data-ttu-id="61864-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61864-115">Properties</span></span>

> <span data-ttu-id="61864-116">**Nota:** Todas las propiedades de este recurso son de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="61864-116">**Note:** All properties of this resource are read-only.</span></span>

| <span data-ttu-id="61864-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="61864-117">Property</span></span>     | <span data-ttu-id="61864-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="61864-118">Type</span></span>   |<span data-ttu-id="61864-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="61864-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="61864-120">completedDateTime</span><span class="sxs-lookup"><span data-stu-id="61864-120">completedDateTime</span></span>|<span data-ttu-id="61864-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="61864-121">DateTimeOffset</span></span>|<span data-ttu-id="61864-122">Representa la solicitud para esta operación de la directiva de datos se ha completado, en la hora UTC, con el formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="61864-122">Represents when the request for this data policy operation was completed, in UTC time, using the ISO 8601 format.</span></span> <span data-ttu-id="61864-123">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="61864-123">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span> <span data-ttu-id="61864-124">NULL hasta que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="61864-124">Null until the operation completes.</span></span>|
|<span data-ttu-id="61864-125">id</span><span class="sxs-lookup"><span data-stu-id="61864-125">id</span></span>|<span data-ttu-id="61864-126">String</span><span class="sxs-lookup"><span data-stu-id="61864-126">String</span></span>| <span data-ttu-id="61864-127">Clave única para esta operación.</span><span class="sxs-lookup"><span data-stu-id="61864-127">Unique key for this operation.</span></span> |
|<span data-ttu-id="61864-128">status</span><span class="sxs-lookup"><span data-stu-id="61864-128">status</span></span>|<span data-ttu-id="61864-129">string</span><span class="sxs-lookup"><span data-stu-id="61864-129">string</span></span>| <span data-ttu-id="61864-130">Los valores posibles son: `notStarted`, `running`, `complete`, `failed` y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="61864-130">Possible values are: `notStarted`, `running`, `complete`, `failed`, `unknownFutureValue`.</span></span>|
|<span data-ttu-id="61864-131">storageLocation</span><span class="sxs-lookup"><span data-stu-id="61864-131">storageLocation</span></span>|<span data-ttu-id="61864-132">String</span><span class="sxs-lookup"><span data-stu-id="61864-132">String</span></span>|<span data-ttu-id="61864-133">La ubicación de la dirección URL a donde se va a exportar datos para las solicitudes de exportación.</span><span class="sxs-lookup"><span data-stu-id="61864-133">The URL location to where data is being exported for export requests.</span></span>|
|<span data-ttu-id="61864-134">userId</span><span class="sxs-lookup"><span data-stu-id="61864-134">userId</span></span>|<span data-ttu-id="61864-135">String</span><span class="sxs-lookup"><span data-stu-id="61864-135">String</span></span>|<span data-ttu-id="61864-136">El identificador para el usuario en quien se realiza la operación.</span><span class="sxs-lookup"><span data-stu-id="61864-136">The id for the user on whom the operation is performed.</span></span>|
|<span data-ttu-id="61864-137">submittedDateTime</span><span class="sxs-lookup"><span data-stu-id="61864-137">submittedDateTime</span></span>|<span data-ttu-id="61864-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="61864-138">DateTimeOffset</span></span>|<span data-ttu-id="61864-139">Representa para esta operación de datos se envió la solicitud, en la hora UTC, con el formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="61864-139">Represents when the request for this data operation was submitted, in UTC time, using the ISO 8601 format.</span></span> <span data-ttu-id="61864-140">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="61864-140">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="61864-141">progreso</span><span class="sxs-lookup"><span data-stu-id="61864-141">progress</span></span>|<span data-ttu-id="61864-142">String</span><span class="sxs-lookup"><span data-stu-id="61864-142">String</span></span>|<span data-ttu-id="61864-143">Especifica el progreso de una operación.</span><span class="sxs-lookup"><span data-stu-id="61864-143">Specifies the progress of an operation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="61864-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="61864-144">Relationships</span></span>
<span data-ttu-id="61864-145">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="61864-145">None.</span></span>


## <a name="json-representation"></a><span data-ttu-id="61864-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="61864-146">JSON representation</span></span>

<span data-ttu-id="61864-147">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="61864-147">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.dataPolicyOperation"
}-->

```json
{
  "completedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "status": "string",
  "storageLocation": "String",
  "userId": "String",
  "submittedDateTime": "String (timestamp)", 
  "progress": "String (double)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "dataPolicyOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
