---
title: Tipo de recurso onenoteOperation
description: Estado de ciertas operaciones de OneNote de larga duración.
author: Jewan-microsoft
ms.openlocfilehash: bbb7b9457ce5a3d7ba9faf45d893ae86cdfd8b32
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326911"
---
# <a name="onenoteoperation-resource-type"></a><span data-ttu-id="583c4-103">Tipo de recurso onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="583c4-103">onenoteOperation resource type</span></span>

<span data-ttu-id="583c4-104">Estado de ciertas operaciones de OneNote de larga duración.</span><span class="sxs-lookup"><span data-stu-id="583c4-104">The status of certain long-running OneNote operations.</span></span>

## <a name="json-representation"></a><span data-ttu-id="583c4-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="583c4-105">JSON representation</span></span>

<span data-ttu-id="583c4-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="583c4-106">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="583c4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="583c4-107">Properties</span></span>
| <span data-ttu-id="583c4-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="583c4-108">Property</span></span>     | <span data-ttu-id="583c4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="583c4-109">Type</span></span>   |<span data-ttu-id="583c4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="583c4-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="583c4-111">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="583c4-111">createdDateTime</span></span>| <span data-ttu-id="583c4-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="583c4-112">DateTimeOffset</span></span> |<span data-ttu-id="583c4-113">La hora de inicio de la operación.</span><span class="sxs-lookup"><span data-stu-id="583c4-113">The start time of the operation.</span></span>|
|<span data-ttu-id="583c4-114">error</span><span class="sxs-lookup"><span data-stu-id="583c4-114">error</span></span>|[<span data-ttu-id="583c4-115">onenoteOperationError</span><span class="sxs-lookup"><span data-stu-id="583c4-115">onenoteOperationError</span></span>](onenoteoperationerror.md)|<span data-ttu-id="583c4-116">Error devuelto por la operación.</span><span class="sxs-lookup"><span data-stu-id="583c4-116">The error returned by the operation.</span></span>|
|<span data-ttu-id="583c4-117">id</span><span class="sxs-lookup"><span data-stu-id="583c4-117">id</span></span>|<span data-ttu-id="583c4-118">string</span><span class="sxs-lookup"><span data-stu-id="583c4-118">string</span></span>|<span data-ttu-id="583c4-119">Id. de operación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="583c4-119">The operation id. Read-only.</span></span>|
|<span data-ttu-id="583c4-120">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="583c4-120">lastActionDateTime</span></span>| <span data-ttu-id="583c4-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="583c4-121">DateTimeOffset</span></span> |<span data-ttu-id="583c4-122">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="583c4-122">The time of the last action of the operation.</span></span>|
|<span data-ttu-id="583c4-123">resourceId</span><span class="sxs-lookup"><span data-stu-id="583c4-123">resourceId</span></span>|<span data-ttu-id="583c4-124">string</span><span class="sxs-lookup"><span data-stu-id="583c4-124">string</span></span>|<span data-ttu-id="583c4-125">Identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="583c4-125">The resource id.</span></span>|
|<span data-ttu-id="583c4-126">resourceLocation</span><span class="sxs-lookup"><span data-stu-id="583c4-126">resourceLocation</span></span>|<span data-ttu-id="583c4-127">string</span><span class="sxs-lookup"><span data-stu-id="583c4-127">string</span></span>|<span data-ttu-id="583c4-p101">URI de recurso del objeto. Por ejemplo, el URI de recurso de una página o sección copiada.</span><span class="sxs-lookup"><span data-stu-id="583c4-p101">The resource URI for the object. For example, the resource URI for a copied page or section.</span></span> |
|<span data-ttu-id="583c4-130">status</span><span class="sxs-lookup"><span data-stu-id="583c4-130">status</span></span>|<span data-ttu-id="583c4-131">cadena</span><span class="sxs-lookup"><span data-stu-id="583c4-131">string</span></span>|<span data-ttu-id="583c4-132">Estado actual de la operación: `notstarted`, `running`, `completed` o `failed`</span><span class="sxs-lookup"><span data-stu-id="583c4-132">The current status of the operation: `notstarted`, `running`, `completed`, `failed`</span></span> |
|<span data-ttu-id="583c4-133">percentComplete</span><span class="sxs-lookup"><span data-stu-id="583c4-133">percentComplete</span></span>|<span data-ttu-id="583c4-134">cadena</span><span class="sxs-lookup"><span data-stu-id="583c4-134">string</span></span>|<span data-ttu-id="583c4-135">El porcentaje de operación completada si la operación todavía tiene el estado `running`</span><span class="sxs-lookup"><span data-stu-id="583c4-135">The operation percent complete if the operation is still in `running` status</span></span>

## <a name="relationships"></a><span data-ttu-id="583c4-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="583c4-136">Relationships</span></span>
<span data-ttu-id="583c4-137">Ninguno</span><span class="sxs-lookup"><span data-stu-id="583c4-137">None</span></span>


## <a name="methods"></a><span data-ttu-id="583c4-138">Métodos</span><span class="sxs-lookup"><span data-stu-id="583c4-138">Methods</span></span>

| <span data-ttu-id="583c4-139">Método</span><span class="sxs-lookup"><span data-stu-id="583c4-139">Method</span></span>           | <span data-ttu-id="583c4-140">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="583c4-140">Return Type</span></span>    |<span data-ttu-id="583c4-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="583c4-141">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="583c4-142">Obtener operation</span><span class="sxs-lookup"><span data-stu-id="583c4-142">Get operation</span></span>](../api/onenoteoperation-get.md) | [<span data-ttu-id="583c4-143">onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="583c4-143">onenoteOperation</span></span>](onenoteoperation.md) |<span data-ttu-id="583c4-144">Obtener el estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="583c4-144">Get the status of the operation.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
