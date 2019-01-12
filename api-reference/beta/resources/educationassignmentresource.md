---
title: tipo de recurso educationAssignmentResource
description: Un objeto contenedor que almacena los recursos asociados a una asignación. El contenedor de agrega la propiedad **distributeForStudentWork** y se indica que se va este recurso
localization_priority: Normal
author: dipakboyed
ms.prod: education
ms.openlocfilehash: eb0879737d0375bf2463268fe29f2c98f2b6ed51
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991352"
---
# <a name="educationassignmentresource-resource-type"></a><span data-ttu-id="dea64-104">tipo de recurso educationAssignmentResource</span><span class="sxs-lookup"><span data-stu-id="dea64-104">educationAssignmentResource resource type</span></span>

> <span data-ttu-id="dea64-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dea64-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dea64-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dea64-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dea64-107">Un objeto contenedor que almacena los recursos asociados a una asignación.</span><span class="sxs-lookup"><span data-stu-id="dea64-107">A wrapper object that stores the resources associated with an assignment.</span></span> <span data-ttu-id="dea64-108">El contenedor agrega la propiedad **distributeForStudentWork** y se indica que este recurso se copiarán en el envío de estudiantes.</span><span class="sxs-lookup"><span data-stu-id="dea64-108">The wrapper adds the **distributeForStudentWork** property and indicates that this resource will be copied to the student submission.</span></span>  <span data-ttu-id="dea64-109">Si el objeto no se copia, cada alumno verán un vínculo para el recurso en la asignación.</span><span class="sxs-lookup"><span data-stu-id="dea64-109">If the object is not copied, each student will see a link to the resource on the assignment.</span></span> <span data-ttu-id="dea64-110">El alumno no podrá actualizar este recurso.</span><span class="sxs-lookup"><span data-stu-id="dea64-110">The student will not be able to update this resource.</span></span> <span data-ttu-id="dea64-111">Se trata de un documento del profesor al alumno con nothing se convierta.</span><span class="sxs-lookup"><span data-stu-id="dea64-111">This is a handout from the teacher to the student with nothing to be turned in.</span></span> <span data-ttu-id="dea64-112">Si el recurso se distribuye, cada estudiante recibirá una copia de este recurso en la lista de recursos de su presentación.</span><span class="sxs-lookup"><span data-stu-id="dea64-112">If the resource is distributed, each student will receive a copy of this resource in the resource list of their submission.</span></span> <span data-ttu-id="dea64-113">Cada alumno será capaz de modificar su copia y enviar para clasificación.</span><span class="sxs-lookup"><span data-stu-id="dea64-113">Each student will be able to modify their copy and submit it for grading.</span></span>


## <a name="methods"></a><span data-ttu-id="dea64-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="dea64-114">Methods</span></span>

| <span data-ttu-id="dea64-115">Método</span><span class="sxs-lookup"><span data-stu-id="dea64-115">Method</span></span>           | <span data-ttu-id="dea64-116">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dea64-116">Return Type</span></span>    |<span data-ttu-id="dea64-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="dea64-117">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="dea64-118">Obtener educationAssignmentResource</span><span class="sxs-lookup"><span data-stu-id="dea64-118">Get educationAssignmentResource</span></span>](../api/educationassignmentresource-get.md) | [<span data-ttu-id="dea64-119">educationAssignmentResource</span><span class="sxs-lookup"><span data-stu-id="dea64-119">educationAssignmentResource</span></span>](educationassignmentresource.md) |<span data-ttu-id="dea64-120">Leer las propiedades y relaciones de un objeto **educationAssignmentResource** .</span><span class="sxs-lookup"><span data-stu-id="dea64-120">Read properties and relationships of an **educationAssignmentResource** object.</span></span>|
|[<span data-ttu-id="dea64-121">Update</span><span class="sxs-lookup"><span data-stu-id="dea64-121">Update</span></span>](../api/educationassignmentresource-update.md) | [<span data-ttu-id="dea64-122">educationAssignmentResource</span><span class="sxs-lookup"><span data-stu-id="dea64-122">educationAssignmentResource</span></span>](educationassignmentresource.md) |<span data-ttu-id="dea64-123">Actualizar un objeto **educationAssignmentResource** .</span><span class="sxs-lookup"><span data-stu-id="dea64-123">Update an **educationAssignmentResource** object.</span></span> |
|[<span data-ttu-id="dea64-124">Delete</span><span class="sxs-lookup"><span data-stu-id="dea64-124">Delete</span></span>](../api/educationassignmentresource-delete.md) | <span data-ttu-id="dea64-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="dea64-125">None</span></span> |<span data-ttu-id="dea64-126">Eliminación de un objeto **educationAssignmentResource** .</span><span class="sxs-lookup"><span data-stu-id="dea64-126">Delete an **educationAssignmentResource** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="dea64-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dea64-127">Properties</span></span>
| <span data-ttu-id="dea64-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dea64-128">Property</span></span>     | <span data-ttu-id="dea64-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="dea64-129">Type</span></span>   |<span data-ttu-id="dea64-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="dea64-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dea64-131">distributeForStudentWork</span><span class="sxs-lookup"><span data-stu-id="dea64-131">distributeForStudentWork</span></span>|<span data-ttu-id="dea64-132">Booleano</span><span class="sxs-lookup"><span data-stu-id="dea64-132">Boolean</span></span>|<span data-ttu-id="dea64-133">Indica si se debe copiar este recurso a cada envío estudiantes para el tipo de modificación y envío.</span><span class="sxs-lookup"><span data-stu-id="dea64-133">Indicates whether this resource should be copied to each student submission for modification and submission.</span></span>|
|<span data-ttu-id="dea64-134">id</span><span class="sxs-lookup"><span data-stu-id="dea64-134">id</span></span>|<span data-ttu-id="dea64-135">String</span><span class="sxs-lookup"><span data-stu-id="dea64-135">String</span></span>| <span data-ttu-id="dea64-136">Identificador de este recurso.</span><span class="sxs-lookup"><span data-stu-id="dea64-136">ID of this resource.</span></span> <span data-ttu-id="dea64-137">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dea64-137">Read-only.</span></span>|
|<span data-ttu-id="dea64-138">resource</span><span class="sxs-lookup"><span data-stu-id="dea64-138">resource</span></span>|[<span data-ttu-id="dea64-139">educationResource</span><span class="sxs-lookup"><span data-stu-id="dea64-139">educationResource</span></span>](educationresource.md)|<span data-ttu-id="dea64-140">Objeto de recurso que se ha asociado con esta asignación.</span><span class="sxs-lookup"><span data-stu-id="dea64-140">Resource object that has been associated with this assignment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="dea64-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="dea64-141">Relationships</span></span>
<span data-ttu-id="dea64-142">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dea64-142">None.</span></span>


## <a name="json-representation"></a><span data-ttu-id="dea64-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dea64-143">JSON representation</span></span>

<span data-ttu-id="dea64-144">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="dea64-144">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationAssignmentResource"
}-->

```json
{
  "distributeForStudentWork": true,
  "id": "String (identifier)",
  "resource": {"@odata.type": "microsoft.graph.educationResource"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationAssignmentResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
