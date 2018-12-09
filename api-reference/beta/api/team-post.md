---
title: Crear un equipo
description: Crear un nuevo equipo.
ms.openlocfilehash: 3f2fa97af217d6109f169e5b2ef75a0c71bde2e7
ms.sourcegitcommit: 12c6e82f1417022540e534ebadbd0e8d7fb5abde
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/08/2018
ms.locfileid: "27210170"
---
# <a name="create-team"></a><span data-ttu-id="e4012-103">Crear equipo</span><span class="sxs-lookup"><span data-stu-id="e4012-103">Create team</span></span>

> <span data-ttu-id="e4012-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e4012-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e4012-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e4012-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e4012-106">Crear un nuevo [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="e4012-106">Create a new [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="e4012-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e4012-107">Permissions</span></span>

<span data-ttu-id="e4012-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e4012-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="e4012-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e4012-110">Permission type</span></span>                        | <span data-ttu-id="e4012-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e4012-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="e4012-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e4012-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="e4012-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e4012-113">Group.ReadWrite.All</span></span>                         |
| <span data-ttu-id="e4012-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e4012-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e4012-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e4012-115">Not supported.</span></span>                              |
| <span data-ttu-id="e4012-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e4012-116">Application</span></span>                            | <span data-ttu-id="e4012-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e4012-117">Group.ReadWrite.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="e4012-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e4012-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /teams
```

## <a name="request-headers"></a><span data-ttu-id="e4012-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e4012-119">Request headers</span></span>

| <span data-ttu-id="e4012-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4012-120">Header</span></span>        | <span data-ttu-id="e4012-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e4012-121">Value</span></span>                     |
| :------------ | :------------------------ |
| <span data-ttu-id="e4012-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="e4012-122">Authorization</span></span> | <span data-ttu-id="e4012-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e4012-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e4012-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e4012-125">Content-Type</span></span>  | <span data-ttu-id="e4012-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e4012-126">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="e4012-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e4012-127">Request body</span></span>

<span data-ttu-id="e4012-128">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto de [equipo](../resources/team.md) .</span><span class="sxs-lookup"><span data-stu-id="e4012-128">In the request body, supply a JSON representation of a [team](../resources/team.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="e4012-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4012-129">Response</span></span>

<span data-ttu-id="e4012-130">Si tiene éxito, esta API devuelve una `202 Accepted` respuesta que contiene un vínculo a la [teamsAsyncOperation](../resources/teamsasyncoperation.md).</span><span class="sxs-lookup"><span data-stu-id="e4012-130">If successful, this API returns a `202 Accepted` response containing a link to the [teamsAsyncOperation](../resources/teamsasyncoperation.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e4012-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e4012-131">Examples</span></span>

### <a name="example---delegated-permissions"></a><span data-ttu-id="e4012-132">Por ejemplo, los permisos delegados</span><span class="sxs-lookup"><span data-stu-id="e4012-132">Example - delegated permissions</span></span>

<span data-ttu-id="e4012-133">Este es un ejemplo de una solicitud mínima.</span><span class="sxs-lookup"><span data-stu-id="e4012-133">Here is an example of a minimal request.</span></span> <span data-ttu-id="e4012-134">Si se omite otras propiedades, el cliente está tomando implícitamente valores predeterminados de la plantilla predefinida representada por `template`.</span><span class="sxs-lookup"><span data-stu-id="e4012-134">By omitting other properties, the client is implicitly taking defaults from the pre-defined template represented by `template`.</span></span>

#### <a name="request"></a><span data-ttu-id="e4012-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e4012-135">Request</span></span>

```http
POST https://graph.microsoft.com/beta/teams
Content-Type: application/json
{
  "template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates/standard",
  "displayName": "My Sample Team",
  "description": "My Sample Team’s Description",
}
```

##### <a name="response"></a><span data-ttu-id="e4012-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4012-136">Response</span></span>

```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
{
}
```

### <a name="example---create-a-team-with-an-app-installed-multiple-channels-with-pinned-tabs-using-delegated-permissions"></a><span data-ttu-id="e4012-137">Ejemplo: creación de un equipo con una aplicación instalada, varios canales con fichas anclados con permisos de delegados</span><span class="sxs-lookup"><span data-stu-id="e4012-137">Example - create a team with an app installed, multiple channels with pinned tabs using delegated permissions</span></span>

<span data-ttu-id="e4012-138">Aquí es la solicitud con una carga completa.</span><span class="sxs-lookup"><span data-stu-id="e4012-138">Here is request with a full payload.</span></span> <span data-ttu-id="e4012-139">El cliente puede invalidar los valores en la plantilla de base y agregar a los elementos con valores de matriz en la medida permitida por las reglas de validación para el `specialization`.</span><span class="sxs-lookup"><span data-stu-id="e4012-139">The client can override values in the base template and add to array-valued items to the extent allowed by validation rules for the `specialization`.</span></span>

#### <a name="request"></a><span data-ttu-id="e4012-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e4012-140">Request</span></span>

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

#### <a name="response"></a><span data-ttu-id="e4012-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4012-141">Response</span></span>

```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
{
}
```

### <a name="example---application-permissions"></a><span data-ttu-id="e4012-142">Por ejemplo, los permisos de aplicación</span><span class="sxs-lookup"><span data-stu-id="e4012-142">Example - application permissions</span></span>

<span data-ttu-id="e4012-143">Este es un ejemplo de una solicitud mínima con permisos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e4012-143">Here is an example of a minimal request using application permissions.</span></span> <span data-ttu-id="e4012-144">Si se omite otras propiedades, el cliente está tomando implícitamente valores predeterminados de la plantilla predefinida representada por `template`.</span><span class="sxs-lookup"><span data-stu-id="e4012-144">By omitting other properties, the client is implicitly taking defaults from the pre-defined template represented by `template`.</span></span> <span data-ttu-id="e4012-145">Cuando emitir una solicitud con permisos de la aplicación de un [usuario](../resources/user.md) debe especificarse en el `owners` colección.</span><span class="sxs-lookup"><span data-stu-id="e4012-145">When issuing a request with application permissions a [user](../resources/user.md) must be specified in the `owners` collection.</span></span>

#### <a name="request"></a><span data-ttu-id="e4012-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e4012-146">Request</span></span>

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

#### <a name="response"></a><span data-ttu-id="e4012-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4012-147">Response</span></span>

```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
{
}
```

## <a name="see-also"></a><span data-ttu-id="e4012-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4012-148">See also</span></span>

- [<span data-ttu-id="e4012-149">Creación de un grupo con un equipo</span><span class="sxs-lookup"><span data-stu-id="e4012-149">Creating a group with a team</span></span>](/graph/teams-create-group-and-team)
