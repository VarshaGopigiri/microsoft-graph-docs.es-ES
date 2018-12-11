---
title: Equipo de actualización
description: Actualizar las propiedades del equipo especificado.
ms.openlocfilehash: 23f65ef1cd1948941bd814a521bdaa0984553dff
ms.sourcegitcommit: 72d4da2a6bfaf99fa4edaf6ce3b97b1a6d96d874
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2018
ms.locfileid: "27222607"
---
# <a name="update-team"></a><span data-ttu-id="98dc4-103">Equipo de actualización</span><span class="sxs-lookup"><span data-stu-id="98dc4-103">Update team</span></span>



<span data-ttu-id="98dc4-104">Actualizar las propiedades del [equipo](../resources/team.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="98dc4-104">Update the properties of the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="98dc4-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="98dc4-105">Permissions</span></span>
<span data-ttu-id="98dc4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="98dc4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="98dc4-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="98dc4-108">Permission type</span></span>      | <span data-ttu-id="98dc4-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="98dc4-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="98dc4-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="98dc4-110">Delegated (work or school account)</span></span> | <span data-ttu-id="98dc4-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98dc4-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="98dc4-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="98dc4-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="98dc4-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98dc4-113">Not supported.</span></span>    |
|<span data-ttu-id="98dc4-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="98dc4-114">Application</span></span> | <span data-ttu-id="98dc4-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98dc4-115">Group.Read.All, Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="98dc4-116">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="98dc4-116">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="98dc4-117">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="98dc4-117">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="98dc4-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="98dc4-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /teams/{id}
```

## <a name="request-headers"></a><span data-ttu-id="98dc4-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="98dc4-119">Request headers</span></span>
| <span data-ttu-id="98dc4-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98dc4-120">Header</span></span>       | <span data-ttu-id="98dc4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="98dc4-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="98dc4-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="98dc4-122">Authorization</span></span>  | <span data-ttu-id="98dc4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="98dc4-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="98dc4-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="98dc4-125">Content-Type</span></span>  | <span data-ttu-id="98dc4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="98dc4-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="98dc4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="98dc4-127">Request body</span></span>
<span data-ttu-id="98dc4-128">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [equipo](../resources/team.md) .</span><span class="sxs-lookup"><span data-stu-id="98dc4-128">In the request body, supply a JSON representation of [team](../resources/team.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="98dc4-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98dc4-129">Response</span></span>

<span data-ttu-id="98dc4-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="98dc4-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="98dc4-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98dc4-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="98dc4-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98dc4-132">Request</span></span>
<span data-ttu-id="98dc4-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98dc4-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_team"
}-->
```http
PATCH https://graph.microsoft.com/beta/teams/{id}
Content-type: application/json
Content-length: 211

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
#### <a name="response"></a><span data-ttu-id="98dc4-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98dc4-134">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update Team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
