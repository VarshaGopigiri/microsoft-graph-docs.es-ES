---
title: Tipo de recurso plannerTaskDetails
description: El recurso **plannerTaskDetails** representa la información adicional de una tarea. Cada objeto task tiene un objeto details.
localization_priority: Normal
ms.openlocfilehash: 0bec5b47d1472eae43906841c5074e4080672817
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888168"
---
# <a name="plannertaskdetails-resource-type"></a><span data-ttu-id="a8d4f-104">Tipo de recurso plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="a8d4f-104">plannerTaskDetails resource type</span></span>

> <span data-ttu-id="a8d4f-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a8d4f-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a8d4f-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a8d4f-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a8d4f-p103">El recurso **plannerTaskDetails** representa la información adicional de una tarea. Cada objeto [task](plannertask.md) tiene un objeto details.</span><span class="sxs-lookup"><span data-stu-id="a8d4f-p103">The **plannerTaskDetails** resource represents the additional information about a task. Each [task](plannertask.md) object has a details object.</span></span>


## <a name="methods"></a><span data-ttu-id="a8d4f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a8d4f-109">Methods</span></span>

| <span data-ttu-id="a8d4f-110">Método</span><span class="sxs-lookup"><span data-stu-id="a8d4f-110">Method</span></span>           | <span data-ttu-id="a8d4f-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8d4f-111">Return Type</span></span>    |<span data-ttu-id="a8d4f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8d4f-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a8d4f-113">Obtener plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="a8d4f-113">Get plannerTaskDetails</span></span>](../api/plannertaskdetails-get.md) | [<span data-ttu-id="a8d4f-114">plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="a8d4f-114">plannerTaskDetails</span></span>](plannertaskdetails.md) |<span data-ttu-id="a8d4f-115">Leer las propiedades y las relaciones del objeto **plannerTaskDetails**.</span><span class="sxs-lookup"><span data-stu-id="a8d4f-115">Read properties and relationships of **plannerTaskDetails** object.</span></span>|
|[<span data-ttu-id="a8d4f-116">Update</span><span class="sxs-lookup"><span data-stu-id="a8d4f-116">Update</span></span>](../api/plannertaskdetails-update.md) | [<span data-ttu-id="a8d4f-117">plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="a8d4f-117">plannerTaskDetails</span></span>](plannertaskdetails.md)    |<span data-ttu-id="a8d4f-118">Actualizar el objeto **plannerTaskDetails**.</span><span class="sxs-lookup"><span data-stu-id="a8d4f-118">Update **plannerTaskDetails** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="a8d4f-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a8d4f-119">Properties</span></span>
| <span data-ttu-id="a8d4f-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a8d4f-120">Property</span></span>     | <span data-ttu-id="a8d4f-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8d4f-121">Type</span></span>   |<span data-ttu-id="a8d4f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8d4f-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a8d4f-123">checklist</span><span class="sxs-lookup"><span data-stu-id="a8d4f-123">checklist</span></span>|[<span data-ttu-id="a8d4f-124">plannerChecklistItems</span><span class="sxs-lookup"><span data-stu-id="a8d4f-124">plannerChecklistItems</span></span>](plannerchecklistitems.md)|<span data-ttu-id="a8d4f-125">Colección de elementos de la lista de comprobación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a8d4f-125">The collection of checklist items on the task.</span></span>|
|<span data-ttu-id="a8d4f-126">description</span><span class="sxs-lookup"><span data-stu-id="a8d4f-126">description</span></span>|<span data-ttu-id="a8d4f-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="a8d4f-127">String</span></span>|<span data-ttu-id="a8d4f-128">Descripción de la tarea</span><span class="sxs-lookup"><span data-stu-id="a8d4f-128">Description of the task</span></span>|
|<span data-ttu-id="a8d4f-129">id</span><span class="sxs-lookup"><span data-stu-id="a8d4f-129">id</span></span>|<span data-ttu-id="a8d4f-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="a8d4f-130">String</span></span>| <span data-ttu-id="a8d4f-131">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a8d4f-131">Read-only.</span></span> <span data-ttu-id="a8d4f-132">Identificador de los detalles de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a8d4f-132">ID of the task details.</span></span> <span data-ttu-id="a8d4f-133">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a8d4f-133">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="a8d4f-134">[Validación de formato](tasks-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="a8d4f-134">[Format validation](tasks-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="a8d4f-135">previewType</span><span class="sxs-lookup"><span data-stu-id="a8d4f-135">previewType</span></span>|<span data-ttu-id="a8d4f-136">string</span><span class="sxs-lookup"><span data-stu-id="a8d4f-136">string</span></span>|<span data-ttu-id="a8d4f-p105">Establece el tipo de vista previa que aparece en la tarea. Los valores posibles son `automatic`, `noPreview`, `checklist`, `description` y `reference`. Si se establece en `automatic`, la aplicación que visualiza la tarea elige la vista previa mostrada.</span><span class="sxs-lookup"><span data-stu-id="a8d4f-p105">This sets the type of preview that shows up on the task. Possible values are: `automatic`, `noPreview`, `checklist`, `description`, `reference`. When set to `automatic` the displayed preview is chosen by the app viewing the task.</span></span>|
|<span data-ttu-id="a8d4f-140">references</span><span class="sxs-lookup"><span data-stu-id="a8d4f-140">references</span></span>|[<span data-ttu-id="a8d4f-141">plannerExternalReferences</span><span class="sxs-lookup"><span data-stu-id="a8d4f-141">plannerExternalReferences</span></span>](plannerexternalreferences.md)|<span data-ttu-id="a8d4f-142">La colección de referencias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a8d4f-142">The collection of references on the task.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a8d4f-143">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a8d4f-143">Relationships</span></span>
<span data-ttu-id="a8d4f-144">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a8d4f-144">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="a8d4f-145">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a8d4f-145">JSON representation</span></span>
<span data-ttu-id="a8d4f-146">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a8d4f-146">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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
