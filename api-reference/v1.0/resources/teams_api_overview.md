# <a name="use-the-microsoft-graph-api-to-work-with-microsoft-teams"></a>Usar la API de Microsoft Graph para trabajar con Microsoft Teams



Microsoft Teams es un área de trabajo en función de chat en Office 365 que proporciona acceso integrado a calendarios específicos de equipo, archivos, notas de OneNote, planes de organizador y mucho más.

## <a name="key-resources-in-microsoft-teams"></a>Recursos clave en Microsoft Teams

| Recurso | Métodos |
|:---------------|:--------|
|[equipo](../resources/team.md)| [los equipos de la lista](../api/user_list_joinedteams.md), [lista de todos los equipos](../../../concepts/teams_list_all_teams.md), [crear](../api/team_put_teams.md), [leer](../api/team_get.md), [Actualizar](../api/team_update.md), [Eliminar](../../v1.0/api/group_delete.md), [clon](../api/team_clone.md), [archivo](../api/team_archive.md), [unarchive](../api/team_unarchive.md) |
|[group](../resources/group.md)| [Agregar a miembros](../api/group_post_members.md), [quitar a miembros](../api/group_delete_members.md), [Agregar propietario](../api/group_post_owners.md), [Quitar propietario](../api/group_delete_owners.md), [obtener archivos](drive.md), [obtener Bloc de notas](../../v1.0/resources/notebook.md), [obtener los planes](plannergroup.md)y [obtener calendario](event.md) |
|[canal](../resources/channel.md)|[lista](../api/channel_list.md), [crear](../api/channel_post.md), [leer](../api/channel_get.md), [Actualizar](../api/channel_patch.md), [Eliminar](../api/channel_delete.md)|
|[teamsTab](../resources/teamstab.md) |[lista](../api/teamstab_list.md), [crear](../api/teamstab_add.md), [leer](../api/teamstab_get.md), [Actualizar](../api/teamstab_update.md), [Eliminar](../api/teamstab_delete.md) |
|[teamsApp](../resources/teamsapp.md)|[lista](../api/teamsapp_list.md), [Publicar](../api/teamsapp_publish.md), [Actualizar](../api/teamsapp_update.md), [Quitar](../api/teamsapp_delete.md)|
|[teamsAppInstallation](../resources/teamsappinstallation.md)| [lista](../api/teamsappinstallation_list.md), [instalar](../api/teamsappinstallation_add.md), [Actualizar](../api/teamsappinstallation_delete.md), [Quitar](../api/teamsappinstallation_delete.md) |
| (Vista previa) [chatMessage](../../beta/resources/chatmessage.md) y [chatThread](../../beta/resources/chatthread.md) | [lista](../../beta/api/channel_list_messages.md), [crear](../../beta/api/channel_post_chatthreads.md), [leer](../../beta/api/channel_get_message.md) |
| (Vista previa) [llamar a](../../beta/resources/call.md) | [respuesta](../../beta/api/call_answer.md), [Rechazar](../../beta/api/call_reject.md), [redirigir](../../beta/api/call_redirect.md), [desactivar](../../beta/api/call_mute.md), [reactivar el audio](../../beta/api/call_unmute.md), [Actualizar metadatos](../../beta/api/call_updatemetadata.md), [cambiar pantalla de uso compartido de rol](../../beta/api/call_changescreensharingrole.md), [los participantes de la lista](../../beta/api/call_list_participants.md), [Invitar a participantes](../../beta/api/participant_invite.md), [Silenciar a todos los participantes](../../beta/api/participant_muteall.md) |

## <a name="teams-and-groups"></a>Los equipos y grupos

En Microsoft Graph, Microsoft Teams está representado por un recurso de [grupo](../resources/group.md) . Las diversas necesidades de colaboración en grupo de direcciones de grupos de Microsoft Teams y Office 365. Casi todas las características basadas en grupos aplican a Microsoft Teams y los grupos de Office 365, como el calendario de grupo, archivos, notas, foto, planes y así sucesivamente. La diferencia principal entre un [equipo](team.md) y un grupo de Office 365 es el modo de comunicación entre los miembros. Los miembros del equipo comunican mediante chat persistente en el contexto de un equipo específico. Los miembros de Office 365 grupo comunican por las conversaciones en grupo, que son las conversaciones de correo electrónico que se producen en el contexto de un grupo en Outlook.

Cualquier grupo que tenga un equipo tiene una propiedad **resourceProvisioningOptions** que contiene "Equipo". 

