---
title: Enumerar todos los equipos en Microsoft Teams para una organización
description: 'Enumerar todos los equipos '
author: nkramer
ms.openlocfilehash: f8f088dd9b7a55d3eb4c927ddef34458caeab507
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304163"
---
# <a name="list-all-teams-in-microsoft-teams-for-an-organization"></a>Enumerar todos los equipos en Microsoft Teams para una organización

Para enumerar todos los [equipos](/graph/api/resources/team?view=graph-rest-beta) de una organización (inquilino), primero encuentra todos los grupos que tienen equipos y, a continuación, obtiene información para cada equipo.

## <a name="get-a-list-of-groups"></a>Obtener una lista de grupos

Para conseguir una lista de todos los [grupos](/graph/api/resources/group?view=graph-rest-beta) de la organización que tienen equipos, obtenga una [lista de todos los grupos](/graph/api/group-list?view=graph-rest-beta) y, después, encuentre en el código los que tienen un propiedad **resourceProvisioningOptions** que contiene "Equipo".
Dado que los grupos son objetos de gran tamaño, use $select para obtener únicamente las propiedades del grupo que le interesan.

```http
GET /groups?$select=id,resourceProvisioningOptions
```

> **Nota**: Habrá equipos antiguos sin usar que no tengan configurado resourceProvisioningOptions. Para obtener más información, consulte [problemas conocidos](known-issues.md#missing-teams-in-list-all-teams).

Aquí tiene un ejemplo de la respuesta. 

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: xxx

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groups",
    "value": [
        {
            "id": "00e897b1-70ba-4cb9-9126-fd5f95c4bb78",
            "resourceProvisioningOptions": []
        },
        {
            "id": "00f6e045-f884-4359-a617-d459ee626862",
            "resourceProvisioningOptions": [
                "Team"
            ]
        }
    ]
}
```

## <a name="get-a-list-of-groups-using-beta-apis"></a>Obtener una lista de grupos con las API de beta

Con las API de la versión beta, puede usar $filter para devolver solo los grupos que tienen equipos.

```http
GET /groups?$filter=resourceProvisioningOptions/Any(x:x eq 'Team')
```

> **Nota**: $filter en /groups solo está disponible a través del extremo beta. resourceProvisioningOptions está disponible en la versión 1.0 y en la beta.

> **Nota**: No se mostrarán determinados equipos antiguos sin usar. Para obtener más información, consulte [problemas conocidos](known-issues.md#missing-teams-in-list-all-teams).

Aquí tiene un ejemplo de la respuesta. 

>**Nota:** Puede que se acorte el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: xxx

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#groups",
    "value": [
        {
            "id": "02bd9fd6-8f93-4758-87c3-1fb73740a315",
            "description": "Welcome to the HR Taskforce team.",
            "displayName": "HR Taskforce",
            "groupTypes": [
                "Unified"
            ],
            "mailEnabled": true,
            "mailNickname": "HRTaskforce",
            "resourceBehaviorOptions": [],
            "resourceProvisioningOptions": [
                "Team"
            ],
            "securityEnabled": false,
            "visibility": "Private",
        },
        {
            "id": "8090c93e-ba7c-433e-9f39-08c7ba07c0b3",
            "description": "Welcome to the team that we've assembled to launch our product.",
            "displayName": "X1050 Launch Team",
            "groupTypes": [
                "Unified"
            ],
            "mailEnabled": true,
            "mailNickname": "X1050LaunchTeam",
            "resourceBehaviorOptions": [],
            "resourceProvisioningOptions": [
                "Team"
            ],
            "securityEnabled": false,
            "visibility": "Private",
        }
    ]
}
```

## <a name="get-team-information-for-a-group"></a>Obtener información de un equipo para un grupo

Para obtener información de equipo para el equipo de un grupo determinado, llame a la API [obtener grupo](/graph/api/team-get?view=graph-rest-beta) e incluya el Id. de grupo.

```http
GET /teams/{group-id}
```

En el ejemplo siguiente se muestra la respuesta.

>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 401

{
  "isArchived" : false,
  "memberSettings": {
    "allowCreateUpdateChannels": true,
    "allowDeleteChannels": true,
    "allowAddRemoveApps": true,
    "allowCreateUpdateRemoveTabs": true,
    "allowCreateUpdateRemoveConnectors": true    
  },
  "guestSettings": {
    "allowCreateUpdateChannels": true,
    "allowDeleteChannels": true 
  },
  "messagingSettings": {
    "allowUserEditMessages": true,
    "allowUserDeleteMessages": true,
    "allowOwnerDeleteMessages": true,
    "allowTeamMentions": true,
    "allowChannelMentions": true    
  },
  "funSettings": {
    "allowGiphy": true,
    "giphyContentRating": "strict",
    "allowStickersAndMemes": true,
    "allowCustomMemes": true
  }
}
```

## <a name="see-also"></a>Vea también

- [Enumerar joinedTeams](/graph/api/user-list-joinedteams?view=graph-rest-beta)
- [Enumerar grupos](/graph/api/group-list?view=graph-rest-beta)
