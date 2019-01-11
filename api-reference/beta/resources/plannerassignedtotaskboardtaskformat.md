---
title: Tipo de recurso plannerAssignedToTaskBoardTaskFormat
description: El recurso **plannerAssignedToTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista AsignadoA del panel de tareas (una vista organizada por usuarios a los que se asignan las tareas). Cada task tendrá un objeto **plannerAssignedToTaskBoardTaskFormat** asociado.
localization_priority: Normal
ms.openlocfilehash: bae551e009faeb40418f10a082bb8955846e8901
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818084"
---
# <a name="plannerassignedtotaskboardtaskformat-resource-type"></a><span data-ttu-id="02703-104">Tipo de recurso plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="02703-104">plannerAssignedToTaskBoardTaskFormat resource type</span></span>

> <span data-ttu-id="02703-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="02703-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="02703-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="02703-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="02703-p103">El recurso **plannerAssignedToTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista AsignadoA del panel de tareas (una vista organizada por usuarios a los que se asignan las tareas). Cada [task](plannertask.md) tendrá un objeto **plannerAssignedToTaskBoardTaskFormat** asociado.</span><span class="sxs-lookup"><span data-stu-id="02703-p103">The **plannerAssignedToTaskBoardTaskFormat** resource represents the information used to render a task correctly in the AssignedTo view of the Task Board (a view organized by users to whom tasks are assigned to). Each [task](plannertask.md) will have one **plannerAssignedToTaskBoardTaskFormat** object associated with it.</span></span>


## <a name="methods"></a><span data-ttu-id="02703-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="02703-109">Methods</span></span>

| <span data-ttu-id="02703-110">Método</span><span class="sxs-lookup"><span data-stu-id="02703-110">Method</span></span>           | <span data-ttu-id="02703-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02703-111">Return Type</span></span>    |<span data-ttu-id="02703-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="02703-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="02703-113">Obtener plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="02703-113">Get plannerAssignedToTaskBoardTaskFormat</span></span>](../api/plannerassignedtotaskboardtaskformat-get.md) | [<span data-ttu-id="02703-114">plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="02703-114">plannerAssignedToTaskBoardTaskFormat</span></span>](plannerassignedtotaskboardtaskformat.md) |<span data-ttu-id="02703-115">Leer las propiedades y las relaciones del objeto **plannerAssignedToTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="02703-115">Read properties and relationships of **plannerAssignedToTaskBoardTaskFormat** object.</span></span>|
|[<span data-ttu-id="02703-116">Update</span><span class="sxs-lookup"><span data-stu-id="02703-116">Update</span></span>](../api/plannerassignedtotaskboardtaskformat-update.md) | [<span data-ttu-id="02703-117">plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="02703-117">plannerAssignedToTaskBoardTaskFormat</span></span>](plannerassignedtotaskboardtaskformat.md)  |<span data-ttu-id="02703-118">Actualizar el objeto **plannerAssignedToTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="02703-118">Update **plannerAssignedToTaskBoardTaskFormat** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="02703-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="02703-119">Properties</span></span>
| <span data-ttu-id="02703-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="02703-120">Property</span></span>     | <span data-ttu-id="02703-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="02703-121">Type</span></span>   |<span data-ttu-id="02703-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="02703-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="02703-123">id</span><span class="sxs-lookup"><span data-stu-id="02703-123">id</span></span>|<span data-ttu-id="02703-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="02703-124">String</span></span>| <span data-ttu-id="02703-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="02703-125">Read-only.</span></span> <span data-ttu-id="02703-126">Identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="02703-126">ID of the resource.</span></span> <span data-ttu-id="02703-127">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="02703-127">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="02703-128">[Validación de formato](tasks-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="02703-128">[Format validation](tasks-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="02703-129">orderHintsByAssignee</span><span class="sxs-lookup"><span data-stu-id="02703-129">orderHintsByAssignee</span></span>|[<span data-ttu-id="02703-130">plannerOrderHintsByAssignee</span><span class="sxs-lookup"><span data-stu-id="02703-130">plannerOrderHintsByAssignee</span></span>](plannerorderhintsbyassignee.md)|<span data-ttu-id="02703-p105">Diccionario de sugerencias usadas para ordenar las tareas en la vista AsignadoA del panel de tareas. La clave de cada entrada es uno de los usuarios a los que se ha asignado la tarea, mientras que el valor es la sugerencia de orden. El formato de cada valor se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="02703-p105">Dictionary of hints used to order tasks on the AssignedTo view of the Task Board. The key of each entry is one of the users the task is assigned to and the value is the order hint. The format of each value is defined as outlined [here](planner-order-hint-format.md).</span></span>|
|<span data-ttu-id="02703-134">unassignedOrderHint</span><span class="sxs-lookup"><span data-stu-id="02703-134">unassignedOrderHint</span></span>|<span data-ttu-id="02703-135">String</span><span class="sxs-lookup"><span data-stu-id="02703-135">String</span></span>|<span data-ttu-id="02703-p106">Valor de sugerencia usado para ordenar la tarea en la vista AsignadoA del panel de tareas si la tarea no está asignada a nadie, o si el diccionario orderHintsByAssignee no proporciona ninguna sugerencia de orden para el usuario al que se ha asignado la tarea. El formato se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="02703-p106">Hint value used to order the task on the AssignedTo view of the Task Board when the task is not assigned to anyone, or if the orderHintsByAssignee dictionary does not provide an order hint for the user the task is assigned to. The format is defined as outlined [here](planner-order-hint-format.md).</span></span>|

## <a name="relationships"></a><span data-ttu-id="02703-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="02703-138">Relationships</span></span>
<span data-ttu-id="02703-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="02703-139">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="02703-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="02703-140">JSON representation</span></span>
<span data-ttu-id="02703-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="02703-141">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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
