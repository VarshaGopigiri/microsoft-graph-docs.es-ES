---
title: Tipo de recurso plannerAssignments
description: 'El recurso **plannerAssignments** representa las asignaciones de un recurso de plannerTask. Este tipo es un tipo abierto. Cada nombre de la propiedad en este tipo '
ms.openlocfilehash: 1cb080ff8d66c2319b77dd560f10422e1663a46d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032403"
---
# <a name="plannerassignments-resource-type"></a><span data-ttu-id="0b3ed-105">Tipo de recurso plannerAssignments</span><span class="sxs-lookup"><span data-stu-id="0b3ed-105">plannerAssignments resource type</span></span>

<span data-ttu-id="0b3ed-p102">El recurso **plannerAssignments** representa las asignaciones de un recurso [plannerTask](plannertask.md). Este tipo es un tipo abierto. Cada nombre de propiedad de este tipo es el identificador de un objeto de usuario al que se ha asignado una tarea. Se pueden asignar los usuarios a las tareas creando nuevas propiedades denominadas con sus identificadores, con un objeto [plannerassignment](plannerassignment.md) con la propiedad orderHint cumplimentada como valor. Se puede anular la asignación de la tarea a las personas asignadas estableciendo en null la propiedad denominada con su identificador.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-p102">The **plannerAssignments** resource represents assignments of a [plannerTask](plannertask.md) resource. This type is an open type. Each property name in this type is the ID of a user object a task is assigned to. The users can be assigned to tasks with creating new properties named with their ID, with a [plannerassignment](plannerassignment.md) object with orderHint property populated as the value. The assignees can be unassigned from the task by setting the propety named with their ID to null.</span></span>


## <a name="properties"></a><span data-ttu-id="0b3ed-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b3ed-111">Properties</span></span>
<span data-ttu-id="0b3ed-p103">El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar los identificadores de los usuarios asignados como nombres de propiedad. La propiedad se debe establecer en un objeto **plannerAssignment** para crear o modificar las personas asignadas o en null para quitarlas.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-p103">Properties of an Open Type can be defined by the client. In this case though, the client must provide assigned user's IDs as property names. The property must be set to a **plannerAssignment** object to create or modify assignees, and to null to remove them.</span></span>

<span data-ttu-id="0b3ed-115">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0b3ed-115">Example:</span></span>

<!-- {
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [ "ca2a1df2-e36b-4987-9f6b-0ea462f4eb47", "4e98f8f1-bb03-4015-b8e0-19bb370949d8" ],
  "@odata.type": "microsoft.graph.plannerAssignments"
}-->
```json
{
  "ca2a1df2-e36b-4987-9f6b-0ea462f4eb47": null,
  "4e98f8f1-bb03-4015-b8e0-19bb370949d8": { 
      "@odata.type": "microsoft.graph.plannerAssignment",
      "orderHint": "String"
    }
}
```
<span data-ttu-id="0b3ed-p104">En este ejemplo se quita el usuario con el id. ca2a1df2-e36b-4987-9f6b-0ea462f4eb47 de la lista de personas asignadas de la tarea y se cambia el orden de la persona asignada con el id. de usuario 4e98f8f1-bb03-4015-b8e0-19bb370949d8. Si la tarea todavía no está asignada al usuario con el identificador 4e98f8f1-bb03-4015-b8e0-19bb370949d8, al actualizar las asignaciones con este valor, se asignará la tarea a este usuario.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-p104">This example removes user with ID ca2a1df2-e36b-4987-9f6b-0ea462f4eb47 from the assignees list of the task, while changing the order of the assignee with user ID 4e98f8f1-bb03-4015-b8e0-19bb370949d8. If the task isn't already assigned to user with ID 4e98f8f1-bb03-4015-b8e0-19bb370949d8, updating the assignments with this value will assign the task to this user.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerAssignments resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->