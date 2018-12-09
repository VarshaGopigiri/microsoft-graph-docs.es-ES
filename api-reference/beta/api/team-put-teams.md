---
title: Crear equipo de grupo
description: Crear un nuevo equipo de un grupo.
ms.openlocfilehash: 50915ff025a724565f1eaa4c37a01942133f9e4f
ms.sourcegitcommit: 12c6e82f1417022540e534ebadbd0e8d7fb5abde
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/08/2018
ms.locfileid: "27209673"
---
# <a name="create-team-from-group"></a><span data-ttu-id="88a59-103">Crear equipo de grupo</span><span class="sxs-lookup"><span data-stu-id="88a59-103">Create team from group</span></span>

> <span data-ttu-id="88a59-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="88a59-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="88a59-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="88a59-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="88a59-106">Crear un nuevo [equipo](../resources/team.md) de un [grupo](../resources/group.md).</span><span class="sxs-lookup"><span data-stu-id="88a59-106">Create a new [team](../resources/team.md) from a [group](../resources/group.md).</span></span>

<span data-ttu-id="88a59-107">Para poder crear un equipo, el grupo debe tener un propietario menos uno.</span><span class="sxs-lookup"><span data-stu-id="88a59-107">In order to create a team, the group must have a least one owner.</span></span>

<span data-ttu-id="88a59-108">Si el grupo se ha creado desde hace menos de 15 minutos, es posible que la llamada de equipo de creación se lleve a cabo con un código de 404 error debido a retrasos en la replicación.</span><span class="sxs-lookup"><span data-stu-id="88a59-108">If the group was created less than 15 minutes ago, it's possible for the Create team call to fail with a 404 error code due to replication delays.</span></span> <span data-ttu-id="88a59-109">El modelo recomendado es volver a intentar la llamada de equipo crear tres veces, con un retraso de segundo 10 entre llamadas.</span><span class="sxs-lookup"><span data-stu-id="88a59-109">The recommended pattern is to retry the Create team call three times, with a 10 second delay between calls.</span></span>

## <a name="permissions"></a><span data-ttu-id="88a59-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="88a59-110">Permissions</span></span>

<span data-ttu-id="88a59-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="88a59-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="88a59-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="88a59-113">Permission type</span></span>      | <span data-ttu-id="88a59-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="88a59-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="88a59-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="88a59-115">Delegated (work or school account)</span></span> | <span data-ttu-id="88a59-116">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="88a59-116">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="88a59-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="88a59-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="88a59-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88a59-118">Not supported.</span></span>    |
|<span data-ttu-id="88a59-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="88a59-119">Application</span></span> | <span data-ttu-id="88a59-120">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="88a59-120">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="88a59-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="88a59-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PUT /groups/{id}/team
```

## <a name="request-headers"></a><span data-ttu-id="88a59-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="88a59-122">Request headers</span></span>

| <span data-ttu-id="88a59-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88a59-123">Header</span></span>       | <span data-ttu-id="88a59-124">Valor</span><span class="sxs-lookup"><span data-stu-id="88a59-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="88a59-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="88a59-125">Authorization</span></span>  | <span data-ttu-id="88a59-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="88a59-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="88a59-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="88a59-128">Content-Type</span></span>  | <span data-ttu-id="88a59-129">application/json</span><span class="sxs-lookup"><span data-stu-id="88a59-129">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="88a59-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="88a59-130">Request body</span></span>

<span data-ttu-id="88a59-131">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto de [equipo](../resources/team.md) .</span><span class="sxs-lookup"><span data-stu-id="88a59-131">In the request body, supply a JSON representation of a [team](../resources/team.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="88a59-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88a59-132">Response</span></span>

<span data-ttu-id="88a59-133">Si es correcta, este método debe devolver un `201 Created` código de respuesta y un objeto de [equipo](../resources/team.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88a59-133">If successful, this method should return a `201 Created` response code and a [team](../resources/team.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="88a59-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88a59-134">Example</span></span>

#### <a name="request"></a><span data-ttu-id="88a59-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="88a59-135">Request</span></span>

<span data-ttu-id="88a59-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88a59-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "create_team"
}-->
```http
PUT https://graph.microsoft.com/beta/groups/{id}/team
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

#### <a name="response"></a><span data-ttu-id="88a59-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88a59-137">Response</span></span>

<span data-ttu-id="88a59-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88a59-138">The following is an example of the response.</span></span> 

><span data-ttu-id="88a59-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="88a59-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="88a59-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="88a59-141">See also</span></span>

- [<span data-ttu-id="88a59-142">Creación de un grupo con un equipo</span><span class="sxs-lookup"><span data-stu-id="88a59-142">Creating a group with a team</span></span>](/graph/teams-create-group-and-team)
