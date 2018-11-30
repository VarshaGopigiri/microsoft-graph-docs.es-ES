---
title: Tipo de recurso plannerBucketTaskBoardTaskFormat
description: El recurso **plannerBucketTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Depósitos del panel de tareas (una vista organizada por tareas dentro de los depósitos a los que están asignadas). Cada task tendrá un objeto **plannerBucketTaskBoardTaskFormat** asociado.
ms.openlocfilehash: 7fb15bf59b2c7ffc0a515baff7b3f0dda8be179f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029000"
---
# <a name="plannerbuckettaskboardtaskformat-resource-type"></a><span data-ttu-id="77611-104">Tipo de recurso plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="77611-104">plannerBucketTaskBoardTaskFormat resource type</span></span>

<span data-ttu-id="77611-p102">El recurso **plannerBucketTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Depósitos del panel de tareas (una vista organizada por tareas dentro de los depósitos a los que están asignadas). Cada [task](plannertask.md) tendrá un objeto **plannerBucketTaskBoardTaskFormat** asociado.</span><span class="sxs-lookup"><span data-stu-id="77611-p102">The **plannerBucketTaskBoardTaskFormat** resource represents the information used to render a task correctly in the Buckets view of the Task Board (a view organized by tasks within the buckets they are assigned to). Each [task](plannertask.md) will have one **plannerBucketTaskBoardTaskFormat** object associated with it.</span></span>


## <a name="methods"></a><span data-ttu-id="77611-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="77611-107">Methods</span></span>

| <span data-ttu-id="77611-108">Método</span><span class="sxs-lookup"><span data-stu-id="77611-108">Method</span></span>           | <span data-ttu-id="77611-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77611-109">Return Type</span></span>    |<span data-ttu-id="77611-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="77611-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="77611-111">Obtener plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="77611-111">Get plannerBucketTaskBoardTaskFormat</span></span>](../api/plannerbuckettaskboardtaskformat-get.md) | [<span data-ttu-id="77611-112">plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="77611-112">plannerBucketTaskBoardTaskFormat</span></span>](plannerbuckettaskboardtaskformat.md) |<span data-ttu-id="77611-113">Leer las propiedades y las relaciones del objeto **plannerBucketTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="77611-113">Read properties and relationships of **plannerBucketTaskBoardTaskFormat** object.</span></span>|
|[<span data-ttu-id="77611-114">Update</span><span class="sxs-lookup"><span data-stu-id="77611-114">Update</span></span>](../api/plannerbuckettaskboardtaskformat-update.md) | [<span data-ttu-id="77611-115">plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="77611-115">plannerBucketTaskBoardTaskFormat</span></span>](plannerbuckettaskboardtaskformat.md)  |<span data-ttu-id="77611-116">Actualizar el objeto **plannerBucketTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="77611-116">Update **plannerBucketTaskBoardTaskFormat** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="77611-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="77611-117">Properties</span></span>
| <span data-ttu-id="77611-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="77611-118">Property</span></span>     | <span data-ttu-id="77611-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="77611-119">Type</span></span>   |<span data-ttu-id="77611-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="77611-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="77611-121">id</span><span class="sxs-lookup"><span data-stu-id="77611-121">id</span></span>|<span data-ttu-id="77611-122">String</span><span class="sxs-lookup"><span data-stu-id="77611-122">String</span></span>| <span data-ttu-id="77611-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="77611-123">Read-only.</span></span> <span data-ttu-id="77611-124">Identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="77611-124">ID of the resource.</span></span> <span data-ttu-id="77611-125">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="77611-125">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="77611-126">[Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="77611-126">[Format validation](planner-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="77611-127">orderHint</span><span class="sxs-lookup"><span data-stu-id="77611-127">orderHint</span></span>|<span data-ttu-id="77611-128">String</span><span class="sxs-lookup"><span data-stu-id="77611-128">String</span></span>|<span data-ttu-id="77611-p104">Sugerencia usada para ordenar tareas en la vista Depósito del panel de tareas. El formato se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="77611-p104">Hint used to order tasks in the Bucket view of the Task Board. The format is defined as outlined [here](planner-order-hint-format.md).</span></span>|

## <a name="relationships"></a><span data-ttu-id="77611-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="77611-131">Relationships</span></span>
<span data-ttu-id="77611-132">Ninguno</span><span class="sxs-lookup"><span data-stu-id="77611-132">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="77611-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="77611-133">JSON representation</span></span>
<span data-ttu-id="77611-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="77611-134">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.plannerBucketTaskBoardTaskFormat"
}-->

```json
{
  "id": "String (identifier)",
  "orderHint": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerBucketTaskBoardTaskFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->