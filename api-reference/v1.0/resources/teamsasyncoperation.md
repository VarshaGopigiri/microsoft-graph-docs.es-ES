---
title: tipo de recurso teamsAsyncOperation
description: 'Una operación asincrónica de Microsoft Teams es una operación que va más allá de la duración de una única solicitud de API. '
ms.openlocfilehash: 4ec60a5f0137c45a9bc0488b31b76f80799e0545
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031359"
---
# <a name="teamsasyncoperation-resource-type"></a><span data-ttu-id="6f4c7-103">tipo de recurso teamsAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="6f4c7-103">teamsAsyncOperation resource type</span></span>



<span data-ttu-id="6f4c7-104">Una operación asincrónica de Microsoft Teams es una operación que va más allá de la duración de una única solicitud de API.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-104">A Microsoft Teams async operation is an operation that transcends the lifetime of a single API request.</span></span> <span data-ttu-id="6f4c7-105">Estas operaciones son prolongados o demasiado caro para llevar a cabo en el plazo de su solicitud de origen.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-105">These operations are long-running or too expensive to complete within the timeframe of their originating request.</span></span>

<span data-ttu-id="6f4c7-106">Cuando se inicia una operación asincrónica, el método devuelve un código de respuesta aceptados 202.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-106">When an async operation is initiated, the method returns a 202 Accepted response code.</span></span> <span data-ttu-id="6f4c7-107">La respuesta contendrá también un encabezado de ubicación, que contiene la ubicación de la teamsAsyncOperation.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-107">The response will also contain a Location header, which contains the location of the teamsAsyncOperation.</span></span> <span data-ttu-id="6f4c7-108">Compruebe periódicamente el estado de la operación mediante la realización de una solicitud GET en esta ubicación; esperar > 30 segundos entre las comprobaciones.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-108">Periodically check the status of the operation by making a GET request to this location; wait >30 seconds between checks.</span></span>
<span data-ttu-id="6f4c7-109">Cuando la solicitud se completa correctamente, el estado se "correcto" y el targetResourceLocation señalará a los recursos creados o modificados.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-109">When the request completes successfully, the status will be "succeeded" and the targetResourceLocation will point to the created/modified resource.</span></span>

## <a name="properties"></a><span data-ttu-id="6f4c7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f4c7-110">Properties</span></span>

