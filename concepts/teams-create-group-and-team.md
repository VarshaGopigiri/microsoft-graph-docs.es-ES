---
title: Crear un grupo con un equipo de Microsoft Teams
description: 'Crear un grupo que incluya un equipo consta de dos pasos: '
author: nkramer
localization_priority: Priority
ms.prod: microsoft-teams
ms.openlocfilehash: 06b25a6da159030407c904622ffebde09c704d98
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970482"
---
# <a name="creating-a-group-with-a-microsoft-teams-team"></a>Crear un grupo con un equipo de Microsoft Teams

Crear un [grupo](/graph/api/resources/group?view=graph-rest-beta) que incluya un [equipo](/graph/api/resources/team?view=graph-rest-beta) consta de dos pasos: 

- [Crear un grupo](/graph/api/group-post-groups?view=graph-rest-beta) con las propiedades correctas.
- [Agregar un equipo](/graph/api/team-put-teams?view=graph-rest-beta) al grupo.

## <a name="create-a-group"></a>Crear un grupo

Para incluir un equipo, debe configurar los siguientes valores de propiedad, como se muestra en el ejemplo siguiente:

- **groupTypes** = { "Unified" } 
- **mailEnabled** = true
- **securityEnabled** = false

```http
POST /groups
{
    "displayName":"Flight 157",
    "mailNickname":"flight157",
    "description":"Everything about flight 157",
    "visibility":"Private",
    "groupTypes":["Unified"],
    "mailEnabled":true,
    "securityEnabled":false,
    "members@odata.bind":[
        "https://graph.microsoft.com/v1.0/users/bec05f3d-a818-4b58-8c2e-2b4e74b0246d",
        "https://graph.microsoft.com/v1.0/users/ae67a4f4-2308-4522-9021-9f402ff0fba8",
        "https://graph.microsoft.com/v1.0/users/eab978dd-35d0-4885-8c46-891b7d618783",
        "https://graph.microsoft.com/v1.0/users/6a1272b5-f6fc-45c4-95fe-fe7c5a676133"
    ],
    "owners@odata.bind":[
        "https://graph.microsoft.com/v1.0/users/6a1272b5-f6fc-45c4-95fe-fe7c5a676133",
        "https://graph.microsoft.com/v1.0/users/eab978dd-35d0-4885-8c46-891b7d618783"
    ]
}
```

En el ejemplo siguiente se muestra la respuesta. 

>**Nota:** Puede que se acorte el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: xxx
{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups/$entity",
    "id":"b7f968af-ca51-42f6-a77e-82c7147bc8f2"
}
```

## <a name="add-a-team-to-the-group"></a>Agregar un equipo al grupo

Agregar un equipo al grupo, como se muestra.

```http
PUT /groups/{id}/team
{ }
```

En el ejemplo siguiente se muestra la respuesta. 

>**Nota:** Puede que se acorte el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: xxx
{
    "@odata.context" : "https://graph.microsoft.com/v1.0/$metadata#teams/$entity",
    "id" : "b7f968af-ca51-42f6-a77e-82c7147bc8f2",
    "webUrl" : "https://example.com",
    "isArchived" : null,
    "memberSettings" : { },
    "guestSettings" : { },
    "messagingSettings" : { },
    "funSettings" : {}
}
```

El equipo creado tiene el mismo identificador que el grupo.
