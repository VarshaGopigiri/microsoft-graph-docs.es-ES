---
title: Tipo de recurso plannerAssignedToTaskBoardTaskFormat
description: El recurso **plannerAssignedToTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista AsignadoA del panel de tareas (una vista organizada por usuarios a los que se asignan las tareas). Cada task tendrá un objeto **plannerAssignedToTaskBoardTaskFormat** asociado.
ms.openlocfilehash: 35aaf5d93e4190fead1234131864e7fab11b96b5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031159"
---
# <a name="plannerassignedtotaskboardtaskformat-resource-type"></a><span data-ttu-id="f1703-104">Tipo de recurso plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="f1703-104">plannerAssignedToTaskBoardTaskFormat resource type</span></span>

<span data-ttu-id="f1703-p102">El recurso **plannerAssignedToTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista AsignadoA del panel de tareas (una vista organizada por usuarios a los que se asignan las tareas). Cada [task](plannertask.md) tendrá un objeto **plannerAssignedToTaskBoardTaskFormat** asociado.</span><span class="sxs-lookup"><span data-stu-id="f1703-p102">The **plannerAssignedToTaskBoardTaskFormat** resource represents the information used to render a task correctly in the AssignedTo view of the Task Board (a view organized by users to whom tasks are assigned to). Each [task](plannertask.md) will have one **plannerAssignedToTaskBoardTaskFormat** object associated with it.</span></span>


## <a name="methods"></a><span data-ttu-id="f1703-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="f1703-107">Methods</span></span>

| <span data-ttu-id="f1703-108">Método</span><span class="sxs-lookup"><span data-stu-id="f1703-108">Method</span></span>           | <span data-ttu-id="f1703-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1703-109">Return Type</span></span>    |<span data-ttu-id="f1703-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1703-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="f1703-111">Obtener plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="f1703-111">Get plannerAssignedToTaskBoardTaskFormat</span></span>](../api/plannerassignedtotaskboardtaskformat-get.md) | [<span data-ttu-id="f1703-112">plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="f1703-112">plannerAssignedToTaskBoardTaskFormat</span></span>](plannerassignedtotaskboardtaskformat.md) |<span data-ttu-id="f1703-113">Leer las propiedades y las relaciones del objeto **plannerAssignedToTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="f1703-113">Read properties and relationships of **plannerAssignedToTaskBoardTaskFormat** object.</span></span>|
|[<span data-ttu-id="f1703-114">Update</span><span class="sxs-lookup"><span data-stu-id="f1703-114">Update</span></span>](../api/plannerassignedtotaskboardtaskformat-update.md) | [<span data-ttu-id="f1703-115">plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="f1703-115">plannerAssignedToTaskBoardTaskFormat</span></span>](plannerassignedtotaskboardtaskformat.md)  |<span data-ttu-id="f1703-116">Actualizar el objeto **plannerAssignedToTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="f1703-116">Update **plannerAssignedToTaskBoardTaskFormat** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="f1703-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f1703-117">Properties</span></span>
| <span data-ttu-id="f1703-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f1703-118">Property</span></span>     | <span data-ttu-id="f1703-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1703-119">Type</span></span>   |<span data-ttu-id="f1703-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1703-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f1703-121">id</span><span class="sxs-lookup"><span data-stu-id="f1703-121">id</span></span>|<span data-ttu-id="f1703-122">String</span><span class="sxs-lookup"><span data-stu-id="f1703-122">String</span></span>| <span data-ttu-id="f1703-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f1703-123">Read-only.</span></span> <span data-ttu-id="f1703-124">Identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="f1703-124">ID of the resource.</span></span> <span data-ttu-id="f1703-125">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f1703-125">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="f1703-126">[Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="f1703-126">[Format validation](planner-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="f1703-127">orderHintsByAssignee</span><span class="sxs-lookup"><span data-stu-id="f1703-127">orderHintsByAssignee</span></span>|[<span data-ttu-id="f1703-128">plannerOrderHintsByAssignee</span><span class="sxs-lookup"><span data-stu-id="f1703-128">plannerOrderHintsByAssignee</span></span>](plannerorderhintsbyassignee.md)|<span data-ttu-id="f1703-p104">Diccionario de sugerencias usadas para ordenar las tareas en la vista AsignadoA del panel de tareas. La clave de cada entrada es uno de los usuarios a los que se ha asignado la tarea, mientras que el valor es la sugerencia de orden. El formato de cada valor se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="f1703-p104">Dictionary of hints used to order tasks on the AssignedTo view of the Task Board. The key of each entry is one of the users the task is assigned to and the value is the order hint. The format of each value is defined as outlined [here](planner-order-hint-format.md).</span></span>|
|<span data-ttu-id="f1703-132">unassignedOrderHint</span><span class="sxs-lookup"><span data-stu-id="f1703-132">unassignedOrderHint</span></span>|<span data-ttu-id="f1703-133">String</span><span class="sxs-lookup"><span data-stu-id="f1703-133">String</span></span>|<span data-ttu-id="f1703-p105">Valor de sugerencia usado para ordenar la tarea en la vista AsignadoA del panel de tareas si la tarea no está asignada a nadie, o si el diccionario orderHintsByAssignee no proporciona ninguna sugerencia de orden para el usuario al que se ha asignado la tarea. El formato se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="f1703-p105">Hint value used to order the task on the AssignedTo view of the Task Board when the task is not assigned to anyone, or if the orderHintsByAssignee dictionary does not provide an order hint for the user the task is assigned to. The format is defined as outlined [here](planner-order-hint-format.md).</span></span>|

## <a name="relationships"></a><span data-ttu-id="f1703-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f1703-136">Relationships</span></span>
<span data-ttu-id="f1703-137">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f1703-137">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="f1703-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f1703-138">JSON representation</span></span>
<span data-ttu-id="f1703-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f1703-139">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.plannerAssignedToTaskBoardTaskFormat"
}-->

```json
{
  "id": "String (identifier)",
  "orderHintsByAssignee": {"@odata.type": "microsoft.graph.plannerOrderHintsByAssignee"},
  "unassignedOrderHint": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerAssignedToTaskBoardTaskFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->