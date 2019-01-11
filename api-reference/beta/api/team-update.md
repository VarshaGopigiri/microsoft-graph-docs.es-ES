---
title: Equipo de actualización
description: Actualizar las propiedades del equipo especificado.
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 478da815a7bdf5dca15ddba358b5e12c46c1f045
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885295"
---
# <a name="update-team"></a><span data-ttu-id="79b70-103">Equipo de actualización</span><span class="sxs-lookup"><span data-stu-id="79b70-103">Update team</span></span>

> <span data-ttu-id="79b70-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="79b70-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="79b70-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="79b70-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="79b70-106">Actualizar las propiedades del [equipo](../resources/team.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="79b70-106">Update the properties of the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="79b70-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="79b70-107">Permissions</span></span>
<span data-ttu-id="79b70-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="79b70-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="79b70-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="79b70-110">Permission type</span></span>      | <span data-ttu-id="79b70-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="79b70-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="79b70-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="79b70-112">Delegated (work or school account)</span></span> | <span data-ttu-id="79b70-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="79b70-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="79b70-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="79b70-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="79b70-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79b70-115">Not supported.</span></span>    |
|<span data-ttu-id="79b70-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="79b70-116">Application</span></span> | <span data-ttu-id="79b70-117">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="79b70-117">Group.Read.All, Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="79b70-118">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="79b70-118">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="79b70-119">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="79b70-119">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="79b70-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79b70-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /teams/{id}
```
## <a name="request-headers"></a><span data-ttu-id="79b70-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="79b70-121">Request headers</span></span>
| <span data-ttu-id="79b70-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79b70-122">Header</span></span>       | <span data-ttu-id="79b70-123">Valor</span><span class="sxs-lookup"><span data-stu-id="79b70-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="79b70-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="79b70-124">Authorization</span></span>  | <span data-ttu-id="79b70-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="79b70-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="79b70-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="79b70-127">Content-Type</span></span>  | <span data-ttu-id="79b70-128">application/json</span><span class="sxs-lookup"><span data-stu-id="79b70-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="79b70-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="79b70-129">Request body</span></span>
<span data-ttu-id="79b70-130">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [equipo](../resources/team.md) .</span><span class="sxs-lookup"><span data-stu-id="79b70-130">In the request body, supply a JSON representation of [team](../resources/team.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="79b70-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79b70-131">Response</span></span>

<span data-ttu-id="79b70-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="79b70-132">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="79b70-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79b70-133">Example</span></span>
#### <a name="request"></a><span data-ttu-id="79b70-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79b70-134">Request</span></span>
<span data-ttu-id="79b70-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="79b70-135">The following is an example of the request.</span></span>
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
#### <a name="response"></a><span data-ttu-id="79b70-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79b70-136">Response</span></span>
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
