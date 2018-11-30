---
title: Tipo de recurso plannerTaskDetails
description: El recurso **plannerTaskDetails** representa la información adicional de una tarea. Cada objeto task tiene un objeto details.
ms.openlocfilehash: 74ba1c5b7c607f30253463e6cfc256fd3119bf45
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032400"
---
# <a name="plannertaskdetails-resource-type"></a><span data-ttu-id="af079-104">Tipo de recurso plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="af079-104">plannerTaskDetails resource type</span></span>

<span data-ttu-id="af079-p102">El recurso **plannerTaskDetails** representa la información adicional de una tarea. Cada objeto [task](plannertask.md) tiene un objeto details.</span><span class="sxs-lookup"><span data-stu-id="af079-p102">The **plannerTaskDetails** resource represents the additional information about a task. Each [task](plannertask.md) object has a details object.</span></span>


## <a name="methods"></a><span data-ttu-id="af079-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="af079-107">Methods</span></span>

| <span data-ttu-id="af079-108">Método</span><span class="sxs-lookup"><span data-stu-id="af079-108">Method</span></span>           | <span data-ttu-id="af079-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af079-109">Return Type</span></span>    |<span data-ttu-id="af079-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="af079-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="af079-111">Obtener plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="af079-111">Get plannerTaskDetails</span></span>](../api/plannertaskdetails-get.md) | [<span data-ttu-id="af079-112">plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="af079-112">plannerTaskDetails</span></span>](plannertaskdetails.md) |<span data-ttu-id="af079-113">Leer las propiedades y las relaciones del objeto **plannerTaskDetails**.</span><span class="sxs-lookup"><span data-stu-id="af079-113">Read properties and relationships of **plannerTaskDetails** object.</span></span>|
|[<span data-ttu-id="af079-114">Update</span><span class="sxs-lookup"><span data-stu-id="af079-114">Update</span></span>](../api/plannertaskdetails-update.md) | [<span data-ttu-id="af079-115">plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="af079-115">plannerTaskDetails</span></span>](plannertaskdetails.md)    |<span data-ttu-id="af079-116">Actualizar el objeto **plannerTaskDetails**.</span><span class="sxs-lookup"><span data-stu-id="af079-116">Update **plannerTaskDetails** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="af079-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="af079-117">Properties</span></span>
| <span data-ttu-id="af079-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="af079-118">Property</span></span>     | <span data-ttu-id="af079-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="af079-119">Type</span></span>   |<span data-ttu-id="af079-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="af079-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="af079-121">checklist</span><span class="sxs-lookup"><span data-stu-id="af079-121">checklist</span></span>|[<span data-ttu-id="af079-122">plannerChecklistItems</span><span class="sxs-lookup"><span data-stu-id="af079-122">plannerChecklistItems</span></span>](plannerchecklistitems.md)|<span data-ttu-id="af079-123">Colección de elementos de la lista de comprobación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="af079-123">The collection of checklist items on the task.</span></span>|
|<span data-ttu-id="af079-124">description</span><span class="sxs-lookup"><span data-stu-id="af079-124">description</span></span>|<span data-ttu-id="af079-125">String</span><span class="sxs-lookup"><span data-stu-id="af079-125">String</span></span>|<span data-ttu-id="af079-126">Descripción de la tarea</span><span class="sxs-lookup"><span data-stu-id="af079-126">Description of the task</span></span>|
|<span data-ttu-id="af079-127">id</span><span class="sxs-lookup"><span data-stu-id="af079-127">id</span></span>|<span data-ttu-id="af079-128">String</span><span class="sxs-lookup"><span data-stu-id="af079-128">String</span></span>| <span data-ttu-id="af079-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af079-129">Read-only.</span></span> <span data-ttu-id="af079-130">Identificador de los detalles de la tarea.</span><span class="sxs-lookup"><span data-stu-id="af079-130">ID of the task details.</span></span> <span data-ttu-id="af079-131">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="af079-131">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="af079-132">[Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="af079-132">[Format validation](planner-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="af079-133">previewType</span><span class="sxs-lookup"><span data-stu-id="af079-133">previewType</span></span>|<span data-ttu-id="af079-134">string</span><span class="sxs-lookup"><span data-stu-id="af079-134">string</span></span>|<span data-ttu-id="af079-135">Esto establece el tipo de vista previa que se muestra en la tarea.</span><span class="sxs-lookup"><span data-stu-id="af079-135">This sets the type of preview that shows up on the task.</span></span> <span data-ttu-id="af079-136">Los valores posibles son: `automatic`, `noPreview`, `checklist`, `description`, `reference`.</span><span class="sxs-lookup"><span data-stu-id="af079-136">The possible values are: `automatic`, `noPreview`, `checklist`, `description`, `reference`.</span></span> <span data-ttu-id="af079-137">Cuando se establece en `automatic` la vista previa que se muestra es elegida por la aplicación de visualización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="af079-137">When set to `automatic` the displayed preview is chosen by the app viewing the task.</span></span>|
|<span data-ttu-id="af079-138">references</span><span class="sxs-lookup"><span data-stu-id="af079-138">references</span></span>|[<span data-ttu-id="af079-139">plannerExternalReferences</span><span class="sxs-lookup"><span data-stu-id="af079-139">plannerExternalReferences</span></span>](plannerexternalreferences.md)|<span data-ttu-id="af079-140">La colección de referencias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="af079-140">The collection of references on the task.</span></span>|

## <a name="relationships"></a><span data-ttu-id="af079-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="af079-141">Relationships</span></span>
<span data-ttu-id="af079-142">Ninguno</span><span class="sxs-lookup"><span data-stu-id="af079-142">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="af079-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="af079-143">JSON representation</span></span>
<span data-ttu-id="af079-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="af079-144">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.plannerTaskDetails"
}-->

```json
{
  "checklist": {"@odata.type": "microsoft.graph.plannerChecklistItems"},
  "description": "String",
  "id": "String (identifier)",
  "previewType": "string",
  "references": {"@odata.type": "microsoft.graph.plannerExternalReferences"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerTaskDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
