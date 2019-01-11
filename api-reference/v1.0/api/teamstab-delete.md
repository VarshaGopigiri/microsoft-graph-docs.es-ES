---
title: Eliminar ficha de canal
description: 'Quita (libera) una ficha desde el canal especificado dentro de un equipo. '
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 2373dd8a27a747fef031631deafc4d771e9cbf29
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811644"
---
# <a name="delete-tab-from-channel"></a><span data-ttu-id="ba5d0-103">Eliminar ficha de canal</span><span class="sxs-lookup"><span data-stu-id="ba5d0-103">Delete tab from channel</span></span>



<span data-ttu-id="ba5d0-104">Quita (libera) una ficha desde el [canal](../resources/channel.md) especificado dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="ba5d0-104">Removes (unpins) a tab from the specified [channel](../resources/channel.md) within a [team](../resources/team.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="ba5d0-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ba5d0-105">Permissions</span></span>
<span data-ttu-id="ba5d0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ba5d0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ba5d0-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ba5d0-108">Permission type</span></span>      | <span data-ttu-id="ba5d0-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ba5d0-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ba5d0-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ba5d0-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ba5d0-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ba5d0-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ba5d0-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ba5d0-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ba5d0-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-113">Not supported.</span></span>    |
|<span data-ttu-id="ba5d0-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ba5d0-114">Application</span></span> | <span data-ttu-id="ba5d0-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ba5d0-115">Group.ReadWrite.All</span></span> |

> <span data-ttu-id="ba5d0-116">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-116">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="ba5d0-117">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-117">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="ba5d0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ba5d0-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{id}/channels/{id}/tabs/{id}
```

## <a name="request-headers"></a><span data-ttu-id="ba5d0-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ba5d0-119">Request headers</span></span>
| <span data-ttu-id="ba5d0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba5d0-120">Header</span></span>       | <span data-ttu-id="ba5d0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ba5d0-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ba5d0-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="ba5d0-122">Authorization</span></span>  | <span data-ttu-id="ba5d0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ba5d0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ba5d0-125">Request body</span></span>
<span data-ttu-id="ba5d0-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ba5d0-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba5d0-127">Response</span></span>

<span data-ttu-id="ba5d0-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ba5d0-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba5d0-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="ba5d0-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ba5d0-131">Request</span></span>
<span data-ttu-id="ba5d0-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
DELETE https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
```
#### <a name="response"></a><span data-ttu-id="ba5d0-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba5d0-133">Response</span></span>
<span data-ttu-id="ba5d0-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-134">The following is an example of the response.</span></span> <span data-ttu-id="ba5d0-135">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-135">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="ba5d0-136">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-136">All of the properties will be returned from an actual call.</span></span>
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete tab from channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
