---
title: Tipo de recurso plannerAssignments
description: 'El recurso **plannerAssignments** representa las asignaciones de un recurso de plannerTask. Este tipo es un tipo abierto. Cada nombre de la propiedad en este tipo '
ms.openlocfilehash: b6a6448dac465b8d8ed64c7326ca3475b624c056
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084072"
---
# <a name="plannerassignments-resource-type"></a>Tipo de recurso plannerAssignments

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **plannerAssignments** representa las asignaciones de un recurso [plannerTask](plannertask.md). Este tipo es un tipo abierto. Cada nombre de propiedad de este tipo es el identificador de un objeto de usuario al que se ha asignado una tarea. Se pueden asignar los usuarios a las tareas creando nuevas propiedades denominadas con sus identificadores, con un objeto [plannerassignment](plannerassignment.md) con la propiedad orderHint cumplimentada como valor. Se puede anular la asignación de la tarea a las personas asignadas estableciendo en null la propiedad denominada con su identificador.


## <a name="properties"></a>Propiedades
El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar los identificadores de los usuarios asignados como nombres de propiedad. La propiedad se debe establecer en un objeto **plannerAssignment** para crear o modificar las personas asignadas o en null para quitarlas.

Ejemplo:

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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
En este ejemplo se quita el usuario con el id. ca2a1df2-e36b-4987-9f6b-0ea462f4eb47 de la lista de personas asignadas de la tarea y se cambia el orden de la persona asignada con el id. de usuario 4e98f8f1-bb03-4015-b8e0-19bb370949d8. Si la tarea todavía no está asignada al usuario con el identificador 4e98f8f1-bb03-4015-b8e0-19bb370949d8, al actualizar las asignaciones con este valor, se asignará la tarea a este usuario.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerAssignments resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->