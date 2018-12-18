---
title: Equipo de actualización
description: Actualizar las propiedades del equipo especificado.
author: nkramer
ms.openlocfilehash: 19a3c55295bc54fcd7f1c9e24f88e386fc4dc2bb
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331923"
---
# <a name="update-team"></a><span data-ttu-id="05f39-103">Equipo de actualización</span><span class="sxs-lookup"><span data-stu-id="05f39-103">Update team</span></span>

> <span data-ttu-id="05f39-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="05f39-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="05f39-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="05f39-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="05f39-106">Actualizar las propiedades del [equipo](../resources/team.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="05f39-106">Update the properties of the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="05f39-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="05f39-107">Permissions</span></span>
<span data-ttu-id="05f39-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="05f39-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="05f39-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="05f39-110">Permission type</span></span>      | <span data-ttu-id="05f39-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="05f39-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="05f39-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="05f39-112">Delegated (work or school account)</span></span> | <span data-ttu-id="05f39-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="05f39-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="05f39-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="05f39-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="05f39-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="05f39-115">Not supported.</span></span>    |
|<span data-ttu-id="05f39-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="05f39-116">Application</span></span> | <span data-ttu-id="05f39-117">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="05f39-117">Group.Read.All, Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="05f39-118">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="05f39-118">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="05f39-119">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="05f39-119">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="05f39-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="05f39-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /teams/{id}
```
## <a name="request-headers"></a><span data-ttu-id="05f39-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="05f39-121">Request headers</span></span>
| <span data-ttu-id="05f39-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05f39-122">Header</span></span>       | <span data-ttu-id="05f39-123">Valor</span><span class="sxs-lookup"><span data-stu-id="05f39-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="05f39-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="05f39-124">Authorization</span></span>  | <span data-ttu-id="05f39-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="05f39-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="05f39-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="05f39-127">Content-Type</span></span>  | <span data-ttu-id="05f39-128">application/json</span><span class="sxs-lookup"><span data-stu-id="05f39-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="05f39-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="05f39-129">Request body</span></span>
<span data-ttu-id="05f39-130">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [equipo](../resources/team.md) .</span><span class="sxs-lookup"><span data-stu-id="05f39-130">In the request body, supply a JSON representation of [team](../resources/team.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="05f39-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05f39-131">Response</span></span>

<span data-ttu-id="05f39-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="05f39-132">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="05f39-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="05f39-133">Example</span></span>
#### <a name="request"></a><span data-ttu-id="05f39-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="05f39-134">Request</span></span>
<span data-ttu-id="05f39-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="05f39-135">The following is an example of the request.</span></span>
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
#### <a name="response"></a><span data-ttu-id="05f39-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05f39-136">Response</span></span>
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