>**Nota:** Se puede cambiar la propiedad **Group.resourceProvisioningOptions** .
No agregar o quitar "Equipo" de esa colección; de lo contrario, se obtienen resultados incorrectos cuando lista todos los equipos.

Los siguientes son las diferencias en el nivel de API entre los equipos y grupos:

- El método de la [lista se unió a los equipos](../api/user_list_joinedteams.md) se aplica sólo a Microsoft Teams.
- Vea también los [problemas conocidos](../../../concepts/known_issues.md) para estas API.

>**Nota:** Si usa la API de grupos en una [aplicación de equipos de Microsoft](https://docs.microsoft.com/en-us/microsoftteams/platform/#apps-in-microsoft-teams) , en lugar de en una aplicación independiente - por ejemplo, como parte de una pestaña o componente que se ejecuta en Microsoft Teams - siga las instrucciones en el artículo [Utilizando Microsoft Graph en las páginas de los equipos de Microsoft](https://docs.microsoft.com/en-us/microsoftteams/platform/resources/microsoft-graph).

## <a name="membership-changes-in-microsoft-teams"></a>Cambios de pertenencia en Microsoft Teams

Para agregar miembros y propietarios a un equipo, cambiar la pertenencia del [grupo](../resources/group.md) con el mismo identificador.

| Caso de uso      | Verb      | URL |
| ------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [Agregar miembro](../api/group_post_members.md)    | POST      | ref de $/members/ /Groups/ {identificador}  |
| [Eliminar miembro](../api/group_delete_members.md)   | DELETE    | /Groups/ {identificador} /members/ {userId} / $ref |
| [Agregar propietario](../api/group_post_owners.md)     | POST       | ref de $/owners/ /Groups/ {identificador} |
| [Eliminar propietario](../api/group_delete_owners.md) | DELETE    | /Groups/ {identificador} /owners/ {userId} / $ref |
| [Equipo de actualización](../api/team_update.md)  | PATCH     | /Teams/ {identificador} |

Se recomienda que cuando se agrega un propietario, también agregue ese usuario como un miembro. Si un equipo tiene un propietario que no es un miembro, los cambios de propiedad y la pertenencia es posible que no aparezca inmediatamente en Microsoft Teams. Además, diferentes aplicaciones y API controlará forma diferente. Por ejemplo, Microsoft Teams mostrará los equipos que el usuario es un miembro o un propietario de, mientras que los cmdlets de PowerShell de los equipos de Microsoft y la API/me/joinedTeams sólo se mostrará el usuario es un miembro de los equipos. Para evitar confusiones, agregue todos los propietarios a así como la lista de miembros. 

Problema conocido: eliminar cuando /groups/ {identificador} / se llama a los propietarios, también se quita el usuario de la /groups/ {identificador} o lista de miembros. Para solucionar este problema, se recomienda que quite el usuario para que los propietarios y miembros, a continuación, espere 10 segundos, a continuación, agregarlos a los miembros.

Cuando no ponga la adición y eliminación de miembros y propietarios, llaves {} alrededor el identificador.

| Speed | Sintaxis | 
| ------ | ----- |
| Rápido | https://graph.microsoft.com/v1.0/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/members/48d31887-5fad-4d73-a9f5-3c356e68a038/$ref | 
| Lento | https://graph.microsoft.com/v1.0/groups/{02bd9fd6-8f93-4758-87c3-1fb73740a315}/members/{48d31887-5fad-4d73-a9f5-3c356e68a038}/$ref | 

De forma similar, si la `userId` en la dirección URL o la carga se expresa como un UPN en lugar de como un GUID, el rendimiento será más lento.

| Speed | Sintaxis | 
| ------ | ----- |
| Rápido | 48d31887-5fad-4d73-a9f5-3c356e68a038 | 
| Lento | John@example.com | 

Cuando se toma la ruta de acceso más lento, si un integrante del grupo actual o un propietario se ha iniciado sesión la aplicación de Microsoft Teams o el sitio Web, el cambio se reflejará en una hora.
Si ninguno de esos usuarios ha iniciado sesión la aplicación de Microsoft Teams o el sitio Web, el cambio no se reflejarán hasta una hora después de que uno de ellos inicia sesión.

## <a name="see-also"></a>Vea también

- [Introducción a la API de los equipos de Microsoft](../../../concepts/teams-concept-overview.md)
- Código de ejemplo: [Líneas aéreas Contoso](https://github.com/microsoftgraph/contoso-airlines-teams-sample), [mini ejemplos de C#](https://github.com/microsoftgraph/csharp-teams-sample-graph)
