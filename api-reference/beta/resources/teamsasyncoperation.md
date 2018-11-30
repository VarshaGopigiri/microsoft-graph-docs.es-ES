---
title: tipo de recurso teamsAsyncOperation
description: 'Una operación asincrónica de Microsoft Teams es una operación que va más allá de la duración de una única solicitud de API. '
ms.openlocfilehash: 66279b933202167f85ed7d1fc4709e8e61034537
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084522"
---
# <a name="teamsasyncoperation-resource-type"></a><span data-ttu-id="deb83-103">tipo de recurso teamsAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="deb83-103">teamsAsyncOperation resource type</span></span>

> <span data-ttu-id="deb83-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="deb83-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="deb83-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="deb83-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="deb83-106">Una operación asincrónica de Microsoft Teams es una operación que va más allá de la duración de una única solicitud de API.</span><span class="sxs-lookup"><span data-stu-id="deb83-106">A Microsoft Teams async operation is an operation that transcends the lifetime of a single API request.</span></span> <span data-ttu-id="deb83-107">Estas operaciones son prolongados o demasiado caro para llevar a cabo en el plazo de su solicitud de origen.</span><span class="sxs-lookup"><span data-stu-id="deb83-107">These operations are long-running or too expensive to complete within the timeframe of their originating request.</span></span>

<span data-ttu-id="deb83-108">Cuando se inicia una operación asincrónica, el método devuelve un código de respuesta aceptados 202.</span><span class="sxs-lookup"><span data-stu-id="deb83-108">When an async operation is initiated, the method returns a 202 Accepted response code.</span></span> <span data-ttu-id="deb83-109">La respuesta contendrá también un encabezado de ubicación, que contiene la ubicación de la teamsAsyncOperation.</span><span class="sxs-lookup"><span data-stu-id="deb83-109">The response will also contain a Location header, which contains the location of the teamsAsyncOperation.</span></span> <span data-ttu-id="deb83-110">Compruebe periódicamente el estado de la operación mediante la realización de una solicitud GET en esta ubicación; esperar > 30 segundos entre las comprobaciones.</span><span class="sxs-lookup"><span data-stu-id="deb83-110">Periodically check the status of the operation by making a GET request to this location; wait >30 seconds between checks.</span></span>
<span data-ttu-id="deb83-111">Cuando la solicitud se completa correctamente, el estado se "correcto" y el targetResourceLocation señalará a los recursos creados o modificados.</span><span class="sxs-lookup"><span data-stu-id="deb83-111">When the request completes successfully, the status will be "succeeded" and the targetResourceLocation will point to the created/modified resource.</span></span>

## <a name="properties"></a><span data-ttu-id="deb83-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="deb83-112">Properties</span></span>

| <span data-ttu-id="deb83-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="deb83-113">Property</span></span> | <span data-ttu-id="deb83-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="deb83-114">Type</span></span>   | <span data-ttu-id="deb83-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="deb83-115">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="deb83-116">id</span><span class="sxs-lookup"><span data-stu-id="deb83-116">id</span></span>|<span data-ttu-id="deb83-117">string</span><span class="sxs-lookup"><span data-stu-id="deb83-117">string</span></span> |<span data-ttu-id="deb83-118">Identificador único de operación.</span><span class="sxs-lookup"><span data-stu-id="deb83-118">Unique operation id.</span></span>|
|<span data-ttu-id="deb83-119">tipo de operación</span><span class="sxs-lookup"><span data-stu-id="deb83-119">operationType</span></span>|[<span data-ttu-id="deb83-120">teamsAsyncOperationType</span><span class="sxs-lookup"><span data-stu-id="deb83-120">teamsAsyncOperationType</span></span>](teamsasyncoperationtype.md) |<span data-ttu-id="deb83-121">Indica qué tipo de operación que se describen.</span><span class="sxs-lookup"><span data-stu-id="deb83-121">Denotes which type of operation is being described.</span></span>|
|<span data-ttu-id="deb83-122">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="deb83-122">createdDateTime</span></span>|<span data-ttu-id="deb83-123">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="deb83-123">DateTimeOffset</span></span> |<span data-ttu-id="deb83-124">Hora de creación de la operación.</span><span class="sxs-lookup"><span data-stu-id="deb83-124">Time when the operation was created.</span></span>|
|<span data-ttu-id="deb83-125">status</span><span class="sxs-lookup"><span data-stu-id="deb83-125">status</span></span>|[<span data-ttu-id="deb83-126">teamsAsyncOperationStatus</span><span class="sxs-lookup"><span data-stu-id="deb83-126">teamsAsyncOperationStatus</span></span>](teamsasyncoperationstatus.md)| <span data-ttu-id="deb83-127">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="deb83-127">Operation status.</span></span>|
|<span data-ttu-id="deb83-128">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="deb83-128">lastActionDateTime</span></span>|<span data-ttu-id="deb83-129">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="deb83-129">DateTimeOffset</span></span> |<span data-ttu-id="deb83-130">Tiempo de cuándo se actualizó por última vez la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="deb83-130">Time when the async operation was last updated.</span></span>|
|<span data-ttu-id="deb83-131">attemptsCount</span><span class="sxs-lookup"><span data-stu-id="deb83-131">attemptsCount</span></span>|<span data-ttu-id="deb83-132">Int32</span><span class="sxs-lookup"><span data-stu-id="deb83-132">Int32</span></span>|<span data-ttu-id="deb83-133">Número de veces que se ha intentado establecer la operación antes de marcarlo correctamente o con errores.</span><span class="sxs-lookup"><span data-stu-id="deb83-133">Number of times the operation was attempted before being marked successful or failed.</span></span>|
|<span data-ttu-id="deb83-134">targetResourceId</span><span class="sxs-lookup"><span data-stu-id="deb83-134">targetResourceId</span></span>|<span data-ttu-id="deb83-135">GUID</span><span class="sxs-lookup"><span data-stu-id="deb83-135">guid</span></span> |<span data-ttu-id="deb83-136">El identificador del objeto que ha creado o modificado como resultado de esta operación asincrónica, normalmente un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="deb83-136">The ID of the object that's created or modified as result of this async operation, typically a [team](../resources/team.md).</span></span>|
|<span data-ttu-id="deb83-137">targetResourceLocation</span><span class="sxs-lookup"><span data-stu-id="deb83-137">targetResourceLocation</span></span>|<span data-ttu-id="deb83-138">string</span><span class="sxs-lookup"><span data-stu-id="deb83-138">string</span></span>|<span data-ttu-id="deb83-139">La ubicación del objeto que ha creado o modificado como resultado de esta operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="deb83-139">The location of the object that's created or modified as result of this async operation.</span></span> <span data-ttu-id="deb83-140">Esta dirección URL debe ser se trata como un valor opaco y no se analiza en sus rutas de acceso de componente.</span><span class="sxs-lookup"><span data-stu-id="deb83-140">This URL should be treated as an opaque value and not parsed into its component paths.</span></span>|
|<span data-ttu-id="deb83-141">error</span><span class="sxs-lookup"><span data-stu-id="deb83-141">error</span></span>|[<span data-ttu-id="deb83-142">operationError</span><span class="sxs-lookup"><span data-stu-id="deb83-142">operationError</span></span>](operationerror.md)|<span data-ttu-id="deb83-143">Cualquier error que hace que la operación asincrónica se lleve a cabo.</span><span class="sxs-lookup"><span data-stu-id="deb83-143">Any error that causes the async operation to fail.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="deb83-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="deb83-144">JSON representation</span></span>

<span data-ttu-id="deb83-145">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="deb83-145">The following is a JSON representation of the resource.</span></span>

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
