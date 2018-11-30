---
title: Usar el organizador de la API de REST
description: Puede usar la API de organizador en Microsoft Graph para crear tareas y asignarlas a los usuarios de un grupo de Office 365.
ms.openlocfilehash: 1befd7a7e504aa8f568c9b28bc8a08322064bd37
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030537"
---
# <a name="use-the-planner-rest-api"></a>Usar el organizador de la API de REST

Puede usar la API de organizador en Microsoft Graph para crear tareas y asignarlas a los usuarios de un grupo de Office 365.

Antes de empezar a trabajar con la API de organizador, merece la pena comprender cómo los objetos principales se relacionan entre sí, así como para los grupos de Office 365.

## <a name="groups"></a>Groups

Los grupos de Office 365 son los propietarios de los planes de la API de organizador.
Para [obtener los planes que pertenecen a un grupo](../api/plannergroup-list-plans.md), realizar la siguiente solicitud HTTP.

``` http
GET /groups/{id}/planner/plans
```

Al [crear un nuevo plan](../api/planner-post-plans.md), realizar su propietario de un grupo mediante la configuración de la `owner` (propiedad) en un objeto de plan. Planes deben pertenecer a grupos.

>**Nota:** El usuario que está creando el plan debe ser miembro del grupo que será el propietario del plan. Cuando se crea un nuevo grupo mediante el uso de [Create group](../api/group-post-groups.md), no se agregan al grupo como un miembro. Una vez creado el grupo, agregarse como un miembro mediante el uso [grupo post (miembros)](../api/group-post-members.md).

## <a name="plans"></a>Planes

[Planes de](plannerplan.md) son los contenedores de [tareas](plannertask.md). Para [crear una tarea en un plan](../api/planner-post-tasks.md), establezca el `planId` (propiedad) en el objeto de tarea para el identificador del plan durante la creación de la tarea.
Actualmente no se pueden crear tareas sin planes.
Para [recuperar las tareas de un plan](../api/plannerplan-list-tasks.md), realizar la siguiente solicitud HTTP.

``` http
GET /planner/plans/{id}/tasks
```

## <a name="tasks"></a>Tareas

Cada tarea puede asignarse a un usuario mediante la adición de una [asignación](plannerassignment.md) en la propiedad [assignments](plannerassignments.md) del objeto de tarea. El identificador del usuario al que se va a asignar la tarea es el nombre de la propiedad abierta en `assignments`, y es necesario especificar la propiedad `orderHint` en la asignación.

## <a name="task-and-plan-details"></a>Detalles de la tarea y del plan 

Los recursos de Planner se organizan en objetos básicos y objetos de detalle. Los objetos básicos proporcionan acceso a propiedades comunes de los recursos, lo que es adecuado para vistas de lista, mientras que los objetos de detalle proporcionan acceso a propiedades grandes de los recursos, lo que es adecuado para vistas detalladas.

## <a name="visualization"></a>Visualización

Además de datos de la tarea y del plan, la API de Planner también ofrece recursos para proporcionar la visualización común de datos de los clientes. Hay varios tipos de datos de visualización disponibles para las tareas:

| Las tareas se muestran como                                                                        | Las tareas se ordenan con información de                                         |
| :---------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------ |
| Lista plana (tareas de un plan)                                                               | La propiedad `orderHint` en las tareas                                                   |
| Lista plana (tareas asignadas a un usuario)                                                      | La propiedad `assigneePriority` en las tareas                                            |
| Vista de panel con columnas para los usuarios asignados (asignados a un panel de tareas)                            | El objeto [assignedToTaskBoardTaskFormat](plannerassignedtotaskboardtaskformat.md) |
| Vista de panel con columnas con el progreso de la tarea hacia su finalización (panel de tareas en curso) | El objeto [progressTaskBoardTaskFormat](plannerprogresstaskboardtaskformat.md)     |
| Vista de panel con columnas personalizadas de tareas (panel de tareas de depósito):                              | El objeto [bucketTaskBoardTaskFormat](plannerbuckettaskboardtaskformat.md)         |

Las columnas personalizadas del panel de tareas de depósito se representan mediante objetos [bucket](plannerbucket.md) y su orden mediante la propiedad `orderHint` en el objeto.

El orden se controla mediante los principios indicados en [Planner order hints](planner-order-hint-format.md) (Sugerencias sobre el orden de Planner).

## <a name="planner-resource-versioning"></a>Control de versiones de los recursos de Planner

