---
title: Usar el organizador de la API de REST
description: Puede usar la API de organizador en Microsoft Graph para crear tareas y asignarlas a los usuarios de un grupo de Office 365.
ms.openlocfilehash: b1ec3f6e179f05a41fa30aec1697c9bfcefad7ee
ms.sourcegitcommit: 02ead22efd4f10cd50f89c9f5aa3b6dfda96aeec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/01/2018
ms.locfileid: "27123955"
---
# <a name="use-the-planner-rest-api"></a>Usar el organizador de la API de REST

Puede usar la API de organizador en Microsoft Graph para crear tareas y asignarlas a los usuarios de un grupo de Office 365.

Antes de empezar a trabajar con la API de organizador, desea comprender cómo los objetos principales se relacionan entre sí, así como para los grupos de Office 365.

## <a name="office-365-groups"></a>Grupos de Office 365

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

Aparte de los datos de tareas y plan, la API de organizador también proporciona recursos para la creación de una visualización de datos comunes entre los clientes. Varios tipos de datos de visualización están disponibles para tareas, como se muestra en la siguiente tabla.

| Las tareas se muestran como                                                                        | Las tareas se ordenan con información de                                         |
| :---------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------ |
| Lista plana (tareas de un plan)                                                               | La propiedad `orderHint` en las tareas                                                   |
| Lista plana (tareas asignadas a un usuario)                                                      | La propiedad `assigneePriority` en las tareas                                            |
| Vista de panel con columnas para los usuarios asignados (asignados a un panel de tareas)                            | El objeto [assignedToTaskBoardTaskFormat](plannerassignedtotaskboardtaskformat.md) |
| Vista de panel con columnas con el progreso de la tarea hacia su finalización (panel de tareas en curso) | El objeto [progressTaskBoardTaskFormat](plannerprogresstaskboardtaskformat.md)     |
| Vista de panel con columnas personalizadas de tareas (panel de tareas de depósito):                              | El objeto [bucketTaskBoardTaskFormat](plannerbuckettaskboardtaskformat.md)         |

Las columnas personalizadas del panel de tareas de depósito se representan mediante objetos [bucket](plannerbucket.md) y su orden mediante la propiedad `orderHint` en el objeto.

El orden se controla mediante los principios descritos en [sugerencias de orden del organizador](planner-order-hint-format.md).

## <a name="planner-resource-versioning"></a>Control de versiones de los recursos de Planner

Versiones de organizador todos los recursos mediante **etags**. Estos **etags** se devuelven con `@odata.etag` (propiedad) en cada recurso. `PATCH`y `DELETE` solicitudes requieren la última **etag** conocidos por el cliente que se especifique con una `If-Match` encabezado.
Organizador de permite que los cambios realizados en las versiones anteriores de recursos, si el cambio previsto no entre en conflicto con los cambios más recientes aceptados por el servicio de organizador en el mismo recurso. Los clientes pueden identificar qué **etag** para el mismo recurso es más reciente mediante el cálculo de qué valor **etag** es mayor en comparación de cadenas ordinal. Cada recurso tiene un único **valor etag**. Los valores de eTag para los distintos recursos, las relaciones de contención, incluidas no se pueden comparar.
Las aplicaciones cliente se espera que controlen el control de versiones relacionados con [códigos de error](/graph/errors) **409** y **412** al leer la versión más reciente del elemento y resolver los cambios en conflicto.

## <a name="common-planner-error-conditions"></a>Condiciones de error comunes de Planner

Además de los [errores generales](/graph/errors) que se aplican a Microsoft Graph, hay algunas condiciones de error específicas de la API de Planner.

### <a name="400-bad-request"></a>400 Solicitud incorrecta

En algunos escenarios comunes, `POST` y `PATCH` solicitudes pueden devolver un código de 400 estado. Las siguientes son algunas de las causas comunes:

* Las propiedades de tipo abierto no son del tipo correcto, o el tipo no se ha especificado, o no contienen ninguna propiedad. Por ejemplo, las propiedades [plannerAssignments](plannerassignments.md) con valores complejos necesitan declarar la propiedad `@odata.type` con el valor `microsoft.graph.plannerAssignment`.
* Los valores de sugerencia de orden no tienen el [formato correcto](planner-order-hint-format.md). Por ejemplo, un valor de sugerencia de orden se ha establecido directamente en el valor devuelto al cliente.
* Los datos no tienen coherencia lógica. Por ejemplo, la fecha de inicio de la tarea es posterior a la fecha de vencimiento de la tarea.

### <a name="403-forbidden"></a>403 Prohibido

Además de los errores generales, la API de organizador también devuelve el código de 403 estado cuando se ha superado un límite definido por el servicio. Si este es el caso, el `code` (propiedad) en el tipo de recurso de error que le indicará el tipo de la excede el límite por la solicitud.
Los siguientes son los valores posibles para los tipos de límite.

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
| MaximumPlannerPlans       | El grupo ya contiene un Plan. Actualmente, los grupos sólo pueden contener un Plan. **Nota:** Algunas aplicaciones de Microsoft pueden superar este límite. En el futuro, extenderemos esta funcionalidad para todas las aplicaciones.                                                                                                      |

### <a name="412-precondition-failed"></a>412 Error de condición previa 

Todas las API de plana `POST`, `PATCH`, y `DELETE` las solicitudes requieren la `If-Match` encabezado a especificarse con el último valor conocido etag del recurso que está sujeto a la solicitud.
También se puede devolver el código de 412 estado si el valor de etag especificado en la solicitud ya no coincide con una versión del recurso en el servicio. En este caso, los clientes deben volver a leer el recurso y obtener un nuevo valor de etag.

