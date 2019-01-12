---
title: Usar el organizador de la API de REST
description: Puede usar la API de organizador en Microsoft Graph para crear tareas y asignarlas a los usuarios de un grupo de Office 365.
author: TarkanSevilmis
localization_priority: Priority
ms.prod: planner
ms.openlocfilehash: 2995cfe32e921889a55ec56c67989ecdfc9716ed
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27942573"
---
# <a name="use-the-planner-rest-api"></a>Usar el organizador de la API de REST

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede usar la API de organizador en Microsoft Graph para crear tareas y asignarlas a los usuarios de un grupo de Office 365.

Antes de empezar a trabajar con la API de organizador, será útil comprender cómo los objetos principales se relacionan entre sí, así como para los grupos de Office 365.

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

## <a name="delta">Realizar un seguimiento de cambios mediante la consulta de delta</a>

Consulta de delta del organizador admite objetos a consultas que el usuario está suscrito a.

Los usuarios se suscriben a los siguientes objetos.

| Tipo de recurso de organizador | Instancias está suscritas                                                                                                                                                                                    |
| :-------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Tareas                 | <ul><li>Creados por el usuario</li><li>Asignados al usuario</li><li>Pertenecen a un plan que posee el usuario</li><li>Contenidos en un plan que se comparten con el usuario a través de la colección de **SharedWith** del plan</li> |
| Planes                 | <ul><li>Compartido con el usuario a través de la colección de **SharedWith** del plan</li></ul>                                                                                                                     |
| Cubos               | <ul><li>Contenidos en un plan que se comparten con el usuario a través de la colección de **SharedWith** del plan</li></ul>                                                                                                 |  |

### <a name="objectcache">Rellenar la caché de objetos para las consultas de delta</a>

Si desea usar la API de consulta delta organizador, mantener una memoria caché local de objetos que el usuario está interesado en observar con el fin de aplicar los cambios de la fuente de respuesta delta.

Los objetos de carga delta que actualmente puede devolver la consulta de delta organizador será de los siguientes tipos:

* [plannerTask](plannertask.md)
* [plannerTaskDetails](plannertaskdetails.md)
* [plannerPlan](plannerplan.md)
* [plannerPlanDetails](plannerplandetails.md)
* [plannerBucket](plannerbucket.md)
* [plannerAssignedToTaskBoardTaskFormat](plannerassignedtotaskboardtaskformat.md)
* [plannerBucketTaskBoardTaskFormat](plannerbuckettaskboardtaskformat.md)
* [plannerAssignedToTaskBoardTaskFormat](plannerassignedtotaskboardtaskformat.md)

Use el correspondiente `GET` métodos en el recurso para obtener el estado inicial de objetos que se rellena en la memoria caché local.

### <a name="differentiating-between-object-creation-and-object-modification"></a>Diferenciarse de creación de objetos y modificación de objeto

En algunos casos, el autor de la llamada puede resultar útil distinguir entre la creación de objetos y modificación del objeto dentro de la consulta de delta del organizador de fuente.

Estas instrucciones se pueden usar para inferir la creación de objetos:

* El `createdBy` (propiedad) sólo aparecerá en objetos recién creados.
* Una recién creada `plannerTask` objeto irá seguido de su correspondiente `plannerTaskDetails` objeto.
* Una recién creada `plannerPlan` objeto irá seguido de su correspondiente `plannerPlanDetails` objeto.

### <a name="usage"></a>Uso

Se espera que el autor de la llamada tiene una memoria caché que contiene los objetos de suscripción. Para obtener información detallada acerca de cómo rellenar la memoria caché local de objetos de suscripción, vea [llenar la memoria caché de objetos para las consultas de delta](#populate-the-object-cache-for-delta-queries).

Flujo de llamadas de consulta del organizador delta es como sigue:

1. El autor de la llamada inicia una consulta de sincronización delta, obtener una `nextLink` y una colección vacía de cambios.
2. El autor de la llamada debe [rellenar la caché de objetos para las consultas de delta](#populate-the-object-cache-for-delta-queries) con los objetos que el usuario está suscrito a, actualización de la caché.
3. El autor de la llamada sigue el `nextLink` proporcionado en la consulta de la sincronización inicial del delta para obtener un nuevo `deltaLink` a los cambios realizados desde el paso anterior.
4. El autor de la llamada aplica los cambios realizados en la respuesta de delta devuelto a los objetos en su memoria caché.
5. El autor de la llamada sigue el nuevo deltaLink para obtener el siguiente deltaLink y cambia con respecto a la actual `deltaLink` se generó.
6. El autor de la llamada se aplica los cambios (si hay alguno) y espera durante un breve período antes de volver a ejecutar el anterior paso y este paso.

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
| MaximumFavoritePlansForUser   | El `favoritePlanReferences` (propiedad) en el recurso [plannerUser](planneruser.md) contiene demasiados valores.                                                                                            |
| MaximumRecentPlansForUser     | El `recentPlanReferences` (propiedad) en el recurso [plannerUser](planneruser.md) contiene demasiados valores.                                                                                              |
| MaximumContextsOnPlan         | El `contexts` (propiedad) en el recurso [plannerPlan](plannerplan.md) contiene demasiados valores.                                                                                                          |
| MaximumPlannerPlans       | El grupo ya contiene un Plan. Actualmente, los grupos sólo pueden contener un Plan. **Nota:** Algunas aplicaciones de Microsoft pueden superar este límite. En el futuro, extenderemos esta funcionalidad para todas las aplicaciones.                                                                                                      |

### <a name="412-precondition-failed"></a>412 Error de condición previa 

Todas las API de plana `POST`, `PATCH`, y `DELETE` las solicitudes requieren la `If-Match` encabezado a especificarse con el último valor conocido etag del recurso que está sujeto a la solicitud.
También se puede devolver el código de 412 estado si el valor de etag especificado en la solicitud ya no coincide con una versión del recurso en el servicio. En este caso, los clientes deben volver a leer el recurso y obtener un nuevo valor de etag.

