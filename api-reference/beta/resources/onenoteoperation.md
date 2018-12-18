---
title: Tipo de recurso onenoteOperation
description: Estado de ciertas operaciones de OneNote de larga duración.
author: Jewan-microsoft
ms.openlocfilehash: 7835c150cbc06915aa8d4e8f8bf1e1257f341ee4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27338678"
---
# <a name="onenoteoperation-resource-type"></a><span data-ttu-id="f4c36-103">Tipo de recurso onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="f4c36-103">onenoteOperation resource type</span></span>

> <span data-ttu-id="f4c36-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f4c36-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f4c36-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f4c36-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f4c36-106">Estado de ciertas operaciones de OneNote de larga duración.</span><span class="sxs-lookup"><span data-stu-id="f4c36-106">The status of certain long-running OneNote operations.</span></span>

## <a name="json-representation"></a><span data-ttu-id="f4c36-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f4c36-107">JSON representation</span></span>

<span data-ttu-id="f4c36-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f4c36-108">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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
## <a name="properties"></a><span data-ttu-id="f4c36-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4c36-109">Properties</span></span>
| <span data-ttu-id="f4c36-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f4c36-110">Property</span></span>     | <span data-ttu-id="f4c36-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4c36-111">Type</span></span>   |<span data-ttu-id="f4c36-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4c36-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f4c36-113">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f4c36-113">createdDateTime</span></span>| <span data-ttu-id="f4c36-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f4c36-114">DateTimeOffset</span></span> |<span data-ttu-id="f4c36-115">La hora de inicio de la operación.</span><span class="sxs-lookup"><span data-stu-id="f4c36-115">The start time of the operation.</span></span>|
|<span data-ttu-id="f4c36-116">error</span><span class="sxs-lookup"><span data-stu-id="f4c36-116">error</span></span>|[<span data-ttu-id="f4c36-117">onenoteOperationError</span><span class="sxs-lookup"><span data-stu-id="f4c36-117">onenoteOperationError</span></span>](onenoteoperationerror.md)|<span data-ttu-id="f4c36-118">Error devuelto por la operación.</span><span class="sxs-lookup"><span data-stu-id="f4c36-118">The error returned by the operation.</span></span>|
|<span data-ttu-id="f4c36-119">id</span><span class="sxs-lookup"><span data-stu-id="f4c36-119">id</span></span>|<span data-ttu-id="f4c36-120">string</span><span class="sxs-lookup"><span data-stu-id="f4c36-120">string</span></span>|<span data-ttu-id="f4c36-121">Id. de operación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f4c36-121">The operation id. Read-only.</span></span>|
|<span data-ttu-id="f4c36-122">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="f4c36-122">lastActionDateTime</span></span>| <span data-ttu-id="f4c36-123">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f4c36-123">DateTimeOffset</span></span> |<span data-ttu-id="f4c36-124">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="f4c36-124">The time of the last action of the operation.</span></span>|
|<span data-ttu-id="f4c36-125">resourceId</span><span class="sxs-lookup"><span data-stu-id="f4c36-125">resourceId</span></span>|<span data-ttu-id="f4c36-126">string</span><span class="sxs-lookup"><span data-stu-id="f4c36-126">string</span></span>|<span data-ttu-id="f4c36-127">Identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="f4c36-127">The resource id.</span></span>|
|<span data-ttu-id="f4c36-128">resourceLocation</span><span class="sxs-lookup"><span data-stu-id="f4c36-128">resourceLocation</span></span>|<span data-ttu-id="f4c36-129">string</span><span class="sxs-lookup"><span data-stu-id="f4c36-129">string</span></span>|<span data-ttu-id="f4c36-p102">URI de recurso del objeto. Por ejemplo, el URI de recurso de una página o sección copiada.</span><span class="sxs-lookup"><span data-stu-id="f4c36-p102">The resource URI for the object. For example, the resource URI for a copied page or section.</span></span> |
|<span data-ttu-id="f4c36-132">status</span><span class="sxs-lookup"><span data-stu-id="f4c36-132">status</span></span>|<span data-ttu-id="f4c36-133">cadena</span><span class="sxs-lookup"><span data-stu-id="f4c36-133">string</span></span>|<span data-ttu-id="f4c36-134">Estado actual de la operación: `notstarted`, `running`, `completed` o `failed`</span><span class="sxs-lookup"><span data-stu-id="f4c36-134">The current status of the operation: `notstarted`, `running`, `completed`, `failed`</span></span> |
|<span data-ttu-id="f4c36-135">percentComplete</span><span class="sxs-lookup"><span data-stu-id="f4c36-135">percentComplete</span></span>|<span data-ttu-id="f4c36-136">cadena</span><span class="sxs-lookup"><span data-stu-id="f4c36-136">string</span></span>|<span data-ttu-id="f4c36-137">El porcentaje de operación completada si la operación todavía tiene el estado `running`</span><span class="sxs-lookup"><span data-stu-id="f4c36-137">The operation percent complete if the operation is still in `running` status</span></span>

## <a name="relationships"></a><span data-ttu-id="f4c36-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f4c36-138">Relationships</span></span>
<span data-ttu-id="f4c36-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f4c36-139">None</span></span>


## <a name="methods"></a><span data-ttu-id="f4c36-140">Métodos</span><span class="sxs-lookup"><span data-stu-id="f4c36-140">Methods</span></span>

| <span data-ttu-id="f4c36-141">Método</span><span class="sxs-lookup"><span data-stu-id="f4c36-141">Method</span></span>           | <span data-ttu-id="f4c36-142">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4c36-142">Return Type</span></span>    |<span data-ttu-id="f4c36-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4c36-143">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="f4c36-144">Obtener operation</span><span class="sxs-lookup"><span data-stu-id="f4c36-144">Get operation</span></span>](../api/onenoteoperation-get.md) | [<span data-ttu-id="f4c36-145">onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="f4c36-145">onenoteOperation</span></span>](onenoteoperation.md) |<span data-ttu-id="f4c36-146">Obtener el estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="f4c36-146">Get the status of the operation.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
