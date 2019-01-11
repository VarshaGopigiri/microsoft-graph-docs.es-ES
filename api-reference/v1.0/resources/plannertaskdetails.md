---
title: Tipo de recurso plannerTaskDetails
description: El recurso **plannerTaskDetails** representa la información adicional de una tarea. Cada objeto task tiene un objeto details.
localization_priority: Normal
ms.openlocfilehash: a183ba0f9b19ea2de700913d29e9586442ba2c03
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806578"
---
# <a name="plannertaskdetails-resource-type"></a><span data-ttu-id="d30a7-104">Tipo de recurso plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="d30a7-104">plannerTaskDetails resource type</span></span>

<span data-ttu-id="d30a7-p102">El recurso **plannerTaskDetails** representa la información adicional de una tarea. Cada objeto [task](plannertask.md) tiene un objeto details.</span><span class="sxs-lookup"><span data-stu-id="d30a7-p102">The **plannerTaskDetails** resource represents the additional information about a task. Each [task](plannertask.md) object has a details object.</span></span>


## <a name="methods"></a><span data-ttu-id="d30a7-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="d30a7-107">Methods</span></span>

| <span data-ttu-id="d30a7-108">Método</span><span class="sxs-lookup"><span data-stu-id="d30a7-108">Method</span></span>           | <span data-ttu-id="d30a7-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d30a7-109">Return Type</span></span>    |<span data-ttu-id="d30a7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d30a7-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d30a7-111">Obtener plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="d30a7-111">Get plannerTaskDetails</span></span>](../api/plannertaskdetails-get.md) | [<span data-ttu-id="d30a7-112">plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="d30a7-112">plannerTaskDetails</span></span>](plannertaskdetails.md) |<span data-ttu-id="d30a7-113">Leer las propiedades y las relaciones del objeto **plannerTaskDetails**.</span><span class="sxs-lookup"><span data-stu-id="d30a7-113">Read properties and relationships of **plannerTaskDetails** object.</span></span>|
|[<span data-ttu-id="d30a7-114">Update</span><span class="sxs-lookup"><span data-stu-id="d30a7-114">Update</span></span>](../api/plannertaskdetails-update.md) | [<span data-ttu-id="d30a7-115">plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="d30a7-115">plannerTaskDetails</span></span>](plannertaskdetails.md)    |<span data-ttu-id="d30a7-116">Actualizar el objeto **plannerTaskDetails**.</span><span class="sxs-lookup"><span data-stu-id="d30a7-116">Update **plannerTaskDetails** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="d30a7-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d30a7-117">Properties</span></span>
| <span data-ttu-id="d30a7-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d30a7-118">Property</span></span>     | <span data-ttu-id="d30a7-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="d30a7-119">Type</span></span>   |<span data-ttu-id="d30a7-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d30a7-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d30a7-121">checklist</span><span class="sxs-lookup"><span data-stu-id="d30a7-121">checklist</span></span>|[<span data-ttu-id="d30a7-122">plannerChecklistItems</span><span class="sxs-lookup"><span data-stu-id="d30a7-122">plannerChecklistItems</span></span>](plannerchecklistitems.md)|<span data-ttu-id="d30a7-123">Colección de elementos de la lista de comprobación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d30a7-123">The collection of checklist items on the task.</span></span>|
|<span data-ttu-id="d30a7-124">description</span><span class="sxs-lookup"><span data-stu-id="d30a7-124">description</span></span>|<span data-ttu-id="d30a7-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="d30a7-125">String</span></span>|<span data-ttu-id="d30a7-126">Descripción de la tarea</span><span class="sxs-lookup"><span data-stu-id="d30a7-126">Description of the task</span></span>|
|<span data-ttu-id="d30a7-127">id</span><span class="sxs-lookup"><span data-stu-id="d30a7-127">id</span></span>|<span data-ttu-id="d30a7-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="d30a7-128">String</span></span>| <span data-ttu-id="d30a7-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d30a7-129">Read-only.</span></span> <span data-ttu-id="d30a7-130">Identificador de los detalles de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d30a7-130">ID of the task details.</span></span> <span data-ttu-id="d30a7-131">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d30a7-131">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="d30a7-132">[Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="d30a7-132">[Format validation](planner-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="d30a7-133">previewType</span><span class="sxs-lookup"><span data-stu-id="d30a7-133">previewType</span></span>|<span data-ttu-id="d30a7-134">string</span><span class="sxs-lookup"><span data-stu-id="d30a7-134">string</span></span>|<span data-ttu-id="d30a7-135">Esto establece el tipo de vista previa que se muestra en la tarea.</span><span class="sxs-lookup"><span data-stu-id="d30a7-135">This sets the type of preview that shows up on the task.</span></span> <span data-ttu-id="d30a7-136">Los valores posibles son: `automatic`, `noPreview`, `checklist`, `description`, `reference`.</span><span class="sxs-lookup"><span data-stu-id="d30a7-136">The possible values are: `automatic`, `noPreview`, `checklist`, `description`, `reference`.</span></span> <span data-ttu-id="d30a7-137">Cuando se establece en `automatic` la vista previa que se muestra es elegida por la aplicación de visualización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d30a7-137">When set to `automatic` the displayed preview is chosen by the app viewing the task.</span></span>|
|<span data-ttu-id="d30a7-138">references</span><span class="sxs-lookup"><span data-stu-id="d30a7-138">references</span></span>|[<span data-ttu-id="d30a7-139">plannerExternalReferences</span><span class="sxs-lookup"><span data-stu-id="d30a7-139">plannerExternalReferences</span></span>](plannerexternalreferences.md)|<span data-ttu-id="d30a7-140">La colección de referencias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d30a7-140">The collection of references on the task.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d30a7-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d30a7-141">Relationships</span></span>
<span data-ttu-id="d30a7-142">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d30a7-142">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="d30a7-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d30a7-143">JSON representation</span></span>
<span data-ttu-id="d30a7-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d30a7-144">Here is a JSON representation of the resource.</span></span>

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
