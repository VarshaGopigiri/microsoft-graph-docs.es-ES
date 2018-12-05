---
title: tipo de recurso dataPolicyOperation
description: Representa una operación de la directiva de datos enviados. Contiene la información necesaria para realizar un seguimiento del estado de una operación. Por ejemplo, un administrador de la compañía puede enviar una solicitud de operación de directiva de datos para exportar datos de un empleado de la compañía y, a continuación, más adelante realizar un seguimiento de dicha solicitud.
ms.openlocfilehash: 6e896fdfa60b733dd91e9da573d998c1949f0d9c
ms.sourcegitcommit: 4a46cfd112c8089fc07e4e5ccdccaf415a3a0e7f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/05/2018
ms.locfileid: "27156036"
---
# <a name="datapolicyoperation-resource-type"></a><span data-ttu-id="e3c25-105">tipo de recurso dataPolicyOperation</span><span class="sxs-lookup"><span data-stu-id="e3c25-105">dataPolicyOperation resource type</span></span>

<span data-ttu-id="e3c25-106">Representa una operación de la directiva de datos enviados.</span><span class="sxs-lookup"><span data-stu-id="e3c25-106">Represents a submitted data policy operation.</span></span> <span data-ttu-id="e3c25-107">Contiene la información necesaria para realizar un seguimiento del estado de una operación.</span><span class="sxs-lookup"><span data-stu-id="e3c25-107">It contains necessary information for tracking the status of an operation.</span></span> <span data-ttu-id="e3c25-108">Por ejemplo, un administrador de la compañía puede enviar una solicitud de operación de directiva de datos para exportar datos de un empleado de la compañía y, a continuación, más adelante realizar un seguimiento de dicha solicitud.</span><span class="sxs-lookup"><span data-stu-id="e3c25-108">For example, a company administrator can submit a data policy operation request to export an employee's company data, and then later track that request.</span></span>

## <a name="methods"></a><span data-ttu-id="e3c25-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e3c25-109">Methods</span></span>

| <span data-ttu-id="e3c25-110">Método</span><span class="sxs-lookup"><span data-stu-id="e3c25-110">Method</span></span>           | <span data-ttu-id="e3c25-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3c25-111">Return Type</span></span>    |<span data-ttu-id="e3c25-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3c25-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e3c25-113">Obtener dataPolicyOperation</span><span class="sxs-lookup"><span data-stu-id="e3c25-113">Get dataPolicyOperation</span></span>](../api/datapolicyoperation-get.md) | [<span data-ttu-id="e3c25-114">dataPolicyOperation</span><span class="sxs-lookup"><span data-stu-id="e3c25-114">dataPolicyOperation</span></span>](datapolicyoperation.md) |<span data-ttu-id="e3c25-115">Leer las propiedades del objeto dataPolicyOperation.</span><span class="sxs-lookup"><span data-stu-id="e3c25-115">Read properties of the dataPolicyOperation object.</span></span>|

## <a name="properties"></a><span data-ttu-id="e3c25-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e3c25-116">Properties</span></span>

> <span data-ttu-id="e3c25-117">**Nota:** Todas las propiedades de este recurso son de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e3c25-117">**Note:** All properties of this resource are read-only.</span></span>

| <span data-ttu-id="e3c25-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e3c25-118">Property</span></span>     | <span data-ttu-id="e3c25-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3c25-119">Type</span></span>   |<span data-ttu-id="e3c25-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3c25-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e3c25-121">completedDateTime</span><span class="sxs-lookup"><span data-stu-id="e3c25-121">completedDateTime</span></span>|<span data-ttu-id="e3c25-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e3c25-122">DateTimeOffset</span></span>|<span data-ttu-id="e3c25-123">Representa la solicitud para esta operación de la directiva de datos se ha completado, en la hora UTC, con el formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="e3c25-123">Represents when the request for this data policy operation was completed, in UTC time, using the ISO 8601 format.</span></span> <span data-ttu-id="e3c25-124">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="e3c25-124">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span> <span data-ttu-id="e3c25-125">NULL hasta que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="e3c25-125">Null until the operation completes.</span></span>|
|<span data-ttu-id="e3c25-126">id</span><span class="sxs-lookup"><span data-stu-id="e3c25-126">id</span></span>|<span data-ttu-id="e3c25-127">String</span><span class="sxs-lookup"><span data-stu-id="e3c25-127">String</span></span>| <span data-ttu-id="e3c25-128">Clave única para esta operación.</span><span class="sxs-lookup"><span data-stu-id="e3c25-128">Unique key for this operation.</span></span> |
|<span data-ttu-id="e3c25-129">status</span><span class="sxs-lookup"><span data-stu-id="e3c25-129">status</span></span>|<span data-ttu-id="e3c25-130">string</span><span class="sxs-lookup"><span data-stu-id="e3c25-130">string</span></span>| <span data-ttu-id="e3c25-131">Los valores posibles son: `notStarted`, `running`, `complete`, `failed` y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="e3c25-131">Possible values are: `notStarted`, `running`, `complete`, `failed`, `unknownFutureValue`.</span></span>|
|<span data-ttu-id="e3c25-132">storageLocation</span><span class="sxs-lookup"><span data-stu-id="e3c25-132">storageLocation</span></span>|<span data-ttu-id="e3c25-133">String</span><span class="sxs-lookup"><span data-stu-id="e3c25-133">String</span></span>|<span data-ttu-id="e3c25-134">La ubicación de la dirección URL a donde se va a exportar datos para las solicitudes de exportación.</span><span class="sxs-lookup"><span data-stu-id="e3c25-134">The URL location to where data is being exported for export requests.</span></span>|
|<span data-ttu-id="e3c25-135">userId</span><span class="sxs-lookup"><span data-stu-id="e3c25-135">userId</span></span>|<span data-ttu-id="e3c25-136">String</span><span class="sxs-lookup"><span data-stu-id="e3c25-136">String</span></span>|<span data-ttu-id="e3c25-137">El identificador para el usuario en quien se realiza la operación.</span><span class="sxs-lookup"><span data-stu-id="e3c25-137">The id for the user on whom the operation is performed.</span></span>|
|<span data-ttu-id="e3c25-138">submittedDateTime</span><span class="sxs-lookup"><span data-stu-id="e3c25-138">submittedDateTime</span></span>|<span data-ttu-id="e3c25-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e3c25-139">DateTimeOffset</span></span>|<span data-ttu-id="e3c25-140">Representa para esta operación de datos se envió la solicitud, en la hora UTC, con el formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="e3c25-140">Represents when the request for this data operation was submitted, in UTC time, using the ISO 8601 format.</span></span> <span data-ttu-id="e3c25-141">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="e3c25-141">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="e3c25-142">progreso</span><span class="sxs-lookup"><span data-stu-id="e3c25-142">progress</span></span>|<span data-ttu-id="e3c25-143">Doble</span><span class="sxs-lookup"><span data-stu-id="e3c25-143">Double</span></span>|<span data-ttu-id="e3c25-144">Especifica el progreso de una operación.</span><span class="sxs-lookup"><span data-stu-id="e3c25-144">Specifies the progress of an operation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e3c25-145">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e3c25-145">Relationships</span></span>
<span data-ttu-id="e3c25-146">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e3c25-146">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="e3c25-147">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e3c25-147">JSON representation</span></span>

<span data-ttu-id="e3c25-148">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e3c25-148">Here is a JSON representation of the resource.</span></span>

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
  "progress": "Double"
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