Planner controla las versiones de todos los recursos mediante ETags. Estas ETags se devuelven con la propiedad `@odata.etag` de cada recurso, y las solicitudes `PATCH` y `DELETE` requieren que se especifique con el encabezado `If-Match` la última ETag conocida por el cliente. Planner permite realizar cambios en las versiones anteriores de los recursos, siempre y cuando el cambio deseado no entre en conflicto con los cambios más recientes aceptados por el servicio de Planner en el mismo recurso. Los clientes pueden identificar qué ETag del recurso es más reciente si calculan qué valor de ETag es mayor en una comparación de cadenas ordinal. Cada recurso tiene una ETag independiente. No se pueden comparar valores de ETag de recursos diferentes, incluidos los que tienen relaciones de contención. Se espera que las aplicaciones cliente controlen dos códigos de estado de error (409 y 412) relacionados con el control de versiones. Para ello, leen la versión más reciente del elemento y resuelven los cambios que entran en conflicto.

## <a name="common-planner-error-conditions"></a>Condiciones de error comunes de Planner

Además de los [errores generales](/graph/errors) que se aplican a Microsoft Graph, hay algunas condiciones de error específicas de la API de Planner.

### <a name="400-bad-request"></a>400 Solicitud incorrecta

Hay varios casos comunes en los que las solicitudes `POST` y `PATCH` pueden obtener un código de estado 400. Entre los problemas frecuentes se incluyen los siguientes:

* Las propiedades de tipo abierto no son del tipo correcto, o el tipo no se ha especificado, o no contienen ninguna propiedad. Por ejemplo, las propiedades [plannerAssignments](plannerassignments.md) con valores complejos necesitan declarar la propiedad `@odata.type` con el valor `microsoft.graph.plannerAssignment`.
* Los valores de sugerencia de orden no tienen el [formato correcto](planner-order-hint-format.md). Por ejemplo, un valor de sugerencia de orden se ha establecido directamente en el valor devuelto al cliente.
* Los datos no tienen coherencia lógica. Por ejemplo, la fecha de inicio de la tarea es posterior a la fecha de vencimiento de la tarea.

### <a name="403-forbidden"></a>403 Prohibido

Además de los errores generales, la API de Planner también devuelve este código de estado cuando se ha excedido un límite definido por el servicio. Si este es el caso, la propiedad `code` del tipo de recurso de error indicará el tipo del límite superado por la solicitud. Los valores posibles para los tipos de límite incluyen los siguientes:

| Valor                         | Descripción                                                                                                                                                                                              |
| :---------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| MaximumProjectsOwnedByUser    | Se ha superado el límite máximo de planes de un grupo. Este límite se basa en la propiedad `owner` del recurso [plannerPlan](plannerplan.md).                                         |
| MaximumProjectsSharedWithUser | Se ha superado el límite máximo de planes compartidos con un usuario.  Este límite se basa en la propiedad `sharedWith` del recurso [plannerPlanDetails](plannerplandetails.md).                   |
| MaximumTasksCreatedByUser     | Se ha superado el límite máximo de tareas creadas por un usuario. Este límite se basa en la propiedad `createdBy` del recurso [plannerTask](plannertask.md).                                    |
| MaximumTasksAssignedToUser    | Se ha superado el límite máximo de tareas asignadas a un usuario. Este límite se basa en la propiedad `assignments` del recurso [plannerTask](plannertask.md).                                 |
| MaximumTasksInProject         | Se ha superado el límite máximo de tareas de un plan. Este límite se basa en la propiedad `planId` del recurso [plannerTask](plannertask.md).                                               |
| MaximumActiveTasksInProject   | Se ha superado el límite máximo de tareas no completadas en un plan. Este límite se basa en las propiedades `planId` y `percentComplete` del recurso [plannerTask](plannertask.md). |
| MaximumBucketsInProject       | Se ha superado el límite máximo de depósitos de un plan. Este límite se basa en la propiedad `planId` del recurso [plannerBucket](plannerbucket.md).                                         |
| MaximumUsersSharedWithProject | La propiedad `sharedWith` del recurso [plannerPlanDetails](plannerplandetails.md) contiene demasiados valores.                                                                                          |
| MaximumReferencesOnTask       | La propiedad `references` del recurso [plannerTaskDetails](plannertaskdetails.md) contiene demasiados valores.                                                                                          |
| MaximumChecklistItemsOnTask   | La propiedad `checklist` del recurso [plannerTaskDetails](plannertaskdetails.md) contiene demasiados valores.                                                                                           |
| MaximumAssigneesInTasks       | La propiedad `assignments` del recurso [plannerTask](plannertask.md) contiene demasiados valores.                                                                                                       |

### <a name="412-precondition-failed"></a>412 Error de condición previa 

Todas las solicitudes `POST`, `PATCH` y `DELETE` de la API de Planner requieren que se especifique un encabezado `If-Match` con el último valor de ETag conocido del recurso que está sujeto a la solicitud. Además, se puede devolver el código de estado 412 si el valor de ETag especificado en la solicitud ya no coincide con una versión del recurso del servicio. En este caso, los clientes deben volver a leer el recurso y obtener una nueva ETag.

