---
title: Introducción a la API de tareas y planes de Planner
description: Planner proporciona a los equipos una forma simple y visual de organizar su trabajo. Los clientes pueden usar Planner para crear planes, organizar y asignar tareas, compartir el progreso y colaborar en contenido.  Planner proporciona varias experiencias interactivas como un panel de tareas, una página de gráficos y una vista Programación, así como aplicaciones integradas en Office 365.
author: TarkanSevilmis
ms.openlocfilehash: cbe56021ad3aad08359b46b06a4ad2e285cac036
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27357165"
---
# <a name="planner-tasks-and-plans-api-overview"></a>Introducción a la API de tareas y planes de Planner
Planner proporciona a los equipos una forma simple y visual de organizar su trabajo. Los clientes pueden usar Planner para crear planes, organizar y asignar tareas, compartir el progreso y colaborar en contenido.  Planner proporciona varias experiencias interactivas como un panel de tareas, una página de gráficos y una vista Programación, así como aplicaciones integradas en Office 365.

**Panel de tareas de Office 365 Planner**

![Captura de pantalla de un panel de tareas de Office 365 Planner](images/plannerboard.png "Imagen de un panel de Planner")


## <a name="why-integrate-with-planner-tasks"></a>¿Por qué debería realizar la integración con las tareas de Planner?
Planner proporciona capacidades de seguimiento de tareas para experiencias de colaboración de Office 365. Si los escenarios requieren el seguimiento de tareas y organizar el trabajo de un equipo o un grupo de usuarios finales, Planner es el servicio adecuado para usted. La integración de Planner puede ayudarle a alcanzar a los millones de usuarios que colaboran en Office 365. 

### <a name="organize-your-teams-work"></a>Organizar el trabajo del equipo
Planner proporciona un espacio compartido donde puede crear un equipo, [crear tareas](/graph/api/planner-post-tasks?view=graph-rest-1.0) y asignarlas a otras personas del equipo. Planner facilita a todos saber quién está haciendo qué y si todo va bien. Puede actualizar las tareas con información adicional, como fechas de vencimiento, el progreso y descripciones, y organizar más las tareas con cubos personalizables y etiquetas de categoría.   

### <a name="collaborate-across-office-365"></a>Colaborar en Office 365
Planner se integra en las experiencias de colaboración en Office 365. Además de los clientes móvil y web de Planner, los usuarios pueden ver y actualizar los planes y las tareas de Planner desde SharePoint y Microsoft Teams.  

Planner usa la tecnología de Microsoft Graph y el servicio de grupo de Office 365. Los archivos que cargue y adjunte a tareas de Planner se almacenan en SharePoint. Los comentarios de Planner se basan en las conversaciones de grupo de Outlook.

<!-- Add image
Note: Put an image here showing the relationship between Planner and other things
-->

### <a name="automate-the-creation-of-plans-and-tasks"></a>Automatizar la creación de tareas y planes
¿Estás trabajando en tipos de proyecto o procesos repetidos? Puede usar la API de Planner para automatizar la creación de un plan y una lista de tareas.  
 
## <a name="top-planner-api-tasks"></a>Principales tareas de la API de Planner

|Operación|URL|
|:--------|:--|
|Ver todos los [planes](/graph/api/resources/plannerplan?view=graph-rest-beta) de un grupo|GET [https://graph.microsoft.com/v1.0/groups/{id}/planner/plans](https://developer.microsoft.com/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)|
|Ver [tareas](/graph/api/resources/plannertask?view=graph-rest-beta) en un plan|GET [https://graph.microsoft.com/v1.0/planner/plans/{id}/tasks](https://developer.microsoft.com/graph/graph-explorer?request=planner/plans/{id}/tasks&version=v1.0)|
|Ver todas [las tareas](/graph/api/planneruser-list-tasks?view=graph-rest-beta) que me asignaron en los planes|GET [https://graph.microsoft.com/v1.0/me/planner/tasks/](https://developer.microsoft.com/graph/graph-explorer?request=me/planner/tasks/&version=v1.0)|
|[Cree una nueva tarea](/graph/api/planner-post-tasks?view=graph-rest-1.0)|POST [https://graph.microsoft.com/v1.0/planner/tasks](https://developer.microsoft.com/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)|
|[Actualizar una tarea](/graph/api/plannertask-update?view=graph-rest-1.0)|PATCH [https://graph.microsoft.com/v1.0/planner/tasks/{task-id}](https://developer.microsoft.com/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)|
|[Eliminar una tarea](/graph/api/plannertask-delete?view=graph-rest-1.0)|ELIMINAR [https://graph.microsoft.com/v1.0/planner/tasks/{id}](https://developer.microsoft.com/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)|

## <a name="api-reference"></a>Referencia de la API
¿Busca la referencia de la API para este servicio?

- [API de Planner en Microsoft Graph v1.0](/graph/api/resources/planner-overview?view=graph-rest-1.0)
- [API de Planner en Microsoft Graph beta](/graph/api/resources/planner-overview?view=graph-rest-beta)


## <a name="next-steps"></a>Pasos siguientes

- [Usar la API de Planner](/graph/api/resources/planner-overview?view=graph-rest-1.0)
- [Trabajar con planes](/graph/api/resources/planner-overview?view=graph-rest-1.0#plans)
- [Trabajar con tareas](/graph/api/resources/planner-overview?view=graph-rest-1.0#tasks)
