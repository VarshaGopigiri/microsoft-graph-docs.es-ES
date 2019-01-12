---
title: Tipo de recurso onenoteOperation
description: Estado de ciertas operaciones de OneNote de larga duración.
author: jewan-microsoft
localization_priority: Normal
ms.prod: onenote
ms.openlocfilehash: eaab313e9399e6e8724d5096b7ac29ec315889ad
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977468"
---
# <a name="onenoteoperation-resource-type"></a><span data-ttu-id="66faa-103">Tipo de recurso onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="66faa-103">onenoteOperation resource type</span></span>

<span data-ttu-id="66faa-104">Estado de ciertas operaciones de OneNote de larga duración.</span><span class="sxs-lookup"><span data-stu-id="66faa-104">The status of certain long-running OneNote operations.</span></span>

## <a name="json-representation"></a><span data-ttu-id="66faa-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="66faa-105">JSON representation</span></span>

<span data-ttu-id="66faa-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="66faa-106">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.operation",
  "@odata.type": "microsoft.graph.onenoteOperation"
}-->

```json
{
  "createdDateTime": "String (timestamp)",
  "error": {"@odata.type": "microsoft.graph.onenoteOperationError"},
  "id": "string (identifier)",
  "lastActionDateTime": "String (timestamp)",
  "resourceId": "string",
  "resourceLocation": "string",
  "status": "string",
  "percentComplete": "string"
}

```
## <a name="properties"></a><span data-ttu-id="66faa-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66faa-107">Properties</span></span>
| <span data-ttu-id="66faa-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66faa-108">Property</span></span>     | <span data-ttu-id="66faa-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="66faa-109">Type</span></span>   |<span data-ttu-id="66faa-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="66faa-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="66faa-111">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="66faa-111">createdDateTime</span></span>| <span data-ttu-id="66faa-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66faa-112">DateTimeOffset</span></span> |<span data-ttu-id="66faa-113">La hora de inicio de la operación.</span><span class="sxs-lookup"><span data-stu-id="66faa-113">The start time of the operation.</span></span>|
|<span data-ttu-id="66faa-114">error</span><span class="sxs-lookup"><span data-stu-id="66faa-114">error</span></span>|[<span data-ttu-id="66faa-115">onenoteOperationError</span><span class="sxs-lookup"><span data-stu-id="66faa-115">onenoteOperationError</span></span>](onenoteoperationerror.md)|<span data-ttu-id="66faa-116">Error devuelto por la operación.</span><span class="sxs-lookup"><span data-stu-id="66faa-116">The error returned by the operation.</span></span>|
|<span data-ttu-id="66faa-117">id</span><span class="sxs-lookup"><span data-stu-id="66faa-117">id</span></span>|<span data-ttu-id="66faa-118">string</span><span class="sxs-lookup"><span data-stu-id="66faa-118">string</span></span>|<span data-ttu-id="66faa-119">Id. de operación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="66faa-119">The operation id. Read-only.</span></span>|
|<span data-ttu-id="66faa-120">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="66faa-120">lastActionDateTime</span></span>| <span data-ttu-id="66faa-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66faa-121">DateTimeOffset</span></span> |<span data-ttu-id="66faa-122">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="66faa-122">The time of the last action of the operation.</span></span>|
|<span data-ttu-id="66faa-123">resourceId</span><span class="sxs-lookup"><span data-stu-id="66faa-123">resourceId</span></span>|<span data-ttu-id="66faa-124">string</span><span class="sxs-lookup"><span data-stu-id="66faa-124">string</span></span>|<span data-ttu-id="66faa-125">Identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="66faa-125">The resource id.</span></span>|
|<span data-ttu-id="66faa-126">resourceLocation</span><span class="sxs-lookup"><span data-stu-id="66faa-126">resourceLocation</span></span>|<span data-ttu-id="66faa-127">string</span><span class="sxs-lookup"><span data-stu-id="66faa-127">string</span></span>|<span data-ttu-id="66faa-p101">URI de recurso del objeto. Por ejemplo, el URI de recurso de una página o sección copiada.</span><span class="sxs-lookup"><span data-stu-id="66faa-p101">The resource URI for the object. For example, the resource URI for a copied page or section.</span></span> |
|<span data-ttu-id="66faa-130">status</span><span class="sxs-lookup"><span data-stu-id="66faa-130">status</span></span>|<span data-ttu-id="66faa-131">cadena</span><span class="sxs-lookup"><span data-stu-id="66faa-131">string</span></span>|<span data-ttu-id="66faa-132">Estado actual de la operación: `notstarted`, `running`, `completed` o `failed`</span><span class="sxs-lookup"><span data-stu-id="66faa-132">The current status of the operation: `notstarted`, `running`, `completed`, `failed`</span></span> |
|<span data-ttu-id="66faa-133">percentComplete</span><span class="sxs-lookup"><span data-stu-id="66faa-133">percentComplete</span></span>|<span data-ttu-id="66faa-134">cadena</span><span class="sxs-lookup"><span data-stu-id="66faa-134">string</span></span>|<span data-ttu-id="66faa-135">El porcentaje de operación completada si la operación todavía tiene el estado `running`</span><span class="sxs-lookup"><span data-stu-id="66faa-135">The operation percent complete if the operation is still in `running` status</span></span>

## <a name="relationships"></a><span data-ttu-id="66faa-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="66faa-136">Relationships</span></span>
<span data-ttu-id="66faa-137">Ninguno</span><span class="sxs-lookup"><span data-stu-id="66faa-137">None</span></span>


## <a name="methods"></a><span data-ttu-id="66faa-138">Métodos</span><span class="sxs-lookup"><span data-stu-id="66faa-138">Methods</span></span>

| <span data-ttu-id="66faa-139">Método</span><span class="sxs-lookup"><span data-stu-id="66faa-139">Method</span></span>           | <span data-ttu-id="66faa-140">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66faa-140">Return Type</span></span>    |<span data-ttu-id="66faa-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="66faa-141">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="66faa-142">Obtener operation</span><span class="sxs-lookup"><span data-stu-id="66faa-142">Get operation</span></span>](../api/onenoteoperation-get.md) | [<span data-ttu-id="66faa-143">onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="66faa-143">onenoteOperation</span></span>](onenoteoperation.md) |<span data-ttu-id="66faa-144">Obtener el estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="66faa-144">Get the status of the operation.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
