---
title: Tipo de recurso onenoteOperation
description: Estado de ciertas operaciones de OneNote de larga duración.
author: Jewan-microsoft
localization_priority: Normal
ms.openlocfilehash: 89c1d1ac3404653ae3996a95bdf40c22fdd3b7c8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845937"
---
# <a name="onenoteoperation-resource-type"></a><span data-ttu-id="c3b0b-103">Tipo de recurso onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="c3b0b-103">onenoteOperation resource type</span></span>

<span data-ttu-id="c3b0b-104">Estado de ciertas operaciones de OneNote de larga duración.</span><span class="sxs-lookup"><span data-stu-id="c3b0b-104">The status of certain long-running OneNote operations.</span></span>

## <a name="json-representation"></a><span data-ttu-id="c3b0b-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c3b0b-105">JSON representation</span></span>

<span data-ttu-id="c3b0b-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c3b0b-106">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="c3b0b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c3b0b-107">Properties</span></span>
| <span data-ttu-id="c3b0b-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c3b0b-108">Property</span></span>     | <span data-ttu-id="c3b0b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c3b0b-109">Type</span></span>   |<span data-ttu-id="c3b0b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3b0b-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c3b0b-111">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c3b0b-111">createdDateTime</span></span>| <span data-ttu-id="c3b0b-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c3b0b-112">DateTimeOffset</span></span> |<span data-ttu-id="c3b0b-113">La hora de inicio de la operación.</span><span class="sxs-lookup"><span data-stu-id="c3b0b-113">The start time of the operation.</span></span>|
|<span data-ttu-id="c3b0b-114">error</span><span class="sxs-lookup"><span data-stu-id="c3b0b-114">error</span></span>|[<span data-ttu-id="c3b0b-115">onenoteOperationError</span><span class="sxs-lookup"><span data-stu-id="c3b0b-115">onenoteOperationError</span></span>](onenoteoperationerror.md)|<span data-ttu-id="c3b0b-116">Error devuelto por la operación.</span><span class="sxs-lookup"><span data-stu-id="c3b0b-116">The error returned by the operation.</span></span>|
|<span data-ttu-id="c3b0b-117">id</span><span class="sxs-lookup"><span data-stu-id="c3b0b-117">id</span></span>|<span data-ttu-id="c3b0b-118">string</span><span class="sxs-lookup"><span data-stu-id="c3b0b-118">string</span></span>|<span data-ttu-id="c3b0b-119">Id. de operación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c3b0b-119">The operation id. Read-only.</span></span>|
|<span data-ttu-id="c3b0b-120">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="c3b0b-120">lastActionDateTime</span></span>| <span data-ttu-id="c3b0b-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c3b0b-121">DateTimeOffset</span></span> |<span data-ttu-id="c3b0b-122">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="c3b0b-122">The time of the last action of the operation.</span></span>|
|<span data-ttu-id="c3b0b-123">resourceId</span><span class="sxs-lookup"><span data-stu-id="c3b0b-123">resourceId</span></span>|<span data-ttu-id="c3b0b-124">string</span><span class="sxs-lookup"><span data-stu-id="c3b0b-124">string</span></span>|<span data-ttu-id="c3b0b-125">Identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="c3b0b-125">The resource id.</span></span>|
|<span data-ttu-id="c3b0b-126">resourceLocation</span><span class="sxs-lookup"><span data-stu-id="c3b0b-126">resourceLocation</span></span>|<span data-ttu-id="c3b0b-127">string</span><span class="sxs-lookup"><span data-stu-id="c3b0b-127">string</span></span>|<span data-ttu-id="c3b0b-p101">URI de recurso del objeto. Por ejemplo, el URI de recurso de una página o sección copiada.</span><span class="sxs-lookup"><span data-stu-id="c3b0b-p101">The resource URI for the object. For example, the resource URI for a copied page or section.</span></span> |
|<span data-ttu-id="c3b0b-130">status</span><span class="sxs-lookup"><span data-stu-id="c3b0b-130">status</span></span>|<span data-ttu-id="c3b0b-131">cadena</span><span class="sxs-lookup"><span data-stu-id="c3b0b-131">string</span></span>|<span data-ttu-id="c3b0b-132">Estado actual de la operación: `notstarted`, `running`, `completed` o `failed`</span><span class="sxs-lookup"><span data-stu-id="c3b0b-132">The current status of the operation: `notstarted`, `running`, `completed`, `failed`</span></span> |
|<span data-ttu-id="c3b0b-133">percentComplete</span><span class="sxs-lookup"><span data-stu-id="c3b0b-133">percentComplete</span></span>|<span data-ttu-id="c3b0b-134">cadena</span><span class="sxs-lookup"><span data-stu-id="c3b0b-134">string</span></span>|<span data-ttu-id="c3b0b-135">El porcentaje de operación completada si la operación todavía tiene el estado `running`</span><span class="sxs-lookup"><span data-stu-id="c3b0b-135">The operation percent complete if the operation is still in `running` status</span></span>

## <a name="relationships"></a><span data-ttu-id="c3b0b-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c3b0b-136">Relationships</span></span>
<span data-ttu-id="c3b0b-137">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c3b0b-137">None</span></span>


## <a name="methods"></a><span data-ttu-id="c3b0b-138">Métodos</span><span class="sxs-lookup"><span data-stu-id="c3b0b-138">Methods</span></span>

| <span data-ttu-id="c3b0b-139">Método</span><span class="sxs-lookup"><span data-stu-id="c3b0b-139">Method</span></span>           | <span data-ttu-id="c3b0b-140">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3b0b-140">Return Type</span></span>    |<span data-ttu-id="c3b0b-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3b0b-141">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="c3b0b-142">Obtener operation</span><span class="sxs-lookup"><span data-stu-id="c3b0b-142">Get operation</span></span>](../api/onenoteoperation-get.md) | [<span data-ttu-id="c3b0b-143">onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="c3b0b-143">onenoteOperation</span></span>](onenoteoperation.md) |<span data-ttu-id="c3b0b-144">Obtener el estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="c3b0b-144">Get the status of the operation.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
