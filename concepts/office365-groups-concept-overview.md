# <a name="overview-of-office-365-groups-in-microsoft-graph"></a>Información general sobre los grupos de Office 365 en Microsoft Graph

Los grupos de Office 365 proporcionan el servicio de suscripción fundamental para que los usuarios puedan compartir conversaciones, archivos, notas, calendarios, planes y muchos otros activos. 

## <a name="why-integrate-with-office-365-groups"></a>¿Por qué debería integrar con grupos de Office 365?   

Los grupos forman la base que permite la colaboración de usuario y la integración en todos los servicios para permitir escenarios enriquecidos de planificación de tareas, trabajo en equipo, educación y más. Cuando se integra con grupos de Office 365, la aplicación puede admitir millones de usuarios, mientras pasan entre las diferentes experiencias en el conjunto de aplicaciones de Office 365 y más allá.  
 
### <a name="create-groups-to-facilitate-teamwork-across-services"></a>Crear grupos para facilitar el trabajo en equipo a través de servicios 
 
Puede usar la API de Microsoft Graph para crear, administrar y eliminar grupos en todo el ciclo de vida de la colaboración. Por ejemplo, puede hacer lo siguiente:  
 
- Use la API [Crear grupo](../api-reference/v1.0/api/group_post_groups.md) para aprovisionar un nuevo grupo. El grupo pasa a estar disponible en una amplia variedad de aplicaciones, como Outlook, SharePoint, Microsoft Teams, Planner e incluso Microsoft Stream. Microsoft Graph se sincroniza en estos servicios conectados para proporcionar acceso directo a todos los miembros del grupo.  
 
    **Cada grupo de Office 365 se integra con un conjunto predeterminado de servicios de Office 365**

    ![Diagrama que muestra la integración de grupos de Office 365 con los archivos, las notas, las tareas, los sitios, las conversaciones y el calendario](images/office365-groups-concept-overview-related-services-infographic.png)  

- Permita a los miembros indicar que un grupo es uno de sus [favoritos](../api-reference/v1.0/api/group_addfavorite.md) o [quitarlo de sus favoritos](../api-reference/v1.0/api/group_removefavorite.md) si lo eligen. 
- [Cree](../api-reference/v1.0/api/group_post_conversations.md), [obtenga](../api-reference/v1.0/api/group_get_conversation.md) o [elimine](../api-reference/v1.0/api/group_delete_conversation.md) conversaciones de grupo desde su aplicación personalizada. 
- Programe [eventos](../api-reference/v1.0/resources/event.md) de calendario en el calendario del grupo. 
- Obtenga información sobre el [sitio de SharePoint](../api-reference/v1.0/resources/site.md) que está asociado a un grupo, como las [listas](../api-reference/v1.0/api/list_list.md) o los [subsitios](../api-reference/v1.0/api/site_list_subsites.md) de la biblioteca de documentos. 
- [Cree un plan](../api-reference/v1.0/api/planner_post_buckets.md) en Planner que pertenezca a un grupo. El plan proporciona una forma visual para realizar un seguimiento del trabajo en equipo al permitirle [crear tareas](../api-reference/v1.0/api/planner_post_tasks.md) que pueden [organizarse en cubos](../api-reference/v1.0/api/planner_post_buckets.md). 
- Acceda al bloc de notas de [OneNote](../api-reference/v1.0/resources/onenote.md) asociado a un grupo, que puede usarse para recopilar notas de reunión y organizar las ideas. 
  
    **Conversaciones y grupos de Office 365 en Outlook en la web**

    ![Captura de pantalla de Outlook en la web con grupos que aparecen en la carpeta Grupos](images/office365-groups-concept-overview-groups-in-outlook.png) 

- [Habilite un grupo de Microsoft Teams](../api-reference/beta/api/team_put_teams.md) (versión preliminar) para permitir a los miembros del grupo participar en el chat persistente.  
- [Elimine grupos](../api-reference/v1.0/api/group_delete.md). Cuando se elimina un grupo, también se eliminará todo el contenido asociado, lo que impide que se produzcan sitios, conversaciones o planes huérfanos. 
 
### <a name="manage-group-membership-seamlessly"></a>Administrar la pertenencia sin problemas 
 
Los grupos de Office 365 son colecciones de usuarios que comparten el acceso a recursos de servicios Microsoft o de la aplicación. Como la pertenencia a grupos se administra de forma centralizada, los cambios realizados a la pertenencia afectan a todos los servicios asociados con el grupo. Puede usar Microsoft Graph para realizar las siguientes tareas de pertenencia a grupos:
 
- [Agregar](../api-reference/v1.0/api/group_post_members.md) y [quitar](../api-reference/v1.0/api/group_delete_members.md) miembros de un grupo existente. 
- Obtener una [lista de propietarios](../api-reference/v1.0/api/group_list_owners.md) o una [lista de miembros](../api-reference/v1.0/api/group_list_members.md) de un grupo. Esto ayuda a transmitir quién tiene acceso al contenido del grupo, o quién debe realizar tareas administrativas, como renovar el grupo o aprobar una solicitud de combinación. 
- Designar grupos como **públicos**, en los que el contenido del grupo está visible para todos los usuarios de la misma organización, o **privados**, en los que el contenido de grupo solo está visible para los miembros, mediante la operación [Actualizar grupo](../api-reference/v1.0/api/group_update.md). 
- [Quitar propietarios](../api-reference/v1.0/api/group_delete_owners.md) que ya no participan en las responsabilidades de propiedad de un grupo determinado de la lista de propietarios del grupo. 
 
### <a name="establish-and-maintain-group-policy-settings"></a>Establecer y mantener la configuración de directiva de grupo 
 
A medida que empieza a crecer el número de grupos creados en una organización, Microsoft Graph admite la capacidad de controlar el uso y el ciclo de vida del grupo. Puede aplicar directivas de grupo en todos los grupos de una organización. Puede usar la API de Microsoft Graph para:

- Configurar una amplia gama de [opciones de configuración de directiva de grupo](../api-reference/v1.0/resources/groupsetting.md) que ayudan a definir comportamientos, como eliminar automáticamente los grupos a menos que los renueve un propietario y aplicar directivas de nomenclatura de grupos de Office 365. 
- [Renovar](../api-reference/v1.0/api/group_renew.md) grupos que estén a punto de expirar para permitir que los miembros del equipo puedan continuar colaborando y accediendo al contenido. Si no se renueva el grupo según la directiva de expiración establecida, se eliminará automáticamente. 
- [Restaurar](../api-reference/v1.0/api/directory_deleteditems_restore.md) grupos eliminados.
 
## <a name="next-steps"></a>Siguientes pasos

- Pruebe algunas solicitudes de API de ejemplo en el [Probador de Graph](https://developer.microsoft.com/es-ES/graph/graph-explorer). 
- Obtenga más información sobre cómo [usar los grupos API](../api-reference/v1.0/resources/groups-overview.md) en Microsoft Graph.
