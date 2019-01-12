---
title: Obtener el equipo
description: Recuperar las propiedades y relaciones del equipo especificado.
author: nkramer
localization_priority: Priority
ms.prod: microsoft-teams
ms.openlocfilehash: 0221983538f14ef3f0c0439f8241974091e8dc0b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943140"
---
# <a name="get-team"></a><span data-ttu-id="17cc0-103">Obtener el equipo</span><span class="sxs-lookup"><span data-stu-id="17cc0-103">Get team</span></span>



<span data-ttu-id="17cc0-104">Recuperar las propiedades y relaciones del [equipo](../resources/team.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="17cc0-104">Retrieve the properties and relationships of the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="17cc0-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="17cc0-105">Permissions</span></span>
<span data-ttu-id="17cc0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="17cc0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="17cc0-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="17cc0-108">Permission type</span></span>      | <span data-ttu-id="17cc0-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="17cc0-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="17cc0-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="17cc0-110">Delegated (work or school account)</span></span> | <span data-ttu-id="17cc0-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="17cc0-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="17cc0-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="17cc0-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="17cc0-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17cc0-113">Not supported.</span></span>    |
|<span data-ttu-id="17cc0-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="17cc0-114">Application</span></span> | <span data-ttu-id="17cc0-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="17cc0-115">Group.Read.All, Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="17cc0-116">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="17cc0-116">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="17cc0-117">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="17cc0-117">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="17cc0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="17cc0-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="17cc0-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="17cc0-119">Optional query parameters</span></span>
<span data-ttu-id="17cc0-120">Este método admite la $select y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17cc0-120">This method supports the $select and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="17cc0-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="17cc0-121">Request headers</span></span>
| <span data-ttu-id="17cc0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17cc0-122">Header</span></span>       | <span data-ttu-id="17cc0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="17cc0-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="17cc0-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="17cc0-124">Authorization</span></span>  | <span data-ttu-id="17cc0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="17cc0-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="17cc0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="17cc0-127">Request body</span></span>
<span data-ttu-id="17cc0-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="17cc0-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="17cc0-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17cc0-129">Response</span></span>

<span data-ttu-id="17cc0-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [equipo](../resources/team.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17cc0-130">If successful, this method returns a `200 OK` response code and a [team](../resources/team.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="17cc0-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17cc0-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="17cc0-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="17cc0-132">Request</span></span>
<span data-ttu-id="17cc0-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17cc0-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
GET https://graph.microsoft.com/v1.0/teams/{id}
```
#### <a name="response"></a><span data-ttu-id="17cc0-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17cc0-134">Response</span></span>
<span data-ttu-id="17cc0-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17cc0-135">The following is an example of the response.</span></span> 

><span data-ttu-id="17cc0-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="17cc0-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
