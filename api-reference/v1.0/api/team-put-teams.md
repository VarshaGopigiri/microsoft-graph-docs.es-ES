---
title: Crear equipo
description: Crear un nuevo equipo en un grupo.
ms.openlocfilehash: d7afffb331bf4a1714083ebb5f95147ec48a65d0
ms.sourcegitcommit: 72d4da2a6bfaf99fa4edaf6ce3b97b1a6d96d874
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2018
ms.locfileid: "27222551"
---
# <a name="create-team"></a><span data-ttu-id="8b7e4-103">Crear equipo</span><span class="sxs-lookup"><span data-stu-id="8b7e4-103">Create team</span></span>



<span data-ttu-id="8b7e4-104">Crear un nuevo [equipo](../resources/team.md) en un [grupo](../resources/group.md).</span><span class="sxs-lookup"><span data-stu-id="8b7e4-104">Create a new [team](../resources/team.md) under a [group](../resources/group.md).</span></span>

<span data-ttu-id="8b7e4-105">Para poder crear un equipo, el grupo debe tener un propietario menos uno.</span><span class="sxs-lookup"><span data-stu-id="8b7e4-105">In order to create a team, the group must have a least one owner.</span></span>

<span data-ttu-id="8b7e4-106">Si el grupo se ha creado desde hace menos de 15 minutos, es posible que la llamada de equipo de creación se lleve a cabo con un código de 404 error debido a retrasos en la replicación.</span><span class="sxs-lookup"><span data-stu-id="8b7e4-106">If the group was created less than 15 minutes ago, it's possible for the Create team call to fail with a 404 error code due to replication delays.</span></span> <span data-ttu-id="8b7e4-107">El modelo recomendado es volver a intentar la llamada de equipo crear tres veces, con un retraso de segundo 10 entre llamadas.</span><span class="sxs-lookup"><span data-stu-id="8b7e4-107">The recommended pattern is to retry the Create team call three times, with a 10 second delay between calls.</span></span>

## <a name="permissions"></a><span data-ttu-id="8b7e4-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="8b7e4-108">Permissions</span></span>

<span data-ttu-id="8b7e4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8b7e4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8b7e4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8b7e4-111">Permission type</span></span>      | <span data-ttu-id="8b7e4-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8b7e4-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8b7e4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8b7e4-113">Delegated (work or school account)</span></span> | <span data-ttu-id="8b7e4-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8b7e4-114">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="8b7e4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8b7e4-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8b7e4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8b7e4-116">Not supported.</span></span>    |
|<span data-ttu-id="8b7e4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8b7e4-117">Application</span></span> | <span data-ttu-id="8b7e4-118">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8b7e4-118">Group.ReadWrite.All</span></span> |

> <span data-ttu-id="8b7e4-119">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="8b7e4-119">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="8b7e4-120">Global Administradores y administradores de servicios de Microsoft Teams pueden tener acceso a los grupos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="8b7e4-120">Global admins and Microsoft Teams service admins can access groups that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="8b7e4-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8b7e4-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PUT /groups/{id}/team
```

## <a name="request-headers"></a><span data-ttu-id="8b7e4-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8b7e4-122">Request headers</span></span>

| <span data-ttu-id="8b7e4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b7e4-123">Header</span></span>       | <span data-ttu-id="8b7e4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8b7e4-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="8b7e4-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="8b7e4-125">Authorization</span></span>  | <span data-ttu-id="8b7e4-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8b7e4-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="8b7e4-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8b7e4-128">Content-Type</span></span>  | <span data-ttu-id="8b7e4-129">application/json</span><span class="sxs-lookup"><span data-stu-id="8b7e4-129">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="8b7e4-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8b7e4-130">Request body</span></span>

<span data-ttu-id="8b7e4-131">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto de [equipo](../resources/team.md) .</span><span class="sxs-lookup"><span data-stu-id="8b7e4-131">In the request body, supply a JSON representation of a [team](../resources/team.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="8b7e4-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b7e4-132">Response</span></span>

<span data-ttu-id="8b7e4-133">Si es correcta, este método debe devolver un `201 Created` código de respuesta y un objeto de [equipo](../resources/team.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8b7e4-133">If successful, this method should return a `201 Created` response code and a [team](../resources/team.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8b7e4-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8b7e4-134">Example</span></span>

#### <a name="request"></a><span data-ttu-id="8b7e4-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8b7e4-135">Request</span></span>

<span data-ttu-id="8b7e4-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8b7e4-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "create_team"
}-->
```http
PUT https://graph.microsoft.com/v1.0/groups/{id}/team
Content-type: application/json

{  
  "memberSettings": {
    "allowCreateUpdateChannels": true
  },
  "messagingSettings": {
    "allowUserEditMessages": true,
    "allowUserDeleteMessages": true
  },
  "funSettings": {
    "allowGiphy": true,
    "giphyContentRating": "strict"
  }
}
```

#### <a name="response"></a><span data-ttu-id="8b7e4-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b7e4-137">Response</span></span>

<span data-ttu-id="8b7e4-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8b7e4-138">The following is an example of the response.</span></span> 

><span data-ttu-id="8b7e4-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8b7e4-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 401

{
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

## <a name="see-also"></a><span data-ttu-id="8b7e4-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b7e4-141">See also</span></span>

- [<span data-ttu-id="8b7e4-142">Creación de un grupo con un equipo</span><span class="sxs-lookup"><span data-stu-id="8b7e4-142">Creating a group with a team</span></span>](/graph/teams-create-group-and-team)
