---
title: Tipo de recurso plannerBucketTaskBoardTaskFormat
description: El recurso **plannerBucketTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Depósitos del panel de tareas (una vista organizada por tareas dentro de los depósitos a los que están asignadas). Cada task tendrá un objeto **plannerBucketTaskBoardTaskFormat** asociado.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: ea557bad20aa0fd10a73e71902b959913e8fff12
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986197"
---
# <a name="plannerbuckettaskboardtaskformat-resource-type"></a><span data-ttu-id="699ff-104">Tipo de recurso plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="699ff-104">plannerBucketTaskBoardTaskFormat resource type</span></span>

> <span data-ttu-id="699ff-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="699ff-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="699ff-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="699ff-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="699ff-p103">El recurso **plannerBucketTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Depósitos del panel de tareas (una vista organizada por tareas dentro de los depósitos a los que están asignadas). Cada [task](plannertask.md) tendrá un objeto **plannerBucketTaskBoardTaskFormat** asociado.</span><span class="sxs-lookup"><span data-stu-id="699ff-p103">The **plannerBucketTaskBoardTaskFormat** resource represents the information used to render a task correctly in the Buckets view of the Task Board (a view organized by tasks within the buckets they are assigned to). Each [task](plannertask.md) will have one **plannerBucketTaskBoardTaskFormat** object associated with it.</span></span>


## <a name="methods"></a><span data-ttu-id="699ff-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="699ff-109">Methods</span></span>

| <span data-ttu-id="699ff-110">Método</span><span class="sxs-lookup"><span data-stu-id="699ff-110">Method</span></span>           | <span data-ttu-id="699ff-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="699ff-111">Return Type</span></span>    |<span data-ttu-id="699ff-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="699ff-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="699ff-113">Obtener plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="699ff-113">Get plannerBucketTaskBoardTaskFormat</span></span>](../api/plannerbuckettaskboardtaskformat-get.md) | [<span data-ttu-id="699ff-114">plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="699ff-114">plannerBucketTaskBoardTaskFormat</span></span>](plannerbuckettaskboardtaskformat.md) |<span data-ttu-id="699ff-115">Leer las propiedades y las relaciones del objeto **plannerBucketTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="699ff-115">Read properties and relationships of **plannerBucketTaskBoardTaskFormat** object.</span></span>|
|[<span data-ttu-id="699ff-116">Update</span><span class="sxs-lookup"><span data-stu-id="699ff-116">Update</span></span>](../api/plannerbuckettaskboardtaskformat-update.md) | [<span data-ttu-id="699ff-117">plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="699ff-117">plannerBucketTaskBoardTaskFormat</span></span>](plannerbuckettaskboardtaskformat.md)  |<span data-ttu-id="699ff-118">Actualizar el objeto **plannerBucketTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="699ff-118">Update **plannerBucketTaskBoardTaskFormat** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="699ff-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="699ff-119">Properties</span></span>
| <span data-ttu-id="699ff-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="699ff-120">Property</span></span>     | <span data-ttu-id="699ff-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="699ff-121">Type</span></span>   |<span data-ttu-id="699ff-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="699ff-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="699ff-123">id</span><span class="sxs-lookup"><span data-stu-id="699ff-123">id</span></span>|<span data-ttu-id="699ff-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="699ff-124">String</span></span>| <span data-ttu-id="699ff-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="699ff-125">Read-only.</span></span> <span data-ttu-id="699ff-126">Identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="699ff-126">ID of the resource.</span></span> <span data-ttu-id="699ff-127">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="699ff-127">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="699ff-128">[Validación de formato](tasks-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="699ff-128">[Format validation](tasks-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="699ff-129">orderHint</span><span class="sxs-lookup"><span data-stu-id="699ff-129">orderHint</span></span>|<span data-ttu-id="699ff-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="699ff-130">String</span></span>|<span data-ttu-id="699ff-p105">Sugerencia usada para ordenar tareas en la vista Depósito del panel de tareas. El formato se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="699ff-p105">Hint used to order tasks in the Bucket view of the Task Board. The format is defined as outlined [here](planner-order-hint-format.md).</span></span>|

## <a name="relationships"></a><span data-ttu-id="699ff-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="699ff-133">Relationships</span></span>
<span data-ttu-id="699ff-134">Ninguno</span><span class="sxs-lookup"><span data-stu-id="699ff-134">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="699ff-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="699ff-135">JSON representation</span></span>
<span data-ttu-id="699ff-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="699ff-136">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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