| <span data-ttu-id="6f4c7-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6f4c7-111">Property</span></span> | <span data-ttu-id="6f4c7-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f4c7-112">Type</span></span>   | <span data-ttu-id="6f4c7-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f4c7-113">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="6f4c7-114">id</span><span class="sxs-lookup"><span data-stu-id="6f4c7-114">id</span></span>|<span data-ttu-id="6f4c7-115">string</span><span class="sxs-lookup"><span data-stu-id="6f4c7-115">string</span></span> |<span data-ttu-id="6f4c7-116">Identificador único de operación.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-116">Unique operation id.</span></span>|
|<span data-ttu-id="6f4c7-117">tipo de operación</span><span class="sxs-lookup"><span data-stu-id="6f4c7-117">operationType</span></span>|[<span data-ttu-id="6f4c7-118">teamsAsyncOperationType</span><span class="sxs-lookup"><span data-stu-id="6f4c7-118">teamsAsyncOperationType</span></span>](teamsasyncoperationtype.md) |<span data-ttu-id="6f4c7-119">Indica qué tipo de operación que se describen.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-119">Denotes which type of operation is being described.</span></span>|
|<span data-ttu-id="6f4c7-120">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="6f4c7-120">createdDateTime</span></span>|<span data-ttu-id="6f4c7-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6f4c7-121">DateTimeOffset</span></span> |<span data-ttu-id="6f4c7-122">Hora de creación de la operación.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-122">Time when the operation was created.</span></span>|
|<span data-ttu-id="6f4c7-123">status</span><span class="sxs-lookup"><span data-stu-id="6f4c7-123">status</span></span>|[<span data-ttu-id="6f4c7-124">teamsAsyncOperationStatus</span><span class="sxs-lookup"><span data-stu-id="6f4c7-124">teamsAsyncOperationStatus</span></span>](teamsasyncoperationstatus.md)| <span data-ttu-id="6f4c7-125">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-125">Operation status.</span></span>|
|<span data-ttu-id="6f4c7-126">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="6f4c7-126">lastActionDateTime</span></span>|<span data-ttu-id="6f4c7-127">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6f4c7-127">DateTimeOffset</span></span> |<span data-ttu-id="6f4c7-128">Tiempo de cuándo se actualizó por última vez la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-128">Time when the async operation was last updated.</span></span>|
|<span data-ttu-id="6f4c7-129">attemptsCount</span><span class="sxs-lookup"><span data-stu-id="6f4c7-129">attemptsCount</span></span>|<span data-ttu-id="6f4c7-130">Int32</span><span class="sxs-lookup"><span data-stu-id="6f4c7-130">Int32</span></span>|<span data-ttu-id="6f4c7-131">Número de veces que se ha intentado establecer la operación antes de marcarlo correctamente o con errores.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-131">Number of times the operation was attempted before being marked successful or failed.</span></span>|
|<span data-ttu-id="6f4c7-132">targetResourceId</span><span class="sxs-lookup"><span data-stu-id="6f4c7-132">targetResourceId</span></span>|<span data-ttu-id="6f4c7-133">GUID</span><span class="sxs-lookup"><span data-stu-id="6f4c7-133">guid</span></span> |<span data-ttu-id="6f4c7-134">El identificador del objeto que ha creado o modificado como resultado de esta operación asincrónica, normalmente un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="6f4c7-134">The ID of the object that's created or modified as result of this async operation, typically a [team](../resources/team.md).</span></span>|
|<span data-ttu-id="6f4c7-135">targetResourceLocation</span><span class="sxs-lookup"><span data-stu-id="6f4c7-135">targetResourceLocation</span></span>|<span data-ttu-id="6f4c7-136">string</span><span class="sxs-lookup"><span data-stu-id="6f4c7-136">string</span></span>|<span data-ttu-id="6f4c7-137">La ubicación del objeto que ha creado o modificado como resultado de esta operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-137">The location of the object that's created or modified as result of this async operation.</span></span> <span data-ttu-id="6f4c7-138">Esta dirección URL debe ser se trata como un valor opaco y no se analiza en sus rutas de acceso de componente.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-138">This URL should be treated as an opaque value and not parsed into its component paths.</span></span>|
|<span data-ttu-id="6f4c7-139">error</span><span class="sxs-lookup"><span data-stu-id="6f4c7-139">error</span></span>|[<span data-ttu-id="6f4c7-140">operationError</span><span class="sxs-lookup"><span data-stu-id="6f4c7-140">operationError</span></span>](operationerror.md)|<span data-ttu-id="6f4c7-141">Cualquier error que hace que la operación asincrónica se lleve a cabo.</span><span class="sxs-lookup"><span data-stu-id="6f4c7-141">Any error that causes the async operation to fail.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="6f4c7-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6f4c7-142">JSON representation</span></span>

<span data-ttu-id="6f4c7-143">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6f4c7-143">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.teamsasyncoperation"
}-->

```json
{
    "id": "string",
    "operationType": "archiveTeam",
    "createdDateTime": "2018-01-01T00:00:00.0000000Z",
    "status": "succeeded",
    "lastActionDateTime": "2018-01-01T00:00:00.0000000Z",
    "attemptsCount": 1,
    "targetResourceId": "fa4aa5a2-a75b-4769-86f4-9e2742a18fda",
    "targetResourceLocation": "/groups('fa4aa5a2-a75b-4769-86f4-9e2742a18fda')/team",
    "error": null
}
```

<!-- uuid: 20fd7863-9545-40d4-ae8f-fee2d115a690
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teams async operation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
