---
title: tipo de recurso de equipo
description: 'Un equipo en Microsoft Teams es una colección de canales. '
author: nkramer
ms.openlocfilehash: 3bb6fde320dbab2c19f151015d7121c3fc840c97
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27323873"
---
# <a name="team-resource-type"></a>tipo de recurso de equipo



Un equipo en Microsoft Teams es una colección de [canales](channel.md). Un canal representa un tema y, por lo tanto, un aislamiento lógico de discusión, dentro de un equipo.

Cada equipo está asociado con un [grupo](../resources/group.md).
El grupo tiene el mismo identificador que el equipo - /groups/ por ejemplo, {identificador} / equipo es el mismo que /teams/ {identificador}.
Para obtener más información sobre cómo trabajar con los miembros de los equipos y grupos, vea [uso de la API de REST de Microsoft Graph para que funcione con los equipos de Microsoft](teams-api-overview.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Crear equipo](../api/team-put-teams.md) | [equipo](team.md) | Crear un nuevo equipo o agregar un equipo a un grupo existente.|
|[Obtener el equipo](../api/team-get.md) | [equipo](team.md) | Recuperar las propiedades y relaciones del equipo especificado.|
|[Equipo de actualización](../api/team-update.md) | [equipo](team.md) |Actualizar las propiedades del equipo especificado. |
|[Eliminar grupo](/graph/api/group-delete?view=graph-rest-1.0) | Ninguno |Eliminar el equipo y el grupo asociado. |
|[Clonación de equipo](../api/team-clone.md) | [teamsAsyncOperation](../resources/teamsasyncoperation.md) |Copie el equipo y el grupo asociado. |
|[Equipo de archivo](../api/team-archive.md) | [teamsAsyncOperation](../resources/teamsasyncoperation.md) |Poner el equipo en un estado de sólo lectura. |
|[Unarchive equipo](../api/team-unarchive.md) | [teamsAsyncOperation](../resources/teamsasyncoperation.md) |Restaure el equipo a un estado de lectura y escritura. |
|[Lista de los equipos](../api/user-list-joinedteams.md) | colección de [equipo](team.md) | Lista de los equipos de que es un miembro. |
|[Lista de todos los equipos](/graph/teams-list-all-teams) | Colección [group](group.md) | Lista de todos los grupos que tienen los equipos. |
|[Publicar aplicaciones en la organización](../resources/teamsapp.md)| [teamsApp](../resources/teamsapp.md) | Crear aplicaciones de los equipos sólo es visible para su organización. |
|[Agregar la aplicación al equipo](../api/teamsappinstallation-add.md) | [teamsappinstallation](teamsappinstallation.md) | Agrega (se instala) una aplicación a un equipo.|
|[Agregar una ficha a canal](../api/teamstab-add.md) | [teamsTab](../resources/teamstab.md) | (Se instala) se agrega una ficha a canal de un equipo.|

## <a name="properties"></a>Propiedades

| Propiedad | Tipo   | Descripción |
|:---------------|:--------|:----------|
|funSettings|[teamFunSettings](teamfunsettings.md) |Opciones para configurar el uso de Giphy, memes y pegatinas en el equipo.|
|guestSettings|[teamGuestSettings](teamguestsettings.md) |Configuración para configurar si los invitados pueden crear, actualizar o eliminar los canales en el equipo.|
|isArchived|Boolean|Si este equipo está en modo de sólo lectura. |
|memberSettings|[teamMemberSettings](teammembersettings.md) |Configuración para configurar si los miembros pueden realizar determinadas acciones, por ejemplo, creación de canales y agrega bots, en el equipo.|
|messagingSettings|[teamMessagingSettings](teammessagingsettings.md) |La configuración de mensajería y menciones en el equipo.|
|webUrl|cadena (sólo lectura) | Un hipervínculo que se vaya al equipo en el cliente de Microsoft Teams. Esta es la URL que se obtiene cuando haga clic en un equipo en el cliente de Microsoft Teams y seleccione **obtener el vínculo al equipo**. Esta dirección URL debe se trata como un objeto binario opaco y no puede analizar. |

## <a name="relationships"></a>Relaciones

| Relación | Tipo   | Descripción |
|:---------------|:--------|:----------|
|canales|colección de [canal](channel.md)|La colección de canales de & mensajes asociados con el equipo.|
|installedApps|colección de [teamsAppInstallation](teamsappinstallation.md)|Las aplicaciones instaladas en este equipo.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.team",
  "baseType": "microsoft.graph.entity"
}-->

```json
{  
  "guestSettings": {"@odata.type": "microsoft.graph.teamGuestSettings"},
  "memberSettings": {"@odata.type": "microsoft.graph.teamMemberSettings"},
  "messagingSettings": {"@odata.type": "microsoft.graph.teamMessagingSettings"},
  "funSettings": {"@odata.type": "microsoft.graph.teamFunSettings"},
  "isArchived": false,
  "webUrl": "https://...longUrl..."
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

## <a name="see-also"></a>Vea también
- [Creación de un grupo con un equipo](/graph/teams-create-group-and-team)
- [Uso de las API de los equipos](teams-api-overview.md)
