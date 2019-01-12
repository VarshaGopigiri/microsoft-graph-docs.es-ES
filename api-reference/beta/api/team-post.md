---
title: Crear un equipo
description: Crear un nuevo equipo.
author: nkramer
localization_priority: Priority
ms.prod: microsoft-teams
ms.openlocfilehash: 018d6085cec94a7aa2697e027f69b4b6f70cfaad
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962740"
---
# <a name="create-team"></a>Crear equipo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Crear un nuevo [equipo](../resources/team.md).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de permiso                        | Permisos (de menos a más privilegiados) |
| :------------------------------------- | :------------------------------------------ |
| Delegado (cuenta profesional o educativa)     | Group.ReadWrite.All                         |
| Delegado (cuenta personal de Microsoft) | No admitida.                              |
| Aplicación                            | Group.ReadWrite.All                         |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /teams
```

## <a name="request-headers"></a>Encabezados de solicitud

| Encabezado        | Valor                     |
| :------------ | :------------------------ |
| Authorization | {token} de portador. Obligatorio. |
| Content-Type  | application/json          |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto de [equipo](../resources/team.md) .

## <a name="response"></a>Respuesta

Si tiene éxito, esta API devuelve una `202 Accepted` respuesta que contiene un vínculo a la [teamsAsyncOperation](../resources/teamsasyncoperation.md).

## <a name="examples"></a>Ejemplos

### <a name="example---delegated-permissions"></a>Por ejemplo, los permisos delegados

Este es un ejemplo de una solicitud mínima. Si se omite otras propiedades, el cliente está tomando implícitamente valores predeterminados de la plantilla predefinida representada por `template`.

#### <a name="request"></a>Solicitud

```http
POST https://graph.microsoft.com/beta/teams
Content-Type: application/json
{
  "template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates/standard",
  "displayName": "My Sample Team",
  "description": "My Sample Team’s Description",
}
```

##### <a name="response"></a>Respuesta

```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
{
}
```

### <a name="example---create-a-team-with-an-app-installed-multiple-channels-with-pinned-tabs-using-delegated-permissions"></a>Ejemplo: creación de un equipo con una aplicación instalada, varios canales con fichas anclados con permisos de delegados

Aquí es la solicitud con una carga completa. El cliente puede invalidar los valores en la plantilla de base y agregar a los elementos con valores de matriz en la medida permitida por las reglas de validación para el `specialization`.

#### <a name="request"></a>Solicitud

```http
POST https://graph.microsoft.com/beta/teams
Content-Type: application/json
{
    "template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates('standard')",
    "visibility": "Private",
    "displayName": "Sample Engineering Team",
    "description": "This is a sample engineering team, used to showcase the range of properties supported by this API",
    "channels": [
        {
            "displayName": "Announcements 📢",
            "isFavoriteByDefault": true,
            "description": "This is a sample announcements channel that is favorited by default. Use this channel to make important team, product, and service announcements."
        },
        {
            "displayName": "Training 🏋️",
            "isFavoriteByDefault": true,
            "description": "This is a sample training channel, that is favorited by default, and contains an example of pinned website and YouTube tabs.",
            "tabs": [
                {
                    "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.web')",
                    "name": "A Pinned Website",
                    "configuration": {
                        "contentUrl": "https://docs.microsoft.com/en-us/microsoftteams/microsoft-teams"
                    }
                },
                {
                    "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.youtube')",
                    "name": "A Pinned YouTube Video",
                    "configuration": {
                        "contentUrl": "https://tabs.teams.microsoft.com/Youtube/Home/YoutubeTab?videoId=X8krAMdGvCQ",
                        "websiteUrl": "https://www.youtube.com/watch?v=X8krAMdGvCQ"
                    }
                }
            ]
        },
        {
            "displayName": "Planning 📅 ",
            "description": "This is a sample of a channel that is not favorited by default, these channels will appear in the more channels overflow menu.",
            "isFavoriteByDefault": false
        },
        {
            "displayName": "Issues and Feedback 🐞",
            "description": "This is a sample of a channel that is not favorited by default, these channels will appear in the more channels overflow menu."
        }
    ],
    "memberSettings": {
        "allowCreateUpdateChannels": true,
        "allowDeleteChannels": true,
        "allowAddRemoveApps": true,
        "allowCreateUpdateRemoveTabs": true,
        "allowCreateUpdateRemoveConnectors": true
    },
    "guestSettings": {
        "allowCreateUpdateChannels": false,
        "allowDeleteChannels": false
    },
    "funSettings": {
        "allowGiphy": true,
        "giphyContentRating": "Moderate",
        "allowStickersAndMemes": true,
        "allowCustomMemes": true
    },
    "messagingSettings": {
        "allowUserEditMessages": true,
        "allowUserDeleteMessages": true,
        "allowOwnerDeleteMessages": true,
        "allowTeamMentions": true,
        "allowChannelMentions": true
    },
    "installedApps": [
        {
            "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.vsts')"
        },
        {
            "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('1542629c-01b3-4a6d-8f76-1938b779e48d')"
        }
    ]
}
```

#### <a name="response"></a>Respuesta

```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
{
}
```

### <a name="example---application-permissions"></a>Por ejemplo, los permisos de aplicación

Este es un ejemplo de una solicitud mínima con permisos de la aplicación. Si se omite otras propiedades, el cliente está tomando implícitamente valores predeterminados de la plantilla predefinida representada por `template`. Cuando emitir una solicitud con permisos de la aplicación de un [usuario](../resources/user.md) debe especificarse en el `owners` colección.

#### <a name="request"></a>Solicitud

```http
POST https://graph.microsoft.com/beta/teams
Content-Type: application/json
{
  "template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates/standard",
  "displayName": "My Sample Team",
  "description": "My Sample Team’s Description",
  "owners@odata.bind": [
    "https://graph.microsoft.com/beta/users('abc123')"
  ]
}
```

#### <a name="response"></a>Respuesta

```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
{
}
```

## <a name="see-also"></a>Vea también

- [Creación de un grupo con un equipo](/graph/teams-create-group-and-team)
