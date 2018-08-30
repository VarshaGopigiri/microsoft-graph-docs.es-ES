# <a name="planner-tasks-and-plans-api-overview"></a>Introducción a la API de tareas y planes de Planner
Planner proporciona a los equipos una forma simple y visual de organizar su trabajo. Los clientes pueden usar Planner para crear planes, organizar y asignar tareas, compartir el progreso y colaborar en contenido.  Planner proporciona varias experiencias interactivas como un panel de tareas, una página de gráficos y una vista Programación, así como aplicaciones integradas en Office 365.

**Panel de tareas de Office 365 Planner**

![Captura de pantalla de un panel de tareas de Office 365 Planner](images/plannerboard.png "Imagen de un panel de Planner")


## <a name="why-integrate-with-planner-tasks"></a>¿Por qué debería realizar la integración con las tareas de Planner?
Planner proporciona capacidades de seguimiento de tareas para experiencias de colaboración de Office 365. Si los escenarios requieren el seguimiento de tareas y organizar el trabajo de un equipo o un grupo de usuarios finales, Planner es el servicio adecuado para usted. La integración de Planner puede ayudarle a alcanzar a los millones de usuarios que colaboran en Office 365. 

### <a name="organize-your-teams-work"></a>Organizar el trabajo del equipo
Planner proporciona un espacio compartido donde puede crear un equipo, [crear tareas](../api-reference/v1.0/api/planner_post_tasks.md) y asignarlas a otras personas del equipo. Planner facilita a todos saber quién está haciendo qué y si todo va bien. Puede actualizar las tareas con información adicional, como fechas de vencimiento, el progreso y descripciones, y organizar más las tareas con cubos personalizables y etiquetas de categoría.   

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
|Ver todos los [planes](../api-reference/beta/resources/plannerplan.md) de un grupo|GET [https://graph.microsoft.com/v1.0/groups/{id}/planner/plans](https://developer.microsoft.com/en-us/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)|
|Ver [tareas](../api-reference/beta/resources/plannertask.md) en un plan|GET [https://graph.microsoft.com/v1.0/planner/plans/{id}/tasks](https://developer.microsoft.com/en-us/graph/graph-explorer?request=planner/plans/{id}/tasks&version=v1.0)|
|Ver todas [las tareas](../api-reference/beta/api/planneruser_list_tasks.md) que me asignaron en los planes|GET [https://graph.microsoft.com/v1.0/me/planner/tasks/](https://developer.microsoft.com/en-us/graph/graph-explorer?request=me/planner/tasks/&version=v1.0)|
|[Cree una nueva tarea](../api-reference/v1.0/api/planner_post_tasks.md)|POST [https://graph.microsoft.com/v1.0/planner/tasks](https://developer.microsoft.com/en-us/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)|
|[Actualizar una tarea](../api-reference/v1.0/api/plannertask_update.md)|PATCH [https://graph.microsoft.com/v1.0/planner/tasks/{task-id}](https://developer.microsoft.com/en-us/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)|
|[Eliminar una tarea](../api-reference/v1.0/api/plannertask_delete.md)|DELETE [https://graph.microsoft.com/v1.0/planner/tasks/{id}](https://developer.microsoft.com/en-us/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)|


## <a name="next-steps"></a>Pasos siguientes

- [Usar la API de Planner](../api-reference/v1.0/resources/planner_overview.md)
- [Trabajar con planes](../api-reference/v1.0/resources/planner_overview.md#plans)
- [Trabajar con tareas](../api-reference/v1.0/resources/planner_overview.md#tasks)
