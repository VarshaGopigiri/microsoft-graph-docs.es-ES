---
title: Usar la API de Microsoft Graph para trabajar con Microsoft Teams
description: Microsoft Teams es un área de trabajo en función de chat en Office 365 que proporciona acceso integrado a calendarios específicos de equipo, archivos, notas de OneNote, planes de organizador y mucho más.
ms.openlocfilehash: b42c33a34e0191eae236f675f29762834dfc29da
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030494"
---
# <a name="use-the-microsoft-graph-api-to-work-with-microsoft-teams"></a>Usar la API de Microsoft Graph para trabajar con Microsoft Teams



Microsoft Teams es un área de trabajo en función de chat en Office 365 que proporciona acceso integrado a calendarios específicos de equipo, archivos, notas de OneNote, planes de organizador y mucho más.

## <a name="key-resources-in-microsoft-teams"></a>Recursos clave en Microsoft Teams

| Recurso | Métodos |
|:---------------|:--------|
|[equipo](../resources/team.md)| [los equipos de la lista](../api/user-list-joinedteams.md), [lista de todos los equipos](/graph/teams-list-all-teams), [crear](../api/team-put-teams.md), [leer](../api/team-get.md), [Actualizar](../api/team-update.md), [Eliminar](/graph/api/group-delete?view=graph-rest-1.0), [clon](../api/team-clone.md), [archivo](../api/team-archive.md), [unarchive](../api/team-unarchive.md) |
|[group](../resources/group.md)| [Agregar a miembros](../api/group-post-members.md), [quitar a miembros](../api/group-delete-members.md), [Agregar propietario](../api/group-post-owners.md), [Quitar propietario](../api/group-delete-owners.md), [obtener archivos](drive.md), [obtener Bloc de notas](/graph/api/resources/notebook?view=graph-rest-1.0), [obtener los planes](plannergroup.md)y [obtener calendario](event.md) |
|[canal](../resources/channel.md)|[lista](../api/channel-list.md), [crear](../api/channel-post.md), [leer](../api/channel-get.md), [Actualizar](../api/channel-patch.md), [Eliminar](../api/channel-delete.md)|
|[teamsTab](../resources/teamstab.md) |[lista](../api/teamstab-list.md), [crear](../api/teamstab-add.md), [leer](../api/teamstab-get.md), [Actualizar](../api/teamstab-update.md), [Eliminar](../api/teamstab-delete.md) |
|[teamsApp](../resources/teamsapp.md)|[lista](../api/teamsapp-list.md), [Publicar](../api/teamsapp-publish.md), [Actualizar](../api/teamsapp-update.md), [Quitar](../api/teamsapp-delete.md)|
|[teamsAppInstallation](../resources/teamsappinstallation.md)| [lista](../api/teamsappinstallation-list.md), [instalar](../api/teamsappinstallation-add.md), [Actualizar](../api/teamsappinstallation-delete.md), [Quitar](../api/teamsappinstallation-delete.md) |
| (Vista previa) [chatMessage](/graph/api/resources/chatmessage?view=graph-rest-beta) y [chatThread](/graph/api/resources/chatthread?view=graph-rest-beta) | [lista](/graph/api/channel-list-messages?view=graph-rest-beta), [crear](/graph/api/channel-post-chatthreads?view=graph-rest-beta), [leer](/graph/api/channel-get-message?view=graph-rest-beta) |
| (Vista previa) [llamar a](/graph/api/resources/call?view=graph-rest-beta) | [respuesta](/graph/api/call-answer?view=graph-rest-beta), [Rechazar](/graph/api/call-reject?view=graph-rest-beta), [redirigir](/graph/api/call-redirect?view=graph-rest-beta), [desactivar](/graph/api/call-mute?view=graph-rest-beta), [reactivar el audio](/graph/api/call-unmute?view=graph-rest-beta), [Actualizar metadatos](/graph/api/call-updatemetadata?view=graph-rest-beta), [cambiar pantalla de uso compartido de rol](/graph/api/call-changescreensharingrole?view=graph-rest-beta), [los participantes de la lista](/graph/api/call-list-participants?view=graph-rest-beta), [Invitar a participantes](/graph/api/participant-invite?view=graph-rest-beta), [Silenciar a todos los participantes](/graph/api/participant-muteall?view=graph-rest-beta) |

## <a name="teams-and-groups"></a>Los equipos y grupos

En Microsoft Graph, Microsoft Teams está representado por un recurso de [grupo](../resources/group.md) . Las diversas necesidades de colaboración en grupo de direcciones de grupos de Microsoft Teams y Office 365. Casi todas las características basadas en grupos aplican a Microsoft Teams y los grupos de Office 365, como el calendario de grupo, archivos, notas, foto, planes y así sucesivamente. La diferencia principal entre un [equipo](team.md) y un grupo de Office 365 es el modo de comunicación entre los miembros. Los miembros del equipo comunican mediante chat persistente en el contexto de un equipo específico. Los miembros de Office 365 grupo comunican por las conversaciones en grupo, que son las conversaciones de correo electrónico que se producen en el contexto de un grupo en Outlook.

Cualquier grupo que tenga un equipo tiene una propiedad **resourceProvisioningOptions** que contiene "Equipo". 

>**Nota:** Se puede cambiar la propiedad **Group.resourceProvisioningOptions** .
No agregar o quitar "Equipo" de esa colección; de lo contrario, se obtienen resultados incorrectos cuando lista todos los equipos.

Los siguientes son las diferencias en el nivel de API entre los equipos y grupos:

- El método de la [lista se unió a los equipos](../api/user-list-joinedteams.md) se aplica sólo a Microsoft Teams.
- Vea también los [problemas conocidos](/graph/known-issues) para estas API.

>**Nota:** Si usa la API de grupos en una [aplicación de equipos de Microsoft](https://docs.microsoft.com/en-us/microsoftteams/platform/#apps-in-microsoft-teams) , en lugar de en una aplicación independiente - por ejemplo, como parte de una pestaña o componente que se ejecuta en Microsoft Teams - siga las instrucciones en el artículo [Utilizando Microsoft Graph en las páginas de los equipos de Microsoft](https://docs.microsoft.com/en-us/microsoftteams/platform/resources/microsoft-graph).

## <a name="membership-changes-in-microsoft-teams"></a>Cambios de pertenencia en Microsoft Teams

Para agregar miembros y propietarios a un equipo, cambiar la pertenencia del [grupo](../resources/group.md) con el mismo identificador.

| Caso de uso      | Verb      | URL |
| ------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [Agregar miembro](../api/group-post-members.md)    | POST      | ref de $/members/ /Groups/ {identificador}  |
| [Eliminar miembro](../api/group-delete-members.md)   | DELETE    | /Groups/ {identificador} /members/ {userId} / $ref |
| [Agregar propietario](../api/group-post-owners.md)     | POST       | ref de $/owners/ /Groups/ {identificador} |
| [Eliminar propietario](../api/group-delete-owners.md) | DELETE    | /Groups/ {identificador} /owners/ {userId} / $ref |
| [Equipo de actualización](../api/team-update.md)  | PATCH     | /Teams/ {identificador} |

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

- [Introducción a la API de los equipos de Microsoft](/graph/teams-concept-overview)
- Código de ejemplo: [Líneas aéreas Contoso](https://github.com/microsoftgraph/contoso-airlines-teams-sample), [mini ejemplos de C#](https://github.com/microsoftgraph/csharp-teams-sample-graph)
